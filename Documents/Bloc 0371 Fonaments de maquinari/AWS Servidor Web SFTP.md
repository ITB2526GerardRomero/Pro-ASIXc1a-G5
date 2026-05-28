## Implementació al núvol AWS - Web/SFTP

En primer lloc crearem un grup de seguretat que permeti tot el tràfic, per poder connectar-nos a la nostra pròpia instància:

![Primera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web01.png)

I comencem a crear la instància amb el nom pertinent: 

![Segona captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web02.png)

Aquestes seran les següents característiques:

![Tercera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web03.png) 

![Quarta captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web04.png)

![Quinta captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web05.png)

Tot seguit a això fem SSH per ficar-nos a la instància i li cambien el hostname per poder identificarla de manera fàcil:  

![Sexta captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web06.png)

Ara que ens hem ficat, crearem l'usuari "administracio" i tot seguit li canviem la contrasenya i li afegim al grup root: 

![Septima captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web07.png)

I les claus de l’usuari Ubuntu les copiem a la home de l'usuari “administracio”, ja que a partir d’ara ens ficarem a aquest:  

![Dècima captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web08.png)

Comprovació que es pot accedir:

![Decimaprimera captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web09.png)

## Instal·lació de nginx:  

![Decimasegona captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web12.png)

![Tretzena captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web13.png)

Comprovació de SFTP:

![Catorzena](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web14.png)

Podem veure que SFTP ve per defecte a la instància

Verifiquem que NGINX funciona correctament ficant l'enllaç públic:

![Quinzena](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web15.png)
 
### Instal·lació de vsftpd i clients LDAP

S'instal·la els paquets necessaris per integrar la màquina amb LDAP: `libnss-ldap`, `libpam-ldap`, 'ldap-utils' i per últim 'nslcd'. Aquests paquets permeten que el servidor web conegui els usuaris del LDAP i pugui autenticar els usuaris contra el directori LDAP d'InnovateTech, i el 'nslcd' és qui permet que hi hagi una connexió.

![bdldap01](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap01.png)

## Configuració de LDAP
 
A l'hora d'instal·lar els paquets anteriors, hem hagut de configurar un par de coses, com la direcció del servei LDAP, i els dc del domini:
 
![bdldap01](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap02.png)
![bdldap01](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap03.png)
 
Es configura el client LDAP apuntant al servidor del directori actiu:
 
```
URI ldap://52.0.2.63
BASE dc=innovatetech,dc=local
```

Això permet que qualsevol servei del sistema (vsftpd, SSH, web) resolgui usuaris contra el servidor LDAP d'InnovateTech.

### VSFTPD i fitxer `/etc/pam.d/vsftpd`

Després d'haver configurat el necessari per el LDAP instal·lem el VSFTP i el configurem per a que s'apigui que ha d'agafar l'autenticació i les comptes del LDAP: 
 
![bdldap01](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap04.png)
![bdldap01](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap05.png)
 
### Fitxer `/etc/nsswitch.conf`
 
![bdldap01](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap06.png)
 
Es modifica el fitxer de resolució de noms del sistema per consultar LDAP:
 
```
passwd:  files systemd ldap
group:  files systemd ldap
shadow: ldap
```
 
Això garanteix que el sistema busqui els usuaris tant en fitxers locals com al servidor LDAP.
 
## Verificació de la integració LDAP
 
### Consulta de tots els usuaris del directori i resolució d'usuaris
 
![bdldap01](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap07.png)
 
S'executa `ldapsearch` des del servidor web per verificar la connectivitat i llistar tots els usuaris del directori LDAP. Es confirma que els 4 usuaris del grup GEDE estan correctament creats a `ou=usuaris,dc=innovatetech,dc=local`:
 
- `uid=elian` — Elian Salvador
- `uid=gerard` — Gerard Romero
- `uid=daniel` — Daniel Roblas
- `uid=elias` — Elias Martinez
 
Això confirma que `nslcd` funciona correctament i el sistema operatiu reconeix els usuaris del directori LDAP.
 
## Instal·lació de PHP i Nginx
 
### Instal·lació de PHP, php-fpm, php-mysql i php-ldap
 
