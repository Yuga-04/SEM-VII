# Implementation of IoT Using Raspberry Pi – 13 Marks

## 1. Introduction

**Raspberry Pi** is a low-cost, credit-card-sized computer that can be used for IoT applications. It supports programming languages such as **Python, C, C++, Java, Scratch and Ruby** and provides **GPIO pins** for interfacing sensors and actuators. 

In IoT, Raspberry Pi can read data from sensors, process it and control actuators according to the sensor readings. 

---

## 2. Basic IoT Implementation Using Raspberry Pi

```text
       Physical Environment
              ↓
        ┌───────────┐
        │  Sensor   │
        └─────┬─────┘
              ↓
       ┌──────────────┐
       │ Raspberry Pi │
       │  Processing  │
       └──────┬───────┘
              ↓
        ┌───────────┐
        │  Network  │
        └─────┬─────┘
              ↓
       IoT Application
              ↓
        ┌───────────┐
        │ Actuator  │
        └───────────┘
```

### Main steps

1. **Sensor interfacing** – Sensors are connected to Raspberry Pi GPIO pins.
2. **Data acquisition** – Raspberry Pi reads the sensor values.
3. **Processing** – The sensor data is processed using a Python program.
4. **Decision making** – A condition is checked based on the sensor reading.
5. **Actuator control** – Raspberry Pi sends a signal to an actuator.
6. **Network connectivity** – Raspberry Pi can communicate with other devices/services over a network. GPIO allows it to interact with physical devices. 

---

# 3. Case Study: Temperature Dependent Automatic Cooling System

The PDF presents a **Temperature Dependent Auto Cooling System** using Raspberry Pi.

### Components Required

* Raspberry Pi
* DHT Sensor
* 4.7 KΩ resistor
* Relay
* Jumper wires
* Mini fan
* Li-Po battery 

---

## 4. Working of the System

```text
          Temperature
              ↓
        ┌──────────┐
        │ DHT Sensor│
        └────┬─────┘
             ↓
        Raspberry Pi
             ↓
     Temperature > 30°C?
          ↙          ↘
        YES           NO
         ↓             ↓
     Relay ON       Fan OFF
         ↓
      Fan ON
```

The **DHT sensor measures temperature**. When the temperature becomes greater than **30°C**, Raspberry Pi activates the relay, which turns ON the fan. 

---

## 5. DHT Sensor Connection

The DHT sensor has four pins:

| Pin   | Function             |
| ----- | -------------------- |
| Pin 1 | 3.3V–5V power supply |
| Pin 2 | Data                 |
| Pin 3 | Null                 |
| Pin 4 | Ground               |

The PDF connects:

* DHT **Pin 1 → 3.3V** of Raspberry Pi
* DHT **Pin 2 → GPIO Pin 11**
* DHT **Pin 4 → Ground** 

---

## 6. Relay Connection

A relay is an **electromechanical switch** with three terminals:

* **NO – Normally Open**
* **Common**
* **NC – Normally Closed** 

Connections:

* Relay **VCC → 5V** of Raspberry Pi
* Relay **GND → Ground**
* Relay **Signal → GPIO Pin 7** 

---

## 7. Fan Connection

The fan is connected to a Li-Po battery through the relay.

* **NO terminal → positive terminal of fan**
* **Common terminal → positive terminal of battery**
* **Negative terminal of battery → negative terminal of fan** 

Thus, when Raspberry Pi activates the relay, the circuit is completed and the **fan turns ON**.

---

## 8. Software Implementation

The PDF uses the **Adafruit Python DHT library** for working with the DHT22 sensor.

Installation:

```text
git clone https://github.com/adafruit/Adafruit_Python_DHT.git
cd Adafruit_Python_DHT
sudo python setup.py install
```

The Python program reads the temperature from the DHT22 and controls the relay/fan based on the temperature condition. 

---

## 9. Advantages

* Automatic temperature monitoring.
* Automatic control of the cooling fan.
* Reduces the need for manual operation.
* Demonstrates sensor-to-actuator IoT implementation.
* Raspberry Pi can also provide network connectivity and remote control of connected devices. 

## 10. Conclusion

Raspberry Pi provides an effective platform for implementing IoT applications. In the **automatic cooling system**, the **DHT sensor senses temperature → Raspberry Pi processes the reading → relay is controlled → fan is switched ON when temperature exceeds 30°C**. This demonstrates how Raspberry Pi integrates **sensors, processing, networking and actuators** to create a practical IoT system.
