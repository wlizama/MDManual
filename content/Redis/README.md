# Redis

Redis según [aws.amazon.com](https://aws.amazon.com/es/elasticache/what-is-redis/) es:
>Redis es un almacén de estructura de datos de valores de clave en memoria rápido y de código abierto [...] Entre los casos de uso principales de Redis se encuentran el almacenamiento en caché, la administración de sesiones, pub/sub y las clasificaciones. Es el almacén de valores de clave más popular en la actualidad. Tiene licencia BSD, está escrito en código C optimizado y admite numerosos lenguajes de desarrollo. Redis es el acrónico de REmote DIctionary Server (servidor de diccionario remoto).
>
>Gracias a su velocidad y facilidad de uso, Redis es una opción popular para aplicaciones web, móviles, de juegos, de tecnología publicitaria y de IoT que requieren el mejor desempeño de su clase.

## Comandos

```sh

# levantar redis server
docker run -p 6379:6379 --rm --name redis redis

# conectar redis cliente

docker run -it --link redis:redis --rm redis redis-cli -h redis -p 6379
```