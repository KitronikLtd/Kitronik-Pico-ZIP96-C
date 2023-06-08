cmake_minimum_required(VERSION 3.13)

# initialize the SDK directly
include(/home/jack/pico/pico-sdk/pico_sdk_init.cmake)

# cmake -DPICO_BOARD=pico .. && make

project(rajaj-single)

# initialize the Raspberry Pi Pico SDK
pico_sdk_init()

add_executable(rajaj-single
	main-single.c
	RAJAJ.c
	ZIP96Pico.c
	ws2812.pio)

pico_generate_pio_header(rajaj-single ${CMAKE_CURRENT_LIST_DIR}/ws2812.pio)

target_include_directories(rajaj-single PRIVATE
	${CMAKE_CURRENT_LIST_DIR}
	${CMAKE_CURRENT_LIST_DIR}/..)

target_link_libraries(rajaj-single
	pico_stdlib
	hardware_gpio
	hardware_pio
	hardware_pwm)

pico_add_extra_outputs(rajaj-single)
