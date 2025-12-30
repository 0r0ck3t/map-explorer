# 🗺️ Map Explorer - Google Maps Clone

A modern, interactive map application built with React and Leaflet, inspired by Google Maps.

## Features

- 🗺️ Interactive map with OpenStreetMap tiles
- 🔍 Location search functionality
- 📍 Click-to-add markers
- 🎨 Modern, responsive UI design
- 📱 Mobile-friendly interface
- ✨ Smooth animations and transitions

## Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn

### Installation

1. Install dependencies:
```bash
npm install
```

2. Start the development server:
```bash
npm run dev
```

3. Open your browser and navigate to `http://localhost:5173`

### Building for Production

```bash
npm run build
```

The built files will be in the `dist` directory.

## Usage

- **Search**: Type a location name in the search bar (e.g., "Paris", "London", "New York")
- **Add Markers**: Click anywhere on the map to add a marker
- **Remove Markers**: Click the × button next to any marker in the sidebar
- **View Location Info**: Search results will show location coordinates

## Technologies Used

- **React** - UI framework
- **Vite** - Build tool and dev server
- **Leaflet** - Open-source mapping library
- **React-Leaflet** - React bindings for Leaflet
- **OpenStreetMap** - Map tile provider

## Analysis of technologies and concepts within the project that align (conceptually or directly) with Google Maps

**1. The "Slippy Map" Concept (Tile-based Maps)**

* **In Google Maps:** Google revolutionized web mapping in 2005 by introducing the concept of loading the map as small squares (tiles)—typically 256x256 pixel images—that load dynamically as the user pans (drags and drops) the map.
* **In the project:** We use Leaflet and OpenStreetMap. Applied Technology:** Tiling system. The map is not a single gigantic image, but a grid of small images requested asynchronously from the server based on x, y, and z (zoom) coordinates.

**2. Single Page Application (SPA) and Asynchronous Loading (AJAX)**

* **In Google Maps:** The map updates without reloading the entire page. Interaction is fluid, similar to a desktop application.
* **In the project:** We use React and Vite. Applied Technology: DOM Manipulation and AJAX (via `fetch` or internal Leaflet mechanisms).

**3. Mercator Projection and Coordinate System**

* **In Google Maps:** The Web Mercator projection is used to transform the spherical globe into a flat 2D map on the screen.
* **In the project:** Leaflet automatically handles this mathematics. Applied Technology: Geometric and geospatial transformations.

**4. Vector Rendering (Overlays)**

* **In Google Maps:** Markers, routes, and shapes are drawn over the map using vector technologies (SVG or Canvas/WebGL).
* **In the project:** React-Leaflet. Applied Technology: SVG (Scalable Vector Graphics) or HTML5 Canvas.
  
