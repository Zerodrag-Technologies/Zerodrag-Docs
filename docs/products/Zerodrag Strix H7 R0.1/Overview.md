# **ZERODRAG STX H7**

The **ZERODRAG STX H7** is a high-performance flight controller developed for next-generation UAV platforms. Powered by the **STM32H743** running at 480 MHz, it delivers exceptional computational capacity for advanced navigation, sensor fusion, and autonomous applications. Its architecture emphasizes **precision sensing and reliability**, featuring dual ICM42688P IMUs, an Infineon DPS310 barometer, and dedicated low-noise power domains.  

With a **30.5 × 30.5 mm standard mounting format**, the STX H7 integrates seamlessly into industry-standard airframes. It offers flexible connectivity through plug-and-play connectors and solder pads, while supporting leading open-source firmware, including **Ardupilot**, **PX4**, **Betaflight**, and **INAV**.

---

## Key Features

- **High-Performance MCU** — STM32H743 @ 480 MHz for advanced flight control and navigation.  
- **Redundant IMU System** — Dual ICM42688P accelerometer/gyroscopes for robust flight data and fault tolerance.  
- **Integrated OSD** — AT7456E for real-time FPV video overlay.  
- **Noise-Isolated Power Supply** — Dedicated low-noise rails for MCU, sensors, and OSD, ensuring clean data and stable performance.  
- **UAVCAN Interface** — Native UAVCAN support for next-generation peripheral integration.  
- **Blackbox Logging** — MicroSD card slot for high-speed flight data recording.  
- **Flexible Power Architecture** — Up to 36 V DC input with onboard 5 V / 2.5 A and 12 V / 2.5 A rails.  
- **Pit Mode on 12 V** — Controlled power switching for VTX management and safety.  

---

## Specifications

**Processor & Storage**  
- MCU: **STM32H743** @ 480 MHz  
- Onboard Blackbox: **MicroSD card slot**  
- OSD: **AT7456E**  

**Sensors**  
- IMU: **2 × ICM42688P** (accelerometer & gyroscope)  
- Barometer: **Infineon DPS310**  

**Power**  
- Input Voltage: **Up to 36 V DC**  
- 5 V Rail: **2.5 A max**  
- 12 V Rail: **2.5 A max**  

**Connectivity**  
- **UARTs:** 7 full ports  
- **I²C:** 2 ports  
- **PWM Outputs:** 12 channels + 1 LED output  
- **CAN:** 1 port (UAVCAN compatible)  
- **ADC:** 6 inputs  
- **USB:** 1 × USB Type-C  
- **PIO:** 1 + dedicated pit control  

**Physical**  
- Mounting: **30.5 × 30.5 mm**  
- Dimensions: **37 × 38.5 × TBD mm**  
- Weight: **TBD**  

**Additional**  
- Plug-and-play connectors alongside solder pads  
- Full MCU breakout available  
- Dedicated low-noise power supply for sensors, OSD, and MCU  
- Pit mode control on 12 V supply  
- Multi-firmware support: **Ardupilot, PX4, Betaflight, INAV**  

---