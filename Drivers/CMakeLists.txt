cmake_minimum_required(VERSION 3.21.0)

project(Drivers)

add_library(${PROJECT_NAME}
STATIC
    STM32F1xx_HAL_Driver/Src/stm32f1xx_hal.c
    STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_cortex.c
    STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_gpio.c
    STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_gpio_ex.c
    STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_pwr.c
    STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_rcc.c
    STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_rcc_ex.c
)

target_compile_definitions(${PROJECT_NAME}
PUBLIC
    USE_HAL_DRIVER
    STM32F103xB
)

target_include_directories(${PROJECT_NAME}
PUBLIC
    STM32F1xx_HAL_Driver/Inc
    STM32F1xx_HAL_Driver/Legacy
    CMSIS/Device/ST/STM32F1xx/Include
    CMSIS/Include
)
