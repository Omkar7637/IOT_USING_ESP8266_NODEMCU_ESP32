# IOT_USING_ESP8266_NODEMCU_ESP32

### **Day 1: Introduction to IoT and Arduino IDE**

**Theory:**
- What is IoT?
  - IoT applications in daily life: Smart homes, wearables, industrial IoT, etc.
  - Overview of IoT architecture (Devices, Communication, Data, Cloud, and Users).
- Arduino IDE Introduction:
  - Setting up the Arduino IDE for ESP8266 and ESP32.
  - Differences between ESP8266, ESP32, and Arduino boards.

**Practical:**
- Setting up Arduino IDE on the computer.
- Installing the ESP8266 and ESP32 board definitions in Arduino IDE.
- Writing and uploading a simple "Hello World" program (Blink LED).

---

### **Day 2: Understanding NodeMCU (ESP8266) and Basic Programming**

**Theory:**
- Introduction to ESP8266 NodeMCU:
  - Features of the ESP8266 (Wi-Fi capabilities, GPIO pins, ADC, etc.).
  - ESP8266 pinout and usage.
- Basic syntax of Arduino programming: Setup() and Loop() functions.

**Practical:**
- Blinking an LED using GPIO pins on NodeMCU.
- Understanding the LED pinout and how to control it.

---

### **Day 3: Digital Input and Output on NodeMCU**

**Theory:**
- GPIO pins and their roles in the ESP8266.
- Reading digital input (Button, Switch).
- Digital output (LED, Buzzer).

**Practical:**
- Controlling an LED with a button press (Digital input and output).
- Debugging using serial monitor.

---

### **Day 4: Introduction to ESP32 and Differences with ESP8266**

**Theory:**
- Key features of ESP32 (Dual-core, Bluetooth, more GPIOs, etc.).
- Difference between ESP8266 and ESP32.
- Advantages of using ESP32 for more complex applications.

**Practical:**
- Setup of the ESP32 in Arduino IDE.
- Writing a "Hello World" program with ESP32.
- Basic LED blink on ESP32.

---

### **Day 5: Analog Input and Output (ADC/DAC)**

**Theory:**
- Introduction to ADC (Analog to Digital Conversion).
- Working with analog signals in IoT.
- ESP32 supports DAC (Digital to Analog Conversion).

**Practical:**
- Reading analog input from a potentiometer.
- Controlling the brightness of an LED using PWM (Pulse Width Modulation).
- Sending analog data over Wi-Fi to a server (basic example).

---

### **Day 6: Communication Protocols: Serial, SPI, and I2C**

**Theory:**
- Overview of Serial, SPI, and I2C protocols.
- Differences between these protocols.
- When to use each protocol in IoT projects.

**Practical:**
- Serial communication with ESP8266/ESP32.
- Connecting an I2C LCD with ESP32 and displaying data.
- Interfacing a sensor (e.g., temperature sensor) using I2C.

---

### **Day 7: Wi-Fi Configuration and Connecting to the Internet**

**Theory:**
- How Wi-Fi works.
- Setting up Wi-Fi credentials in ESP8266 and ESP32.
- Connecting to Wi-Fi in the Arduino IDE.

**Practical:**
- Connecting NodeMCU/ESP32 to a Wi-Fi network.
- Testing connectivity with a simple HTTP request.

---

### **Day 8: Using HTTP Protocol to Connect to a Web Server**

**Theory:**
- Overview of HTTP protocol.
- Sending HTTP requests from ESP8266/ESP32 to a web server.
- RESTful APIs and JSON format.

**Practical:**
- Sending GET/POST requests from ESP8266/ESP32 to a simple server.
- Parsing JSON data in Arduino.

---

### **Day 9: IoT Cloud Platforms (ThingSpeak) Introduction**

**Theory:**
- Introduction to IoT cloud platforms: Why are they necessary?
- Overview of ThingSpeak, a popular IoT platform.
- Creating an account and setting up a channel.

**Practical:**
- Sending sensor data (e.g., temperature, humidity) from ESP8266/ESP32 to ThingSpeak.
- Visualizing the data on ThingSpeak.

---

### **Day 10: Interfacing Sensors with NodeMCU and ESP32**

**Theory:**
- Overview of common IoT sensors: Temperature, humidity, motion, gas sensors, etc.
- Understanding sensor calibration and interfacing.

**Practical:**
- Interfacing a DHT11/DHT22 temperature and humidity sensor with ESP8266/ESP32.
- Sending sensor data to the ThingSpeak cloud platform.

---

### **Day 11: Controlling Devices Remotely via Web (Web Server)**

**Theory:**
- Introduction to web servers.
- How IoT devices can act as a server and communicate via HTTP requests.

**Practical:**
- Creating a simple web server on ESP8266/ESP32 to control an LED.
- Accessing the web server through a browser or mobile app.

---

### **Day 12: Bluetooth Communication with ESP32 (Optional)**

**Theory:**
- Introduction to Bluetooth Low Energy (BLE) with ESP32.
- Use cases for Bluetooth in IoT applications.

**Practical:**
- Controlling an LED using Bluetooth with ESP32.
- Sending and receiving data via Bluetooth between ESP32 and a mobile phone.

---

### **Day 13: Automation with IoT (MQTT Protocol)**

**Theory:**
- Introduction to MQTT protocol: Why it's lightweight and suitable for IoT.
- Basic concepts of MQTT brokers, topics, and subscribers.

**Practical:**
- Setting up an MQTT broker (e.g., Eclipse Mosquitto).
- Sending and receiving messages between ESP8266/ESP32 and an MQTT broker.

---

### **Day 14: Final Project and Review**

**Theory:**
- Recap of all the key concepts covered.
- How to plan, design, and implement an IoT project.

**Practical:**
- Final mini-project: Using ESP8266/ESP32 to collect data from a sensor and control an actuator (LED or relay) based on data or user input.
- Overview of scaling IoT solutions and integrating more complex systems.

---
### **Day 1: Introduction to IoT and Arduino IDE**

---

### **Theory:**

#### **What is IoT?**
The **Internet of Things (IoT)** refers to a network of physical objects, devices, or things that are embedded with sensors, software, and other technologies to connect and exchange data with other devices or systems over the internet or local networks. These devices can range from simple sensors to complex systems that interact with the real world.

**Key aspects of IoT:**
- **Connectivity**: IoT devices are connected to the internet or other devices to share and receive data.
- **Automation and Control**: IoT devices can be controlled remotely or autonomously based on programmed logic.
- **Data Collection and Analysis**: IoT devices collect data from the environment and send it to cloud servers or local systems for analysis.

#### **IoT Applications in Daily Life:**
1. **Smart Homes:**
   - **Smart Thermostats (e.g., Nest)**: These adjust the temperature of a house based on user preferences or environmental conditions.
   - **Smart Lights**: Control lighting remotely via smartphone or based on motion.
   - **Security Systems**: Cameras and sensors that monitor your home and send alerts to your phone.
   
2. **Wearables:**
   - **Fitness Trackers (e.g., Fitbit, Apple Watch)**: These monitor health data, such as steps walked, heart rate, calories burned, and even sleep patterns.
   - **Smartwatches**: Wearables that can receive notifications, track health data, and interact with your smartphone.

3. **Industrial IoT (IIoT):**
   - **Predictive Maintenance**: Using sensors on industrial machinery to predict when a part might fail, reducing downtime.
   - **Smart Factories**: IoT devices monitor production lines in real-time, enabling optimization of processes, reducing waste, and ensuring quality.
   - **Supply Chain Monitoring**: IoT sensors track products in transit, ensuring they are handled properly and arrive on time.

#### **Overview of IoT Architecture:**

1. **Devices**:
   - These are the **things** in IoT: sensors, actuators, or any device capable of collecting data or acting on data. For example, temperature sensors, cameras, motors, lights, etc.

2. **Communication**:
   - Communication refers to how IoT devices send and receive data. It can happen through various protocols like **Wi-Fi**, **Bluetooth**, **Zigbee**, **LoRa**, **NB-IoT**, etc.

3. **Data**:
   - The data generated by IoT devices can be anything from temperature readings to the status of a machine. This data needs to be stored, processed, and analyzed to provide valuable insights.

4. **Cloud**:
   - Cloud computing is crucial for IoT systems as it provides the **scalability** to store large amounts of data generated by IoT devices and the **processing power** to analyze the data. Platforms like **ThingSpeak**, **AWS IoT**, **Google Cloud IoT** are commonly used to manage IoT devices.

5. **Users**:
   - IoT systems often include human users who interact with the system through a **user interface** (web or mobile application). The users may configure devices, check the data, or make decisions based on the information provided by the IoT system.

---

### **Arduino IDE Introduction:**

#### **Setting up the Arduino IDE for ESP8266 and ESP32:**
The **Arduino IDE** is a popular open-source environment for writing and uploading code to various embedded devices, including ESP8266 and ESP32. It simplifies the process of programming microcontrollers for IoT projects.

**Steps to set up the Arduino IDE for ESP8266/ESP32:**

