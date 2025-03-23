# RootMaster: Android Rooting Tool

Developed by @rxdsec

RootMaster is a comprehensive C++ command-line tool designed to simplify the process of rooting Android devices. It provides a unified interface for unlocking bootloaders, flashing custom recovery images, and installing superuser access across multiple device manufacturers.

## Features

- **Bootloader Unlocking**: Automated bootloader unlocking for supported devices
- **Custom Recovery Installation**: Flash custom recovery images like TWRP
- **Superuser Installation**: Install Magisk or SuperSU for root access
- **Auto-Download**: Automatically download recovery images and Magisk installers
- **Multi-Device Support**: Built-in profiles for various manufacturers (Pixel, Samsung, Xiaomi/Redmi, Oppo, Vivo, Realme, OnePlus, Tecno, Infinix, and more)
- **Safety Checks**: Verification procedures to prevent bricking devices
- **Manufacturer-Specific Methods**: Optimized rooting techniques for different device families

## Prerequisites

Before using RootMaster, ensure you have the following:

1. **ADB and Fastboot** installed on your system
2. **USB Debugging** enabled on your Android device
3. **OEM Unlocking** enabled in Developer Options (if applicable)
4. **Backed up** all important data on your device (rooting may cause data loss)

## Building from Source

```bash
# Clone the repository
git clone https://github.com/rxdsec634/rootmaster.git
cd rootmaster

# Create build directory
mkdir -p build && cd build

# Configure and build
cmake ..
make
```

## Usage

### Basic Command Syntax

```
./bin/rootmaster <command> [options]
```

### Available Commands

- `detect` - Detect connected Android devices
- `info` - Display detailed information about connected devices
- `download` - Download recovery images and Magisk installer
- `unlock` - Unlock the bootloader of a device
- `flash` - Flash a custom recovery image
- `root` - Install superuser access (Magisk)
- `auto` - Perform complete rooting process automatically
- `help` - Display help information

### Command Examples

#### Detect Connected Devices
```
./bin/rootmaster detect
```

#### Display Detailed Device Information
```
./bin/rootmaster info
```

#### Download Recovery and Magisk
```
./bin/rootmaster download
```

#### Unlock Bootloader
```
./bin/rootmaster unlock <device-id>
```

#### Flash Custom Recovery
```
./bin/rootmaster flash <device-id> --recovery /path/to/recovery.img
```

#### Install Root Access
```
./bin/rootmaster root <device-id> --magisk /path/to/magisk.zip
```

#### Complete Rooting Process
```
./bin/rootmaster auto <device-id> --recovery /path/to/recovery.img --magisk /path/to/magisk.zip
```

## Supported Devices

RootMaster currently supports the following device manufacturers and brands:

### Google
- All Pixel devices (Pixel 2 through Pixel 8 series)
- Other Google-branded devices

### Samsung
- Galaxy S series (S7 and newer)
- Galaxy Note series (Note 8 and newer)
- Galaxy A series
- Galaxy Tab series

### Xiaomi Ecosystem
- Xiaomi Mi series
- Redmi series
- POCO phones

### BBK Electronics Brands
- OnePlus (5 series and newer)
- Oppo (Find, Reno series)
- Vivo (X, Y, V series)
- Realme (GT, Number series)

### Transsion Holdings Brands
- Tecno (Camon, Spark series)
- Infinix (Hot, Note series)
- Itel

Support for additional manufacturers and specific models is being added continuously. Check for updates regularly.

## Warning

**ROOTING YOUR DEVICE MAY:**
- Void your warranty
- Expose your device to security risks
- Cause data loss
- Potentially "brick" your device if done incorrectly

**USE AT YOUR OWN RISK!**

## Troubleshooting

### Device Not Detected
- Verify USB debugging is enabled
- Try a different USB cable or port
- Reinstall ADB drivers on your computer

### Bootloader Unlock Failed
- Ensure OEM unlocking is enabled in Developer Options
- Check if your device manufacturer allows bootloader unlocking
- For some devices, you may need to request an unlock code from the manufacturer

### Recovery Flashing Failed
- Verify you have the correct recovery image for your exact device model
- Some devices require specific partitioning or firmware versions

### Root Access Not Working
- Try an alternative root method
- Check if your device's firmware version is supported by the root method

### Download Issues
- Ensure you have an active internet connection
- Check firewall settings that might block download requests
- If your device model isn't recognized, try entering it manually
- For recovery images, you may need to download them manually if automatic detection fails

## Contributing

Contributions to RootMaster are welcome! To contribute:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Disclaimer

This tool is provided for educational purposes only. The developers are not responsible for any damage caused to devices through the use of this software. Always research thoroughly before attempting to root any device.
