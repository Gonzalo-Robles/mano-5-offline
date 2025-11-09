Manual de Usuario – Mano Robótica Controlada por WiFi Wemos D1 mini (ESP8266)
1. Descripción General
Este sistema permite controlar una mano robótica con servomotores mediante una interfaz web inalámbrica, sin necesidad de conexión a Internet. El microcontrolador ESP8266 crea su propia red WiFi y un servidor web local al que el usuario puede acceder desde cualquier dispositivo (celular, notebook, tablet) para manipular los movimientos de los dedos.
2. Componentes Principales
Componente	Descripción
ESP8266 (NodeMCU o Wemos D1 Mini)	Controlador principal con WiFi integrado.
5 Servomotores	Controlan los dedos Pulgar, Índice, Medio, Anular y Meñique.
LED WiFi (D4)	Indica actividad del sistema (parpadea cada segundo).
Botón de Reset (D3)	Reinicia el sistema.
Fuente de alimentación 5V	Proporciona energía estable a los servos y al ESP8266.
3. Funcionamiento General
1. El ESP8266 crea una red WiFi local llamada 'ManoRobotica' con la contraseña '12345678'.
2. El usuario se conecta a esa red WiFi desde su dispositivo.
3. En el navegador, ingresar: http://192.168.0.1
4. Se abrirá una página web con sliders y botones interactivos para controlar los dedos y ejecutar gestos.
4. Interfaz Web
La interfaz cuenta con tres secciones: Movimiento fino (control individual de dedos), Acciones rápidas (gestos predefinidos), y Juguemos (formas Piedra, Papel o Tijera).

5. Detalles Técnicos
Función	Descripción
Modo WiFi	Access Point (AP) sin router externo.
IP fija	192.168.0.1
Puerto HTTP	80
Bibliotecas	ESP8266WiFi.h, ESP8266WebServer.h, Servo.h, ESP8266mDNS.h
Pins de servos	D0 (Pulgar), D8 (Índice), D5 (Medio), D6 (Anular), D7 (Meñique)
LED estado	D4 (GPIO2) – parpadea cada segundo
Botón Reset	D3 (GPIO0)
6. Encendido y Conexión
1. Conecte la alimentación de 5V a los servos y al ESP8266.
2. Espere que el LED parpadee.
3. Conéctese a la red WiFi 'ManoRobotica'.
4. Ingrese la contraseña '12345678'.
5. En el navegador, escriba http://192.168.0.1 para acceder al panel.
7. Uso Básico
Use los sliders para mover los dedos individualmente. Los botones permiten ejecutar gestos rápidos, abrir la mano, realizar una demo o jugar Piedra, Papel o Tijera.
8. Recomendaciones
• No alimente los servos desde el pin 5V del ESP8266.
• Use una fuente externa de al menos 2A con masa común (GND).
• Evite mover los servos manualmente.• Si la web no carga, revise la conexión WiFi.
9. Posibles Mejoras
• Integración con WiFiManager.
• Control por voz o sensores.
• Adaptación a ESP32.
