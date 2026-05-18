## Implementació al núvol AWS - Web/SFTP

Primer, crearem un grup de seguretat, que permet tot el tràfic per aixì poder connectar-nos a la nostra pròpia màquina:

![Primera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web01.png)

I comencem a crear la màquina, amb el nom pertinent i principalment escollim una AMI gratuïta ja que si no els terminen ràpidament:  
![Segona captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web02.png)

I com a targeta utilitzarem la t3.micro, ja que també és gratuïta:  
![Tercera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web03.png)

Utilitzarem una nova par de claus, ja que aixì podem identificar bé la màquina i ficar-nos a ella:  
![Quarta captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web04.png)

I li ficarem al grup de seguretat creat anteriorment:  
![Quinta captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web05.png)

Tot seguit a això fem ssh per ficar-nos a la màquina:  
![Sexta captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web06.png)

Ara que ens hem ficat, crearem l'usuari de administració:  
![Septima captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web07.png)

I tot seguit li canviem la contrasenya i li afegim al grup root:  
![Octava captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web08.png) 
![Novena captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web09.png)

I les claus de l’usuari ec2 les copiem a la home de l'usuari “administracio”, ja que a partir d’ara ens ficarem a aquest:  
![Dècima captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web10.png)

I verifiquem que podem ficar-nos:  
![Decimaprimera captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web11.png)

Després d’això anem amb l’instal·lació de nginx:  
![Decimasegona captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web12.png)

I fem que el servei inici quan inici la màquina:  
![Tretzena captura](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web13.png)

I per últim pel SFTP, la màquina ja ve amb SFTP per defecte, i ho podem verificar amb l\< comanda pertinent:  
![Catorzena](../../Imatges/Bloc%200371%20Fonaments%20de%20maquinari/web14.png)