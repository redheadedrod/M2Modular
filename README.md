# M2-Modular
New Macchina M2 firmware

This software is an attempt to make modular firmware for the M2 (And compatible) Devices. 
While this software will contain code from the original M2RET firmware, it is to be engineered
from the groundup to provide modularity in design to be able to plug in or remove components
easily without needing to rewrite portions of the code. While Collin Kidder did great work with the
original M2RET, which is based off GVRET, neither of those packages were designed to support the
flexibility of the M2. This project is an attempt to provide this flexibility and to support not
only the M2 but upcoming additional hardware that Macchina comes out with based off the M2 Arduino Due
based hardware. 

## M2-Libraries to include
You will need the following libraries to make this work. Please note that this software is only known
to work with these named libaries as they exist in the redheadedrod repositories. Newer versions may
exist in the original creators repositories but they may not have been tested with this firmware yet.

* ToDo
* ToDo

This software will provide modularity and flexibility in three major areas. These areas and possible examples include:

#### Protocol Modularity. Allow protocols to be added or left off depending on intended usage. 
  * LIN (And variants) (Current LIN Library to be integrated)
  * J1850VPW (Current library to be expanded and implimented with 4x speeds included)
  * J1850PWM (Planned but no work has been started)
  * CANBUS (Already implimented, will be first protocol added)
  * SWCAN (Same as CANBUS)
  * ALDL (Under development. Will use external port on current models. May be included on future models)
 
#### Interface Modularity. Provide connections to USB, XBee UART/SPI interfaces, External UART/SPI interfaces.
  * Communicate with the M2 as is now done through USB. Actual interface to be totally tranparent to operation.
    * USB port
    * Xbee SPI or UART
    * External SPI or UART
    * Support for WiFi, BT, full time Cellular or other similar external protocols.(Need individual "drivers")
  * Console. Main console mainly used for debuging. Basic commands and status logging.
    * Write to SDcard (Optional)
    * Use any port (UART/SPI/USB) not already used as the R/W port.
  * Special use devices. Devices that are not console and nor normal I/O devices. May have own command set.
    * Serial HMI's such as Nextion which have simple display with touch screen.
    * Limited Cellular to support commands such as remote start.
    
#### Interface protocol modularity. To support the M2 being used in different environments. 
  * GVRET - To maintain current M2RET compatibility
  * ELM/STN - ELM MAY be supported in current M2RET software but it will be verified and expanded to include STN commands
  * AVT - Support to emulate the AVT API. 
  * OpenXC


**Please note that the above list is a suggested list of potential implimentations **

The initial priority is to get this new firmware working the same as the M2RET software to include the ESP32 WiFi/BT module 
and possibly a Cellular module as well. 

