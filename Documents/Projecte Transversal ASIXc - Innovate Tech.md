# Projecte Transversal ASIXc - Innovate Tech

Aquest document unifica les diferents fases del projecte de transformació tecnològica i modernització per a l'empresa **Innovate Tech**. L'objectiu principal és proporcionar una base tecnològica sòlida que integri la infraestructura de maquinari i els serveis de xarxa per millorar la capacitat operativa i comunicativa de l'empresa.

---

## 1. Fonaments de Maquinari i Proposta de CPD (Bloc 0371)

Per tal de garantir la continuïtat del negoci i donar suport als serveis multimèdia, la primera fase del projecte se centra en el disseny i implementació d'un Centre de Processament de Dades (CPD) eficient, segur i sostenible.

# 1.1 - Ubicació Física del CPD

**1- Situació de la sala a l’edifici**

*Innova Tech* és una empresa de consultoria tecnològica i desenvolupament de software:

- 50-80 empleats  
- 4 departaments distribuïts en: Vendes, Suport tècnic, Administració i Logística.  
- Serveis que ofereix: Desenvolupament de software personalitzat, consultoria cloud i formació tècnica.  
- Clients: Són petites i mitjanes empreses (PYMES) o startups (empresas noves).

On estem ubicats?  
Tenim la seu en el **Districte 22@,Barcelona**, concretament en un edifici d’oficines de 4 plantes més un soterrani. Aquest districte és la zona d'innovació tecnològica de Barcelona, on es concentren startups, consultores Tech i empreses de serveis digitals.

Ubicació CPD?  
EL CPD s'ubicarà en el soterrani  (planta \-1), el qual ocuparà uns **48m² (8m x 6m)** amb una altura lliure de **3,5 metres**.

Hem escollit el soterrani per diverses raons:

- Temperatura estable:

En el soterrani, la temperatura varia només ±2°C durant tot l’any, això gràcies a **l'aïllament natural del soterra**. En una planta superior la variació seria més alta, ja que intervenen diferents factors com, el sol, el vent, els canvis d’estació, etc.  
Amb això fem que el sistema d’aire condicionat treballi menys per mantenir la temperatura adequada, menys consum energètic i més sostenible. 

- Protecció contra fenòmens meteorològics:

La sala del CPD i el CPD no tindràn finestres, llavors no hi ha risc de trencaments pel temps meteorològic, a més de no tindre exposició directa al vent, pluja o neu.  
En el cas de possible inundació urbana, el soterrani té sensors d'aigua connectats a l'alarma.

- Seguretat física:

Difícil accés des de l’exterior, ja que no té finestres i portes directes al carrer, l’únic accés és per l'interior de l'edifici, passant per control d’accés principal, amb això es redueix el risc de vandalisme o intrusió.

- Aïllament acústic: 

El sistema d’aire condicionat fa soroll (50-70 dB), com es trova al soterrani aquest soroll no afecta a les oficines de les plantes superiors o als veïns, i aixì els empleats poden treballar tranquils.

   
**2- Sistemes de climatització (aire condicionat). Nivells de temperatura, humitat i**  
**neteja de l’aire.**

Hem instal·lat **2 unitats CRAC** (Computer Room Air Conditioning) de 10 kW cadascun. No hem escollit un aire condicionat domèstic, ja que aquest mantenen la temperatura amb una precisió de ±3°C i un CRAC professional la manté en ±1°C.  
És de importància escollir l’opció correcta, ja que els servidors són sensibles, si la temperatura puja a 30°C, el servidor es pot apagar automàticament per protegir-se. En una empresa que ofereix servei 24/7 a clients, una apagada de servidors és sinònim de perdudes de diners i reputació.

Hem ficat 2 unitats:

- 1 CRAC està actiu tot el temps, cobrint els 3,5 kW que generen els nostres servidors.  
- 1 CRAC està en standby, en el cas que falli el primer, el segon s’activa automàticament en menys de 30 segons.

Temperatura objectiva, **22°C** (el rang permès: 18-27°C segons la normativa **ASHRAETC 9.9**).  
Hem especificat els 22°C, ja que cada grau per sota, incrementa el consum elèctric un 4%.

En el cas de ficar la CPD a 18°C, es dir 4°C menys:

- Consum extra: 4°C x 4% \= 16% mes electricitat  
- Cost anual extra: \~1.200€  
- Impacte ambiental: \+1,5 tones CO₂/any

En conclusió, mantenir la CPD en 22°C es l’equilibri entre seguretat tèrmica i eficiència energètica.

**Humitat relativa**, un 50% (rang permès: 46-60%)

La humitat és molt important. Sí aquesta és **inferior de 40%**:

- L’aire és massa sec.  
- Es genera electricitat estàtica.  
- Es poden espatllar component electrònics a causa d’espurnes.

Sí es **superior a 60%**:

- L’aire està massa humit.  
- Es forma condensació i això genera gotes d’aigua.  
- Aigua \+ electricitat \= curtcircuit.

El nostre CRAC té un humidificador/deshumidificador integrat que ajusta automàticament.  
Per a la **neteja de l’aire**, tenen filtres **HEPA H13** (retenen el 99,95% de les partícules de 0,3 micres o més gran).

És de molta importància tenir un aire net, ja que la pols s’acumula en els ventiladors i dispersors dels servidors i actua com aïllador tèrmic.

- Canviem els filtres cada sis mesos   
- Els servidors es mantenen nets durant 2-3 anys sense necessitat d’obrir-los.  
- Allarguem la seva vida útil un 40%.

Configuració del passadís fred/calent.

Els dos racks estan col·locats un al costat de l'altre, creant:

- Passadís fred: La part frontal dels racks, on el CRAC impulsa l’aire fred.  
- Passadís calent: La part posterior dels racks, on s’acumula l’aire calent que expulsen els servidors.

La funció del CRAC és, que aspira l’aire calent del passadís posterior, l’enfreda i el torna a impulsar al passadís frontal. Utilitzat aquest model l’aire fred no és barrella amb el calent, el CRAC treballa de forma eficient \= estalviant un 30-40% en refrigeració.

**3- Mesures per dificultar la identificació de la sala.**

Fora de l'edifici:

- No col·locar cartells informatius.  
- Les reixetes de ventilació del CRAC que donen a l’exterior, han de tenir el mateix disseny que la resta de ventilació general de l'edifici. 

Dintre de l’edifici:

- Que la porta del CPD, estigui sense identificar.  
- Ha d'haver-hi el mateix model de porta que a la resta de portes de l’edifici.  
- Que la sala no aparegui en els plànols d'evacuació públics, només en documentació interna restringida.

Això es fa per dificultar possibles atacs d'enginyeria social, a més de complir amb la normativa ENS que obliga a no divulgar l'ubicació de instal·lacions crítiques.

**4- Distribució i gestió del cablejat**

En el CPD tenim dos tipus de cables:

Cables de dades (blaus):

- Connecten servidors, switches, sortida a internet.  
- Coure Cat 6A.
- Fibra òptica OM4 en el cas de que calgui connectar amb un altre edifici.

Cables elèctrics (negres):

- Conectant els servidors, PDU, SAI.

Per normativa els cables de dades i elèctrics hauran de tenir una separació mínima de 30 cm, TIA942, ja que els cables electrònics generen camps electromagnètics i en el cas que un cable de dades passes a prop d’un cable elèctric es pot produir errors de transmissió, paquets corruptes, retransmissió o latència.

A més és important que cada cable tingui una etiqueta en els dos extrems, per identificar quin serà el seu origen i el seu destí, En un CPD amb més de 50 cables, si has de localitzar un cable en específic, seria massa complicat si no porten l’etiqueta.

**5- Terra tècnic i sostre tècnic.**

**Terra tècnic** és bàsicament un terra fals elevat uns 60 cm, damunt el terra real. En aquell forat, passen cables elèctrics i l’aire fred que expulsa el CRAC. A més té com a funció amagar el cablejat elèctric, d’aquesta manera no tenim tots els cables per terra i prevenim possibles accidents.  
Components:   
**Sòl real:** El formigó original del soterrani.  
**Estructura metál·lica:** Potes ajustables de 60 cm d’altura.  
**Panells:** Plaques d’acer galvanitzat de 60x60 cm que es col·loquen sobre de l’estructura.  
**Reixetes:** Alguns panells tenen forats per on surt l’aire fred.

