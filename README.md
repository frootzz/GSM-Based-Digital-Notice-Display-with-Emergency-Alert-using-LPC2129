# GSM-Based Digital Notice Display with Emergency Alert using LPC2129

## 1. Project Overview

This project is a GSM-based digital notice display system developed using the LPC2129 (ARM7) microcontroller and SIM800C GSM module.

The system receives SMS messages through the GSM module and displays the message content on a 16×2 alphanumeric LCD. It also provides visual and audio indications using red and green LEDs and a buzzer for normal and emergency message notifications.

The system helps deliver notices and emergency alerts remotely through GSM communication.

## 2. Hardware Components

- LPC2129 – ARM7 Microcontroller
- SIM800C – GSM Module
- 16×2 Alphanumeric LCD Display
- Red LED
- Green LED
- Buzzer
- Push Button

## 3. Software and Tools Used

- Embedded C
- Keil µVision – Code Development
- Flash Magic – Program Uploading
- HyperTerminal – Serial Communication Testing

## 4. Pin Configuration

### A. GSM Module (SIM800C) – UART0

| SIM800C Pin | LPC2129 Pin | Function |
|---|---|---|
| TXD | P0.1 (RXD0) | GSM Data Reception |
| RXD | P0.0 (TXD0) | GSM Data Transmission |
| GND | GND | Common Ground |
| VCC | External Power Supply | Power Supply |

### B. 16×2 LCD Display – 8-bit Mode

| LCD Pin | LPC2129 Pin | Function |
|---|---|---|
| D0 | P0.18 | Data |
| D1 | P0.19 | Data |
| D2 | P0.21 | Data |
| D3 | P0.22 | Data |
| D4 | P0.23 | Data |
| D5 | P0.24 | Data |
| D6 | P0.25 | Data |
| D7 | P0.27 | Data |
| RS | P0.8 | Register Select |
| E | P0.9 | Enable |

### C. LED, Buzzer and Push Button

| Component | LPC2129 Pin | Function |
|---|---|---|
| Green LED | P1.23 | Emergency Status Indication |
| Red LED | P1.24 | Normal Message Indication |
| Buzzer | P1.25 | Audio Alert |
| Push Button | P1.26 | Buzzer Control |

*Note: Pin assignments are based on the source code. Verify them against the actual hardware connections.*

## 5. Communication Interface

- UART0 is used for serial communication between the LPC2129 microcontroller and SIM800C GSM module.
- The LCD is interfaced with the LPC2129 in 8-bit mode.
- GPIO pins are used to control the LEDs, buzzer and push button.
- AT commands are used to configure GSM communication and send SMS messages.
- In code keep the phone number of other to communicate with the sim inside the GSM. Do not enter the phone number of the sim inserted in the GSM.
- In program you should edit the number in gsm.c

## 6. Working Principle

1. The LPC2129 microcontroller initializes the UART0, LCD, LEDs, buzzer and GSM module.
2. The SIM800C GSM module receives SMS messages from a mobile phone.
3. The received message is processed by the LPC2129.
4. The system extracts the message content between the `*` and `#` symbols.
5. The extracted message is displayed on the 16×2 LCD.
6. If the message contains the keyword `EMERGENCY`, the system activates the emergency indication and sends an emergency SMS.
7. For normal messages, the system provides a different LED and buzzer indication.
8. The push button is used to switch off the buzzer.

## 7. Key Features

- Wireless message reception using GSM technology.
- Digital notice display using a 16×2 LCD.
- Emergency message identification.
- SMS-based emergency notification.
- Red and green LED status indications.
- Buzzer-based audio alert.
- Push-button buzzer control.

## 8. Applications

- Educational institutions.
- Digital notice boards.
- Emergency notification systems.
- Public information display systems.
- Hospitals and other organizations.

## 9. Project Outcome

Developed a GSM-based digital notice display system using the LPC2129 ARM7 microcontroller. The system demonstrates wireless SMS reception, LCD interfacing, UART communication, message processing and emergency alert functionality.

## 10. Repository Contents

- Source_Code – Embedded C source files.
- Circuit_Diagram – Hardware circuit details.
- Project_Images – Project hardware photographs.
- README.md – Project documentation.

## 11. Future Enhancements

- Support for longer messages.
- Multiple recipient emergency notifications.
- Improved message storage and display.
- Integration with IoT-based monitoring systems.

---
**Project Domain:** Embedded Systems

**Microcontroller:** LPC2129 (ARM7)

**Communication:** GSM / UART

**Programming Language:** Embedded C
