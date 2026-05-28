## Ansible 
### El paper central del nostre servidor Ansible

Hem implementat un servidor Ansible dedicat per actuar com el cervell i l'orquestrador de tota la nostra infraestructura. Els motius i avantatges principals d'aquesta decisió són els següents:

*   **Automatització eficient i centralitzada:** En lloc de connectar-nos manualment via SSH a cada servidor per configurar-los d'un en un, Ansible ens permet executar *playbooks*. Això significa que podem aplicar configuracions, actualitzacions i canvis a totes les màquines alhora de manera totalment automatitzada, estalviant temps i minimitzant els errors humans.
*   **Recuperació immediata (Infraestructura com a Codi):** Aquest servidor emmagatzema els fitxers de configuració `.yml`, els quals actuen com un registre i una còpia de seguretat exacta de com han d'estar configurats els nostres equips. Si un servei crític cau o es corromp (com el servidor web o el de *syslog*), aquests fitxers ens permeten restaurar i tornar a desplegar tota la instal·lació i configuració des de zero en menys de 30 segons.
*   **Arquitectura neta i sense agents:** Un dels grans avantatges d'Ansible és que no requereix instal·lar programari addicional o agents pesats als servidors de destí. Simplement aprofita el protocol SSH, que ja ve integrat de sèrie en els sistemes operatius, per connectar-se, aplicar els canvis de configuració necessaris i desconnectar-se, mantenint els equips de la infraestructura lleugers i segurs.


1.INSTAL·LACIÓ D'INSTÀNCIA  

Primer de tot hauriem d'iniciar el Launch d'AWS:  
![image1](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible1.png)

Crearem les claus, perquè així els nostres companys puguin connectar-se al nostre servidor només passant-li la nostra clau pública:

![image2](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible2.png)  

![image3](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible3.png)

Seleccionarem la clau abans creada como també l’edició de l’ordinador de lloguer que viu en un centre de dades d'Amazon, permetrem la conexió via SSH desde qualsevol lloc:

![image4](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible4.png)  

![image5](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible5.png)

![image6](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible6.png)

Llavors llançem l'instància:

![image7](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible7.png)

Una vegada creada, el primer que farem serà assignar-li la IP elàstica perquè sigui estàtica i així no canviï de IP cada cert temps.
Per a això ens dirigirem al menú de l'esquerra a l’apartat “Direcciones IP elásticas”.
I li associarem una nova IP elástica:

![image8](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible8.png)

![image9](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible9.png)

Comprovarem que la instància s'ha creat bé i que també té l'IP elàstica correctament assignada.

![image10](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible10.png)

Una vegada assignat hauré de connectar-me al servidor Ansible via SSH, però primer de tot hauré de canviar els permisos de la clau pública si inicio des d’Ubuntu amb la comanda chmod 400 clau-ansible.pem.

![image11](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible11.png)

Ara si enganxarem l'ordre abans copiada i veurem que efectivamente podrem conectar-nos.

![image12](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible12.png)

2.CONFIGURACIÓ DEL SERVIDOR

Un cop entrat a la màquina canviarem tant l'hostname com també crearem l'usuari “administracio” amb contrasenya “@ITB2026”.

![image13](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible13.png)

![image14](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible14.png)

![image15](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible15.png)

Una vegada hem fet la creació de l'usuari li copiarem les claus SSH de l'usuari ubuntu perquè pugui iniciar sessió sense contrasenya i afegirem al grup root.
A més, editem el fitxer sudoers per a concedir-li privilegis totals d'administrador (sudo) en el sistema.

![image16](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible16.png)

![image17](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible17.png)

Reiniciarem el servidor perquè es desin tots els canvis.

![image18](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible18.png)

Veurem que efectivament podem entrar sense contrasenya amb l'usuari creat prèviament i que té permisos de sudo.

![image19](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible19.png)