**Sostre tècnic**, és una estructura suspesa a uns centímetres per sota del sostre original, té una distància d’uns 3 metres sobre el terra tècnic. Una de les seves funcions és, recollir l’aire calent, ja que puja (l’aire calent és més lleuger) i entra al sostre tècnic fent que el CRAC aspiri aquest, l’enfredi i el torni a impulsar al terra tècnic. També passen cables de dades, com ja hem comentat els cables de dades aniran separats dels elèctrics que van per terra.  
Components:  
**Panels modulars:** Fets d’alumini ignífug (no crema en cas d’incendi).  
**Classificació:** MO (material no combustible segons normativa europea).

**6- Planells, dibuixos, diagrames dels elements anteriorment citats.**

**Plànol de planta del CPD**

![Plànol de planta del CPD](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/planta-cpd.png)

Vista superior de la sala mostrant la disposició dels 2 racks en configuració passadís fred/calent, les 2 unitats CRAC i la porta d'accés.

**Tall lateral - flux d'aire**

![Tall lateral - flux d'aire](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/flux-aire2.png)

Cicle complet de refrigeració mostrant com l'aire fred surt del terra tècnic, passa pels servidors, i torna al CRAC pel sostre tècnic.

**Distribució del cablejat**

![Distribució del cablejat](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/cablejat.png)

Separació física de 50 cm entre el cablejat de dades (sostre tècnic) i el cablejat elèctric (terra tècnic).

**7- Estructuració dels racks (mínim 2 racks).**

![Vista frontal dels racks](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/racks-frontal.png)

Hem instal·lat 2 racks de 42U del model APC NetShelter SX, tenen 600 mm d’ample exterior amb interior estàndard de 19 polzades, 1.070 mm de fons, suporten 1.360 kg de càrrega, portes perforades i pany.

Cada rack té:

1- **PDU intel·ligent (1U a la part inferior, U5-1):** regleta vertical amb 24 endolls C13 i monitoratge de consum elèctric individual per presa. Permet veure quin equip consumeix quant des d'un panell web.

2- **Organitzadors de cables** **(1U entre zones):** mantenen el cablatge ordenat. Sense ells, en 6 mesos el rack és un embull de cables.

3- **Panells cecs (a totes les U buides):** bloquegen el pas d'aire per les U no ocupades. Mantenen el flux d'aire correcte entre passadís fred i calent.

4- **Sensors de temperatura i humitat:** monitoren les condicions internes del rack. Connectats al sistema de monitoratge.

5- **Patch panels (part superior):** on acaben els cables de dades. Permeten connectar/desconnectar equips sense manipular els cables fixos.

Seguretat física dels racks:

Cada un dels racks té un pany amb clau física en les portes frontal i posterior, de la qual només el personal autoritzat té accés a les claus, aquestes claus es guarden en una caixa de seguretat fora del CPD, a més de tindre un procediment de control d’accés, tindre un registre de qui obre el rack i quan.

Normatives aplicades:

- **ANSI/EIA-310-D:** Estàndard de racks de 19 polzades. 
- **TIA-942:** Infraestructura de telecomunicacions per a CPDs.
- **ISO/IEC 11801:** Cablejat genèric.

# 1.2 - Infraestructura IT

# **Infraestructura IT**

A continuació es descriurà la infrastructura IT proposada per al CPD de Innova Tech basat en el pla de distribució presentat.

**Pla general del CPD**

El CPD disposa d'una superfície de 8 x 6 m², organitzada en:

- Zona principal de racks de servidors.  
- Zona de control i monitoratge.  
- Sistemes de climatització redundants.  
- Seguretat física mitjançant cambres i extintors.  
- Passadissos optimitzats per a manteniment i flux d'aire.

| Servidor | Funció | Model Prupossat | CPU | RAM | Emmagatzematge |
| ----- | ----- | ----- | ----- | ----- | ----- |
| WEB-SFTP | Web \+ SFTP | Dell PowerEdge R350 | 4 vCPU | 8 GB | 250 GB SSD |
| LDAP-AD | Directori Actiu | Dell PowerEdge R350 | 4 vCPU | 8 GB | 250 GB SSD |
| LOGS | Centralització de logs | HPE ProLiant DL360 | 4 vCPU | 16 GB | 500 GB SSD |
| AUDIO | Streaming d'audio | Dell PowerEdge R250 | 2 vCPU | 4 GB | 120 GB SSD |
| VIDEO | Streaming de vídeo | HPE ProLiant DL380 | 8 vCPU | 16 GB | 1 TB SSD |
| JITSI | Videoconferències | Dell PowerEdge R550 | 8 vCPU | 16 GB | 500 GB SSD |
| DATABASE | Base de dades | HPE ProLiant DL360 | 8 vCPU | 32 GB | RAID 1 SSD |
| ANSIBLE | Automatizació | Dell PowerEdge R250 | 2 vCPU | 4 GB | 120 GB SSD |

# **Patch Panels**

S'utilizarán patch panels Cat6A per a la distribució estructurada del clabejat.

## **Característiques**

| Element | Quantitat | Característiques |
| ----- | ----- | ----- |
| Patch Panel Cat6A | 4 | 24 ports RJ45 |
| Patch Panel Fibra | 2 | LC-LC multimode |
| Organitzador de cable | 8 | Horitzontal i vertical |
| Safata rack | 6 | Gestió d'equips |

## **Funcions**

* Organització del cablejat estructurat.  
* Reducció d'interferències.  
* Facilitar manteniment.  
* Separació entre xarxa de dades i administració.

# **Switches**

La infraestructura de xarxa utiliza switches gestionables de nivell empresarial.

| Switch | Model | Ports | Funció |
| ----- | ----- | ----- | ----- |
| Core Switch | Cisco Catalyst 9200 | 48 ports | Backbone principal |
| Switch Rack A | Cisco CBS350 | 24 ports | Servidors producció |
| Switch Rack B | Cisco CBS350 | 24 ports | Serveis multimedia |
| Switch Gestió | TP-Link JetStream | 16 ports | Administració i monitoratge |

## **Característiques de xarxa**

- VLANs separades.
- QoS per a tràfic multimèdia.
- STP/RSTP.
- Link Aggregation.
- Monitorizació SNMP.

# **Distribució dels racks**

La distribució física segueix una estructura optimizada per a:

* Refrigeració.  
* Mantenimentt.  
* Seguretat.  
* Escalabilitat.

## **Organització de racks**

| Rack | Contingut |
| ----- | ----- |
| Rack A | Web, SFTP, LDAP |
| Rack B | Logs i monitoratge |
| Rack C | Audio streaming |
| Rack D | Video streaming |
| Rack E | Jitsi Meet |
| Rack F | Base de dades |
| Rack G | Switches principals |
| Rack H | Patch panels |

# **Distribució interna d'un rack**

## **Exemple d'estructura de rack estàndar**

| Posició U | Element |
| ----- | ----- |
| U1-U2 | Patch Panel |
| U3 | Switch |
| U4-U6 | Servidor |
| U7 | Safata organització |
| U8-U10 | Segon servidor |
| U11 | PDU elèctrica |
| U12 | Espai ventilació |

## **Flux de connexió**

Internet  
  │  
Firewall  
  │  
Core Switch  
  ├── Rack A (Web/SFTP/LDAP)  
  ├── Rack B (Logs)  
  ├── Rack C (Audio)  
  ├── Rack D (Video)  
  ├── Rack E (Jitsi)  
  └── Rack F (Database)

# **Distribució segons el pla**

Segons el pla del CPD:

* Els racks estan distribuïts en files amb passadissos de manteniment.

* Els sistemes d’aire condicionat (AA) estan col·locats estratègicament per mantenir el flux d’aire fred/calent.

* La zona de control i monitorització està aïllada de l’àrea principal.

* Les càmeres cobreixen les entrades i els passadissos crítics.

* Els extintors estan repartits a les cantonades i a les zones centrals.

Aquesta distribució permet:

* Una millor circulació de l’aire.

* Reducció dels punts calents.

* Accés ràpid per al manteniment.

* Seguretat física reforçada.

---

 **Justificació tècnica**

L'infraestructura proposa compleix:

* Alta disponibilitat.

* Escalabilitat.

* Seguretat física y lógica.

* Organització professional del cablejat.

* Compatibilitat amb AWS híbrid.

* Optimització energètica.

# 1.3 - SAI

**Càlcul d’energia per a cada servidor:**

| Equip | Consum aproximat |
| :---- | :---- |
| 8 servidors | 8 x 200W \= 1600W |
| Switches | 150 W |
| Firewall | 100 W |
| NAS/backup | 400 W |

**1. Càlcul de la càrrega elèctrica total**

Abans d'escollir el SAI, el primer que hem de determinar és quanta energia consumeixen tots els nostres equips crítics de manera simultània. Si hi ha un tall elèctric, el sistema ha de poder mantenir-los tots encesos.

Servidors: Disposem de 8 servidors amb un consum aproximat de 200 W cadascun. Això ens dona un subtotal de 1600 W.

Xarxa i Seguretat: Hem de sumar l'equipament de connectivitat, com els switches (150 W), i el firewall per a la seguretat perimetral (100 W).

Emmagatzematge: El nostre sistema de NAS i còpies de seguretat suposa un consum addicional de 400 W.

Total: En sumar-ho tot, obtenim un consum màxim aproximat de 2600 W. El SAI que implementem haurà de ser capaç d'entregar, com a mínim, aquesta quantitat d'energia de forma contínua.

**2. Definició de l'autonomia necessària**

L'autonomia és el temps que les bateries del SAI ens permetran mantenir els equips funcionant un cop s'ha perdut el subministrament elèctric. És important destacar que el nostre objectiu no és continuar treballant durant hores sense corrent.

En el disseny del nostre CPD, hem establert un objectiu de 20 minuts. Aquest marge de temps és l'estàndard a la indústria (normalment entre 15 i 30 minuts) i ens cobreix davant de dos escenaris:

Donar temps suficient perquè el generador elèctric de l'edifici arrenqui automàticament i assumeixi la càrrega.

En cas de no disposar de generador, proporcionar un marge segur per enviar un senyal d'apagada controlada als servidors. Això ens permet tancar processos i bases de dades correctament, evitant la pèrdua de dades o la corrupció dels discs que provocaria una apagada sobtada.

**3. Elecció de la capacitat del SAI**

Per cobrir aquesta demanda, hem plantejat l'ús d'un SAI de 3000 VA (Voltamperes). En termes de potència real, a causa del factor de potència, un equip d'aquestes característiques acostuma a tenir un límit efectiu d'uns 2700 W.

Atès que el nostre consum total calculat és de 2600 W, treballarem molt a prop del límit de la capacitat de l'equip. Quan un SAI treballa pràcticament al 100% de la seva càrrega, les bateries internes s'esgoten molt més de pressa i, per si soles, no arribarien a cobrir els nostres requisits de temps.

**4. La nostra solució professional**

Com que operarem al límit de la capacitat en watts i un sol SAI base no aguantaria els 20 minuts que ens hem marcat com a objectiu, implementarem una solució més avançada i escalable:

Equip principal: Utilitzarem un SAI de gamma empresarial, en concret el model APC Smart-UPS 3000VA.

Expansió d'autonomia: Per aconseguir garantir aquests 20-25 minuts reals amb una càrrega tan alta, hi afegirem un pack d'expansió (mòduls de bateries externes que es connecten al SAI principal).

Redundància: Disposarem de 2 mòduls de bateries redundants. Això garanteix que, si una bateria falla internament, l'altra continuarà donant servei, assegurant que el CPD es mantingui operatiu i complint amb els nostres estàndards de seguretat i fiabilitat.

# 1.4 - Seguretat Física, Lògica i Prevenció de Riscos

-  ## Seguretat física:   
  La seguretat física implica tenir el lloc vigilat 24/7 de diferents maneres, tenir objectes de detecció. Les principals maneres de vigilància són:  
    
- Elements d’accés al CPD:

  Poder accedir a la sala del CPD només amb unes claus, targetes especials d’identificació o un factor de doble autenticació per a usuaris importants a l’empresa.


- Càmeres de seguretat i miralls:

  Les càmeres de seguretat serveixen per poder rastrejar qui entra a la sala del CPD. Que fa dintre d’aquesta i durant quins períodes de temps ha estat dintre de la sala. El cas dels miralls convexos serveix per ajudar les càmeres a veure el que serien punts cecs sense els miralls.


- Sistemes de prevenció, detecció i extinció d’incendis:

  Per a prevenir cap incendi, principalment s'ha de tenir climatització, ja que aquest permet que el CPD no se s'obreescalfi i tingui problemes de temperatura, en qualsevol cas, també tenir un termòmetre per veure tant la temperatura com l’humitat.

  Per poder detectar en cas d'haver-hi algun objecte incendiat o que el mateix CPD estigui en llames utilitzar detectors de fum i detectors de calentor d’alta sensibilitat, o com hem dit anteriorment podem utilitzar un termòmetre.

  Per un altra part per a poder extingir l’incendi, tenir extintors de C02, ja que són els únics que van millor per apagar incendis elèctrics, el que són en aquest cas.

- ## Seguretat lògica:  
  En canvi, la seguretat lògica ha de ser més rigorosa, ja que els servidors en un CPD contenen informació valuosa, és per això que aplicarem la següent seguretat:

- Restricció d’accés per autorització:

  Només es permet l’accés als servidors a usuaris específics i dels quals només es poden ficar certes persones amb les restriccions necessàries, i amb certs permisos.


- Firewalls:

  El firewall clarament ha d’estar actiu per tots els ports i només es pot permetre l’accés des de certs ordinadors i certs ports que seran els que utilitzaran els ordinadors per poder conectarse a aquest. És a dir, una filtració de ports i protocols.


- Mointoratge:

  Programes de monitoratge i recull de logs per poder veure, quin error succeeix, quan succeeix, i per què succeeix. En tot cas el programa de monitoratge, envia un missatge als ordinadors centrals quan succeixi algun error.


- ## Còpies de seguretat:

  Es fària principalment una còpia de seguretat base cada diumenge perquè, si es fastigueja alguna màquina, o es perd alguna cosa entre les màquines poder recuperar-la. I a part fer còpies diferencials diàries per poder fer un backup en el cas que passi alguna cosa, d’un dia l'altre.


- RAIDs:

  En el cas de les RAIDs, el que pensem que és més recomanable és fer una RAID 0+1, ja que en cas d'haver-hi algun problema les dades es poden recuperar de manera eficaç i ràpida.

- Prevenció de riscos laborals:  
  En quant a prevenció de riscos laborals, volem que els treballadors també portin seguretat, tant per a ells, com per al CPD.  
    
  Principalment, el terra i la roba que porten els treballadors han de ser aïllants d’electricitat perquè els treballadors no siguin electrocutats i els servidors no puguin patir cap tipus de sobrecàrrega.  
    
  També es pot tenir en compte els riscos ergonòmics, per exemple, a l’hora de portar els servidors, o els racs, com tenen un alt pes, el millor és utilitzar carros amb els quals es puguin portar aquests aparells.
    
  I podem evitar riscos ambientals, per exemple, posar els CRACs ja mencionats abans per a poder evitar una temperatura molt alta i que així sigui estable, també es poden aplicar auriculars per controlar el soroll en el cas dels treballadors.  
    
    
- ## Maneres de fer això més sostenible:  
  Per poder fer que el CPD sigui sostenible es poden aplicar diferent protocols, com per exemple:  
- Instal·lació de plaques solars per poder alimentar així el CPD.  
- Reutilització de l’aire utilitzat, sempre que es faci servir un filtre per poder netejar aquest aire, i així reutilitzar-ho.  
- Il·luminació mitjançant llums LED de baix consum.
- I apagar els equips no necessaris a les hores punta per a què no consumeixin.


# 1.5 - Implementació al Núvol (AWS)
 
## Ansible 
### El paper central del nostre servidor Ansible

Hem implementat un servidor Ansible dedicat per actuar com el cervell i l'orquestrador de tota la nostra infraestructura. Els motius i avantatges principals d'aquesta decisió són els següents:

*   **Automatització eficient i centralitzada:** En lloc de connectar-nos manualment via SSH a cada servidor per configurar-los d'un en un, Ansible ens permet executar *playbooks*. Això significa que podem aplicar configuracions, actualitzacions i canvis a totes les màquines alhora de manera totalment automatitzada, estalviant temps i minimitzant els errors humans.
*   **Recuperació immediata (Infraestructura com a Codi):** Aquest servidor emmagatzema els fitxers de configuració `.yml`, els quals actuen com un registre i una còpia de seguretat exacta de com han d'estar configurats els nostres equips. Si un servei crític cau o es corromp (com el servidor web o el de *syslog*), aquests fitxers ens permeten restaurar i tornar a desplegar tota la instal·lació i configuració des de zero en menys de 30 segons.
*   **Arquitectura neta i sense agents:** Un dels grans avantatges d'Ansible és que no requereix instal·lar programari addicional o agents pesats als servidors de destí. Simplement aprofita el protocol SSH, que ja ve integrat de sèrie en els sistemes operatius, per connectar-se, aplicar els canvis de configuració necessaris i desconnectar-se, mantenint els equips de la infraestructura lleugers i segurs.


1. Instal·lació d'instància 

Primer de tot hauriem d'iniciar el Launch d'AWS:  
![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible1.png)

Crearem les claus, perquè així els nostres companys puguin connectar-se al nostre servidor només passant-li la nostra clau pública:

![image2](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible2.png)  

![image3](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible3.png)

Seleccionarem la clau abans creada como també l’edició de l’ordinador de lloguer que viu en un centre de dades d'Amazon, permetrem la conexió via SSH desde qualsevol lloc:

![image4](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible4.png)  

![image5](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible5.png)

![image6](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible6.png)

Llavors llançem l'instància:

![image7](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible7.png)

Una vegada creada, el primer que farem serà assignar-li la IP elàstica perquè sigui estàtica i així no canviï de IP cada cert temps.
Per a això ens dirigirem al menú de l'esquerra a l’apartat “Direcciones IP elásticas”.
I li associarem una nova IP elástica:

![image8](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible8.png)

![image9](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible9.png)

Comprovació:

![image10](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible10.png)

Es copia la commanda per després utilitzar-la, encara això, he de canviar els permisos de la clau:

![image11](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible11.png)

Ara si, peguem la comanda copiada enteriorment que ens permetrà accedir a la instància:

![image12](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible12.png)

2. Configuració del servidor

Una vegada dins de la instància primer cambiem el hostname, i després creem l'usuari "administracio" amb contrasenya “@ITB2026”:

![image13](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible13.png)

![image14](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible14.png)

![image15](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible15.png)

Una vegada hem fet la creació de l'usuari li copiem les claus SSH de l'usuari ubuntu perquè pugui iniciar sessió sense contrasenya, a part d'això l'afegim al grup root junt a ficar-ho al fitxer sudoers per concedir privilegis d'administrador:

![image16](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible16.png)

![image17](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible17.png)

Reiniciem el servidor perquè es desin tots els canvis:

![image18](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible18.png)

I veiem que efectivament podem entrar sense contrasenya amb l'usuari creat prèviament i que té permisos de sudo:

![image19](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible19.png)

3.Actualització i instal·lació d'ansible

Actualitzem la llista de paquets del sistema i instal·lem les eines necessàries per poder llençar les instàncies d'AWS mitjançant els playbooks:

![image19](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible20.png)

![image19](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible21.png)

4.Creació, execució i comprobació de playbook del servidor web

Primer de tot, hem d'agafar les credencials que m'ha passat el meu company per enganxar-les en un document anomenat "credentials", gràcies a aquest fitxer, ens deixa crear la instància per al meu company:

![image19](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible22.png)

![image19](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible23.png)

![image19](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible24.png)

![image19](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible26.png)

Ara hem de crear el playbook pel servdior web:

![image19](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible25.png)

![image19](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible27.png)

![image19](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible28.png)

![image19](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible29.png)

![image19](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible30.png)

![image19](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible31.png)



## Servei de directori actiu per a guardar els usuaris.

Avanç de llançar la EC2, necesiten crear una clave SSH, per poder accedir a la instància:

![Clau LDAP](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/Clau-ldap.png)

Una vegada creades el parell de claus, llencem la instància del servidor amb les següents característiques:

![Instància AWS 1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/instancia1..png)

![Instància AWS 2](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/instancia2.png)

![Instància AWS 3](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/instancia3.png)

![Instància AWS 4](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/instancia4.png)

Ens connectem a la instància via SSH:

![Accés SSH](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ssh-acceder.png)

**Centralització d’usuaris.**

Modifiquem el hostname:

![Hostname](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/hostname.png)

![Fitxer etc/hosts](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/etc-hosts.png)

**Instal·lació OpenLDAP.**

Utilitzem la comanda “sudo apt install \-y slapd ldap-utils”:

![Instal·lació slapd](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/install-slapd.png)

Configurem la contrasenya de l’administrador:

![Admin contrasenya](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/admin-contra.png)

Verifiquem que s’ha fet la instal·lació correctament:

![Status servei](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/status.png)

**Configuracions de Slapd.**

![Slapd evidència 1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd1.png)

![Slapd evidència 2](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd2.png)

![Slapd evidència 3](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd3.png)

![Slapd evidència 4](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd4.png)

![Slapd evidència 5](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd5.png)

![Slapd evidència 6](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd6.png)

Comprovació:

![Comprovació slapd](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/comprobslapd.png)

**Creació d'usuari administrador, accés amb clau publica/privada.**

Fem la configuració necessària al fitxer, "sudo nano /etc/ssh/sshd_config":

![Admin SSH 1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/adminssh1.png)

![Admin SSH 2](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/adminssh2.png)

Comprovació amb l'usurai administració:

![Admin Login](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/adminlogin.png)

# Estructura d'Usuaris del Directori LDAP
 
## Fitxer de creació d'usuaris (`usuarios.ldif`)
 
![usuarios.ldif](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/estruct04.png)
 
Els 4 usuaris s'han creat mitjançant el fitxer `~/usuarios.ldif`. Cada entrada defineix els atributs necessaris per al funcionament del compte al sistema i al directori:
 
- **`objectClass: inetOrgPerson`** — dades personals (nom i cognoms).
- **`objectClass: posixAccount`** — integració Unix (UID, GID, shell, directori home).
- **`objectClass: shadowAccount`** — gestió de contrasenyes.
Tots comparteixen `gidNumber: 10000`, `loginShell: /bin/bash` i `userPassword: @ITB2026`.
 
---
 
## Estructura completa del directori
 
![ldapsearch complet](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/estruct01.png)
 
El directori LDAP s'organitza sota `dc=innovatetech,dc=local` amb dues unitats organitzatives:
 
```
dc=innovatetech,dc=local
├── ou=usuaris   → conté els 4 usuaris del grup
└── ou=grups     → reservat per a grups de treball
```
 
Cada usuari té un `uidNumber` únic i el seu propi `homeDirectory`.
 
---
 
## Verificació dels usuaris creats
 
![ldapsearch usuaris](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/estruct02.png)
 
Es confirma que els 4 usuaris estan correctament registrats a `ou=usuaris,dc=innovatetech,dc=local`:
 
| uid | Nom complet | uidNumber |
|---|---|---|
| elian | Elian Salvador | 10001 |
| gerard | Gerard Romero | 10002 |
| daniel | Daniel Roblas | 10003 |
| elias | Elias Martinez | 10004 |
 
---
 
## Estat del servei OpenLDAP
 
![slapd status](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/estruct03.png)
 
El servei `slapd` es troba en estat **active (running)**. La versió instal·lada és OpenLDAP `2.6.10` sobre Ubuntu 24.04, en funcionament des de l'inici del servidor.


## Implementació al núvol AWS - Web/SFTP

En primer lloc crearem un grup de seguretat que permeti tot el tràfic, per poder connectar-nos a la nostra pròpia instància:

![Primera captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web01.png)

I comencem a crear la instància amb el nom pertinent: 

![Segona captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web02.png)

Aquestes seran les següents característiques:

![Tercera captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web03.png) 

![Quarta captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web04.png)

![Quinta captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web05.png)

Tot seguit a això fem SSH per ficar-nos a la instància i li cambien el hostname per poder identificarla de manera fàcil:  

![Sexta captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web06.png)

Ara que ens hem ficat, crearem l'usuari "administracio" i tot seguit li canviem la contrasenya i li afegim al grup root: 

![Septima captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web07.png)

I les claus de l’usuari Ubuntu les copiem a la home de l'usuari “administracio”, ja que a partir d’ara ens ficarem a aquest:  

![Dècima captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web08.png)

Comprovació que es pot accedir:

![Decimaprimera captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web09.png)

## Instal·lació de nginx:  

![Decimasegona captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web12.png)

![Tretzena captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web13.png)

Comprovació de SFTP:

![Catorzena](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web14.png)

Podem veure que SFTP ve per defecte a la instància

Verifiquem que NGINX funciona correctament ficant l'enllaç públic:

![Quinzena](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web15.png)
 
### Instal·lació de vsftpd i clients LDAP

S'instal·la els paquets necessaris per integrar la màquina amb LDAP: `libnss-ldap`, `libpam-ldap`, 'ldap-utils' i per últim 'nslcd'. Aquests paquets permeten que el servidor web conegui els usuaris del LDAP i pugui autenticar els usuaris contra el directori LDAP d'InnovateTech, i el 'nslcd' és qui permet que hi hagi una connexió.

![bdldap01](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap01.png)

## Configuració de LDAP
 
A l'hora d'instal·lar els paquets anteriors, hem hagut de configurar un par de coses, com la direcció del servei LDAP, i els dc del domini:
 
![bdldap01](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap02.png)
![bdldap01](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap03.png)
 
Es configura el client LDAP apuntant al servidor del directori actiu:
 
```
URI ldap://52.0.2.63
BASE dc=innovatetech,dc=local
```

Això permet que qualsevol servei del sistema (vsftpd, SSH, web) resolgui usuaris contra el servidor LDAP d'InnovateTech.

### VSFTPD i fitxer `/etc/pam.d/vsftpd`

Després d'haver configurat el necessari per el LDAP instal·lem el VSFTP i el configurem per a que s'apigui que ha d'agafar l'autenticació i les comptes del LDAP: 
 
![bdldap01](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap04.png)
![bdldap01](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap05.png)
 
### Fitxer `/etc/nsswitch.conf`
 
![bdldap01](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap06.png)
 
Es modifica el fitxer de resolució de noms del sistema per consultar LDAP:
 
```
passwd:  files systemd ldap
group:  files systemd ldap
shadow: ldap
```
 
Això garanteix que el sistema busqui els usuaris tant en fitxers locals com al servidor LDAP.
 
## Verificació de la integració LDAP
 
### Consulta de tots els usuaris del directori i resolució d'usuaris
 
![bdldap01](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap07.png)
 
S'executa `ldapsearch` des del servidor web per verificar la connectivitat i llistar tots els usuaris del directori LDAP. Es confirma que els 4 usuaris del grup GEDE estan correctament creats a `ou=usuaris,dc=innovatetech,dc=local`:
 
- `uid=elian` — Elian Salvador
- `uid=gerard` — Gerard Romero
- `uid=daniel` — Daniel Roblas
- `uid=elias` — Elias Martinez
 
Això confirma que `nslcd` funciona correctament i el sistema operatiu reconeix els usuaris del directori LDAP.
 
## Instal·lació de PHP i Nginx
 
### Instal·lació de PHP, php-fpm, php-mysql i php-ldap
 
![bdldap01](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap08.png)
 
S'instal·la **PHP** amb el mòdul `php-fpm` per processar fitxers PHP a través de Nginx. El sistema instal·la automàticament totes les dependències necessàries.
 
S'instal·len les extensions PHP necessàries per a l'aplicació web:
 
- **php-mysqli** — per connectar amb la base de dades MySQL d'InnovateTech.
- **php-ldap** — per autenticar els usuaris contra el servidor LDAP.
 
## Configuració de Nginx
 
### Fitxer `/etc/nginx/sites-available/default`
 
![bdldap01](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap09.png)
 
Es configura Nginx per processar fitxers PHP via FastCGI, apuntant al socket de `php-fpm`:
 
```nginx
location ~ \.php$ {
   include snippets/fastcgi-php.conf;
   fastcgi_pass unix:/run/php/php8.3-fpm.sock;
}
```
 
## Desplegament de l'aplicació web
 
### Fitxers de l'aplicació
 
![bdldap01](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap10.png)
![bdldap01](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap11.png)
![bdldap01](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap12.png)
![bdldap01](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap13.png)
 
Es creen els 4 fitxers PHP que formen l'aplicació de gestió d'InnovateTech:
 
| Fitxer | Funció |
|---|---|
| `index.php` | Redirigeix a `login.php` |
| `login.php` | Autenticació d'usuaris via LDAP |
| `dashboard.php` | Interfície principal amb les 14 taules de la BBDD |
| `logout.php` | Tancament de sessió |
 
## Resultat final
 
### Pantalla de login
 
![bdldap01](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap14.png)
 
Pantalla d'accés de l'aplicació web accessible des de `http://3.210.137.51`. L'autenticació es realitza contra el servidor LDAP d'InnovateTech (`ldap://52.0.2.63`). Els usuaris s'autentiquen amb les seves credencials del directori actiu.
 
### Dashboard principal
 
![bdldap01](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/bdldap15.png)
 
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

![Primera captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog01.png)

Una vegada creades les claus .pem:

![Segona captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog02.png)

Ara instal·lem el servei que ens permetrà realitzar els logs de tots els servidors:

![Tercera captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog03.png)

Ara editem el fitxer de configuració de logs del servidor /etc/rsyslog.conf:

![Cuarta captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog04.png)

Ara crearem les carpetes pels logs remots en el fitxer /etc/rsyslog.d/remote.conf:

![5 captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog05.png)

Això fa:

- Una carpeta per a cada servidor.  
- Logs separats automàticament.

Reiniciem el servei:

![Sisena captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog06.png)

Per a la comprovació caldrà instalar el rsyslog en els servidors i en el fitxer /etc/rsyslog.conf afegir la linea *.* @18.212.86.171:514 i despres reiniciar client, 'sudo systemctl restart rsyslog' i finalment veure al directori que hem configurat, ho podem fer amb 'cd /var/log/remote/' i per a cada servidor 'web01/', 'ldap01/', 'db01/'.


Creació usuari "administracio":

![Sisena captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog08.png)

Comprovació del funcionament dels logs:

![Sisena captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog09.png)

---

### 2. Serveis de Xarxes i Internet: Àudio i Vídeo (Bloc 0375)

Un cop consolidada la infraestructura de maquinari (tant local com al núvol), el següent pas és desplegar els serveis que donaran suport a la comunicació interna i la formació corporativa d'Innovate Tech, recolzant-se sobre la base ja dissenyada.

# 2.1 - Descripció General dels Serveis
Implementació d'una arquitectura multimèdia que suporti la distribució de continguts en streaming i eines de videoconferència en temps real, accessibles des de clients locals i navegadors web.

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

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio01.png)

