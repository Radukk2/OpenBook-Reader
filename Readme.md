# OpenBook Reader - Project
Block Chart : Block_chart.png file in the root of the directory

Bill of Materials : The bill of materials file can be found at /Manufacturing/Bom.csv

Hardware description
1. Microcontroller - ESP32-C6-WROOM-1-N8
    CPU: 32-bit RISC-V single-core @ up to 160MHz
    Memory: 320KB ROM, 512KB HP SRAM, 16KB LP SRAM
    Connectivity: Wi-Fi 6, Bluetooth LE 5.0
    Interfaces: GPIO, SPI, UART, I2C, PWM   
    Operating Voltage: 3.3V

   - The given microcontroller uses the following power modes: 
        When the device is active it consumes from 160 to 260 mA.
        When modem sleeps it ranges from 3 to 20 mA.
        On light the device consumes 0.8 mA.
        In Deep-sleep mode it consumes 10 μA.
        Hibernation modes consumes 2.5 μA.

2. Display Interface 7.5" E-Paper Display
    - Interface: SPI via FPC connector
    - Pins:   EPD_CS: GPIO10
            EPD_DC: GPIO5
            EPD_RST: GPIO23
            EPD_BUSY: GPIO3
            MOSI, SCK: Shared with SD card
            Used pins : Pins.xlsx  provieds the full ecplination

    The reasons why we use ePaper is for: 
                                        - ultra-low power consumption
                                        - excellent sunlight readability
3. Storage Solutions
    - MicroSD Card with the SPI interface.
    - 64MB NOR Flash with the same SPI interface.

4. Real time clocks
    We use a DS3231SN model for its high accuracy, backup supported battery.

5. Power Management
    USB-C Interface 
    MCP73831 - Li-Po Battery Charging that is used for charging


6. Buttons
    There are also 3 buttons: reset, boot and change. These are used for user's interaction with the device.

Used Pins: Described fully in Pins.xlsx





