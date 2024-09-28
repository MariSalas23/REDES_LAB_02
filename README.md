# Laboratorio I: Interconexión

## Integrantes:
- **Nicolás Almonacid Muñoz** (0000293190)
- **Juan Pablo Restrepo Coca** (0000305110)
- **Mariana Salas Gutiérrez** (0000296781)

## 1. Introducción
Las redes empresariales permiten la interconexión de múltiples dispositivos en entornos corporativos, facilitando la comunicación interna y el acceso a servicios externos, como internet. Este informe detalla el diseño, simulación y análisis de una red empresarial utilizando el software Cisco Packet Tracer, dando solución y planteando los desafíos y soluciones presentados durante la configuración y validación.

## 2. Objetivo
El objetivo del presente laboratorio es diseñar, implementar y analizar una red empresarial que conecte distintos tipos de dispositivos, considerando distintos parámetros como eficiencia y optimización de recursos. En el diseño de esta red se emplean conceptos vistos en clase, conceptos claves en el área de las redes y comunicación de datos.

## 3. Metodología
Para llevar a cabo el laboratorio y desarrollar la solución de la problemática establecida, se emplea la herramienta de **Cisco Packet Tracer** [1] con el fin de realizar el diseño de la red y su respectiva simulación. Este software nos permite diseñar y simular el comportamiento de una red empresarial, probando las configuraciones de routers, switches, servidores y otros dispositivos necesarios para el funcionamiento de la red. Se configuraron distintos protocolos esenciales como DNS, DHCP y HTTP para asegurar el correcto funcionamiento de la red.

## 4. Desarrollo de la solución

La topología de la red está diseñada para una empresa que conecta sus dispositivos a una red corporativa centralizada con acceso a una red más amplia (WAN) y a servicios externos, como internet, VPNs y servidores en la nube. La red local se segmenta mediante VLANs para organizar y optimizar el tráfico de diferentes tipos de dispositivos, usuarios y servicios. Se implementan técnicas avanzadas de seguridad y administración para garantizar la estabilidad, confiabilidad y escalabilidad de la red a largo plazo.
![Imagen](RedEmpresarial.jpg)

### Elementos
- **Access Point:** LAP1 utilizado para proporcionar conectividad inalámbrica.
- **Servidor:** Servidor DNS y servidor DHCP para la asignación de direcciones IP de manera dinámica.
- **Switches:** Se utilizaron switches 2960 para segmentar el tráfico en la red local.
- **Router:** Cisco 2811, el cual conecta la red local al ISP.
- **Dispositivos finales:** Laptops, PCs y smartphones que se intercomunican entre ellos y acceden a la red.

### Topología
En este caso, la topología de la red es de tipo estrella. Esta fue escogida por ser sencilla de implementar y de mantener, razones por las cuales es comúnmente utilizada en redes pequeñas o medianas, donde hay una cantidad limitada de dispositivos y una baja demanda de ancho de banda. Todos los dispositivos finales se conectan a switches centrales, y a su vez, estos se conectan al router para obtener acceso a la WAN.

### Tipos de redes
- **Red de Área Local (LAN):** Es el tipo de red empleada para la red implementada en este laboratorio.
- **Red de Área Local Inalámbrica (WLAN):** Para los dispositivos móviles, PCs, impresoras, tablets y laptops que usan medios no guiados.
- **Red de Área Amplia (WAN):** La red externa que permite el acceso a internet mediante el router.

### Protocolos y modelos
- DNS (Sistema de nombres de dominio).
- DHCP (Protocolo de configuración dinámica de direcciones IP).
- HTTP (Hypertext Transfer Protocol).
- Modelo TCP/IP.

### Arquitecturas y servicios
La red empresarial implementa una arquitectura cliente-servidor robusta, ofreciendo servicios clave como DNS para la resolución de nombres y DHCP para la asignación dinámica de direcciones IP. El enrutamiento inter-VLAN asegura la comunicación eficiente entre departamentos, mientras que NAT permite el acceso a internet. Además, se implementan firewalls y servidores AAA para garantizar la seguridad, autenticación y auditoría. Los empleados remotos pueden acceder de forma segura a la red a través de VPNs, y los protocolos de monitorización como SNMP y Syslog aseguran la supervisión en tiempo real del rendimiento de la red.

### Segmentación mediante VLANs
Se crearon diferentes VLANs para organizar el tráfico en la red local:
- **VLAN 20:** Para dispositivos invitados como smartphones.
- **VLAN 40:** Para dispositivos internos como PCs y tablets.
- **VLAN 55:** Para el servidor y dispositivos del equipo de TI.

### Comparación de diseño de redes SOHO y empresariales
El diseño de redes SOHO se diferencia del empresarial en términos de escalabilidad, costo y complejidad. Mientras que una red SOHO está orientada a un número limitado de dispositivos, una red empresarial debe manejar una mayor cantidad de dispositivos, usuarios y tráfico.

- **Equipos:** Las redes SOHO suelen utilizar equipos de gama baja o media, como routers y switches de nivel básico. En redes empresariales, los equipos incluyen routers de mayor capacidad y switches administrados.
- **Servicios:** Las redes empresariales requieren servicios avanzados, como VPN, balanceo de carga y mayor seguridad, mientras que en SOHO se prioriza el acceso a internet y la gestión básica de dispositivos.
- **Protocolos:** En redes empresariales, los protocolos de enrutamiento avanzados como BGP o EIGRP son comunes. En redes SOHO, se utilizan principalmente protocolos simples como RIP y NAT para gestionar el tráfico interno y externo.

### Esquema de direccionamiento IPv4
Se aplicó una metodología de diseño estructurado, donde se segmentó la red en subredes adecuadas para garantizar la correcta distribución de direcciones IP. La segmentación asegura un manejo eficiente de los recursos de IP y la escalabilidad futura del sistema.

### Simulación y análisis de resultados
La simulación de la red se llevó a cabo en **Cisco Packet Tracer**, donde se probaron diferentes escenarios de conexión. Se simularon fallos en el router y en algunos dispositivos de la red para verificar la resiliencia del sistema.

## 5. Desafíos
Durante el proceso de configuración en **Cisco Packet Tracer**, uno de los desafíos más grandes fue la correcta configuración de las VLANs y la asignación de direcciones IP dinámicas utilizando DHCP. La configuración del WLC también fue un gran reto a solucionar.

## 6. Conclusión
En conclusión, la propuesta de la red empresarial permite la correcta conexión de una red de área local al internet. Durante el desarrollo de la solución se presentaron desafíos, especialmente en la implementación de VLANs y servicios avanzados como NAT y AAA. A pesar de los retos, este trabajo reforzó los conocimientos del grupo sobre el diseño de redes empresariales y la configuración de dispositivos en **Cisco Packet Tracer**.

## 7. Referencias
[1] "Cisco Packet Tracer", *Cisco Systems*, 2024. [Enlace]. Disponible: https://www.netacad.com/courses/networking/