Accedim a ella:

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio02.png)

Creació usuari "administracio":

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio03.png)

Instal·lar Icecast2:

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio04.png)

Realitzem la següent configuració al servei:

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio05.png)

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio06.png)

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio07.png)

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio08.png)

Funcionament del servei:

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio09.png)

Per enviar l’audio a la pàgina instal·larem el servei ffmpeg:

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio10.png)

Una vegada descarregat el mp3, utilitzarem la commanda següent indicant el audio a utilitzar, la direcció de la pàgina i les credencials del usuari que permet pujar l’audio:

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio11.png)

Comprovació de que es pot escoltar l’audio desde la ruta:

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio12.png)

Execució de la comanda:

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio13.png)

# Amplada de banda

## **Objectiu**

Analitzar el rendiment de xarxa disponible per comprovar si la infraestructura implementada és adequada per suportar els serveis multimèdia del projecte, especialment el servei d’àudio en streaming implementat amb Icecast2.

# **Proves de velocitat realitzades**

Instal·lació del servei 'speedtest-cli':

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio14.png)

La prova es va executar directament des del servidor AWS EC2 on està implementat el servei d’àudio.

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio15.png)

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

# 2.3 - Implantació del Servei de Vídeo i Videoconferència

**Funcionalitat del servei de vídeo:**

