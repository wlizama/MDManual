# Maven

Maven simplifica mucho el proceso de build del código, permitiéndonos compilar cualquier tipo de proyecto de la misma manera, librándonos de todas las dificultades que estos procesos implican.

## Instalación en Windows

- Maven es una herramienta Java, por lo que debe tener Java instalado antes de continuar.

- Descargar [instalador](https://www-us.apache.org/dist/maven/maven-3/3.6.1/binaries/apache-maven-3.6.1-bin.zip) y colocar la ubicacion de la carpeta `/bin` dentro de la variable PATH.

- Comprobar con el comando 
  ```sh
  mvn --version
  ```

## Creando proyecto

```sh
    mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=my-app
```

Esto comando crea una estructura como la siguiente

![image](../../assets/images/maven-standard-project-structure.png "Estructura maven proyect")

## Build del proyecto

```sh
    mvn package
```

![image](../../assets/images/maven-building-output.png "Building output OK")

## Referencias

- [Maven in 5 minutes](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html)

- [Documentación](https://maven.apache.org/guides/index.html)