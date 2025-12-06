# Thermometer

A digital thermometer system designed to detect human body temperature using embedded C programming. The system includes an audible alert that activates when temperature exceeds 40°C (104°F), notifying concerned staff of potentially dangerous fever levels.

## Features

- **Temperature Monitoring**: Real-time body temperature measurement using ADC (Analog to Digital Converter)
- **Visual Display**: Four-digit seven-segment display showing temperature with one decimal place precision
- **Audio Alert**: Buzzer alarm activates when temperature exceeds 40°C
- **Temperature Range**: Measures up to 500°C (though optimized for body temperature detection)

## Technologies Used

- **Programming Language**: Embedded C (mikroC PRO for PIC)
- **Microcontroller**: PIC microcontroller
- **Simulation Software**: Proteus Design Suite
- **Development Board**: EasyPIC v7 Development Board
- **Hardware Components**:
  - Temperature sensor (Analog input on RB0)
  - Seven-segment display (4-digit, common cathode)
  - Buzzer (connected to RC2)

## Hardware Configuration

- **Port A (LATA)**: Seven-segment display multiplexing control
- **Port B (RB0)**: Analog input for temperature sensor
- **Port C (RC2)**: Buzzer output
- **Port D**: Seven-segment display data output

## How It Works

1. The ADC reads the analog temperature sensor value (10-bit resolution)
2. The value is converted to temperature: `Temperature = (ADC_value / 1024) × 500`
3. Temperature is displayed on four seven-segment displays
4. If temperature exceeds 40°C, the buzzer activates

## Circuit Diagram

![Thermometer Circuit](https://github.com/emansarahafi/Thermometor/assets/85173630/2117b761-0331-495b-a70f-962b79703351)

## Project Files

- `Thermometer.c` - Main source code in C
- `Thermometer.asm` - Generated assembly code
- `proteus/Thermometer.pdsprj` - Proteus simulation project
- Various mikroC project files (.mcppi, .cfg, etc.)

## Setup and Usage

1. Open `Thermometer.mcppi` in mikroC PRO for PIC
2. Build the project to generate hex file
3. Open `proteus/Thermometer.pdsprj` in Proteus
4. Load the generated hex file into the microcontroller in Proteus
5. Run the simulation

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
