# Projecte Transversal ASIXc - Innovate Tech

Aquest document unifica les diferents fases del projecte de transformació tecnològica i modernització per a l'empresa **Innovate Tech**. L'objectiu principal és proporcionar una base tecnològica sòlida que integri la infraestructura de maquinari i els serveis de xarxa per millorar la capacitat operativa i comunicativa de l'empresa.

---

## 1. Fonaments de Maquinari i Proposta de CPD (Bloc 0371)

Per tal de garantir la continuïtat del negoci i donar suport als serveis multimèdia, la primera fase del projecte se centra en el disseny i implementació d'un Centre de Processament de Dades (CPD) eficient, segur i sostenible.

### 1.1 Ubicació i Infraestructura Física

**Ubicació Física del CPD - Innovate Tech**

**1. Situació de la sala a l’edifici**

*Innovate Tech* és una empresa de consultoria tecnològica i desenvolupament de programari:
- 50-80 empleats.
- 4 departaments distribuïts en: Vendes, Suport tècnic, Administració i Logística.
- Serveis que ofereix: Desenvolupament de programari personalitzat, consultoria cloud, formació tècnica.
- Clients: Són petites i mitjanes empreses (PIMES) o startups (empreses noves).

**On estem ubicats?** Tenim la seu al **Districte 22@, Barcelona**, concretament en un edifici d’oficines de 4 plantes més un soterrani. Aquest districte és la zona d'innovació tecnològica de Barcelona, on es concentren startups, consultores Tech i empreses de serveis digitals.

**Ubicació del CPD** El CPD s'ubicarà al soterrani (planta -1), on ocuparà uns **48m² (8m x 6m)** amb una alçada lliure de **3,5 metres**.

Hem escollit el soterrani per diverses raons:
- **Temperatura estable:** Al soterrani, la temperatura varia només ±2°C durant tot l’any, gràcies a l'**aïllament natural del subsol**. En una planta superior la variació seria més alta, ja que intervenen diferents factors com el sol, el vent, els canvis d’estació, etc. Amb això fem que el sistema d’aire condicionat treballi menys per mantenir la temperatura adequada, aconseguint menys consum energètic i sent més sostenibles.
- **Protecció contra fenòmens meteorològics:** El CPD no tindrà finestres, llavors no hi ha risc de trencaments pel temps meteorològic, a més de no tenir exposició directa al vent, pluja o neu. En el cas de possible inundació urbana, el soterrani té sensors d'aigua connectats a l'alarma.
- **Seguretat física:** Accés difícil des de l’exterior, ja que no té finestres ni portes directes al carrer. L’únic accés és per l'interior de l'edifici, passant pel control d’accés principal, reduint així el risc de vandalisme o intrusió.
- **Aïllament acústic:** El sistema d’aire condicionat fa soroll (50-70dB). Al soterrani, aquest soroll no afecta les oficines de les plantes superiors ni els veïns; els empleats poden treballar tranquils.

**2. Sistemes de climatització (aire condicionat). Nivells de temperatura, humitat i neteja de l’aire.**

Hem instal·lat **2 unitats CRAC** (Computer Room Air Conditioning) de 10kW cadascuna. No hem escollit un aire condicionat domèstic, ja que aquests mantenen la temperatura amb una precisió de ±3°C, mentre que un CRAC professional la manté en ±1°C. És de gran importància escollir l’opció correcta ja que els servidors són sensibles; si la temperatura puja a 30°C, el servidor es pot apagar automàticament per protegir-se. En una empresa que ofereix servei 24/7 als clients, una apagada de servidors és sinònim de pèrdues de diners i reputació.

Hem col·locat 2 unitats:
- 1 CRAC actiu tot el temps, cobrint els 3,5kW que generen els nostres servidors.
- 1 CRAC en standby; en cas que falli el primer, el segon s’activa automàticament en menys de 30 segons.

**Temperatura objectiu:** **22°C** (el rang permès: 18-27°C segons la normativa **ASHRAE TC 9.9**). Hem especificat els 22°C ja que cada grau per sota incrementa el consum elèctric un 4%. En el cas de configurar el CPD a 18°C (4°C menys):
- Consum extra: 4°C x 4% = 16% més d'electricitat.
- Cost anual extra: ~1.200€.
- Impacte ambiental: +1,5 tones de CO₂/any.
En conclusió, mantenir el CPD a 22°C és l’equilibri perfecte entre seguretat tèrmica i eficiència energètica.

