# Projecte Transversal ASIXc - Innovate Tech

Aquest document unifica les diferents fases del projecte de transformació tecnològica i modernització per a l'empresa **Innovate Tech**. L'objectiu principal és proporcionar una base tecnològica sòlida que integri la infraestructura de maquinari i els serveis de xarxa per millorar la capacitat operativa i comunicativa de l'empresa.

---

## 1. Fonaments de Maquinari i Proposta de CPD (Bloc 0371)

Per tal de garantir la continuïtat del negoci i donar suport als serveis multimèdia, la primera fase del projecte se centra en el disseny i implementació d'un Centre de Processament de Dades (CPD) eficient, segur i sostenible.

**Ubicació Física del CPD \- Innovate Tech**

**1- Situació de la sala a l’edifici**

*Innova Tech* és una empresa de consultoria tecnològica i desenvolupament de software:

- 50-80 empleats  
- 4 departaments distribuïts en: Vendes, Suport tècnic, Administració i Logística.  
- Serveis que ofereix: Desenvolupament de software personalitzat, consultoria cloud, formació tècnica.  
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

Els dos racks estan col·locats cara a cara creant:

- Passadís fred: La part frontal dels racks, on el CRAC impulsa l’aire fred.  
- Passadís calent: La part posterior dels racks, on s’acumula l’aire calent que expulsen els servidors.

La funció del CRAC és, que aspira l’aire calent del passadís posterior, l’enfreda i el torna a impulsar al passadís frontal. Utilitzat aquest model l’aire fred no és barrella amb el calent, el CRAC treballa de forma eficient \= estalviant un 30-40% en refrigeració.

**3- Mesures per dificultar la identificació de la sala.**

Fora de l'edifici:

- No col·locar cartells informatius.  
- Les reixetes de ventilació del CRAC que donen a l’exterior, han de tenir el mateix disseny que la resta de ventilació general de l'edifici. 

Dintre de l’edifici:

- Que la porta del CPD, estigui sense identificar.  
- Ha d'haver-hi el mateix model porta que a la resta de portes de l’edifici.  
- Que la sala no aparegui en els plànols d'evacuació públics, només en documentació interna restringida.

Això es fa per dificultar possibles atacs d'enginyeria social, a més de complir amb la normativa ENS que obliga a no divulgar l'ubicació de instal·lacions crítiques.

**4- Distribució i gestió del cablejat**

En el CPD tenim dos tipus de cables:

Cables de dades (blaus):

- Connecten servidors, switches, sortida a internet.  
- Coure Cat 6A.
- Fibra òptica OM4 en el cas de que calgui connectar amb un altre edifici.

Cables elèctrics (negres):

- Conectant servidors, PDU, SAI.

Per normativa els cables de dades i elèctrics hauran de tenir una separació mínima de 30 cm, TIA942, ja que els cables electrònics generen camps electromagnètics i en el cas que un cable de dades passes a prop d’un cable elèctric es pot produir errors de transmissió, paquets corruptes, retransmissió o latència.

A més és important que cada cable tingui una etiqueta en els dos extrems, per identificar quin serà el seu origen i el seu destí, En un CPD amb més de 50 cables, si has de localitzar un cable en específic, seria massa complicat si no porten l’etiqueta.

**5- Terra tècnic i sostre tècnic.**

**Terra tècnic** és bàsicament un terra fals elevat uns 60 cm, damunt el terra real. En aquell forat, passen cables elèctrics i l’aire fred que expulsa el CRAC. A més té com a funció amagar el cablejat elèctric, d’aquesta manera no tenim tots els cables per terra i prevenim possibles accidents.  
Components:   
**sòl real:** El formigó original del soterrani.  
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

4- **Sensors de temperatura i humitat:** monitoren les condicions internes del rack. Connectats al sistema de monitoratge (CloudWatch, gestionat per Daniel).

5- **Patch panels (part superior):** on acaben els cables de dades. Permeten connectar/desconnectar equips sense manipular els cables fixos.

Seguretat física dels racks:

Cada un dels racks té un pany amb clau física en les portes frontal i posterior, de la qual només el personal autoritzat té accés a les claus, aquestes claus es guarden en una caixa de seguretat fora del CPD, a més de tindre un procediment de control d’accés, tindre un registre de qui obre el rack i quan.

Normatives aplicades:

- **ANSI/EIA-310-D:** Estàndard de racks de 19 polzades. 
- **TIA-942:** Infraestructura de telecomunicacions per a CPDs  
- **ISO/IEC 11801:** Cablejat genèric

### 1.2 Infraestructura IT

## **Infraestructura IT**

A continuació es descriura la infrastructura IT proposada per al CPD de Inova Tech basat en el pla de distribució presentat.

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
| Switch Gestió | TP-Link JetStream | 16 ports | Administració i monitoratje |

## **Característiques de xarxa**

VLANs separades.

QoS per a tràfic multimèdia.

STP/RSTP.

Link Aggregation.

Monitorizació SNMP.

# **Distribució dels racks**

La distribució física segueix una estructura optimizada per a:

* Refrigeració.  
* Mantenimentt.  
* Seguretat.  
* Escalabilitat.

## **Organizació de racks**

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
| U7 | Safata organitzaciṕ |
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

Escalabilitat.

Seguretat física y lógica.

Organizació professional del cablejat.

Compatibilitat amb AWS híbrid.

Optimizació energètica.

### 1.3 SAI

**Càlcul d’energia per a cada servidor:**

| Equip | Consum aproximat |
| :---- | :---- |
| 8 servidors | 8 x 200W \= 1600W |
| Switches | 150 W |
| Firewall | 100 W |
| NAS/backup | 400 W |

**Total:**

2600W

**Decidir autonomía:**

Exemple:

* 15 minuts,  
* 30 minuts,  
* 1 hora.

El normal en CPDs:

* 15-30 min.

Perquè:

* Després entra el generador,  
* o s'apaga controladament.

**Escollir SAI:**

Un SAI de:

* 3000VA  
* Normalment soporta \~2700W.

**Objectiu:**

Mantenir el CPD funcionant, després d’un tall elèctric, durant 20 minuts.

**Solució profesional:**

**SAI principal:**

Model:

* APC Smart-UPS 3000VA.

Capacitat:

* 2700W.

Autonomía:

* \~20-25 minuts a càrrega mitja.

Bateries:

2 mòduls de bateries redundants.

1 SAI principal \+ pack de expansió.

### 1.4 Seguretat Física, Lògica i Prevenció de Riscos

-  ## Seguretat física:   
  La seguretat física implica tenir el lloc vigilat 24/7 de diferents maneres, tenir objectes de detecció, les principals maneres de vigilància són:  
    
- Elements d’accés al CPD:

  Poder accedir a la sala del CPD només amb unes claus, targetes especials d’identificació o un factor de doble autenticació per a usuaris importants a l’empresa.


- Càmeres de seguretat i miralls:

  Les càmeres de seguretat serveixen per poder rastrejar qui entra a la sala del CPD, que fa dintre d’aquesta i durant quins períodes de temps ha estat dintre de la sala. El cas dels miralls convexos serveix per ajudar les càmeres a veure el que serien punts cecs sense elles.


- Sistemes de prevenció, detecció i extinció d’incendis:

  Per a prevenir cap incendi, principalment tenir climatització, ja que aquest permet que el CPD no se s'obreescalfi  i tingui problemes de temperatura, en qualsevol cas, també tenir un termòmetre per veure tant la temperatura com l’humitat.

  Per poder detectar en cas d'haver-hi algun objecte incendiat o que el mateix CPD estigui en llames utilitzar detectors de fum i detectors de calentor d’alta sensibilitat, com dit anteriorment un termòmetre.

  Per un altra part per a poder extingir l’incendi, tenir extintors de C02, ja que són els únics que van millor per apagar incendis elèctrics, el que és en aquest cas.


- Vies d’evacuació:

  Per a poder evacuar a la gent que hi hagi dintre, el més recomanat és posar una sortida d’incendis a l’altre costat de la sala, millor si aquesta es troba a lluny dels servidors del CPD, perquè no hi hagi objectes que poden interrompre el camí a aquesta.

- ## Seguretat lògica:  
  En canvi, la seguretat lògica ha de ser més rigorosa, ja que els servidors en un CPD contenen informació més valuós, és per això que aplicarem la següent seguretat:

- Restricció d’accés per autorització:

  Només es permet l’accés als servidors a usuaris específics i dels quals només es poden ficar certes persones amb les restriccions necessàries, i amb certs permisos.


