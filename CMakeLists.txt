cmake_minimum_required(VERSION 3.5)

# Build InterruptButton as an ESP-IDF component
if(ESP_PLATFORM)
idf_component_register(
    SRCS "InterruptButton.cpp"
    INCLUDE_DIRS "."
    REQUIRES 
        driver
        esp_timer
        #PRIV_REQUIRES
    )
return()
endif()

project(InterruptButton VERSION 1.0.0)
#target_compile_options(${COMPONENT_TARGET} PRIVATE -fno-rtti)
