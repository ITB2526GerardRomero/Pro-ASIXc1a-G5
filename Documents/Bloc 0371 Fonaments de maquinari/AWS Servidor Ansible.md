Dues de les màquines (com a mínim) han d’estar configurades amb Ansible  
(incloent tota la configuració feta al servidor).  
Primer de tot, per a què volem un servidor Ansible a part, el tenim ja que és el cervell de la nostra infraestructura, per començar en lloc d'estar entrant via SSH d'un en un als nostres servidors per configurar-los a mà, llencem els playbooks des d'Ansible i podrà treballar en totes les màquines alhora.
Tindrem en aquest servidor fitxers .yml que són el backup dels nostres servidors, si el servidor web o syslog es trenquen ara mateix, podrem restaurar tota la instal·lació i configuració en menys de 30 segons tant de la instancia com del servei.
A més Ansible no necessita instal·lar programes pesats a les màquines dels nostres companys, es connecta via SSH que ja ve en la instal·lació fa els canvis i se'n va.

1.INSTAL·LACIÓ D'INSTÀNCIA

Primer de tot hauré d'iniciar el Launch d'AWS per fer llençar les instàncies, entrarem a AWS i seguidament anirem a l'apartat EC2.
Una vegada aquí anirem a l'apartat d'“Instances” i llançarem una instància amb l'opció “Launch instances”.
Escollirem el sistema operatiu Ubuntu Server 24.04, amb el nom ANSIBLE.
![image1](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible1.png)

Crearem les claus, perquè així els nostres companys puguin connectar-se al nostre servidor només passant-li la nostra clau pública.

![image2](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible2.png)  
![image3](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible3.png)

Seleccionarem la clau abans creada como també l’edició de l’ordinador de lloguer que viu en un centre de dades d'Amazon, permetrem la conexió via SSH desde qualsevol lloc.

![image4](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible4.png)  
![image5](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible5.png)
![image6](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible6.png)

I amb tot configurat podem llençar la nostra instància amb l’opció “Lanzar instancia”que ens apareix a la dreta .

![image7](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ansible7.png)

Una vegada creada, el primer que farem serà assignar-li la IP elàstica perquè sigui estàtica i així no canviï de IP cada cert temps.
Per a això ens dirigirem al menú de l'esquerra a l’apartat “Direcciones IP elásticas”.
I ens associarem una nova IP elástica.

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

