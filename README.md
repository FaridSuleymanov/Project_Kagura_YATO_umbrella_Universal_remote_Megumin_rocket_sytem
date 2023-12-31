# Project Kagura, YATO-umbrella system and Project Megumin

This repository contains the source code for the Project Kagura, YATO-umbrella system, and Project Megumin. The system is composed of three main components: the Kagura system, the YATO-umbrella system, a transmitter controller that communicates with both systems, and the Project Megumin which is focused on controlling the vector thrust of a solid fuel rocket engine.

## Kagura System

The Kagura system is a motorized device that uses an MPU6050 sensor for motion detection and control. It uses an RF24 radio module for wireless communication. The system also controls a set of lights and an alarm, both of which can be toggled on and off.

The Kagura system is controlled by a joystick. The joystick's X and Y positions are mapped to the movement of the motors. The system also uses the MPU6050 sensor to adjust the speed of the motors based on the tilt angle of the device.

The code for the Kagura system is contained in the file `mobilized_platform_test_code.ino`.

## YATO-umbrella System

The YATO-umbrella system is a device that uses stepper motors for movement. It also uses an RF24 radio module for wireless communication. The system controls a camera relay and a servo trigger.

The YATO-umbrella system is also controlled by a joystick. The joystick's X and Y positions are mapped to the movement of the stepper motors. The system also uses a button to control the servo trigger.

The code for the YATO-umbrella system is contained in the file `receiver_test_code.ino`.

## Project Megumin

Project Megumin is focused on controlling the vector thrust of a solid fuel rocket engine. The system uses two servos to control the two axes of the vector thrust control. An MPU6050 sensor is used to measure the forces acting on the rocket, and an Arduino Nano is used to calculate how far to move the servo in order for the rocket to move upwards in a stabilized manner, controlled only by the thrust vector control (TVC).

The code for the Project Megumin is contained in the file `rocket_stabilization_test_code.ino`.

## Transmitter Controller

The transmitter controller is a device that sends control signals to both the Kagura and YATO-umbrella systems. It uses an RF24 radio module for wireless communication. The controller has a joystick and a button for user input. The joystick's X and Y positions and the button state are sent to the Kagura and YATO-umbrella systems.

The transmitter controller also has an OLED display that shows a bitmap image.

The code for the transmitter controller is contained in the file `transmitter_for_mobilized_platform_and_turret_test_code.ino`.

## Installation

1. Clone the repository to your local machine.
2. Open the `.ino` files in the Arduino IDE.
3. Connect your Arduino board to your computer.
4. Select the correct board and port in the Arduino IDE.
5. Upload the code to your Arduino board.

## Usage

Use the joystick and button on the transmitter controller to control the Kagura and YATO-umbrella systems. The joystick controls the movement of the motors, and the button toggles the lights and alarm on the Kagura system and the servo trigger on the YATO-umbrella system.

## Dependencies

This project uses the following libraries:

- `Wire.h`
- `SPI.h`
- `nRF24L01.h`
- `RF24.h`
- `MPU6050_tockn.h`
- `CytronMotorDriver.h`
- `Adafruit_GFX.h`
- `Adafruit_SSD1306.h`
- `ezButton.h`
- `I2Cdev.h`
- `MPU6050_6Axis_MotionApps20.h`
- `Servo.h`

Make sure to install these libraries in the Arduino IDE before running the code.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the GNU General Public License v3.0 - see the `LICENSE` file for details.
