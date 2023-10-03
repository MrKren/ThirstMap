# ThirstMap

ThirstMap is a cloud based online monitoring system for keeping tabs on plants all over the world using the concept of the Internet of Things (IoT). This monorepo contains all the code necessary to run the ThirstMap system and is split into 3 distinct parts: [Backend](/api-server/README.md), [Frontend](/web-app/README.md) and [IoT Client](/esp32-client/README.md).

## Backend: API-Server

The backend API server consists of a dockerized python Django project that writes information from the IoT clients to a Postgres Database and then serves the frontend with data.

Read more [here](/api-server/README.md).

## Frontend: Web-App

The frontend web app is a single page React app written in Typescript that consumes the backend API server.

Read more [here](/web-app/README.md).

## IoT Client: ESP32-Client

The IoT client is written for a FireBeetle ESP32 Microcontroller with an attached variety of sensors.

Read more [here](/esp32-client/README.md).
