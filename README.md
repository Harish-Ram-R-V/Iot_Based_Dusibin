# Smart Dustbin with Smart Alarm and IoT Integration

This project involves building a smart dustbin system that uses sensors to monitor:
    Garbage fill level
    Movement near the bin (for automatic lid opening)
    Temperature
    Gas concentration (for detecting foul smells or gas leaks)
It also includes a Smart Alarm System for safety by indicating hazardous temperature or gas levels. In the future, this system will be upgraded with Blynk IoT for real-time mobile app monitoring.

🗑️ Smart Dustbin Functionality:
Components Used:

    Ultrasonic Sensor (for distance measurement)
    PIR Sensor (motion detection)
    Servo Motor (for opening lid)
    LEDs (status indication)
    Buzzer (alert for motion)
    Arduino Uno (microcontroller)

Working Explanation:

    The ultrasonic sensor checks the garbage fill level by measuring the distance from the top of the dustbin to the trash.
    If the distance is greater than 7 cm, the bin is considered not full:
        Green LED (pin 8) turns ON.
        Red LED (pin 11) is OFF.
        If motion is detected by the PIR sensor (pin 4):
            The buzzer is turne OFF briefly.
            The servo motor opens the lid to 90°, allowing the user to deposit garbage.
            Then the servo closes the lid again.
    If the distance is less than or equal to 7 cm, the dustbin is full:
        Red LED turns ON.
        Green LED turns OFF.
        Lid remains closed.

🚨 Smart Alarm System Functionality:
 Components Used
    LM35/Analog Temp Sensor (connected to A1)
    Gas Sensor (connected to A0)
    LED (overheat indicator)
    Buzzer (gas alert)
    Arduino Uno

Working Explanation:
    The system reads temperature from A1 and gas levels from A0.
    If temperature exceeds 80°C:
        LED on pin 13 turns ON to alert overheating.
    If gas levels exceed threshold (100):
        Buzzer on pin 7 is activated to signal foul smell or gas leak.

🔄 Future Improvements & Blynk IoT Integration:
  🔗 Planned Additions:
    
    Connect temperature, gas, and garbage level data to the Blynk IoT app using WiFi (via ESP8266 or NodeMCU).
    Mobile Notifications:
        Real-time notification when the bin is full.
        Alerts when temperature or gas exceeds safe levels.
    Smart Messaging:
        When garbage smell exceeds a threshold, an automated message will be sent to the garbage collection team.
    Data Logging:
        Track bin usage, environmental stats via Blynk dashboards.

📱 Mobile Dashboard Example (via Blynk):
    Gauge Widget for garbage level
    Temperature display
    Gas level display
    Switches or automation rules for alerts

💡 Further Enhancements:
    Add weight sensor to measure garbage weight.
    Include camera module for remote bin condition check.
    Integrate voice control or gesture-based lid opening.
    Solar-powered system for energy efficiency
    
## see my tinkercad circuit simulation here: 
    https://www.tinkercad.com/things/ciTeTpKyNeC-smart-dustbin?sharecode=71OB5XNtMvTUXvO3SESpw54_bzQcyq7cuv4gtJYwEWs
