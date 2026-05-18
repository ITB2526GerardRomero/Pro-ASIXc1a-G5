
## **Infraestructura IT**

A continuació es descriura la infrastructura IT proposada per al CPD de Inova Tech basat en el pla de distribució presentat.

**Pla general del CPD**

El CPD disposa d'una superfície de 20x20 metres, organitzada en:

- Zona principal de racks de servidors.  
- Zona de control i monitoratge.  
- Sistemes de climatització redundants.  
- Seguretat física mitjançant cambres i extintors.  
- Passadissos optimitzats per a manteniment i flux d'aire.

| Servidor | Función | Modelo Propuesto | CPU | RAM | Almacenamiento |
| ----- | ----- | ----- | ----- | ----- | ----- |
| WEB-SFTP | Web \+ SFTP | Dell PowerEdge R350 | 4 vCPU | 8 GB | 250 GB SSD |
| LDAP-AD | Directorio Activo | Dell PowerEdge R350 | 4 vCPU | 8 GB | 250 GB SSD |
| LOGS | Centralización de logs | HPE ProLiant DL360 | 4 vCPU | 16 GB | 500 GB SSD |
| AUDIO | Streaming de audio | Dell PowerEdge R250 | 2 vCPU | 4 GB | 120 GB SSD |
| VIDEO | Streaming de vídeo | HPE ProLiant DL380 | 8 vCPU | 16 GB | 1 TB SSD |
| JITSI | Videoconferencias | Dell PowerEdge R550 | 8 vCPU | 16 GB | 500 GB SSD |
| DATABASE | Base de datos | HPE ProLiant DL360 | 8 vCPU | 32 GB | RAID 1 SSD |
| ANSIBLE | Automatización | Dell PowerEdge R250 | 2 vCPU | 4 GB | 120 GB SSD |

# **Patch Panels**

Se utilizarán patch panels Cat6A para la distribución estructurada del cableado.

## **Características**

| Elemento | Cantidad | Características |
| ----- | ----- | ----- |
| Patch Panel Cat6A | 4 | 24 puertos RJ45 |
| Patch Panel Fibra | 2 | LC-LC multimodo |
| Organizadores de cable | 8 | Horizontal y vertical |
| Bandejas rack | 6 | Gestión de equipos |

## **Funciones**

* Organización del cableado estructurado.  
* Reducción de interferencias.  
* Facilitar mantenimiento.  
* Separación entre red de datos y administración.

# **Switches**

La infraestructura de red utiliza switches gestionables de nivel empresarial.

| Switch | Modelo | Puertos | Función |
| ----- | ----- | ----- | ----- |
| Core Switch | Cisco Catalyst 9200 | 48 puertos | Backbone principal |
| Switch Rack A | Cisco CBS350 | 24 puertos | Servidores producción |
| Switch Rack B | Cisco CBS350 | 24 puertos | Servicios multimedia |
| Switch Gestión | TP-Link JetStream | 16 puertos | Administración y monitorización |

## **Características de red**

VLANs separadas.

QoS para tráfico multimedia.

STP/RSTP.

Link Aggregation.

Monitorización SNMP.

# **Distribución de los racks**

La distribución física sigue una estructura optimizada para:

* Refrigeración.  
* Mantenimiento.  
* Seguridad.  
* Escalabilidad.

## **Organización de racks**

| Rack | Contenido |
| ----- | ----- |
| Rack A | Web, SFTP, LDAP |
| Rack B | Logs y monitorización |
| Rack C | Audio streaming |
| Rack D | Video streaming |
| Rack E | Jitsi Meet |
| Rack F | Base de datos |
| Rack G | Switches principales |
| Rack H | Patch panels |

# **Distribución interna de un rack**

## **Ejemplo de estructura de rack estándar**

| Posición U | Elemento |
| ----- | ----- |
| U1-U2 | Patch Panel |
| U3 | Switch |
| U4-U6 | Servidor |
| U7 | Bandeja organización |
| U8-U10 | Segundo servidor |
| U11 | PDU eléctrica |
| U12 | Espacio ventilación |

## **Flujo de conexión**

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

# **Distribución según el plano**

Según el plano del CPD:

* Los racks están distribuidos en filas con pasillos de mantenimiento.  
* Los sistemas de aire acondicionado (AA) están colocados estratégicamente para mantener flujo frío/caliente.  
* La zona de control y monitorización está aislada del área principal.  
* Las cámaras cubren entradas y pasillos críticos.  
* Los extintores están repartidos en esquinas y zonas centrales.

Esta distribución permite:

* Mejor circulación del aire.  
* Reducción de puntos calientes.  
* Acceso rápido para mantenimiento.  
* Seguridad física reforzada.

---

 **Justificación técnica**

La infraestructura propuesta cumple:

* Alta disponibilidad.

Escalabilidad.

Seguridad física y lógica.

Organización profesional del cableado.

Compatibilidad con AWS híbrido.

Optimización energética.
