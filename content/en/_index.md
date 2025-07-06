---
title: Homepage
linkTitle: Homepage
---

# Flashbootloader_RH850_Generic

A generic automotive flash bootloader project targeting the Renesas RH850 microcontroller family. This repository is structured for integration with automotive ECUs and includes modules for EEPROM, Flash driver, hardware abstraction, and demo applications.

## Features

- **Support for Renesas RH850**: Designed for use with the RH850 microcontroller family.
- **Automotive BSW Structure**: Modular Basic Software (BSW) layers for easy integration.
- **EEPROM Abstraction**: Wrapper drivers for EEPROM operations.
- **Flash Programming**: Tools and scripts to manage and program Flash memory.
- **Bootloader Core**: UDS (ISO 14229) diagnostics and CAN interface support.
- **Demo Application**: Example application for evaluation and integration.

## Project Structure

```
BSW/
  ├── Eep/         # EEPROM driver abstraction
  ├── Flash/       # Flash programming driver and build scripts
  └── Fbl/         # Bootloader core and hardware abstraction
Demo/
  └── DemoAppl/    # Demo application and project-specific files
Misc/
  └── HexView/     # Utility tools and disclaimers
```

## Getting Started

### Prerequisites

- **Hardware**: Renesas RH850 microcontroller (e.g., R7F701313EAFP)
- **Compiler**: GreenHills 2015.1.7 (as referenced in source comments)
- **Toolchain**: Standard automotive build tools (Make, batch scripts)

### Build Instructions

1. Go to the Flash build directory:
   ```
   cd BSW/Flash/Build
   ```
2. Use the provided Makefile or batch scripts (e.g., `Makefile`, `MkFlashRom.bat`) to build the Flash driver or bootloader.
3. See `Demo/DemoAppl/Appl/` for demo project files and integration examples.

### Flashing & Usage

- The output can be programmed to the target RH850 MCU using standard programming tools.
- The bootloader communicates via CAN and supports ISO 14229 (UDS) services for diagnostics and reprogramming.

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

## Disclaimer

Some files and code are copyright © Vector Informatik GmbH and/or provided as-is, without warranty.
See also `Misc/HexView/disclaimer.txt` for further notices.

## References

- [Renesas RH850 Family](https://www.renesas.com/us/en/products/microcontrollers-microprocessors/rh850-automotive-microcontroller)
- [UDS / ISO 14229](https://en.wikipedia.org/wiki/Unified_Diagnostic_Services)

---

*This README provides a general overview. For advanced configuration, customization, or troubleshooting, please refer to the code comments and build scripts.*
