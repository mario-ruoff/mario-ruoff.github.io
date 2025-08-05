---
layout: project
title: "J.A.R.V.I.L."
date: 2021-07-18
imageurl: pexels-eberhardgross-2088205.jpg
pagecolorhue: 0

stack:
    - Python
    - MQTT
    - Redis
    - InfluxDB
    - Docker

links:
  - text: "Repository"
    icon: "code"
    url: "https://github.com/mario-ruoff/jarvil"

excerpt: "Just A Rather Very Intelligent Library - An IoT library room booking service"

description: "J.A.R.V.I.L. stands for 'Just A Rather Very Intelligent Library'. It is a project of the 'Smart Cities & IoT' course at the University of Stuttgart. It's main goal is to simplify and automate various tasks in a modern library to make daily work easier for students."
---

## System Architecture
![System Architecture](/assets/images/jarvil-architecture.jpg)

## Services

- **Arduino Configuration:**  
  Supports remote Arduino programming via Bluetooth (StandartFirmata_Bluetooth) or USB (StandartFirmata) using pyFirmata. Devices are configured by uploading the appropriate firmware through the Arduino IDE.

- **System Setup:**  
  The system runs on multiple Raspberry Pi containers managed with Docker Compose. Each container provides specific services:
  - Development: All services for live development.
  - Pi-1: MQTT broker and analysis.
  - Pi-2: Time slot booking.
  - Pi-3: MQTT endpoint.

- **MQTT Broker (Mosquitto):**  
  Facilitates communication between system components on port 1883. MQTT-Explorer is recommended for testing.

- **Database (InfluxDB):**  
  Stores time series data collected by the system. Accessible at port 8086 with default credentials ("grafana"/"password").

- **Time Slot Booking Service:**  
  Users book library visits via a web interface (http://localhost:5000/). Bookings require basic personal information and are cached in Redis (http://localhost:6379/).

See the [Wiki](https://github.com/mario-ruoff/jarvil/wiki/) for full documentation.
