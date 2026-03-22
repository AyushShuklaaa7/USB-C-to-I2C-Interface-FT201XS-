Overview

This project converts USB communication to I2C using the FT201XS, making it useful for testing, debugging, or interfacing with I2C-based sensors and modules.
The board is powered via USB-C and includes an onboard LDO to generate a stable 3.3V supply, which is used for both the IC and I2C communication.

⚙️Key Components

1. FT201XS (USB to I2C Bridge)
2. TLV71333PDBVR (3.3V LDO)
3. USB-C Connector
4. Power Indicator LED

🧠 Design Approach & Working

* This board is designed to provide a simple bridge between USB and I2C communication using the FT201XS IC.
* the USB D+/D- differential pairs are routed with matched lengths and kept short to ensure error-free USB Full-Speed communication.
* When the board is connected via USB-C, the 5V (VBUS) from the USB is used as the primary power source. This 5V is passed through a polyfuse for overcurrent protection and then filtered using a ferrite bead to reduce high-frequency noise. A power indicator LED is connected to VBUS to show when the board is powered.
* The 5V input is then regulated down to 3.3V using an onboard LDO. This 3.3V supply powers the FT201XS IC,The FT201XS acts as a USB-to-I2C bridge.
* It communicates with the host computer over USB and converts those signals into I2C signals (SDA and SCL), which are exposed through the output header.
* For flexibility, both 3.3V (regulated) and 5V (VBUS) are exposed on the output header. While 5V can be used to power external modules, the I2C communication itself is strictly limited to 3.3V logic levels.
* Additional protection is included using an ESD protection device on the USB data lines (D+ and D−) to safeguard the board from electrostatic discharge events.
* An additional pin header is connected to the CBUS0 pin of the FT201XS. This pin can be configured for various functions such as GPIO, status indication, or other control signals, depending on the application.


Tools Used 
KiCad (for schematic and PCB design)

Preview

(Add your PCB screenshots or 3D renders here)
