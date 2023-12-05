# Generador del sitio HSMTY.org

Este es el código que usa [Hugo](https://gohugo.io/) para generar el sitio del [hackerspace](https://hsmty.org), todo
el contenido se encuentra en [el repositorio de contenido](https://github.com/hsmty/web_content/).
Si quieres contribuir con el contenido debes de ir a ese repositorio. Aquí se configura la
funcionalidad y estética del sitio

## Contribuir

Para contribuir al proyecto debes de [instala Hugo](https://gohugo.io/installation/) para poder
probar los cambios al proyecto. El proyecto tiene dos submodulos: el tema y el contenido. El
contenido es manejado en su propio [repositorio](https://github.com/hsmty/web_content/). Cada
que la rama `public` del repositorio de contenido es actualizada actualiza automáticamente el
submodulo en la rama `main` de este repositorio y eso, a su vez, inicia una actualización de
la página pública.

```shell
$ git clone git@github.com:hsmty/hsmty.github.io.git
$ cd hsmty.github.io/
$ git submodule init
$ git submodule update
```

Para contribuir a este repositorio se hace a través de Pull Request, para la cual necesitarás
hacer un _fork_ de este repositorio en tu usario de Github, usando el botón _fork_ en la parte
superior derecha.

Esto creará una copia del repositorio en tu usuario, en el cuál deberás clonar a tu
computadora para modificar.

Recuerda agregar el repositorio original como `upstream` en tu copia local:

```shell
$ git remote add upstream git@github.com:hsmty/hsmty.github.io.git
```

Cada que vayas a realizar un nuevo cambio, en tu repositorio actualiza la rama `main` desde
`upstream` y luego crea una rama en la que vayas a agregar tus cambios.

```shell
$ git checkout main
$ git pull upstream main
$ git checkout -b <nombre-de-tu-rama>
```

Recuerda reemplazar `<nombre-de-tu-rama>` por un nombre descriptivo, sin espacio, de tus cambios.

Una vez que estén listos tus cambios haz `commit` de ellos y empujalos a tu repositorio:

```
$ git commit -m "<Descripción de mis cambios>" <mis-archivos-modificados>
$ git push -u origin <nombre-de-tu-rama>
```

Una vez hecho esto tendrás que ir al sitio de Github, ya sea de tu _fork_ o del repositorio original
y ahí crear un _Pull Request_ para solicitar que tus cambios sean agregados al repositorio.
