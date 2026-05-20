Bloc 0375 Serveis de xarxes i internet

· Funcionalitat del servei de vídeo:

La funcionalitat que volem amb el servei de vídeo són varies, per exemple volem que:

- Els treballadors es puguin enviar vídeos entre si per poder veure com fan manteniment dels servidors.  
- Els treballadors puguin fer videoconferències en directe com a medida per fer una reunió en cas de que algu no estigui disponible.  
- Accés des  de qualsevol navegador web.  
- Hi hagi compatibilitat amb videos moderns.

Primer de tot crearem una altra màquina amb Ubuntu, que serà el servidor de video:

![Primera imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video01.png)

I, al igual que les altres màquines, li crearem un nou par de claus:

![Segona imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video02.png)

Ara per necessitat de la pràctica instal·lem el servei web de Nginx:

![Tercera imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video03.png)

Ara és quan començem amb la part de streaming. Principalment instalant el RTMP (Real-Time Messaging Protocol), que és qui ens permet poder fer la transmissió en directe desde l'aplicació dessitjada:

![Quarta imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video04.png)

I després d'això hem de configurar l'arxiu de configuració del Nginx per a que pugui utilitzar tant el RTMP, com el HLS, el qual aquest ultim ens permetrà poder observar el directe desde el navegador mitjançant uns petits troçets amb l'extensió m3u8:

![Quinta imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video05.png)
![Sisena imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video06.png)

Després d'haver configurat l'anterior ens anem a una gravadora, al nostre cas, el OBS Studio, y a la part de directe com a servidor posem l'enllaç RTMP del nostre servidor, amb la clau test, que és a ón es guarden com a tal els trosets d'aquell directe:

![Setena imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video07.png)

I demanat per la pràctica, al programa del OBS Studio, o el que sigui de gravació, i posem com a codificador el H264 i el format d'enregistrament com a MP4:

![11 imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video11.png)

Com hem configurat tot de manera correcta, no ens surt cap error a la hora de fer la transmissió i la podrem fer sense cap problema:

![Vuitena imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video08.png)

I ara si ens fiquem al següent enllaç (http://98.80.217.120:8080/hls/test.m3u8) podrem veure la transmissió en directe, cap aclarir que té un retard molt gran entre el que passa i el que surt al navegador:

![Novena imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video09.png)

També si observem la carpeta on hem especificat l'arxiu a on hem posat els arxius podem veure que s'han creat els diferents arxius:

![Dècima imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video10.png)

· Descripció del protocol de videoconferència:

WebRTC (Web Real-Time Communication) és un protocol o projecte open source que ens permet tenir una connexió a video, audio i de metadata de manera real. Aquest projecte permet als usuaris conectarse principalment des de navegadors, encara això també aplicacions mòbils per instal·lar.

Al nostre cas utilitzarem l’eina Jitsi Meet que al igual que WebRTC és un eina de videoconferènia i missatgeria instantànea que conté protocols de missatgeria instantània i telefonia populars.

A l’hora d’instal·lar l’eina hem visitat la seva pàgina web per veure com instal·lar-ho:  
https://jitsi.org/downloads/ubuntu-debian-installations-instructions/

Ara per a la part de videoconferència primer descarregarem el repositori jitsi des de la seva pàgina oficial i després li afegirem el repositori oficial al nostre ordinador:

![Instal jitsi imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video12.png)

Després instal·lem l'aplicació mitjançant apt:

![APT jitsi imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video13.png)

Ara el jitsi ens demana un nom de domini a la que posar, per a la hora de buscar la reunió pel navegador, tenir una mena de identificador, al nostre cas com no tenim un nom de domini ja que no tenim bind9 instal·lat, li posem que sigui simplement la IP pública de la màquina:

![Nom jitsi imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video14.png)

I com utilitza HTTPS li donem que encripti els certificats, no posem email i ni tampoc número de telèfon:

![Encriptació jitsi imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video15.png)

![Email jitsi imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video16.png)

![Telèfon jitsi imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video17.png)

I ara podrem verificar que funcionen les reunions si ens fiquem a l'adreça pertinent, com l'hem posat la IP elàstica al navegador també li posem la IP elàstica, també hem fet una prova des de el telèfon mòbil per veure que ens podem ficar des de un tercer:

![Verificiació jitsi imatge video](../../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video18.png)
