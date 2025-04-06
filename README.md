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

