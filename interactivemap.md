# 📡 GPS Tracker for the A9G Module

A production-ready GPS tracking dashboard for the A9G GSM+GPS module. The project pairs an Express/Socket.IO backend with a Leaflet-powered frontend to deliver live multi-device tracking, geofence awareness, and historical insights backed by PostgreSQL.

## 🚀 Key Features

- 🔌 **Real-time updates** – Socket.IO streams new locations to every connected browser without manual refreshes.
- 🗺️ **Interactive Leaflet map** – Visualize trackers, paths, and optional geofences with automatic map fitting per device.
- 🚗 **Multi-device management** – Filter the dashboard, inspect the latest status card, and review history per device.
- 🛡️ **Geofence insights** – Submit optional geofence coordinates; the UI highlights inside/outside status and distance from center.
- 🪪 **Device directory** – `/api/devices` exposes the roster of known trackers with last-seen timestamps and active state.
- 🧹 **Remote maintenance** – Clear stored coordinates, trigger manual refreshes, or force WebSocket reconnects directly from the UI.
- 📊 **Database-backed history** – PostgreSQL stores up to 1000 of the most recent points (per request) for reliable auditing.
- 🔺 **Circle and polygon geofences** – Backend and UI support circle and polygon fences with normalized responses.

## 🧱 Tech Stack

- **Backend:** Node.js, Express, PostgreSQL (`pg`), Socket.IO, dotenv, CORS
- **Frontend:** HTML, CSS, Leaflet 1.9, Socket.IO client 4.x, vanilla JavaScript (`public/app.js`)
- **Deployment:** Designed for Render, Railway, Fly.io, or any Node host that supports WebSockets and PostgreSQL
