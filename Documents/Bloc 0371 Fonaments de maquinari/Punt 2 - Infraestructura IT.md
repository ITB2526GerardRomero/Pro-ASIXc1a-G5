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