- Firewalls:

  El firewall clarament ha d’estar actiu per tots els ports i només es pot permetre l’accés des de certs ordinadors i certs ports que seran els que utilitzaran els ordinadors per poder conectarse a aquest. És a dir, una filtració de ports i protocols.


- Mointoratge:

  Programes de monitoratge i recull de logs per poder veure, quin error succeeix, quan succeeix, i per què succeeix. En tot cas el programa de monitoratge, envia un missatge als ordinadors centrals quan ocorre algun error.


- ## Còpies de seguretat:

  Es fària principalment una còpia de seguretat base cada diumenge perquè, si es fastigueja alguna màquina, o es perd alguna cosa entre les màquines poder recuperar-la. I a part fer còpies diferencials diàries per poder fer un backup en el cas que passi alguna cosa, d’un dia l'altre.


- RAIDs:

  En el cas de les RAIDs, el que pensem que és més recomanable és fer una RAID 0+1, ja que en cas d'haver-hi algun problema les dades es poden recuperar de manera eficaç i ràpida.

- Prevenció de riscos laborals:  
  Quant a prevenció de riscos laborals, volem que els treballadors també portin seguretat, tant per a ells, com per al CPD.  
    
  Principalment, el terra i la roba que porten els treballadors han de ser aïllants d’electricitat perquè els treballadors no siguin electrocutats i els servidors no puguin patir cap tipus sobrecàrrega.  
    
  També es pot tenir en compte els riscos ergonòmics, per exemple, a l’hora de portar els servidors, o els racs, com tenen un alt pes el millor és utilitzar carros amb els quals es puguin portar aquests aparats.
    
  I podem evitar riscos ambientals, per exemple posar ventiladors per a poder evitar una temperatura molt alta i que així sigui estable, també es poden aplicar auriculars per controlar el soroll en el cas dels treballadors.  
    
    
- ## Maneres de fer això més sostenible:  
  Per poder fer que el CPD sigui sostenible es poden aplicar maneres, com per exemple:  
- Instal·lació de plaques solars per poder alimentar així el CPD.  
- Reutilització de l’aire utilitzat, sempre que es faci servir un filtre per poder netejar aquest aire, i així reutilitzar-ho.  
- Il·luminació mitjançant llums LED de baix consum  
- I apagar els equips no necessaris a les hores punta per què no consumeixin.


### 1.5 Implementació al Núvol (AWS)
 
## Ansible 
Primer de tot, per a què volem un servidor Ansible a part, el tenim ja que és el cervell de la nostra infraestructura, per començar en lloc d'estar entrant via SSH d'un en un als nostres servidors per configurar-los a mà, llencem els playbooks des d'Ansible i podrà treballar en totes les màquines alhora.  
Tindrem en aquest servidor fitxers .yml que són el backup dels nostres servidors, si el servidor web o syslog es trenquen ara mateix, podrem restaurar tota la instal·lació i configuració en menys de 30 segons.  
A més Ansible no necessita instal·lar programes pesats a les màquines dels nostres companys, es connecta via SSH que ja ve en la instal·lació fa els canvis i se'n va.

1.INSTAL·LACIÓ D'INSTÀNCIA  

Primer de tot hauré d'iniciar el Launch d'AWS.  

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/1-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/2-ansible.png)

Entrarem a AWS i seguidament anirem a l'apartat EC2.  

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/3-ansible.png)  

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/4-ansible.png)  

Una vegada aquí anirem a l'apartat d'“Instances” i llançarem una instància amb l'opció “Launch instances”.  

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/5-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/6-ansible.png)

Llançarem la instància en el sistema operatiu Ubuntu Server 24.04, amb el nom ANSIBLE.  

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/7-ansible.png)

Crearem les claus, perquè així els nostres companys puguin connectar-se al nostre servidor només passant-li la nostra clau.  
![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/8-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/9-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/10-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/11-ansible.png)
I amb tot configurat podrem llançar la nostra instància.  

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/12-ansible.png)

Podem veure com efectivament s'ha creat correctament.  

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/13-ansible.png)

Una vegada creada, el primer que farem serà assignar-li la IP elàstica perquè sigui estàtica i així no canviï de IP cada cert temps.  
Per a això ens dirigirem al menú de l'esquerra.
![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/14-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/15-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/16-ansible.png)

