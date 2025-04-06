TSC-PROJECT


## 2. BOM - Bill of Materials

| Name of component | Device                                       | Check Prices                                                                                                | DataSheet                                                                                                 |
|-------------------|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| BOOT_BUTTON       | BUTTON_CUSYOMV1                             | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| C1                | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| C1_BAT            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| C1_BAT1           | EAGLE-LTSPICE_CC0402                         | #N/A                                                                                                            | #N/A                                                                                                           |
| C1_BAT2           | EAGLE-LTSPICE_CC0402                         | #N/A                                                                                                            | #N/A                                                                                                           |
| C2                | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| C2_BAT\           | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| C3                | RCL_CPOL-EUCT3528                            | #N/A                                                                                                            | #N/A                                                                                                           |
| C4                | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |


## Descriere Funcționalități Hardware
1. Unitate de Control – ESP32-C6
Dispozitivul utilizează ESP32-C6-WROOM-1, un microcontroller bazat pe o arcelă RISC-V de 32 de biți, operând la o frecvență maximă de 160 MHz.

Memorie:

512 KB SRAM integrat pentru procesare rapidă.

8 MB memorie flash externă (W25Q512JVEIQ) pentru stocare persistentă.

Conectivitate:

Wi-Fi 6 (802.11ax), Bluetooth Low Energy 5, port USB 2.0 (full-speed).

Periferice: Interfețe SPI, I²C, UART și 22 de pini GPIO configurabili.

Eficiență Energetică: Modele de operare sleep și deep sleep (<10µA) pentru economisire baterie.

2. Afișaj E-Ink (7.5 inch)
Afișajul Waveshare (rezoluție 800×480 px) oferă o experiență de citire fără oboseală oculară.

Interfață: Comunicare prin SPI 4-fire, cu semnale dedicate (CS, DC, RST, BUSY).

Consum Energie:

0W în stare statică (imaginea rămâne vizibilă fără alimentare).

Vârf de 25mA în timpul actualizării afișajului.
Beneficiu: Ideal pentru aplicații cu autonomie ridicată datorită lipsei consumului în afara perioadelor de refresh.

3. Senzor Multi-Parametru – BME680
Funcționalități:

Măsurători precise pentru temperatură (±0.5°C), umiditate (±3%), presiune atmosferică și compuși organici volatili (VOC).

Interfață: Magistrală I²C la 400 kHz, partajată cu alte componente.

Consum: Doar 2.1µA în standby și până la 3.7mA în activitate.
Avantaj: Integrarea a patru senzori într-un singur cip simplifică designul și reduce costurile.

4. Sistem de Management al Energiei
Baterie: Li-Po 2500mAh (3.7V) pentru ore întregi de funcționare.

Încărcare: Modulul MCP73831 asigură încărcare sigură prin USB-C la curent de până la 1A.

Monitorizare Baterie: MAX17048 urmărește nivelul de încărcare și tensiune în timp real, comunicând prin I²C.

Regulator LDO: XC6220A331MR-G generează o tensiune stabilă de 3.3V pentru circuitele sensibile.

5. Interfață Utilizator – Butoane Tactile
3 butoane cu feedback tactil pentru navigare, selecție și control.

Debouncing: Implementat prin circuite RC (hardware) sau algoritmi în firmware, prevenind semnale false.

6. Port USB-C
Funcții Duale: Încărcare baterie și transfer de date (firmware, fișiere).

Securitate: Protecție ESD cu USBLC6-2SC6Y și rezistențe de terminare conforme standardelor USB.

7. Conector Qwiic pentru Expansiune
4 Pini Standardizați (VCC, GND, SDA, SCL) pentru conectarea rapidă a senzorilor I²C.

Utilizare: Prototipare sau adăugare de funcționalități suplimentare (ex: senzor de lumină).

8. Slot MicroSD
Conector 112A-TAAR-R03: Suportă carduri microSD pentru stocare suplimentară (e-book-uri, log-uri).

Interfață Configurabilă: Funcționează în mod SPI sau SD standard, în funcție de cerințele firmware-ului.

9. Ceas Real-Time (DS3231)
Precizie: Abatere de doar ±2ppm în condiții normale.

Backup Energie: Supercondensator sau baterie mică menține timpul chiar și fără alimentare principală.

10. Memorie Flash Externă
W25Q512JVEIQ: Conectată prin interfață Quad SPI, oferind viteză ridicată de citire/scriere (până la 133 MHz).

