# NeoPixel-LED-Control-with-ESP32-and-Firebase
This project demonstrates how to interface NeoPixel LEDs with an ESP32 microcontroller, enabling remote control through a mobile application using Firebase as the backend. The application allows users to change colors, patterns, and effects of the NeoPixel strip in real-time.
# Aim
To interface the ESP 32 with Neo pixel Led Controll It using An Appcication 
# components 
* Esp 32
* NEO pixel Led
## connection 
![neo](https://github.com/user-attachments/assets/5af56533-9bc9-4f82-9edc-e84e66a45650)
## pins
* GND ----> GND(Esp32)
* VCC ----> 5v
* DATA ----> pins 13
# Procedure
1. Create a Esp32 Project On Visual Studio Code With Arduino FrameWork
2. Interface Esp32 microcontroller with Neo pixel and do an Example code
    * lib_deps = adafruit/Adafruit NeoPixel@^1.12.3
3. Create a Firebase Project For Read the RealTime Data
4. Collect The network credentials, URL database, and project API key ,Email ,Password
5. Install the Firebase-ESP-Client Library.Then, program the Esp32 to Interface with Firebase
    * Library ---> lib_deps = mobizt/Firebase Arduino Client Library for ESP8266 and ESP32@^4.4.14
6. Insert your network credentials To the project work.
# Reference code 
```
#include <Adafruit_NeoPixel.h>
#ifdef __AVR__
  #include <avr/power.h>
#endif
#define PIN        13
#define NUMPIXELS  10

Adafruit_NeoPixel pixels(NUMPIXELS, PIN, NEO_GRB + NEO_KHZ800);
#define DELAYVAL 200

void setup()
{
  pixels.begin();
}

void loop()
{
  pixels.clear();

  for(int i=0; i<NUMPIXELS; i++)
  {
    pixels.setPixelColor(i, pixels.Color(0, 150, 0));
    pixels.show();
    delay(DELAYVAL);
  }
}
```
# OUTPUT
![VideoCapture_20241016-122346](https://github.com/user-attachments/assets/447a3973-313c-44d5-ab88-38b90b603d0c)
![VideoCapture_20241016-122350](https://github.com/user-attachments/assets/ae4b9c4e-f5a9-4266-9013-e58177a34790)
![VideoCapture_20241016-122353](https://github.com/user-attachments/assets/1171dadf-034f-4191-a17a-c9ae754a1781)