Una vegada creada i confirmant la seva correcta configuració, la hi assignarem al nostre servidor ansible anteriorment creat.  

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/17-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/18-ansible.png)

Veurem que s'ha associat correctament anant a les instàncies i veient la IP elàstica del nostre servidor.  

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/19-ansible.png)

Una vegada assignat hauré de connectar-me al servidor Ansible via SSH, però primer de tot hauré de canviar els permisos de la clau pública si inicio des d'Ubuntu.  

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/20-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/21-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/22-ansible.png)

Copio la commanda per després utilitzar-la, encara això he de canviar els permisos de la clau.

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/23-ansible.png)

Ara si, peguem la comanda copiada enteriorment.

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/24-ansible.png)

Una vegada dins de la màquina cambien tant el hostname, com la creació de l'usuario "administracio".

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/25-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/26-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/27-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/28-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/29-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/30-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/31-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/32-ansible.png)

Actualitzo la màquina.

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/33-ansible.png)

I instal·lo l'ansible.

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/34-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/35-ansible.png)

Creació de scripts.  

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/36-ansible.png)

Primer vaig a crear les claus de les màquines.

La del syslog  

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/37-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/38-ansible.png)

La de la web  

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/39-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/40-ansible.png) 

I la meva pròpia  

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/41-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/42-ansible.png)

Li cambio els permisos a les claus.

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/43-ansible.png)

Creació de l'arxiu de hosts.  

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/44-ansible.png)

Desactivar la verificació de claus d'Ansible.  

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/45-ansible.png)

Creación de scripts  

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/46-ansible.png)

Primer el web  

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/47-ansible.png)

Justificació:  

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/48-ansible.png)

Després el syslog. 

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/49-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/50-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/51-ansible.png)

![image1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/52-ansible.png)


## Servei de directori actiu per a guardar els usuaris.

Avanç de llançar la EC2, necesiten crear una clave SSH, per poder accedir a la máquina.

![Clau LDAP](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/Clau-ldap.png)

Una vegada creades el parell de claus, llencem la instancia del servidor amb les següents característiques:

![Instància AWS 1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/instancia1..png)

![Instància AWS 2](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/instancia2.png)

![Instància AWS 3](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/instancia3.png)

![Instància AWS 4](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/instancia4.png)

Ens connectem a la maquina via SSH.

![Accés SSH](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ssh-acceder.png)

**Centralització d’usuaris.**

Fixar el hostname.

![Hostname](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/hostname.png)

![Fitxer etc/hosts](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/etc-hosts.png)

**Instal·lació OpenLDAP.**

Utilitzem la comanda “sudo apt install \-y slapd ldap-utils”.

![Instal·lació slapd](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/install-slapd.png)

Configurem la contrasenya de l’administrador

![Admin contrasenya](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/admin-contra.png)

Verifiquem que s’ha fet la instal·lació correctament

![Status servei](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/status.png)

**Configuracions de Slapd.**

![Slapd evidència 1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd1.png)

![Slapd evidència 2](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd2.png)

![Slapd evidència 3](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd3.png)

![Slapd evidència 4](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd4.png)

![Slapd evidència 5](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd5.png)

![Slapd evidència 6](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd6.png)

Comprovació

![Comprovació slapd](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/comprobslapd.png)

**Creació d'usuari administrador, accés amb clau publica/privada.**

Fem la configuració necessària al fitxer, "sudo nano /etc/ssh/sshd_config".

![Admin SSH 1](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/adminssh1.png)

![Admin SSH 2](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/adminssh2.png)

Comprovació amb l'usurai administració.

![Admin Login](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/adminlogin.png)

## Implementació al núvol AWS - Web/SFTP

Primer, crearem un grup de seguretat, que permet tot el tràfic per aixì poder connectar-nos a la nostra pròpia màquina:

![Primera captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web01.png)

I comencem a crear la màquina, amb el nom pertinent i principalment escollim una AMI gratuïta ja que si no els terminen ràpidament:  
![Segona captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web02.png)

I com a targeta utilitzarem la t3.micro, ja que també és gratuïta:  
![Tercera captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web03.png)

Utilitzarem una nova par de claus, ja que aixì podem identificar bé la màquina i ficar-nos a ella:  
![Quarta captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web04.png)

I li ficarem al grup de seguretat creat anteriorment:  
![Quinta captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web05.png)