La funcionalitat que volem amb el servei de vídeo són varies, per exemple volem que:

- Els treballadors es puguin enviar vídeos en streaming entre si per poder veure com fan manteniment dels servidors.  
- Els treballadors puguin fer videoconferències en directe com a medida per fer una reunió en cas de que algu no estigui disponible.  
- Accés des de qualsevol navegador web.  
- Hi hagi compatibilitat amb videos moderns i antics, a part de que tinguin qualsevol tipus d'extensió.

Primer de tot crearem una altra instància en AWS, que serà el servidor de vídeo:

![Primera imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video01.png)

![Segona imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video02.png)

Ara instal·larem el servei web de Nginx:

![Tercera imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video03.png)

D'aquí començem la part de streaming. Instal·lant RTMP (Real-Time Messaging Protocol), que és qui ens permet poder fer la transmissió en directe desde l'aplicació dessitjada:

![Quarta imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video04.png)

Després d'això hem de configurar l'arxiu de configuració del Nginx per a que pugui utilitzar tant RTMP com HLS, el qual aquest últim ens permetrà poder observar el directe desde el navegador mitjançant un enllaç:

![Quinta imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video05.png)
![Sisena imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video06.png)

Una vegada feta la configuració anterior anem a una gravadora (OBS Studio) i a la part de directe com a servidor posem l'enllaç RTMP del nostre servidor, amb la clau test, que és a ón es guarden els troçets del directe:

