# Laboratorio II: Red SOHO

## Integrantes
- **Nicolás Almonacid Muñoz** (0000293190)
- **Juan Pablo Restrepo Coca** (0000305110)
- **Mariana Salas Gutiérrez** (0000296781)

## Video
https://youtu.be/Y2BbUOhOkcc?feature=shared

## Introducción
Las redes empresariales permiten la interconexión de múltiples dispositivos en entornos corporativos, facilitando la comunicación interna y el acceso a servicios externos, como internet. Este informe detalla el diseño, simulación y análisis de una red SOHO utilizando el software Cisco Packet Tracer, dando solución y planteando los desafíos y soluciones presentados durante la configuración y validación.

## Objetivo
El objetivo del presente laboratorio es diseñar, implementar y analizar una red empresarial que conecte distintos tipos de dispositivos, considerando distintos parámetros como eficiencia y optimización de recursos. En el diseño de esta red se emplean conceptos vistos en clase, conceptos claves en el área de las redes y comunicación de datos.

## 1. Metodología
Para llevar a cabo el laboratorio y desarrollar la solución de la problemática establecida, se emplea la herramienta de **Cisco Packet Tracer** [1] con el fin de realizar el diseño de la red y su respectiva simulación. Este software nos permite diseñar y simular el comportamiento de una red empresarial, probando las configuraciones de routers, switches, servidores y otros dispositivos necesarios para el funcionamiento de la red. Se configuraron distintos protocolos esenciales como DNS, DHCP y HTTP para asegurar el correcto funcionamiento de la red.
- **Montaje:** Inicialmente, se realiza el cableado estructurado. Luego, se agrega el módulo WIC-2T para conexiones seriales en los router, Wireless LAN Controller (WLC) 3504 y Lightweight Access Point (LAP) 3702i. Después, se realiza la conexión por medio de las interfaces. Finalmente, se agregan las viñetas y recuadros para que quede más organizado.
- **Configuración:** La primera configuración que se realiza es la de los dispositivos switch para crear las VLAN y definir sus puertos. Posteriormente, se configuraron los router para asignar las direcciones IP a las VLAN y definir el servidor DHCP. Tras configurar el router, se determina el servicio de DHCP en el servidor agregando un gateway, dirección IP de inicio y máscara de red para cada VLAN. A todos los routers y switches se les hizo la configuración básica (contraseña y hostname). Con las redes funcionando, se conectan a través de los routers determinados por rutas estáticas. Al final, se agregan los servicios de DNS y HTTP con sus respectivos servidores para poder acceder a una página web.
- **Verificación:** Primero, se envía un ping desde el router SOHO a los diferentes dispositivos para confirmar que estén bien conectados. Luego, se manda un ping desde PC1 a PC3 para verificar la conectividad entre la misma VLAN. De la misma manera, se revisa la conectividad entre VLAN diferentes. También se confirma que el WLC y el LAP puedan hacer ping entre ellos. Después, se manda un ping entre routers y cuando funciona, se envía otro pero desde un PC. La última prueba que se realizó fue abrir la página *www.jnm.net* desde un PC.

## 2. Resultados de configuración y verificación de funcionamiento de la topología

La topología de la red está diseñada para una empresa que conecta sus dispositivos a una red corporativa centralizada con acceso a una red más amplia (WAN) y a servicios externos. La red local se segmenta mediante VLANs para organizar y optimizar el tráfico de diferentes tipos de dispositivos, usuarios y servicios. Se implementan técnicas avanzadas de seguridad y administración para garantizar la estabilidad, confiabilidad y escalabilidad de la red a largo plazo.

![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/top.png)
**Figura 1.** Topología.

### Elementos
- **Access Point:** LAP1 utilizado para proporcionar conectividad inalámbrica.
- **Servidor:** Servidor DNS y servidor DHCP para la asignación de direcciones IP de manera dinámica.
- **Switches:** Se utilizaron switches 2960 para segmentar el tráfico en la red local.
- **Router:** Cisco 2811, el cual conecta la red local al ISP.
- **Dispositivos finales:** Laptops, PCs y smartphones que se intercomunican entre ellos.

