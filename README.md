# A Repo to hold the config files for my home automation build

My home automation system consists of the following:

* Home Assistant
* Node Red
* Mosquitto MQTT Broker
* Zigbee2MQTT

Each of these is running as a Docker container (see [docker-compose.yml](./docker-compose.yml)) on a old Dell Optiplex USFF PC (i5 / 4GB RAM) that is running Ubuntu 18.04

I am using all the default supported latest images for everything from Docker Hub. I have avoided any special or custom builds.

## Home Assistant

[homeassistant/home-assistant](https://hub.docker.com/r/homeassistant/home-assistant) image from Docker Hub. At the time of writing that's 0.103.5

## Node Red

The stock [nodered/node-red](https://hub.docker.com/r/nodered/node-red) container from Docker Hub.

At the moment I'm not using Node Red for any automations. I have used it for some testing and debugging of things, but then converted the automation back to YAML. I can see a future where complex multistage automations end up here, but we'll see.

## Mosquitto

This is the offical [eclipse-mosquitto](https://hub.docker.com/_/eclipse-mosquitto) docker iamage, running with out of the box configs for now.

## Zigbee2MQTT

[koenkk/zigbee2mqtt](https://hub.docker.com/r/koenkk/zigbee2mqtt)

This was a revelation. I had been battling the broken Zigbee implementation on a Vera Plus hub and gettig nowhere. Got this running all my Zigbee devices just came to life.

I am using a cc2531 controller plugged into a USB port on the Dell PC. It's running the Zigbee2MQTT firmware.

## Hardware / IoT Devices

##### WiFi
* 5 x Lifx Color 1000 (original 11W models)
* 1 x Wemo Switch
* 1 x Sonoff POW 2
* 1 x Whitelabel (Tuya based) blind controller
* 2 x Moorescloud Holiday Christmas lights
* 3 x Sonos Speakers (2 Ikea Lamps, 1 Bookshelf)

##### Zigbee
* 4 x Ikea Tradfri globes
* 2 x Xiaomi Aqara double paddle switches
* 1 x Xiaomi Aqara door sensor
* 1 x Xiaomi Aqara temperature & humidity sensor
* 1 x Ikea Tradfri Repeater

