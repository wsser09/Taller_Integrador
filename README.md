# Integrantes
- Gerardo Araya Fallas
- Carlos Elizondo Alfaro
- Walter Serrano Concepción
- Fabián Chacón Solano

# CA2RXU LoRa APRS Tracker/Station

This firmware is for using ESP32 based boards with LoRa Modules and GPS to live in the APRS world.

![Screenshot](https://github.com/richonguzman/LoRa_APRS_Tracker/blob/main/images/OledScreen2.jpeg)

__(NOTE: To use Tx/Rx capabilities of this tracker you should have also an Tx/Rx <a href="https://github.com/richonguzman/LoRa_APRS_iGate" target="_blank">LoRa iGate</a> near you)__

____________________________________________________

## You can support this project to continue to grow:

[<img src="https://github.com/richonguzman/LoRa_APRS_Tracker/blob/main/images/github-sponsors.png">](https://github.com/sponsors/richonguzman)     [<img src="https://github.com/richonguzman/LoRa_APRS_Tracker/blob/main/images/paypalme.png">](http://paypal.me/richonguzman)

____________________________________________________

- Tracker with complete MENU !!! (see Wiki to know how to access it)
    - Read, Write and Delete Messages (with I2C Keyboard or Phone).
    - Asking Weather Report.
    - Listening to other Trackers arround.
    - Changing Display Eco Mode (turn off after 4 seg) and Screen Brightness.
- Processor from 240Mhz to 80MHz to save almost 20% power consumption.
- All GPS beacons/packet are encoded for less time on RF/LoRa Tx.
- Oled Screen shows Altitude+Speed+Course or BME280 Wx Data or Number of New Messages Received.
- Oled Screen shows Recent Heard Trackers/Station/iGates Tx.
- Bluetooth capabilities to connect (Android + APRSDroid) or (iPhone + APRS.fi app) and use it as TNC.
- Led Notifications for Tx and Messages Received.
- Sound Notifications with YL44 Buzzer Module.
- Wx data with BME280 Module showed on Screen and transmited as Wx Telemetry.
- Winlink Mails through APRSLink.
- Posibility to change between 3 mayor Frequencies used by LoRa APRS Worldwide.

____________________________________________________

# WIKI (English / Español)

### FAQ: GPS, Bluetooth, Winlink, BME280 and more --> <a href="https://github.com/richonguzman/LoRa_APRS_Tracker/wiki/00.-FAQ-(frequently-asked-questions)" target="_blank">here</a>

### Supported Boards and buying links --> <a href="https://github.com/richonguzman/LoRa_APRS_Tracker/wiki/1000.-Supported-Boards-and-Buying-Links" target="_blank">here</a>

### 1. Installation Guide --> <a href="https://github.com/richonguzman/LoRa_APRS_Tracker/wiki/01.-Installation-Guide-%23-Guia-de-Instalacion" target="_blank">here</a>

### 2. Tracker Configuration and Explanation for each setting --> <a href="https://github.com/richonguzman/LoRa_APRS_Tracker/wiki/02.-Tracker-Configuration--%23--Configuracion-del-Tracker" target="_blank">here</a>

### 3. Upload Firmware and Filesystem --> <a href="https://github.com/richonguzman/LoRa_APRS_Tracker/wiki/03.-Upload-Firmware-and-Filesystem-%23-Subir-Firmware-y-sistema-de-archivos" target="_blank">here</a>

### 4. Tracker Menu Guide --> <a href="https://github.com/richonguzman/LoRa_APRS_Tracker/wiki/04.-Menu-Guide-%23-Guía-del-menú" target="_blank">here</a>

____________________________________________________
## Timeline (Versions):

- 2024.08.16 BLE support for Android devices (not APRSDroid yet).
- 2024.08.12 Added support for EByte E220 400M30S 1Watt LoRa module for DIY ESP32 Tracker (LLCC68 supports spreading factor only in range of 5 - 11!)
- 2024.08.02 New gpsEcoMode added for Testing.
- 2024.08.02 ESP32S3 DIY LoRa GPS added.
- 2024.07.30 HELTEC V3 TNC added.
- 2024.07.01 All boards with 433MHZ and 915MHz versions now.
- 2024.06.21 3rd Party Packets decode added following the corrections on iGate Firmware.
- 2024.06.21 If Tracker Speed > 200km/hr and/or Altitude > 9.000 mts , path ("WIDE1-1") will be omited as its probably a plane.
- 2024.06.21 Wx Telemetry Tx on Tracker only if standing still > 15min. (On screen Wx Data will be available but won't be sent if moving).
- 2024.06.07 Dynamic Height Correction of the BME280 Pressure readings.
- 2024.05.21 WEMOS ESP32 Battery Holder + LoRa SX1278 + GPS Module support added.
- 2024.05.16 all boards now work with Radiolib (LoRa) library from @jgromes.
- 2024.05.13 BME modules will be autodetected (I2C Address and if it is BME280/BMP280/BME680).
- 2024.05.10 PacketBuffer for Rx (25 Seg) and Tx outputPacketBuffer for sending with ACK Request.
- 2024.05.07 HELTEC V3 and Wireless Tracker Battery Measurements at 30seg to avoid accelerated discharge.
- 2024.05.06 New Output Buffer for Messages with retry posibilities.
- 2024.04.25 Added Lilygo TTGO T-Deck (add Neo6Mv2 GPS) support.
- 2024.04.12 Added HELTEC Wireless Tracker support.
- 2024.03.22 3 times pressing middle button for T-Beams turns the Tracker off.
- 2024.03.08 ESP32_C3 DIY LoRa + GPS board added. Thanks Julian OE1JLN.
- 2024.02.29 Now you can change between (EU,PL,UK) LoRa APRS frequencies used worldwide.
- 2024.02.24 New Partitions: more memory for new code/firmware (still > 500 Rx messages available)
- 2024.02.21 Winlink Mails through APRSLink ( https://www.winlink.org/APRSLink/ )
- 2024.01.26 Added Helmut OE5HWN MeshCom PCB support.
- 2024.01.18 BME modules have now a single reading per minute.
- 2024.01.05 Added HELTEC V3 with NEO8M GPS. Thanks Asbjørn LA1HSA.
- 2024.01.04 Added TTGO Lilygo T-Beam S3 Supreme V3 support. Thanks Johannes OE2JPO.
- 2023.12.31 PowerManagment Library AXP192/AXP2101 updated.
- 2023.12.27 Added Led-Flashlight like Baofeng UV5R Led.
- 2023.12.27 Added LoRa APRS Packet Decoder to Stations Menu.
- 2023.12.26 Added BME680 (to the already BME/BMP280) support for Wx Telemetry Tx.
- 2023.12.22 Added APRSThrusday on Messages Menu to parcitipate from this exercise ( https://aprsph.net/aprsthursday/ )
- 2023.12.19 Added support for T-Beam V1.2 with Neo8M GPS and SX1262 LoRa Modules.
- 2023.12.18 Added Mic-E encoding and decoding.
- 2023.12.12 Added BMP280 (to the already BME280) support for Wx Telemetry Tx.
- 2023.12.11 Added support for EByte 400M30S 1Watt LoRa module for DIY ESP32 Tracker.
- 2023.12.07 Added TTGO Lilygo LoRa32 v2.1 board as Bluetooth TNC(Android/Apple) and as a Tracker (with external GPS module).
- 2023.12.07 Added ESP32 as DIY Tracker (with external GPS Module) with LoRa SX1278 module.
- 2023.12.06 T-Beam V1.2 as default board.
- 2023.12.05 Updated packets recognition (+Objects + Mic-E).
- 2023.11.28 Adding BLE connection to use it as TNC with APRS.fi app for iOS.
- 2023.11.07 DigiRepeater Mode added in Emergency Menu.
- 2023.10.23 COMPLETE New Menu for Keyboard add-on.
- 2023.10.22 Added Keyboard Support over I2C ( CARDKB from https://m5stack.com )
- 2023.10.07 Screen Brightness control added.
- 2023.10.01 Added Wx Telemetry Tx with BME280 Module attached to Tracker.
- 2023.09.28 Added Support for V.1 board with SX1268 LoRa Module.
- 2023.09.25 Wiki added.
- 2023.09.16 Adding Led notification for Beacon Tx and for Message Received.
- 2023.09.14 Adding buzzer sounds for BootUp, BeaconTx, MessageRx and more.
- 2023.09.11 Saving last used Callsign into internal Memory to remember it at next boot.
- 2023.09.05 Adding "simplified Tracker Mode": only GPS beacons Tx.
- 2023.08.27 Adding support to connect BME280 and see Temperature, Humidity, Pressure.
- 2023.08.12 Adding also support for old V0_7 board. Thanks Béla Török.
- 2023.08.09 Adding Bluetooth capabilities with Kiss and TNC2, TTGO Lora 32. Thanks Thomas DL9SAU.
- 2023.08.08 Added Maidenhead info on Screen. Thanks Mathias "mpbraendli".
- 2023.08.06 Added Bluetooth Support for TNC in Android/APRSDroid. Thanks Valentin F4HVV.
- 2023.08.05 New Support for SH1106 Oled Screen (0,96" and 1.3")
- 2023.07.24 New Validation for Callsings, Overlay change and New Icons (Bike, Motorcycle).
- 2023.07.18 Add Support for triggering PTT to external amplifier.
- 2023.07.16 New Icons for Oled Screen (Runner, Car, Jeep)
- 2023.07.01 Added Support for new T-Beam AXP2101 v1.2 Board.
- 2023.06.26 Weather Report now stays until button pressed, to avoid missing it.
- 2023.06.25 Sends comment after X count of beacons.
- 2023.06.24 displayEcoMode=true doesn't turn the screen off at boot.
- 2023.06.23 Return to from any Menu number to Main Menu (Tracker) after 30 segs.
- 2023.06.20 Major Code Repacking.
- 2023.06.01 Adding Turn Slope calculations for Smart Beacon and Display Eco Mode.
- 2023.05.29 New Config file for adding more new ideas to the Tracker.
- 2023.05.27 Adding Altitude + Speed or Course + Speed in the encoded GPS info.
- 2023.05.21 Adding Last-Heard LoRa Stations/Trackers.
- 2023.05.14 Adding Menu.
- 2023.05.12 Saving Messages to Internal Memory.
- 2023.04.16 Sending and Receiving LoRa Packets.

____________________________________________________
## This code was based on the work of :
- https://github.com/aprs434/lora.tracker : Serge - ON4AA on base91 byte-saving/encoding
- https://github.com/lora-aprs/LoRa_APRS_Tracker : Peter - OE5BPA LoRa Tracker
- https://github.com/Mane76/LoRa_APRS_Tracker : Manfred - DC2MH (Mane76) mods for multiple Callsigns and processor speed
- https://github.com/dl9sau/TTGO-T-Beam-LoRa-APRS : Thomas - DL9SAU for the Kiss <> TNC2 lib
____________________________________________________

# Hope You Enjoy this, 73 !!  CA2RXU , Valparaiso, Chile

# Pasos de diseño:
- Definir los entregables.
- Definir los paquetes de trabajo (son las tareas internas de los entregables), lo cual incluye las plataformas a utilizar con el dispositivo y las personas asignadas para realizar cada tarea, si se le hace algún empaquetado al dispostivo, todo depende de cada entregable en el proyecto.
- Estimar el trabajo en cuanto a tiempo y costo (el scope de cada tarea), estimación del workpackage, de esta manera es posible calcular presupuestos.
- Agenda del trabajo (cuándo nos va a dar el entregable).

En un gráfico de Gantt
- Se agrega un objetivo, ejemplo: diseñar la interfase de despliegue de datos del módulo.
- Workpackage => Crear la interface en watson.
- Se asigna una persona con un tiempo de entrega.
- Asegurar los recursos para el proyecto (elementos adicionales de los que ya nos han brindado), porta baterías, baterías, componentes electrónicos, etc. Esto se consigna a una lista y se le llama BOM (Bill of materials), también puede haber recurso humano, por ejemplo solicitar a algún externo colaboración,no necesariamente el recurso humano va en el BOM, usualmente en esta parte van los componentes que se requieren para construir o terminar de ensamblar el producto, esta tabla también puede incluir los costos. Importante poner el part number de los componentes en la tabla.
- Posteriormente se incorpora el presupuesto a la agenda, esto significa que es necesario tener listos los componentes antes de que comience una tarea que requiera el recurso.
- Identificar los indicadores de rendimiento o funcionamiento, por ejemplo cuántas medidas obtuvimos de la comunicación de los dispositivos.
- Identificar factores críticos del proyecto, por ejemplo componentes que no se encuentran en stock y es necesario tenerlos en cuenta para el seguimiento del proyecto.
- Los indicadores funcionan para el test bench, es el banco de pruebas a ejecutar para comprobar que este va acorde a los entregables del proyecto. El diseño va enfocado a las pruebas que se realizan con el test bench, en la documentación se debe plasmar la información de los casos críticos y en qué no se puede utilizar. "Este dispositivo solo funciona para....". Si se logra todas las comunicaciones o no, hay que diseñar el dispositivo en el rango según los casos identificados.
- Añadir un 30% de costos al presupuesto inicial permite tener un margen para imprevistos.
- Entregable 12 de Agosto, diagramas de primer, segundo y tercer nivel y comenzar a montar el esqueleto del diseño del proyecto.
