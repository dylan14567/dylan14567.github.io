---
layout: post
---

En este articulo veremos como instalar ubuntu en android sin root, y usaremos la aplicación termux.

Termux es un emulador de terminal de Android y una aplicación de entorno Linux que funciona directamente sin necesidad de enraizamiento ni configuración. Más información en: [https://termux.com](https://termux.com)

La instalación de ubuntu sera mediante proot, PRoot es una implementación de espacio de usuario de ```chroot, mount --bind```, y ```binfmt_misc```. Esto significa que los usuarios no necesitan ningún privilegio o configuración para hacer cosas como usar un directorio arbitrario como el nuevo sistema de archivos raíz, hacer que los archivos sean accesibles en algún otro lugar de la jerarquía del sistema de archivos o ejecutar programas creados para otra arquitectura de CPU de forma transparente a través del modo de usuario QEMU. 

No será Ubuntu Desktop, será como un Ubuntu Server (técnicamente hablando es Ubuntu Core). 

Más información de proot en: [https://wiki.termux.com/wiki/PRoot](https://wiki.termux.com/wiki/PRoot)

# Que es Ubuntu

Ubuntu es un sistema operativo de software libre y código abierto. Es una distribución de Linux basada en Debian. Puede correr en computadores de escritorio y servidores. Está orientado al usuario promedio, con un fuerte enfoque en la facilidad de uso y en mejorar la experiencia del usuario. [Wikipedia](https://es.wikipedia.org/wiki/Ubuntu)

# Instalación

Para instalar Ubuntu en Termux nesesitaremos instalar proot y para eso tenemos que ejecutar estos comandos:

```shell

pkg update -y && pkg upgrade -y
pkg install proot -y

```

Una vez instalado proot, nesecitamos instalar proot-distro.

proot-distro es un script que te permite instalar distribuciónes linux en Termux.

```shell

pkg install proot-distro

```

Una vez instalado debemos ejecutar el comando: ``` proot-distro install ubuntu-20.04 ```, esto instalara ubuntu en termux, una vez finalizada la instalación debemos ejecutar el comando ```proot-distro login ubuntu-20.04```, una vez ejecutado el comando se abra iniciado la interfaz de consola de ubuntu.