### Tipos de redes
- **Red de Área Local (LAN):** Es el tipo de red empleada en este laboratorio.
- **Red de Área Local Inalámbrica (WLAN):** Para los dispositivos móviles, PCs, impresoras, tablets y laptops que usan medios no guiados.
- **Red de Área Amplia (WAN):** La red externa que permite el acceso a internet mediante el router.

### Protocolos, servicios y modelos
- DNS (Sistema de nombres de dominio).
- DHCP (Protocolo de configuración dinámica de direcciones IP).
- HTTP (Hypertext Transfer Protocol).
- Modelo TCP/IP.

![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/pagina.png)
**Figura 2.** Página personalizada con las iniciales de los integrantes.

### Segmentación mediante VLANs
Se crearon diferentes VLANs para organizar el tráfico en la red local:
- **VLAN 20:** Para dispositivos invitados como smartphones.
- **VLAN 40:** Para dispositivos internos como PCs y tablets.
- **VLAN 55:** Para el servidor y dispositivos del equipo de TI.
- **VLAN 99:** Nativa.

### Esquema de direccionamiento IPv4
Se aplicó una metodología de diseño estructurado, donde se segmenta la red en subredes adecuadas para garantizar la correcta distribución de direcciones IP. La segmentación asegura un manejo eficiente de los recursos de IP y la escalabilidad futura del sistema. Se emplea el servicio DHCP con éxito como se ve a continuación.

![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/dhcp1.png)
**Figura 3.** DHCP.

- Más capturas de configuración y verificación se encuentran en los siguientes apartados para resolver las preguntas propuestas en el laboratorio, analizar los resultados y justificar las conclusiones.

## 3. Respuestas a las preguntas formuladas en la sección de procedimiento

- **(1)**  El esquema de direccionamiento IPv4 basado en los requerimientos de red, y considerando X = 1, se presenta en las tablas de subnetting y direccionamiento en el apartado *4. Resultados y Análisis*.
  
- **(2)**  El montaje de la topología propuesta se puede visualizar en la *Figura 1*.
  
- **(3)**  A continuación, se demuestra la configuración básica en los routers y switches, definiendo una contraseña y hostname. A lo largo de la Wiki, se muestra evidencia de la correcta configuración de las VLAN y direcciones IP.
  
![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/confi.png)
**Figura 4.** Configuración básica.

Aunque no se consiguió conectar los dispositivos móviles a la WLAN, si se logró establecer una conexión entre WLC y LAP, logrando entrar a WLC para configurarlo desde un PC.

![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/wireless.png)
**Figura 5.** Conexión entre WLC y LAP.
  
- **(4)**  Se emplea asignación y traducción estática para los servidores. Para la red de SOHO, los demás dispositivos cuentan con asignación dinámica por medio del DHCP. La traducción dinámica se puede aplicar a esta parte de la red considerando que podrían añadirse más dispositivos y hacerlo de forma manual no sería muy eficiente. NAT se debe configurar en el router, al igual que en R_SOHO se configuró la IP del DHCP Server.

- **(5)**  Para verificar la asignación eficiente del esquema de direccionamiento desarrollado (tabla de direccionamiento), se usa el comando TCP/IP *show ip interface brief*.
  
![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/ip.png)
**Figura 6.** Direcciones IP de las Interfaces.
  
- **(6)  y  (7)** Para verificar que se hayan creado y configurado correctamente las VLANs que se definieron en la tabla de subnetting, se utiliza el comando *show vlan brief*.
  
![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/vlan.png)

**Figura 7.** VLANs.