![Setena imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video07.png)

Llavors al OBS Studio posem com a codificador el H264 i el format d'enregistrament com a MP4:

![11 imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video11.png)

Com hem configurat tot de manera correcta, no apareix cap error a l'hora de fer la transmissió i es pot fer sense cap problema:

![Vuitena imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video08.png)

Ara, si ens fiquem al següent enllaç (http://98.80.217.120:8080/hls/test.m3u8) podrem veure la transmissió en directe, cap aclarir que té un delay una mica gran entre el que passa i el que surt al navegador:

![Novena imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video09.png)

També si observem la carpeta on hem especificat anteriorment al bloc de RTMP, veurem com es creen els trossos de la transmissió:

![Dècima imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video10.png)

**Descripció del protocol de videoconferència:**

WebRTC (Web Real-Time Communication) és un protocol o projecte open source que ens permet tenir una connexió a video, audio i de metadata de manera real. Aquest projecte permet als usuaris conectarse principalment des de navegadors, encara això també aplicacions mòbils per instal·lar.

Al nostre cas utilitzarem l’eina Jitsi Meet que al igual que WebRTC és un eina de videoconferènia i missatgeria instantànea que conté protocols de missatgeria instantània i telefonia populars.

A l’hora d’instal·lar l’eina hem visitat la seva pàgina web per veure com instal·lar-ho:  
https://jitsi.org/downloads/ubuntu-debian-installations-instructions/

Ara per la part de videoconferència primer descarregarem el repositori jitsi des de la seva pàgina oficial i després li afegirem el repositori oficial al nostre ordinador:

![Instal jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video12.png)

Després instal·lem l'aplicació mitjançant apt:

![APT jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video13.png)

Ara el jitsi ens demana un nom que assigna a l'enllaç de les videoconferències, al nostre cas com no tenim un nom de domini ja que no tenim bind9 instal·lat li posem que sigui simplement la IP pública de la màquina:

![Nom jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video14.png)

Com utilitza HTTPS fiquem que encripti els certificats, no fiquem email ni número de telèfon, ja que no dispossem de cap:

![Encriptació jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video15.png)

![Email jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video16.png)

![Telèfon jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video17.png)

Ara verifiquem que funcionen les reunions si ens fiquem a l'adreça pertinent, com l'hem posat la IP elàstica com a nom de domini, al navegador també li posem la IP elàstica, amb això hem inclòs una prova des d'un telèfon mòbil per verificar que és multiplataforma:

![Verificiació jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video18.png)

**Comprovacions d'amplada de banda:**

Necessitarem instal·lar el servei de speedtest client per poder veure aixì la pujada i baixada en velocitat:

![Install speedtest](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video19.png)

Llavors primer anem a fer la verificació de la velocitat amb el Nginx desactivat, ja que és qui porta els serveis de streaming i videoconferència:

![Comprovació speedtest sense Nginx](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video20.png)

Verifiquem la latència:

![Ping](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video21.png)

Per últim, anem a verificar la pujada i baixada amb els serveis actius, i mentre fa una transmissió:

![Comprovació speedtest amb Nginx](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video22.png)

Amb aquestes dades hem arribat a la conclusió de que el sistema és acceptable per a una petita empresa. En canvi, no es pot utilizar per a sistemes que ocupin gran quantitat de recursos, ja que es faria inestable.

Algunes millores a incorporas per a una empresa poden ser:
- Segementació de la xarxa.
- Millora del hardware.
- Una connexió multioperadora.

## 3. Disseny i implementació d'una base de dades (Bloc 0377)

Som Innovate Tech, una empresa de consultoria tecnològica amb seu al Districte 22@ de Barcelona. Disposem d’una estructura interna amb 4 departaments:

- Vendes.
- Suport Tècnic.  
- Administració. 
- Logística.

Per aquest motiu necessitem una base de dades que doni suport a:

- La gestió del personal i l’estructura organitzativa de l’empresa.  
- El sistema de comunicació interna, videotrucades i gestió del streaming d’àudio i vídeo.  
- El control d’accés, seguretat i auditoria de la base i els sistemes instal·lats.

**Llançament de la instància.**

![BBDD1](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/bbdd1.png?raw=true)

![BBDD2](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/bbdd2.png?raw=true)

![BBDD3](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/bbdd3.png?raw=true)


Comprovació d’accés a la instància des de SSH:

![SSHBBDD](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/sshbbdd.png?raw=true)

Creació de l’usuari per accedir mitjançant clau pública/privada, més comprovació que es pot accedir:

![Admin conf](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/admin_conf.png?raw=true)

![Comprobación admin](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/comprob-admin.png?raw=true)

# 3.1 - Context del Projecte

Innovate Tech disposa d’una estructura interna amb 4 departaments principal com ja havíem comentat abans. Aquests departaments necessiten eines de comunicació eficients, incloent-hi un sistema de videoconferències i trucades per coordinar les seves operacions diàries.  
Aquesta base de dades servirà com a font de dades per a l’aplicació de gestió que residirà al servidor web.

S’ha escollit MySQL com a sistema gestor de bases de dades, per els següents motius:

- És àmpliament utilitzat en entorns empresarials reals, amb moltes instal·lacions actives.  
- Té suport  complet per a triggers, events programats i procediments emmagatzemats, necessaris per a l’auditoria i automatització del projecte.  
- Integració nativa amb aplicacions web mitjançant PHP, Python i Node.js.  
- Sense cost de llicència (open source, llicència GPL).

# 3.2 - Disseny i Implementació de la Base de Dades

La Base de dades d’Innovate Tech ha de  cobrir les següents àrees funcionals:

- Gestió del personal i estructura organitzativa.  
- Sistema de comunicació interna.  
- Catàleg de vídeos en streaming.  
- Anàlisis d’amplada de banda  
- Control d'accés i auditoria.

A continuació es detallen les entitats, atributs i relacions que componen la base de dades.

**3.2.1 Gestió del Personal i Estructura Organitzativa**

La base de dades ha de gestionar tota la informació relacionada amb el personal de l’empresa.

Taula: departaments

Emmagatzema els departaments de l'empresa (Vendes, Suport Tècnic, Administració, Logística).

\- codi\_departament (VARCHAR 10\) — Clau primària. Codi únic del departament.  
\- nom (VARCHAR 100\) — Nom complet del departament.  
\- telefon (VARCHAR 15\) — Telèfon de contacte del departament.

Taula: empleats

Emmagatzema les dades personals de cada empleat.

\- dni (VARCHAR 9\) — Clau primària. DNI únic per a cada empleat, tal com indica l'enunciat.  
\- nom (VARCHAR 50\) — Nom de l'empleat.  
\- cognoms (VARCHAR 100\) — Cognoms de l'empleat.  
\- adreca (VARCHAR 200\) — Adreça completa.  
\- telefon (VARCHAR 15\) — Telèfon de contacte.  
\- codi\_departament (VARCHAR 10\) — Clau forana cap a departaments. Cada empleat pertany a un únic departament.

**3.2.2 Sistema de Comunicació Interna**

La base de dades ha de gestionar els usuaris del sistema de comunicació, la configuració de qualitat i el registre de trucades.

Taula: usuaris\_comunicacio

Emmagatzema els usuaris que poden fer videotrucades i accedir al streaming.

\- id\_usuari (INT AUTO\_INCREMENT) — Clau primària.  
\- nom\_complet (VARCHAR 150\) — Nom complet de l'usuari.  
\- correu (VARCHAR 100 UNIQUE) — Correu electrònic únic.  
\- extensio (VARCHAR 20\) — Extensió o identificador de trucades.  
\- estat (ENUM 'actiu','bloquejat') — Estat actual de l'usuari. L'enunciat exigeix distinció entre actiu i bloquejat per al control de trucades.  
\- tipus (ENUM 'intern','extern') — Distinció entre treballadors interns i clients externs, tal com demana l'enunciat.  
\- enllac\_videotrucada (VARCHAR 255\) — Enllaç per iniciar una videotrucada. L'enunciat indica que s'ha de poder generar per a cada usuari.  
\- dni\_empleat (VARCHAR 9 NULLABLE) — Clau forana cap a empleats. Només s'omple si l'usuari és intern (treballador).

Taula: configuracio\_qualitat

Emmagatzema les configuracions de qualitat de vídeo i àudio per a grups d’usuaris.

\- id\_configuracio (INT AUTO\_INCREMENT) — Clau primària.  
\- nivell\_qualitat (ENUM 'alta','mitja','baixa') — Els tres nivells que indica l'enunciat.  
\- resolucio\_video (VARCHAR 20\) — Resolució (ex: 1080p, 720p, 480p).  
\- bitrate\_audio (INT) — Qualitat d'àudio en Kbps.  
\- amplada\_banda\_min (INT) — Amplada de banda mínima necessària en Mbps. Permet que el sistema recuperi la configuració inferior quan l'usuari té limitacions.  
\- descripcio (TEXT) — Descripció de la configuració.

Taula: configuracio\_servidor

Emmagatzema els paràmetres del servidor de videotrucades.

\- id\_config (INT AUTO\_INCREMENT) — Clau primària.  
\- parametre (VARCHAR 100\) — Nom del paràmetre (ex: max\_participants, timeout).  
\- valor (VARCHAR 200\) — Valor del paràmetre.  
\- protocol (VARCHAR 20\) — Protocol utilitzat (WebRTC, SIP, etc.).  
\- port (INT) — Port del servei.  
\- descripcio (TEXT) — Descripció del paràmetre.

Taula: trucades

Registre de cada trucada realitzada al sistema.

\- id\_trucada (INT AUTO\_INCREMENT) — Clau primària.  
\- id\_originador (INT) — Clau forana cap a usuaris\_comunicacio. Qui inicia la trucada.  
\- id\_destinatari (INT) — Clau forana cap a usuaris\_comunicacio. Qui rep la trucada.  
\- data\_inici (DATETIME) — Data i hora d'inici de la trucada.  
\- data\_fi (DATETIME) — Data i hora de finalització.  
\- durada\_total (INT) — Durada total en segons.  
\- id\_qualitat (INT) — Clau forana cap a configuracio\_qualitat. Qualitat de servei usada.  
\- puntuacio (TINYINT) — Valoració de l'usuari de l'1 al 5\.  
\- comentari (TEXT) — Comentari opcional de l'usuari sobre la trucada.

**3.2.3 Catàleg de Vídeos en Streaming**

Taula: videos\_streaming

Emmagatzema la informació dels vídeos disponibles al sistema d'streaming.

\- id\_video (INT AUTO\_INCREMENT) — Clau primària.  
\- titol (VARCHAR 200\) — Títol del vídeo.  
\- descripcio (TEXT) — Descripció del contingut.  
\- categoria (VARCHAR 50\) — Categoria per facilitar cerques.  
\- durada (INT) — Durada en segons.  
\- data\_publicacio (DATE) — Data de publicació.  
\- url\_streaming (VARCHAR 255\) — Enllaç directe al servidor d'streaming.  
\- paraules\_clau (TEXT) — Paraules clau per a cerques per títol, categoria o keywords, tal com demana l'enunciat.

**3.2.4 Anàlisi d'Amplada de Banda**

Taula: mesures\_amplada\_banda

Emmagatzema els resultats de les mesures d'amplada de banda.

\- id\_mesura (INT AUTO\_INCREMENT) — Clau primària.  
\- data\_hora (DATETIME) — Data i hora de la mesura.  
\- id\_usuari\_mesurat (INT) — Clau forana cap a usuaris\_comunicacio. Usuari o equip mesurat.  
\- id\_operari (INT) — Clau forana cap a usuaris\_comunicacio. Operari que ha realitzat la mesura.  
\- velocitat\_baixada (DECIMAL 10,2) — Velocitat de baixada en Mbps.  
\- velocitat\_pujada (DECIMAL 10,2) — Velocitat de pujada en Mbps.  
\- latencia (INT) — Latència en mil·lisegons.  
\- resultat (ENUM 'acceptable','no acceptable') — Classificació tal com indica l'enunciat.  
\- notes (TEXT) — Observacions addicionals de l'operari.

**3.2.5 Control d'Accés i Auditoria**

Taula: avisos

Taula de log d'auditoria on es registren els intents no autoritzats d'accés o modificació.

\- id\_avis (INT AUTO\_INCREMENT) — Clau primària.  
\- usuari (VARCHAR 100\) — Usuari que ha intentat l'acció.  
\- taula\_afectada (VARCHAR 100\) — Taula sobre la qual s'ha intentat l'operació.  
\- operacio (VARCHAR 50\) — Tipus d'operació (INSERT, UPDATE, DELETE).  
\- data\_hora (DATETIME) — Data i hora de l'intent.  
\- descripcio (TEXT) — Detalls addicionals de l'intent.

Taula: backup\_log

Registre dels events de backup realitzats automàticament.

\- id\_backup (INT AUTO\_INCREMENT) — Clau primària.  
\- data\_hora (DATETIME) — Data i hora del backup.  
\- taules\_incloses (TEXT) — Llista de taules copiades.  
\- resultat (ENUM 'ok','error') — Resultat del backup.  
\- fitxer\_generat (VARCHAR 255\) — Ruta del fitxer de backup generat.

**3.2.6 Gestió Comercial**

Taula: clients

Gestió dels clients externs de l'empresa que contracten els serveis d'InnovateTech.

\- id\_client (INT AUTO\_INCREMENT) — Clau primària.  
\- nom (VARCHAR 100\) — Nom del client.  
\- cognoms (VARCHAR 100\) — Cognoms del client.  
\- empresa (VARCHAR 150\) — Empresa a la qual pertany el client.  
\- correu (VARCHAR 100, UNIQUE) — Correu electrònic de contacte.  
\- telefon (VARCHAR 15\) — Telèfon de contacte.  
\- adreca (VARCHAR 200\) — Adreça completa del client.

Taula: productes

Catàleg de productes i serveis tecnològics oferts per l'empresa.

\- id\_producte (INT AUTO\_INCREMENT) — Clau primària.  
\- nom (VARCHAR 150\) — Nom del producte o servei.  
\- descripcio (TEXT) — Descripció detallada del producte.  
\- preu (DECIMAL 10,2, CHECK preu \>= 0\) — Preu unitari en euros.  
\- categoria (VARCHAR 50\) — Categoria del producte (Software, Seguretat, Backup, etc.).  
\- estoc (INT DEFAULT 0, CHECK estoc \>= 0\) — Unitats disponibles.

Taula: comandes

Registre de comandes realitzades pels clients.

\- id\_comanda (INT AUTO\_INCREMENT) — Clau primària.  
\- id\_client (INT) — Clau forana cap a clients. Client que realitza la comanda.  
\- data\_comanda (DATETIME DEFAULT CURRENT\_TIMESTAMP) — Data i hora de la comanda.  
\- estat (ENUM 'pendent','enviada','lliurada','cancel·lada') — Estat actual de la comanda.  
\- total (DECIMAL 10,2) — Import total de la comanda.

**3.2.7 Gestió Administrativa**

Taula: nomines

Gestió de nòmines mensuals dels empleats de l'empresa. 

\- id\_nomina (INT AUTO\_INCREMENT) — Clau primària.  
\- dni\_empleat (VARCHAR 9\) — Clau forana cap a empleats. Empleat al qual correspon la nòmina.  
\- mes (INT, CHECK mes BETWEEN 1 AND 12\) — Mes de la nòmina (1-12).  
\- any\_nomina (INT) — Any de la nòmina.  
\- salari\_base (DECIMAL 10,2) — Salari base mensual.  
\- complements (DECIMAL 10,2 DEFAULT 0\) — Complements salarials (antiguitat, productivitat, etc.).  
\- deduccions (DECIMAL 10,2 DEFAULT 0\) — Deduccions (IRPF, Seguretat Social, etc.).  
\- total (DECIMAL 10,2) — Import net a percebre (salari\_base \+ complements \- deduccions).

**Instal·lació de MySQL al servidor:** 

![MySQL](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/mysql.png?raw=true)

![MySQL status](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/mysqlstatus.png?raw=true)

Creació de la Base de Dades i taules.

![SHOW TABLES](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/showtabless.png?raw=true)

![MySQL 1](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/mysql1.png?raw=true)

![MySQL 2](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/mysql2.png?raw=true)

![MySQL 3](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/mysql3.png?raw=true)

![MySQL 4](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/mysql4.png?raw=true)

![MySQL 5](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/mysql5.png?raw=true)

![MySQL 6](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/mysql6.png?raw=true)

![MySQL 7](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/mysql7.png?raw=true)

Dades de prova inserides (inserts):

![INSERT1](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/insert1.png?raw=true)
![INSERT2](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/insert2.png?raw=true)
![INSERT3](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/insert3.png?raw=true)
![INSERT4](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/insert4.png?raw=true)
![INSERT5](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/insert5.png?raw=true)
![INSERT6](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/insert6.png?raw=true)
![INSERT7](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/insert7.png?raw=true)
![INSERT8](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/insert8.png?raw=true)
![INSERT9](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/insert9.png?raw=true)
![INSERT10](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/insert10.png?raw=true)


# 3.3 - Gestió d'Usuaris, Rols i Permisos

S’han creat 4 rols amb permisos diferenciats segons les funcions de cada tipus d’usuari.

**Rol "Admin"**  
Té accés total a totes les taules de la base de dades, pot crear, modificar i eliminar qualsevol estructura o dada. Está destinat al administrador de sistemes i de base de dades.

![ROL1](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/rol1.png?raw=true)

**Rol "Vendes"**  
Permisos de SELECT, INSERT i UPDATE sobre les taules relacionades amb la gestió comercial.

\- clients: Per gestionar els clients de l'empresa.  
\- comandes: Per registrar i actualitzar comandes.  
\- productes: Per consultar i modificar el catàleg.  
\- trucades: Per registrar les trucades amb clients.  
\- usuaris\_comunicacio (SELECT): Per consultar dades de contacte.

![ROL2](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/rol2.png?raw=true)

**Rol "Administracio"**  
Permisos de SELECT, INSERT i UPDATE sobre les taules de gestió de personal.

\- empleats: Gestió del personal intern.  
\- nomines: Gestió de nòmines mensuals.  
\- departaments: Estructura organitzativa.

![ROL3](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/rol3.png?raw=true)

**Rol "Treballador"**  
Permisos de SELECT (només consultas) 

\- productes: Consultar el catàleg.  
\- videos\_streaming: Accedir al catàleg de vídeos.  
\- configuracio\_qualitat i configuracio\_servidor: Consultar configuracions del sistema.

![ROL4](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/rol4.png?raw=true)

Comprovació:

![Comparativa roles](https://github.com/ITB2526GerardRomero/Pro-ASIXc1a-G5/blob/main/Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/rolcompr.png?raw=true)

# Script de creació automatitzada d'usuaris

Per al nostre projecte, hem creat una script que ens automatitza i simplifica enormement la tasca de donar d'alta nous treballadors al sistema.

El que fa aquest programa és guiar-nos pas a pas fent-nos unes poques preguntes bàsiques per pantalla, com el nom, el correu i el departament al qual pertany la persona. Perquè sigui més ràpid i còmode, el mateix sistema genera per nosaltres la informació restant, com ara assignar-li una extensió de telèfon aleatòria i un enllaç personal per a videotrucades.

De manera automàtica, la nostra eina s'encarrega de:

* **Validar les dades:** Revisar que no ens hàgim equivocat en escriure els correus, contrasenyes o departaments.
* **Gestionar els permisos:** Assignar a cada empleat exactament els accessos que necessita per treballar, basant-se en el seu lloc.
* **Crear l'usuari:** Donar d'alta la persona de forma real a la nostra base de dades perquè ja pugui començar a treballar.
* **Generar un registre:** Guardar una còpia escrita en un arxiu amb totes les operacions que s'han fet, per si necessitem revisar-les en el futur.

En resum, hem convertit una tasca que abans era manual i propensa a errors en un procés molt ràpid que fa tota la feina pesada per nosaltres.

![Script 01](/Imatges/Bloc%200377%20Administració%20de%20bases%20de%20dades/Scriptuser01.png)
![Script 02](/Imatges/Bloc%200377%20Administració%20de%20bases%20de%20dades/Scriptuser02.png)
![Script 03](/Imatges/Bloc%200377%20Administració%20de%20bases%20de%20dades/Scriptuser03.png)
![Script 04](/Imatges/Bloc%200377%20Administració%20de%20bases%20de%20dades/Scriptuser04.png)
![Script 05](/Imatges/Bloc%200377%20Administració%20de%20bases%20de%20dades/Scriptuser05.png)
![Script 06](/Imatges/Bloc%200377%20Administració%20de%20bases%20de%20dades/Scriptuser06.png)

# Control d'Accés i Auditoria (Triggers)

Per complir amb els requisits de seguretat de la base de dades, hem dissenyat un script que actua com un vigilant constant i automàtic [cite: 3]. Aquesta eina instal·la uns mecanismes interns, anomenats "triggers", que salten sols en el moment exacte en què algú intenta fer una acció que no toca o supera els seus límits. 

A continuació, detallem com la nostra eina dona resposta a cada punt demanat:

### 1. Control d'ús i bloquejos (Trucades)
El primer vigilant s'encarrega de controlar l'ús que cada persona fa del sistema de trucades [cite: 3]. Actua de manera preventiva just abans que es faci una nova trucada [cite: 1]:

*   **Límit de minuts i trucades diàries:** Revisa automàticament si l'usuari ha gastat tots els minuts que té assignats al mes o si ha superat el nombre màxim de trucades que pot fer en un sol dia [cite: 1, 2, 3]. Si és així, atura la trucada i guarda un avís explicant quin límit s'ha superat [cite: 1, 2, 3].
*   **Gestió d'usuaris bloquejats:** També comprova l'estat de la persona. Si per algun motiu el seu compte està marcat com a "bloquejat" (ja sigui temporalment o per sempre), el sistema li prohibeix fer la trucada i registra l'intent [cite: 1, 3].

### 2. Auditoria de Seguretat (Taula d'avisos)
Per garantir que ningú accedeix a informació confidencial, hem creat una taula especial on es guarden tots els avisos d'intents no permesos [cite: 3]. Hem configurat dos vigilants més per a aquesta tasca:

*   **Protecció de Nòmines:** Si algú que treballa a vendes o com a treballador ras intenta remenar a la taula de nòmines (que és informació sensible), el sistema li talla el pas immediatament [cite: 2, 3]. A l'instant, apunta a la nostra taula d'avisos qui ho ha intentat, què volia fer exactament, i l'hora i el dia de l'incident [cite: 2, 3].
*   **Protecció de Trucades:** De la mateixa manera, si un usuari de l'àrea d'administració intenta modificar les dades del sistema de trucades dels clients (cosa que no li correspon), el sistema ho bloqueja i deixa l'intent registrat a la taula d'auditoria [cite: 2, 3].

En resum, hem construït un sistema de defensa que funciona en segon pla, aturant qualsevol acció no permesa i deixant-ne constància per poder revisar-ho posteriorment.

![Trigger 01](/Imatges/Bloc%200377%20Administració%20de%20bases%20de%20dades/trigger01.png)

![Trigger 02](/Imatges/Bloc%200377%20Administració%20de%20bases%20de%20dades/trigger02.png)

![Trigger 03](/Imatges/Bloc%200377%20Administració%20de%20bases%20de%20dades/trigger03.png)

# 3.4 - Disseny Entitat-Relació i Model Relacional

Aqui es troba el diagrama del disseny relacional:

![Diagrama BD](../Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/Base%20de%20dades%20del%20projecte.png)
