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

## Analiză a tehnologiilor și conceptelor din proiect care se regăsesc (conceptual sau direct) în Google Maps
1. Conceptul de "Slippy Map" (Hărți bazate pe Tile-uri)
         În Google Maps: Google a revoluționat hărțile web în 2005 prin introducerea conceptului de a încărca harta sub formă de pătrate mici (tiles), de obicei imagini de 256x256 pixeli, care se încarcă dinamic pe măsură ce utilizatorul trage de hartă (drag & drop).
         În proiect: Folosim Leaflet și OpenStreetMap.
         Tehnologia aplicată: Sistemul de tiling (mozaicare). Harta nu este o singură imagine gigantică, ci un grid de imagini mici cerute asincron de la server pe baza coordonatelor x, y și z (zoom).

2. Single Page Application (SPA) și Încărcare Asincronă (AJAX)
      În Google Maps: Harta se actualizează fără a reîncărca pagina. Interacțiunea este fluidă, similară cu o aplicație desktop.
      În proiect: Folosim React și Vite.
      Tehnologia aplicată: DOM Manipulation și AJAX (prin fetch sau mecanismele interne Leaflet).
3. Proiecția Mercator și Sistemul de Coordonate
      În Google Maps: Se folosește proiecția Web Mercator pentru a transforma globul sferic într-o hartă 2D plată pe ecran.
      În proiectul tău: Leaflet gestionează automat această matematică.
      Tehnologia aplicată: Transformări geometrice și geospațiale.
4. Randare Vectorială (Overlay-uri)
      În Google Maps: Markerii, rutele și formele sunt desenate peste hartă folosind tehnologii vectoriale (SVG sau Canvas/WebGL).
      În proiectul tău: React-Leaflet.
      Tehnologia aplicată: SVG (Scalable Vector Graphics) sau HTML5 Canvas.
  