Tot seguit a això fem ssh per ficar-nos a la màquina:  
![Sexta captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web06.png)

Ara que ens hem ficat, crearem l'usuari de administració:  
![Septima captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web07.png)

I tot seguit li canviem la contrasenya i li afegim al grup root:  
![Octava captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web08.png) 
![Novena captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web09.png)

I les claus de l’usuari ec2 les copiem a la home de l'usuari “administracio”, ja que a partir d’ara ens ficarem a aquest:  
![Dècima captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web10.png)

I verifiquem que podem ficar-nos:  
![Decimaprimera captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web11.png)

Després d’això anem amb l’instal·lació de nginx:  
![Decimasegona captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web12.png)

I fem que el servei inici quan inici la màquina:  
![Tretzena captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web13.png)

I finalment pel SFTP, la màquina ja ve amb SFTP per defecte, i ho podem verificar amb la comanda pertinent:  
![Catorzena](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web14.png)

També podem verificar que funciona NGINX posant l'enllaç públic al navegador:
![Quinzena](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web15.png)

## AWS Syslog01

Creació de la instancia:

| Configuració | Valor |
| :---- | :---- |
| Nom | logs01 |
| SO | Ubuntu Server 24.04 |
| Tipo | t3.micro |
| IP privada | 10.0.1.30 |
| Seguretat | Port 514 obert |

![Primera captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog01.png)

Una vegada creades les claus pem., les guardem a la carpeta compartida del drive del grup i accedim a la maquina:

![Segona captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog02.png)

Ara instal·lem el servei que ens permetra realitzar els logs de tots els servidors:

![Tercera captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog03.png)

Ara editem el fitxer de configuració de logs del servidor /etc/rsyslog.conf i descomentarem algunas líneas:

![Cuarta captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog04.png)

Ara crearem les carpetes per als logs remots en el fitxer /etc/rsyslog.d/remote.conf :

![5 captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog05.png)

Això fa:

- una carpeta per servidor.  
- logs separats automàticament.

Reiniciem el servei:

![Sisena captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog06.png)

Per a la comprovació caldra instalar el rsyslog en els servidors i en el fitxer /etc/rsyslog.conf afegir la linea *.* @18.212.86.171:514 i despres reiniciar client sudo systemctl restart rsyslog i finalment veure en el cd /var/log/remote web01/ ldap01/ db01/


Finalment creem l'usuari administracio:

![Sisena captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog08.png)

Comprovacio del funcionament dels logs:

![Sisena captura](../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/syslog09.png)

---

## 2. Serveis de Xarxes i Internet: Àudio i Vídeo (Bloc 0375)

Un cop consolidada la infraestructura de maquinari (tant local com al núvol), el següent pas és desplegar els serveis que donaran suport a la comunicació interna i la formació corporativa d'Innovate Tech, recolzant-se sobre la base ja dissenyada.

### 2.1 Descripció General dels Serveis
Implementació d'una arquitectura multimèdia que suporti la distribució de continguts en streaming i eines de videoconferència en temps real, accessibles des de clients locals i navegadors web.

### 2.2 Implantació del Servei d'Àudio
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

Creació de la instància:

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio01.png)

Accedim a ella:

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio02.png)

Creació usuari administració:

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio03.png)

INSTALAR ICECAST2:

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio04.png)

Editem el fitxer de configuració del servei per a configurar el servei:

Contrasenyes:

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio05.png)

CAMBIAR HOSTNAME:

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio06.png)

ACTIVAR ICECAST:

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio07.png)

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio08.png)

Funcionament del servei:

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio09.png)

Per enviar l’audio a la pàgina utilitzem el servei ffmpeg.

Instal·lació:

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio10.png)

Una vegada descarregat el mp3, utilitzem la comanda següent indicant el audio la direcció de la pàgina i les credencials del usuari que permet pujar l’audio.

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio11.png)

Comprovació de que es pot escoltar l’audio desde la ruta:

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio12.png)

Execució de la comanda:

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio13.png)

# **PUNT DE CONTROL TRANSVERSAL — Amplada de banda**

## **Objectiu**

Analitzar el rendiment de xarxa disponible per comprovar si la infraestructura implementada és adequada per suportar els serveis multimèdia del projecte, especialment el servei d’àudio en streaming implementat amb Icecast2.

---

