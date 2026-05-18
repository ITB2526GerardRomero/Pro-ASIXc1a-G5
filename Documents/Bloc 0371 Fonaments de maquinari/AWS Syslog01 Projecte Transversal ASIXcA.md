Creació de la instancia:

| Configuració | Valor |
| :---- | :---- |
| Nom | logs01 |
| SO | Ubuntu Server 24.04 |
| Tipo | t3.micro |
| IP privada | 10.0.1.30 |
| Seguretat | Port 514 obert |

![Primera captura](../../Imatges/syslog01.png)

Una vegada creades les claus pem., les guardem a la carpeta compartida del drive del grup i accedim a la maquina:

![Segona captura](../../Imatges/syslog02.png)

Ara instal·lem el servei que ens permetra realitzar els logs de tots els servidors:

![Tercera captura](../../Imatges/syslog03.png)

Ara editem el fitxer de configuració de logs del servidor /etc/rsyslog.conf i descomentarem algunas líneas:

![Cuarta captura](../../Imatges/syslog04.png)

Ara crearem les carpetes per als logs remots en el fitxer /etc/rsyslog.d/remote.conf :

![5 captura](../../Imatges/syslog05.png)

Això fa:

- una carpeta per servidor.  
- logs separats automàticament.

Reiniciem el servei:

![Sisena captura](../../Imatges/syslog06.png)
