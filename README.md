
[ANISMA Main Repository](https://github.com/augmented-human-lab/ANISMA) 
* [ANISMA Software](https://github.com/augmented-human-lab/ANISMA-software)
* [ANISMA Controller Board](https://github.com/augmented-human-lab/ANISMA-controller-board)
* **ANISMA Driver Board** <-- You are here!

# ANISMA Driver Board

This repository provides the Eagle Project files for the ANISMA Driver Board

The Driver Board connects to an Arduino Uno as controller board. They support eight output pins that are fully controlled and can be extended by adding more Driver Boards to an I2C bus system. We use a PCA9685 16-channel LED controller in combination with four MAX14874 dual-channel push-pull drivers in order to control the current flow using pulse-width-modulation (PWM) and dynamically set the polarity (VCC, GND, HIGH-Z) for each output pin. 

# How to get the board

Using the following link you can get direct access to the Gerber files and Bill of Materials (BOM): 
https://www.pcbway.com/project/shareproject/ANISMA_Driver_Board_3e5c784f.html

If you want you can purchase the board directly including assembly via PCBWay.

<a href="https://www.pcbway.com/project/shareproject/ANISMA_Driver_Board_3e5c784f.html"><img src="https://www.pcbway.com/project/img/images/frompcbway-1220.png" alt="PCB from PCBWay" /></a>


# Wiring

Wire the ANISMA Controller Board with the Arduino Uno as follows: 


| Arduino Uno | ANISMA Controller Board | Power Supply (9V Battery) |
|-------------|-------------------------|---------------------------|
| SCL         | SCL                     |                           |
| SDA         | SDA                     |                           |
| 5V          | 5V                      |                           |
| GND1        | GND                     |                           |
| GND2        |                         | -                         |
|             | VSS/12V/9V              | +                         |

![anisma wiring](https://user-images.githubusercontent.com/62531877/225809384-2a9c4176-21af-4df1-a093-90e84da6943f.png)

# Connecting your ANISMA skin deformation device to the ANISMA Driver Board
Now you can hook up your ANISMA devices to the driver board output pins. To see what pins of your ANISMA skin deformation device need to be connected to which driver board output pins, go to the Animate view in the ANISMA Software, make sure the Arduino Uno Controller Board is connected to your computer, and click "Replay with Controllerboard". Now at each node the pin number should be displayed to which to connect your device.
