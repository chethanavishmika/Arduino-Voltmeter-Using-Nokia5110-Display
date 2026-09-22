# Arduino Voltmeter using Nokia 5110 Display

A compact DC Voltmeter built with an **Arduino Uno** , a **Voltage Sensor Module (0–25V)** , and a **Nokia 5110 LCD** screen (PCD8544 controller) . 

This project measures DC voltage up to 25V using an analog input pin  and displays the real-time voltage on the Nokia 5110 screen .

---

## 📸 Overview & Features

* **Voltage Measurement Range:** 0V to 25V DC (using standard 5:1 voltage divider sensor) .
* **Real-time Display:** High-contrast display of current voltage on a classic 84x48 monochrome Nokia 5110 LCD .
* **Low Power & Simple Assembly:** Ideal weekend electronics project for beginners learning ADC readings and SPI LCD interfacing.

---

## 🛠 Hardware Required

| Component | Quantity | Description |
| :--- | :--- | :--- |
| **Arduino Uno** | 1 | ATmega328P Microcontroller Board  |
| **Nokia 5110 LCD** | 1 | 84x48 PCD8544 Monochrome Graphic Display  |
| **Voltage Sensor Module** | 1 | Voltage Divider Module (0–25V Max Input)  |
| **Breadboard & Wires** | - | Jumper wires for interconnections  |

---

## 🔌 Wiring & Pin Mapping

### 1. Nokia 5110 Display to Arduino Uno
> **Note:** Pin 8 (LIGHT/LED) is connected directly to 3.3V for backlight, and Pin 7 (GND) connects to Common Ground .

| Nokia 5110 Pin | Pin Name | Arduino Uno Pin | Wire Color (in diagram) |
| :--- | :--- | :--- | :--- |
| **Pin 1** | RST (Reset) | Digital Pin 8 | Yellow  |
| **Pin 2** | CE / CS (Chip Enable) | Digital Pin 9 | Grey  |
| **Pin 3** | DC (Data/Command) | Digital Pin 10 | Blue  |
| **Pin 4** | DIN / MOSI (Data In) | Digital Pin 11 | Brown  |
| **Pin 5** | CLK / SCK (Clock) | Digital Pin 12 | Magenta  |
| **Pin 6** | VCC | 5V | Red  |
| **Pin 7** | BL / LIGHT | GND Rail | Black  |
| **Pin 8** | GND | GND Rail | Black  |

### 2. Voltage Sensor Module to Arduino Uno

| Voltage Sensor Pin | Arduino Pin / Connection | Description |
| :--- | :--- | :--- |
| **S** (Signal) | **Analog Pin A0** | Voltage Sense Output (Green Wire)  |
| **+** | *Unconnected* | Not needed for passive voltage divider  |
| **-** | **GND** | Ground Rail (Black Wire)  |
| **Input Screw Terminal** | Voltage Source (+ / -) | Connect DC source to measure (0–25V)  |

---

## 📚 Required Libraries

Install these libraries via the **Arduino IDE Library Manager** (*Sketch > Include Library > Manage Libraries*):

1. **`Adafruit GFX Library`** by Adafruit
2. **`Adafruit PCD8544 Nokia 5110 LCD Library`** by Adafruit

---

## 🚀 How to Run

1. Wire your components following the pin mapping table above .
2. Connect your **Arduino Uno** to your computer via USB .
3. Open Arduino IDE, select board as **Arduino Uno**, and choose your COM port .
4. Upload the sketch code.
5. Connect the external DC voltage source (e.g., Li-ion battery or power supply) to the input terminal of the voltage sensor module .

---

## 📜 License
This project is open-source and available under the **MIT License**.
