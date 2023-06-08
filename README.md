# Kitronik Pico ZIP96 Retro Gamer
 
This repo contains the C library file for the [Kitronik ZIP96 Retro Gamer for Raspberry Pi Pico](https://kitronik.co.uk/5347).

The `ZIP96Pico.c` and `ZIP96Pico.h` files provide the library functions that we can use to control the ZIP96 Retro Gamer.

This includes everything from the buttons, vibration motor and buzzer, to the screen and a Colour struct to help with storing RGB values for the ZIPLEDs.

The ZIP96Pico C library also requires the `ws2812.pio` file, to run the PIO for control of the ZIPLEDs.

Examples for how to use this library can be found in the Run Along, Jump & Jump game. There are two versions of this game, a single player version and the wireless two player version.

## Play Run Along, Jump & Jump
To play the game simply download one of the UF2 game files in the `Run Along, Jump & Jump` folder and use the BOOTSEL button to load them onto your Pico.

The `rajaj-single.uf2` file contains the single player version of Run Along, Jump & Jump.

The `rajaj-client.uf2` and `rajaj-server.uf2` files contain the wireless two player version of Run Along, Jump & Jump. This version of the game requires two Kitronik ZIP96 Retro Gamers and two Raspberry Pi Pico W's. One of the Pico W's needs to have the `rajaj-server.uf2` file loaded onto it. The other Pico W needs to have the `rajaj-client.uf2` file loaded onto it.

## PicoWNetworking
On top of the ZIP96Pico library, there is also a PicoWNetworking library available in the `PicoWNetworking.c` and `PicoWNetworking.h` files.

This provides a simpler interface for using the networking chip on the Pico W.

Examples for how to use this library for both server and client functionality can be found in the `main-server.c` and `main-client.c` files inside the `Run Along, Jump & Jump/Wireless Two Player` folder.

The PicoWNetworking C library also requires the `lwipopts.h` file, to set common settings used for Pico W Networking.
