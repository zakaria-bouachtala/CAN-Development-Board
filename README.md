# CAN-Development-Board
this repository is about creating a PCB of a costum and reconfigurable CAN bus development board based on PIC18F25k80 using the design sofware Kicad v5.
# Features
The board contains a High-speed CAN network (up to 1Mbps) of 4 configurable Nodes, a CAN bus Data-Reader and a built-in voltage regulator (12V DC input) with current limitation. 
## Nodes :
* each node is made of a MCU (PIC18F25K80) with an external 4MHz-Clock and a built-in CAN Controller and 12-bits ADC Module
* the MCU is associated with a CAN transceiver (MCP2551) to convert Signals from the MCU to the CAN bus(CAN-High & CAN-Low)
* the nodes are also associated with LEDs to test if the data is transmitting/received properly via the CAN bus 
## CAN Bus DATA-Reader :
For the purpose of reading,decoding and exploiting the Data and signals that traversing the CAN network, our Development Board contains a Data reader based on a MCP Module that communicate with an external MCU via the SPI protocol
> the MCP Module integrates a CAN transceiver (TJA1050) with a CAN Controller (MCP2515) ans SPI Interface 
## Alimentation :
the board has two separate voltage sources
* Direct 5V DC connector
* 12V DC Jack port (with a built-in Voltage Regulator)
## Applications :
the board can be used for several CAN_bus purpose-based applications, as the nodes are totally re-configurable and the CAN network can be extended or reduced depending on the application
>UART, I2C, SPI, Analog and GPIO Pins of each MCU are accessible to use for different applications
# PCB Details :
for the electric schematic and the integrated circuit design we are using the free version of KIcad 5 
>Our (153.42 mm* 98.04 mm) PCB comes with 2 layers and through-Hole technology (THT) component
# Future Features :
* *First half* : add a built-in bootloaders in the board to allow direct programming of the MCUs
* *second half* : Replacing the Node's MCUs with esp32 modules to support the OTA(over the air) Programming and add more wireless features and IoT concepts
# Refrences :
* You can find here more component libraries : [Kicad Library](https://www.digikey.com/en/resources/design-tools/kicad)
* For more details about the MCU used in the board (PIC18F25K80) you can visit their official website : [Microship PIC18F](microchip.com/en-us/product/PIC18F25K80)
* You can download the free version of the software Kicad from here : [KICAD](https://www.kicad.org/download/)
* If you are interested in the OTA programing with the ESP32, this article by the official Website suits you : [Espressif](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-reference/system/ota.html)
### NOTE :
the project is under development for now, the PCB and Gerber files will be added later for those who wants to print the module for their personal applications.