- **(8)  y  (9)** Se verifica que haya conectividad entre dispositivos pertenecientes a la misma VLAN con el comando *ping IP_Destino*. En este ejemplo, se hace desde PC1 (IP 172.17.20.3), que se conecta con PC3 (IP 172.17.20.2), ambos son de la VLAN 20. Como el resultado es exitoso y PC3 envía reply, se confirma que los dispositivos tienen conectividad con su puerta de enlace, puesto que logran recorrer la ruta. Adicionalmente, los dispositivos de diferente VLAN también se conectan como se muestra en la siguiente imagen, donde se hizo un ping de PC1 a PC4 (IP 172.17.40.3) y a Printer0 (IP 172.17.55.4). Es decir, existe conectividad entre PCs pertenecientes a VLAN distintas gracias a la correcta configuración de los routers, switches y DHCP. Antes de terminar el DHCP, habían problemas de comunicación entre VLANs, probablemente porque asignar tantas IP de forma manual es ineficiente y pueden ocurrir errores en el proceso.

![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/conexion1.png)
**Figura 8.** Ping de PC1 a PC3 y Printer0.

- **(10)** El protocolo STP está configurado y el comando es *show spanning tree*. En este caso, para la VLAN 20, la interface fa 0/1 de SW2 fue escogida como raíz por su menor prioridad. Normalmente, se escoge la de menor prioridad, pero en caso de contar con la misma, el siguiente criterio es la menor dirección MAC. Está en estado "FWD" (Forwarding), lo que significa que está activo y reenviando tráfico hacia el puente raíz.
  
![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/stp.png)
**Figura 9.** Spanning-Tree.
  
- **(11)** El comando para realizar un telnet es *telnet Dirección_IP*. En la siguiente imagen se muestra que es posible hacer telnet de un PC a R_SOHO y switches.
  
![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/telnet.png)
**Figura 10.** Telnet.

- **(12)** El tipo de enrutamiento en las interfaces de red es estático, ya que son rutas simples que casi no varían, como en el caso de las conexiones seriales. También porque se trata de una opción para redes pequeñas, como es el caso de SERVERS, donde solo hay dos servidores y un switch. 

![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/rutas.png)
**Figura 11.** Rutas.

- **(13)** Los dispositivos de la red SOHO tienen acceso a la página web personalizada alojada en el Servidor Web. El nombre de dominio es gestionado por el servidor DNS. Este nombre debe tener el siguiente formato: Iniciales_nombres_estudiantes.net. La página que se despliega se puede ver en la *Figura 2*.

![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/dns.png)
**Figura 12.** DNS.

- **(14)** No se utilizó otro servicio adicional.

