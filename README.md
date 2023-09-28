# SE20UARI071_Sensor

## Team Members

SE20UARI071-J.Revanth Kumar

SE20UARI036 -B.Abhiram

SE20UARI081 -K.Harshith

SE20UARI166 - K.Vishnu Vardhan

## Raspberry Pi Temperature and Humidity Sensor Project

![__1__](https://github.com/revanthjavvaji/SE20UARI071_Sensor/assets/114976742/fa69d969-3c5a-47f1-b91d-f45c033e12fd)

DHCT11 Sensor

### Applications
HVAC, dehumidifiers, testing and inspection equipment, consumer goods, automotive,
automation, data loggers, weather stations, home appliances, humidity regulator, medical and other
relevant humidity measurement and control.

### Product Highlights
Low-cost, long-term stability, relative humidity and temperature measurement, excellent quality,
fast response, anti-interference ability, long distance signal transmission, the digital signal output,
precise calibration.

### Parameters
Relative Humidity

Resolution：16Bit

Repeatability：±1%RH

Accuracy：25℃ ±5%RH

Interchangeability：Fully interchangeable

Response time：1/e (63%)25℃ 6s

1m/s Air 6s

Hysteresis：<±0.3%RH

Long-term stability：<±0.5%RH/yr

Temperature

Resolution：16Bit

Repeatability：±1℃

Accuracy：25℃ ±2℃

Response time：1/e (63%) 10S

Electrical Characteristics

Power supply：DC 3.3～5.5V


Supply current：Measure 0.3mA Standby 60μA
Sampling period：Secondary Greater than 2 seconds

### Pin Description
1. VDD supply 3.3 ~ 5.5V DC
2. DATA serial data, single-bus
3. NC NC
4. GND grounding, power negative

![image](https://github.com/revanthjavvaji/SE20UARI071_Sensor/assets/114976742/3df6ae88-d6e2-42bf-9bbf-38cdc7b74a19)

RaspBerryPI

### Specifications

Broadcom BCM2711, Quad core Cortex-A72 (ARM v8) 64-bit SoC @ 1.8GHz

1GB, 2GB, 4GB or 8GB LPDDR4-3200 SDRAM (depending on model)

2.4 GHz and 5.0 GHz IEEE 802.11ac wireless, Bluetooth 5.0, BLE

Gigabit Ethernet

2 USB 3.0 ports; 2 USB 2.0 ports.

Raspberry Pi standard 40 pin GPIO header (fully backwards compatible with previous boards)

2 × micro-HDMI® ports (up to 4kp60 supported)

2-lane MIPI DSI display port

2-lane MIPI CSI camera port

4-pole stereo audio and composite video port

H.265 (4kp60 decode), H264 (1080p60 decode, 1080p30 encode)

OpenGL ES 3.1, Vulkan 1.0

Micro-SD card slot for loading operating system and data storage

5V DC via USB-C connector (minimum 3A*)

5V DC via GPIO header (minimum 3A*)

Power over Ethernet (PoE) enabled (requires separate PoE HAT)

Operating temperature: 0 – 50 degrees C ambient

## Setting Up a Raspberry Pi for Temperature and Humidity Data Collection

### Prerequisites
- Raspberry Pi (any model with GPIO pins)
- DHT11 temperature and humidity sensor
- MicroSD card with an installed OS
- Internet connection for package installation
- Jumper wires for connections
- Powerbank for Raspberry Pi power supply

### Installation

**Step 1: Install VNC Viewer**
Begin by installing VNC Viewer on your computer. This will allow you to remotely access the Raspberry Pi's graphical interface.

1. Visit the official VNC Viewer website [VNC Viewer Downloads](https://www.realvnc.com/en/connect/download/viewer/).
2. Download and follow the installation instructions tailored to your operating system.

**Step 2: Raspberry Pi Initial Setup**
Ensure that your Raspberry Pi is up and running with the Raspbian OS.

**Step 3: Flash the MicroSD Card**
1. Obtain the Raspbian OS image from the official Raspberry Pi website [Raspberry Pi Downloads](https://www.raspberrypi.org/software/operating-systems/).
2. Use a tool like Etcher to flash the Raspbian OS image onto your microSD card.
3. Insert the microSD card into your Raspberry Pi.

**Step 4: Connect the DHT11 Sensor**
Make the following connections between the DHT11 sensor and the Raspberry Pi using jumper wires:

- VCC (Power): Connect to the Raspberry Pi's 3.3V pin.
- Data: Connect to any GPIO pin (for example, we used pin 23).
- GND (Ground): Connect to a ground (GND) pin on the Raspberry Pi.

**Step 5: Power On the Raspberry Pi**
Ensure your Raspberry Pi is powered off, then insert the microSD card with the Raspbian OS. Power on the Raspberry Pi.

**Step 6: Enable GPIO on Raspberry Pi**
Access the Raspberry Pi configuration tool:

- Navigate to "Interfacing Options" and activate "GPIO."

**Step 7: Install Required Software**
Execute the following commands to update package lists and install the necessary Python library for the DHT11 sensor:

```shell
sudo apt-get update
sudo python get-pip
```
**Step 8: Python Code**
Create a Python script (e.g., `Adafruit.py`) to read data from the DHT11 sensor. You can use the sample code provided in the project repository as a reference.

**Step 9: Running the Python Script**
Run your Python script to collect temperature and humidity data from the sensor. Monitor the console output for the data readings.

**Step 10: Optional - Data Storage**
If desired, modify your Python script to save the collected data in a file, database, or upload it to a cloud service for further analysis.

## Setting Up Firebase for Data Storage

### Creating a Firebase Account and Project
Follow these steps to create a Firebase account, set up a new project, and generate a service account key.

**Step 1: Sign in to Firebase**
Visit the [Firebase website](https://firebase.google.com/) and log in to your existing Firebase account.

**Step 2: Create a New Project**
Create a new project by clicking the "+ Add project" button and follow the on-screen instructions. You can choose any name for your project.

**Step 3: Access Project Configuration**
After successfully creating the project, you'll be redirected to the project configuration page.

**Step 4: Generating a Service Account Key**
- Go to "Service Accounts" in the Firebase Console by opening the "Settings" menu.
- Generate a new private key by clicking on "Generate New Private Key" and confirm the action by clicking "Generate Key."

We have successfully created a Firebase account, set up a project, and generated a private key for the service account. This key will be used to authenticate and interact with Firebase services from application. Data collected in Firebase

![Link](https://test-dht11-7b85f-default-rtdb.firebaseio.com/)


![image](https://github.com/revanthjavvaji/SE20UARI071_Sensor/assets/114976742/17efe3de-8007-4ac0-b66b-8b0605aec382)


![image](https://github.com/revanthjavvaji/SE20UARI071_Sensor/assets/114976742/f8a67fdd-718e-404d-9823-4f57d83a5ec1)






