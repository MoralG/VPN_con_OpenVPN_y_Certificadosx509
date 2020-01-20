# VPN con OpenVPN y certificados x509

#### En esta práctica cada pareja de alumnos va a configurar dos escenarios:

## VPN de acceso remoto con OpenVPN y certificados x509

#### Configura una conexión VPN de acceso remoto entre dos equipos:

* Uno de los dos equipos (el que actuará como servidor) estará conectado a dos redes
* Para la autenticación de los extremos se usarán obligatoriamente certificados digitales, que se generarán utilizando openssl y se almacenarán en el directorio /etc/openvpn, junto con los parámetros Diffie-Helman y el certificado de la propia Autoridad de Certificación.
* Se utilizarán direcciones de la red 10.99.99.0/24 para las direcciones virtuales de la VPN. La dirección 10.99.99.1 se asignará al servidor VPN.
* Los ficheros de configuración del servidor y del cliente se crearán en el directorio /etc/openvpn de cada máquina, y se llamarán servidor.conf y cliente.conf respectivamente. La configuración establecida debe cumplir los siguientes aspectos:
    * El demonio openvpn se manejará con systemctl.
    * Se debe configurar para que la comunicación esté comprimida.
    * La asignación de direcciones IP será dinámica.
    * Existirá un fichero de log en el equipo.
    * Se mandarán a los clientes las rutas necesarias.

* Tras el establecimiento de la VPN, la máquina cliente debe ser capaz de acceder a una máquina que esté en la otra red a la que está conectado el servidor.

#### Documenta el proceso detalladamente. Explica los distintos parámetros de los ficheros de configuración. ¿Qué es el parámetro Diffie-Helman?

## VPN sitio a sitio con OpenVPN y certificados x509

#### Configura una conexión VPN sitio a sitio entre dos equipos del cloud:

* Cada equipo estará conectado a dos redes, una de ellas en común
* Para la autenticación de los extremos se usarán obligatoriamente certificados digitales, que se generarán utilizando openssl y se almacenarán en el directorio /etc/openvpn, junto con con los parámetros Diffie-Helman y el certificado de la propia Autoridad de Certificación.
* Se utilizarán direcciones de la red 10.99.99.0/24 para las direcciones virtuales de la VPN.
* Tras el establecimiento de la VPN, una máquina de cada red detrás de cada servidor VPN debe ser capaz de acceder a una máquina del otro extremo.