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

SpecialistSmartScan es un script de escaneo de red que permite realizar escaneos de hosts y puertos en un rango de direcciones IP. Además, permite obtener información detallada sobre los servicios que se encuentran en cada puerto escaneado.

### Instalación

Para usar SpecialistSmartScan es necesario instalar las siguientes dependencias:

* scapy
* colorama
* argparse
* nmap
* pyfiglet
* pyperclip

Puedes instalarlas ejecutando el siguiente comando:

```pip install -r requirements.txt```

Si se ejecuta en linux aparte de nmap también necesitará el aplicativo xclip, este se instala con el siguiente comando:

```sudo apt install xclip```

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


El script cuenta con los siguientes argumentos:

- `-r` o `--rango`: permite especificar un rango de direcciones IP a escanear.
- `-p` o `--ports`: permite especificar una lista de puertos a escanear junto con el argumento `-s`.
- `-s` o `--scan`: permite especificar una dirección IP a la cual se le realizará un escaneo de puertos abiertos.

### Uso

```python script.py -r 192.168.1.0/24```

Este comando escaneará todos los hosts activos en el rango de direcciones `192.168.1.0/24` y mostrará su dirección IP y dirección MAC.

```python script.py -s 192.168.1.5```

Este comando escaneará todos los puertos abiertos en el host especificado, en este caso `192.168.1.5`

```python script.py -s 192.168.1.5 -p "[53, 80, 139, 443, 445]"```

Este comando escaneará la dirección IP `192.168.1.5` en busca de los puertos especificados en la lista y mostrará información sobre cada puerto abierto encontrado.

;)
