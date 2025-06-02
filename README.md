# DHT22 Monitoring with ESP32

This project demonstrates how to use an ESP32 to monitor temperature and humidity using a DHT22 sensor and display the data on a web interface. The ESP32 serves as a web server, providing real-time updates of sensor readings.

## Features

- **Wi-Fi Connectivity**: Connects to a Wi-Fi network to serve the web interface.
- **DHT22 Sensor Integration**: Reads temperature and humidity data from the DHT22 sensor.
- **Web Interface**: Displays real-time temperature and humidity data on a webpage.
- **LED Control**: Blinks an LED with a frequency based on the temperature reading.

## Requirements

- ESP32 board
- DHT22 sensor
- LED
- Resistors and wires for connections

## Libraries Used

- `WiFi.h`: For Wi-Fi connectivity.
- `AsyncTCP.h`: For asynchronous TCP communication.
- `ESPAsyncWebServer.h`: For creating the web server.
- `DHT.h` and `Adafruit_Sensor.h`: For interfacing with the DHT22 sensor.

## Pin Configuration

- **DHT Sensor Pin**: Connected to GPIO 25.
- **LED Pin**: Connected to GPIO 2.

## Setup Instructions

1. **Install Libraries**:
    - Install the required libraries (`ESPAsyncWebServer`, `AsyncTCP`, `DHT`) in your Arduino IDE.

2. **Configure Wi-Fi**:
    - Replace `SSID_WIFI` and `WIFI_PASSWORD` with your Wi-Fi credentials in the code.

3. **Upload Code**:
    - Upload the provided code to your ESP32 using the Arduino IDE.

4. **Connect Hardware**:
    - Connect the DHT22 sensor to GPIO 25 and the LED to GPIO 2.

5. **Access Web Interface**:
    - After uploading the code, open the Serial Monitor to find the ESP32's IP address.
    - Open a browser and navigate to the IP address to view the web interface.

## How It Works

- The ESP32 reads temperature and humidity data from the DHT22 sensor every 2 seconds.
- The data is served via a web interface, which updates every 2 seconds using JavaScript.
- The LED blinks with a frequency based on the temperature reading.

## Notes

- Ensure the DHT22 sensor is properly connected and powered.
- The LED blinking frequency is mapped to the temperature range (15°C to 40°C).

## License

This project is MIT.
