# Overview
Here is the Docker (Compose) repository used on my Synology NAS. I find that the GUI does not work as well as I had hoped (macvlan support is non-existant).

## Containers

### Home Assistant
Home Assistant is the brains behind my home automation setup. This allows all my devices (regardless of make/model) to cooperate together. This is the driver behind this project since I require port 80 access to improve the system's WAF (Wife-Acceptance Factor) score and allow Alexa to be an interface.

### Ring Alarm <-> MQTT Bridge
Repackaged version of TSightler's [Ring-MQTT](https://github.com/tsightler/ring-mqtt) project. Since this touches my security system, I audit and rebuild it myself.

### MQTT Message Broker
Eclipse Mosquitto, an Open Source MQTT Broker. All of my Tasmota flashed devices connect to this container.
