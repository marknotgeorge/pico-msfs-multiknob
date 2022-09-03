cmake_minimum_required(VERSION 3.13)

include(pico_sdk_import.cmake)

project(pico-msfs-multiknob)

pico_sdk_init()

add_subdirectory(lib)

add_executable(pico-msfs-multiknob    
    main.cpp
)

pico_enable_stdio_usb(pico-msfs-multiknob 1)
pico_enable_stdio_uart(pico-msfs-multiknob 1)

pico_add_extra_outputs(pico-msfs-multiknob)

target_link_libraries(pico-msfs-multiknob pico_stdlib hardware_i2c ssd1306)