Utilizare: Stochează firmware, setări și conținut utilizator (ex: cărți electronice).
| C4_USB            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| C5                | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| C5_USB            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| C6                | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| C7                | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| C8                | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| C9                | EAGLE-LTSPICE_CC0402                         | #N/A                                                                                                            | #N/A                                                                                                           |
| C10               | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| C10_SUPERCAP      | CPH3225A                                     | https://www.snapeda.com/parts/CPH3225A/Seiko+Instruments/view-part/?ref=eda                                   | https://www.snapeda.com/parts/CPH3225A/Seiko+Instruments/view-part/?ref=eda                                   |
| CHANGE_BUTTON     | BUTTON_CUSYOMV1                             | https://industry.panasonic.com/global/en/products/control/switch-light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch-light-touch/number/evqpuj02k                  |
| CHG_LED           | ADAFRUIT_LEDCHIP-LED0603                     | https://www.snapeda.com/parts/KP-1608SURCK/Kingbright/view-part/?ref=search&t=LED%200603                       | https://www.snapeda.com/parts/KP-1608SURCK/Kingbright/view-part/?ref=search&t=LED%200603                       |
| C_DELAY           | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| D1                | USBLC6-2SC6Y                                 | https://www.snapeda.com/parts/USBLC6-2SC6Y/STMicroelectronics/view-part/?ref=eda                              | https://www.snapeda.com/parts/USBLC6-2SC6Y/STMicroelectronics/view-part/?ref=eda                              |
| D2                | ESP32_WROVER_AVX---SD0805S020S1R0_AVX_...    | https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D              | http://datasheets.avx.com/schottky.pdf                                                                         |
| D3                | MBR0530                                      | https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D              | https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D              |
| D4                | MBR0530                                      | https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda                                                | https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda                                                |
| D5                | MBR0530                                      | https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda                                                | https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda                                                |
| D6                | PGB1010603MR                                 | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      |
| D7                | ESP32_WROVER_AVX---SD0805S020S1R0_AVX_...    | https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D              | http://datasheets.avx.com/schottky.pdf                                                                         |
| D8                | PGB1010603MR                                 | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      |
| D9                | PGB1010603MR                                 | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      |
| D10               | PGB1010603MR                                 | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      |
| D11               | PGB1010603MR                                 | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      |
| D12               | PGB1010603MR                                 | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      |
| EPD_C1            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| EPD_C2            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| EPD_C5            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| EPD_C6            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| EPD_C7            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| EPD_C8            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| EPD_C9            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| EPD_C10           | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| EPD_C11           | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| EPD_C12           | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| IC1               | BD5229G-TR                                   | https://componentsearchengine.com/part-view/BD5229G-TR/ROHM%20Semiconductor                                    | https://componentsearchengine.com/part-view/BD5229G-TR/ROHM%20Semiconductor                                    |
| IC4               | XC6220A331MR-G                               | https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex                                              | https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex                                              |
| J1                | FH34SRJ-24S-0.5SH_99_                        | https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex                                              | https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex                                              |
| J2                | SAMACSYS_PARTS_USB4110-GF-A                  | https://componentsearchengine.com/part-view/USB4110-GF-A/GCT%20(GLOBAL%20CONNECTOR%20TECHNOLOGY               | https://componentsearchengine.com/part-view/USB4110-GF-A/GCT%20(GLOBAL%20CONNECTOR%20TECHNOLOGY               |
| J3                | QWIIC_CONNECTORJS-1MM                        | #N/A                                                                                                            | #N/A                                                                                                           |
| J4                | 112A-TAAR-R03_ATTEND                         | https://store.comet.srl.ro/Catalogue/Product/43497/                                                            | https://store.comet.srl.ro/Catalogue/Product/43497/                                                            |
| L1                | 744043680IND_4828-WE-TPC_WRE                 | https://eu.mouser.com/ProductDetail/Wurth-Elektronik/744043680?qs=PGXP4M47uW6VkZq%252BkzjrHA%3D%3D               | https://eu.mouser.com/ProductDetail/Wurth-Elektronik/744043680?qs=PGXP4M47uW6VkZq%252BkzjrHA%3D%3D               |
| PFMF.050.1        | ESP32C6_VARISTORCN1812                       | https://www.mouser.co.uk/ProductDetail/EPCOS-TDK/B72520T0350K062?qs=dEfas%2FXlABIszF52uu7vrg%3D%3D              | https://www.mouser.co.uk/ProductDetail/EPCOS-TDK/B72520T0350K062?qs=dEfas%2FXlABIszF52uu7vrg%3D%3D              |
| Q1                | ESP32_WROVER_SPARKFUN-DISCRETESEMI_MOSFET_...| https://componentsearchengine.com/part-view/DMG2305UX-7/Diodes%20Incorporated                                  | https://componentsearchengine.com/part-view/DMG2305UX-7/Diodes%20Incorporated                                  |
| Q2                | ESP32_WROVER_SPARKFUN-DISCRETESEMI_MOSFET_...| #N/A                                                                                                            | #N/A                                                                                                           |
| Q3                | D8                                           | https://componentsearchengine.com/part-view/SI1308EDL-T1-GE3/Vishay                                           | https://componentsearchengine.com/part-view/SI1308EDL-T1-GE3/Vishay                                           |
| R1                | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R1-PINH           | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R1-PINH1          | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R1_BAT            | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R1_PWRUSB         | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R2                | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R2-PINH           | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R2-PINH1          | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R2-USB            | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R2-USB1           | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R2_BAT            | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R3                | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R4                | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R5                | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R6                | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R7                | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R8                | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R9                | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R10               | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| RESET_BUTTON      | BUTTON_CUSYOMV1                             | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| R_BOOT            | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R_CAPACITOR       | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R_CHANGE          | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R_CL1             | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| R_RESET           | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | #N/A                                                                                                            | #N/A                                                                                                           |
| SENSOR2           | ESP32_WROVER_BME680_BME680                   | https://www.snapeda.com/parts/BME680/Bosch/view-part/?welcome=home                                            | https://www.snapeda.com/parts/BME680/Bosch/view-part/?welcome=home                                            |
| SJ1              | SJ                                           | https://grabcad.com/library/solder-jumpers-1                                                                   | https://grabcad.com/library/solder-jumpers-1                                                                   |
| TP1               | TPTP20R                                      | #N/A                                                                                                            | #N/A                                                                                                           |
| TP2               | TPTP20R                                      | #N/A                                                                                                            | #N/A                                                                                                           |
| TP3               | TPTP20R                                      | #N/A                                                                                                            | #N/A                                                                                                           |
| TP4               | TPTP20R                                      | #N/A                                                                                                            | #N/A                                                                                                           |
| TP5               | TPTP20R                                      | #N/A                                                                                                            | #N/A                                                                                                           |
| TP6               | TPTP20R                                      | #N/A                                                                                                            | #N/A                                                                                                           |
| TP7               | TPTP20R                                      | #N/A                                                                                                            | #N/A                                                                                                           |
| TP8               | TPTP20R                                      | #N/A                                                                                                            | #N/A                                                                                                           |
| TP9               | TPTP20R                                      | #N/A                                                                                                            | #N/A                                                                                                           |
| TP10              | TPTP20R                                      | #N/A                                                                                                            | #N/A                                                                                                           |
| TP11              | TPTP20R                                      | #N/A                                                                                                            | #N/A                                                                                                           |
| TP12              | TPTP20R                                      | #N/A                                                                                                            | #N/A                                                                                                           |
| TP13              | TPTP20R                                      | #N/A                                                                                                            | #N/A                                                                                                           |
| TP14              | TPTP20R                                      | #N/A                                                                                                            | #N/A                                                                                                           |
| TP15              | TPTP20R                                      | #N/A                                                                                                            | #N/A                                                                                                           |
| TP16              | TPTP20R                                      | #N/A                                                                                                            | #N/A                                                                                                           |
| TP17              | TPTP20R                                      | #N/A                                                                                                            | #N/A                                                                                                           |
| U1                | W25Q512JVEIQ                                 | https://www.snapeda.com/parts/W25Q512JVEIQ/Winbond+Electronics/view-part/?ref=eda                             | https://www.snapeda.com/parts/W25Q512JVEIQ/Winbond+Electronics/view-part/?ref=eda                             |
| U2                | ESP32-C6-WROOM-1-N8                          | https://www.snapeda.com/parts/ESP32-C6-WROOM-1-N8/Espressif+Systems/view-part/?ref=eda                        | https://www.snapeda.com/parts/ESP32-C6-WROOM-1-N8/Espressif+Systems/view-part/?ref=eda                        |
| U3                | DS3231SN#                                    | https://www.snapeda.com/parts/DS3231SN%23/Analog+Devices/view-part/?ref=eda                                   | https://www.snapeda.com/parts/DS3231SN%23/Analog+Devices/view-part/?ref=eda                                   |
| U4                | MAX17048G+T10                                | https://www.snapeda.com/parts/MAX17048G+T10/Analog+Devices/view-part/?ref=eda                                 | https://www.snapeda.com/parts/MAX17048G+T10/Analog+Devices/view-part/?ref=eda                                 |
| U5                | ESP32_WROVER_SPARKFUN-IC-POWER_MCP73831      | https://eu.mouser.com/ProductDetail/Microchip-Technology/MCP73831T-2ACI-OT?qs=yUQqVecv4qvbBQBGbHx0Mw%3D%3Dcf   | https://eu.mouser.com/ProductDetail/Microchip-Technology/MCP73831T-2ACI-OT?qs=yUQqVecv4qvbBQBGbHx0Mw%3D%3Dcf   |
