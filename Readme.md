<div align="center">

# DOCKER

</div>

<br>

<div align="center">

## 1. Descarga la imagen "alpine" SIN ARRANCARLA y comprueba que está en tu equipo

</div>

**`sudo docker pull alpine`**

El primer comando descarga la imagen de Alpine.

**`sudo docker images`**

Con el segundo comando visualizamos la imagen sin arrancarla.

<br>

<div align="center">

## 2. Crea un contenedor sin ponerle nombre. ¿Está arrancado? Obtén el nombre

</div>

**`sudo docker run alpine`**

Con este comando creamos un contenedor sin nombre y sin arrancar.

**`sudo docker ps -a`**

Con este comando visualizamos los contenedores que tenemos.

<br>

<div align="center">

## 3. Crea un contenedor con el nombre 'dam_alp1'. ¿Cómo puedes acceder a él?

</div>

**`sudo docker run --name dam_alp1 -it alpine`**

Con este comando creo un contenedor con el nombre `dam_alp1`.

**`sudo docker container start -- dam_alp1`**

Con este comando arranco el contenedor.

**`sudo docker exec -it dam_alp1 sh`**

Con este comando accedo al contenedor.

<br>

<div align="center">

## 4. Comprueba qué IP tiene y si puedes hacer un ping a google.com

</div>

**`sudo docker inspect dam_alp1 | grep IPA`**

Con este comando obtengo la IP del contenedor.

**`sudo docker exec -it dam_alp1 sh`**

Dentro del contenedor escribimos lo siguiente:

**`ping -c 2 google.com`**

<br>

<div align="center">

## 5. Crea un contenedor con el nombre 'dam_alp2'. ¿Puedes hacer ping entre los contenedores?

</div>

**`sudo docker run --name dam_alp2 -it alpine`**

Con este comando creo un contenedor con el nombre `dam_alp2`.

**`sudo docker container start -- dam_alp2`**

Con este comando arranco el contenedor.

**`sudo docker inspect dam_alp2 | grep IPA`** → 172.17.0.3

Dentro del contenedor `dam_alp1` escribimos lo siguiente:

**`ping -c 2 172.17.0.3`**

<br>

<div align="center">

## 6. Sal del terminal, ¿qué ocurrió con el contenedor?

</div>

Al salir de la terminal, los contenedores ya inicializados siguen funcionando.

**`sudo docker ps -a`**

Para comprobar los contenedores creados.

<br>

<div align="center">

## 7. ¿Cuánta memoria en el disco duro ocupaste?

</div>

**`sudo docker stats`**

Con este comando obtengo la memoria que ocupa Docker en el disco duro.

Memoria ocupada: 0.00%.

<br>

<div align="center">

## 8. ¿Cuánta RAM ocupan los contenedores? ¿Hay algún comando Docker para saber esto?

</div>

**`sudo docker stats`**

Con este comando obtengo la memoria que ocupan los contenedores.

RAM ocupada: 0.02% del primer contenedor.

RAM ocupada: 0.01% del segundo contenedor.