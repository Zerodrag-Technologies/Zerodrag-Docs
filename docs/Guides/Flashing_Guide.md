# STM32 Flight Controller Flashing Guide

This document provides a step-by-step procedure to perform a clean firmware flash on STM32-based flight controllers. It applies regardless of whether firmware is currently present on the device.

---

## Pre-Requisites

### Hardware
- USB Type-C cable  
	- Please ensure the cable used has data capabilities
- STM32-based flight controller  

### Software
- [STM32Cube Programmer](https://www.st.com/en/development-tools/stm32cubeprog.html) (latest version recommended)  

---

## Procedure

### 1. Enter Bootloader Mode (DFU Mode)

1. Ensure the flight controller is powered off.  
2. Press and hold the **BOOT** button.  
3. While holding the button, connect the flight controller to the host PC via USB-C.  
4. The device should power on without LED activity.  

**Verification:**  
- In Windows Device Manager, the device should be enumerated as **STM32 BOOTLOADER** under USB devices.  
- If not detected, confirm driver installation and repeat the procedure.  

---

### 2. Connect with STM32Cube Programmer

1. Launch **STM32Cube Programmer**.  
2. In the connection mode dropdown (upper right), select **USB**.  
3. Confirm that **USB1** is displayed in the port field.  
4. Click **Connect**.  
   - Device information (chip ID, memory size) should be displayed in the log window.  

---

### 3. Load Firmware Image

1. Click the **Open File** icon.  
2. Select the required firmware image:  
   - **Ardupilot** (`.hex`)  
   - **Betaflight** (`.hex`)  
   - **INAV** (`.hex`)  
   - **PX4** (`.bin`)  

---

### 4. Erase and Program Device

1. Navigate to the **Erasing & Programming** section.  
2. Execute **Full Chip Erase** to remove any existing firmware.  
3. Under **Download**, select the firmware image.  
4. Click **Start Programming**.  
   - Progress will be indicated in the status bar.  
   - Upon completion, confirmation will be displayed in the log.  

---

### 5. Reboot the Device

1. Disconnect the USB cable.  
2. Power cycle the flight controller.  
3. Verify that the device boots with the newly installed firmware. LED indicators should correspond to the expected behavior of the selected firmware.  

---

## Completion

The STM32 flight controller is now flashed and ready for configuration through the respective ground control or configuration software.  

## Troubleshooting

### Device Not Detected in DFU Mode
- Confirm that the **BOOT** button was pressed before USB connection.  
- Ensure USB drivers for STM32 DFU are installed.  
- Try a different USB port or cable.  
- Check Device Manager → the device should appear as **STM32 BOOTLOADER**.  

### Connection Failure in STM32Cube Programmer
- Reconfirm the board is in DFU mode.  
- Verify that **USB** is selected as the connection interface.  
- If the port field does not display **USB1**, reinstall STM32Cube Programmer and drivers.  

### Flashing Errors
- Perform a **Full Chip Erase** before programming.  
- Confirm that the selected firmware image is compatible with the target hardware.  
- Retry programming after reconnecting the device in DFU mode.  

### Device Does Not Boot After Flash
- Ensure the correct firmware target (Ardupilot, Betaflight, INAV, PX4) was used.  
- Reflash using a verified firmware build.  
- If the issue persists, repeat the flashing process after a full erase.  

### USB Not Detected After Successful Flash
- In some cases, the flight controller may not be recognized immediately after flashing.  
- **Disconnect and reconnect the USB cable** to force re-enumeration.  
- If still not detected, power cycle the device and verify firmware installation.  