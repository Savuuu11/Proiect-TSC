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
