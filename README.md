# Arduino Door Lock System

This project implements a secure door lock system using an Arduino microcontroller. It features a 4x4 keypad for password entry, an I2C LCD for user feedback, and a servo motor to actuate the lock.

## Features

- **Password-Protected:** Secure your door with a customizable password.
- **LCD Display:** An I2C LCD provides real-time feedback and instructions.
- **Servo Motor Actuator:** A servo motor reliably controls the locking mechanism.
- **User-Friendly Keypad:** A 4x4 keypad allows for easy password entry.
- **Visual Indicators:** Custom characters on the LCD indicate locked/unlocked states.

## Hardware Requirements

- **Arduino Uno** (or any other compatible board)
- **4x4 Keypad**
- **1602 I2C LCD Display**
- **Servo Motor** (e.g., SG90)
- **Jumper Wires**
- **Breadboard**

## Software Requirements

- **Arduino IDE:** To upload the code to the Arduino board.
- **Libraries:**
  - `Keypad.h`
  - `LiquidCrystal_I2C.h`
  - `Servo.h`

## Installation

1.  **Hardware Setup:**
    *   Connect the 4x4 keypad to the Arduino digital pins 1 through 8.
    *   Connect the I2C LCD display to the Arduino's I2C pins (SDA, SCL).
    *   Connect the servo motor to digital pin 0.
    *   Power the components accordingly.

2.  **Software Setup:**
    *   Open the `sketch_dec30b.ino` file in the Arduino IDE.
    *   Install the required libraries (`Keypad`, `LiquidCrystal_I2C`, `Servo`) through the Library Manager.
    *   Select your board and port from the `Tools` menu.
    *   Upload the sketch to your Arduino.

## Usage

1.  **Power On:** Power up the Arduino. The LCD will display a welcome message.
2.  **Enter Password:** The LCD will prompt you to enter the password. Use the keypad to enter the pre-set password (`137926A`).
3.  **Correct Password:** If the password is correct, the servo motor will unlock the door, and the LCD will display an "Opened" message.
4.  **Incorrect Password:** If the password is incorrect, the LCD will display a "Wrong Password" message and a countdown timer before you can try again.
5.  **Lock the Door:** To lock the door, press the `#` key on the keypad. The servo motor will move to the locked position, and the LCD will confirm that the door is closed.
