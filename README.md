
# Facial Recognition System 👤🔐

The Facial Recognition System is a smart security project that simulates real facial scanning using a Raspberry Pi and Arduino. When a known face appears in front of the webcam, the system displays their name, unlocks access using a servo motor, lights up an RGB LED, and plays a success tone through a piezo buzzer. If the face is unknown, the system shows “Unknown” and can trigger a warning response or deny access.

---

## 📦 Components

- Raspberry Pi 4
- USB Webcam
- Arduino Uno (or compatible)
- Breadboard
- Jumper wires
- Servo motor (for access control)
- RGB LED (for status display)
- Piezo buzzer (for audio feedback)
- Resistors (for LED protection)
- USB power cable (for Raspberry Pi and Arduino)
- Software Libraries:
  - `face_recognition` (Python)
  - `opencv-python`
  - `pyserial`

---

## 🔧 Installation & Setup

### Build the hardware:

1. **Connect the Servo Motor**  
   - Signal → Arduino digital pin (e.g., pin 9)  
   - Power → 5V  
   - GND → GND

2. **Wire the RGB LED**  
   - Red, Green, Blue legs → Arduino PWM pins (e.g., 3, 5, 6) with resistors  
   - Common cathode/anode to GND/5V as needed

3. **Piezo Buzzer**  
   - Signal → Arduino digital pin (e.g., pin 8)  
   - GND → GND

4. **USB Webcam**  
   - Connect to Raspberry Pi via USB port

---

## 💡 How It Works

The webcam captures video and checks for faces using face_recognition.

If a match is found in the known faces list:

 - Raspberry Pi sends a signal to the Arduino via serial.
   
   
 - The Arduino moves the servo to "unlock" position.
   
   
 - RGB LED turns green.
   
 
 - Piezo buzzer beeps a success tone.
 
 If no match is found:
   
   
 - Raspberry Pi sends a different signal.
   
  
 - Servo remains locked.
   
  
 - RGB LED turns red or stays off.

   
## 🖼️ Images / Videos

<img width="680" height="621" alt="Screenshot 2025-08-04 at 9 30 42 AM" src="https://github.com/user-attachments/assets/d2577b5e-3a87-43d6-a28f-43e66ccdcd69" />



## 🔗 Simulation Links

-   [Tinkercad Simulation](https://www.tinkercad.com/things/iE3MKtVbNjL/editel)

## 🙌 Credits

Created by: Zahara BG
