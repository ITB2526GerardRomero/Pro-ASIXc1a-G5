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
