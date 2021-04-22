---
layout: post1
---

Un repositorio apt es un lugar donde se almacena paquetes, en este tutorial veremos como crear un repositorio apt.

Para crear el repositorio apt tenemos que ir a termux y ejecutar estos comandos.

```shell

pkg update -y && pkg upgrade -y
pkg install gnupg -y
pkg install termux-apt-repo -y

```

Una vez instalado eso tenemos que crear una carpeta con ``` mkdir ``` y dentro de esa carpeta ponemos nuestros paquetes.

Luego tenemos que poner estos comandos para generar una clave GPG:

```

gpg --gen-key

```

Una vez hecho eso se habra creado una clave GPG y tenemos que listar las claves disponibles para verificar que se creo la clave y tenemos que poner el comando ``` gpg --list-keys ```

Una vez hecho eso tenemos que exportar una clave publica y para hacer eso tenemos que poner los siquentes comandos:

```shell

gpg --export --armor correo@dominio.com >> clave.key

```

Al haber hecho eso la clave se habra exportado en el archivo clave.key.

Una vez hecho eso tenemos que ir ``` $HOME ``` y poner el siquiente comando:

```shell

cd $HOME
termux-apt-repo nombredelacarpeta dist

```

Para que esto funcione debemos poner esto en un sitio web y una vez hecho eso tenemos colocar los siquientes comandos:

```shell

pkg update -y && pkg upgrade -y

```

Listo


