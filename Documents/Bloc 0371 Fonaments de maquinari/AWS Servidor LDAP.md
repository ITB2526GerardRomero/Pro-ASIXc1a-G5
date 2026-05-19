**· Servei de directori actiu per a guardar els usuaris.**

Avanç de llançar la EC2, necesiten crear una clave SSH, per poder accedir a la máquina.

![Clau LDAP](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/Clau-ldap.png)

Una vegada creades el parell de claus, llencem la instancia del servidor amb les següents característiques:

![Instància AWS 1](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/instancia1..png)

![Instància AWS 2](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/instancia2.png)

![Instància AWS 3](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/instancia3.png)

![Instància AWS 4](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/instancia4.png)

Ens connectem a la maquina via SSH.

![Accés SSH](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/ssh-acceder.png)

**Centralització d’usuaris.**

Fixar el hostname.

![Hostname](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/hostname.png)

![Fitxer etc/hosts](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/etc-hosts.png)

**Instal·lació OpenLDAP.**

Utilitzem la comanda “sudo apt install \-y slapd ldap-utils”.

![Instal·lació slapd](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/install-slapd.png)

Configurem la contrasenya de l’administrador

![Admin contrasenya](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/admin-contra.png)

Verifiquem que s’ha fet la instal·lació correctament

![Status servei](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/status.png)

**Configuracions de Slapd.**

![Slapd evidència 1](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd1.png)

![Slapd evidència 2](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd2.png)

![Slapd evidència 3](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd3.png)

![Slapd evidència 4](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd4.png)

![Slapd evidència 5](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd5.png)

![Slapd evidència 6](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/slapd6.png)

Comprovació

![Comprovació slapd](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/comprobslapd.png)

**Creació d'usuari administrador, accés amb clau publica/privada.**

fem la configuració necessària al fitxer, "sudo nano /etc/ssh/sshd_config".

