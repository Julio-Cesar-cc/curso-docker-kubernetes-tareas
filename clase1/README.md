# Clase 1 - Introducción a Containers y Docker

## Objetivo

Desplegar un servidor web con HTTPD con Docker.

## Desarrollo

### 1. Ejecutar el container

```bash
docker run -d -p 8081:80 --name mi-apache httpd
```

**Explicación:** Este comando crea y ejecuta un container con httpd en segundo plano (-d), en el puerto 8081 del equipo.

**Salida:**
```
c02f3d8e5d483b80594417b901da9a34149f779b9ab9048960c1fd1b76988cf4
```

**Screenshot:**

![Container creado](screenshots/img_1.png)

### 2. Verificar que está corriendo

```bash
docker ps
```

**Screenshot:**

![Container corriendo](screenshots/img_2.png)

### 3. Acceder desde el navegador

Accedí a `http://localhost:8081` y obtuve:

![Httpd funcionando](screenshots/img_3.png)

Accediendo a los logs

```bash
docker logs mi-apache
```

**Screenshot:**

Los logs generados son:

![Mostrando logs](screenshots/img_4.png)

### 4. Limpieza

Deteniendo el contenedor

```bash
docker stop mi-apache
```

![Deteniendo contenedor](screenshots/img_5.png)

Eliminando el contenedor

```bash
docker rm mi-apache
```

![Eliminando contenedor](screenshots/img_6.png)

Verificando contenedores existentes

```bash
docker ps -a
```

![Contenedores](screenshots/img_7.png)

## Conclusiones

Aprendí a ejecutar containers en segundo plano.
