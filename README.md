# **Smart Irrigation System**

## **Overview**
The Smart Irrigation System is a connected device designed to automate and monitor the watering of plants. It uses a solenoid valve, temperature and moisture sensors, and an ESP32 microcontroller with wireless communication to enable remote and local control. The system features:
- **Automated Watering**: Based on soil moisture and user-defined schedules.
- **Remote Control**: Access the system via a mobile app or web interface.
- **Data Logging**: Store and analyze temperature, moisture levels, and watering schedules.

---

## **Features**
- Soil moisture monitoring with capacitive sensors.
- Wireless control of a solenoid valve using an ESP32 microcontroller.
- Local and cloud-based communication using protocols like MQTT and HTTP.
- User interface for real-time control and data visualization.
- Alerts and notifications for low moisture levels or errors.
- Expandable architecture for integrating additional sensors or smart home systems.

---

## **Components**
### **Hardware**
- **Soil Moisture Sensor**: Soil Moisture Sensor (I used AZDelivery Soil Moisture Sensor Hygrometer Module V1.2).
- **Valve**: 12V Solenoid Valve (I used GREDIA 1/4" DC 12V Solenoid Valve (Normally Closed)).
- **Microcontroller**: ESP32 Relay Board (ESP32-WROOM).
- **Power Supply**: DC 12V wall adapter (with potential battery support in the future).

### **Software**
- **Programming Language**: C/C++ for ESP32 firmware.
- **Communication Protocols**: MQTT, HTTP, or Matter (TBD).
- **Database**: SQLite (local) with potential for cloud-based storage.
- **User Interface**: Web and mobile apps for control and data display.

---

## **Architecture**
This project features a hybrid architecture with both local and cloud-based components:
1. **Local Control**: Direct communication between ESP32 and local devices.
2. **Cloud Connectivity**: Integration with a cloud service for remote access and data storage.
3. **Automation Logic**:
   - Soil moisture below threshold: Open the valve.
   - Scheduled watering: Automatically trigger at specific times.
   - External conditions (e.g., rain): Adjust watering schedule dynamically.

---

## **Setup Instructions**
### **Hardware Assembly**
1. Connect the soil moisture sensor to the ESP32's analog input pin.
2. Connect the solenoid valve to the relay module, ensuring proper power supply connections.
3. Power the ESP32 and test connections using a multimeter.

### **Firmware Setup**
1. Install the Arduino IDE or ESP-IDF for programming the ESP32.
2. Clone this repository and upload the initial test firmware to the ESP32.
3. Verify sensor and valve functionality using the serial monitor.

---

## **Milestones**
1. **Sensor Integration**: Test and calibrate the soil moisture sensor.
2. **Valve Control**: Implement control logic for the solenoid valve.
3. **Wireless Communication**:
   - Set up MQTT for local communication.
   - Integrate with a cloud-based service.
4. **Database**: Design a schema for storing sensor data and user settings.
5. **User Interface**:
   - Build a basic web app.
   - Develop a mobile-friendly interface.
6. **Testing and Validation**: Create automated test cases and perform real-world testing.

---

## **Future Plans**
- **Battery Power**: Transition to battery-powered operation for portability.
- **Integration**: Add support for smart home ecosystems using Matter or HomeKit.
- **Scalability**: Expand the system to support multiple zones and plants.
- **Advanced Features**: Use weather API data to adjust watering dynamically.

---

## **License**
This project is licensed under the MIT License. See `LICENSE` for details.
