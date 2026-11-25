# Fieldnote — GPS Map Camera

A mobile-first, browser-based GPS camera. Start the camera and allow location access to capture high-resolution photos stamped with an editable address, coordinates, accuracy, an optional note, and the current Indian Standard Time. Captures download as JPEGs and remain in the page's session history until you leave.

## Run it

Serve this folder over HTTPS (or `localhost`, which browsers treat as a secure context) and open `index.html`. Camera and geolocation permissions do not work on ordinary insecure HTTP pages.

For a quick local preview with Python:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Features

- Live camera preview with front/rear camera switching where supported.
- High-accuracy geolocation watch and OpenStreetMap reverse geocoding.
- Leaflet map preview using OpenStreetMap tiles, plus a link to the location on OSM.
- Indian date/time formatting using the `Asia/Kolkata` time zone.
- Editable address and optional note included in a permanent, high-resolution canvas stamp.
- JPEG download and in-memory photo history for the current browser session.

Camera and location access require user permission. The map, reverse-geocoding service, and Leaflet are loaded from third-party services; the app does not upload captured photos. Respect the OpenStreetMap tile and Nominatim usage policies for production or high-volume use.
