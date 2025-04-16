## OPENBOOK E-BOOK READER
OpenBook – Proiect TSC 2025
OpenBook este un prototip de eBook reader open-source, dezvoltat în jurul microcontrolerului ESP32-C6. Dispozitivul este echipat cu un afișaj E-Ink, baterie Li-Po, încărcare prin USB-C, slot pentru card microSD și o serie de senzori de mediu. Proiectul a presupus realizarea completă a schemei electrice, proiectarea plăcii PCB, modelarea 3D și generarea fișierelor pentru fabricație.

## Diagrama bloc
![Diagrama](https://github.com/user-attachments/assets/99139243-29ee-4272-857f-b19547ab3e1b)


### Caracteristici Cheie
- **Alimentare prin USB-C**  
  Permite programarea ușoară și încărcarea bateriei, asigurând o integrare simplificată cu sursa de alimentare.
- **Microcontroller ESP32-C6**  
  Dispune de un nucleu RISC-V, Wi-Fi 6, BLE și 8MB memorie flash internă pentru aplicații complexe și conectivitate modernă.
- **Senzori Integrați**  
  - **BME688:** Măsoară temperatura, umiditatea, presiunea și concentrațiile de gaze.  
  - **DS3231:** Modul RTC de înaltă precizie, care menține ceasul de timp real chiar și în absența alimentării principale.
- **Stocare Suplimentară**  
  - **Card SD (SPI):** Permite stocarea locală a e-book-urilor și datelor adiționale.  
  - **Memorie NOR Flash (W25Q512):** Oferă spațiu suplimentar de stocare prin interfața SPI.
- **Afișaj E-Paper**  
  Realizează afișajul e-book-urilor cu consum ultra-redus, prin actualizări doar la nevoie.
- **Monitorizare Baterie**  
  Modulul MAX17048 monitorizează nivelul de încărcare al bateriei, contribuind la gestionarea eficientă a consumului de energie.

## Bill of materials (BOM)

| Component                          | Supplier Link                                                                                                                                                 | Datasheet                                                                                                         |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| XC6220A331MR-G                     | [Model](https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex)                                                                                      | [Datasheet](https://product.torexsemi.com/system/files/series/xc6220.pdf)                                            |
| W25Q512JVEIQ                       | [Model](https://www.snapeda.com/parts/W25Q512JVEIQ/Winbond+Electronics/view-part/?ref=eda)                                                                        | [Datasheet](https://www.winbond.com/resource-files/W25Q512JV%20SPI%20RevB%2006252019%20KMS.pdf)                      |
| USBLC6-2SC6Y                       | [Model](https://www.snapeda.com/parts/USBLC6-2SC6Y/STMicroelectronics/view-part/?welcome=home&ref=eda)                                                            | [Datasheet](https://www.snapeda.com/parts/USBLC6-2SC6Y/STMicroelectronics/datasheet/)                              |
| USB4110-GF-A                       | [Model](https://componentsearchengine.com/part-view/USB4110-GF-A/GCT%20(GLOBAL%20CONNECTOR%20TECHNOLOGY))                                                        | [Datasheet](https://gct.co/files/drawings/usb4110.pdf)                                                             |
| SJ                                 | [Model](https://grabcad.com/library/solder-jumpers-1)                                                                                                          | [Datasheet]()                                                                                                     |
| SI1308EDL-T1-GE3 MOSFET             | [Model](https://www.snapeda.com/parts/SI1308EDL-T1-GE3/Vishay+Siliconix/view-part/?welcome=home&ref=eda)                                                        | [Datasheet](https://www.snapeda.com/parts/SI1308EDL-T1-GE3/Vishay%20Siliconix/datasheet/)                           |
| Resistor 0402                      | [Model](https://grabcad.com/library/resistor-0402-1)                                                                                                           | [Datasheet](https://www.yageo.com/upload/media/product/products/datasheet/rchip/PYu-RC_Group_51_RoHS_L_12.pdf)       |
| RCL CPOL 3528                      | [Model](https://www.snapeda.com/parts/CPH3225A/Seiko+Instruments/view-part/?ref=eda)                                                                             | [Datasheet](https://s3.amazonaws.com/snapeda/datasheet/TAJB475K025RNJ_AVX.pdf)                                     |
| QWIIC Connector                    | [Model](https://www.snapeda.com/parts/PRT-14417/SparkFun/view-part/)                                                                                           | [Datasheet](https://www.snapeda.com/parts/PRT-14417/SparkFun%20Electronics/datasheet/)                              |
| PGB1010603MR                       | [Model](https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda)                                                                               | [Datasheet](https://www.snapeda.com/parts/PGB1010603MR/Littelfuse%20Inc./datasheet/)                                |
| MBR0530 Schottky Diode             | [Model](https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=snap)                                                                                        | [Datasheet](https://www.snapeda.com/parts/MBR0530/ON%20Semiconductor/datasheet/)                                   |
| MAX17048G+T10                      | [Model](https://www.snapeda.com/parts/MAX17048G+T10/Analog+Devices/view-part/?ref=eda)                                                                            | [Datasheet](https://www.snapeda.com/parts/MAX17048G+T10/Analog%20Devices/datasheet/)                                |
| LED Chip 0603                      | [Model](https://www.snapeda.com/parts/KP-1608SURCK/Kingbright/view-part/?ref=search&t=LED%200603)                                                                 | [Datasheet](https://www.snapeda.com/parts/KP-1608SURCK/Kingbright/datasheet/)                                      |
| FH34SRJ-24S-0.5SH                  | [Model](https://ro.mouser.com/ProductDetail/Hirose-Connector/FH34SRJ-24S-0.5SH99?qs=vcbW%252B4%252BSTIpKBl5ap9J8Fw%3D%3D)                                       | [Datasheet](https://www.snapeda.com/parts/FH34SRJ-24S-0.5SH(99)/Hirose%20Connector/datasheet/)                     |
| ESP32C6 WROOM-1-N8                 | [Model](https://www.snapeda.com/parts/ESP32-C6-WROOM-1-N8/Espressif+Systems/view-part/?ref=eda)                                                                    | [Datasheet](https://www.snapeda.com/parts/ESP32-C6-WROOM-1-N8/Espressif%20Systems/datasheet/)                       |
| ESP32C6 Varistor 1812              | [Model]()                                                                                                                                                      | [Datasheet]()                                                                                                     |
| ESP32 WROVER MCP73831 Power Management | [Model](https://www.snapeda.com/parts/BME680/Bosch/view-part/?welcome=home)                                                                                 | [Datasheet](https://www.snapeda.com/parts/MCP73831T-2ACI/OT/Microchip/datasheet/)                                  |
| ESP32 WROVER BME680 Sensor         | [Model](https://www.snapeda.com/parts/BME680/Bosch/view-part/?welcome=home)                                                                                     | [Datasheet](https://www.bosch-sensortec.com/media/boschsensortec/downloads/datasheets/bst-bme680-ds001.pdf)         |
| ESP32 WROVER 0805 Capacitor        | [Model]()                                                                                                                                                      | [Datasheet]()                                                                                                     |
| DS3231SN                           | [Model](https://www.snapeda.com/parts/DS3231SN%23/Analog+Devices/view-part/?ref=eda)                                                                             | [Datasheet](https://www.snapeda.com/parts/DS3231SN%23/Analog%20Devices/datasheet/)                                  |
| Custom Button                      | [Model](https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k)                                                            | [Datasheet](https://industry.panasonic.com/global/en/downloads?tab=catalog&small_g_cd=203&part_no=EVQPUJ02K)         |
| CPH3225A                         | [Model](https://www.snapeda.com/parts/CPH3225A/Seiko+Instruments/view-part/?ref=snap)                                                                           | [Datasheet](https://www.snapeda.com/parts/CPH3225A/Seiko%20Instruments/datasheet/)                                |
| Capacitor 0402                     | [Model](https://ro.mouser.com/c/passive-components/capacitors/ceramic-capacitors/?q=CC0402&srsltid=AfmBOoogjqwwed3xvp6V5-bfVkRuawirfMcnAC47L-UQdC3mnXJk097M) | [Datasheet](https://componentsearchengine.com/Datasheets/2/CC0402MRX5R5BB106.pdf)                                  |
| BD5229G-TR                         | [Model](https://componentsearchengine.com/part-view/BD5229G-TR/ROHM%20Semiconductor)                                                                            | [Datasheet](https://fscdn.rohm.com/en/products/databook/datasheet/ic/power/voltage_detector/bd52xxg-e.pdf)         |
| 744043680                          | [Model](https://ro.mouser.com/ProductDetail/Wurth-Elektronik/744043680?qs=PGXP4M47uW6VkZq%252BkzjrHA%3D%3D)                                                   | [Datasheet](https://www.we-online.com/components/products/datasheet/744043680.pdf)                                  |
| 112A-TAAR-R03                      | [Model](https://store.comet.srl.ro/Catalogue/Product/43497/)                                                                                                  | [Datasheet](https://www.snapeda.com/parts/112A-TAAR-R03/Attend/datasheet/)                                         |
                                             

## Consum

| Component                        | Current Draw (mA) | Voltage (V) | Power (mW)   |
|----------------------------------|-------------------|-------------|--------------|
| ESP32-C6 (Wi-Fi active)          | 200               | 3.3         | 660          |
| E-Paper Display (Updating)       | 40                | 3.3         | 132          |
| BME688 Sensor (Measuring)        | 3.1               | 3.3         | 10.23        |
| RTC Module (Active)              | 0.15              | 3.3         | 0.495        |
| SD Card (Active)                 | 50                | 3.3         | 165          |
| Externar NOR Flash               | 25                | 3.3         | 82.5         |
| **Total Estimated Power Consumption** | ~318.5 mA         | 3.3         | 1050.72      |


### Arhitectura Hardware
- **Alimentare și Protecție:**  
  Sistemul beneficiază de alimentare prin USB-C și include protecții ESD (varistori, diodă TVS) pentru siguranța componentelor. Circuitul de încărcare Li-Po (MCP73831) și regulatorul LDO asigură o tensiune stabilă de 3.3V.
- **Conectivitate și Interfețe:**  
  Microcontrollerul ESP32-C6-WROOM-1 acționează ca nucleu central, conectând diferite periferice prin:
  - **SPI:** Utilizat pentru afișajul E-Paper, Cardul SD și memoria NOR Flash.  
  - **I2C:** Folosit pentru senzorii BME688 și DS3231, precum și pentru monitorizarea bateriei.  
  - **GPIO:** Gestionarea butoanelor de control (RESET, BOOT) și alte funcții digitale.

### Mapare Pini ESP32-C6
| Component                                | ESP32-C6 Pin(s)                                                     | Interface | Scop                                                                                   |
|------------------------------------------|---------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------|
| **E-Paper Display**                      | IO7 (MOSI), IO6 (SCK), IO10 (CS), IO5 (DC), IO23 (RST), IO3 (BUSY)    | SPI       | Transferă datele imaginii către afișaj și controlează starea acestuia.                  |
| **Battery Monitoring (MAX17048)**        | IO21 (SDA), IO22 (SCL)                                               | I2C       | Monitorizează tensiunea bateriei și starea de încărcare pentru un management energetic eficient. |
| **USB-C Connection**                     | GPIOs prin circuit de protecție și reglementare                       | USB       | Furnizează alimentarea și permite programarea ESP32-C6.   
| **MicroSD Card**                         | IO7 (MOSI), IO6 (SCK), IO4 (SS_SD), IO2 (MISO)                        | SPI       | Permite stocarea și accesarea fișierelor de e-book.                                     |
| **Environmental Sensor (BME688)**        | IO21 (SDA), IO22 (SCL)                                               | I2C       | Măsoară temperatura, umiditatea, presiunea și calitatea aerului.                        |
| **RTC Module (DS3231)**                  | IO21 (SDA), IO22 (SCL), IO18 (RST), IO1 (32KHz), IO0 (INT_RTC)         | I2C       | Menține ceasul de timp real în mod precis, chiar și în absența alimentării principale.    |
| **External NOR Flash**                   | IO11 (CS), IO6 (SCK), IO2 (MISO), IO7 (MOSI)                          | SPI       | Oferă stocare suplimentară pentru datele aplicațiilor și firmware.                      |
| **Control Buttons**                      | IO9 (BOOT), IO15 (CHANGE), EN (RESET)                                  | GPIO      | Permite interacțiunea utilizatorului prin funcții de boot, reset și alte comenzi digitale.|        

## Observații Suplimentare

- Traseele de alimentare au o lățime de 0.3 mm, iar traseele de semnal sunt proiectate cu o lățime de 0.15 mm, pentru a asigura o transmisie clară și o pierdere minimă de semnal.
- PCB-ul are o grosime de 1 mm și include planuri de masă pe ambele straturi, pentru a optimiza împământarea și a reduce interferențele electromagnetice.
- Conectorii, afișajul E-Paper și bateria au fost integrate în modelul 3D, iar acestea au fost testate riguros pentru a asigura o potrivire perfectă în carcasă.
- Carcasa a fost importată și aliniată cu placa pentru a obține render-uri vizuale realiste, facilitând astfel evaluarea designului final.
- Toate fișierele de proiect au fost verificate prin ERC (Electrical Rules Check) și DRC (Design Rules Check) pentru a asigura conformitatea cu standardele de proiectare și a elimina eventualele erori de fabricație.