# **Proves de velocitat realitzades**

Per realitzar les proves de rendiment de xarxa s’ha utilitzat l’eina:

speedtest-cli

La prova es va executar directament des del servidor AWS EC2 on està implementat el servei d’àudio.

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio14.png)

![Primera captura](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/audio15.png)

# **Resultats obtinguts**

| Paràmetre | Resultat |
| ----- | ----- |
| Download | 1949.06 Mbit/s |
| Upload | 1869.21 Mbit/s |
| Latència | 6.502 ms |

Servidor de prova utilitzat:

Internet Subway (Richmond, VA)

---

# **Anàlisi dels resultats**

Els resultats obtinguts mostren un rendiment de xarxa molt elevat i una latència extremadament baixa.

La velocitat de descàrrega i pujada supera àmpliament els requisits necessaris per al servei d’àudio implementat.

El servei de streaming configurat utilitza codificació MP3 amb un bitrate aproximat de:

128 kbps (0.128 Mbps)

Comparant aquest consum amb l’ample de banda disponible:

| Element | Consum aproximat |
| ----- | ----- |
| Streaming d’àudio | 0.128 Mbps |
| Upload disponible | 1869 Mbps |

Es pot concloure que el consum del servei és pràcticament insignificant respecte a la capacitat disponible de la infraestructura AWS.

La latència de:

6.5 ms

És excel·lent per serveis en temps real i garanteix una reproducció estable sense talls ni interrupcions.

# **Relació amb els serveis multimèdia**

## **Servei d’àudio**

El servei d’àudio és el menys exigent en consum d’amplada de banda. El bitrate utilitzat permet reproducció estable fins i tot en connexions modestes.

# **Classificació del sistema**

## **Sistema acceptable**

La infraestructura implementada es considera plenament acceptable per oferir:

* Streaming d’àudio,  
* Serveis multimèdia,  
* Comunicacions en temps real.

Els resultats obtinguts garanteixen estabilitat i qualitat suficient per múltiples clients connectats simultàniament.

---

# **Propostes d’optimització**

Tot i els bons resultats obtinguts, es proposen les següents millores:

* Implementació de QoS per prioritzar tràfic multimèdia.  
* Utilització de compressió MP3 eficient.  
* Reducció del bitrate en connexions lentes.  
* Ús de connexions cablejades per reduir latència.  
* Balanceig de càrrega per suportar múltiples clients simultanis.  
* Monitorització contínua de l’ample de banda i latència.


### 2.3 Implantació del Servei de Vídeo i Videoconferència

Bloc 0375 Serveis de xarxes i internet

· Funcionalitat del servei de vídeo:

La funcionalitat que volem amb el servei de vídeo són varies, per exemple volem que:

- Els treballadors es puguin enviar vídeos en streaming entre si per poder veure com fan manteniment dels servidors.  
- Els treballadors puguin fer videoconferències en directe com a medida per fer una reunió en cas de que algu no estigui disponible.  
- Accés des de qualsevol navegador web.  
- Hi hagi compatibilitat amb videos moderns i antics, a part de que tinguin qualsevol tipus d'extensió.

Primer de tot crearem una altra màquina amb Ubuntu, que serà el servidor de video:

![Primera imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video01.png)

I, al igual que les altres màquines, li crearem un nou par de claus:

![Segona imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video02.png)

Ara per necessitat de la pràctica instal·lem el servei web de Nginx:

![Tercera imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video03.png)

Ara és quan començem amb la part de streaming. Principalment instalant el RTMP (Real-Time Messaging Protocol), que és qui ens permet poder fer la transmissió en directe desde l'aplicació dessitjada:

![Quarta imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video04.png)

I després d'això hem de configurar l'arxiu de configuració del Nginx per a que pugui utilitzar tant el RTMP, com el HLS, el qual aquest ultim ens permetrà poder observar el directe desde el navegador mitjançant uns petits troçets amb l'extensió m3u8:

![Quinta imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video05.png)
![Sisena imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video06.png)

Després d'haver configurat l'anterior ens anem a una gravadora, al nostre cas, el OBS Studio, y a la part de directe com a servidor posem l'enllaç RTMP del nostre servidor, amb la clau test, que és a ón es guarden com a tal els trosets d'aquell directe:

![Setena imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video07.png)

