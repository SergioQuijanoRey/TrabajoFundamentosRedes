---
title: Memoria Trabajo Fundamentos de Redes
author: Sergio Quijano Rey, Daniel Gonzálvez
---

# Motivación

La motivación que hay detrás de este trabajo es la de estudiar cómo funcionan los productos de almacenamiento en la nube, a través de la creación de un servidor bastante básico de almacenamiento en red sobre nuestro propio servidor. 

Para ello hemos usado una *Raspberry Pi 3* en la que hemos instalado el programa de software libre *Nextcloud*. Sobre este servidor muy básico hemos tenido que realizar ciertas labores de administración, más propias de una asignatura como *Ingeniería de Servidores*, y otras labores centradas en aspectos de redes. 

Esto nos ha permitido conocer y aprender hasta cierto punto los aspectos a tener en cuenta para crear infraestructuras de este tipo, centrándonos especialmente en aspectos específicos de las redes.

# Especificación del hardware usado

El hardware que hemos usado es el siguiente:

* Raspberry Pi 3 Model B:
    * CPU Quad Core 1,2GHz Broadcom BCM2837 64bit
    * 1GB RAM
    * Tarjeta SD *Samsumg Evo*, 64 GB (actúa como disco duro del ordenador)
* Cargador de móvil *MicroUSB*: dará corriente a la *Raspberry Pi 3*

# Instalación básica del servidor

## Instalación del sistema operativo

Lo primero que necesitamos es descargar el sistema operativo que vamos a usar. Nostros vamos a usar *Ubuntu Server* para la *Raspberry Pi 3*. Podemos descargar un fichero `.img` del siguiente link: [Página de descarga](https://ubuntu.com/download/iot/raspberry-pi)

Una vez descargado el archivo tenemos que quemarlo en la tarjeta SD. Usando un adaptador `SD-USB` lo conectamos a nuestro ordenador. Localizamos la tarjeta SD usando el comando `lsblk`. Al ver que el dispostivo está ubicado en `/dev/sdb`, usamos el siguiente comando para quemar la imagen del sistema en la tarjeta SD: `sudo dd if="ubuntu-raspberry.img" of="/dev/sdb" bs=4M status=progress`. Una alternativa a usar la línea de comandos es usar un programa con interfaz gráfica como `etcher`. 

## Configuración inicial del sistema

Ahora introducimos la tarjeta SD en la *Raspberry Pi* y conectamos el cargador, tanto a la *Raspberry Pi* como a la corriente. También conectamos un cable `ethernet` desde el router hasta la *Raspberry Pi*, para tener conexión a internet

Gracias a que estamos usando *Ubuntu Server*, por defecto tiene el servicio `ssh` habilitado por defecto. Así que entramos al administrador del router escribiendo en la barra de nuestro navegador la dirección `192.168.1.1`. Tras esto podemos localizar su dirección local, como se muestra en la **Imagen 1**:

![Imagen 1](localizar_raspberry.png)

Hacemos ssh a nuestro servidor con la dirección que acabamos de obtener: `ssh ubuntu@192.168.1.8`. `ubuntu` es el usuario por defecto que está creado, además de `root`. Este usuario está en la lista de `sudoers`, por lo que tenemos privilegios de administración a través de él. Pero para facilitar las cosas, nos registramos como `root` usando el comando `sudo su -`. 

El primer paso es hacer una primera actualización del sistema con `apt update; apt upgrade`, e instalar algunos paquetes básicos para trabajar, como pueden ser `vim` o `make`

## Creación del usuario de administración

# Aspectos de Redes en la instalación del servidor

# Instalación de Nextcloud

# Uso básico de Nextcloud

# Análisis del sistema

# Referencias
