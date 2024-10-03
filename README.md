# Sketchetron: Merging Robotics and Art

## Introduction

**Sketchetron** is a unique fusion of technology and creativity. It seeks to create an autonomous robot capable of producing original two-dimensional artwork on paper without the need for human intervention. This project is a testament to the possibilities of combining engineering with artistic expression, transforming mechanical precision into creative output.

## Project Goals

The main goal of the **Sketchetron** project is to build a robot that can autonomously create art. By leveraging engineering and design, Sketchetron will not only draw basic shapes but also replicate logos and even generate sketches from given images. 

### Phases of the Project

- **Phase 1**: Drawing basic geometric shapes on an A3 sheet.
- **Phase 2**: Reproducing the Robotics Club logo within a 15cm x 15cm area.
- **Phase 3**: Sketching an image provided on the spot.

## Components Required

The build includes the following essential components:

- **Motors & Movement**:
  - 2 NEMA 17 Stepper Motors
  - 4 8mm Smooth Rods (two at 400mm, two at 320mm)
  - 8 LM8UU Bearings
  - 2 GT2 20-tooth Pulleys
  - 10 F623ZZ Bearings
  - 1 GT2 Belt (1.4m long)

- **Frame & Support**:
  - 2 M10 Threaded Rods (400mm each)
  - 8 M10 Nuts
  - Various M3 Screws, Nuts, and Washers

- **Electronics**:
  - 1 Arduino UNO
  - 1 CNC Shield
  - 1 SG90 Micro Servo (with 250mm extension cable)
  - 1 12V 2A Power Supply
  - 1 USB Cable

- **Drawing Mechanism**:
  - 1 Pen Holder

## Assembly Instructions

1. **Construct the Frame**:
   - Begin by inserting LM8UU bearings into the smooth rods, which are then fixed to the motor support frame.
   - Attach the NEMA 17 motors to the frame with M3 screws.

2. **Set Up the Movement System**:
   - Install the GT2 pulleys on the motors and insert the GT2 belt.
   - Attach the servo motor and pen holder to the moving carriage.

3. **Electronic Setup**:
   - Mount the Arduino UNO and CNC Shield to the frame.
   - Connect the power supply, motors, and servo.

4. **Final Assembly**:
   - Ensure the pen holder is correctly installed and all components are properly secured for smooth operation.

## Software Configuration

### Installing GRBL Firmware

The robot is powered by a customized version of the **GRBL** firmware. This modified version supports servo control, allowing the pen to be lifted and lowered when required. GRBL drives the stepper motors and ensures precise drawing commands.

### Installation Steps

1. **Upload GRBL to Arduino UNO**: Use the Arduino IDE to upload the GRBL firmware.
2. **Vector Drawing with Inkscape**: Inkscape is a powerful, free vector graphic software used to design images and create the necessary G-code.
3. **Sending Commands via Universal Gcode Sender**: This Java-based tool sends the G-code to the Arduino, instructing the robot to execute the drawing.

### Calibration

To ensure accurate drawing, it's important to calibrate the machine:

1. Open the **Universal Gcode Sender** and use the terminal to check the current firmware settings by typing `$$`.
2. Check parameters **$100** (X-axis steps per mm) and **$101** (Y-axis steps per mm).
3. Adjust these values to **80** (for a 200-step motor and a 20-tooth pulley with a 2mm pitch GT2 belt) by typing `$100=80` and `$101=80`.
4. Once calibrated, the robot will produce drawings that match the dimensions set in Inkscape.

## Enhancements for the Future

- **Wireless Functionality**: Integrating Bluetooth for remote control.
- **Artificial Intelligence**: Leveraging AI to generate more dynamic and intelligent drawings.
- **Advanced Artistic Features**: Experimenting with color blending, shading, and other techniques to improve the quality of sketches.

## Conclusion

**Sketchetron** demonstrates the fascinating intersection of robotics and art, pushing the boundaries of autonomous systems. This project showcases how machines can be used creatively, transforming mechanical movements into artistic expression. 


