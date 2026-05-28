## Ansible 
### El paper central del nostre servidor Ansible

Hem implementat un servidor Ansible dedicat per actuar com el cervell i l'orquestrador de tota la nostra infraestructura. Els motius i avantatges principals d'aquesta decisió són els següents:

*   **Automatització eficient i centralitzada:** En lloc de connectar-nos manualment via SSH a cada servidor per configurar-los d'un en un, Ansible ens permet executar *playbooks*. Això significa que podem aplicar configuracions, actualitzacions i canvis a totes les màquines alhora de manera totalment automatitzada, estalviant temps i minimitzant els errors humans.
*   **Recuperació immediata (Infraestructura com a Codi):** Aquest servidor emmagatzema els fitxers de configuració `.yml`, els quals actuen com un registre i una còpia de seguretat exacta de com han d'estar configurats els nostres equips. Si un servei crític cau o es corromp (com el servidor web o el de *syslog*), aquests fitxers ens permeten restaurar i tornar a desplegar tota la instal·lació i configuració des de zero en menys de 30 segons.
*   **Arquitectura neta i sense agents:** Un dels grans avantatges d'Ansible és que no requereix instal·lar programari addicional o agents pesats als servidors de destí. Simplement aprofita el protocol SSH, que ja ve integrat de sèrie en els sistemes operatius, per connectar-se, aplicar els canvis de configuració necessaris i desconnectar-se, mantenint els equips de la infraestructura lleugers i segurs.


1. Instal·lació d'instància 

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

Comprovació:

![image10](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible10.png)

Es copia la commanda per després utilitzar-la, encara això, he de canviar els permisos de la clau:

![image11](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible11.png)

Ara si, peguem la comanda copiada enteriorment que ens permetrà accedir a la instància:

![image12](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible12.png)

2.CONFIGURACIÓ DEL SERVIDOR

Una vegada dins de la instància primer cambiem el hostname, i després creem l'usuari "administracio" amb contrasenya “@ITB2026”:

![image13](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible13.png)

![image14](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible14.png)

![image15](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible15.png)

Una vegada hem fet la creació de l'usuari li copiem les claus SSH de l'usuari ubuntu perquè pugui iniciar sessió sense contrasenya, a part d'això l'afegim al grup root junt a ficar-ho al fitxer sudoers per concedir privilegis d'administrador:

![image16](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible16.png)

![image17](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible17.png)

Reiniciem el servidor perquè es desin tots els canvis:

![image18](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible18.png)

I veiem que efectivament podem entrar sense contrasenya amb l'usuari creat prèviament i que té permisos de sudo:

![image19](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible19.png)

3.ACTUALITZACIÓ I INSTAL·LACIÓ D'ANSIBLE

Actualitzarem la llista de paquets del sistema i instal·larem les eines necessàries per poder llançar les instàncies d'AWS mitjançant els playbooks.

![image19](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible20.png)

![image19](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible21.png)

4.CREACIÓN , EJECUCIÓN Y COMPROBACION DE PLAYBOOK DEL SERVIDOR WEB

Primero tengo que coger las credenciales de mi compañero que me habra pasado

![image19](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible22.png)

![image19](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible23.png)

![image19](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible24.png)

![image19](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible25.png)

![image19](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible26.png)

![image19](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible27.png)

![image19](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible28.png)

![image19](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible29.png)

![image19](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible30.png)

![image19](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible31.png)

