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

# 3.4 - Disseny Entitat-Relació i Model Relacional

Aqui es troba el diagrama del disseny relacional:

![Diagrama BD](../../Imatges/Bloc%200377%20Administraci%C3%B3%20de%20bases%20de%20dades/Base%20de%20dades%20del%20projecte.png)
