# Laboratorio I: Interconexión

## Integrantes:
- **Nicolás Almonacid Muñoz** (0000293190)
- **Juan Pablo Restrepo Coca** (0000305110)
- **Mariana Salas Gutiérrez** (0000296781)

## 1. Introducción
Las redes SOHO (Small Office Home Office) permiten la interconexión de dispositivos en un entorno doméstico o de pequeñas oficinas, facilitando la comunicación y el acceso a servicios externos, como internet. Este informe detalla el diseño, simulación y análisis de una red SOHO utilizando el software Cisco Packet Tracer, dando solución y planteando los desafios y soluciones presentados durante la configuración y validación.

## 2. Objetivo
El objetivo del presente laboratorio es diseñar, implementar y analizar una red SOHO que conecte distintos tipos de dispositivos, considerando distintos parámetros como eficiencia y optimización de recursos. En el diseño de esta red se emplean conceptos vistos en clase, conceptos claves en el área de las redes y comunicación de datos.

## 3. Metodología
Para llevar a cabo el laboratorio y desarrollar la solución de la problemática establecida, se emplea la herramienta de CISCO Packet Tracer [1] con el fin de realizar el diseño de la red y su respectiva simulación. Este software nos permite diseñar y simular el comportamiento de en este caso una red empresarial, probando las configuraciones de routers, switches, servers y otros dispositivos necesarios para el funcionamiento de la red. Se configuraron distintos protoclos esenciales como DNS, DHCP y HTTP para asegurar el correcto funcionamiento de la red. 

## 4. Desarrollo de la solución

La topología de la red está basada en una configuración SOHO que conecta los dispositivos de la familia a una red más amplia (WAN) para obtener acceso a servicios en internet. La red local se segmenta mediante VLANs para organizar el tráfico de diferentes dispositivos
![Imagen](redes_lab01.jpg)

### Elementos
- **Access Point:** LAP1 utilizado para proporcionar conectividad inalámbrica
- **Servidor:** Servidor DNS y servidor DHCP para la asignación de direcciones IP de manera dinámica
- **Switches:** Se utilizaron switches 2960 para segmentar el tráfico en la red local
- **Router:** Cisco 2811 el cual conecta la red local al ISP
- **Dispositivos finales:** Laptops, PCs y Smartphones que se intercomunican entre ellos y acceeden a la red 
  
### Topología
En este caso, la topología de la red es de tipo estrella. Esta fue escogida por ser sencilla de implementar y de mantener, razones por las cuales es comúnmente utilizada en redes pequeñas o medianas, donde hay una cantidad limitada de dispositivos y una baja demanda de ancho de banda, donde todos los dispositivos finales se conectan a switches centrales y a su vez, estos se conectan al router para obtener acceso a la WAN

### Tipos de redes
- **Red de Área Local (LAN):** Es el tipo de red empleada para la red implementada en este laboratorio
- **Red de Área Local Inalámbrica (WLAN):** Para los dispositivos móviles, PCs, impresoras, Tablets y Laptops que usan medios no guiados.
- **Red de Área Amplia (WAN):** La red externa que permite el acceso a internet mediante el router 

### Protocolos y modelos
- DNS (Sistema de nombres de dominio)
- DHCP (Protocolo de configuración dinámica de direcciones IP)
- HTTP (Hypertext Transfer Protocol)
- Modelo TCP/IP

### Arquitecturas y servicios
Para facilitar que Fernando Pérez y su familia naveguen por Disney+, la arquitectura de la red cliente-servidor proporciona servicios como DNS y DHCP.

### Segmentación mediante VLANs
Se crearon diferentes VLANs para organizar el tráfocp en la red local:
- VLAN 20: Para dispositivos invitados como smartphones
- VLAN 40: Para dispositivos internos como PCs y tablets
- Vlan 55: Para el servidor y dispositivos de equipo de TI

## 5. Desafíos
Durante el proceso de configuración en Cisco Packet Tracer, uno de los desafíos más grandes fue la correcta configuración de las VLANs y la asignación de direcciones IP dinámicas utilizando DHCP. La configuración del WLC también fue un gran reto a solucionar

## 6. Conclusión
En conclusión, la propuesta de la red SOHO permite la correcta conexión de una red de área local al internet. Sin embargo, durante el desarrollo de la solución se presentaron desafíos ya que se contaba con poca experiencia utilizando Cisco Packet Tracer y a pesar de que es el segundo laboratorio, la implementación de este fue mucho más dificíl, demorado y complejo. Por ende, este trabajo reforzó los conocimientos del grupo acerca de no solo el diseño de una red para ser aplicada en una situación de la vida real, si no también del programa de Cisco.

## 7. Referencias
[1] "Cisco Packet Tracer", *Cisco Systems*, 2024. [Enlace]. Disponible: https://www.netacad.com/courses/networking/
****
