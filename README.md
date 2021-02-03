# laravel-docker-alpine-lamp


Genera una aplicación laravel contenerizada siguiendo los siguientes pasos:


* **PASO 1:** 
~~~
Ingresar al proyecto laravel
~~~

* **PASO 2:** 
~~~
git submodule add https://github.com/laradevs/container-alpine.git
~~~

* **PASO 3:** 
~~~
cd container-alpine
cp .env.dist .env

cd configs
cp dist.freetds.conf freetds.conf
cp dist.httpd.conf httpd.conf
cp dist.php.ini php.ini
cp dist.redis.conf redis.conf

~~~

* **PASO 4:** 
~~~
Modifica los parametros de nombres de contenedores e imagenes para iniciar
~~~


* **PASO 5 Optional:** 
~~~

Si creaste un nuevo nombre de red debes ejecutar el siguiente comando

docker network create mired

~~~


* **PASO 6:** 
~~~
docker-compose build
~~~

* **PASO 7:** 
~~~
docker-compose up -d
~~~


Saludos
Ernesto Liberio
