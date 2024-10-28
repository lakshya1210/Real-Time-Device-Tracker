# Real-Time Device Tracker

This project is a real-time device tracking application built using **Node.js**, **Express**, and **Socket.io**. It provides an interactive map for tracking the live location of devices, powered by **Leaflet** and **OpenStreetMap** tiles for visualization.

## Features

- **Real-Time Location Updates:** Tracks devices in real time with live updates using Socket.io.
- **Interactive Map with Leaflet:** Displays device locations on a map using Leaflet, utilizing OpenStreetMap tiles for rendering.
- **High Accuracy Geolocation:** Configured for high accuracy with a 5-second timeout and no caching of location data to ensure precision.
- **Dynamic Marker Management:** Automatically adds, updates, and removes markers based on device activity.
- **Error Handling:** Handles geolocation errors gracefully to ensure smooth operation.

## How It Works

1. **Frontend**: Uses JavaScript to access the browser's Geolocation API. If geolocation is enabled, it sends the device's latitude and longitude to the server via Socket.io. The geolocation options are set with:
   - High accuracy enabled
   - 5-second timeout
   - No caching for data accuracy
2. **Backend**: Receives location data and broadcasts it to all connected clients.
3. **Map and Markers**: Leaflet renders the map, and markers are dynamically managed to show the location of each tracked device.

## Technologies Used

- **Node.js** and **Express** for the server.
- **Socket.io** for real-time, bidirectional communication.
- **Leaflet** for map rendering and marker management.
- **OpenStreetMap** for map tiles.