I demanat per la pràctica, al programa del OBS Studio, o el que sigui de gravació, i posem com a codificador el H264 i el format d'enregistrament com a MP4:

![11 imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video11.png)

Com hem configurat tot de manera correcta, no ens surt cap error a la hora de fer la transmissió i la podrem fer sense cap problema:

![Vuitena imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video08.png)

I ara si ens fiquem al següent enllaç (http://98.80.217.120:8080/hls/test.m3u8) podrem veure la transmissió en directe, cap aclarir que té un retard molt gran entre el que passa i el que surt al navegador:

![Novena imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video09.png)

També si observem la carpeta on hem especificat l'arxiu a on hem posat els arxius podem veure que s'han creat els diferents arxius:

![Dècima imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video10.png)

· Descripció del protocol de videoconferència:

WebRTC (Web Real-Time Communication) és un protocol o projecte open source que ens permet tenir una connexió a video, audio i de metadata de manera real. Aquest projecte permet als usuaris conectarse principalment des de navegadors, encara això també aplicacions mòbils per instal·lar.

Al nostre cas utilitzarem l’eina Jitsi Meet que al igual que WebRTC és un eina de videoconferènia i missatgeria instantànea que conté protocols de missatgeria instantània i telefonia populars.

A l’hora d’instal·lar l’eina hem visitat la seva pàgina web per veure com instal·lar-ho:  
https://jitsi.org/downloads/ubuntu-debian-installations-instructions/

Ara per a la part de videoconferència primer descarregarem el repositori jitsi des de la seva pàgina oficial i després li afegirem el repositori oficial al nostre ordinador:

![Instal jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video12.png)

Després instal·lem l'aplicació mitjançant apt:

![APT jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video13.png)

Ara el jitsi ens demana un nom de domini a la que posar, per a la hora de buscar la reunió pel navegador, tenir una mena de identificador, al nostre cas com no tenim un nom de domini ja que no tenim bind9 instal·lat, li posem que sigui simplement la IP pública de la màquina:

![Nom jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video14.png)

I com utilitza HTTPS li donem que encripti els certificats, no posem email i ni tampoc número de telèfon:

![Encriptació jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video15.png)

![Email jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video16.png)

![Telèfon jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video17.png)

I ara podrem verificar que funcionen les reunions si ens fiquem a l'adreça pertinent, com l'hem posat la IP elàstica al navegador també li posem la IP elàstica, també hem fet una prova des de el telèfon mòbil per veure que ens podem ficar des de un tercer:

![Verificiació jitsi imatge video](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video18.png)

Comprovacions d'amplada de banda:

Necessitarem instal·lar el servei de speedtest client per poder veure aixì la pujada i baixada en velocitat:

![Install speedtest](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video19.png)

Llavors primer anem a fer la verificació de la velocitat amb el Nginx desactivat, ja que és qui porta els serveis de streaming i videoconferència:

![Comprovació speedtest sense Nginx](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video20.png)

I verifiquem la latència:

![Ping](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video21.png)

Per ultim, anem a verificar la pujada i baixada amb els serveis actius, i mentre fa la transmissió, és a dir, activareme el Nginx:

![Comprovació speedtest amb Nginx](../Imatges/Bloc%200375%20Serveis%20de%20xarxes%20i%20internet/video22.png)

Amb aquestes dades hem pogut observar que aquest sistema si que pot ser necessari per a un CPD, en canvi, ha de ser un CPD simple i que no gasti molts recursos, en el cas contrari, ja sigui per a una empresa en la que gasti molts recursos, no es suficient. És a dir, que per portar coses petites com un servidor, docker entre altres, si que pot ser util.

Si volguessim utilitzar-ho per a una empressa llavors algunes millores per a la infraestructura podrien ser, per exemple, segmentació de xarxa, millora de hardware dels dispositius i una connexió multioperadora.


### 2.4 Comprovacions d'Amplada de Banda i Rendiment
*En aquest apartat s'ha de detallar:*
- Resultats de les proves de rendiment de xarxa: velocitat de baixada, pujada i latència.
- Anàlisi del comportament amb múltiples serveis actius (àudio i vídeo) per evitar degradació del servei.
- Classificació del sistema (Acceptable / No acceptable) i propostes de millora.

---

*(Nota: En la següent iteració del document s'incorporaran les seccions de Bases de Dades i Digitalització, unint l'estructura organitzativa i de seguretat).*
