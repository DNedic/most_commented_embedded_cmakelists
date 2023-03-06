# The most thoroughly commented embedded CMakeLists file project
This repository contains an example embedded CMake project using an STM32F103 MCU. It contains [the most thoroughly commented embedded CMakeLists file](CMakeLists.txt).

# Building
To build the project in the default Debug mode use the following commands:
```bash
cmake -S . -B build -DCMAKE_BUILD_TYPE=Debug -DCMAKE_TOOLCHAIN_FILE=arm-none-eabi-gcc.cmake
cmake --build build
```
