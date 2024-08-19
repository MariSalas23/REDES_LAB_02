# Laboratorio I: Interconexión

## Integrantes:
- **Nicolás Almonacid Muñoz** (0000293190)
- **Juan Pablo Restrepo Coca** (0000305110)
- **Mariana Salas Gutiérrez** (0000296781)

## 1. Introducción
En la actualidad, las redes son fundamentales para la tecnología moderna. Son estas las que permiten la conexión de dispositivos a nivel mundial, facilitando la comunicación entre personas, empresas y organizaciones en diferentes ubicaciones geográficas. Es decir, gracias a ellas, se puede acceder a sitios web, entre otras cosas.

## 2. Objetivo
El objetivo del presente laboratorio es permitir que Fernando Pérez y sus familiares puedan acceder al sitio web de Disney+ desde su hogar, utilizando sus dispositivos personales, mediante una red y comunicación de datos.

## 3. Metodología
Para llevar a cabo el laboratorio y desarrollar la solución de la problemática establecida, se emplea la herramienta de CISCO Packet Tracer [1] con el fin de realizar el diseño de la red y su respectiva simulación. Es importante mencionar que para simular la estructura de una casa real, se utiliza una imagen de fondo [2] que se encuentra referenciada al final de la wiki.

## 4. Desarrollo de la solución

Se plantea a la casa de la familia Pérez como una red local (LAN), también teniendo dispositivos conectados de forma inalámbrica (WLAN). Los dispositivos personales se conectan al router y este al modem. Este último se encuentra conectado a una red de área amplia (WAN), la cual se encarga de permitir la comunicación entre el servidor de Disney+ y el hogar de la familia Pérez.

![Imagen](redes_lab01.jpg)

### Elementos
- **Servidor:** disneyplus.com
- **Modem:** El dispositivo que permite la comunicación entre la red WAN y la casa de la familia Pérez.
- **Router:** Después de que el módem obtiene la información de Internet, este transmite los datos a los dispositivos personales.
- **Smartphones, laptop y PC:** Dispositivos desde los cuales los integrantes de la familia Pérez navegan por el sitio web de Disney +.
  
### Topología
En este caso, la topología de la red es de tipo estrella. Esta fue escogida por ser sencilla de implementar y de mantener, razones por las cuales es comúnmente utilizada en redes pequeñas o medianas, donde hay una cantidad limitada de dispositivos y una baja demanda de ancho de banda, tales como la red doméstica de la casa de la familia Pérez.

### Tipos de redes
- **Red de Área Local (LAN):** Es el tipo de red empleada para el hogar de la familia Pérez.
- **Red de Área Local Inalámbrica (WLAN):** Para los dispositivos móviles que usan medios no guiados.
- **Red de Área Amplia (WAN):** Se representa en la simulación en Cisco con Cloud-PT Internet.

### Protocolos y modelos
- DNS (Sistema de nombres de dominio)
- DHCP (Protocolo de configuración dinámica de host)
- HTTP (Hypertext Transfer Protocol)
- Modelo TCP/IP

### Arquitecturas y servicios
Para facilitar que Fernando Pérez y su familia naveguen por Disney+, la arquitectura de la red cliente-servidor proporciona servicios como DNS y DHCP.

## 5. Desafíos
Para completar este laboratorio, el mayor desafío encontrado fue lograr la funcionalidad en Cisco Packet Tracer. Por ello, fue necesario buscar información adicional acerca del programa para aplicar los conceptos de DNS y DHCP [3].

## 6. Conclusión
En conclusión, la propuesta de la red para permitir que la familia Pérez pueda navegar por el sitio web de disneyplus.com desde sus dispositivos ha sido exitosa. Sin embargo, durante el desarrollo de la solución se presentaron desafíos ya que se contaba con poca experiencia utilizando Cisco Packet Tracer y se trataba del primer laboratorio. Por ende, este trabajo reforzó los conocimientos del grupo acerca de no solo el diseño de una red para ser aplicada en una situación de la vida real, si no también del programa de Cisco.

## 7. Referencias
[1] "Cisco Packet Tracer", *Cisco Systems*, 2024. [Enlace]. Disponible: https://www.netacad.com/courses/networking/

[2] "Sketching 3D Illustrations of Interior Spaces", *Pngtree*, 2023. Accedido el 19 de agosto de 2024. [En línea]. Disponible: https://es.pngtree.com/freebackground/sketching-3d-illustrations-of-interior-spaces_5812116.html

[3] CARLOS ALEJANDRO FLORES HILAZACA. *"1125 - CREAR UNA RED SIMPLE CON PACKET TRACER"*. (19 de abril de 2020). Accedido el 19 de agosto de 2024. [Video en línea]. Disponible: https://www.youtube.com/watch?v=FA0D6bQjPg4
