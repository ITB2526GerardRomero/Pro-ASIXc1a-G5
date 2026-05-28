## Servei de directori actiu per a guardar els usuaris.

Avanç de llançar la EC2, necesiten crear una clave SSH, per poder accedir a la instància:

![Clau LDAP](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/Clau-ldap.png)

Una vegada creades el parell de claus, llencem la instància del servidor amb les següents característiques:

![Instància AWS 1](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/instancia1..png)

![Instància AWS 2](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/instancia2.png)

![Instància AWS 3](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/instancia3.png)

![Instància AWS 4](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/instancia4.png)

Ens connectem a la instància via SSH:

![Accés SSH](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ssh-acceder.png)

**Centralització d’usuaris.**

Modifiquem el hostname:

![Hostname](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/hostname.png)

![Fitxer etc/hosts](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/etc-hosts.png)

**Instal·lació OpenLDAP.**

Utilitzem la comanda “sudo apt install \-y slapd ldap-utils”:

![Instal·lació slapd](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/install-slapd.png)

Configurem la contrasenya de l’administrador:

![Admin contrasenya](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/admin-contra.png)

Verifiquem que s’ha fet la instal·lació correctament:

![Status servei](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/status.png)

**Configuracions de Slapd.**

![Slapd evidència 1](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd1.png)

![Slapd evidència 2](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd2.png)

![Slapd evidència 3](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd3.png)

![Slapd evidència 4](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd4.png)

![Slapd evidència 5](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd5.png)

![Slapd evidència 6](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd6.png)

Comprovació:

![Comprovació slapd](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/comprobslapd.png)

**Creació d'usuari administrador, accés amb clau publica/privada.**

Fem la configuració necessària al fitxer, "sudo nano /etc/ssh/sshd_config":

![Admin SSH 1](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/adminssh1.png)

![Admin SSH 2](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/adminssh2.png)

Comprovació amb l'usurai administració:

![Admin Login](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/adminlogin.png)

# Estructura d'Usuaris del Directori LDAP
 
## Fitxer de creació d'usuaris (`usuarios.ldif`)
 
![usuarios.ldif](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/estruct04.png)
 
Els 4 usuaris s'han creat mitjançant el fitxer `~/usuarios.ldif`. Cada entrada defineix els atributs necessaris per al funcionament del compte al sistema i al directori:
 
- **`objectClass: inetOrgPerson`** — dades personals (nom i cognoms).
- **`objectClass: posixAccount`** — integració Unix (UID, GID, shell, directori home).
- **`objectClass: shadowAccount`** — gestió de contrasenyes.
Tots comparteixen `gidNumber: 10000`, `loginShell: /bin/bash` i `userPassword: @ITB2026`.
 
---
 
## Estructura completa del directori
 
![ldapsearch complet](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/estruct01.png)
 
El directori LDAP s'organitza sota `dc=innovatetech,dc=local` amb dues unitats organitzatives:
 
```
dc=innovatetech,dc=local
├── ou=usuaris   → conté els 4 usuaris del grup
└── ou=grups     → reservat per a grups de treball
```
 
Cada usuari té un `uidNumber` únic i el seu propi `homeDirectory`.
 
---
 
## Verificació dels usuaris creats
 
![ldapsearch usuaris](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/estruct02.png)
 
Es confirma que els 4 usuaris estan correctament registrats a `ou=usuaris,dc=innovatetech,dc=local`:
 
| uid | Nom complet | uidNumber |
|---|---|---|
| elian | Elian Salvador | 10001 |
| gerard | Gerard Romero | 10002 |
| daniel | Daniel Roblas | 10003 |
| elias | Elias Martinez | 10004 |
 
---
 
## Estat del servei OpenLDAP
 
![slapd status](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/estruct03.png)
 
El servei `slapd` es troba en estat **active (running)**. La versió instal·lada és OpenLDAP `2.6.10` sobre Ubuntu 24.04, en funcionament des de l'inici del servidor.
