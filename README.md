# USO DE LA TERMINAL

Compendio de chuletas para usar la terminal.

## Índice:

1. Comandos Básicos
2. Uso de Symfony.
3. Sincronizar Git con github.

## 3. Sincronizar git con Github.

### 1. Subir un repositorio.

La primera posibilidad es que ya tengamos un repositorio local y queramos subirlo a GitHub. Recordemos que para GitHub es importante que tengamos un archivo `README.md`.

El Siguiente paso es crear un repositorio en GitHub, con el que enlazaremos nuestro repositorio local. Le ponemos el nombre y decidimos si va a ser un repositorio público o privado. No es recomendable hacer más configuraciones en principio, para que no haya interferencia en las versiones y podamos sincronizar nuestro repositorio local sin problemas.

**En la carpeta del proyecto** abrimos la terminal para hacer la conexión, y escribimos la orden con el enlace al repositorio **que nos de Github**.

```bash
git remote add origin https://github.com/TuUsuario/nombre-del-proyecto.git
```

Si todo ha funcionado como debería, **no pasará nada**. Ahora, para enviar tu repositorio local a GitHub, tienes que ejecutar la orden `push`. Dependiendo de tu versión, tendrás que utilizar la palabra `master` o `main` para referirte a la rama principal.

```bash
git push origin master
```

Si todo ha ido bien, ya estará subido a Github.

### 2. Bajar un repositorio alojado en GitHub.

En la página del repositorio de Github, verás en la esquina superior derecha el botón `<> Code`. Al pincharlo, te aparecerá el enlace del repositorio.

Para clonar ese repositorio en tu espacio de trabajo local, abre la terminal en el directorio que vaya a contener el proyecto, y usa el comando `clone` de la siguiente manera:

```bash
git clone https://github.com/TuUsuario/nombre-del-proyecto.git
```

**OJO CUIDAO:** Recuerda que muchos proyectos, como los creados con _composer_ y _Symphony_, tienen una serie de directorios temporales que normalmente son ignorados por git al hacer el _commit_, y será necesario crearlos de nuevo para que funcionen correctamente.

Para este caso específico, será tan sencillo como volver a instalar composer **en el directorio del proyecto:**

```bash
composer install
```

### 3. Sincronización.

Si lo has hecho bien, al menos en teoría, cuando modifiques un archivo en tu proyecto y hagas un _commit_, en la sección **_Control de código fuente_** de tu _VisualStudio_
debería de aparecer una flecha circular para sincronizar con github. pinchar ahí es el equivalente a un `PULL` y así lo mantendrás sincronizado.

**_SI NO APARECE DIRECTAMENTE_** esta flecha, en la sección **_"Control de Fuente"_** tienes tres puntitos "`...`" para seleccionar más acciones.
ahí debería de aparecer la opción **_`"Incorporar cambios (pull)"`_**.