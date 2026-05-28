# 2.2 - Implantació del Servei d'Àudio
**Descripció del servei:**

El servei d’àudio implementat permet la transmissió de contingut multimèdia en temps real mitjançant tecnologia de streaming.

Aquest sistema permet:

- Reproduir àudio remotament.
- Acedir des d’un navegador web.
- Centralitzar emissions d’àudio.
- Distribuir contingut multimèdia a diferents clients simultàneament.
  
**Funcionament del servei:**

El servidor d’àudio funciona utilitzant un sistema de streaming basat en Icecast2.

Client emissor → Servidor Icecast2 → Clients receptors
1. Un client emissor envia l’àudio al servidor.
2. El servidor Icecast2 rep el flux d’àudio.
3. Els usuaris poden connectar-se mitjançant navegador web o reproductors multimèdia.
4. El servidor distribueix l’àudio en temps real.

L’accés al servidor es realitza mitjançant:

- Autenticació d’usuaris.
- Contrasenyes configurades al servidor Icecast2.
- Administració remota segura mitjançant SSH amb claus públiques/privades.

Validació del servei:

- Emissió correcta d’àudio.
- Connexió de clients remots.
- Reproducció des de navegador web.
- Verificació de l’estabilitat del streaming.

La implementació del servei d’àudio permet:

- Centralitzar emissions multimèdia.
- Reduir costos d’infraestructura.
- Facilitar la distribució d’àudio.
- Millorar l’accessibilitat dels continguts.

Dades de la instancia:

| Configuración | Valor |
| ----- | ----- |
| Nombre | audio01 |
| SO | Ubuntu Server 24.04 |
| Tipo | t3.micro |
| Storage | 15 GB |
| Security Group | HTTP \+ SSH \+ 8000 |

Creació de la instància:

![Primera captura](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio01.png)

Accedim a ella:

![Primera captura](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio02.png)

Creació usuari "administracio":

![Primera captura](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio03.png)

Instal·lar Icecast2:

![Primera captura](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio04.png)

Realitzem la següent configuració al servei:

![Primera captura](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio05.png)

![Primera captura](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio06.png)

![Primera captura](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio07.png)

![Primera captura](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio08.png)

Funcionament del servei:

![Primera captura](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio09.png)

Per enviar l’audio a la pàgina instal·larem el servei ffmpeg:

![Primera captura](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio10.png)

Una vegada descarregat el mp3, utilitzarem la commanda següent indicant el audio a utilitzar, la direcció de la pàgina i les credencials del usuari que permet pujar l’audio:

![Primera captura](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio11.png)

Comprovació de que es pot escoltar l’audio desde la ruta:

![Primera captura](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio12.png)

Execució de la comanda:

![Primera captura](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio13.png)

# Amplada de banda

## **Objectiu**

Analitzar el rendiment de xarxa disponible per comprovar si la infraestructura implementada és adequada per suportar els serveis multimèdia del projecte, especialment el servei d’àudio en streaming implementat amb Icecast2.

# **Proves de velocitat realitzades**

Instal·lació del servei 'speedtest-cli':

![Primera captura](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio14.png)

La prova es va executar directament des del servidor AWS EC2 on està implementat el servei d’àudio.

![Primera captura](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio15.png)

# **Resultats obtinguts:**

| Paràmetre | Resultat |
| ----- | ----- |
| Download | 1949.06 Mbit/s |
| Upload | 1869.21 Mbit/s |
| Latència | 6.502 ms |

# **Anàlisi dels resultats**

Els resultats obtinguts mostren un rendiment de xarxa molt elevat i una latència extremadament baixa.

La velocitat de descàrrega i pujada supera àmpliament els requisits necessaris per al servei d’àudio implementat.

El servei de streaming configurat utilitza codificació MP3 amb un bitrate aproximat de 128 kbps (0.128 Mbps).

Comparant aquest consum amb l’ample de banda disponible, es pot concloure que el consum del servei és pràcticament insignificant respecte a la capacitat disponible de la infraestructura AWS. La latència és de 6.5 ms.

| Element | Consum aproximat |
| ----- | ----- |
| Streaming d’àudio | 0.128 Mbps |
| Upload disponible | 1869 Mbps |

És excel·lent per serveis en temps real i garanteix una reproducció estable sense talls ni interrupcions.

El servei d’àudio és el menys exigent en consum d’amplada de banda. El bitrate utilitzat permet reproducció estable fins i tot en connexions modestes.

## **Classificació del sistema:**

La infraestructura implementada es considera plenament acceptable per oferir:

* Streaming d’àudio.  
* Serveis multimèdia.  
* Comunicacions en temps real.

Els resultats obtinguts garanteixen estabilitat i qualitat suficient per múltiples clients connectats simultàniament.

# **Propostes d’optimització**

Tot i els bons resultats obtinguts, es proposen les següents millores:

- Implementació de QoS per prioritzar tràfic multimèdia.  
- Utilització de compressió MP3 eficient.  
- Reducció del bitrate en connexions lentes.  
- Ús de connexions cablejades per reduir latència.  
- Balanceig de càrrega per suportar múltiples clients simultanis.  
- Monitorització contínua de l’ample de banda i latència.
