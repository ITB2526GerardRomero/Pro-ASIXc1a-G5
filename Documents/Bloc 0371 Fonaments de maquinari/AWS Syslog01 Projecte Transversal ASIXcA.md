Creació de la instancia:

| Configuració | Valor |
| :---- | :---- |
| Nom | logs01 |
| SO | Ubuntu Server 24.04 |
| Tipo | t3.micro |
| IP privada | 10.0.1.30 |
| Seguretat | Port 514 obert |

![Primera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog01.png)

Una vegada creades les claus pem., les guardem a la carpeta compartida del drive del grup i accedim a la maquina:

![Segona captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog02.png)

Ara instal·lem el servei que ens permetra realitzar els logs de tots els servidors:

![Tercera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog03.png)

Ara editem el fitxer de configuració de logs del servidor /etc/rsyslog.conf i descomentarem algunas líneas:

![Cuarta captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog04.png)

Ara crearem les carpetes per als logs remots en el fitxer /etc/rsyslog.d/remote.conf :

![5 captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog05.png)

Això fa:

- una carpeta per servidor.  
- logs separats automàticament.

Reiniciem el servei:

![Sisena captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog06.png)

Per a la comprovació caldra instalar el rsyslog en els servidors i en el fitxer /etc/rsyslog.conf afegir la linea *.* @10.0.1.30:514 i despres reiniciar client sudo systemctl restart rsyslog i finalment veure en el cd /var/log/remote web01/ ldap01/ db01/


Finalment creem l'usuari administracio:

![Sisena captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog08.png)
