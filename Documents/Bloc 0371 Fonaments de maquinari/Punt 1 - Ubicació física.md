**Ubicació Física del CPD \- Innovate Tech**

**1- Situació de la sala a l’edifici**

*Innova Tech* es una empresa de consultoría tecnológica i desenvolupament de software:

- 50-80 empleats  
- 4 departaments distribuïts en: Ventas, Suport tècnic, Administració i Logística.  
- Serveis que ofereix: Desenvolupament de software personalitzat, consultoria cloud, formació tècnica.  
- Clients: Son petites i mitjanes empresas (PYMES) o startups (empresas noves).

On estem ubicats?  
Tenim la seu en el **Districte 22@,Barcelona**, concretament en un edifici d’oficines de 4 plantes més un soterrani. Aquest districte es la zona de innovació tecnològica de Barcelona, on es concentren startups, consultores Tech i empreses de serveis digitals.

Ubicació CPD?  
EL CPD se ubicará en el soterrani  (planta \-1), on ocupará uns **48m² (8m x 6m)** amb una altura lliure de **3,5 metres**.

Hem escollit el soterrani per diverses raons:

- Temperatura estable:

En el soterrani, la temperatura varia només ±2°C durant tot l’any, això gràcies al **aïllament natural del subterra**. En una planta superior la variació seria més alta, ja que intervenen diferents factors como, el sol, el vent, els canvis d’estació, etc.  
Amb això fem que el sistema d’aire condicionat treballi menys per mantenir la temperatura adequada, menys consum energètic i més sostenible. 

- Protecció contra fenòmens meteorològics:

El CPD, no no tindrà finestres, llavors no hi ha risc de trencaments per el temps meteorològic, a més de no tindre exposició directa al vent, pluja o neu.  
En el cas de posible inundació urbana, el soterrani te sensors d'aigua connectats a la alarma.

- Seguretat fisica:

Difícil accés des de l’exterior, ja que no te finestres i portes directes a al carrer, l’únic accés és per l'interior de l'edifici, passant per control d’accés principal, amb això es redueix el risc de vandalisme o intrusió.

- Aïllament acústic: 

El sistema d’aire condicionat fa soroll (50-70dB), El soterrani aquest soroll no afecta a les oficines de la planta superiors o als veïns, el empleat poden treballar tranquils.

   
**2- Sistemes de climatització (aire condicionat). Nivells de temperatura, humitat i**  
**neteja de l’aire.**

Hem instal·lat **2 unitats CRAC** (Computer Room Air Conditioning) de 10kW cadascun. No hem escollit un aire condicionat domestic ja que aquest mantenen la temperatura amb una precisió de ±3°C i un CRAC profesional la manté en ±1°C.  
Es de importancia escollir l’opció correcta ja que el servidors son sensibles, si la temperatura puja a 30°C, el servidor es pot apagar automàticament per protegir se. En una empresa que ofereix servei 24/7 a clients, un apagó de servidors es sinónim de perdudas de diner i reputació.

Hem ficat 2 unitats:

- 1 CRAC esta actiu tot el temps, cobrint els 3,5kW que generan el nostres servidors.  
- 1 CRAC esta en standby, en el cas que falli el primer, el segon s’activa automàticament en menys de 30 segons.

Temperatura objectiu, **22°C** (el rang permès: 18-27°C segons la normativa **ASHRAETC 9.9**).  
Hem especificat els 22°C ya que cada grau per sota, incrementa el consum elèctric un 4%.

En el cas de ficar la CPD a 18°C, es dir 4°C menys:

- Consum extra: 4°C x 4% \= 16% mes electricitat  
- Cost anual extra: \~1.200€  
- Impacte ambiental: \+1,5 tonas CO₂/año

En conclusió mantenir la CPD en 22°C es l’equilibri entre seguretat tèrmica i eficiencia energetica.

**Humitat relativa**, un 50% (rang permès: 46-60%)

La humitat és molt important, si la es **inferior de 40%**:

- L’aire és massa sec.  
- Es genera electricitat estàtica.  
- Es poden espatllar component electronics a causa d’espurnes.

Si es **superior a 60%**:

- L’aire està massa humit.  
- Es forma condensació i això genera gotes d’aigua.  
- Aigua \+ electricitat \= curtcircuit.

El nostre CRAC te un humidificador/deshumidificador integrat que ajusta automàticament.  
Per a la **neteja de l’aire**, tenen filtres **HEPA H13** (retenen el 99,95% de partícules de 0,3 micres o més gran).

És de molta importància tenir un aire net, ja que la pols s’acumula en els ventiladors i dispersors dels servidors i actua com aïllador tèrmic.

- Canviem els filtres cada 6 mesos   
- Els servidors es mantenen nets durant 2-3 anys sense necessitat d’orbirlos.  
- Allarguem la seva vida útil un 40%.

Configuració del passadís fred/calent.

Els dos racks estan col·locats cara a cara creant:

- Passadís fred: La part frontal dels racks, on el CRAC impulsa l’aire fred.  
- Passadís calent: La part posterior dels racks, on s’acumula l’aire calent que expulsan els servidors.

La funció del CRAC es, que aspira l’aire calent del passadís posterior, l’enfreda y el torna a impulsar al passadís frontal. Utilizat aquest model l’aire fred no es barrella amb el calent, el CRAC treballa de forma eficient \= estalviant un 30-40% en refrigeració.

