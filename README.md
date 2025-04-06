# E-book Reader Open-Source
Savu Alin Ion 332CC

### Diagrama

![Hardware Diagram](Images/diagram.png)


### BOM

| Name of Component | Device                                                                       | Check Prices (J)                                                                                                     | DataSheet                                                                                                        |
|-------------------|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| BOOT_BUTTON       | BUTTON_CUSYOMV1                                                              | [Link](https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k)                   | [Link](https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k)               |
| C1                | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | [Link](https://componentsearchengine.com/part-view/CC0402MRX5R5BB106/YAGEO)                                              | [Link](https://componentsearchengine.com/part-view/CC0402MRX5R5BB106/YAGEO)                                          |
| C1_BAT            | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| C1_BAT1           | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL)/YAGEO | #REF!                                                                                                                | #REF!                                                                                                            |
| C1_BAT2           | EAGLE-LTSPICE_CC0402                                                         | #N/A                                                                                                                 | #N/A                                                                                                             |
| C2                | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| C2_BAT\           | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| C3                | RCL_CPOL-EUCT3528                                                            | [Link](https://a360.co/4iZy6AA)                                                                                        | [Link](https://a360.co/4iZy6AA)                                                                                    |
| C4                | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| C4_USB            | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| C5                | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| C5_USB            | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| C6                | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| C7                | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| C8                | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| C9                | EAGLE-LTSPICE_CC0402                                                         | #N/A                                                                                                                 | #N/A                                                                                                             |
| C10               | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| C10_SUPERCAP      | CPH3225A                                                                     | EAGLE-LTSPICE_C0402                                                                                                  | EAGLE-LTSPICE_C0402                                                                                              |
| CHANGE_BUTTON     | BUTTON_CUSYOMV1                                                              | [Link](https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k)                   | [Link](https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k)               |
| CHG_LED           | ADAFRUIT_LEDCHIP-LED0603                                                     | [Link](https://www.snapeda.com/parts/KP-1608SURCK/Kingbright/view-part/?ref=search&t=LED%200603)                       | [Link](https://www.snapeda.com/parts/KP-1608SURCK/Kingbright/view-part/?ref=search&t=LED%200603)                   |
| C_DELAY           | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| D1                | USBLC6-2SC6Y                                                                 | [Link](https://www.snapeda.com/parts/USBLC6-2SC6Y/STMicroelectronics/view-part/?ref=eda)                               | [Link](https://www.snapeda.com/parts/USBLC6-2SC6Y/STMicroelectronics/view-part/?ref=eda)                           |
| D2                | ESP32_WROVER_AVX---SD0805S020S1R0_AVX_SD0805S020S1R0_0_0AVX_SD0805S020S1R0_0_0 | [Link](https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D)                | [Link](https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D)            |
| D3                | MBR0530                                                                      | [Link](https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D)                | [Link](https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D)            |
| D4                | MBR0530                                                                      | [Link](https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda)                                              | [Link](https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda)                                          |
| D5                | MBR0530                                                                      | [Link](https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda)                                              | [Link](https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda)                                          |
| D6                | PGB1010603MR                                                                 | [Link](https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda)                                      | [Link](https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda)                                  |
| D7                | ESP32_WROVER_AVX---SD0805S020S1R0_AVX_SD0805S020S1R0_0_0AVX_SD0805S020S1R0_0_0 | [Link](https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D)                | [Link](https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D)            |
| D8                | PGB1010603MR                                                                 | [Link](https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda)                                      | [Link](https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda)                                  |
| D9                | PGB1010603MR                                                                 | [Link](https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda)                                      | [Link](https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda)                                  |
| D10               | PGB1010603MR                                                                 | [Link](https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda)                                      | [Link](https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda)                                  |
| D11               | PGB1010603MR                                                                 | [Link](https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda)                                      | [Link](https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda)                                  |
| D12               | PGB1010603MR                                                                 | [Link](https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda)                                      | [Link](https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda)                                  |
| EPD_C1            | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| EPD_C2            | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| EPD_C5            | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| EPD_C6            | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| EPD_C7            | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| EPD_C8            | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| EPD_C9            | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| EPD_C10           | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| EPD_C11           | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| EPD_C12           | ESP32_WROVER_EAGLE-LTSPICE_CC0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| IC1               | BD5229G-TR                                                                   | [Link](https://componentsearchengine.com/part-view/BD5229G-TR/ROHM%20Semiconductor)                                      | [Link](https://componentsearchengine.com/part-view/BD5229G-TR/ROHM%20Semiconductor)                                  |
| IC4               | XC6220A331MR-G                                                               | [Link](https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex)                                                | [Link](https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex)                                            |
| J1                | FH34SRJ-24S-0.5SH_99_                                                        | [Link](https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex)                                                | [Link](https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex)                                            |
| J2                | SAMACSYS_PARTS_USB4110-GF-A                                                  | [Link](https://componentsearchengine.com/part-view/USB4110-GF-A/GCT%20(GLOBAL%20CONNECTOR%20TECHNOLOGY)                  | [Link](https://componentsearchengine.com/part-view/USB4110-GF-A/GCT%20(GLOBAL%20CONNECTOR%20TECHNOLOGY)              |
| J3                | QWIIC_CONNECTORJS-1MM                                                        | [Link](https://www.snapeda.com/parts/PRT-14417/SparkFun%20Electronics/view-part/?ref=search&t=qwiic)                   | [Link](https://www.snapeda.com/parts/PRT-14417/SparkFun%20Electronics/view-part/?ref=search&t=qwiic)               |
| J4                | 112A-TAAR-R03_ATTEND                                                         | [Link](https://store.comet.srl.ro/Catalogue/Product/43497/)                                                          | [Link](https://store.comet.srl.ro/Catalogue/Product/43497/)                                                      |
| L1                | 744043680IND_4828-WE-TPC_WRE                                                 | [Link](https://eu.mouser.com/ProductDetail/Wurth-Elektronik/744043680?qs=PGXP4M47uW6VkZq%252BkzjrHA%3D%3D)              | [Link](https://eu.mouser.com/ProductDetail/Wurth-Elektronik/744043680?qs=PGXP4M47uW6VkZq%252BkzjrHA%3D%3D)          |
| PFMF.050.1        | ESP32C6_VARISTORCN1812                                                       | [Link](https://www.mouser.co.uk/ProductDetail/EPCOS-TDK/B72520T0350K062?qs=dEfas%2FXlABIszF52uu7vrg%3D%3D)                | [Link](https://www.mouser.co.uk/ProductDetail/EPCOS-TDK/B72520T0350K062?qs=dEfas%2FXlABIszF52uu7vrg%3D%3D)            |
| Q1                | ESP32_WROVER_SPARKFUN-DISCRETESEMI_MOSFET_PCH-DMG2305UX-7                     | [Link](https://componentsearchengine.com/part-view/DMG2305UX-7/Diodes%20Incorporated)                                    | [Link](https://componentsearchengine.com/part-view/DMG2305UX-7/Diodes%20Incorporated)                                |
| Q2                | ESP32_WROVER_SPARKFUN-DISCRETESEMI_MOSFET_PCH-DMG2305UX-7                     | #N/A                                                                                                                 | #N/A                                                                                                             |
| Q3                | D8                                                                           | [Link](https://componentsearchengine.com/part-view/SI1308EDL-T1-GE3/Vishay)                                             | [Link](https://componentsearchengine.com/part-view/SI1308EDL-T1-GE3/Vishay)                                         |
| R1                | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R1-PINH           | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R1-PINH1          | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R1_BAT            | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R1_PWRUSB         | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R2                | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | [Link](https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL)                           | [Link](https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL)                       |
| R2-PINH           | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R2-PINH1          | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R2-USB            | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R2-USB1           | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R2_BAT            | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R3                | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R4                | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R5                | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R6                | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R7                | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R8                | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R9                | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R10               | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| RESET_BUTTON      | BUTTON_CUSYOMV1                                                              | [Link](https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k)                   | [Link](https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k)               |
| R_BOOT            | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R_CAPACITOR       | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R_CHANGE          | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R_CL1             | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| R_RESET           | ESP32_WROVER_EAGLE-LTSPICE_RR0402                                            | #N/A                                                                                                                 | #N/A                                                                                                             |
| SENSOR2           | ESP32_WROVER_BME680_BME680                                                   | [Link](https://www.snapeda.com/parts/BME680/Bosch/view-part/?welcome=home)                                           | [Link](https://www.snapeda.com/parts/BME680/Bosch/view-part/?welcome=home)                                       |
| SJ1               | SJ                                                                           | [Link](https://grabcad.com/library/solder-jumpers-1)                                                                 | [Link](https://grabcad.com/library/solder-jumpers-1)                                                             |
| TP1               | TPTP20R                                                                      | #N/A                                                                                                                 | #N/A                                                                                                             |
| TP2               | TPTP20R                                                                      | #N/A                                                                                                                 | #N/A                                                                                                             |
| TP3               | TPTP20R                                                                      | #N/A                                                                                                                 | #N/A                                                                                                             |
| TP4               | TPTP20R                                                                      | #N/A                                                                                                                 | #N/A                                                                                                             |
| TP5               | TPTP20R                                                                      | #N/A                                                                                                                 | #N/A                                                                                                             |
| TP6               | TPTP20R                                                                      | #N/A                                                                                                                 | #N/A                                                                                                             |
| TP7               | TPTP20R                                                                      | #N/A                                                                                                                 | #N/A                                                                                                             |
| TP8               | TPTP20R                                                                      | #N/A                                                                                                                 | #N/A                                                                                                             |
| TP9               | TPTP20R                                                                      | #N/A                                                                                                                 | #N/A                                                                                                             |
| TP10              | TPTP20R                                                                      | #N/A                                                                                                                 | #N/A                                                                                                             |
| TP11              | TPTP20R                                                                      | #N/A                                                                                                                 | #N/A                                                                                                             |
| TP12              | TPTP20R                                                                      | #N/A                                                                                                                 | #N/A                                                                                                             |
| TP13              | TPTP20R                                                                      | #N/A                                                                                                                 | #N/A                                                                                                             |
| TP14              | TPTP20R                                                                      | #N/A                                                                                                                 | #N/A                                                                                                             |
| TP15              | TPTP20R                                                                      | #N/A                                                                                                                 | #N/A                                                                                                             |
| TP16              | TPTP20R                                                                      | #N/A                                                                                                                 | #N/A                                                                                                             |
| TP17              | TPTP20R                                                                      | #N/A                                                                                                                 | #N/A                                                                                                             |
| U1                | W25Q512JVEIQ                                                                 | [Link](https://www.snapeda.com/parts/W25Q512JVEIQ/Winbond+Electronics/view-part/?ref=eda)                              | [Link](https://www.snapeda.com/parts/W25Q512JVEIQ/Winbond+Electronics/view-part/?ref=eda)                          |
| U2                | ESP32-C6-WROOM-1-N8                                                          | [Link](https://www.snapeda.com/parts/ESP32-C6-WROOM-1-N8/Espressif+Systems/view-part/?ref=eda)                        | [Link](https://www.snapeda.com/parts/ESP32-C6-WROOM-1-N8/Espressif+Systems/view-part/?ref=eda)                    |
| U3                | DS3231SN#                                                                    | [Link](https://www.snapeda.com/parts/DS3231SN%23/Analog+Devices/view-part/?ref=eda)                                   | [Link](https://www.snapeda.com/parts/DS3231SN%23/Analog+Devices/view-part/?ref=eda)                               |
| U4                | MAX17048G+T10                                                                | [Link](https://www.snapeda.com/parts/MAX17048G+T10/Analog+Devices/view-part/?ref=eda)                                 | [Link](https://www.snapeda.com/parts/MAX17048G+T10/Analog+Devices/view-part/?ref=eda)                             |
| U5                | ESP32_WROVER_SPARKFUN-IC-POWER_MCP73831                                      | [Link](https://componentsearchengine.com/part-view/MCP73831T-2ATI%2FOT/Microchip)                                      | [Link](https://componentsearchengine.com/part-view/MCP73831T-2ATI%2FOT/Microchip)                                  |

## Descriere Funcționalități Hardware

---

## 1. Unitate de Control – ESP32-C6  
- **Microcontroller**: `ESP32-C6-WROOM-1` (32-bit RISC-V @ 160 MHz)  
- **Memorie**:  
  - 512 KB SRAM integrat pentru procesare rapidă.  
  - 8 MB flash extern (`W25Q512JVEIQ`) pentru stocare persistentă.  
- **Conectivitate**:  
  - Wi-Fi 6 (802.11ax), Bluetooth Low Energy 5.  
  - Port USB 2.0 (full-speed).  
- **Periferice**:  
  - SPI, I²C, UART.  
  - 22 de pini GPIO configurabili.  
- **Eficiență energetică**:  
  - Moduri `sleep` și `deep sleep` (<10µA).  

---

## 2. Afișaj E-Ink (7.5 inch)  
- **Model**: Waveshare 800×480 px.  
- **Interfață**:  
  - SPI 4-fire (CS, DC, RST, BUSY).  
- **Consum energie**:  
  - **0W** în stare statică.  
  - Vârf de **25mA** la actualizare.  
- **Beneficiu**:  
  - Imagine persistentă fără alimentare.  

---

## 3. Senzor Multi-Parametru – BME680  
- **Măsurători**:  
  - Temperatură (±0.5°C), umiditate (±3%), presiune atmosferică, VOC.  
- **Interfață**: I²C @ 400 kHz.  
- **Consum**:  
  - 2.1µA în standby, 3.7mA în activitate.  
- **Avantaj**: Integrare 4-în-1 într-un singur cip.  

---

## 4. Sistem de Management al Energiei  
- **Baterie**: Li-Po 2500mAh (3.7V).  
- **Încărcare**:  
  - Controler `MCP73831` (1A via USB-C).  
- **Monitorizare**:  
  - `MAX17048` pentru nivel încărcare, tensiune și alertă.  
- **Regulator LDO**:  
  - `XC6220A331MR-G` (3.3V stabil).  

---

## 5. Interfață Utilizator – Butoane Tactile  
- **3 butoane** pentru navigare, selecție și control.  
- **Debouncing**:  
  - Hardware (circuite RC) sau software.  

---

## 6. Port USB-C  
- **Funcții**:  
  - Încărcare baterie și transfer date.  
- **Protecție**:  
  - Diodă ESD `USBLC6-2SC6Y`.  

---

## 7. Conector Qwiic pentru Expansiune  
- **4 pini standard**: VCC, GND, SDA, SCL.  
- **Scop**: Conectare senzori I²C externi (ex: senzor de lumină).  

---

## 8. Slot MicroSD  
- **Conector**: `112A-TAAR-R03`.  
- **Capacitate**: Suportă carduri microSD (stocare e-book-uri/log-uri).  
- **Interfață**: Configurabilă SPI/SD.  

---

## 9. Ceas Real-Time (DS3231)  
- **Precizie**: ±2ppm.  
- **Backup**: Supercondensator/baterie secundară.  

---

## 10. Memorie Flash Externă  
- **Model**: `W25Q512JVEIQ`.  
- **Interfață**: Quad SPI (133 MHz).  
- **Utilizare**: Firmware, setări, conținut utilizator.  

--- 

### 🔌 Interfețe și Alocare Resurse  

#### **Interfețe Utilizate**  
| Protocol | Componente Conectate               |  
|----------|------------------------------------|  
| **SPI**  | E-Paper, Memorie Flash, Card SD    |  
| **I²C**  | BME680, MAX17048, DS3231, Qwiic    |  
| **GPIO** | Butoane, Semnale Control E-Paper   |  
| **USB**  | Alimentare + Transfer Date (USB-C) |  

---

#### **Estimare Autonomie Baterie**  
| Componentă             | Consum (Activ) | Consum (Standby) |  
|------------------------|----------------|------------------|  
| **ESP32-C6**           | 80 mA          | <10 µA           |  
| **E-Paper (refresh)**  | 25 mA          | 0 mA             |  
| **BME680**             | 3.6 mA         | 2.1 µA           |  
| **MAX17048**           | -              | 50 µA            |  
| **DS3231**             | 3.5 mA         | <1 µA            |  
| **Total**              | ~150 mA        | ~100 µA          |  

---

#### **Mapare Pini ESP32-C6**  
| Pin   | Funcție Principală                 | Detalii                          |  
|-------|------------------------------------|----------------------------------|  
| GPIO1 | I²C SDA                            | Senzori BME680, MAX17048, DS3231 |  
| GPIO2 | I²C SCL                            | Clock pentru magistrala I²C      |  
| GPIO5 | SPI MISO (E-Paper)                 | Recepție date afișaj             |  
| GPIO6 | SPI MOSI (E-Paper)                 | Transmitere date afișaj          |  
| GPIO7 | SPI CLK (E-Paper)                  | Semnal ceas SPI                  |  
| GPIO8 | SPI CS (E-Paper)                   | Selectare chip afișaj            |  
| GPIO9 | DC (E-Paper)                       | Comutare date/comenzi            |  
| GPIO10| RST (E-Paper)                      | Reset hardware afișaj            |  
| GPIO11| BUSY (E-Paper)                     | Indică ocupare afișaj            |  
| GPIO12| Buton #1                           | Navigare "Pagina Următoare"      |  
| GPIO13| Buton #2                           | Navigare "Pagina Anterioară"     |  
| GPIO14| Buton #3                           | Meniu/Selectare                  |  
| GPIO15| ALERT (MAX17048)                   | Avertizare baterie scăzută       |  
| GPIO19| SD Card CS                         | Selectare card MicroSD           |  

---

### Conluzii
A fost un proiect foarte muncitoresc, care merita mai mult decat 2 pct.
Timp de lucru: 70h
