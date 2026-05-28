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

![Sisena captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog09.png)