1. **Download and Install the Arduino IDE**:
   - If you don’t already have it, download the Arduino IDE from [here](https://www.arduino.cc/en/software) and install it on your system.

2. **Add ESP8266 and ESP32 Board Manager URLs**:
   - To program the ESP8266 or ESP32, you need to add the board manager URLs in the IDE:
     - Go to **File > Preferences**.
     - In the **Additional Boards Manager URLs** field, add the following URLs:
       - For ESP8266: `http://arduino.esp8266.com/stable/package_esp8266com_index.json`
       - For ESP32: `https://dl.espressif.com/dl/package_esp32_index.json`

3. **Install the Board Definitions**:
   - Go to **Tools > Board > Board Manager**.
   - Search for **ESP8266** or **ESP32** and click **Install** to add the necessary board definitions.

4. **Select the Correct Board and Port**:
   - Go to **Tools > Board** and select **ESP8266** (NodeMCU) or **ESP32**.
   - Go to **Tools > Port** and choose the correct port to which your board is connected.

#### **Differences Between ESP8266, ESP32, and Arduino Boards:**
- **ESP8266**:
  - Single-core processor.
  - Built-in Wi-Fi module.
  - Limited GPIO pins (12-17 pins, depending on the board).
  - Lacks Bluetooth functionality.
  - Suitable for basic IoT applications where Wi-Fi connectivity is needed.

- **ESP32**:
  - Dual-core processor, providing better performance.
  - Built-in Wi-Fi and Bluetooth (both Classic and BLE).
  - More GPIO pins (34 pins).
  - More advanced features like DAC, touch sensing, and better power management.
  - Suitable for more complex IoT applications requiring Wi-Fi, Bluetooth, or additional peripherals.

- **Arduino Boards (e.g., Arduino Uno)**:
  - Primarily used for simpler applications or learning programming.
  - Limited connectivity options (no Wi-Fi, Bluetooth, etc.).
  - More GPIO pins, but lacks the advanced features of ESP32 or ESP8266.
  - Better suited for standalone applications or interfacing with external shields (e.g., Ethernet shields).

---

### **Practical:**

#### **1. Setting up Arduino IDE on the Computer:**
- **Download and Install Arduino IDE** from the official website (https://www.arduino.cc/en/software).
- **Install USB drivers** if required for your ESP8266/ESP32 device to communicate with your PC.

#### **2. Installing the ESP8266 and ESP32 Board Definitions:**
- Open **Arduino IDE** and follow the steps above to add board manager URLs.
- Install the necessary definitions for **ESP8266** and **ESP32** boards.
- Select the correct board and port in the **Tools** menu.

#### **3. Writing and Uploading a Simple "Hello World" Program (Blink LED):**

The "Hello World" program for hardware usually involves blinking an LED. This program is a good starting point for understanding the basic workflow of Arduino programming.

**Code:**
```cpp
void setup() {
  // Initialize the digital pin as an output.
  pinMode(LED_BUILTIN, OUTPUT);  // Built-in LED for NodeMCU/ESP32
}

void loop() {
  digitalWrite(LED_BUILTIN, HIGH);   // Turn the LED on
  delay(1000);                       // Wait for 1 second
  digitalWrite(LED_BUILTIN, LOW);    // Turn the LED off
  delay(1000);                       // Wait for 1 second
}
```

- **Explanation:**
  - `setup()` is executed once when the program starts. Here, we initialize the pin connected to the LED as an output pin.
  - `loop()` continuously runs, turning the LED on and off with a delay of 1 second (1000 milliseconds).

**Upload the Program:**
- After writing the program, click on the **Upload** button (right arrow) in the IDE to upload the code to your ESP8266/ESP32 board.
- Observe the **LED blinking** on your board, indicating that the program is running successfully.

---

### **Day 2: Understanding NodeMCU (ESP8266) and Basic Programming**

---

### **Theory:**

#### **Introduction to ESP8266 NodeMCU:**
The **NodeMCU** is a low-cost development board based on the **ESP8266** Wi-Fi module, commonly used in IoT applications due to its compact size and Wi-Fi capabilities. It allows you to connect to Wi-Fi networks and can control devices remotely.

**Key Features of the ESP8266 (NodeMCU):**
1. **Wi-Fi Capabilities**:
   - **Wi-Fi 802.11 b/g/n**: Allows ESP8266 to connect to Wi-Fi networks.
   - Can operate in **Station Mode** (client) or **Access Point Mode** (server), enabling both connecting to a Wi-Fi network and creating a network.

2. **GPIO Pins**:
   - ESP8266 has **17 GPIO pins**, but not all are usable for input/output functions. Some pins are shared with other functions, like the internal flash memory.
   - Commonly used pins for general purposes include **GPIO0, GPIO2, GPIO5**, etc.

3. **Analog-to-Digital Converter (ADC)**:
   - ESP8266 features a **10-bit ADC** which can measure voltage between **0V and 1V**. The ADC pin (usually **A0**) can be used to read analog values, which are typically used for sensors.

4. **Onboard Flash Memory**:
   - Most NodeMCU boards come with **4MB of flash memory** which is used for storing the firmware and user programs.

5. **Low Power Consumption**:
   - The ESP8266 is energy-efficient, with several power-saving modes, making it ideal for battery-operated IoT applications.

6. **Serial Communication**:
   - The ESP8266 supports **UART**, which allows communication with other devices like sensors or other microcontrollers.

#### **ESP8266 Pinout and Usage:**
- **NodeMCU Pinout** includes the following:
  - **GPIO0, GPIO1 (TX), GPIO2 (RX)**, GPIO3 to GPIO16.
  - **A0 (ADC Pin)**: Can be used to read analog signals (0 to 1V).
  - **VCC (3.3V)** and **GND (Ground)** are used for power supply and grounding.
  - **RST (Reset)**: Used to reset the board.
  - **EN (Enable)**: Used to enable the chip.
  
**Pinout Overview:**
- **GPIO Pins**: Configurable as inputs/outputs, used for controlling LEDs, motors, or reading sensors.
- **ADC Pin**: Only one analog input pin is available.
- **UART Pins (TX/RX)**: Used for serial communication.
- **D Pins (Digital)**: Usually mapped to GPIO pins, but they are often referred to by numbers like **D0, D1, etc.**.

**Important Notes on Pin Usage**:
- **GPIO0** and **GPIO2** are involved in boot mode selection. These pins should generally not be used as outputs during boot-up.
- Some pins are **pull-up** or **pull-down** by default, and their behavior can be different based on the board configuration.

---

#### **Basic Syntax of Arduino Programming:**

In **Arduino programming**, the syntax is simple, with two main functions: **`setup()`** and **`loop()`**.

1. **`setup()` Function**:
   - This function is executed once at the beginning of the program.
   - It is used for initializing variables, pin modes, starting serial communication, etc.
   - Example: Setting a pin to output mode for controlling an LED.
   
   **Example:**
   ```cpp
   void setup() {
     pinMode(LED_BUILTIN, OUTPUT);  // Initialize the built-in LED as an output
   }
   ```

2. **`loop()` Function**:
   - This function is executed repeatedly after the `setup()` function finishes.
   - The `loop()` function runs continuously, enabling real-time control and interaction with hardware.
   - Example: Blinking an LED by switching it on and off with a delay.
   
   **Example:**
   ```cpp
   void loop() {
     digitalWrite(LED_BUILTIN, HIGH);   // Turn the LED on
     delay(1000);                       // Wait for 1 second
     digitalWrite(LED_BUILTIN, LOW);    // Turn the LED off
     delay(1000);                       // Wait for 1 second
   }
   ```

---

### **Practical:**

#### **1. Blinking an LED Using GPIO Pins on NodeMCU:**

**Objective:** Control an LED using one of the GPIO pins on the NodeMCU board (ESP8266).

**Required Materials:**
- **NodeMCU ESP8266 board**
- **LED**
- **220Ω Resistor**
- **Breadboard and Jumper wires**

**Steps:**
1. **Connect the LED to the NodeMCU:**
   - **Anode (long leg)** of the LED to the **GPIO pin** (e.g., GPIO2).
   - **Cathode (short leg)** of the LED to the **ground** through a **220Ω resistor**.

2. **Write the Code:**
   Use the following simple Arduino code to blink the LED. This code will turn the LED on for 1 second and off for 1 second, repeatedly.

   ```cpp
   void setup() {
     // Initialize GPIO2 as output for controlling LED
     pinMode(D2, OUTPUT);  // D2 maps to GPIO4 on NodeMCU
   }

   void loop() {
     // Turn LED on
     digitalWrite(D2, HIGH);
     delay(1000);  // Wait for 1 second
     
     // Turn LED off
     digitalWrite(D2, LOW);
     delay(1000);  // Wait for 1 second
   }
   ```

   **Explanation:**
   - `pinMode(D2, OUTPUT);`: Configures pin D2 as an output to control the LED.
   - `digitalWrite(D2, HIGH);`: Turns the LED on by applying HIGH voltage to GPIO2.
   - `digitalWrite(D2, LOW);`: Turns the LED off by applying LOW voltage to GPIO2.
   - `delay(1000);`: Pauses for 1000 milliseconds (1 second).

3. **Upload the Code:**
   - Connect your NodeMCU to the computer via a USB cable.
   - Select the correct **Board** (`NodeMCU 1.0`) and **Port** in the Arduino IDE.
   - Click the **Upload** button to upload the code to the NodeMCU.

4. **Observe the LED:**
   - Once the code is uploaded successfully, you should see the LED blinking on the NodeMCU board.

#### **2. Understanding the LED Pinout and How to Control It:**

- The NodeMCU board has a **built-in LED** connected to **GPIO2** (D4 pin on the board).
- If you prefer to use this built-in LED instead of connecting an external one, you can modify the code as follows:

   ```cpp
   void setup() {
     pinMode(LED_BUILTIN, OUTPUT);  // Initialize the built-in LED as an output
   }

   void loop() {
     digitalWrite(LED_BUILTIN, HIGH);  // Turn the LED on
     delay(1000);  // Wait for 1 second
     digitalWrite(LED_BUILTIN, LOW);   // Turn the LED off
     delay(1000);  // Wait for 1 second
   }
   ```

- In this code, `LED_BUILTIN` is a predefined constant in Arduino that corresponds to the pin connected to the built-in LED on the NodeMCU.

---

### **Day 3: Digital Input and Output on NodeMCU**

---

### **Theory:**

#### **GPIO Pins and Their Roles in the ESP8266:**
The **GPIO pins** on the ESP8266 (NodeMCU) are versatile and can be used for both **digital input** and **digital output**. These pins are typically used for connecting various peripherals like LEDs, sensors, and switches to interact with the board.

- **Digital Input**: Allows the board to receive data from external devices. For example, you can connect a button or a switch to the GPIO pins to detect whether the button is pressed or not.
  
- **Digital Output**: Allows the board to control external devices like LEDs, buzzers, motors, etc. You can send HIGH (1) or LOW (0) signals to these devices to turn them on or off.

#### **Reading Digital Input:**
To read digital input, we use the `digitalRead()` function. It allows you to check whether a pin is receiving a **HIGH** (1) or **LOW** (0) signal.
- **HIGH** means the pin is receiving **3.3V** (for ESP8266).
- **LOW** means the pin is receiving **0V** (ground).

**Digital Input Devices**:
- **Button**: When the button is pressed, it creates a connection between the input pin and ground, which is read as LOW.
- **Switch**: Similar to buttons, switches can also be used to toggle between HIGH and LOW states.

#### **Digital Output:**
To control external devices like LEDs, buzzers, or relays, the **digitalWrite()** function is used. It sends a HIGH (1) or LOW (0) signal to a pin.
- **LEDs**: When a pin is set to HIGH, the LED turns on, and when it is set to LOW, the LED turns off.
- **Buzzers**: Similar to LEDs, when the pin is set to HIGH, the buzzer sounds.

**Digital Output Devices**:
- **LED**: Commonly used for indicators and status displays.
- **Buzzer**: Used for generating sound (usually for alarms or notifications).

#### **Pull-up and Pull-down Resistors:**
- **Pull-up Resistor**: Keeps the input pin HIGH when no external connection is made. This is usually used in buttons or switches to avoid floating pins.
- **Pull-down Resistor**: Keeps the input pin LOW when no external connection is made.

In the **NodeMCU (ESP8266)**, you can activate the internal pull-up or pull-down resistors in software to simplify circuit design.

---

### **Practical:**

#### **1. Controlling an LED with a Button Press (Digital Input and Output):**

**Objective:** Read the state of a button (digital input) and control an LED (digital output) based on whether the button is pressed or not.

**Required Materials:**
- **NodeMCU ESP8266 board**
- **LED**
- **220Ω Resistor**
- **Pushbutton**
- **10kΩ Resistor** (for pull-down)
- **Breadboard and Jumper wires**

**Steps:**
1. **Button Circuit:**
   - Connect the **button** to a GPIO pin (e.g., GPIO5 or D1 pin) on the NodeMCU.
   - Connect the other side of the button to **ground**.
   - Add a **10kΩ pull-down resistor** between the GPIO pin and ground. This ensures that the GPIO pin reads **LOW** when the button is not pressed.

2. **LED Circuit:**
   - Connect the **LED** to another GPIO pin (e.g., GPIO2 or D4 pin) on the NodeMCU.
   - Connect the other side of the LED to **ground** via a **220Ω resistor**.

3. **Write the Code:**
   The code will check the button state and turn the LED on or off accordingly. Here’s an example:

   ```cpp
   const int buttonPin = D1;      // Pin connected to the button
   const int ledPin = D4;         // Pin connected to the LED

   void setup() {
     pinMode(buttonPin, INPUT_PULLUP);  // Set buttonPin as input with internal pull-up resistor
     pinMode(ledPin, OUTPUT);           // Set ledPin as output
     Serial.begin(9600);                // Start serial communication for debugging
   }

   void loop() {
     int buttonState = digitalRead(buttonPin);  // Read the button state
     
     // Debugging: print the button state to the Serial Monitor
     Serial.println(buttonState);

     // If button is pressed (LOW), turn the LED on
     if (buttonState == LOW) {
       digitalWrite(ledPin, HIGH);   // Turn LED on
     } else {
       digitalWrite(ledPin, LOW);    // Turn LED off
     }
     delay(50);  // Small delay to debounce button press
   }
   ```

**Explanation of Code**:
- **`pinMode(buttonPin, INPUT_PULLUP)`**: Configures the button pin as an input with the internal pull-up resistor enabled. This ensures that the pin is **HIGH** when the button is not pressed and **LOW** when it is pressed.
- **`digitalRead(buttonPin)`**: Reads the button state. If pressed, it reads LOW; otherwise, it reads HIGH.
- **`digitalWrite(ledPin, HIGH)`**: Turns the LED on when the button is pressed.
- **`digitalWrite(ledPin, LOW)`**: Turns the LED off when the button is not pressed.

4. **Upload the Code:**
   - Select the correct **Board** (NodeMCU 1.0) and **Port** in the Arduino IDE.
   - Click the **Upload** button to upload the code to the NodeMCU.

5. **Test the Circuit:**
   - When you press the button, the LED should turn on.
   - When you release the button, the LED should turn off.
   - Open the **Serial Monitor** to see the real-time button state (HIGH or LOW).

---

#### **2. Debugging Using Serial Monitor:**

The **Serial Monitor** is a great tool for debugging your code. You can use it to print out values from your program, which is especially helpful when dealing with inputs and outputs.

1. **Using Serial Monitor**:
   - In the example code above, we used `Serial.println(buttonState);` to print the button state to the Serial Monitor.
   - This will display the current state of the button (0 for pressed, 1 for not pressed) in the Serial Monitor.

2. **Steps for Debugging**:
   - Ensure that **Serial.begin(9600)** is included in the `setup()` function.
   - Use `Serial.print()` or `Serial.println()` to display variables or states at various points in the program.
   - Open the **Serial Monitor** in Arduino IDE (Tools > Serial Monitor) to observe the printed output.
  
---

### **Conclusion:**

- Understand how to use **digital input** and **digital output** on the NodeMCU board.
- Control external devices like LEDs and read button presses using **GPIO pins**.
- Implement basic **debouncing** and **serial debugging** to check and troubleshoot their code.

### **Day 4: Introduction to ESP32 and Differences with ESP8266**

---

### **Theory:**

#### **Key Features of ESP32:**
The **ESP32** is a more advanced and powerful microcontroller compared to the **ESP8266**. Below are its key features:

- **Dual-Core Processor**: The ESP32 features a **dual-core processor** (up to **240 MHz**) while the ESP8266 has a **single-core** processor (up to **80 MHz**). This makes the ESP32 more efficient for running multiple tasks simultaneously.
  
- **Bluetooth Capabilities**: The ESP32 supports both **Bluetooth Classic** and **Bluetooth Low Energy (BLE)**. This is an important feature when building IoT devices that need to communicate with mobile devices, wearables, or other Bluetooth-enabled devices.

- **More GPIO Pins**: The ESP32 has **34 GPIO pins** (compared to ESP8266's 17 GPIO pins), which provide more flexibility when connecting peripherals, sensors, and actuators.

- **Higher Clock Speed**: The ESP32 runs at a maximum clock speed of **240 MHz**, providing better performance for demanding applications.

- **Analog-to-Digital Converter (ADC)**: The ESP32 has **12-bit ADCs** (in contrast to the ESP8266’s 10-bit ADCs) that provide higher resolution for analog readings, which is useful for more precise sensors.

- **Wi-Fi and Ethernet Support**: Like the ESP8266, the ESP32 also has **Wi-Fi capabilities** but can also support **Ethernet** connections, adding more flexibility for various networking setups.

- **PWM, DACs, and More**: The ESP32 includes additional features like **PWM outputs**, **DACs** (Digital to Analog Converters), **I2S interfaces**, and **hardware acceleration** for cryptographic operations.

#### **Difference Between ESP8266 and ESP32:**
| Feature                   | **ESP8266**                    | **ESP32**                          |
|---------------------------|---------------------------------|-------------------------------------|
| **Processor**              | Single-core, 80 MHz             | Dual-core, 240 MHz                  |
| **Wi-Fi**                  | Yes                             | Yes                                 |
| **Bluetooth**              | No                              | Yes (Classic and BLE)               |
| **GPIO Pins**              | 17 GPIO pins                    | 34 GPIO pins                        |
| **Analog Inputs**          | 1 ADC, 10-bit resolution        | 12-bit ADC, multiple channels       |
| **DAC**                    | No                              | Yes (2 channels)                    |
| **PWM**                    | Yes                             | Yes (more advanced PWM control)     |
| **PWM Resolution**         | 8-bit                           | 12-bit                              |
| **Clock Speed**            | 80 MHz                          | 240 MHz                             |
| **Ethernet Support**       | No                              | Yes (via external PHY)              |
| **Hardware Cryptography** | No                              | Yes (hardware acceleration)         |
| **Power Consumption**      | Low                             | Can be lower depending on the mode |

#### **Advantages of Using ESP32 for More Complex Applications:**
- **Higher Processing Power**: The ESP32’s dual-core processor and faster clock speed make it suitable for more demanding applications, such as running complex algorithms or handling multiple tasks simultaneously.
  
- **Bluetooth Connectivity**: The inclusion of Bluetooth allows ESP32 to communicate with a broader range of devices, such as smartphones, fitness trackers, or Bluetooth sensors.
  
- **More I/O Pins**: With more GPIO pins and additional features like DACs and ADCs, the ESP32 is better suited for projects that require multiple sensors, actuators, and interfaces.

- **Advanced Networking**: The ESP32 supports both **Wi-Fi** and **Ethernet** connectivity, making it versatile for networking-intensive projects like home automation, IoT devices, and smart gateways.

- **Low Power Consumption**: The ESP32 has low-power modes, which makes it suitable for battery-operated devices that need to run for long periods without draining the battery.

---

### **Practical:**

#### **1. Setup of the ESP32 in Arduino IDE:**

To begin using the **ESP32** with the **Arduino IDE**, you need to follow these steps:

1. **Install the ESP32 Board Package**:
   - Open Arduino IDE.
   - Go to **File > Preferences**.
   - In the "Additional Boards Manager URLs" field, add the following URL:
     ```
     https://dl.espressif.com/dl/package_esp32_index.json
     ```
   - Go to **Tools > Board > Boards Manager**.
   - Search for **ESP32** and click **Install** on the **ESP32 by Espressif Systems**.

2. **Select the ESP32 Board**:
   - Go to **Tools > Board > ESP32 Dev Module** (or choose your specific ESP32 board).
   - Select the correct **Port** under **Tools > Port**.

3. **Test the Setup**:
   - Once the board and port are set up, it’s time to test the environment.

#### **2. Writing a "Hello World" Program with ESP32:**

Let’s write a simple "Hello World" program to blink an LED on the ESP32. This will help familiarize students with the basic functionality and demonstrate that the ESP32 setup is working.

**Code:**

```cpp
void setup() {
  // Initialize LED pin (on most ESP32 boards, onboard LED is on GPIO 2)
  pinMode(2, OUTPUT);  
}

void loop() {
  // Turn LED on
  digitalWrite(2, HIGH);
  delay(1000);  // Wait for 1 second
  
  // Turn LED off
  digitalWrite(2, LOW);
  delay(1000);  // Wait for 1 second
}
```

**Explanation:**
- **`pinMode(2, OUTPUT)`**: Initializes GPIO pin 2 as an output pin (for the LED).
- **`digitalWrite(2, HIGH)`**: Turns the LED on by setting GPIO pin 2 to HIGH (3.3V).
- **`delay(1000)`**: Waits for 1 second (1000 milliseconds).
- **`digitalWrite(2, LOW)`**: Turns the LED off by setting GPIO pin 2 to LOW (0V).
- This process continues indefinitely in the `loop()` function.

#### **3. Basic LED Blink on ESP32:**

1. **Circuit Setup**: Connect an LED to **GPIO2** (or any other available GPIO pin) on the ESP32 board. Don’t forget to use a **220Ω resistor** to limit the current flowing through the LED.

2. **Upload the Code**:
   - Once the program is written, click the **Upload** button in Arduino IDE to send the code to the ESP32.
   - After successful uploading, the onboard LED should start blinking every 1 second.

3. **Test the Circuit**:
   - The onboard LED or an external LED connected to the specified GPIO pin should blink on and off in 1-second intervals, indicating that the program is running correctly.

---

### **Conclusion:**

- Understand the **key features** of the **ESP32** and how it differs from the ESP8266.
- Be familiar with the **Arduino IDE setup** for ESP32 and able to upload code to the board.
- Have hands-on experience with the **basic LED blink program** on the ESP32, which is foundational for learning how to control devices using GPIO pins.

### **Day 5: Analog Input and Output (ADC/DAC)**

---

### **Theory:**

#### **Introduction to ADC (Analog to Digital Conversion):**
- **What is ADC?**
  - **Analog to Digital Conversion (ADC)** is the process of converting continuous analog signals (which vary smoothly over time) into a digital format that can be processed by a microcontroller. 
  - ADC is essential in IoT applications where sensors like temperature, light, and humidity output analog signals that need to be converted into a digital form for processing.

- **How does ADC work?**
  - The **ADC** works by sampling the analog signal at regular intervals and converting each sample to a corresponding digital value using a process called **quantization**.
  - Typically, ADCs have a specified **resolution** (such as 10-bit, 12-bit), which determines how many discrete values the analog signal can be divided into. A **12-bit ADC** can represent the analog value as one of **4096** (2^12) different levels, whereas a **10-bit ADC** represents the value with 1024 levels.

- **ADC on ESP32:**
  - The **ESP32** has **12-bit ADCs** and can read analog signals from multiple pins (up to 18 on some models). These ADCs are useful for reading sensor values like temperature, light intensity, or potentiometer positions.

#### **Working with Analog Signals in IoT:**
- **IoT devices** often need to interface with sensors that provide **analog signals**, such as temperature, light intensity, or humidity. 
- The ESP32's ADC allows you to convert these analog signals to digital data that can be transmitted over networks, processed by algorithms, and used for decision-making or automation.
  
#### **ESP32 Supports DAC (Digital to Analog Conversion):**
- **Digital to Analog Conversion (DAC)** is the opposite process of ADC. It converts a digital value into a corresponding analog voltage.
- The **ESP32** has built-in DAC channels on GPIO pins **25** and **26** that allow you to output an analog signal (PWM-controlled) from a digital value.
  
  - DAC can be useful for applications such as controlling the brightness of LEDs, audio output, or generating smooth analog signals from a microcontroller.

---

### **Practical:**

#### **1. Reading Analog Input from a Potentiometer:**
To demonstrate how to read an analog signal, we will use a **potentiometer** (variable resistor) to provide a changing voltage that will be read by the ESP32's **ADC** pin.

**Components:**
- Potentiometer (10kΩ is a typical value)
- ESP32 board
- Jumper wires
- Breadboard

**Circuit Setup:**
- **Potentiometer**: One end connected to **3.3V**, the other end connected to **GND**, and the wiper (middle pin) connected to **GPIO34** (or any other ADC pin).
- **ESP32**: Connect the potentiometer to the **GPIO34** pin (or any other ADC-capable pin).
  
**Code:**
```cpp
int potPin = 34;  // ADC pin (GPIO34)
int potValue = 0;  // Variable to store potentiometer value

void setup() {
  Serial.begin(115200);
}

void loop() {
  // Read the potentiometer value (range 0-4095 for 12-bit ADC)
  potValue = analogRead(potPin);
  
  // Print the value to the Serial Monitor
  Serial.println(potValue);
  
  delay(500);  // Wait for 500ms
}
```

**Explanation:**
- **`analogRead(potPin)`** reads the voltage from the potentiometer and converts it to a digital value (0 to 4095 for a 12-bit ADC).
- The value is printed to the **Serial Monitor**, where you can observe how the value changes as you adjust the potentiometer.

#### **2. Controlling the Brightness of an LED Using PWM (Pulse Width Modulation):**
In this exercise, we’ll control the brightness of an LED using a **PWM signal** generated by the **ESP32**.

**Components:**
- ESP32 board
- LED
- 220Ω Resistor
- Jumper wires

**Circuit Setup:**
- **LED**: Connect the **anode (longer leg)** of the LED to **GPIO13** (or any PWM-capable pin) and the **cathode (shorter leg)** to **GND** through a **220Ω resistor**.

**Code:**
```cpp
int ledPin = 13;  // LED connected to GPIO13
int potPin = 34;  // Potentiometer connected to GPIO34
int potValue = 0;  // Variable to store potentiometer value
int ledBrightness = 0;  // Variable to store PWM value for LED

void setup() {
  pinMode(ledPin, OUTPUT);
  Serial.begin(115200);
}

void loop() {
  // Read potentiometer value
  potValue = analogRead(potPin);
  
  // Map the potentiometer value (0-4095) to LED brightness (0-255)
  ledBrightness = map(potValue, 0, 4095, 0, 255);
  
  // Control LED brightness using PWM
  analogWrite(ledPin, ledBrightness);
  
  // Print the potentiometer and LED brightness values to Serial Monitor
  Serial.print("Potentiometer Value: ");
  Serial.print(potValue);
  Serial.print("\t LED Brightness: ");
  Serial.println(ledBrightness);
  
  delay(100);  // Small delay
}
```

**Explanation:**
- **`analogRead(potPin)`** reads the potentiometer value.
- **`map(potValue, 0, 4095, 0, 255)`** maps the 12-bit ADC value (0-4095) to a PWM value (0-255) for the LED brightness.
- **`analogWrite(ledPin, ledBrightness)`** adjusts the brightness of the LED using PWM based on the potentiometer value.
  
The **PWM** works by turning the LED on and off very quickly, with the **duty cycle** (percentage of time the LED is on) controlling the perceived brightness. A higher duty cycle means the LED is on more, making it appear brighter.

#### **3. Sending Analog Data Over Wi-Fi to a Server:**
In this exercise, we’ll read analog data (from a potentiometer) and send it to a web server over **Wi-Fi**.

**Components:**
- ESP32 board
- Potentiometer
- Jumper wires

**Circuit Setup:**
- Same as the potentiometer setup for reading analog data.

**Code:**
```cpp
#include <WiFi.h>

const char* ssid = "your_SSID";     // Replace with your Wi-Fi SSID
const char* password = "your_PASSWORD"; // Replace with your Wi-Fi password

const char* host = "http://your-server.com/receive_data"; // Replace with your server URL

int potPin = 34;  // Potentiometer connected to GPIO34
int potValue = 0;  // Variable to store potentiometer value

void setup() {
  Serial.begin(115200);
  delay(10);
  
  // Connect to Wi-Fi
  WiFi.begin(ssid, password);
  
  Serial.print("Connecting to WiFi");
  while (WiFi.status() != WL_CONNECTED) {
    delay(500);
    Serial.print(".");
  }
  
  Serial.println("Connected to WiFi");
}

void loop() {
  // Read the potentiometer value (range 0-4095)
  potValue = analogRead(potPin);
  
  // Connect to the server
  WiFiClient client;
  
  if (client.connect(host, 80)) {
    // Send data to the server (HTTP POST request)
    client.println("POST /receive_data HTTP/1.1");
    client.println("Host: your-server.com");
    client.println("Content-Type: application/x-www-form-urlencoded");
    client.print("Content-Length: ");
    client.println(String(potValue).length());
    client.println();
    client.print(potValue);  // Send potentiometer value
    
    client.stop();
  }
  
  delay(1000);  // Send data every second
}
```

**Explanation:**
- **Wi-Fi Connection**: The ESP32 connects to a Wi-Fi network using the `WiFi.begin()` function.
- **HTTP POST Request**: The potentiometer value is sent as part of an HTTP POST request to a specified server.
- The server must be set up to handle incoming data at the specified endpoint (`/receive_data`).

---

### **Conclusion:**

- Understand **ADC and DAC** concepts and how they are used in IoT applications.
- Be able to **read analog data** from a potentiometer and send it to a server over Wi-Fi.
- Know how to **control LED brightness** using **PWM** on the ESP32.

### **Day 6: Communication Protocols: Serial, SPI, and I2C**

---

### **Theory:**

#### **Overview of Serial, SPI, and I2C Protocols:**

1. **Serial Communication:**
   - **Definition**: Serial communication refers to transmitting data one bit at a time over a single communication line. It is the most basic form of communication in microcontrollers and used for debugging, logging, and simple data exchange.
   - **How it Works**: Data is sent bit by bit, typically in **8-bit chunks (1 byte)**. This can be done **asynchronous** (like UART) or **synchronous**.
   - **Common Use Cases**: 
     - Debugging using **Serial Monitor**.
     - Communication between microcontrollers.
     - Connecting modules like **GPS**, **Bluetooth**, or **Wi-Fi**.
  
2. **SPI (Serial Peripheral Interface):**
   - **Definition**: SPI is a synchronous **serial communication protocol** used to transfer data between a **master** device (like the ESP32) and one or more **slave** devices (such as sensors, displays, or memory chips).
   - **Key Features**:
     - **4 wires**: 
       - **MISO (Master In Slave Out)**: Carries data from the slave to the master.
       - **MOSI (Master Out Slave In)**: Carries data from the master to the slave.
       - **SCK (Clock)**: Carries the clock signal generated by the master.
       - **SS (Slave Select)**: Selects the active slave.
   - **Speed**: SPI allows high-speed communication compared to I2C.
   - **Common Use Cases**: 
     - **SD card communication**.
     - **OLED and TFT displays**.
     - **ADC/DAC chips**.
  
3. **I2C (Inter-Integrated Circuit):**
   - **Definition**: I2C is another synchronous protocol but uses only two wires: **SDA (Serial Data)** and **SCL (Serial Clock)**.
   - **Key Features**:
     - **Two wires**: 
       - **SDA** (Data Line): Transfers data between devices.
       - **SCL** (Clock Line): Carries the clock signal.
     - **Multiple devices**: I2C supports multiple devices on the same bus, each with a unique address.
   - **Speed**: Typically slower than SPI, but sufficient for sensors and small displays.
   - **Common Use Cases**: 
     - **Sensors** (e.g., temperature, humidity).
     - **Displays** (e.g., I2C LCD screens).
     - **EEPROMs** and other memory devices.

#### **Differences Between Serial, SPI, and I2C:**

| Feature                  | Serial                | SPI                      | I2C                         |
|--------------------------|-----------------------|--------------------------|-----------------------------|
| **Number of Wires**       | 2 wires (TX, RX)      | 4 wires (MISO, MOSI, SCK, SS) | 2 wires (SDA, SCL)         |
| **Speed**                 | Low (9600 bps typical) | High (up to 10 Mbps)     | Medium (100 kbps to 1 Mbps) |
| **Data Transfer**         | One bit at a time     | Full-duplex, multiple bits at once | Half-duplex, one bit at a time |
| **Number of Devices**     | 2 devices (TX, RX)    | One master, multiple slaves | One master, multiple slaves |
| **Complexity**            | Simple                | Moderate (Requires more pins) | Simple (Requires addressing) |
| **Common Applications**   | Debugging, communication | Display, sensors, SD card | Sensors, displays, EEPROM   |

#### **When to Use Each Protocol in IoT Projects:**
- **Serial** is best suited for debugging, logging, and simple communication between two devices (e.g., Arduino and a PC).
- **SPI** is ideal when you need fast communication between devices, especially when high-speed data transfer is necessary (e.g., connecting a display, SD card, or a fast sensor).
- **I2C** is a good choice when you have multiple devices with limited pins (e.g., connecting several sensors, EEPROMs, or displays) in a low-speed communication scenario.

---

### **Practical:**

#### **1. Serial Communication with ESP8266/ESP32:**
In this exercise, we will use **serial communication** to send and receive data between the **ESP32** and a **PC** (via the Serial Monitor).

**Components:**
- ESP32 or ESP8266 board
- Jumper wires

**Code:**
```cpp
void setup() {
  Serial.begin(115200);  // Initialize serial communication at 115200 baud rate
  Serial.println("Hello, Serial Communication!");  // Send message to Serial Monitor
}

void loop() {
  if (Serial.available() > 0) {  // Check if data is available
    char incomingByte = Serial.read();  // Read the incoming byte
    Serial.print("Received: ");
    Serial.println(incomingByte);  // Print the received byte
  }
}
```

**Explanation:**
- **`Serial.begin(115200)`** initializes serial communication at a baud rate of 115200.
- **`Serial.available()`** checks if there is incoming data from the Serial Monitor.
- **`Serial.read()`** reads the byte of data sent from the Serial Monitor.
- **`Serial.println()`** sends the received byte back to the Serial Monitor.

#### **2. Connecting an I2C LCD with ESP32 and Displaying Data:**
In this exercise, we will connect an I2C LCD to the **ESP32** and display data (e.g., potentiometer value).

**Components:**
- ESP32 board
- I2C 16x2 LCD
- Potentiometer
- Jumper wires

**Circuit Setup:**
- **I2C LCD**: Connect the **SDA** to **GPIO21** and **SCL** to **GPIO22** (default I2C pins on ESP32).
- **Potentiometer**: One end to **3.3V**, the other end to **GND**, and the wiper to **GPIO34**.

**Code:**
```cpp
#include <Wire.h>
#include <LiquidCrystal_I2C.h>

LiquidCrystal_I2C lcd(0x27, 16, 2);  // Set the I2C address and size (16x2)

int potPin = 34;  // Potentiometer connected to GPIO34
int potValue = 0;

void setup() {
  lcd.begin();
  lcd.print("I2C LCD Test");
  delay(2000);
}

void loop() {
  potValue = analogRead(potPin);  // Read potentiometer value
  lcd.clear();
  lcd.print("Pot Value: ");
  lcd.print(potValue);
  delay(500);
}
```

**Explanation:**
- The **`Wire`** library is used for I2C communication.
- The **`LiquidCrystal_I2C`** library is used to control the I2C LCD.
- **`lcd.print()`** displays the text on the LCD screen.
- The potentiometer value is read using **`analogRead()`** and displayed on the LCD.

#### **3. Interfacing a Sensor (e.g., Temperature Sensor) Using I2C:**
In this exercise, we will interface an I2C **temperature sensor** (e.g., **HTU21D** or **BMP280**) and display the temperature on the **I2C LCD**.

**Components:**
- ESP32 board
- I2C Temperature Sensor (e.g., **HTU21D**)
- I2C LCD
- Jumper wires

**Circuit Setup:**
- **I2C LCD**: Connect **SDA** to **GPIO21** and **SCL** to **GPIO22**.
- **HTU21D** sensor: Connect **SDA** to **GPIO21** and **SCL** to **GPIO22**.

**Code (for HTU21D):**
```cpp
#include <Wire.h>
#include <LiquidCrystal_I2C.h>
#include <HTU21D.h>

LiquidCrystal_I2C lcd(0x27, 16, 2);  // Set the I2C address for the LCD
HTU21D mySensor;  // Create a sensor object

void setup() {
  lcd.begin();
  lcd.print("I2C Sensor Test");
  delay(2000);
  mySensor.begin();  // Initialize the sensor
}

void loop() {
  float temperature = mySensor.readTemperature();  // Read temperature from sensor
  lcd.clear();
  lcd.print("Temp: ");
  lcd.print(temperature);
  lcd.print(" C");
  delay(1000);  // Wait for 1 second
}
```

**Explanation:**
- The **`HTU21D`** library is used to interface with the temperature sensor.
- **`mySensor.readTemperature()`** reads the temperature in Celsius.
- The temperature is displayed on the **I2C LCD**.

---

### **Conclusion:**

- Understand the differences between **Serial**, **SPI**, and **I2C** protocols.
- Be able to communicate using **Serial** for debugging and simple data exchange.
- Connect an **I2C LCD** with **ESP32** and display data.
- Interface an **I2C sensor** (e.g., temperature sensor) with **ESP32** and display readings on the LCD.

### **Day 7: Wi-Fi Configuration and Connecting to the Internet**

---

### **Theory:**

#### **How Wi-Fi Works:**
- **Wi-Fi (Wireless Fidelity)** is a technology that uses **radio waves** to provide network connectivity to devices over short distances (typically within a range of 100 meters).
- **Wi-Fi networks** are based on the **IEEE 802.11** family of standards. It operates in the **2.4 GHz** or **5 GHz** frequency bands.
- **Wi-Fi communication** typically works through an access point (AP), which provides a bridge between devices and the internet or local network. Devices connect wirelessly to the AP using a **SSID (Service Set Identifier)** and **password**.
- When a device (like the **ESP8266** or **ESP32**) is connected to Wi-Fi, it can send and receive data packets to/from the internet.

#### **Setting up Wi-Fi Credentials in ESP8266 and ESP32:**
- Both the **ESP8266** and **ESP32** have built-in **Wi-Fi** modules, so there is no need for an external Wi-Fi module.
- You can set up the Wi-Fi connection by providing the network **SSID** (name of the Wi-Fi) and the **password** in your code.
- Using the **`WiFi`** library in the Arduino IDE, you can configure and manage Wi-Fi connections.

#### **Connecting to Wi-Fi in Arduino IDE:**
1. **Include Wi-Fi Library**: First, you need to include the library for Wi-Fi:
   ```cpp
   #include <WiFi.h>  // For ESP32
   #include <ESP8266WiFi.h>  // For ESP8266
   ```
2. **Initialize Wi-Fi**: In your code, specify the **SSID** and **password**.
3. **Wi-Fi Connection**: The ESP board will use the `WiFi.begin(SSID, password)` function to connect to the network. After that, it will check if the connection was successful by checking `WiFi.status()`.

**Example of Wi-Fi connection setup:**
```cpp
#include <WiFi.h>  // For ESP32, use ESP8266WiFi.h for ESP8266

const char* ssid = "your_wifi_ssid";  // Replace with your Wi-Fi SSID
const char* password = "your_wifi_password";  // Replace with your Wi-Fi password

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);  // Connect to Wi-Fi
  while (WiFi.status() != WL_CONNECTED) {  // Wait until connected
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to Wi-Fi");
  Serial.print("IP Address: ");
  Serial.println(WiFi.localIP());  // Print IP address after successful connection
}

void loop() {
  // Your main code goes here
}
```
- **`WiFi.begin(ssid, password)`**: This function starts the connection attempt.
- **`WiFi.status()`**: This function checks the current status of the Wi-Fi connection.
  - If the connection is successful, it will return **`WL_CONNECTED`**.
- **`WiFi.localIP()`**: After the ESP board successfully connects, this function will return the **IP address** assigned to it.

#### **Testing Connectivity with a Simple HTTP Request:**
Once the device is connected to Wi-Fi, you can send an **HTTP request** to a server (e.g., get data from a website or send data to an API) to test the internet connectivity.

1. **ESP8266/ESP32 HTTP Request:**
   - **HTTP GET Request**: To test the connection, you can send an HTTP GET request to a server.
   - To perform an HTTP request, you can use the **WiFiClient** class or the **HTTPClient** library for more advanced HTTP operations.

---

### **Practical:**

#### **1. Connecting NodeMCU/ESP32 to a Wi-Fi Network:**

In this practical session, the student will connect the **NodeMCU (ESP8266)** or **ESP32** to a Wi-Fi network.

**Components:**
- ESP8266 or ESP32 board
- USB cable for programming
- Wi-Fi network with SSID and password

**Steps:**
1. Open the Arduino IDE and write the code for connecting to Wi-Fi using the example provided in the theory section.
2. Upload the code to the NodeMCU/ESP32.
3. Open the **Serial Monitor** to see the output.
4. If the Wi-Fi connection is successful, you will see a message like:
   ```
   Connected to Wi-Fi
   IP Address: 192.168.1.x
   ```

---

#### **2. Testing Connectivity with a Simple HTTP Request:**

Once the Wi-Fi connection is established, we will use the **HTTPClient** library (for ESP32) or **ESP8266HTTPClient** library (for ESP8266) to send a simple HTTP GET request to a public API or website.

**Code:**
```cpp
#include <WiFi.h>            // For ESP32, use ESP8266WiFi.h for ESP8266
#include <HTTPClient.h>      // For HTTP requests

const char* ssid = "your_wifi_ssid";  // Replace with your Wi-Fi SSID
const char* password = "your_wifi_password";  // Replace with your Wi-Fi password
const char* serverName = "http://example.com";  // Replace with the URL you want to connect to

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);  // Connect to Wi-Fi
  while (WiFi.status() != WL_CONNECTED) {  // Wait until connected
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to Wi-Fi");
  Serial.print("IP Address: ");
  Serial.println(WiFi.localIP());  // Print the IP address assigned

  // Send HTTP GET request
  HTTPClient http;
  http.begin(serverName);  // Specify the URL
  int httpCode = http.GET();  // Send GET request
  if (httpCode > 0) {
    String payload = http.getString();  // Get the response payload
    Serial.println("HTTP Response Code: " + String(httpCode));
    Serial.println("Response Payload: " + payload);  // Print the response
  } else {
    Serial.println("Error in HTTP request");
  }
  http.end();  // End the HTTP connection
}

void loop() {
  // Main loop can be used for other tasks
}
```

**Explanation:**
- **`HTTPClient`**: This library is used for sending HTTP requests.
- **`http.begin(serverName)`**: This function specifies the server URL (endpoint).
- **`http.GET()`**: This sends an HTTP GET request to the specified server.
- **`http.getString()`**: This retrieves the response payload from the server.

- If the request is successful, it will print the **HTTP response code** (e.g., 200 for success) and the **response payload** (the body of the response).

---

### **Conclusion:**

- Understand the concept of **Wi-Fi** and how it works.
- Be able to **connect their ESP8266 or ESP32** to a Wi-Fi network using the **Arduino IDE**.
- Test **Wi-Fi connectivity** by making a simple **HTTP GET request** to a server or website.

### **Day 8: Using HTTP Protocol to Connect to a Web Server**

---

### **Theory:**

#### **Overview of HTTP Protocol:**
- **HTTP (HyperText Transfer Protocol)** is the fundamental protocol used for communication on the **World Wide Web (WWW)**. It defines the rules for **requesting and delivering** web resources (such as HTML files, images, or data).
- **HTTP Requests**:
  - **GET**: Retrieves data from the server.
  - **POST**: Sends data to the server (commonly used to submit form data).
- **HTTP Response**:
  - The server sends a response with a **status code** (e.g., 200 for success, 404 for not found).
  - The response may include the requested data, often in **JSON** or **HTML** format.

#### **Sending HTTP Requests from ESP8266/ESP32 to a Web Server:**
- The **ESP8266** and **ESP32** can communicate with web servers using **HTTP requests**.
- You can use libraries like `HTTPClient` (for ESP32) and `ESP8266HTTPClient` (for ESP8266) to send HTTP requests and handle responses.
  
  **Steps:**
  1. Initialize the connection to the **Wi-Fi network**.
  2. Use `http.begin(url)` to specify the **server URL**.
  3. Use `http.GET()` for sending a **GET request** or `http.POST()` for sending a **POST request**.
  4. Handle the response and **parse** the data returned by the server.

#### **RESTful APIs and JSON Format:**
- **RESTful APIs (Representational State Transfer)**:
  - A set of rules for building web services that allow communication between different systems using HTTP.
  - RESTful APIs are designed around the concept of **resources** (e.g., users, products) which are accessed using standard HTTP methods like GET, POST, PUT, DELETE.
  
- **JSON (JavaScript Object Notation)**:
  - A lightweight data-interchange format, easy to read and write for humans and machines.
  - Used extensively in web services to exchange data between the client (ESP8266/ESP32) and the server.

Example of a JSON object:
```json
{
  "temperature": 23.5,
  "humidity": 60
}
```

---

### **Practical:**

#### **1. Sending GET/POST Requests from ESP8266/ESP32 to a Simple Server:**

**Objective:**
- Learn to send **GET** and **POST** requests to a web server using ESP8266/ESP32.

**Components:**
- ESP8266 or ESP32 board
- Wi-Fi network with SSID and password
- A web server that accepts HTTP requests (you can use platforms like **ThingSpeak**, **Adafruit IO**, or your own local server).

**Steps:**
1. First, establish a Wi-Fi connection (as done previously on Day 7).
2. Use the **HTTPClient** library to send GET or POST requests to a server.
   
**GET Request Example (ESP32 or ESP8266):**
```cpp
#include <WiFi.h>  // For ESP32, use ESP8266WiFi.h for ESP8266
#include <HTTPClient.h>

const char* ssid = "your_wifi_ssid";  // Replace with your Wi-Fi SSID
const char* password = "your_wifi_password";  // Replace with your Wi-Fi password
const char* serverName = "http://example.com/api/data";  // Replace with your server URL

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);  // Connect to Wi-Fi
  while (WiFi.status() != WL_CONNECTED) {  // Wait until connected
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to Wi-Fi");

  // Sending GET request
  HTTPClient http;
  http.begin(serverName);  // Specify the URL
  int httpCode = http.GET();  // Send GET request
  if (httpCode > 0) {
    String payload = http.getString();  // Get the response payload
    Serial.println("HTTP Response Code: " + String(httpCode));
    Serial.println("Response Payload: " + payload);  // Print the response
  } else {
    Serial.println("Error in GET request");
  }
  http.end();  // End the HTTP connection
}

void loop() {
  // Main loop can be used for other tasks
}
```

**POST Request Example (ESP32 or ESP8266):**
```cpp
#include <WiFi.h>  // For ESP32, use ESP8266WiFi.h for ESP8266
#include <HTTPClient.h>

const char* ssid = "your_wifi_ssid";  // Replace with your Wi-Fi SSID
const char* password = "your_wifi_password";  // Replace with your Wi-Fi password
const char* serverName = "http://example.com/api/data";  // Replace with your server URL

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);  // Connect to Wi-Fi
  while (WiFi.status() != WL_CONNECTED) {  // Wait until connected
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to Wi-Fi");

  // Sending POST request with data
  HTTPClient http;
  http.begin(serverName);  // Specify the URL
  http.addHeader("Content-Type", "application/json");  // Specify content type

  String jsonData = "{\"temperature\": 23.5, \"humidity\": 60}";  // JSON data to send
  int httpCode = http.POST(jsonData);  // Send POST request with data
  if (httpCode > 0) {
    String payload = http.getString();  // Get the response payload
    Serial.println("HTTP Response Code: " + String(httpCode));
    Serial.println("Response Payload: " + payload);  // Print the response
  } else {
    Serial.println("Error in POST request");
  }
  http.end();  // End the HTTP connection
}

void loop() {
  // Main loop can be used for other tasks
}
```

- In the **GET** request, we simply retrieve data from the server.
- In the **POST** request, we send **JSON data** to the server (in this case, data for temperature and humidity).

---

#### **2. Parsing JSON Data in Arduino:**

In many IoT applications, the server response is often in **JSON** format. Arduino can parse this JSON response using a library such as **ArduinoJson**.

**Steps:**
1. Install the **ArduinoJson** library via the **Library Manager** in the Arduino IDE.
2. Use the library to parse JSON data received from a web server.

**JSON Parsing Example:**
```cpp
#include <WiFi.h>              // For ESP32, use ESP8266WiFi.h for ESP8266
#include <HTTPClient.h>
#include <ArduinoJson.h>  // Include ArduinoJson library

const char* ssid = "your_wifi_ssid";
const char* password = "your_wifi_password";
const char* serverName = "http://example.com/api/data";

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to Wi-Fi");

  // Send GET request
  HTTPClient http;
  http.begin(serverName);
  int httpCode = http.GET();
  if (httpCode > 0) {
    String payload = http.getString();
    Serial.println("HTTP Response Code: " + String(httpCode));
    Serial.println("Response Payload: " + payload);

    // Parse the JSON response
    DynamicJsonDocument doc(1024);
    deserializeJson(doc, payload);  // Parse the JSON payload

    // Extract values from JSON
    float temperature = doc["temperature"];  // Access temperature value
    int humidity = doc["humidity"];         // Access humidity value

    Serial.print("Temperature: ");
    Serial.println(temperature);
    Serial.print("Humidity: ");
    Serial.println(humidity);
  } else {
    Serial.println("Error in GET request");
  }
  http.end();
}

void loop() {
  // Main loop for other tasks
}
```

- **`DynamicJsonDocument`**: This creates a memory buffer for storing the parsed JSON object.
- **`deserializeJson(doc, payload)`**: This function takes the raw JSON string (`payload`) and parses it into the `doc` object.
- **Accessing JSON data**: After parsing, you can access values from the JSON object by using the keys (e.g., `"temperature"` and `"humidity"`).

---

### **Conclusion:**
- Understand the basics of the **HTTP protocol** and how it is used to send requests and receive responses from a web server.
- Be able to send **GET** and **POST** requests from the **ESP8266** or **ESP32** to a web server.
- Be familiar with the concept of **RESTful APIs** and how to handle **JSON data** for communication between IoT devices and servers.

### **Day 9: IoT Cloud Platforms (ThingSpeak) Introduction**

---

### **Theory:**

#### **Introduction to IoT Cloud Platforms: Why Are They Necessary?**
- **IoT cloud platforms** provide the infrastructure and tools to collect, store, analyze, and visualize data from IoT devices. These platforms make it easier to manage large amounts of sensor data and control connected devices remotely.
- **Necessity of IoT Cloud Platforms**:
  - **Data Storage**: IoT devices generate large amounts of data that need to be stored in a secure and scalable environment.
  - **Remote Access**: Cloud platforms allow users to access data from anywhere and at any time.
  - **Real-time Monitoring**: Data collected from IoT devices can be visualized in real-time, helping to monitor systems efficiently.
  - **Data Analytics**: Advanced cloud platforms provide tools to analyze and interpret sensor data for decision-making.
  - **Scalability**: As more IoT devices are deployed, cloud platforms allow systems to scale easily, handling more devices and more data.

---

#### **Overview of ThingSpeak, a Popular IoT Platform:**
- **ThingSpeak** is a widely used open-source IoT platform that enables users to collect, analyze, and visualize data from IoT devices. It is built on top of **MATLAB** for data analysis and visualization.
- **Key Features of ThingSpeak**:
  - **Data Channels**: You can create channels to store different types of data (e.g., temperature, humidity, etc.).
  - **APIs for Communication**: ThingSpeak provides APIs that allow IoT devices (like ESP8266/ESP32) to send and receive data.
  - **Visualization**: ThingSpeak provides real-time graphing of data for easy monitoring and analysis.
  - **MATLAB Integration**: ThingSpeak integrates with MATLAB for advanced data analytics and processing.
  - **Real-time Data Collection**: ThingSpeak allows you to collect data in real-time via HTTP, MQTT, and other protocols.

---

#### **Creating an Account and Setting Up a Channel:**
1. **Creating an Account**:
   - Go to the [ThingSpeak website](https://thingspeak.com/) and click on **Sign Up**.
   - Fill in your details (name, email, etc.) to create an account.

2. **Setting Up a Channel**:
   - After logging in, click on **My Channels** and then click on **New Channel**.
   - Provide the necessary information for your channel, such as:
     - **Channel Name**: Name of your channel (e.g., “Temperature and Humidity”).
     - **Fields**: Specify the fields that will hold data (e.g., "Temperature", "Humidity").
     - Optionally, enable **location data**, **unit labels**, and other settings.
   - Click **Save Channel** after entering all the necessary details.
   - **Channel API Keys**: After creating the channel, you’ll be provided with an **API Key** (Write API Key). This key will be used to send data from your ESP8266/ESP32 device to the ThingSpeak platform.

---

### **Practical:**

#### **Sending Sensor Data (e.g., Temperature, Humidity) from ESP8266/ESP32 to ThingSpeak:**

**Objective:**
- Learn how to send data (e.g., temperature and humidity) from ESP8266/ESP32 to the ThingSpeak platform for storage and visualization.

**Components:**
- ESP8266/ESP32 board
- DHT11/DHT22 sensor (for temperature and humidity)
- ThingSpeak account (with API keys)

**Steps:**

1. **Connect the Sensor to ESP8266/ESP32**:
   - For temperature and humidity, you can use a **DHT11** or **DHT22** sensor. Connect the sensor to one of the GPIO pins on the ESP8266/ESP32.
   
   **Wiring for DHT11/DHT22**:
   - **VCC** -> 3.3V (ESP8266/ESP32)
   - **GND** -> GND
   - **DATA** -> GPIO pin (e.g., D2 on ESP8266/ESP32)

2. **Install Libraries**:
   - Install the **DHT sensor library** from the Arduino IDE Library Manager (`DHT sensor library by Adafruit`).
   - Install the **ThingSpeak library** for sending data to the platform.

3. **Writing the Code**:
   - The following example code will connect to Wi-Fi, read data from the sensor, and send it to ThingSpeak.

```cpp
#include <ESP8266WiFi.h>         // For ESP8266, use ESP32WiFi.h for ESP32
#include <ThingSpeak.h>           // ThingSpeak library
#include <DHT.h>                  // DHT sensor library

const char* ssid = "your_wifi_ssid";        // Replace with your Wi-Fi SSID
const char* password = "your_wifi_password";  // Replace with your Wi-Fi password

const char* server = "api.thingspeak.com";  // ThingSpeak server
const unsigned long channelID = YOUR_CHANNEL_ID;  // Replace with your channel ID
const char* writeAPIKey = "YOUR_WRITE_API_KEY";  // Replace with your channel's write API key

WiFiClient client;

DHT dht(D2, DHT22);  // Initialize DHT sensor, using GPIO pin D2 and DHT22 sensor

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);
  
  // Wait for connection
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to WiFi!");

  ThingSpeak.begin(client);  // Initialize ThingSpeak
  dht.begin();  // Initialize DHT sensor
}

void loop() {
  float humidity = dht.readHumidity();   // Read humidity
  float temperature = dht.readTemperature(); // Read temperature
  
  if (isnan(humidity) || isnan(temperature)) {
    Serial.println("Failed to read from DHT sensor!");
    return;
  }

  // Send data to ThingSpeak
  ThingSpeak.setField(1, temperature);  // Field 1 for temperature
  ThingSpeak.setField(2, humidity);     // Field 2 for humidity

  int x = ThingSpeak.writeFields(channelID, writeAPIKey);  // Send data to ThingSpeak
  if (x == 200) {
    Serial.println("Data sent successfully");
  } else {
    Serial.println("Failed to send data");
  }

  delay(20000);  // Wait for 20 seconds before sending the next data
}
```

**Explanation of the Code**:
- **Wi-Fi Setup**: The ESP8266/ESP32 connects to a Wi-Fi network using the **WiFi.begin** function.
- **DHT Sensor**: The code reads data from the **DHT22** sensor (temperature and humidity).
- **ThingSpeak API**: The **ThingSpeak.setField()** function assigns sensor readings to specific fields in the ThingSpeak channel. The **ThingSpeak.writeFields()** function sends the data to ThingSpeak.
- **Data Transmission Interval**: The data is sent every 20 seconds (`delay(20000)`).

4. **Visualization on ThingSpeak**:
   - After the data is sent to ThingSpeak, log into your ThingSpeak account.
   - Go to your channel and view the real-time graph for temperature and humidity.
   - The data should be displayed automatically as it’s updated in real-time.

---

### **Conclusion:**
- Understand the necessity and benefits of **IoT cloud platforms**.
- Be familiar with **ThingSpeak**, a popular IoT platform for storing and visualizing sensor data.
- Be able to send sensor data (e.g., temperature and humidity) from **ESP8266/ESP32** to **ThingSpeak**.
- Know how to visualize IoT data in **real-time** on the ThingSpeak platform.

### **Day 10: Interfacing Sensors with NodeMCU and ESP32**

---

### **Theory:**

#### **Overview of Common IoT Sensors:**
In the IoT world, sensors are critical components used to collect data from the physical environment and feed that data to microcontrollers or cloud platforms for analysis and action. Some common sensors used in IoT applications include:

1. **Temperature Sensors**:
   - **DHT11/DHT22**: These are popular sensors for measuring temperature and humidity. The DHT11 is cheaper but has a lower accuracy range, while the DHT22 offers higher accuracy.
   - **LM35**: A temperature sensor that provides analog output proportional to the temperature.

2. **Humidity Sensors**:
   - **DHT11/DHT22**: Both of these sensors also measure humidity along with temperature.
   - **HIH-4030**: Another popular humidity sensor that provides an analog output.

3. **Motion Sensors**:
   - **PIR (Passive Infrared) Sensor**: Detects motion by measuring infrared radiation changes. Used for security and automation applications.

4. **Gas Sensors**:
   - **MQ Series Sensors**: These sensors can detect various gases such as CO, CO2, methane, LPG, and alcohol. The MQ-2, MQ-3, and MQ-7 are commonly used for air quality monitoring.

5. **Light Sensors**:
   - **LDR (Light Dependent Resistor)**: Changes its resistance based on the intensity of light. Useful in applications like automatic lighting systems.
   
---

#### **Understanding Sensor Calibration and Interfacing:**

- **Calibration**: Calibration ensures that the sensor provides accurate readings. Some sensors, like the **DHT11/DHT22**, are factory calibrated, but others might require manual calibration using known reference values.
  - **DHT11/DHT22**: These sensors are already factory-calibrated, so you don't need to worry much about calibration for basic usage.
  
- **Interfacing Sensors with Microcontrollers**:
  - **Digital Sensors** (e.g., DHT11/DHT22) send data as a digital signal that can be directly read by the microcontroller’s GPIO pins.
  - **Analog Sensors** (e.g., LDR, gas sensors) require analog-to-digital conversion (ADC) before the microcontroller can process the data. Both ESP8266 and ESP32 have built-in ADC capabilities, though the ESP32 has a more advanced ADC with higher resolution.
  
- **Wiring and Connections**:
  - **DHT11/DHT22**: These sensors have three pins: **VCC** (power), **GND** (ground), and **DATA** (output).
  - Connect the **DATA** pin to any available GPIO pin (e.g., D2 on ESP8266 or GPIO 21 on ESP32).
  - A **pull-up resistor** (4.7kΩ or 10kΩ) is typically required between the **DATA** pin and **VCC** to ensure proper data transmission.

---

### **Practical:**

#### **Interfacing a DHT11/DHT22 Temperature and Humidity Sensor with ESP8266/ESP32:**

**Objective**:
- Learn to interface a **DHT11/DHT22** temperature and humidity sensor with an ESP8266 or ESP32 and send the readings to the **ThingSpeak** cloud platform for monitoring.

**Components**:
- ESP8266/ESP32 board
- **DHT11** or **DHT22** sensor
- **10kΩ resistor** (optional, for pull-up on the DATA pin)
- Jumper wires
- Breadboard (optional)

**Steps**:

1. **Wiring the DHT11/DHT22 to ESP8266/ESP32**:
   - **DHT11/DHT22 Pinout**:
     - **VCC** -> 3.3V (ESP8266/ESP32)
     - **GND** -> GND
     - **DATA** -> GPIO pin (e.g., D2 on ESP8266 or GPIO 21 on ESP32)
     - Use a **10kΩ pull-up resistor** between the **DATA** pin and **VCC**.

   **Connection Example for DHT22 with ESP8266**:
   - **VCC** -> 3.3V
   - **GND** -> GND
   - **DATA** -> GPIO D2

2. **Install the Required Libraries**:
   - **DHT sensor library**: Install the `DHT sensor library by Adafruit` from the Arduino IDE Library Manager.
   - **ThingSpeak library**: Install the `ThingSpeak` library for easy integration with the ThingSpeak platform.

3. **Write the Code**:
   Here's an example code to interface the **DHT22** sensor and send data to **ThingSpeak**:

```cpp
#include <ESP8266WiFi.h>         // For ESP8266, use ESP32WiFi.h for ESP32
#include <ThingSpeak.h>           // ThingSpeak library
#include <DHT.h>                  // DHT sensor library

const char* ssid = "your_wifi_ssid";        // Replace with your Wi-Fi SSID
const char* password = "your_wifi_password";  // Replace with your Wi-Fi password

const char* server = "api.thingspeak.com";  // ThingSpeak server
const unsigned long channelID = YOUR_CHANNEL_ID;  // Replace with your channel ID
const char* writeAPIKey = "YOUR_WRITE_API_KEY";  // Replace with your channel's write API key

WiFiClient client;

DHT dht(D2, DHT22);  // Initialize DHT sensor, using GPIO pin D2 and DHT22 sensor

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);
  
  // Wait for connection
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to WiFi!");

  ThingSpeak.begin(client);  // Initialize ThingSpeak
  dht.begin();  // Initialize DHT sensor
}

void loop() {
  float humidity = dht.readHumidity();   // Read humidity
  float temperature = dht.readTemperature(); // Read temperature
  
  if (isnan(humidity) || isnan(temperature)) {
    Serial.println("Failed to read from DHT sensor!");
    return;
  }

  // Send data to ThingSpeak
  ThingSpeak.setField(1, temperature);  // Field 1 for temperature
  ThingSpeak.setField(2, humidity);     // Field 2 for humidity

  int x = ThingSpeak.writeFields(channelID, writeAPIKey);  // Send data to ThingSpeak
  if (x == 200) {
    Serial.println("Data sent successfully");
  } else {
    Serial.println("Failed to send data");
  }

  delay(20000);  // Wait for 20 seconds before sending the next data
}
```

**Explanation of the Code**:
- **Wi-Fi Setup**: The ESP8266/ESP32 connects to a Wi-Fi network using the `WiFi.begin()` function.
- **DHT Sensor**: The sensor readings (temperature and humidity) are fetched using the `dht.readTemperature()` and `dht.readHumidity()` functions.
- **ThingSpeak API**: The data from the sensor is sent to ThingSpeak using the `ThingSpeak.setField()` and `ThingSpeak.writeFields()` functions.
- **Transmission Interval**: The data is sent every 20 seconds (`delay(20000)`).

4. **Verify the Data on ThingSpeak**:
   - After uploading the code, the data from your sensor should start appearing on ThingSpeak.
   - Visit your ThingSpeak channel to view the temperature and humidity readings displayed on the live graph.

---

### **Conclusion:**
- Understand how to interface **temperature and humidity sensors** (DHT11/DHT22) with **ESP8266/ESP32**.
- Be able to send sensor data to the **ThingSpeak** cloud platform for visualization.
- Gain hands-on experience in reading sensor values, sending them over Wi-Fi, and visualizing the data in real-time.

### **Day 11: Controlling Devices Remotely via Web (Web Server)**

---

### **Theory:**

#### **Introduction to Web Servers:**

A **web server** is a software application or hardware device that serves web pages to users. It listens for HTTP requests from clients (such as web browsers or mobile apps) and responds by delivering the requested resources, such as HTML pages, images, or data.

In the context of IoT (Internet of Things), an IoT device can act as a web server. This means the device can host a web page or API that can be accessed remotely over the internet or a local network. Through these web interfaces, users can control or monitor IoT devices.

#### **How IoT Devices Can Act as Servers and Communicate via HTTP Requests:**

- **IoT Web Servers**: In an IoT setup, devices like the ESP8266 and ESP32 can host a web server using their internal capabilities. These microcontrollers can receive and respond to HTTP requests (GET/POST) to control devices (like LEDs, motors, or sensors) or retrieve data from sensors.
  
- **HTTP Requests**:
  - **GET**: The client requests information from the server (e.g., sensor data or device status).
  - **POST**: The client sends data to the server (e.g., control commands to turn an LED on or off).
  
- **Benefits**:
  - **Remote Control**: IoT devices can be controlled remotely using a simple web browser or mobile app.
  - **Real-time Communication**: The devices can send or receive real-time data.

---

### **Practical:**

#### **Creating a Simple Web Server on ESP8266/ESP32 to Control an LED:**

**Objective**:
- Set up a simple web server on an ESP8266/ESP32 that can remotely control an LED.

**Components**:
- ESP8266/ESP32 board
- LED
- 220Ω resistor
- Jumper wires
- Breadboard (optional)

**Steps**:

1. **Wiring the LED to ESP8266/ESP32**:
   - **Anode (longer leg) of LED** -> GPIO pin (e.g., D2 on ESP8266 or GPIO 2 on ESP32).
   - **Cathode (shorter leg) of LED** -> GND through a **220Ω resistor**.

2. **Install Required Libraries**:
   - **ESP8266WiFi.h** or **WiFi.h** (for ESP32).
   - **ESP8266WebServer.h** or **WebServer.h** (for ESP32).
   - These libraries are included with the ESP8266/ESP32 board definitions in the Arduino IDE.

3. **Write the Code**:

```cpp
#include <ESP8266WiFi.h>           // For ESP8266; use WiFi.h for ESP32
#include <ESP8266WebServer.h>       // For ESP8266; use WebServer.h for ESP32

const char* ssid = "your_wifi_ssid";            // Replace with your Wi-Fi SSID
const char* password = "your_wifi_password";    // Replace with your Wi-Fi password

ESP8266WebServer server(80); // HTTP server on port 80 for ESP8266; use WebServer for ESP32

int ledPin = D2; // LED connected to GPIO D2 (for ESP8266); use GPIO 2 for ESP32

void setup() {
  Serial.begin(115200);

  // Connect to Wi-Fi
  WiFi.begin(ssid, password);
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to WiFi");

  // Set the LED pin as output
  pinMode(ledPin, OUTPUT);

  // Serve the control page for the LED
  server.on("/", HTTP_GET, []() {
    String html = "<html><body><h1>LED Control</h1>";
    html += "<p><a href=\"/on\"><button>Turn ON</button></a></p>";
    html += "<p><a href=\"/off\"><button>Turn OFF</button></a></p>";
    html += "</body></html>";
    server.send(200, "text/html", html);
  });

  // Control the LED based on URL paths
  server.on("/on", HTTP_GET, []() {
    digitalWrite(ledPin, HIGH); // Turn ON the LED
    server.send(200, "text/html", "LED is ON <br><a href=\"/\">Go Back</a>");
  });

  server.on("/off", HTTP_GET, []() {
    digitalWrite(ledPin, LOW);  // Turn OFF the LED
    server.send(200, "text/html", "LED is OFF <br><a href=\"/\">Go Back</a>");
  });

  // Start the web server
  server.begin();
  Serial.println("Web server started");
}

void loop() {
  server.handleClient(); // Handle incoming client requests
}
```

**Explanation of the Code**:
- **Wi-Fi Setup**: The ESP8266/ESP32 connects to the local Wi-Fi network using the `WiFi.begin()` method.
- **Web Server**: The `ESP8266WebServer` (or `WebServer` for ESP32) listens for HTTP GET requests at specific URLs.
  - At the root URL (`/`), the server serves a simple HTML page with two buttons: one to turn the LED **on** and one to turn it **off**.
  - The `/on` URL turns the LED on, and the `/off` URL turns the LED off.
- **Control Buttons**: Clicking the buttons on the webpage sends an HTTP GET request to the server, which then controls the LED accordingly.

4. **Upload the Code and Test**:
   - Upload the code to the ESP8266/ESP32.
   - Open the **Serial Monitor** to get the IP address assigned to your device.
   - Open a **web browser** and enter the IP address of the ESP8266/ESP32. You should see a page with two buttons: **Turn ON** and **Turn OFF**.
   - Clicking the buttons will turn the LED on and off remotely.

---

### **Accessing the Web Server Through a Browser or Mobile App**:

1. **Using a Web Browser**:
   - After uploading the code and connecting the ESP8266/ESP32 to your Wi-Fi network, open the **Serial Monitor** to find the device's IP address.
   - Enter the IP address into the address bar of any web browser on the same network. You will see the web page served by the ESP8266/ESP32.
   - By clicking the **Turn ON** or **Turn OFF** buttons, you can control the LED remotely.

2. **Using a Mobile App**:
   - You can also use mobile apps like **Blynk**, **ThingSpeak**, or a custom-built app that makes HTTP requests to control the LED on your IoT device. However, for simplicity, the browser-based control is sufficient for this lesson.

---

### **Conclusion:**
- Understand how IoT devices can act as web servers and communicate via HTTP requests.
- Be able to create a simple web server on **ESP8266/ESP32** to control an **LED**.
- Learn how to remotely control IoT devices through a web browser or mobile app. 

This exercise introduces the fundamental concept of web-based control in IoT systems, which is widely used in smart home automation, remote monitoring, and various IoT applications.

### **Day 12: Bluetooth Communication with ESP32 (Optional)**

---

### **Theory:**

#### **Introduction to Bluetooth Low Energy (BLE) with ESP32:**

**Bluetooth Low Energy (BLE)** is a wireless communication technology designed for low-power devices. It is ideal for IoT applications where energy efficiency is critical, such as in wearables, health monitoring devices, and other battery-powered sensors.

- **ESP32 and BLE**:
  - The **ESP32** is equipped with both **Bluetooth Classic** and **Bluetooth Low Energy (BLE)** capabilities, making it versatile for a wide range of applications.
  - **BLE** enables devices to communicate over short distances while consuming minimal power.
  
- **Key Features of BLE**:
  - **Low Power**: BLE uses minimal power, which allows IoT devices to operate for long periods on battery power.
  - **Fast Pairing**: BLE devices can be paired with other devices quickly and efficiently.
  - **Secure Communication**: BLE supports secure communication using encryption and pairing mechanisms.
  - **Multiple Devices**: BLE supports communication with multiple devices, making it suitable for applications like smart home systems where many devices communicate simultaneously.

#### **Use Cases for Bluetooth in IoT Applications:**

- **Smart Home Devices**: BLE is commonly used for controlling and monitoring devices like lights, thermostats, and locks.
- **Health and Fitness Tracking**: Wearables like fitness trackers and heart rate monitors use BLE to communicate with mobile phones or other devices.
- **Asset Tracking**: BLE-based beacons are used for tracking assets in warehouses or retail spaces.
- **Industrial IoT**: BLE sensors can monitor machinery and environmental conditions in industrial settings, providing real-time data to workers or systems.

---

### **Practical:**

#### **Controlling an LED Using Bluetooth with ESP32:**

**Objective**:
- Use the **ESP32's BLE functionality** to control an **LED** remotely via a mobile phone or tablet.

**Components**:
- ESP32 board
- LED
- 220Ω resistor
- Jumper wires
- Breadboard (optional)
- Mobile phone with a BLE-compatible app (e.g., **nRF Connect** or **Bluetooth Terminal**)

---

#### **Steps:**

1. **Wiring the LED to ESP32**:
   - **Anode (longer leg)** of LED -> GPIO 2 (or any available GPIO pin) on ESP32.
   - **Cathode (shorter leg)** of LED -> GND through a **220Ω resistor**.

2. **Install Required Libraries**:
   - **BLEDevice.h**, **BLEUtils.h**, and **BLEServer.h** (These are included in the **ESP32 BLE Arduino library**).
   - You can install this library via the Arduino IDE Library Manager (Search for "ESP32 BLE Arduino").

3. **Write the Code for BLE Communication**:

```cpp
#include <BLEDevice.h>
#include <BLEUtils.h>
#include <BLEServer.h>

#define LED_PIN 2  // LED connected to GPIO 2

// BLE Service and Characteristic UUIDs
#define SERVICE_UUID         "12345678-1234-1234-1234-123456789abc"
#define CHARACTERISTIC_UUID  "abcdabcd-1234-1234-1234-123456789abc"

BLECharacteristic *pCharacteristic;

void setup() {
  Serial.begin(115200);
  
  // Set the LED pin as output
  pinMode(LED_PIN, OUTPUT);

  // Initialize BLE
  BLEDevice::init("ESP32_LED_Control");
  BLEServer *pServer = BLEDevice::createServer();
  
  // Create a service
  BLEService *pService = pServer->createService(SERVICE_UUID);

  // Create a characteristic for controlling the LED
  pCharacteristic = pService->createCharacteristic(
      CHARACTERISTIC_UUID,
      BLECharacteristic::PROPERTY_READ |
      BLECharacteristic::PROPERTY_WRITE
  );
  
  // Start the service
  pService->start();

  // Start advertising the BLE device
  BLEAdvertising *pAdvertising = pServer->getAdvertising();
  pAdvertising->start();

  Serial.println("BLE Device Ready");
}

void loop() {
  // Read the value of the characteristic
  if (pCharacteristic->getValue() == "1") {
    digitalWrite(LED_PIN, HIGH);  // Turn ON the LED
  } else if (pCharacteristic->getValue() == "0") {
    digitalWrite(LED_PIN, LOW);   // Turn OFF the LED
  }
}
```

---

#### **Explanation of the Code**:

- **BLE Initialization**:
  - The ESP32 is initialized as a BLE server using `BLEDevice::init("ESP32_LED_Control")`.
  - A **BLE service** is created with a custom **UUID** (`SERVICE_UUID`), and a **BLE characteristic** is created to control the LED (`CHARACTERISTIC_UUID`).
  
- **LED Control**:
  - The BLE characteristic allows the client (the mobile phone) to send values to the ESP32 to control the LED. If the characteristic's value is `"1"`, the LED turns **on**, and if it's `"0"`, the LED turns **off**.

- **Advertising**:
  - The ESP32 advertises itself as a BLE device using `BLEAdvertising` so that it can be detected by mobile devices or BLE apps.

---

#### **Testing the BLE Communication**:

1. **Upload the Code**: Upload the code to the ESP32 using the Arduino IDE.
2. **Scan for the ESP32 BLE Device**: 
   - Use a BLE scanning app like **nRF Connect** (available for Android and iOS) or a Bluetooth terminal app.
   - Scan for available BLE devices, and you should see a device named **"ESP32_LED_Control"**.
3. **Connect to the ESP32**:
   - Once you connect, you'll see the **LED control characteristic** (with UUID `abcdabcd-1234-1234-1234-123456789abc`).
4. **Control the LED**:
   - Send a **"1"** to turn the LED **on** and a **"0"** to turn it **off**.
   - The LED will respond to the commands sent from your mobile app.

---

### **Conclusion:**

- Understand how to set up **Bluetooth Low Energy (BLE)** communication using the **ESP32**.
- Learn how to create a **simple BLE server** to control an **LED** via Bluetooth.
- Be able to interact with an **ESP32** over Bluetooth using a mobile phone app to send and receive data, demonstrating the potential for wireless control in IoT applications.

**Optional Exercises**:
- Extend the project to control more devices, like motors or sensors, over Bluetooth.
- Add additional BLE characteristics to control other aspects of the ESP32, such as reading sensor data.

### **Day 13: Automation with IoT (MQTT Protocol)**

---

### **Theory:**

#### **Introduction to MQTT Protocol:**

**MQTT (Message Queuing Telemetry Transport)** is a lightweight messaging protocol designed for low-bandwidth, high-latency, and unreliable networks, making it ideal for IoT applications. It operates on the **publish-subscribe model** which provides an efficient way to send messages to many devices without requiring a direct connection between all devices.

- **Why MQTT is Lightweight and Suitable for IoT**:
  - **Low Overhead**: MQTT uses a small packet size (fixed header of 2 bytes) and minimal bandwidth, making it ideal for constrained devices and networks.
  - **Efficient Communication**: The publish-subscribe model decouples devices from each other, allowing devices to send and receive data asynchronously, without needing to know the specifics of other devices.
  - **Quality of Service (QoS)**: MQTT supports different levels of message delivery assurance (QoS 0, 1, 2), which is essential for ensuring reliable communication in IoT applications.
  - **Persistent Sessions**: MQTT allows persistent sessions where messages can be retained for subscribers even when they are temporarily disconnected.

#### **Basic Concepts of MQTT:**

- **Broker**:
  - The **MQTT broker** is a central server responsible for receiving, filtering, and forwarding messages to subscribers. It handles the entire messaging infrastructure.
  - Popular MQTT brokers include **Mosquitto**, **HiveMQ**, and **EMQX**.

- **Topic**:
  - Topics are hierarchical strings used to organize the messages. Each message is associated with a **topic**, which defines the message’s content category (e.g., `home/livingroom/temperature`).
  - Topics are structured in a tree-like manner, where the "slash" (`/`) is used to separate different levels of the topic.

- **Publisher**:
  - A **publisher** sends messages to a specific topic on the broker. The publisher does not need to know about the subscribers, just the topic they are publishing to.

- **Subscriber**:
  - A **subscriber** listens to a specific topic or group of topics and receives messages that are published to those topics.

- **Quality of Service (QoS)**:
  - **QoS 0**: "At most once" delivery, messages may be lost.
  - **QoS 1**: "At least once" delivery, messages are guaranteed to be delivered but may be duplicated.
  - **QoS 2**: "Exactly once" delivery, messages are guaranteed to be delivered exactly once.

---

### **Practical:**

#### **Setting up an MQTT Broker (Eclipse Mosquitto):**

**Objective**: 
- Set up the **Mosquitto MQTT broker** on your local machine or server.
- Use the **ESP8266/ESP32** to send and receive messages to/from the broker.

---

#### **Steps to Set up Mosquitto MQTT Broker**:

1. **Download and Install Mosquitto**:
   - **Windows**: Download the installer from [Eclipse Mosquitto](https://mosquitto.org/download/). Run the installer and follow the installation steps.
   - **Linux (Ubuntu)**:
     ```bash
     sudo apt update
     sudo apt install mosquitto mosquitto-clients
     ```

2. **Start the Mosquitto Broker**:
   - After installation, you can start Mosquitto using the following command:
     - **Windows**: Mosquitto will run as a service after installation.
     - **Linux**: 
       ```bash
       sudo systemctl start mosquitto
       sudo systemctl enable mosquitto
       ```

3. **Test the Broker**:
   - To test the broker locally, use the `mosquitto_sub` (subscriber) and `mosquitto_pub` (publisher) tools:
     - Open a terminal and subscribe to a topic:
       ```bash
       mosquitto_sub -h localhost -t "test/topic"
       ```
     - Open another terminal and publish a message to the topic:
       ```bash
       mosquitto_pub -h localhost -t "test/topic" -m "Hello from MQTT"
       ```
     - The subscriber terminal should display the message `"Hello from MQTT"`.

---

#### **ESP8266/ESP32 with MQTT**:

1. **Install MQTT Libraries in Arduino IDE**:
   - Install the **PubSubClient** library from the Arduino Library Manager:
     - In Arduino IDE: `Sketch` → `Include Library` → `Manage Libraries`.
     - Search for **PubSubClient** and install it.

2. **Code for Sending and Receiving Messages Using MQTT**:

```cpp
#include <ESP8266WiFi.h>
#include <PubSubClient.h>

const char* ssid = "your_SSID";             // Your Wi-Fi network SSID
const char* password = "your_PASSWORD";     // Your Wi-Fi network password
const char* mqtt_server = "broker_address"; // MQTT broker address (e.g., localhost or IP)

WiFiClient espClient;
PubSubClient client(espClient);

void setup() {
  Serial.begin(115200);
  delay(10);

  // Connect to Wi-Fi
  WiFi.begin(ssid, password);
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to WiFi");

  // Setup MQTT client
  client.setServer(mqtt_server, 1883);  // Port 1883 is the default MQTT port
  client.setCallback(mqttCallback);

  // Connect to MQTT broker
  while (!client.connected()) {
    Serial.print("Attempting MQTT connection...");
    if (client.connect("ESP8266_Client")) {
      Serial.println("connected");
      // Subscribe to a topic
      client.subscribe("test/topic");
    } else {
      Serial.print("Failed, rc=");
      Serial.print(client.state());
      delay(5000);
    }
  }
}

void loop() {
  client.loop();  // Maintain connection to MQTT broker

  // Publish a message to the topic every 5 seconds
  if (client.connected()) {
    client.publish("test/topic", "Hello from ESP8266");
  }
  delay(5000);
}

void mqttCallback(char* topic, byte* payload, unsigned int length) {
  Serial.print("Message arrived on topic: ");
  Serial.println(topic);
  Serial.print("Message: ");
  for (int i = 0; i < length; i++) {
    Serial.print((char)payload[i]);
  }
  Serial.println();
}
```

---

#### **Explanation of the Code**:

- **Wi-Fi Connection**: 
  - The ESP8266 connects to the Wi-Fi network using the `WiFi.begin()` function.
  
- **MQTT Setup**:
  - The MQTT client is created using `PubSubClient` and connected to the MQTT broker using `client.connect()`. The broker address is provided as a string (can be a local IP or `localhost` if Mosquitto is running locally).
  
- **Publishing Messages**:
  - The `client.publish()` function sends messages to the topic `"test/topic"` every 5 seconds. These messages will be received by any subscriber to that topic.

- **Callback Function**:
  - The `mqttCallback()` function is called whenever a message is received from a subscribed topic. It prints the topic and message to the Serial Monitor.

---

#### **Testing the MQTT Communication**:

1. **Upload the Code to ESP8266**: Upload the code to your ESP8266 using the Arduino IDE.
2. **Monitor Messages**: 
   - Open the **Serial Monitor** to see the status of the MQTT connection.
   - You should see messages being sent from the ESP8266 to the topic `"test/topic"`.
3. **Subscribe with Mosquitto**: Use `mosquitto_sub` to subscribe to the same topic:
   ```bash
   mosquitto_sub -h localhost -t "test/topic"
   ```
4. **Check the Output**:
   - The messages sent from the ESP8266 (e.g., "Hello from ESP8266") should appear in the terminal where you subscribed to the topic.

---

### **Conclusion:**

- Understand the **MQTT protocol** and how it works in IoT communication.
- Set up and run an **MQTT broker** (Mosquitto) on a local machine.
- Be able to **send and receive MQTT messages** using the **ESP8266/ESP32**, demonstrating how IoT devices can interact with a central broker to share data.

**Optional Exercises**:
- Integrate more sensors and devices (e.g., temperature, humidity) to send data to the MQTT broker.
- Build a simple **IoT automation** system where one device triggers another device through MQTT messaging.

### **Day 14: Final Project and Review**

---

### **Theory:**

#### **Recap of All Key Concepts Covered**:
Over the past 13 days, we have explored a range of essential topics for building IoT solutions. Here's a quick summary of what was covered:

1. **Introduction to ESP32/ESP8266**: 
   - Basic hardware and software setup.
   - Key features of ESP32 (dual-core, Bluetooth, etc.) and how it compares to ESP8266.

2. **Analog Inputs/Outputs (ADC/DAC)**:
   - Working with analog signals using ADC (Analog to Digital Conversion) and DAC (Digital to Analog Conversion).
   - PWM (Pulse Width Modulation) for controlling devices like LEDs.

3. **Communication Protocols (Serial, SPI, I2C)**:
   - Overview and practical usage of Serial, SPI, and I2C protocols.
   - Interfacing I2C devices like sensors and LCD displays.

4. **Wi-Fi Configuration and HTTP**:
   - Setting up Wi-Fi on ESP8266/ESP32.
   - Sending and receiving data over HTTP.

5. **IoT Cloud Platforms (ThingSpeak)**:
   - Introduction to IoT cloud platforms and setting up ThingSpeak.
   - Sending sensor data to cloud platforms for real-time monitoring.

6. **Web Server on ESP32**:
   - Building a web server on ESP32 to control devices (LED) via a web interface.

7. **Bluetooth Communication**:
   - Introduction to Bluetooth Low Energy (BLE) and how to control devices using Bluetooth on ESP32.

8. **Automation with MQTT**:
   - Understanding MQTT protocol for lightweight messaging in IoT.
   - Sending and receiving messages between devices using MQTT brokers.

---

#### **How to Plan, Design, and Implement an IoT Project**:
An IoT project can be broken down into the following stages:

1. **Planning**:
   - Define the problem you're solving and the desired outcome (e.g., smart home system, environmental monitoring).
   - Identify the sensors and actuators needed.
   - Select the platform and communication protocols (e.g., Wi-Fi, Bluetooth, MQTT).

2. **Design**:
   - Create a **block diagram** of the IoT system (e.g., sensors, actuators, microcontroller, cloud/server).
   - Choose the right **IoT hardware** (e.g., ESP32, ESP8266, sensors like DHT11, gas sensor, etc.).
   - Select an **IoT platform** or cloud service for data storage and visualization (e.g., ThingSpeak, Firebase, AWS IoT).

3. **Implementation**:
   - Set up the **microcontroller** (e.g., ESP8266/ESP32) and interface it with sensors and actuators.
   - Implement the communication protocol (e.g., HTTP, MQTT, Bluetooth).
   - Connect the system to the **cloud** or local server for data storage and control.
   - Test the system for functionality and stability.

4. **Testing and Scaling**:
   - Test the system with real-world data.
   - Troubleshoot and ensure that all parts are working together smoothly.
   - **Scaling**: Once the system is functional, you can scale it by adding more sensors, expanding the network with more devices, and integrating complex features like machine learning or edge computing.

---

### **Practical:**

#### **Final Mini-Project**: Using ESP8266/ESP32 to Collect Data from a Sensor and Control an Actuator (LED or Relay)

**Objective**: 
- Build a simple IoT project where the ESP8266/ESP32 collects data from a sensor (e.g., temperature sensor, motion sensor) and controls an actuator (LED or relay) based on data or user input.

**Components**:
- ESP8266 or ESP32
- Temperature sensor (e.g., DHT11 or DHT22)
- LED or relay module
- Resistor (for LED)
- Jumper wires
- Breadboard

---

#### **Steps to Build the Mini-Project**:

1. **Hardware Setup**:
   - Connect the **DHT11/DHT22 sensor** to the ESP8266/ESP32 (VCC, GND, DATA pin).
   - Connect an **LED** to a GPIO pin of the ESP8266/ESP32, using a resistor in series with the LED.
   - Alternatively, you can use a **relay module** if you want to control higher-voltage devices.

2. **Software Setup**:
   - Install the required libraries in Arduino IDE: 
     - `DHT` library for temperature and humidity sensor.
     - `PubSubClient` for MQTT (if applicable).
   
   - **Write Code**: The code will perform the following tasks:
     - Read data from the sensor (e.g., temperature).
     - If the temperature exceeds a certain threshold, turn on the LED or activate the relay.
     - Send sensor data to a cloud platform (e.g., ThingSpeak) or display it on a local web server.

---

#### **Sample Code**:

```cpp
#include <ESP8266WiFi.h>
#include <DHT.h>

#define DHTPIN 2           // Pin connected to DHT sensor (GPIO2)
#define DHTTYPE DHT22      // DHT 22 (AM2302)
DHT dht(DHTPIN, DHTTYPE);

const char* ssid = "your_SSID";
const char* password = "your_PASSWORD";
const char* server = "api.thingspeak.com"; // ThingSpeak server

int LED_PIN = 5;  // GPIO pin for LED (D1 on NodeMCU)

WiFiClient client;

void setup() {
  Serial.begin(115200);
  pinMode(LED_PIN, OUTPUT);
  
  // Connect to Wi-Fi
  WiFi.begin(ssid, password);
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to WiFi");

  // Initialize the DHT sensor
  dht.begin();
}

void loop() {
  // Read temperature and humidity
  float temperature = dht.readTemperature();
  float humidity = dht.readHumidity();

  if (isnan(temperature) || isnan(humidity)) {
    Serial.println("Failed to read from DHT sensor!");
    return;
  }

  // Print data to Serial Monitor
  Serial.print("Temperature: ");
  Serial.print(temperature);
  Serial.print(" °C, Humidity: ");
  Serial.print(humidity);
  Serial.println(" %");

  // Control LED based on temperature
  if (temperature > 30) {
    digitalWrite(LED_PIN, HIGH);  // Turn on LED if temperature exceeds 30°C
  } else {
    digitalWrite(LED_PIN, LOW);   // Turn off LED
  }

  // Send data to ThingSpeak (if applicable)
  if (client.connect(server, 80)) {
    String postStr = "field1=" + String(temperature) + "&field2=" + String(humidity);
    client.print("POST /update HTTP/1.1\n");
    client.print("Host: " + String(server) + "\n");
    client.print("Connection: close\n");
    client.print("X-THINGSPEAKAPIKEY: your_API_key\n");
    client.print("Content-Type: application/x-www-form-urlencoded\n");
    client.print("Content-Length: " + String(postStr.length()) + "\n\n");
    client.print(postStr);
  }

  delay(10000); // Wait for 10 seconds before reading again
}
```

---

#### **Explanation of the Code**:

- **Wi-Fi Setup**: Connects the ESP8266 to the Wi-Fi network.
- **DHT Sensor**: Reads the temperature and humidity data from the DHT11/DHT22 sensor.
- **LED Control**: If the temperature exceeds 30°C, the LED is turned on, else it's turned off.
- **ThingSpeak Integration**: Sends the sensor data (temperature and humidity) to ThingSpeak for remote monitoring.

---

### **Overview of Scaling IoT Solutions and Integrating More Complex Systems**:

- **Adding More Sensors**: You can expand your IoT system by adding more sensors (e.g., motion sensors, light sensors, soil moisture sensors).
- **Cloud Integration**: Cloud platforms (e.g., AWS IoT, Google Cloud IoT) can be used to scale the system for handling larger data, better security, and real-time analytics.
- **Edge Computing**: Instead of sending data to the cloud continuously, you can process data at the edge (on the device) to reduce latency and bandwidth usage.
- **Security Considerations**: As IoT systems scale, it's important to implement security mechanisms like data encryption, secure communication, and authentication.

---

### **Conclusion**:
- **Recap** key IoT concepts learned throughout the course.
- **Plan, design, and implement** a basic IoT project.
- Gain hands-on experience with **sensor data collection**, **actuator control**, and **cloud integration**.
- Learn how to **scale IoT solutions** and explore further opportunities for more complex IoT systems.

---
---

### **Step 1: Blinking an LED**

#### **Board: Arduino Uno**
**Explanation**:
- The first project is a simple "Blink" program, which turns the onboard LED (or an external LED) on and off in a set interval.

```cpp
// Blink an LED on Arduino Uno

int ledPin = 13;  // Onboard LED pin (for Arduino Uno)

void setup() {
  pinMode(ledPin, OUTPUT);  // Set the LED pin as an output
}

void loop() {
  digitalWrite(ledPin, HIGH);  // Turn the LED on
  delay(1000);  // Wait for 1 second
  digitalWrite(ledPin, LOW);  // Turn the LED off
  delay(1000);  // Wait for 1 second
}
```
**Explanation**:
- **pinMode(ledPin, OUTPUT)**: This sets pin 13 (the onboard LED) as an output pin.
- **digitalWrite(ledPin, HIGH)**: Turns the LED on.
- **delay(1000)**: Waits for 1 second.
- **digitalWrite(ledPin, LOW)**: Turns the LED off.

---

#### **Board: NodeMCU (ESP8266)**

```cpp
// Blink an LED on NodeMCU (ESP8266)

int ledPin = 2;  // Onboard LED pin for NodeMCU (GPIO2)

void setup() {
  pinMode(ledPin, OUTPUT);  // Set the LED pin as an output
}

void loop() {
  digitalWrite(ledPin, HIGH);  // Turn the LED on
  delay(1000);  // Wait for 1 second
  digitalWrite(ledPin, LOW);  // Turn the LED off
  delay(1000);  // Wait for 1 second
}
```

**Explanation**:
- **GPIO2**: NodeMCU's onboard LED is typically connected to GPIO2. The pin number is different than Arduino, but the functionality remains the same.

---

#### **Board: ESP32**

```cpp
// Blink an LED on ESP32

int ledPin = 2;  // Onboard LED pin for ESP32 (GPIO2)

void setup() {
  pinMode(ledPin, OUTPUT);  // Set the LED pin as an output
}

void loop() {
  digitalWrite(ledPin, HIGH);  // Turn the LED on
  delay(1000);  // Wait for 1 second
  digitalWrite(ledPin, LOW);  // Turn the LED off
  delay(1000);  // Wait for 1 second
}
```

**Explanation**:
- **GPIO2**: Similar to NodeMCU, ESP32’s onboard LED is typically connected to GPIO2, so we use the same setup.

---

### **Step 2: Reading Temperature from DHT11 Sensor**

#### **Board: Arduino Uno**
**Explanation**:
- Reading temperature from the DHT11 sensor and displaying it on the Serial Monitor.

```cpp
#include <DHT.h>

#define DHTPIN 2  // Pin where the DHT11 is connected
#define DHTTYPE DHT11  // Define sensor type

DHT dht(DHTPIN, DHTTYPE);  // Initialize DHT sensor

void setup() {
  Serial.begin(9600);  // Start serial communication
  dht.begin();  // Initialize DHT sensor
}

void loop() {
  float temperature = dht.readTemperature();  // Read temperature in Celsius
  if (isnan(temperature)) {
    Serial.println("Failed to read from DHT sensor!");
  } else {
    Serial.print("Temperature: ");
    Serial.print(temperature);
    Serial.println(" °C");
  }
  delay(2000);  // Wait 2 seconds before reading again
}
```

**Explanation**:
- **DHT**: We include the DHT library to interact with the temperature sensor.
- **dht.readTemperature()**: Reads the temperature from the sensor.

---

#### **Board: NodeMCU (ESP8266)**

```cpp
#include <DHT.h>

#define DHTPIN 2  // Pin where the DHT11 is connected
#define DHTTYPE DHT11  // Define sensor type

DHT dht(DHTPIN, DHTTYPE);  // Initialize DHT sensor

void setup() {
  Serial.begin(9600);  // Start serial communication
  dht.begin();  // Initialize DHT sensor
}

void loop() {
  float temperature = dht.readTemperature();  // Read temperature in Celsius
  if (isnan(temperature)) {
    Serial.println("Failed to read from DHT sensor!");
  } else {
    Serial.print("Temperature: ");
    Serial.print(temperature);
    Serial.println(" °C");
  }
  delay(2000);  // Wait 2 seconds before reading again
}
```

**Explanation**:
- The setup and code structure are identical to the Arduino Uno version. The only difference is that for NodeMCU, the DHT sensor is connected to GPIO2 (but you can modify this based on your actual wiring).

---

#### **Board: ESP32**

```cpp
#include <DHT.h>

#define DHTPIN 4  // Pin where the DHT11 is connected
#define DHTTYPE DHT11  // Define sensor type

DHT dht(DHTPIN, DHTTYPE);  // Initialize DHT sensor

void setup() {
  Serial.begin(9600);  // Start serial communication
  dht.begin();  // Initialize DHT sensor
}

void loop() {
  float temperature = dht.readTemperature();  // Read temperature in Celsius
  if (isnan(temperature)) {
    Serial.println("Failed to read from DHT sensor!");
  } else {
    Serial.print("Temperature: ");
    Serial.print(temperature);
    Serial.println(" °C");
  }
  delay(2000);  // Wait 2 seconds before reading again
}
```

**Explanation**:
- The setup and code are very similar to the NodeMCU example. ESP32's pin for DHT11 might be different (GPIO4 in this case).

---

### **Step 3: Sending Data to ThingSpeak (IoT Cloud Platform)**

#### **Board: Arduino Uno**

```cpp
#include <WiFi.h>
#include <ThingSpeak.h>

const char *ssid = "your_SSID";
const char *password = "your_PASSWORD";
const char *myWriteAPIKey = "your_WRITE_API_KEY";
WiFiClient client;

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);  // Connect to Wi-Fi
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  ThingSpeak.begin(client);  // Initialize ThingSpeak client
}

void loop() {
  float temperature = analogRead(A0);  // Read temperature or sensor data
  ThingSpeak.writeField(1, temperature, myWriteAPIKey);  // Send data to ThingSpeak
  delay(15000);  // Wait 15 seconds
}
```

**Explanation**:
- **WiFi.begin**: Connects to Wi-Fi.
- **ThingSpeak.writeField**: Sends data to ThingSpeak platform.

---

#### **Board: NodeMCU (ESP8266)**

```cpp
#include <ESP8266WiFi.h>
#include <ThingSpeak.h>

const char *ssid = "your_SSID";
const char *password = "your_PASSWORD";
const char *myWriteAPIKey = "your_WRITE_API_KEY";
WiFiClient client;

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);  // Connect to Wi-Fi
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  ThingSpeak.begin(client);  // Initialize ThingSpeak client
}

void loop() {
  float temperature = analogRead(A0);  // Read temperature or sensor data
  ThingSpeak.writeField(1, temperature, myWriteAPIKey);  // Send data to ThingSpeak
  delay(15000);  // Wait 15 seconds
}
```

**Explanation**:
- The structure is the same as the Arduino Uno code. The only difference is that NodeMCU uses ESP8266, and Wi-Fi is handled through the **ESP8266WiFi.h** library.

---

#### **Board: ESP32**

```cpp
#include <WiFi.h>
#include <ThingSpeak.h>

const char *ssid = "your_SSID";
const char *password = "your_PASSWORD";
const char *myWriteAPIKey = "your_WRITE_API_KEY";
WiFiClient client;

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);  // Connect to Wi-Fi
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  ThingSpeak.begin(client);  // Initialize ThingSpeak client
}

void loop() {
  float temperature = analogRead(34);  // Read temperature or sensor data (GPIO34)
  ThingSpeak.writeField(1, temperature, myWriteAPIKey);  // Send data to ThingSpeak
  delay(15000);  // Wait 15 seconds
}
```

**Explanation**:
- The setup for ESP32 is very similar to NodeMCU, but you need to use the **WiFi.h** library. The GPIO pin for analog readings (e.g., GPIO34) can be different on ESP32.

---

---

### **Step 4: Building a Web Server on ESP8266/ESP32 to Control an LED**

In this step, we will set up a simple web server on the ESP8266 or ESP32 to control an LED using HTTP requests from a browser or mobile app.

#### **Board: NodeMCU (ESP8266)**

```cpp
#include <ESP8266WiFi.h>
#include <ESP8266WebServer.h>

const char *ssid = "your_SSID";
const char *password = "your_PASSWORD";
ESP8266WebServer server(80);  // Create web server object on port 80

int ledPin = 2;  // GPIO2 (Onboard LED pin)

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);  // Connect to Wi-Fi
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to WiFi");

  pinMode(ledPin, OUTPUT);  // Set LED pin as output

  // Define web server routes
  server.on("/", HTTP_GET, handleRoot);  // Handle root route
  server.on("/led/on", HTTP_GET, turnLedOn);  // Turn LED ON route
  server.on("/led/off", HTTP_GET, turnLedOff);  // Turn LED OFF route

  server.begin();  // Start the server
}

void loop() {
  server.handleClient();  // Handle client requests
}

void handleRoot() {
  server.send(200, "text/html", "<h1>ESP8266 Web Server</h1><a href='/led/on'>Turn LED ON</a><br><a href='/led/off'>Turn LED OFF</a>");
}

void turnLedOn() {
  digitalWrite(ledPin, HIGH);  // Turn the LED on
  server.send(200, "text/html", "<h1>LED is ON</h1><a href='/led/off'>Turn LED OFF</a>");
}

void turnLedOff() {
  digitalWrite(ledPin, LOW);  // Turn the LED off
  server.send(200, "text/html", "<h1>LED is OFF</h1><a href='/led/on'>Turn LED ON</a>");
}
```

**Explanation**:
- **ESP8266WebServer**: This library sets up the web server on the ESP8266.
- **server.on()**: Defines the routes. We have three routes here: `/`, `/led/on`, and `/led/off`.
- **server.send()**: Sends a response to the client, in this case, HTML content.

---

#### **Board: ESP32**

```cpp
#include <WiFi.h>
#include <WebServer.h>

const char *ssid = "your_SSID";
const char *password = "your_PASSWORD";
WebServer server(80);  // Create web server object on port 80

int ledPin = 2;  // GPIO2 (Onboard LED pin)

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);  // Connect to Wi-Fi
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to WiFi");

  pinMode(ledPin, OUTPUT);  // Set LED pin as output

  // Define web server routes
  server.on("/", HTTP_GET, handleRoot);  // Handle root route
  server.on("/led/on", HTTP_GET, turnLedOn);  // Turn LED ON route
  server.on("/led/off", HTTP_GET, turnLedOff);  // Turn LED OFF route

  server.begin();  // Start the server
}

void loop() {
  server.handleClient();  // Handle client requests
}

void handleRoot() {
  server.send(200, "text/html", "<h1>ESP32 Web Server</h1><a href='/led/on'>Turn LED ON</a><br><a href='/led/off'>Turn LED OFF</a>");
}

void turnLedOn() {
  digitalWrite(ledPin, HIGH);  // Turn the LED on
  server.send(200, "text/html", "<h1>LED is ON</h1><a href='/led/off'>Turn LED OFF</a>");
}

void turnLedOff() {
  digitalWrite(ledPin, LOW);  // Turn the LED off
  server.send(200, "text/html", "<h1>LED is OFF</h1><a href='/led/on'>Turn LED ON</a>");
}
```

**Explanation**:
- The code for ESP32 is very similar to the ESP8266 example. The only major change is using **WebServer** instead of **ESP8266WebServer**.
- The web page is served on port 80, and the LED can be controlled using HTTP requests like `/led/on` and `/led/off`.

---

### **Step 5: Connecting to the Internet and Making HTTP Requests**

Now, we will send HTTP requests from the ESP8266/ESP32 to an external web server (like a weather API) and display the results.

#### **Board: NodeMCU (ESP8266)**

```cpp
#include <ESP8266WiFi.h>
#include <ESP8266HTTPClient.h>

const char *ssid = "your_SSID";
const char *password = "your_PASSWORD";
const char *server = "http://api.openweathermap.org/data/2.5/weather?q=London&appid=your_API_KEY";  // Example weather API

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);  // Connect to Wi-Fi
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to WiFi");
}

void loop() {
  if (WiFi.status() == WL_CONNECTED) {
    HTTPClient http;  // Create an HTTPClient object
    http.begin(server);  // Specify the server URL
    int httpCode = http.GET();  // Send GET request to the server

    if (httpCode > 0) {
      String payload = http.getString();  // Get the response payload
      Serial.println(payload);  // Print the payload (JSON response)
    } else {
      Serial.println("Error in HTTP request");
    }
    http.end();  // End HTTP connection
  }
  delay(10000);  // Wait for 10 seconds before the next request
}
```

**Explanation**:
- **HTTPClient**: This library allows the ESP8266 to make HTTP requests.
- **http.begin()**: Initializes the HTTP connection to the server.
- **http.GET()**: Sends a GET request to the weather API.
- The response is printed to the Serial Monitor.

---

#### **Board: ESP32**

```cpp
#include <WiFi.h>
#include <HTTPClient.h>

const char *ssid = "your_SSID";
const char *password = "your_PASSWORD";
const char *server = "http://api.openweathermap.org/data/2.5/weather?q=London&appid=your_API_KEY";  // Example weather API

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);  // Connect to Wi-Fi
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to WiFi");
}

void loop() {
  if (WiFi.status() == WL_CONNECTED) {
    HTTPClient http;  // Create an HTTPClient object
    http.begin(server);  // Specify the server URL
    int httpCode = http.GET();  // Send GET request to the server

    if (httpCode > 0) {
      String payload = http.getString();  // Get the response payload
      Serial.println(payload);  // Print the payload (JSON response)
    } else {
      Serial.println("Error in HTTP request");
    }
    http.end();  // End HTTP connection
  }
  delay(10000);  // Wait for 10 seconds before the next request
}
```

**Explanation**:
- The code for ESP32 is very similar to ESP8266. The only major difference is the use of **WiFi.h** for ESP32 and **HTTPClient** for sending HTTP requests.

---

### **Step 6: Controlling a Relay Module via Web Server**

Now, let's control a relay module to turn on/off an appliance (like a light) through a web interface.

#### **Board: NodeMCU (ESP8266)**

```cpp
#include <ESP8266WiFi.h>
#include <ESP8266WebServer.h>

const char *ssid = "your_SSID";
const char *password = "your_PASSWORD";
ESP8266WebServer server(80);

int relayPin = 5;  // GPIO5 for relay control

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to WiFi");

  pinMode(relayPin, OUTPUT);

  server.on("/", HTTP_GET, handleRoot);  // Root page
  server.on("/relay/on", HTTP_GET, turnRelayOn);  // Turn relay ON
  server.on("/relay/off", HTTP_GET, turnRelayOff);  // Turn relay OFF

  server.begin();
}

void loop() {
  server.handleClient();
}

void handle

Root() {
  server.send(200, "text/html", "<h1>Relay Control</h1><a href='/relay/on'>Turn Relay ON</a><br><a href='/relay/off'>Turn Relay OFF</a>");
}

void turnRelayOn() {
  digitalWrite(relayPin, HIGH);  // Turn on relay
  server.send(200, "text/html", "<h1>Relay is ON</h1><a href='/relay/off'>Turn Relay OFF</a>");
}

void turnRelayOff() {
  digitalWrite(relayPin, LOW);  // Turn off relay
  server.send(200, "text/html", "<h1>Relay is OFF</h1><a href='/relay/on'>Turn Relay ON</a>");
}
```

---

#### **Board: ESP32**

```cpp
#include <WiFi.h>
#include <WebServer.h>

const char *ssid = "your_SSID";
const char *password = "your_PASSWORD";
WebServer server(80);

int relayPin = 5;  // GPIO5 for relay control

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to WiFi");

  pinMode(relayPin, OUTPUT);

  server.on("/", HTTP_GET, handleRoot);  // Root page
  server.on("/relay/on", HTTP_GET, turnRelayOn);  // Turn relay ON
  server.on("/relay/off", HTTP_GET, turnRelayOff);  // Turn relay OFF

  server.begin();
}

void loop() {
  server.handleClient();
}

void handleRoot() {
  server.send(200, "text/html", "<h1>Relay Control</h1><a href='/relay/on'>Turn Relay ON</a><br><a href='/relay/off'>Turn Relay OFF</a>");
}

void turnRelayOn() {
  digitalWrite(relayPin, HIGH);  // Turn on relay
  server.send(200, "text/html", "<h1>Relay is ON</h1><a href='/relay/off'>Turn Relay OFF</a>");
}

void turnRelayOff() {
  digitalWrite(relayPin, LOW);  // Turn off relay
  server.send(200, "text/html", "<h1>Relay is OFF</h1><a href='/relay/on'>Turn Relay ON</a>");
}
```

---

---

### **Step 7: Using MQTT Protocol for Communication Between Devices**

In this step, we will create a communication system between devices (e.g., ESP8266/ESP32) using the MQTT protocol. We will send sensor data from the device to an MQTT broker and control an actuator (LED/Relay) using MQTT commands.

#### **Board: NodeMCU (ESP8266)**

1. **Install the MQTT Library**: Use the `PubSubClient` library to handle MQTT communication.

2. **Setup Code**: The ESP8266 will connect to an MQTT broker (such as Eclipse Mosquitto) and send sensor data. We will also listen for commands to control an LED.

```cpp
#include <ESP8266WiFi.h>
#include <PubSubClient.h>

const char* ssid = "your_SSID";
const char* password = "your_PASSWORD";
const char* mqtt_server = "broker.hivemq.com"; // Public MQTT Broker
WiFiClient espClient;
PubSubClient client(espClient);

int ledPin = 2;  // GPIO2 (Onboard LED pin)
int sensorPin = A0;  // Analog sensor pin

void setup() {
  Serial.begin(115200);
  pinMode(ledPin, OUTPUT);
  WiFi.begin(ssid, password);
  
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to WiFi");

  client.setServer(mqtt_server, 1883);  // MQTT broker settings
  client.setCallback(callback);  // Set the callback function for incoming messages
}

void loop() {
  if (!client.connected()) {
    reconnect();
  }
  client.loop();  // Keep the connection alive
  
  // Publish sensor data every 10 seconds
  int sensorValue = analogRead(sensorPin);  // Read sensor data
  char sensorData[50];
  sprintf(sensorData, "Sensor Value: %d", sensorValue);
  client.publish("esp8266/sensor", sensorData);
  delay(10000);
}

void callback(char* topic, byte* payload, unsigned int length) {
  // Handle incoming messages and control the LED based on the message
  String message = "";
  for (int i = 0; i < length; i++) {
    message += (char)payload[i];
  }
  
  if (message == "LED_ON") {
    digitalWrite(ledPin, HIGH);
  } else if (message == "LED_OFF") {
    digitalWrite(ledPin, LOW);
  }
}

void reconnect() {
  while (!client.connected()) {
    Serial.print("Attempting MQTT connection...");
    if (client.connect("ESP8266Client")) {
      Serial.println("connected");
      client.subscribe("esp8266/led");  // Subscribe to the LED control topic
    } else {
      Serial.print("failed, rc=");
      Serial.print(client.state());
      delay(5000);
    }
  }
}
```

**Explanation**:
- **PubSubClient**: This is the MQTT client library for ESP8266.
- **client.setCallback()**: Defines a function to handle incoming MQTT messages.
- **client.publish()**: Sends the sensor data to the MQTT broker.
- **client.subscribe()**: Subscribes to a topic (`esp8266/led`) to receive commands for controlling the LED.

---

#### **Board: ESP32**

```cpp
#include <WiFi.h>
#include <PubSubClient.h>

const char* ssid = "your_SSID";
const char* password = "your_PASSWORD";
const char* mqtt_server = "broker.hivemq.com"; // Public MQTT Broker
WiFiClient espClient;
PubSubClient client(espClient);

int ledPin = 2;  // GPIO2 (Onboard LED pin)
int sensorPin = 34;  // GPIO34 (Analog sensor pin for ESP32)

void setup() {
  Serial.begin(115200);
  pinMode(ledPin, OUTPUT);
  WiFi.begin(ssid, password);

  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to WiFi");

  client.setServer(mqtt_server, 1883);  // MQTT broker settings
  client.setCallback(callback);  // Set the callback function for incoming messages
}

void loop() {
  if (!client.connected()) {
    reconnect();
  }
  client.loop();  // Keep the connection alive
  
  // Publish sensor data every 10 seconds
  int sensorValue = analogRead(sensorPin);  // Read sensor data
  char sensorData[50];
  sprintf(sensorData, "Sensor Value: %d", sensorValue);
  client.publish("esp32/sensor", sensorData);
  delay(10000);
}

void callback(char* topic, byte* payload, unsigned int length) {
  // Handle incoming messages and control the LED based on the message
  String message = "";
  for (int i = 0; i < length; i++) {
    message += (char)payload[i];
  }
  
  if (message == "LED_ON") {
    digitalWrite(ledPin, HIGH);
  } else if (message == "LED_OFF") {
    digitalWrite(ledPin, LOW);
  }
}

void reconnect() {
  while (!client.connected()) {
    Serial.print("Attempting MQTT connection...");
    if (client.connect("ESP32Client")) {
      Serial.println("connected");
      client.subscribe("esp32/led");  // Subscribe to the LED control topic
    } else {
      Serial.print("failed, rc=");
      Serial.print(client.state());
      delay(5000);
    }
  }
}
```

**Explanation**:
- The MQTT protocol on the ESP32 is implemented similarly to the ESP8266. The difference is mainly in the hardware-specific definitions (e.g., sensor pin).
- **WiFi.h** is used instead of **ESP8266WiFi.h** for the ESP32.

---

### **Step 8: Integrating a Sensor (e.g., DHT11/DHT22) to Send Data to MQTT**

Let’s extend our project by adding a temperature and humidity sensor (DHT11/DHT22) and sending the data to an MQTT broker.

#### **Board: NodeMCU (ESP8266)**

1. **Install DHT Sensor Library**: You need the `DHT` library to interface with the sensor.

2. **Setup Code**:

```cpp
#include <ESP8266WiFi.h>
#include <PubSubClient.h>
#include <DHT.h>

const char* ssid = "your_SSID";
const char* password = "your_PASSWORD";
const char* mqtt_server = "broker.hivemq.com"; // Public MQTT Broker
WiFiClient espClient;
PubSubClient client(espClient);

DHT dht(5, DHT22);  // DHT sensor is connected to GPIO5

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);
  
  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to WiFi");

  client.setServer(mqtt_server, 1883);
  client.setCallback(callback);

  dht.begin();
}

void loop() {
  if (!client.connected()) {
    reconnect();
  }
  client.loop();
  
  // Read temperature and humidity from DHT sensor
  float temperature = dht.readTemperature();
  float humidity = dht.readHumidity();
  
  // Publish the data
  char tempStr[10];
  char humStr[10];
  dtostrf(temperature, 1, 2, tempStr);
  dtostrf(humidity, 1, 2, humStr);
  
  client.publish("esp8266/temperature", tempStr);
  client.publish("esp8266/humidity", humStr);

  delay(2000);  // Send data every 2 seconds
}

void callback(char* topic, byte* payload, unsigned int length) {
  // Handle incoming messages
}

void reconnect() {
  while (!client.connected()) {
    Serial.print("Attempting MQTT connection...");
    if (client.connect("ESP8266Client")) {
      Serial.println("connected");
      client.subscribe("esp8266/led");
    } else {
      Serial.print("failed, rc=");
      Serial.print(client.state());
      delay(5000);
    }
  }
}
```

**Explanation**:
- **DHT sensor**: The DHT22 (or DHT11) sensor is used for measuring temperature and humidity.
- The sensor data is read using the `readTemperature()` and `readHumidity()` methods.
- The sensor data is then published to the MQTT broker, where other devices can subscribe to it.

---

#### **Board: ESP32**

The setup for ESP32 is similar to the ESP8266 example, with slight differences in hardware pin configuration and using the **WiFi.h** library.

```cpp
#include <WiFi.h>
#include <PubSubClient.h>
#include <DHT.h>

const char* ssid = "your_SSID";
const char* password = "your_PASSWORD";
const char* mqtt_server = "broker.hivemq.com"; // Public MQTT Broker
WiFiClient espClient;
PubSubClient client(espClient);

DHT dht(5, DHT22);  // DHT sensor is connected to GPIO5

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);
  
  while (WiFi.status() != WL_CONNECTED) {
    delay

(1000);
    Serial.println("Connecting to WiFi...");
  }
  Serial.println("Connected to WiFi");

  client.setServer(mqtt_server, 1883);
  client.setCallback(callback);

  dht.begin();
}

void loop() {
  if (!client.connected()) {
    reconnect();
  }
  client.loop();
  
  // Read temperature and humidity from DHT sensor
  float temperature = dht.readTemperature();
  float humidity = dht.readHumidity();
  
  // Publish the data
  char tempStr[10];
  char humStr[10];
  dtostrf(temperature, 1, 2, tempStr);
  dtostrf(humidity, 1, 2, humStr);
  
  client.publish("esp32/temperature", tempStr);
  client.publish("esp32/humidity", humStr);

  delay(2000);  // Send data every 2 seconds
}

void callback(char* topic, byte* payload, unsigned int length) {
  // Handle incoming messages
}

void reconnect() {
  while (!client.connected()) {
    Serial.print("Attempting MQTT connection...");
    if (client.connect("ESP32Client")) {
      Serial.println("connected");
      client.subscribe("esp32/led");
    } else {
      Serial.print("failed, rc=");
      Serial.print(client.state());
      delay(5000);
    }
  }
}
```

---

