# Nmap

![Nmap](https://concienciat.gva.es/wp-content/uploads/2018/03/nmap.png)

Nmap se utiliza para explorar redes, realizar análisis de seguridad, auditoría de red y búsquedas de puertos abiertos en la máquina remota. Analiza en busca de hosts en directo, sistemas operativos, filtros de paquetes y puertos abiertos que se ejecutan en máquinas remotas. 

Entre los comandos más utilizados de Nmap podemos encontrar los siguientes:

* Escaneo mediante el nombre de host:

    ```bash
    nmap server2.mimaquina.com
    ```

    Con la bandera **-v** se obtiene una información más detallada acerca de la máquina remota. 

* Escaneo mediante direcciones IP:

    ```bash
    nmap 192.168.0.101
    ```

    Con la bandera **-v** se obtiene una información más detallada acerca de la máquina remota.

* Puede escanear múltiples hosts simplemente escribiendo sus direcciones IP o nombres de host con Nmap:

    ```bash
    nmap 192.168.0.101 192.168.0.102 192.168.0.103
    ```

* Puede escanear toda una subred o rango de direcciones IP con Nmap proporcionando el comodín *. 

    ```bash
    nmap 192.168.0.*
    ```

* Puede llevar a cabo exploraciones en varias direcciones IP simplemente especificando el último octeto de la dirección IP. Por ejemplo, aquí se realiza un análisis de las direcciones IP 192.168.0.101, 192.168.0.102 y 192.168.0.103.

    ```bash
    nmap 192.168.0.101,102,103
    ```

* Para especificar un rango de direcciones IP en el desempeño de escaneo con Nmap:

    ```bash
    nmap 192.168.0.101-110
    ```

* Para excluir algunos hosts al realizar una exploración de red completa o cuando se escanea con los comodines con la opción de "–exclude". 

    ```bash
    nmap 192.168.0.* --exclude 192.168.0.100
    ```

* Con Nmap, puede detectar qué sistema operativo y la versión que está ejecutando en el host remoto. Para habilitar la detección de sistema operativo y versión, la exploración de la escritura y la Ruta de seguimiento, podemos usar la opción "-A" con NMAP. 

    ```bash
    nmap -A 192.168.0.101
    ```

* Utilice la opción "-O" y "-osscan-guess" también ayuda a descubrir la información del sistema operativo.

    ```bash
    nmap -O server2.mimaquina.com
    ```

* El siguiente comando realizará una búsqueda en un host remoto para detectar si los filtros de paquetes o Firewall se utiliza por el anfitrión.

    ```bash
    nmap -sA 192.168.0.101
    ```

* Para escanear un host si está protegido por algún software de filtrado de paquetes o cortafuegos. 

    ```bash
    nmap -sA 192.168.0.101
    ```
* Para escanear un host si está protegido por ningún software de filtrado de paquetes o cortafuegos. 

    ```bash
    nmap -PN 192.168.0.101
    ```

* Con la ayuda de la opción "-sP" simplemente podemos comprobar qué hosts están vivos y en red, con esta opción se salta nmap detección de puertos y otras cosas. 

    ```bash
    nmap -sP 192.168.0.*
    ```

* Usted puede realizar un análisis rápido con la opción "-F" para las exploraciones para los puertos que figuran en los archivos de nmap-services y deja todos los demás puertos.

    ```bash
    nmap -F 192.168.0.101
    ```

* Nmap. Se puede especificar el puerto que desee nmap para escanear con la opción "-p", por defecto escanea nmap sólo puertos TCP:

    ```bash
    nmap -p 80 server2.mimaquina.com
    ```

* Escanear un puerto TCP:

    ```bash
    nmap -p T:8888,80 server2.mimaquina.com
    ```

* Escanear un puerto UDP:

    ```bash
    nmap -sU 53 server2.mimaquina.com
    ```

* Podemos encontrar versiones de servicios que se ejecutan en máquinas remotas con la opción "-sV":

    ```bash
    nmap -sV 192.168.0.101
    ```

* A veces, los cortafuegos de filtrado de paquetes bloquea las solicitudes de ping ICMP estándar, en ese caso, podemos utilizar métodos TCP ACK y TCP Syn para escanear hosts remotos:

    ```bash
    nmap -PS 192.168.0.101
    ```

* Analizar Host remoto para puertos específicos con TCP ACK:

    ```bash
    nmap -PA -p 22,80 192.168.0.101
    ```

* Analizar Host remoto para puertos específicos con TCP Syn:

    ```bash
    nmap -PS -p 22,80 192.168.0.101
    ```

* Realizar un escaneo sigiloso:

    ```bash
    nmap -sS 192.168.0.101
    ```

* Compruebe más puertos utilizando TCP Syn:

    ```bash
    nmap -sT 192.168.0.101
    ```

* Realizar un análisis tcp nula para engañar a un servidor de seguridad:

    ```bash
    nmap -sN 192.168.0.101
    ```