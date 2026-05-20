Descripció del servei:

El servei d’àudio implementat permet la transmissió de contingut multimèdia en temps real mitjançant tecnologia de streaming.

Aquest sistema permet:

reproduir àudio remotament,
accedir des d’un navegador web,
centralitzar emissions d’àudio,
distribuir contingut multimèdia a diferents clients simultàniament.
Funcionament del servei

El servidor d’àudio funciona utilitzant un sistema de streaming basat en Icecast2.

El funcionament és el següent:

Client emissor → Servidor Icecast2 → Clients receptors
Un client emissor envia l’àudio al servidor.
El servidor Icecast2 rep el flux d’àudio.
Els usuaris poden connectar-se mitjançant navegador web o reproductors multimèdia.
El servidor distribueix l’àudio en temps real.

Seguretat i administració

L’accés al servidor es realitza mitjançant:

autenticació d’usuaris,
contrasenyes configurades al servidor Icecast2,
administració remota segura mitjançant SSH amb claus públiques/privades.
Validació del servei

Es van realitzar proves funcionals:

emissió correcta d’àudio,
connexió de clients remots,
reproducció des de navegador web,
verificació de l’estabilitat del streaming.
Beneficis del sistema

La implementació del servei d’àudio permet:

centralitzar emissions multimèdia,
reduir costos d’infraestructura,
facilitar la distribució d’àudio,
millorar l’accessibilitat dels continguts.

Dades de la instancia:

| Configuración | Valor |
| ----- | ----- |
| Nombre | audio01 |
| SO | Ubuntu Server 24.04 |
| Tipo | t3.micro |
| Storage | 15 GB |
| Security Group | HTTP \+ SSH \+ 8000 |

Creció de la instancia:

![Primera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio01.png)

Accedim a ella:

![Primera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio02.png)

Creació usuari administració:

![Primera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio03.png)

INSTALAR ICECAST2:

![Primera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio04.png)

Editem el fitxer de configuració del servei per a configurar el servei:

Contrasenyas:

![Primera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio05.png)

CAMBIAR HOSTNAME:

![Primera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio06.png)

ACTIVAR ICECAST:

![Primera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio07.png)

![Primera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio08.png)

Funcionament del servei:

![Primera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio09.png)

Per a enviar l’audio a la pàgina utilitza el servei ffmpeg.

Instal·lació:

![Primera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio10.png)

Una vegada descarregat el mp3, utilitzem la comanda següent indicant el audio la direcció de la pàgina i les credencials del usuari que permet pujar l’audio.

![Primera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio11.png)

Comprovació de que es pot escoltar l’audio desde la ruta

![Primera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio12.png)

Execució de la comanda:

![Primera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio13.png)
