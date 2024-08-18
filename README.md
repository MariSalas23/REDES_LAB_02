# Laboratorio I: Interconexión

## Integrantes:
- **Nicolás Almonacid Muñoz** (0000293190)
- **Juan Pablo Restrepo Coca** (0000305110)
- **Mariana Salas Gutiérrez** (0000296781)

## Introducción
Las redes son fundamentales para 

## Objetivo
El objetivo del presente laboratorio es permitir que Fernando Pérez y sus familiares puedan acceder al sitio web de Disney+ desde su hogar, utilizando sus dispositivos personales, mediante una red y comunicación de datos.

## Metodología
Para llevar a cabo el laboratorio y desarrollar la solución de la problemática establecida, se emplea la herramienta de CISCO Packet Tracer [1] con el fin de realizar el diseño de la red y su respectiva simulación. Es importante mencionar que para simular la estructura de una casa real, se utiliza una imagen de fondo [2] que se encuentra referenciada al final de la wiki.

## Desarrollo de la solución

...
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
- Un servicio de DNS, como Amazon Route 53, es un servicio distribuido globalmente que convierte los nombres legibles por las personas, como www.example.com, en las direcciones IP numéricas, como 192.0.2.1, que utilizan los equipos para conectarse entre sí. DHCP

## Desafíos

## Conclusión
En conclusión, la propuesta de la red para permitir que la familia Pérez pueda navegar por el sitio web de disneyplus.com desde sus dispositivos ha sido exitosa. Sin embargo, durante el desarrollo de la solución se presentaron desafíos al ser el primer laboratorio y contar con poca experiencia utilizando Cisco Packet Tracer. Por ende, el laboratorio reforzó los conocimientos del grupo acerca de no solo el programa, si no también del diseño de una red para ser aplicada en una situación de la vida real.

## Referencias
[1] "Cisco Packet Tracer," *Cisco Systems*, 2024. [Enlace]. Disponibilidad: https://www.netacad.com/courses/networking/
[2] "Sketching 3D Illustrations of Interior Spaces," *Pngtree*, 2023. [Enlace]. Disponibilidad: https://es.pngtree.com/freebackground/sketching-3d-illustrations-of-interior-spaces_5812116.html (consultado el: 17 de agosto de 2024).
[3] "DNS vs DHCP: Exploring the Key Differences," *Ascent Optics*, 2023. [Enlace]. Disponibilidad: https://ascentoptics.com/blog/es/dns-vs-dhcp-exploring-the-key-differences/#:~:text=R%3A%20DNS%20(Sistema%20de%20nombres,a%20dispositivos%20en%20una%20red. (consultado el: 17 de agosto de 2024).
