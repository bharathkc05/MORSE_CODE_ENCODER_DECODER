# 📡 Arduino Morse Code Decoder with LCD & Buzzer  

This project implements a **Morse code encoder/decoder** using an **Arduino**, a **push button**, an **LCD (I2C)**, an **LED**, and a **buzzer**.  
It allows you to input Morse code by pressing a button, with **short presses for dots** and **long presses for dashes**.  
The code is **decoded in real-time**, displayed on the LCD, and signaled with light and sound.  

## ✨ Features  
- Encode Morse code with a **push button**  
- **LED & buzzer** provide dot/dash feedback  
- Automatic **dot/dash detection** based on press duration  
- Decodes Morse sequences into **alphanumeric characters**  
- Displays both **Morse input** and **decoded text** on a 16x2 LCD  
- Adds **spaces between words** automatically after inactivity  

## 🛠 Hardware Requirements  
- Arduino (Uno, Nano, etc.)  
- 16x2 I2C LCD (`0x27` address by default)  
- Push button (with pull-up)  
- LED + resistor  
- Buzzer (active/passive)  
- Jumper wires & breadboard  

## ⚡ Circuit Connections  

| Component   | Pin |
|-------------|-----|
| Push button | D2 (with internal pull-up) |
| LED         | D4 |
| Buzzer      | D5 |
| LCD SDA     | A4 |
| LCD SCL     | A5 |

## 📖 Usage Instructions  
1. Upload the sketch to your Arduino.  
2. **Press button briefly** → `.` (dot)  
3. **Press button longer** → `-` (dash)  
4. Pause → the character is decoded and displayed.  
5. Wait longer (~3 seconds) → space between words.  

LCD display format:  
M: .... . .-.. .-.. ---
T: HELLO

## 🧩 Example  
- Input: `....` → **H**  
- Input: `.` → **E**  
- Input: `.-..` → **L**  
- Input: `---` → **O**  

LCD shows:  
M: ---
T: HELLO

## 📂 File  
- `morse_decoder.ino` → main Arduino sketch  

## 🔮 Future Improvements  
- Add support for **punctuation in Morse**  
- Store decoded messages in **EEPROM**  
- Enable **serial input/output** for logging  
