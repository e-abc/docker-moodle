# Docker para instalación de moodle
> Esta imagen contiene todos los requerimientos necesarios para instalar una plataforma Moodle


## Tags soportados y sus respectivos links a `Dockerfile`

-	[`eabc/moodle:latest`](https://github.com/e-abc/docker-moodle/blob/master/7.1/Dockerfile)
-	[`eabc/moodle:7.1`](https://github.com/e-abc/docker-moodle/blob/master/7.1/Dockerfile)
-	[`eabc/moodle:7.0`](https://github.com/e-abc/docker-moodle/blob/master/7.0/Dockerfile)
-	[`eabc/moodle:5.6`](https://github.com/e-abc/docker-moodle/blob/master/5.6/Dockerfile)

### Descargar imagen
```console
$ docker pull eabc/moodle
```

> Cada tag pertenece a la version de php

### Ejemplo

```console
$ docker run -d -p 8080:80 --name my-moodle-instance -v /path/to/moodlefiles:/var/www/html -v /path/to/moodledatadir:/var/www/moodledata --network=my-net eabc/moodle:tag
```



* Donde `/path/to/moodlefiles` va la ruta de los archivos de moodle
* Donde `/path/to/moodledatadir` va la ruta del directorio moodledata (Debe tener permisos de escritura y lectura)
* Donde `my-net` debe ir el network de la base de datos. Si se usa el tipo de network host se pasara por alto el mapeo de puertos
* Donde `tag` va el tag correspondiente a la version de php que se desea instalar (5.6, 7.0, 7.1)

### Instalación

* Ingresar mediante el navegador web a localhost:8080 (o al dominio y puerto que corresponda) y seguir los pasos que indica la pantalla.