**Humitat relativa:** un 50% (rang permès: 46-60%). La humitat és molt important:
- Si és **inferior al 40%**: L’aire és massa sec, es genera electricitat estàtica i es poden espatllar components electrònics a causa d’espurnes.
- Si és **superior al 60%**: L’aire està massa humit, es forma condensació generant gotes d’aigua (aigua + electricitat = curtcircuit).
El nostre CRAC té un humidificador/deshumidificador integrat que s'ajusta automàticament.

Per a la **neteja de l’aire**, tenen filtres **HEPA H13** (retenen el 99,95% de partícules de 0,3 micres o més grans). És de molta importància tenir un aire net, ja que la pols s’acumula en els ventiladors i dissipadors dels servidors actuant com a aïllant tèrmic:
- Canviem els filtres cada 6 mesos.
- Els servidors es mantenen nets durant 2-3 anys sense necessitat d’obrir-los.
- Allarguem la seva vida útil un 40%.

**Configuració del passadís fred/calent:**
Els dos racks estan col·locats cara a cara creant:
- Passadís fred: La part frontal dels racks, on el CRAC impulsa l’aire fred.
- Passadís calent: La part posterior dels racks, on s’acumula l’aire calent que expulsen els servidors.
La funció del CRAC és aspirar l’aire calent del passadís posterior, refredar-lo i tornar-lo a impulsar al passadís frontal. Utilitzant aquest model, l’aire fred no es barreja amb el calent, i el CRAC treballa de forma eficient = estalviant un 30-40% en refrigeració.

**3. Mesures per dificultar la identificació de la sala.**

Fora de l'edifici:
- No col·locar cartells informatius.
- Les reixetes de ventilació del CRAC que donen a l’exterior han de tenir el mateix disseny que la resta de ventilació general de l'edifici.

Dins de l’edifici:
- La porta del CPD ha d'estar sense identificar.
- Mateix model que la resta de portes de l’edifici.
- Que la sala no aparegui en els plànols d'evacuació públics, només en documentació interna restringida.
Això es fa per dificultar possibles atacs d'enginyeria social, a més de complir amb la normativa ENS que obliga a no divulgar la ubicació d'instal·lacions crítiques.

**4. Distribució i gestió del cablejat**

Al CPD tenim dos tipus de cables:
- **Cables de dades (blaus):** Connecten servidors, switches i sortida a internet. Utilitzen Coure Cat 6A o Fibra òptica OM4 en cas de connectar amb un altre edifici.
- **Cables elèctrics (negres):** Connecten servidors, PDU i SAI.

Per normativa (TIA-942), els cables de dades i elèctrics hauran de tenir una separació mínima de 30cm, ja que els cables elèctrics generen camps electromagnètics i podrien produir errors de transmissió, paquets corruptes o latència. A més, és important que cada cable tingui una etiqueta als dos extrems per identificar quin és el seu origen i el seu destí.

**5. Terra tècnic i sostre tècnic.**

- **Terra tècnic:** És un fals terra elevat uns 60 cm damunt del terra real. Per aquest espai passen els cables elèctrics i l’aire fred que expulsa el CRAC. Ajuda a prevenir accidents.
  - *Components:* Sòl real (formigó original), Estructura metàl·lica (potes ajustables de 60 cm), Panells (plaques d’acer galvanitzat de 60x60 cm) i Reixetes (per on surt l’aire fred).
- **Sostre tècnic:** És una estructura suspesa a uns centímetres per sota del sostre original, a uns 3 metres sobre el terra tècnic. Recull l’aire calent (que puja per ser més lleuger) perquè el CRAC l'aspiri. També hi passen els cables de dades.
  - *Components:* Panells modulars d’alumini ignífug, amb classificació M0 (material no combustible).

**6. Planells, dibuixos i diagrames de l'espai.**

**Plànol de planta del CPD**
![Plànol de planta del CPD](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/planta-cpd.png)
Vista superior de la sala mostrant la disposició dels 2 racks en configuració passadís fred/calent, les 2 unitats CRAC i la porta d'accés.

