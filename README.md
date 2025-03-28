# SimulacroRedes1
https://github.com/csantillgar/SimulacroRedes1.git
## Pregunta 1: Modelos OSI y TCP/IP

### a) Descripción de las principales diferencias entre el modelo OSI y el modelo TCP/IP

1. **Número de capas:**
   - **Modelo OSI:** Tiene 7 capas: Física, Enlace de Datos, Red, Transporte, Sesión, Presentación y Aplicación.
   - **Modelo TCP/IP:** Tiene 4 capas: Acceso a la Red, Internet, Transporte y Aplicación.

2. **Orientación (teórica vs. práctica):**
   - **Modelo OSI:** Es un modelo teórico, creado como una guía para entender y diseñar sistemas de comunicación. No necesariamente se implementa tal cual en la práctica.
   - **Modelo TCP/IP:** Es un modelo práctico utilizado en la implementación real de redes. Está basado en los protocolos reales como TCP y IP.

3. **Manejo de la capa de aplicación:**
   - **Modelo OSI:** Divide la capa de aplicación en tres subcapas: Sesión, Presentación y Aplicación. Cada subcapa tiene una función más específica (por ejemplo, la capa de presentación maneja la conversión de datos).
   - **Modelo TCP/IP:** En el modelo TCP/IP, toda esta funcionalidad se agrupa bajo la capa de Aplicación, simplificando el proceso.

### b) Ventajas y limitaciones de cada modelo

#### Modelo OSI:
- **Ventajas:** Proporciona una vista detallada y estructurada de las funciones de red. Facilita la enseñanza y comprensión de redes.
- **Limitaciones:** Es más complejo y no se adapta de manera directa a los protocolos reales empleados en redes.

#### Modelo TCP/IP:
- **Ventajas:** Es más práctico y se adapta a la implementación real de redes. Utiliza los protocolos estándar de internet (TCP, IP).
- **Limitaciones:** Al agrupar varias funciones en la capa de aplicación, puede ser menos detallado para ciertos aspectos de redes.

---

## Pregunta 2: Función de la Capa de Transporte

La capa de Transporte en ambos modelos (OSI y TCP/IP) es responsable de asegurar la entrega correcta y confiable de los datos entre los sistemas finales de la red.

1. **Garantía de entrega:** La capa de transporte se encarga de la segmentación y reensamblaje de los datos. En TCP, esta capa garantiza la entrega confiable a través de mecanismos como la numeración de secuencia y la retransmisión de paquetes perdidos.
2. **Protocolos asociados:**
   - **Modelo OSI:** En OSI, la capa de transporte puede utilizar protocolos como X.25 o TPKT.
   - **Modelo TCP/IP:** En TCP/IP, los protocolos más comunes son TCP (Transmission Control Protocol) para la comunicación confiable y UDP (User Datagram Protocol) para la comunicación no confiable.

---

## Pregunta 3: TCP vs. UDP

1. **Orientación a conexión:**
   - **TCP:** Es orientado a conexión, lo que significa que establece una conexión antes de la transmisión de datos.
   - **UDP:** Es sin conexión, no establece ninguna conexión antes de enviar los datos.

2. **Fiabilidad y control de errores:**
   - **TCP:** Proporciona fiabilidad a través de confirmaciones, control de flujo y retransmisiones en caso de errores.
   - **UDP:** No garantiza la entrega ni la fiabilidad. No tiene control de errores a nivel de protocolo.

3. **Velocidad y orden de entrega:**
   - **TCP:** Es más lento debido a sus mecanismos de control de flujo y fiabilidad, pero asegura que los datos lleguen en el orden correcto.
   - **UDP:** Es más rápido ya que no tiene mecanismos de control de errores ni de orden de entrega.

4. **Ejemplos de aplicaciones:**
   - **TCP:** Web (HTTP/HTTPS), Transferencia de archivos (FTP), correo electrónico (SMTP).
   - **UDP:** Video en tiempo real, juegos en línea, VoIP, transmisión de audio (DNS, DHCP).

---

## Pregunta 4: Protocolo para Transferencia de Archivos

### a) ¿Qué protocolo de la capa de aplicación se utiliza tradicionalmente para la transferencia de archivos en redes TCP/IP?

El protocolo más común para la transferencia de archivos es **FTP (File Transfer Protocol)**. Es utilizado para transferir archivos entre un cliente y un servidor a través de la red.

### b) Alternativas al protocolo FTP:

1. **SFTP (SSH File Transfer Protocol):** A diferencia de FTP, SFTP ofrece seguridad mediante la encriptación, ya que utiliza SSH para proteger los datos transferidos.
2. **TFTP (Trivial File Transfer Protocol):** Una versión más simple y ligera de FTP, pero sin seguridad, y generalmente usado para configuraciones de red o sistemas que requieren menos funcionalidad que FTP.

---

## Pregunta 5: Resolución de Nombres en DNS

### Proceso de resolución de nombres en DNS:

1. El usuario ingresa una URL en su navegador, como `www.ejemplo.com`.
2. **Consulta local:** El sistema operativo verifica si la IP de `www.ejemplo.com` está almacenada en la caché DNS. Si está, la consulta se resuelve localmente.
3. **Consulta a servidores DNS:** Si no está en la caché, el sistema envía la solicitud a un servidor DNS recursivo, que a su vez consulta a otros servidores para resolver la dirección.
4. **Rol de los servidores raíz:** Si el servidor recursivo no tiene la IP en su caché, consulta primero a uno de los servidores raíz. Los servidores raíz redirigen la consulta a los servidores de dominio de nivel superior (.com, .org, etc.), que luego dirigen la consulta al servidor autoritativo para el dominio `ejemplo.com`.
5. **Respuesta:** Una vez que el servidor autoritativo devuelve la IP correcta, el sistema la almacena en la caché DNS y establece la conexión con el servidor web correspondiente.

---

## Pregunta 6: Comunicación en el Modelo TCP/IP

El proceso de comunicación entre dos dispositivos en una red TCP/IP implica varias capas, cada una con funciones específicas:

1. **Capa de Aplicación:** El software de la aplicación (por ejemplo, un navegador web) genera los datos que se envían. Esta capa también maneja los protocolos de comunicación entre aplicaciones como HTTP, FTP, etc.
2. **Capa de Transporte:** Esta capa asegura que los datos lleguen correctamente a su destino. Si se utiliza TCP, garantiza la entrega confiable, maneja la segmentación de los datos y controla el flujo de información.
3. **Capa de Internet:** Esta capa se encarga de enrutar los paquetes entre dispositivos a través de redes intermedias. El protocolo IP (Internet Protocol) se encarga de dirigir los paquetes de un host a otro mediante direcciones IP.
4. **Capa de Acceso a Red:** Es responsable de la transmisión física de los datos a través del medio de transmisión, como cables, fibra óptica o conexiones inalámbricas. Esto incluye protocolos como Ethernet, Wi-Fi, etc.

Este proceso asegura que los datos sean correctamente enviados, recibidos y entregados a su destino final, mientras que cada capa realiza su tarea específica en la comunicación.

