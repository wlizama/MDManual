# Docker

Docker es una herramienta que permite el manejo de contenedores y puede compararse a usar una maquina virtual pero con mayores beneficios.

## Enlaces de interes

- [Instalation on Ubuntu](https://docs.docker.com/install/linux/docker-ce/ubuntu/)

- [Docker Hub image explorer](https://hub.docker.com/search?q=&type=image)

## Comandos varios

```sh
# lista de images en ejecución
docker ps

# generar imagen usando archivo docker file
docker build -t php-testing-app .

# poner en funcionamiento contenedor
docker run -it php-testing-app

# eliminar contenedores
docker rm fcae16cb80b4

# Eliminar imagen
docker rmi ace107852095

## automatizado para rearmado de web en archivo .sh
docker rmi php-testing-app --force
docker build -t php-testing-app .
docker run -it php-testing-app
```