**Tall lateral - flux d'aire**
![Tall lateral - flux d'aire](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/flux-aire.png)
Cicle complet de refrigeració mostrant com l'aire fred surt del terra tècnic, passa pels servidors, i torna al CRAC pel sostre tècnic.

**Distribució del cablejat**
![Distribució del cablejat](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/cablejat.png)
Separació física de 50 cm entre el cablejat de dades (sostre tècnic) i el cablejat elèctric (terra tècnic).

**7. Estructuració dels racks.**

![Vista frontal dels racks](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/racks-frontal.png)

Hem instal·lat 2 racks de 42U del model APC NetShelter SX (600 mm d’ample exterior, interior de 19 polzades, 1.070 mm de fons, suporten 1.360 kg, portes perforades i pany).
Cada rack té:
1. **PDU intel·ligent (1U, part inferior):** Monitorització de consum elèctric individual.
2. **Organitzadors de cables (1U entre zones):** Mantenen el cablejat ordenat.
3. **Panells cecs:** Bloquegen el pas d'aire per les U no ocupades.
4. **Sensors de temperatura i humitat:** Connectats al sistema de monitorització.
5. **Patch panels (part superior):** On acaben els cables de dades.

*Seguretat física dels racks:* Pany amb clau física en portes frontal i posterior; claus en caixa de seguretat externa amb control d'accés i registre d'obertures.
*Normatives:* ANSI/EIA-310-D, TIA-942, ISO/IEC 11801.

---

### 1.2 Infraestructura IT i Elèctrica

A continuació es descriu la infraestructura IT proposada per al CPD d'Innovate Tech.

#### Estructura General
El CPD disposa d'una superfície organitzada en:
- Zona principal de racks de servidors.
- Zona de control i monitoratge.
- Sistemes de climatització redundants.
- Passadissos optimitzats per a manteniment i flux d'aire.

#### Maquinari IT: Servidors

| Servidor | Funció | Model Proposat | CPU | RAM | Emmagatzematge |
| --- | --- | --- | --- | --- | --- |
| WEB-SFTP | Web + SFTP | Dell PowerEdge R350 | 4 vCPU | 8 GB | 250 GB SSD |
| LDAP-AD | Directori Actiu | Dell PowerEdge R350 | 4 vCPU | 8 GB | 250 GB SSD |
| LOGS | Centralització de logs | HPE ProLiant DL360 | 4 vCPU | 16 GB | 500 GB SSD |
| AUDIO | Streaming d'àudio | Dell PowerEdge R250 | 2 vCPU | 4 GB | 120 GB SSD |
| VIDEO | Streaming de vídeo | HPE ProLiant DL380 | 8 vCPU | 16 GB | 1 TB SSD |
| JITSI | Videoconferències | Dell PowerEdge R550 | 8 vCPU | 16 GB | 500 GB SSD |
| DATABASE | Base de dades | HPE ProLiant DL360 | 8 vCPU | 32 GB | RAID 1 SSD |
| ANSIBLE | Automatització | Dell PowerEdge R250 | 2 vCPU | 4 GB | 120 GB SSD |

#### Patch Panels i Switches
S'utilitzaran patch panels Cat6A per a la distribució estructurada del cablejat:
- 4 Patch Panels Cat6A (24 ports RJ45)
- 2 Patch Panels Fibra (LC-LC multimode)
- 8 Organitzadors de cable
Això permet l'organització del cablejat estructurat, redueix interferències, facilita el manteniment i separa la xarxa de dades de l'administració.

La infraestructura de xarxa utilitza switches gestionables de nivell empresarial (QoS, STP/RSTP, VLANs separades):
- **Core Switch:** Cisco Catalyst 9200 (48 ports) - Backbone principal.
- **Switches de Racks:** Cisco CBS350 (24 ports) - Servidors producció i serveis multimèdia.
- **Switch Gestió:** TP-Link JetStream (16 ports) - Administració.

#### Infraestructura Elèctrica: Sistemes Redundants i SAI

**Càlcul d’energia:**
- 8 servidors x 200W = 1600W
- Switches = 150 W
- Firewall = 100 W
- NAS/backup = 400 W
**Total estimat = 2600W**

**Elecció de l'autonomia i del SAI:**
L'objectiu és mantenir el CPD funcionant després d’un tall elèctric durant almenys 20 minuts (temps suficient per a una apagada controlada o l'entrada del generador).
- **SAI principal:** APC Smart-UPS 3000VA (Capacitat ~2700W).
- **Autonomia:** ~20-25 minuts a càrrega mitjana.
- **Bateries:** 2 mòduls de bateries redundants (1 SAI principal + pack d'expansió).

---

### 1.3 Seguretat Física, Lògica i Prevenció de Riscos

#### Seguretat Física
Implica tenir el lloc vigilat 24/7 i sistemes de protecció contra accidents:
- **Control d’accés al CPD:** Entrada restringida mitjançant claus físiques, targetes especials d’identificació o un factor de doble autenticació per a personal autoritzat.
- **Videovigilància:** Càmeres de seguretat per rastrejar accessos i activitats. S'utilitzen miralls convexos per eliminar els punts cecs.
- **Detecció i extinció d’incendis:** Control de temperatura i humitat, detectors de fum i calor d’alta sensibilitat. Extintors de CO2 (els únics recomanats per apagar incendis elèctrics).
- **Vies d’evacuació:** Sortida d’emergència ubicada a l'extrem oposat de la sala, lliure d'obstacles i allunyada dels servidors principals.

#### Seguretat Lògica
La informació als servidors és vital, per tant s'apliquen polítiques rigoroses:
- **Restricció d’accés:** Només usuaris autoritzats tenen accés lògic als sistemes, basat en el principi de mínims privilegis.
- **Firewalls:** Filtració estricta de ports i protocols, permetent només l'accés des d'equips o IP específiques.
- **Monitorització:** Sistemes de recull de logs i alertes per detectar i notificar problemes de rendiment o atacs al moment.
- **Còpies de seguretat:** Còpia de seguretat base cada cap de setmana (diumenge) i còpies diferencials diàries.
- **RAID:** Ús de configuracions com RAID 0+1 (o RAID 1 per bases de dades) per assegurar rendiment i tolerància a fallades ràpida.

#### Prevenció de Riscos Laborals i Sostenibilitat
- **Riscos elèctrics:** Ús de terra i roba aïllant d'electricitat per als treballadors (EPIs).
- **Riscos ergonòmics:** Ús de carros elevadors per al transport de servidors i equipament pesat per evitar lesions musculars.
- **Riscos ambientals:** Condicionament acústic i ús d'auriculars si el soroll supera els límits de confort.
- **Sostenibilitat:** Possibilitat d'instal·lació de plaques solars per suplementar l'alimentació, il·luminació LED de baix consum i sistemes d'apagada o reducció de potència per equips no crítics fora d'hores punta.

---

### 1.4 Implementació al Núvol (AWS)
*Nota: Aquest apartat es completarà documentant la infraestructura orientada al núvol que inclou el Servei Web, transferència segura SFTP, LDAP, centralització de logs i administració remota automatitzada amb Ansible mitjançant claus públiques/privades.*

---

## 2. Serveis de Xarxes i Internet: Àudio i Vídeo (Bloc 0375)

Un cop consolidada la infraestructura de maquinari (tant local com al núvol), el següent pas és desplegar els serveis que donaran suport a la comunicació interna i la formació corporativa d'Innovate Tech, recolzant-se sobre la base ja dissenyada.

### 2.1 Descripció General dels Serveis
Implementació d'una arquitectura multimèdia que suporti la distribució de continguts en streaming i eines de videoconferència en temps real, accessibles des de clients locals i navegadors web.

### 2.2 Implantació del Servei d'Àudio

El servei d’àudio implementat permet la transmissió de contingut multimèdia en temps real mitjançant tecnologia de streaming basada en **Icecast2**.
Aquest sistema permet:
- Reproduir àudio remotament accedint des d’un navegador web.
- Centralitzar emissions d’àudio.
- Distribuir contingut multimèdia a diferents clients simultàniament (Client emissor → Servidor Icecast2 → Clients receptors).

**Dades de la instància AWS:**
| Configuració | Valor |
| --- | --- |
| Nom | audio01 |
| SO | Ubuntu Server 24.04 |
| Tipus | t3.micro |
| Storage | 15 GB |
| Security Group | HTTP + SSH + 8000 |

*Creació i accés a la instància:*
![Primera captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio01.png)
![Segona captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio02.png)
![Tercera captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio03.png)

*Instal·lació i configuració d'Icecast2:*
![Quarta captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio04.png)
![Cinquena captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio05.png)
![Sisena captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio06.png)
![Setena captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio07.png)
![Vuitena captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio08.png)
![Novena captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio09.png)

Per enviar l’àudio al servidor utilitzem **FFmpeg**:
![Desena captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio10.png)
S'utilitza una comanda indicant la ruta del fitxer mp3, la direcció del servidor i les credencials de l'usuari.
![Onzena captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio11.png)
![Dotzena captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio12.png)
![Tretzena captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio13.png)


### 2.3 Implantació del Servei de Vídeo i Videoconferència

La funcionalitat d'aquest servei busca que els treballadors es puguin enviar vídeos de suport tècnic, fer videoconferències en directe des de navegadors web i garantir la compatibilitat moderna.

#### Servidor de Streaming de Vídeo (NGINX + RTMP/HLS)

Es crea una màquina Ubuntu dedicada per al servidor de vídeo.
![Primera imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video01.png)
![Segona imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video02.png)

Instal·lem NGINX i el mòdul RTMP (Real-Time Messaging Protocol):
![Tercera imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video03.png)
![Quarta imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video04.png)

Es configura NGINX per suportar RTMP i HLS (que permet reproduir el directe des del navegador en petits fragments .m3u8):
![Quinta imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video05.png)
![Sisena imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video06.png)

S'utilitza OBS Studio per la transmissió en format H.264 i MP4:
![Setena imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video07.png)
![11 imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video11.png)
![Vuitena imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video08.png)

Reproducció via HLS directament des del navegador i evidència dels fitxers .ts generats:
![Novena imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video09.png)
![Dècima imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video10.png)

#### Videoconferència (Jitsi Meet i WebRTC)
WebRTC permet connexió de vídeo i àudio en temps real. S'ha optat per Jitsi Meet instal·lat a través dels repositoris oficials:
![Instal jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video12.png)
![APT jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video13.png)

A falta de domini propi, s'ha utilitzat la IP pública (elàstica) amb certificats autofirmats:
![Nom jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video14.png)
![Encriptació jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video15.png)
![Email jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video16.png)
![Telèfon jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video17.png)

Comprovació de trucada funcional des d'un client remot (telèfon mòbil):
![Verificiació jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video18.png)


### 2.4 Comprovacions d'Amplada de Banda i Rendiment

L'objectiu principal d'aquesta fase és analitzar si la infraestructura de xarxa suporta els serveis multimèdia implementats sense degradació de la qualitat. Totes les proves s'han fet utilitzant l'eina `speedtest-cli`.

#### 2.4.1 Resultats a la màquina d'Àudio (Icecast2)
La prova es va executar des de la instància EC2 encarregada de l'streaming d'àudio:
![Primera captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio14.png)
![Primera captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/audio15.png)

| Paràmetre | Resultat |
| --- | --- |
| Download | 1949.06 Mbit/s |
| Upload | 1869.21 Mbit/s |
| Latència | 6.502 ms |

El consum d'Icecast2 en MP3 ronda els **0.128 Mbps (128 kbps)**, la qual cosa suposa un impacte insignificant davant dels gairebé 1869 Mbps d'upload disponibles a l'entorn Cloud d'AWS. La latència és pràcticament imperceptible.

#### 2.4.2 Resultats a la màquina de Vídeo (NGINX / Jitsi)
![Install speedtest](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video19.png)

S'han realitzat proves comparatives per avaluar l'impacte dels serveis actius:
**Sense el servei de streaming/NGINX actiu:**
![Comprovació speedtest sense Nginx](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video20.png)
![Ping](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video21.png)

**Amb NGINX i serveis actius transmetent:**
![Comprovació speedtest amb Nginx](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video22.png)

#### 2.4.3 Classificació i Anàlisi
**Classificació del sistema:** Acceptable per a entorns de prova o PIMES petites, però podria ser No Acceptable per a un desplegament massiu sense canvis d'arquitectura.

L'anàlisi de les dades revela que per suportar coses petites com un servidor aïllat o certs contenidors Docker, la capacitat de xarxa és molt alta. Tot i així, el consum de CPU, I/O i xarxa creix ràpidament durant una videoconferència múltiple en Jitsi o streaming en HLS a molts clients. 

#### 2.4.4 Propostes de Millora
Per portar aquesta infraestructura a un entorn empresarial robust de grans dimensions es proposa:
1. **Segmentació de xarxa (VLANs):** Separar el tràfic de dades del tràfic de vídeo/àudio.
2. **Implementació de QoS:** Prioritzar el tràfic multimèdia als switches del CPD i a l'enrutament per evitar talls si hi ha càrregues de descàrrega concurrents.
3. **Escalabilitat del maquinari i connectivitat:** Connectivitat multioperador per assegurar redundància de red (BGP), i Balanceig de Càrrega (Load Balancers d'AWS o HAProxy) per donar suport a molts clients simultanis.
4. **Optimització del Bitrate:** Compressió H.265 en comptes de H.264 o reducció de bitrate adaptatiu (ABR) si les connexions dels clients són més lentes.

---

*(Nota: En la següent iteració del document s'incorporaran les seccions de Bases de Dades i Digitalització, unint l'estructura organitzativa i de seguretat).*
