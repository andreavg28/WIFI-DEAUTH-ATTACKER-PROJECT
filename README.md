# ESP32 WiFi Deauthentication Attacker

# Descripción:

Este proyecto implementa un dispositivo de hardware hacking basado en el ESP32 que realiza un ataque de desautenticación (deauth) WiFi, interrumpiendo temporalmente las conexiones de redes inalámbricas cercanas. El dispositivo escanea redes WiFi, selecciona la red con la señal más fuerte, y envía paquetes de desautenticación para desconectar dispositivos de la red objetivo. Una pantalla OLED SSD1306 muestra información en tiempo real, como el SSID de la red objetivo, el canal utilizado y el conteo de paquetes enviados.

Nota Importante: Este proyecto es únicamente para fines educativos y de investigación en entornos controlados y autorizados. El uso de este código para interrumpir redes sin permiso es ilegal y va en contra de las leyes de ciberseguridad en la mayoría de los países. ¡Úsalo de manera ética y responsable!


# Características:

Escanea redes WiFi y selecciona automáticamente la red con mejor señal.
Envía paquetes de desautenticación en el canal de la red objetivo.
Muestra información en tiempo real en una pantalla OLED (SSID, canal, paquetes enviados).
Configuración para operar en la región de EE.UU. (modificable según la región).
Código optimizado para el ESP32 con soporte para WiFi y comunicación I2C.
# Uso:

Carga el código en un ESP32 utilizando el Arduino IDE o PlatformIO.
Conecta una pantalla OLED SSD1306 a los pines I2C (SDA: 21, SCL: 22).
El dispositivo escaneará redes WiFi, seleccionará la de mayor señal y comenzará a enviar paquetes de desautenticación.
La pantalla OLED mostrará el estado del ataque, incluyendo el SSID, canal y número de paquetes enviados.
Advertencia: Este proyecto debe usarse solo en redes propias o con permiso explícito del propietario. El mal uso puede tener consecuencias legales.

# Requisitos
# Software:
Arduino IDE o PlatformIO para cargar el código en el ESP32.
Librerías necesarias:
WiFi.h (incluida en el núcleo de ESP32 para Arduino).
U8g2lib (para controlar la pantalla OLED).
Wire.h (para comunicación I2C, incluida en el núcleo de Arduino).
Configura el entorno de desarrollo para el ESP32 (instala el núcleo ESP32 en Arduino IDE).
# Hardware:
Microcontrolador: ESP32 (cualquier modelo con soporte WiFi, como el ESP32-DevKitC).
Pantalla OLED: SSD1306 128x64 con interfaz I2C.
Cables y protoboard: Para conectar la pantalla OLED al ESP32.
Fuente de alimentación: Cable USB o batería compatible con el ESP32 (5V o 3.3V según el modelo).
Conexiones físicas:
# Conexión 
Conecta la pantalla OLED al ESP32:
SDA → Pin 21
SCL → Pin 22
VCC → 3.3V o 5V (según el modelo de la pantalla)
GND → GND
# Configuración adicional:

Asegúrate de que el entorno de desarrollo tenga las librerías U8g2lib y el núcleo ESP32 instalados.
Verifica que el ESP32 esté configurado para operar en la región correcta (el código está configurado para EE.UU. con wifi_country
