● Implementació al núvol AWS (5 p)  
○ Ansible (1,5p)  
Primer de tot, per a què volem un servidor Ansible a part, el tenim ja que és el cervell de la nostra infraestructura, per començar en lloc d'estar entrant via SSH d'un en un als nostres servidors per configurar-los a mà, llencem els playbooks des d'Ansible i podrà treballar en totes les màquines alhora.  
Tindrem en aquest servidor fitxers .yml que són el backup dels nostres servidors, si el servidor web o syslog es trenquen ara mateix, podrem restaurar tota la instal·lació i configuració en menys de 30 segons.  
A més Ansible no necessita instal·lar programes pesats a les màquines dels nostres companys, es connecta via SSH que ja ve en la instal·lació fa els canvis i se'n va.

1.INSTAL·LACIÓ D'INSTÀNCIA  
Primer de tot hauré d'iniciar el Launch d'AWS.  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/1-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/2-ansible.png)
Entrarem a AWS i seguidament anirem a l'apartat EC2.  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/3-ansible.png)  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/4-ansible.png)  
Una vegada aquí anirem a l'apartat d'“Instances” i llançarem una instància amb l'opció “Launch instances”.  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/5-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/6-ansible.png)
Llançarem la instància en el sistema operatiu Ubuntu Server 24.04, amb el nom ANSIBLE.  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/7-ansible.png)
Crearem les claus, perquè així els nostres companys puguin connectar-se al nostre servidor només passant-li la nostra clau.  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/8-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/9-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/10-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/11-ansible.png)
I amb tot configurat podrem llançar la nostra instància.  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/12-ansible.png)
Podem veure com efectivament s'ha creat correctament.  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/13-ansible.png)
Una vegada creada, el primer que farem serà assignar-li la IP elàstica perquè sigui estàtica i així no canviï de IP cada cert temps.  
Per a això ens dirigirem al menú de l'esquerra.
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/14-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/15-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/16-ansible.png)
Una vegada creada i confirmant la seva correcta configuració, la hi assignarem al nostre servidor ansible anteriorment creat.  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/17-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/18-ansible.png)
Veurem que s'ha associat correctament anant a les instàncies i veient la IP elàstica del nostre servidor.  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/19-ansible.png)
Una vegada assignat hauré de connectar-me al servidor Ansible via SSH, però primer de tot hauré de canviar els permisos de la clau pública si inicio des d'Ubuntu.  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/20-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/21-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/22-ansible.png)
Copio el comando para luego utilizarlo, tendre que cambiar los permisos de la clave.  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/23-ansible.png)
Ahora si pegaremos el comando antes copiado  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/24-ansible.png)
Una vez entrado a la máquina cambiaremos tanto el hostname como la creación del usuario administracio.  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/25-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/26-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/27-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/28-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/29-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/30-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/31-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/32-ansible.png)
Actualizo la máquina  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/33-ansible.png)
Y instalo ansible
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/34-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/35-ansible.png)
Creación de scripts.  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/36-ansible.png)
Primero creo las claves de las maquinas
La del syslog  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/37-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/38-ansible.png)
La de la web  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/39-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/40-ansible.png) 
Y mi clave propia  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/41-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/42-ansible.png)
Le cambiare los permisos a ls claves.  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/43-ansible.png)
Creo el archivo hosts.  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/44-ansible.png)
Desactivar la verificación de claves en Ansible.  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/45-ansible.png)
Creación de scripts  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/46-ansible.png)
Primero el web  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/47-ansible.png)
Justificacion:  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/48-ansible.png)
Luego el de syslog  
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/49-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/50-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/51-ansible.png)
(../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/52-ansible.png)

