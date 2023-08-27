# Library Attendance System with Arduino

This project is an Arduino-based Library Attendance System that utilizes RFID card scanning, an LCD display, an RTC module, and an SD card module to track student attendance in a library.

## Table of Contents

- [Features](#features)
- [Components](#components)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Features

- RFID card scanning for student identification.
- Real-time clock (RTC) for accurate timestamping.
- Data logging to an SD card for attendance records.
- Visual feedback through an LCD display.
- Servo motor for access control.

## Components

To replicate this project, you'll need the following components:

- Arduino board
- MFRC522 RFID module
- RTC DS3231 module
- SD card module
- I2C LCD display
- Servo motor
- RFID cards for student identification

## Installation

1. **Arduino IDE**: Install the Arduino IDE on your computer if you haven't already.

2. **Libraries**: Install the required libraries by going to "Sketch" -> "Include Library" -> "Manage Libraries" in the Arduino IDE. Install the following libraries:
   - MFRC522 by GithubCommunity (for RFID)
   - RTClib by Adafruit (for RTC)
   - SD by Arduino (for SD card)
   - Wire by Arduino (for I2C)

3. **Hardware Connections**: Connect the components to the Arduino board following the wiring diagram for your specific setup. Refer to the code comments for pin configurations.

4. **Upload Code**: Open the Arduino sketch (`Library_Attendance.ino`) in the Arduino IDE and upload it to your Arduino board.

## Usage

1. **Card Registration**: Prepare RFID cards for each student and add their UID values to the `cards` array in the code. Also, add their names and student numbers to the respective arrays.

2. **Running the System**: Power on the Arduino system. It will display the date and time on the LCD. When a student scans their RFID card, their attendance is recorded and displayed on the LCD. Invalid cards or duplicate scans are also handled.

3. **Data Storage**: Attendance records are saved to an SD card in the "test.txt" file.

4. **Access Control**: A servo motor is used for access control. It opens briefly for authorized users.

5. **Monitoring**: You can monitor the system's activity through the Arduino IDE's Serial Monitor.

## Contributing

Contributions to this project are welcome. If you have ideas for improvements or bug fixes, please feel free to open an issue or create a pull request.

## License

This project is open-source and available under the [MIT License](LICENSE). You are free to use, modify, and distribute this code for your purposes.