**3- Mesures per dificultar la identificació de la sala.**

Fora del edifici:

- No colocar cartells informatius.  
- Les reixetes de ventilació del CRAC que donen a l’exterior, tinguin el mateix diseny que la resta de ventilació general de l'edifici. 

Dintre de l’edifici:

- La porta del CPD, estigui sense identificar.  
- Mateix model a la resta de portes de l’edifici.  
- Que la sala no apareix en el plànols d'evacuació públics, només en documentació interna restingida.

Això es fa per dificultar posibles atacs d'enginyeria social, a més de complir amb la normativa ENS que obliga a no divulgar la ubicación de instalacións critiques.

**4- Distribució i gestió del cablejat**

En el CPD tenim dos tipus de cables:

Cables de dades (blaus):

- Conectan servidors, switches, sortida a internet.  
- Coure Cat 6A  
- Fibra óptica OM4 en el cas que es necessiti connectar amb un altre edifici.

Cables elèctrics (negres):

- Conectan servidors, PDU, SAI

Per normativa els cables de dades i elèctrics hauran de tenir una separació mínima de 30cm, TIA942, ja que els cables electronics generen camps electromagnètics i en el cas de que un cable de dades passes a prop d’un cable elèctric es pot produir errors de transmissió, paquets corruptes, retransmisión o latència.

A més és important que cada cable tingui una etiqueta en els dos extrems, per identificar quien será el seu origen y el seu destí, En un CPD amb més de 50 cables, si tens que localitzar un cable es específic, seria massa complicat si no porten l’etiqueta.

**5- Terra tècnic i sostre tècnic.**

**Terra tècnic** és bàsicament un terra fals elevat uns 60 cm, damunt el terra real. En aquell forat, passen cables elèctrics i l’aire fred que expulsa el CRAC. A més té com a funció amagar el cablejat electric, d’aquesta manera no tenim tots els cables per terra i prevenim possibles accidents.  
Components:   
**sòl real:** El formigó original del soterrani.  
**Estructura metálica:** Potes ajustables de 60 cm d’altura.  
**Panels:** Plaques d’acer galvanitzat de 60x60 cm que es colocan sobre de l’estructura.  
**Reixetes:** Algunos panels tenen forats per on surt l’aire fred.

**Sostre tècnic**, es una estructura suspesa a uns centímetres per sota del sostre original, té una distància d’uns 3 metres sobre el terra tècnic. Una de les seves funcions es, recollir l’aire calent ja què puja (l’aire calent és més lleuger) entra al sostre tècnic y el CRAC aspira aquest, l’enfreda i el torna a impulsar al terra tècnic. També passen cables de dades, com ja hem comentat el cables de dades aniran separats dels elèctrics que van per terra.  
Components:  
**Panels modulars:** Fets d’alumini ignífug (no crema en cas d’incendi).  
**Classificació:** MO (material no combustible segons normativa europea).

**6- Planells, dibuixos, diagrames dels elements anteriorment citats.**

**Plànol de planta del CPD**

![Plànol de planta del CPD](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/planta-cpd.png)

Vista superior de la sala mostrant la disposició dels 2 racks en configuració passadís fred/calent, les 2 unitats CRAC i la porta d'accés.

**Tall lateral - flux d'aire**

![Tall lateral - flux d'aire](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/flux-aire2.png)

Cicle complet de refrigeració mostrant com l'aire fred surt del terra tècnic, passa pels servidors, i torna al CRAC pel sostre tècnic.

**Distribució del cablejat**

![Distribució del cablejat](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/cablejat.png)

Separació física de 50 cm entre el cablejat de dades (sostre tècnic) i el cablejat elèctric (terra tècnic).

**7- Estructuració dels racks (mínim 2 racks).**

![Vista frontal dels racks](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/racks-frontal.png)

Hem instal·lat 2 racks de 42U del model APC NetShelter SX, tenen 600 mm d’ample exterior amb interior estándar de 19 polzades, 1.070 mm de fons, soportan 1.360 kg de càrrega, portes perforades i pany.

Cada rack té:

1- **PDU intel·ligent (1U a la part inferior, U5-1):** regleta vertical amb 24 endolls C13 i monitorització de consum elèctric individual per presa. Permet veure quin equip consumeix quant des dun panell web.

2- **Organitzadors de cables** **(1U entre zones):** mantenen el cablatge ordenat. Sense ells, en 6 mesos el rack és un embull de cables.

3- **Panells cecs (a totes les U buides):** bloquegen el pas d'aire per les U no ocupades. Mantenen el flux dʻaire correcte entre passadís fred i calent.

4- **Sensors de temperatura i humitat:** monitoren les condicions internes del rack. Connectats al sistema de monitorització (CloudWatch, gestionat per Daniel).

5- **Patch panels (part superior):** on acaben els cables de dades. Permeten connectar/desconnectar equips sense manipular els cables fixos.

Seguretat física del racks:

Cada un dels racks té un pany amb clau fisica en les portes frontal i posterior, de la qual només el personal autoritzat té accés a les claus, aquestes claus es guarden en una caixa de seguretat fora del CPD, a més de tindre un procediment de control d’acceś, tindre un registre de qui obre el rack i quan.

Normatives aplicades:

- **ANSI/EIA-310-D:** Estàndard de racks de 19 polzades  
- **TIA-942:** Infraestructura de telecomunicacions per a CPDs  
- **ISO/IEC 11801:** Cablejat genèric
