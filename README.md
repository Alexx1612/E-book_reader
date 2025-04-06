## OPENBOOK E-BOOK READER
OpenBook – Proiect TSC 2025
OpenBook este un prototip de eBook reader open-source, dezvoltat în jurul microcontrolerului ESP32-C6. Dispozitivul este echipat cu un afișaj E-Ink, baterie Li-Po, încărcare prin USB-C, slot pentru card microSD și o serie de senzori de mediu. Proiectul a presupus realizarea completă a schemei electrice, proiectarea plăcii PCB, modelarea 3D și generarea fișierelor pentru fabricație.

## Diagrama bloc
![esp32_block_diagram](https://github.com/user-attachments/assets/3ff822c3-2a7e-427a-aea1-734309ce878a)

## Funcționalitate hardware
ESP32-C6 controlează toate perifericele prin interfețele GPIO, SPI și I2C.

Afișajul E-Ink este operat prin SPI și are linii dedicate pentru RESET, DC și BUSY.

Bateria Li-Po este încărcată cu ajutorul controlerului MCP73831 și monitorizată de senzorul MAX17048.

Senzorul BME688 oferă date despre temperatură, umiditate, presiune și compuși volatili.

Modulul RTC DS3231 păstrează ora exactă și permite moduri eficiente de deep sleep.

Cardul microSD utilizează aceeași magistrală SPI cu afișajul.

Toate componentele sunt montate pe layer-ul TOP, iar rutarea este realizată în două straturi.


## Observații
Traseele de alimentare au o lățime de 0.3 mm, iar cele de semnal 0.15 mm

PCB-ul are o grosime de 1 mm, cu planuri de masă pe ambele straturi

Conectorii, ecranul și bateria au fost integrate în modelul 3D și testate pentru potrivirea în carcasă

Carcasa a fost importată și aliniată cu placa pentru redări vizuale realiste

Toate fișierele au fost verificate cu ERC (Electrical Rules Check) și DRC (Design Rules Check)
