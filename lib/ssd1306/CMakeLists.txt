cmake_minimum_required(VERSION 3.13)

add_library(ssd1306 INTERFACE)

target_sources(ssd1306 INTERFACE 
    ${CMAKE_CURRENT_SOURCE_DIR}/src/SSD1306.cpp 
    ${CMAKE_CURRENT_SOURCE_DIR}/src/GFX.cpp
)

target_link_libraries(ssd1306 INTERFACE)

target_include_directories(ssd1306 INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)