![bdldap01](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap08.png)
 
S'instal·la **PHP** amb el mòdul `php-fpm` per processar fitxers PHP a través de Nginx. El sistema instal·la automàticament totes les dependències necessàries.
 
S'instal·len les extensions PHP necessàries per a l'aplicació web:
 
- **php-mysqli** — per connectar amb la base de dades MySQL d'InnovateTech.
- **php-ldap** — per autenticar els usuaris contra el servidor LDAP.
 
## Configuració de Nginx
 
### Fitxer `/etc/nginx/sites-available/default`
 
![bdldap01](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap09.png)
 
Es configura Nginx per processar fitxers PHP via FastCGI, apuntant al socket de `php-fpm`:
 
```nginx
location ~ \.php$ {
   include snippets/fastcgi-php.conf;
   fastcgi_pass unix:/run/php/php8.3-fpm.sock;
}
```
 
## Desplegament de l'aplicació web
 
### Fitxers de l'aplicació
 
![bdldap01](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap10.png)
![bdldap01](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap11.png)
![bdldap01](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap12.png)
![bdldap01](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap13.png)
 
Es creen els 4 fitxers PHP que formen l'aplicació de gestió d'InnovateTech:
 
| Fitxer | Funció |
|---|---|
| `index.php` | Redirigeix a `login.php` |
| `login.php` | Autenticació d'usuaris via LDAP |
| `dashboard.php` | Interfície principal amb les 14 taules de la BBDD |
| `logout.php` | Tancament de sessió |
 
## Resultat final
 
### Pantalla de login
 
![bdldap01](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap14.png)
 
Pantalla d'accés de l'aplicació web accessible des de `http://3.210.137.51`. L'autenticació es realitza contra el servidor LDAP d'InnovateTech (`ldap://52.0.2.63`). Els usuaris s'autentiquen amb les seves credencials del directori actiu.
 
### Dashboard principal
 
![bdldap01](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap15.png)
 
Un cop autenticat, l'usuari accedeix al dashboard principal que mostra:
 
- **Estadístiques en temps real** de les 6 taules principals: 10 empleats, 4 clients, 5 productes, 5 comandes, 15 trucades, 6 vídeos.
- **Sidebar de navegació** amb les 14 taules organitzades en 4 seccions: Recursos Humans, Comercial, Comunicació i Sistema.
- **Nom i estat de l'usuari** autenticat (Gerard — En línia).
- **Resum tècnic** del sistema: MySQL 8.0, AWS EC2, estat Operatiu, autenticació OpenLDAP.
La base de dades es troba en un servidor AWS EC2 separat (`32.192.128.228`) i totes les dades es mostren en temps real.

## AWS Syslog

Creació de la instancia:

| Configuració | Valor |
| :---- | :---- |
| Nom | logs01 |
| SO | Ubuntu Server 24.04 |
| Tipo | t3.micro |
| IP privada | 10.0.1.30 |
| Seguretat | Port 514 obert |

![Primera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog01.png)

Una vegada creades les claus .pem:

![Segona captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog02.png)

Ara instal·lem el servei que ens permetrà realitzar els logs de tots els servidors:

![Tercera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog03.png)

Ara editem el fitxer de configuració de logs del servidor /etc/rsyslog.conf:

![Cuarta captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog04.png)

Ara crearem les carpetes pels logs remots en el fitxer /etc/rsyslog.d/remote.conf:

![5 captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog05.png)

Això fa:

- Una carpeta per a cada servidor.  
- Logs separats automàticament.

Reiniciem el servei:

![Sisena captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog06.png)

Per a la comprovació caldrà instalar el rsyslog en els servidors i en el fitxer /etc/rsyslog.conf afegir la linea *.* @18.212.86.171:514 i despres reiniciar client, 'sudo systemctl restart rsyslog' i finalment veure al directori que hem configurat, ho podem fer amb 'cd /var/log/remote/' i per a cada servidor 'web01/', 'ldap01/', 'db01/'.


Creació usuari "administracio":

![Sisena captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog08.png)

Comprovació del funcionament dels logs:

![Sisena captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog09.png)
