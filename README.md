# Web-GIS Application

This project is a simple Web-GIS application that integrates **Leaflet.js** for interactive map functionality and uses WMS (Web Map Service) from a local GeoServer for serving geospatial data.

## Features

- Displays an interactive map using OpenStreetMap tiles.
- Integrates WMS services through GeoServer.
- Provides links to `GetCapabilities` and `GetMap` requests for WMS layers.

## Prerequisites

To run this project locally, ensure you have the following:

1. **GeoServer** installed and running on `http://localhost:8080/`.
2. A WMS layer published in GeoServer, accessible via:
   - `GetCapabilities`: `/geoserver/wms?service=wms&version=1.1.1&request=GetCapabilities`
   - `GetMap`: `/geoserver/wms?service=WMS&version=1.1.0&request=GetMap&layers=layer_group&bbox=...`

3. A compatible web browser.

## How to Run

1. Clone this repository or download the HTML file.
2. Place the project in a directory accessible by a web server (e.g., Apache, Nginx, or a local server like `http-server`).
3. Make sure GeoServer is running and configured to serve your WMS layers.
4. Open the HTML file in your browser.

## External Libraries Used

- [Leaflet.js](https://leafletjs.com/) (v1.7.1): A JavaScript library for interactive maps.
- [jQuery](https://jquery.com/) (v3.5.1): A fast, small, and feature-rich JavaScript library.
- `L.TileLayer.BetterWMS.js`: A custom Leaflet extension for handling WMS layers better.

## Map Details

- **Center**: Latitude 40.7128, Longitude -74.006 (New York City by default).
- **Zoom Level**: 13.
- **Tile Layer**: OpenStreetMap.

## WMS Requests

This application opens two WMS-related URLs in new tabs:

1. **GetCapabilities**: Provides metadata about available layers and styles.
2. **GetMap**: Retrieves the WMS layer as a map image.

## Project Structure

- `index.html`: Main HTML file containing the map and script logic.
- `lib/L.TileLayer.BetterWMS.js`: Custom Leaflet extension for WMS layers.

## Customization

- Update the `center` coordinates and `zoom` in the JavaScript section to focus on a different location.
- Replace `layer_group` in the `GetMap` request URL with your own WMS layer name.
- Adjust the `bbox`, `width`, and `height` parameters in the `GetMap` request as needed.

## License

This project uses OpenStreetMap tiles, which are licensed under the [Open Database License](https://opendatacommons.org/licenses/odbl/). Please ensure compliance with applicable licenses for GeoServer and external libraries.

## Acknowledgements

- [OpenStreetMap](https://www.openstreetmap.org/)
- [Leaflet.js](https://leafletjs.com/)
