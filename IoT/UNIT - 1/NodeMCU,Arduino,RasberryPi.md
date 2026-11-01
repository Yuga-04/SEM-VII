# Hardware Platforms Used in IoT – Arduino, Raspberry Pi and NodeMCU (13 Marks)

## 1. Introduction

Hardware platforms play an important role in the development of Internet of Things (IoT) applications. They act as the physical interface between sensors, actuators and the internet.

The three commonly used hardware platforms in IoT are:

1. Arduino
2. Raspberry Pi
3. NodeMCU

These platforms are used to collect data from sensors, process information and control devices based on the received data.

## 2. Arduino

[1.3 Getting to Know Your Arduino Board — SunFounder Beginners Lab Kit  documentation](https://images.openai.com/static-rsc-4/By4kAB7G0iw4Bso8W6cvR1AbJQ85hSwnjhk0ZvH7QDLoLOJ4dzufPfx2XYJu-ywOrAFYc4q2f--4ZPqJsdnE7vxKrYNfLVYTr7lGOQo1H0Ry0qbgcPTjhz_Ot0hGat909Cv2JFH83IQ5s-u9BGsIvfsIgiDIlRO5htzUV8l4RtI?purpose=inline)

[docs.sunfounder.com](https://docs.sunfounder.com/projects/beginners-lab-kit/en/latest/lessons/1.3_know_the_board.html?utm_source=chatgpt.com)

Arduino is an open-source prototyping platform based on easy-to-use hardware and software. It consists of a programmable circuit board containing a microcontroller and Arduino IDE software, which is used to write and upload programs.

### Features of Arduino

1. Arduino boards can read analog and digital input signals from different sensors.
2. They convert sensor inputs into outputs such as activating motors and turning LEDs ON/OFF.
3. The board can be programmed using Arduino IDE.
4. It does not require an additional programmer to upload code. A USB cable is sufficient.
5. Arduino IDE uses a simplified version of C++, making programming easier.
6. It provides a standard hardware form factor with easily accessible microcontroller functions.

### Components of Arduino UNO

The important components of an Arduino UNO board are:

| Component            | Function                                                   |
| -------------------- | ---------------------------------------------------------- |
| Power USB            | Supplies power and uploads programs through USB.           |
| Power Barrel Jack    | Connects an external power supply.                         |
| Voltage Regulator    | Controls and stabilizes the voltage supplied to the board. |
| Crystal Oscillator   | Helps Arduino calculate time using a 16 MHz clock.         |
| Reset Button         | Restarts the Arduino program.                              |
| Analog Pins          | Six pins (A0–A5) read analog sensor signals.               |
| Digital I/O Pins     | 14 pins used for digital input and output.                 |
| Main Microcontroller | Acts as the brain of the Arduino board.                    |
| ICSP Pins            | Used for in-circuit serial programming.                    |
| TX and RX LEDs       | Indicate serial data transmission and reception.           |
| AREF                 | Provides an external reference voltage for analog inputs.  |

### Applications of Arduino

- Temperature and humidity monitoring.
- LED and motor control.
- Home automation systems.
- Sensor-based monitoring systems.
- Controlling electronic devices using actuators.

Programming language: Simplified C++ using Arduino IDE.

## 3. Raspberry Pi

[Raspberry Pi 3 Model B | vilros.com                      – Vilros.com](https://images.openai.com/static-rsc-4/pU6H_oNpf86iKV1WaA2cD1IfZOcNkmzz7y09-grgFf8CwicUW1HSWtmva5XyXtNSgPQWmcr7BJzW-7PJXsCaFkJR1rLElOAkOYLXjyTMokJ5qSKN_uih9L9YYEz_5VNDKSvU038YUM_1HnJxLEBFA9K8Ss8tm2iFbeWCBbjwGOo?purpose=inline)

[vilros.com](https://vilros.com/products/raspberry-pi-3-model-b?utm_source=chatgpt.com)

Raspberry Pi is a low-cost, credit-card-sized computer that can be connected to a monitor or television using HDMI and operated with a standard keyboard and mouse.

It is a small computer that enables people of all ages to explore computing.

### Features of Raspberry Pi

1. It is a low-cost, credit-card-sized computer.
2. It can perform almost all the functions of a desktop computer.
3. It supports internet browsing, high-definition video playback, spreadsheets, word processing and games.
4. Programs can be written using Python, C, C++, Java, Scratch and Ruby.
5. It supports different operating systems such as:
   - Raspbian
   - NOOBS
   - Ubuntu Mate
   - Snappy Ubuntu Core
   - Windows 10 Core
   - RISC OS
6. It provides GPIO (General Purpose Input/Output) pins to communicate with external circuits and sensors.

### Architecture of Raspberry Pi

[File:Raspberrypi block function v01.svg - Wikimedia Commons](https://images.openai.com/static-rsc-4/TvLV8ku0PR6JQwU4Tfu14pxWmWLW4cowVKAl7JOarP-_3luK-TvnTBb7Iq_pxvAN5U3voIRpv5EH7YdAKspAUF9Daw7mp71T9yUm6KCxmlRl9ucnb4Uh-6KOI6yiBN0W_PhYfUIPbLdSR65jWAMqnKm14FLXaut0CQ30-8ScL_w?purpose=inline)

[commons.wikimedia.org](https://commons.wikimedia.org/wiki/File%3ARaspberrypi_block_function_v01.svg?utm_source=chatgpt.com)

The basic architecture consists of:

1. CPU/GPU: Performs processing operations and handles graphics.
2. RAM: Stores temporary data and instructions during execution.
3. I/O: Provides input and output communication.
4. USB Hub: Connects USB devices and Ethernet interfaces.
5. Ethernet: Provides network connectivity.
6. USB: Connects external devices such as keyboards and mice.

### GPIO Pin Configuration

- GPIO stands for General Purpose Input/Output.
- These pins provide a physical interface between Raspberry Pi and the external world.
- They communicate with sensors, extension boards and custom circuits.
- A GPIO pin can be configured as HIGH or LOW.
- HIGH represents 3.3V, while LOW represents OFF.
- GPIO pins can receive sensor inputs and control output devices such as LEDs.

### Applications of Raspberry Pi

- Media streaming applications.
- Home automation.
- Robot control.
- Virtual Private Network (VPN).
- Lightweight web servers with IoT.
- Sensor monitoring and data acquisition.

Programming languages: Python, C, C++, Java, Scratch and Ruby.

## 4. NodeMCU

[How to Use NodeMCU: Pinouts, Specs, and Examples | Cirkit Designer](https://images.openai.com/static-rsc-4/mdU-6He1iu-Vr_ru2piZyulOUYcQEUrnT11aqJiV0uPBbGh9cHfT3JSYTncyg8mqdMmXJtKCSAjjhzHELRo_-f9ve_i-Nu9OFmxTWmmxZQ3KdFKWg8VPUdxHZJgNE7Z32J21K6COfrLgBvHViBtzJ37_fRsWk5pxn-IuU2Wo_jc?purpose=inline)

[docs.cirkitdesigner.com](https://docs.cirkitdesigner.com/component/f639d017-85b1-1e05-5b23-88979b09180e/nodemcu?utm_source=chatgpt.com)

NodeMCU is an open-source firmware and development kit based on the ESP8266 System on Chip (SoC). It enables IoT prototyping using Lua scripts or C/C++ programming languages.

### Core Specifications

| Specification       | Details                            |
| ------------------- | ---------------------------------- |
| Input Voltage       | 3.3V DC                            |
| Current Consumption | Approximately 250 mA               |
| RAM                 | 32 KB                              |
| Data RAM            | 80 KB                              |
| Flash Memory        | Approximately 200 KB               |
| Processor           | ESP8266 SoC, 80/160 MHz 32-bit CPU |
| Wi-Fi               | Built-in Wi-Fi (802.11 b/g/n)      |

### Features of NodeMCU

1. It provides built-in Wi-Fi connectivity.
2. It supports multiple programmable I/O pins.
3. It supports GPIO, ADC, PWM, I²C, SPI and UART interfaces.
4. It provides a USB interface for power supply and programming.
5. It is a low-cost and Arduino-compatible development platform.
6. It can work as a Wi-Fi station or access point.
7. It can host a web server to control sensors and I/O devices using HTTP or WebSocket.
8. It can interface with LEDs, motors, servos, sensors and relays.

### Programming and Development Environments

NodeMCU supports the following development environments:

- Lua firmware (default).
- Arduino IDE.
- PlatformIO (VS Code).

### Applications of NodeMCU

1. LED Control: Controls LEDs using a web interface with PWM.
2. Servo Motor Control: Controls servo motor angles through Wi-Fi.
3. Sensor Monitoring: Connects DHT11 temperature and humidity sensors.
4. Home Automation: Controls electronic devices remotely.
5. IoT Applications: Sends sensor information through wireless networks.

## 5. Comparison of Arduino, Raspberry Pi and NodeMCU

The following table compares the three hardware platforms based on their features and applications.

| Features         | Arduino                                    | Raspberry Pi                         | NodeMCU                                               |
| ---------------- | ------------------------------------------ | ------------------------------------ | ----------------------------------------------------- |
| Type             | Microcontroller-based prototyping platform | Single-board computer                | ESP8266-based IoT development board                   |
| Processing       | Microcontroller                            | CPU/GPU                              | 32-bit ESP8266 CPU                                    |
| Connectivity     | USB; external connectivity can be added    | Ethernet and USB                     | Built-in Wi-Fi                                        |
| Programming      | Simplified C++                             | Python, C, C++, Java, etc.           | Lua and C/C++                                         |
| Operating System | No general-purpose OS required             | Supports Raspbian, Ubuntu and others | Uses ESP8266 firmware                                 |
| Memory           | Depends on the Arduino board               | RAM and storage support              | 32 KB RAM, 80 KB data RAM, approximately 200 KB flash |
| GPIO             | Analog and digital I/O                     | GPIO pins                            | GPIO, ADC, PWM, I²C, SPI, UART                        |
| Cost             | Low-cost                                   | Low-cost computer                    | Low-cost                                              |
| Main Purpose     | Sensor interfacing and device control      | General-purpose computing and IoT    | Wi-Fi-based IoT applications                          |

### Applications Comparison

| Arduino                | Raspberry Pi           | NodeMCU                    |
| ---------------------- | ---------------------- | -------------------------- |
| LED control            | Media streaming        | Wi-Fi LED control          |
| Temperature monitoring | Home automation        | Wireless sensor monitoring |
| Motor control          | Robot control          | Servo motor control        |
| Sensor interfacing     | Lightweight web server | Remote device control      |

## 6. Conclusion

Arduino, Raspberry Pi and NodeMCU are important hardware platforms used in IoT applications.

- Arduino is suitable for sensor interfacing and controlling electronic devices.
- Raspberry Pi is suitable for applications requiring computing capabilities, GPIO interfacing and operating systems.
- NodeMCU is suitable for low-cost IoT applications requiring built-in Wi-Fi connectivity.

Therefore, the selection of a hardware platform depends on the application requirements, processing needs, connectivity and cost.

PDF reference: Unit I – Sensors and Hardware for IoT, pages 9–14. The Arduino UNO components are illustrated on pages 9–11, Raspberry Pi architecture and GPIO configuration on pages 11–13, and NodeMCU specifications and applications on pages 13–14.&#x20;

Unit 1.pdf



Exam tip: For 13 marks, draw the Arduino UNO board, Raspberry Pi architecture and NodeMCU board diagrams. Include the comparison table to make your answer complete and easy to evaluate.
