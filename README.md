# Smart Light Classifier – ESP32 TinyML

## Project Description

This project demonstrates a complete **Mini Integration Project** using an ESP32 by combining **WiFi, LDR sensor, OLED display, LED control, and on-device TinyML classification**.

The LDR sensor measures the real-time light intensity. A TensorFlow Lite Micro model classifies the reading as **Dark, Normal, or Bright**. Based on the model's prediction, the ESP32 automatically controls an LED and displays the result on an OLED. The classification results are also logged to a web dashboard through WiFi.

## Objective

- Interface an LDR sensor with ESP32.
- Read real-time light intensity values.
- Use TensorFlow Lite Micro for on-device classification.
- Classify light levels as Dark, Normal, or Bright.
- Automatically control an LED based on the prediction.
- Display the sensor value and prediction on an OLED.
- Connect the ESP32 to WiFi.
- Log classification results to a web dashboard.

## Components Required

- ESP32 Development Board
- LDR Sensor
- SSD1306 OLED Display
- LED
- Resistor
- USB Cable
- Arduino IDE
- TensorFlow Lite for Microcontrollers library
- Trained `.tflite` model
- WiFi Network
- Jumper Wires

## Working

```text
LDR Sensor
     ↓
ESP32
     ↓
Read Light Intensity
     ↓
TFLite Micro Model
     ↓
Dark / Normal / Bright
     ↓
   ┌───────────────┐
   ↓               ↓
 OLED Display    LED Control
   ↓
WiFi Connection
     ↓
Web Dashboard
     ↓
Log Sensor & Prediction
```

## Example

The LDR sensor provides a real-time light reading.

```text
LDR Reading: 28
```

The TinyML model classifies the reading.

```text
Predicted Class: Normal
```

The OLED displays the result.

```text
Light: 28
Status: Normal
```

The ESP32 also sends the result through WiFi to the web dashboard.

```text
WiFi: Connected
Status: Normal
Data: Logged
```

## Automatic LED Control

The LED is controlled according to the model prediction.

```text
Dark   → LED ON
Normal → LED OFF
Bright → LED OFF
```

## Technologies Used

- ESP32
- LDR Sensor
- SSD1306 OLED
- LED
- Arduino IDE
- C/C++
- WiFi
- TensorFlow Lite
- TensorFlow Lite for Microcontrollers
- TinyML
- Web Dashboard

## Expected Output

The OLED displays the current light reading and classification.

```text
Smart Light
LDR: 28
Status: Normal
```

The web dashboard displays the logged sensor readings and predicted classes.

```text
LDR Value    Status
---------------------
28           Normal
12           Dark
35           Bright
```

## Result

The **Smart Light Classifier** successfully integrates an LDR sensor, OLED display, LED control, WiFi connectivity, and an on-device TensorFlow Lite Micro model. The system classifies real-time light levels as **Dark, Normal, or Bright**, automatically controls the LED, displays the result on the OLED, and logs the results to a web dashboard.
