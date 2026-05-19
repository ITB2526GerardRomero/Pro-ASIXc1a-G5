Dades de la instancia:

| Configuración | Valor |
| ----- | ----- |
| Nombre | audio01 |
| SO | Ubuntu Server 24.04 |
| Tipo | t3.micro |
| Storage | 15 GB |
| Security Group | HTTP \+ SSH \+ 8000 |

Creció de la instancia:

![][image1]

Accedim a ella:

![][image2]

Creació usuari administració:

![][image3]

INSTALAR ICECAST2:

![][image4]

Editem el fitxer de configuració del servei per a configurar el servei:

Contrasenyas:

![][image5]

CAMBIAR HOSTNAME:

![][image6]

ACTIVAR ICECAST:

![][image7]

![][image8]

Funcionament del servei:

![][image9]

Ara obrim el VLC de l’ordinador, obrim la configuracio de flux, seleccionem un arxiu mp3 i configurem la seva emissio:

![][image10]

Ara podem veure com es reprodueix l’audio del VLC al Icecast del servidor via web:

![][image11]

També podem veure dades dels escoltadors:

![][image12]
