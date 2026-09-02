# Sensors – Characteristics and Classification

## 1. Introduction

A **sensor** is a hardware device used to convert a **physical event or characteristic into an electrical signal** that can be understood by a system.

**Example:** A thermometer senses temperature and converts it into an electrical signal for the system. 

In IoT, sensors are important because they collect information from the physical environment and provide it to the IoT system for processing and decision-making.

---

# 2. Characteristics of Sensors

### 1. Range

The **range** is the minimum and maximum value of a physical variable that a sensor can measure.

**Example:** An RTD can measure temperature from **−200°C to 800°C**. 

### 2. Span

Span is the difference between the maximum and minimum input values.

**Example:**
RTD span = 800 − (−200) = **1000°C**. 

### 3. Accuracy

Accuracy indicates how close the measured value is to the **true value**. It is generally expressed as a percentage of full scale or reading. 

### 4. Precision

Precision indicates the **closeness among a set of measured values**. 

### 5. Linearity

Linearity is the **maximum deviation of the measured sensor output from the ideal curve**. 

### 6. Hysteresis

Hysteresis is the difference in sensor output when the input is varied in **increasing and decreasing directions**. 

### 7. Resolution

Resolution is the **minimum change in input that can be detected** by the sensor. 

### 8. Reproducibility

Reproducibility is the ability of a sensor to produce the **same output when the same input is applied**. 

### 9. Repeatability

Repeatability is the ability of a sensor to produce the **same output under the same physical and measurement conditions**. 

### 10. Response Time

Response time is the time taken by the sensor output to reach a specified percentage, such as **95%**, of its final value after a change in input. 

---

# 3. Classification of Sensors

The PDF classifies sensors in **three ways**:

```text
                     SENSORS
                        │
        ┌───────────────┼────────────────┐
        ↓               ↓                ↓
   Power Requirement   Output          Data Measured
        │               │                │
   ┌────┴────┐      ┌────┴────┐      ┌────┴─────┐
   ↓         ↓      ↓         ↓      ↓          ↓
 Active   Passive  Analog   Digital Scalar    Vector
```

---

## 3.1 Based on Power Requirement

### A. Active Sensors

Active sensors **do not require an external energy source** and directly generate an electrical signal in response to the input.

**Examples:**

* Thermocouple
* Photodiode
* Piezoelectric sensor

### B. Passive Sensors

Passive sensors **require an external power/excitation signal**. They modify this excitation signal to produce the output.

**Example:** Strain gauge. 

---

## 3.2 Based on Output

### A. Analog Sensors

Analog sensors produce a **continuous output signal or voltage** generally proportional to the quantity being measured.

**Examples:**

* Temperature
* Speed
* Pressure
* Displacement
* Strain

A thermometer or thermocouple can continuously respond to changes in temperature. 

### B. Digital Sensors

Digital sensors produce **discrete output values**, generally represented as binary **1 or 0 (ON/OFF)**.

**Example:** A digital sensor can provide an ON/OFF signal when a particular condition is detected. 

---

# 3.3 Based on Type of Data Measured

### A. Scalar Sensors

Scalar sensors produce an output proportional mainly to the **magnitude** of the measured quantity.

**Examples:**

* Temperature
* Colour
* Pressure
* Strain

**Example:** A thermometer measures room temperature irrespective of the sensor's orientation. 

### B. Vector Sensors

Vector sensors provide information about the **magnitude, direction and orientation** of a quantity.

**Examples:**

* Sound
* Image
* Velocity
* Acceleration
* Orientation

**Example:** An accelerometer measures acceleration along the **X, Y and Z axes**. 

---

# 4. Summary Table

| Classification        | Types   | Example                  |
| --------------------- | ------- | ------------------------ |
| **Power requirement** | Active  | Thermocouple             |
|                       | Passive | Strain gauge             |
| **Output**            | Analog  | Thermometer/Thermocouple |
|                       | Digital | Digital ON/OFF sensor    |
| **Data measured**     | Scalar  | Temperature sensor       |
|                       | Vector  | Accelerometer            |

---

## 5. Conclusion

Sensors are the **basic data-collection components of an IoT system**. They convert physical conditions into electrical signals and allow IoT devices to understand their environment. Sensors can be classified based on **power requirement, output and type of data measured**. Their characteristics such as **range, accuracy, precision, resolution, linearity and response time** determine their suitability for a particular IoT application. 
