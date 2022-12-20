---
title: Presentación SpecialistSmartScan
author: C0C05
date: 2022-12-20
categories: [Scripts]
tags: [Scripting, Python, Hacking, Fingerprinting ]
image:
  path: ../../assets/img/commons/avatar.jpg
  width: 200
  height: 200
  alt: SpecialistSmartScan
---
## SpecialistSmartScan ##

![imagen logo](../../assets/img/commons/Specialist.JPG)

Este script es un escáner de red y puertos que utiliza varias herramientas y librerías para facilitar el análisis de la red. 

Algunas de las librerías y herramientas utilizadas son:
- `scapy`: es una librería de Python que se utiliza para enviar, escuchar y analizar paquetes de red. 
- `colorama`: es una librería de Python que se utiliza para añadir colores a la salida de texto en la consola.
- `argparse`: es una librería de Python que se utiliza para facilitar el procesamiento de argumentos en línea de comandos.
- `time`: es una librería de Python que se utiliza para medir tiempos y realizar operaciones relacionadas con la fecha y hora.
- `re`: es una librería de Python que se utiliza para trabajar con expresiones regulares.
- `threading`: es una librería de Python que se utiliza para crear y controlar hilos (threads).
- `pyperclip`: es una librería de Python que se utiliza para acceder al portapapeles del sistema.
- `nmap`: es una herramienta de red que se utiliza para escanear y analizar redes.
- `signal`: es una librería de Python que se utiliza para enviar y recibir señales.
- `pyfiglet`: es una librería de Python que se utiliza para crear texto en ASCII art.

El script comienza definiendo un manejador de señales para capturar la señal `SIGINT` (que se envía cuando se pulsa `Ctrl+C`) y mostrar un mensaje de salida segura al usuario antes de finalizar el script.

Luego, se define la función `ip_scan` que realiza un escaneo de ARP para buscar hosts activos en un rango de IPs especificado. La función utiliza la librería `scapy` para crear y enviar un paquete ARP y escuchar la respuesta. Finalmente, muestra los hosts activos encontrados y el tiempo que ha tardado el escaneo.

La función `port_scan` realiza un escaneo de puertos TCP para ver si están abiertos en una dirección IP especificada. Utiliza la librería `socket` para crear un socket y conectarse al puerto especificado. Si la conexión se establece correctamente, significa que el puerto está abierto y se muestra en pantalla.

La función `scan` utiliza la herramienta `nmap` para escanear puertos y obtener información adicional sobre ellos, como el servicio que se está ejecutando en el puerto, el producto que lo util

Puedes descargarte el script en el repositorio [SpecialistSmartScan](https://github.com/C0C05/SpecialistSmartScan)

;)
