cmake_minimum_required(VERSION 3.12)

# ========================= board setup ===========================
# Uncomment one of the environment variable to use 3rd party board
# Comment all sets board to Pico as default

# Adafruit Feather RP2040
#set(PICO_BOARD ADAFRUIT_FEATHER_RP2040)

# Pimoroni Tiny 2040 2MB
set(PICO_BOARD PIMORONI_TINY2040_2MB)

# =================================================================

# initialize pico-sdk from submodule
# note: this must happen before project()
include(pico-sdk/pico_sdk_init.cmake)

project(Pico-FreeRTOS)

# Initialize the SDK
pico_sdk_init()

add_subdirectory(FreeRTOS)
add_subdirectory(ProjectFiles)