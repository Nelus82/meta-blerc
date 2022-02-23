# meta-blerc-shield

## General
This driver is to control your Nvidia Shield (or any device that accepts a bluetooth keyboard) from your Neeo with help of meta2 (https://github.com/jac459/meta). You need additional hardware (ESP32) to simulate a bluetooth keyboard. I made the driver as simple as possible for my needs. The driver uses Websocket to communicate with the ESP. If you miss something do not hesitate to ask or help.

The ESP32 must be flashed with BLE-Remote-Companion (https://github.com/hannemann/BLE-Remote-Companion. This software turns an ESP32 into a virtual keyboard and mouse running a websocket server and/or Home Assistant websocket API client. The built in webserver offers a HTML page with a grapical remote, a simple keyboard and mouse functionality.


## Requirements
- Neeo
- working installation of meta2 (https://github.com/jac459/meta)
- ESP32 with BLE-Remote-Companion
- Nvidia Shield (or any device that accepts a bluetooth keyboard)


## ESP32 Hardware
I've tested BLE-Remote-Companion on a ESP-WROOM-32, that worked very well. To reduce the latency to a minimum hanneman added hardware support for a ESP with ethernet (WT32-ETH01). This works perfectly en very fast, I'm getting the same experience as the default remote.


## Installation instructions
- Add Device on Neeo
- Search driver (BLERC_Shield)
- Fill in the IP of the BLE-Remote-Companion.
- Select a room which the device should be added.
- Setup the device acording your needs


## Remapping keys
A big advantage of this driver is that you can remap almost every key on the keyboard. Inside Kodi you can use the standard C key to get a context menu, but I also remapped keys to syns subtitles. Inside the Shield I remapped keys to applications, that way I can start Netflix with a shortcut on the neeo. The possibilities are endless


## WebSocket
WebSocket needs a active connection to communicate, this connection is activated by the power_on command. Keep this in mind if you want to use a shortcut in a different recipe.


I want to thank Jac459 and MarkusM for helping me and for creating this fantastic piece of software that brings our Neeo to life (as it was intended).
Also want to thank hanneman (https://github.com/hannemann) for creating BLE-Remote-Companion.

Telegram Group: https://t.me/joinchat/NocMDU9RCVP9hSCJxPsCEg
