# AnyPS5 - Run PS5 Games on Windows and Linux

Tool for automatic executables porting to Linux and Windows.

![anyps5_collage1](https://github.com/user-attachments/assets/ed2f0b2d-33d3-46d7-ab88-767ca872fc99)

Includes a [relinker](core/relinker) that converts executable to the target system's native format and implementations of system prx libraries suitable for dynamic linking. No emulation or separate runtime process.

## Download

| Platform | Architecture | File | Download |
|----------|--------------|------|----------|
| **Windows** | x86_64 | `prx-windows-v0.1.5.zip` | [⬇ Download](https://github.com/OctagonDragonfly/AnyPS5/releases/download/v0.1.5/prx-windows-v0.1.5.zip) |
| **Linux** | x86_64 | `prx-linux-v0.1.5.zip` | [⬇ Download](https://github.com/OctagonDragonfly/AnyPS5/releases/download/v0.1.5/prx-linux-v0.1.5.zip) |

**Windows:** Download and extract the ZIP archive, then run `relinker-v0.1.5.exe`.

## Status

![libraries](https://boykopovar.github.io/AnyPS5/badge-libraries.svg) ![RDNA2 reference shader forms decoded](https://boykopovar.github.io/AnyPS5/badge-shaders.svg) ![gfx1013 reference shader forms decoded](https://boykopovar.github.io/AnyPS5/badge-shaders-gfx1013.svg) ![implemented in 7 days](https://boykopovar.github.io/AnyPS5/badge-week.svg)

![progress map](https://boykopovar.github.io/AnyPS5/progress.svg)

<sub>* System libraries: percentage of the functions known to the project so far, not of every PS5 system function. The total grows as more functions are declared.</sub>

Unsupported or unexpected states throw a C++ exception, usually `std::runtime_error`. An exception that nothing catches prints its `what()` to stderr and ends the process.

The [shader recompiler](core/shader/recompiler/Recompiler.cpp) successfully produces SPIR-V (validated via [Spirv-Tools](3rdparty/SPIRV-Tools) when built with `ANYPS5_ENABLE_SPIRV_TOOLS`).

## Input mapping

SDL-mapped game controllers are supported, including analog sticks and triggers. Keyboard and mouse controls can be configured with an `anyps5-input.ini` file. See [input mapping](docs/user/INPUT_MAPPING.md) for the supported devices and configuration format.

## Disclaimer

This project is intended for interoperability, research, preservation, and compatibility purposes. It does not include, distribute, or require copyrighted software, firmware, cryptographic keys, or proprietary libraries. Users are responsible for ensuring that any binaries used with this project are obtained and used in accordance with applicable laws and their respective license terms.

AnyPS5 is an independent project and is not affiliated with, authorized or endorsed by Sony Interactive Entertainment. "PlayStation" and "PS5" are trademarks of Sony Interactive Entertainment Inc.

## License

This project is licensed under the GNU General Public License version 2 only.
