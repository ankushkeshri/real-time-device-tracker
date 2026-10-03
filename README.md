# Real-Time Device Tracker 📍

A low-latency, real-time geolocation tracking web application built using **Node.js**, **Express**, **Socket.IO**, **EJS**, and **Leaflet.js**. The application captures live GPS coordinates from mobile or browser devices using the HTML5 Geolocation API, streams them bi-directionally over WebSockets, and dynamically updates multi-client markers on an interactive OpenStreetMap layer.

---

## 🚀 Key Features

* **Real-Time Geolocation Streaming:** Continuous coordinate tracking via `navigator.geolocation.watchPosition` with high-accuracy settings and zero-cache timeouts.
* **Bi-Directional WebSocket Communication:** Low-latency event streaming powered by Socket.IO to broadcast client coordinates across all active sessions.
* **Dynamic OpenStreetMap Integration:** Client-side map rendering and dynamic marker updates using Leaflet.js CDN integration.
* **Automatic Session Cleanup:** Detects client disconnect events and instantly removes inactive device markers from all active map dashboards.
* **Server-Side Rendered View Container:** Built using Express with EJS templating and static file middleware serving modular CSS/JS assets.

---

## 🛠️ Tech Stack

* **Backend Environment:** Node.js
* **Web Framework:** Express.js
* **Real-Time Engine:** Socket.IO
* **Templating Engine:** EJS
* **Frontend:** JavaScript (ES6+), HTML5 Geolocation API, CSS3
* **Map Renderer:** Leaflet.js

---

## 📂 Project Architecture & Structure

```text
Real Time Tracker/
├── public/
│   ├── css/
│   │   └── style.css        # Full-screen viewport & map container styling
│   └── js/
│       └── script.js       # Client Geolocation API, Socket events & Leaflet logic
├── views/
│   └── index.ejs           # Main EJS layout container loading Leaflet & Socket.IO CDNs
├── app.js                  # Express server setup, route definition & Socket.IO event handler
├── package.json
└── README.md
