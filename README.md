# Hand Gesture Controlled RC Car 🚗✋

Control your RC car with hand gestures using ESP32, MPU6050, and L298N motor driver!

## ✨ Features
- Wireless ESP-NOW communication
- Intuitive hand gesture control
- Low latency response (50ms)
- Auto-calibrating MPU6050

## 🔧 Hardware Required

### Transmitter (Controller):
- ESP32 Dev Board
- MPU6050 Accelerometer
- Breadboard & jumper wires
- Power source (USB/Battery)

### Receiver (Car):
- ESP32 Dev Board
- L298N Motor Driver
- 2-4 DC Motors
- Robot chassis
- Motor battery (6-12V)
- Jumper wires

## 📚 Libraries Required

Install via Arduino IDE Library Manager:

1. **ESP32 Board Support** (v2.0.0+)
   - Add to Board Manager URLs:
```
https://dl.espressif.com/dl/package_esp32_index.json
```

2. **MPU6050_light** by rfetick (v1.1.0+)
   - Search "MPU6050_light" in Library Manager

## 🚀 Quick Start

### Step 1: Find Receiver MAC Address
```bash
1. Upload mac_address_finder/mac_address_finder.ino to receiver ESP32
2. Open Serial Monitor (115200 baud)
3. Copy the MAC address shown
```

### Step 2: Update Transmitter Code

### Step 3: Wire Connections

**Transmitter (MPU6050 to ESP32):**
| MPU6050 | ESP32 |
|---------|-------|
| VCC | 3.3V    |
| GND | GND     |
| SCL | GPIO 22 |
| SDA | GPIO 21 |

**Receiver (L298N to ESP32):**
| L298N | ESP32   |
|-------|---------|
| IN1   | GPIO 5  |
| IN2   | GPIO 18 |
| IN3   | GPIO 19 |
| IN4   | GPIO 21 |
| GND   | GND     |

Supply vcc to +12V of L298N
Supplu Gnd to Gnd of L298N

Esp32 Vin to +5v of L298N
Esp32 Gnd to Gnd of L298N

Left side motor vcc to OUT4
Left side motor Gnd to OUT3
Right side motor vcc to OUT2
Right side motor Gnd to OUT1

### Step 4: Upload Code


