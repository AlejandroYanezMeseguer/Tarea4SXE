# Tarea4SXE

### En esta practica aprenderemos a instalar y configurar wordpress

#### 1. Utiliza la imagen de Ubuntu , tag 22 y apoyandote en esta guía sigue sus instrucciones para instalar LAMP en dicho contenedor.

##### Lo primero que haremos sera bajar la imagen de ubuntu indicada en el enunciado con el siguiente comando
´´´
sudo docker pull ubuntu:22.04       #Copiar para bajar la imagen de ubuntu
´´´

##### Ahora crearemos e iniciaremos el contenedor Para instalar todo lo necesario
```
sudo docker container create -i -t  -p  8080:80 --name WordPress ubuntu:22.04    #Copiar para crear el contenedor

sudo docker container start --attach -i  WordPress        #Copiar para iniaciar el contenedor
```

##### Una vez creado el contenedor seguiremos la guia empezando por actualizar los paquetes
```
sudo apt update    #Copiar para actualizar paquetes
```

##### Instalamos apache2 Usando el siguiente comando
```
sudo apt install -y apache2 apache2-utils    #Copiar para instalar apache
```

##### Instalamos mariaDB y lo iniciamos
```
sudo apt install -y mariadb-server mariadb-client     #Copiar para instalar el servicio de mariDB

service mariadb start     #Copiar para iniciarlo
```

##### Hacemos la instalacion segura de mysql
```
sudo mysql_secure_installation      #Copiar para hacer la instalacion de msql
```

##### Por ultimo instalamos php y lo configuramos en un meno que nos pedira de que region somos
```
sudo apt install -y php php-mysql libapache2-mod-php
```
##### Para comporbar que php funciona pondremos lo siguiente en el navegador
```
http://10.0.2.15/info.php
```