- **(15)** Los archivos TXT con las configuraciones también se encuentran anexados en la tarea de Teams.
     * [Configuración de Routers](https://github.com/MariSalas23/REDES_LAB_02/raw/main/Router_Config.txt)
     * [Configuración de Switches](https://github.com/MariSalas23/REDES_LAB_02/raw/main/Switch_Config.txt)

## 4. Resultados y Análisis

### 1) Responda a cada una de las preguntas guías del diseño estructurado propuesta en clase y documente todo el proceso de desarrollo del esquema de direccionamiento IPv4 propuesto por su equipo y diligencie las tablas de subneteo y direccionamiento de la red. 

#### Preguntas

- **¿Cuántas subredes necesito?** 172.17.0.0 / 16 necesita 4 subredes para la topología propuesta.
- **¿Cuántos hosts requieren?** VLAN 20 y VLAN 40 requieren 1022 hosts, VLAN 55 y 99 requieren de 254 hosts.
- **¿Qué dispositivos son parte de cada subnet?**
     * *VLAN 20:* Para PC1, PC3 y Smartphone.
     * *VLAN 40:* Para PC2, PC4 y Tablet.
     * *VLAN 55:* Para Servers, Printers y Laptop.
     * *VLAN 99:* Para nodos intermedios.
- **¿Cuáles son privadas y públicas?** Los nodos finales que quieren acceder a internet necesitan direcciones públicas, los demás pueden tener direcciones privadas.
- **¿Dónde deberían conservarse las direcciones?** Las direcciones son estáticas en los servidores. Las demás pueden ser dinámicas.
- **¿Cómo se asignan los dispositivos y las interfaces?** Se muestra en las tablas a continuación.

#### Tabla de Subnetting
![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/sub1.png)

##### Proceso
Para calcular la dirección de broadcast de una red, identificamos la dirección IP y su máscara de subred. Ambas se convierten a binario, luego se realiza una operación AND entre la dirección IP y la máscara para obtener la dirección de red. Con esta dirección, se localizan los bits de host (ceros en la máscara) y se cambian todos esos bits por 1 en la dirección de red para obtener la dirección de broadcast. Por ejemplo, para la red 172.17.40.0/22, la dirección de broadcast resultante sería 172.17.43.255.

![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/pro.png)

#### Tabla de Direccionamiento
![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/a.png)

### 2) Presente el análisis y proceso de configuración de los servicios de red requeridos para el correcto funcionamiento de la red empresarial. 

#### DNS
Respecto al proceso de configuración del DNS, primero se le asigna de forma estática su IP, es 161.130.2.4, la cual es la que se pone para configurar el DNS server en los dispositivos con el DHCP. Como se muestra en la siguiente imagen, el servicio de DHCP define el dominio como  *www.jnm.net* y lo dirige a 161.130.2.5, número que hace referencia al Web Server al ser su IP. Esto es lo que permite modificar el HTML y darle personalización a la página web.

![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/server.png)
**Figura 13.** Servidor DNS.

#### HTTP
Para configurar el servicio de HTTP primero se configuró la dirección IP de forma estática, de acuerdo con la tabla de direccionamiento. Como pertenece a la red de SERVERS, su dirección es 161.130.2.5, perteneciendo a la red 161.132.130.0 / 28. La máscara fue seleccionada para permitir 10 host, como indicaba el laboratorio. Finalmente, se modifica el index.html para que muestre la página personalizada que aparece en la *Figura 2*.

![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/http.png)
**Figura 14.** HTTP.

Los servicios DNS y HTTP demuestran ser exitosos y tienen el comportamiento esperado. Lo anterior se debe a que existe la debida conexión entre el servidor web y el servidor DNS, como se evidencia en la simulación. Además, se logra visualizar la página web como se ve en la *Figura 2* al ingresar, desde un PC por medio del web browser, *www.jnm.net*, que es la dirección creada a partir de las iniciales de los integrantes.

![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/con1.png)
**Figura 15.** Conexión entre DNS y HTTP.

#### DHCP
Continuando con el DHCP, se configura de manera estática su dirección IP, la cual pertenece a la red SOHO. Cada VLAN tiene su propio default gateway y dirección IP de inicio (con su respectiva máscara delimitada en la tabla), aunque comparten DNS Server (161.130.2.4) y WLC  (172.17.55.5). Todo esto se puede ver en la *Figura 3*, que aparece al inicio de la wiki. Finalmente, en R_SOHO se asignó como IP helper la dirección 172.17.55.2, haciendo referencia al servidor DHCP. La configuración del servicio se puede evidenciar con la conexión entre el servidor de DHCP y los diferentes dispositivos. 

![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/disp.png)
**Figura 16.** Conexión entre Servidor DHCP y dispositivos.

La *Figura 3* también muestra una captura de cómo se le asigna al PC su dirección IP por medio del DHCP con éxito, demostrando una buena conexión, tanto a nivel físico como lógico, entre los dispositivos. Es decir, con una correcta comunicación gracias a las VLANs, su configuración en los diferentes switches, y buen manejo del R_SOHO.

### 3) Evalúe el flujo bidireccional de datos generado al acceder a la página alojada en el servidor Web por los nodos terminales (PCs y dispositivos móviles) de las diferentes VLANs que conforman la topología de la Figura 1, utilizando el servicio DNS. Como también, al verificar la conectividad de un PCs a otro y de un PC al Gateway. Justifique su análisis utilizando capturas con el simulador y los filtros de paquetes de Cisco Packet Tracer. 

El flujo bidireccional de datos generados al acceder a la página alojada en el servidor Web por los nodos terminales de las diferentes VLAN que conforman la topología de la *Figura 1*, utilizando el DNS, permite la comunicación entre las redes y dentro de estas mismas. Inicialmente, se confirma que exista conexión de los routers a los dispositivos y al revés. En la captura del simulador se evidencia como esto fue exitoso, indicando un buen manejo del enrutamiento. En este caso, en R_SOHO se encuentran los gateways de las VLANs, demostrando conectividad de un PC al Gateway.

![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/routers.png)
**Figura 17.** Conexión entre dispositivos y routers.

Además, con la simulación también se verifica la conectividad entre PCs. Estos dispositivos pertenecen a diferentes VLANs y aun así pueden comunicarse, siendo indicativo de la correcta configuración de R_SOHO y de los switches.

![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/cond.png)
**Figura 18.** Conexión entre dispositivos.

Para terminar, a continuación se muestra la página abierta desde el PC4. Toda esta información sugiere que debe existir una conexión entre todos los nodos (terminales e intermedios) para lograr el funcionamiento de una red empresarial, escenario aplicable a la vida real. Entonces, que la simulación muestra capturas exitosas, indica la correcta configuración de la topología.

![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/PC4.png)
**Figura 19.** Visualización de la página desde PC4.

## 5. Desafíos
Durante el proceso de configuración en **Cisco Packet Tracer**, uno de los desafíos más grandes fue la correcta configuración de las VLANs y la asignación de direcciones IP dinámicas utilizando DHCP, ya que antes de lograr aplicar el servicio DHCP, la comunicación entre diferentes VLANs fallaba, posiblemente debido a un error al momento de configurar las direcciones de manera estática. Por ello, se realizó una búsqueda de información y se utilizó la fuente [2] para resolver dudas y seguir los pasos para implementar las VLANs y el DHCP. Igualmente, se presentaban problemas en la capa 3 en el enrutamiento, pero se solucionó creando rutas estáticas. La configuración del WLC también fue un gran reto, que al final no se pudo solucionar, ya que, aunque se ingresaba a la página resultante de la IP del WLC desde el web browser del PC, la configuración no se guardaba correctamente y no permitía avanzar al siguiente paso de abrir https://WLC_IP. El proceso descrito en [3] se intentó en los computadores de los tres integrantes del grupo. De acuerdo con la simulación, existe conectividad entre el PC1, el WLC y el LAP, indicando funcionamiento de la capa física y de la capa de enlace, por lo que el problema puede estar relacionado directamente con la configuración del WLC y no con las conexiones realizadas en la red por medio de los switches.

![Imagen](https://github.com/MariSalas23/REDES_LAB_02/raw/main/desafio.png)
**Figura 20.** Conexión entre LAP, WLC y PC.

## 6. Conclusiones y Recomendaciones
En conclusión, la propuesta de la red empresarial permite la correcta conexión de una red de área local al internet. Durante el desarrollo de la solución se presentaron desafíos, especialmente en la implementación de VLANs y servicios como DHCP. A pesar de los retos, este trabajo reforzó los conocimientos del grupo sobre el diseño de redes empresariales y la configuración de dispositivos en **Cisco Packet Tracer**, logrando a través de la configuración de VLANs, DHCP, DNS y HTTP, establecer una red funcional que facilita la comunicación entre dispositivos. 

Se recomienda trabajar utilizando comandos como *show interfaces*, *show vlan brief*, *show running-config*, *show spanning-tree*, *show ip interface brief* y demás para lograr identificar problemas en las capas 1, 2 y/o 3. Adicionalmente, en Cisco Packet Tracer a veces es necesario reiniciar dispositivos cuando no están funcionando pese a que las configuraciones están bien hechas, ya que se trata de un entorno que puede presentar fallos temporales.

## 7. Referencias
[1] "Cisco Packet Tracer", *Cisco Systems*, 2024. [Enlace]. Disponible: https://www.netacad.com/courses/networking/

[2] "Configuración de una red con múltiples VLAN y servicio DHCP en un mismo servidor - Packet Tracer", YouTube, 2021. [Online]. Disponible: https://www.youtube.com/watch?v=Ekr0vXDnlrM&list=LL&index=7. [Accessed: 28-Sep-2024].

[3] "Como Configurar un WLC y Servidor DHCP", YouTube, 2023. [Online]. Disponible: https://www.youtube.com/watch?v=WRF9f2hPIRA. [Accessed: 28-Sep-2024].
