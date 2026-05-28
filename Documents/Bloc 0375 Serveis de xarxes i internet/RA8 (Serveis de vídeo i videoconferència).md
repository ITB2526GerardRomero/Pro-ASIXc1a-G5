# 2.3 - Implantació del Servei de Vídeo i Videoconferència

**Funcionalitat del servei de vídeo:**

La funcionalitat que volem amb el servei de vídeo són varies, per exemple volem que:

- Els treballadors es puguin enviar vídeos en streaming entre si per poder veure com fan manteniment dels servidors.  
- Els treballadors puguin fer videoconferències en directe com a medida per fer una reunió en cas de que algu no estigui disponible.  
- Accés des de qualsevol navegador web.  
- Hi hagi compatibilitat amb videos moderns i antics, a part de que tinguin qualsevol tipus d'extensió.

Primer de tot crearem una altra instància en AWS, que serà el servidor de vídeo:

![Primera imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video01.png)

![Segona imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video02.png)

Ara instal·larem el servei web de Nginx:

![Tercera imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video03.png)

D'aquí començem la part de streaming. Instal·lant RTMP (Real-Time Messaging Protocol), que és qui ens permet poder fer la transmissió en directe desde l'aplicació dessitjada:

![Quarta imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video04.png)

Després d'això hem de configurar l'arxiu de configuració del Nginx per a que pugui utilitzar tant RTMP com HLS, el qual aquest últim ens permetrà poder observar el directe desde el navegador mitjançant un enllaç:

![Quinta imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video05.png)
![Sisena imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video06.png)

Una vegada feta la configuració anterior anem a una gravadora (OBS Studio) i a la part de directe com a servidor posem l'enllaç RTMP del nostre servidor, amb la clau test, que és a ón es guarden els troçets del directe:

![Setena imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video07.png)

Llavors al OBS Studio posem com a codificador el H264 i el format d'enregistrament com a MP4:

![11 imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video11.png)

Com hem configurat tot de manera correcta, no apareix cap error a l'hora de fer la transmissió i es pot fer sense cap problema:

![Vuitena imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video08.png)

Ara, si ens fiquem al següent enllaç (http://98.80.217.120:8080/hls/test.m3u8) podrem veure la transmissió en directe, cap aclarir que té un delay una mica gran entre el que passa i el que surt al navegador:

![Novena imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video09.png)

També si observem la carpeta on hem especificat anteriorment al bloc de RTMP, veurem com es creen els trossos de la transmissió:

![Dècima imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video10.png)

**Descripció del protocol de videoconferència:**

WebRTC (Web Real-Time Communication) és un protocol o projecte open source que ens permet tenir una connexió a video, audio i de metadata de manera real. Aquest projecte permet als usuaris conectarse principalment des de navegadors, encara això també aplicacions mòbils per instal·lar.

Al nostre cas utilitzarem l’eina Jitsi Meet que al igual que WebRTC és un eina de videoconferènia i missatgeria instantànea que conté protocols de missatgeria instantània i telefonia populars.

A l’hora d’instal·lar l’eina hem visitat la seva pàgina web per veure com instal·lar-ho:  
https://jitsi.org/downloads/ubuntu-debian-installations-instructions/

Ara per la part de videoconferència primer descarregarem el repositori jitsi des de la seva pàgina oficial i després li afegirem el repositori oficial al nostre ordinador:

![Instal jitsi imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video12.png)

Després instal·lem l'aplicació mitjançant apt:

![APT jitsi imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video13.png)

Ara el jitsi ens demana un nom que assigna a l'enllaç de les videoconferències, al nostre cas com no tenim un nom de domini ja que no tenim bind9 instal·lat li posem que sigui simplement la IP pública de la màquina:

![Nom jitsi imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video14.png)

Com utilitza HTTPS fiquem que encripti els certificats, no fiquem email ni número de telèfon, ja que no dispossem de cap:

![Encriptació jitsi imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video15.png)

![Email jitsi imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video16.png)

![Telèfon jitsi imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video17.png)

Ara verifiquem que funcionen les reunions si ens fiquem a l'adreça pertinent, com l'hem posat la IP elàstica com a nom de domini, al navegador també li posem la IP elàstica, amb això hem inclòs una prova des d'un telèfon mòbil per verificar que és multiplataforma:

![Verificiació jitsi imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video18.png)

**Comprovacions d'amplada de banda:**

Necessitarem instal·lar el servei de speedtest client per poder veure aixì la pujada i baixada en velocitat:

![Install speedtest](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video19.png)

Llavors primer anem a fer la verificació de la velocitat amb el Nginx desactivat, ja que és qui porta els serveis de streaming i videoconferència:

![Comprovació speedtest sense Nginx](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video20.png)

Verifiquem la latència:

![Ping](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video21.png)

Per últim, anem a verificar la pujada i baixada amb els serveis actius, i mentre fa una transmissió:

![Comprovació speedtest amb Nginx](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video22.png)

Amb aquestes dades hem arribat a la conclusió de que el sistema és acceptable per a una petita empresa. En canvi, no es pot utilizar per a sistemes que ocupin gran quantitat de recursos, ja que es faria inestable.

Algunes millores a incorporas per a una empresa poden ser:
- Segementació de la xarxa.
- Millora del hardware.
- Una connexió multioperadora.
