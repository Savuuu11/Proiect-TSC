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

🛠 **Diagramă Simplificată**:  
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
