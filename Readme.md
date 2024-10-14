DOCKER


1. Descarga la imagen "alpine" SIN ARRANCARLA y comprueba que está en tu equipo

sudo docker pull alpine

El primer comando descarga la imagen de alpine

sudo docker images


Con el segundo comando visualizamos la imagen sin arrancarla


2. Crea un contenedor sin ponerle nombre. ¿está arrancado? Obtén el nombre

sudo docker run alpine

Con este comando creamos un contenedor sin nombre y sin arrancar 

sudo docker ps -a

Con este comando visualizamos los contenedores que tenemos

3. Crea un contenedor con el nombre 'dam_alp1'. ¿Como puedes acceder a él?

sudo docker run --name dam_alp1 -it alpine

Con este comando creo un contenedor con el nombre dam_alp1

sudo docker container start -- dam_alp1

Con este comando arranco el contenedor

sudo docker exec -it dam_alp1 sh

Con este comando accedo al contenedor

4. Comprueba que ip tiene y si puedes hacer un ping a google.com

5. Crea un contenedor con el nombre 'dam_alp2'. ¿Puedes hacer ping entre los contenedores?

6. Sal del terminal, ¿que ocurrió con el contenedor?

7. ¿Cuanta memoria en el disco duro ocupaste?

8. ¿Cuanta RAM ocupan los contenedores? ¿Hay algún comando docker para saber esto?.
