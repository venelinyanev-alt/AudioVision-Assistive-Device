# AudioVision-Assistive-Device
An open-source assistive device for the visually impaired using ESP32 and AI.
# AudioVision: ESP32-Based Assistive Device for the Visually Impaired

Project Overview
An open-source assistive device that uses computer vision and AI to help visually impaired individuals navigate their environment. The device describes the world around them through audio feedback.

Hardware Architecture
Master Unit: ESP32-S3 development board (handles user interaction, AI communication, and audio output)

Vision Unit: ESP32-CAM module (captures high-quality images based on master commands)

Communication: High-speed SPI interface between Master and Vision units for minimal latency

Audio: INMP441 I2S microphone for wake-word detection and MAX98357A I2S amplifier for clear speech output

Display: I2C OLED display (SSD1306) for settings configuration and system status feedback

Key Features
Voice-controlled operation with wake-word detection

Real-time image capture and AI-based description

Audio feedback through high-quality speech synthesis

Visual interface for configuration and status monitoring

Offline functionality for basic commands

Privacy-focused design

Display Functionality
The I2C OLED display provides:

⚙️ System configuration menu

🔋 Battery status indicator

📶 Wi-Fi connection status

🎤 Voice activation status

🔍 AI processing status

ℹ️ System information and debug messages

Software Architecture
Master-Slave Communication: Custom SPI protocol for efficient image transfer

AI Integration: Designed to work with Xiaozhi AI vision API for image description

Voice Interface: Wake-word detection and Text-to-Speech (TTS) functionality

Display Interface: I2C communication with OLED for user feedback

Hardware Connections
ESP32-S3 Master Unit Connections:
I2S Microphone (INMP441):

WS → GPIO 4

SCK → GPIO 5

SD → GPIO 6

I2S Amplifier (MAX98357A):

DIN → GPIO 7

BCLK → GPIO 15

LRC → GPIO 16

I2C OLED Display (SSD1306):

SDA → GPIO 41

SCL → GPIO 42

SPI to ESP32-CAM:

SCK → GPIO 36

MISO → GPIO 37

MOSI → GPIO 35 (optional)

CS → GPIO 48

Goals
Create affordable, reliable assistive technology

Open design for community improvement

Privacy-focused (no cloud dependency for core functionality)

Easy to assemble and configure

Extensible platform for future enhancements

Target Users
Visually impaired individuals

Rehabilitation centers

Accessibility technology researchers

STEM education programs

License
MIT License - see LICENSE file for details.

Contributing
We welcome contributions from developers, designers, and accessibility experts. Please see our contribution guidelines for more information.

Support
For technical support and questions, please open an issue in this repository or contact our development team.

