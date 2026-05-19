**· Servei de directori actiu per a guardar els usuaris.**

Avanç de llançar la EC2, necesiten crear una clave SSH, per poder accedir a la máquina.

\[Foto creación de claves\]

Una vegada creades el parell de claus, llencem la instancia del servidor amb les següents característiques:

\[Fotos instancia1234\]

Ens connectem a la maquina via SSH.

\[ssh-acceder\]

**Centralització d’usuaris.**

Fixar el hostname.

\[hostname\]  
\[etc-hosts\]

**Instal·lació OpenLDAP.**

Utilitzem la comanda “sudo apt install \-y slapd ldap-utils”.

\[install-slapd\]

Configurem la contrasenya de l’administrador

\[admin-contra\]

Verifiquem que s’ha fet la instal·lació correctament

\[status\]

**Configuracions de Slapd.**

\[slapd123456\]

Comprovació

\[comprobslapd\]

