# Global Wealth Flow Map

This is a React-based visualization application that shows the wealth transfer patterns between countries in the Global North and Global South. It uses proper geographic mapping tools to represent the flows accurately on a world map.

## Features

- Interactive world map using proper geographic boundaries
- Visualization of different wealth flow types (profit repatriation, resource extraction, debt service, etc.)
- Filtering by flow type
- Detailed tooltips with country and flow information
- Summary statistics of global wealth flows
- Zooming and panning capabilities

## Installation

1. Clone this repository
2. Install dependencies:

```bash
npm install
```

3. Download the world topology data:
   
   You need to download the world geography data in TopoJSON format. The easiest way to do this is:

   ```bash
   mkdir -p src/data
   curl -o src/data/world-110m.json https://unpkg.com/world-atlas@2.0.2/countries-110m.json
   ```

   Alternatively, you can save the file manually from [https://unpkg.com/world-atlas@2.0.2/countries-110m.json](https://unpkg.com/world-atlas@2.0.2/countries-110m.json) and save it in the `src/data` directory.

4. Create a `worldData.json` file:

   Instead of using dynamically fetched data, this visualization uses a preloaded JSON file. Create a file named `worldData.json` in the `src` directory with the contents of the downloaded TopoJSON world map data.

## Running the application

```bash
npm start
```

The application will be available at [http://localhost:3000](http://localhost:3000).

## Project Structure

- `GlobalWealthFlow.jsx` - Main component containing the map visualization
- `App.js` - Root React component
- `index.css` - Tailwind CSS imports and global styles
- `worldData.json` - World map data in TopoJSON format (you need to create this from downloaded data)

## Technologies Used

- React
- react-simple-maps (for geographic visualization)
- d3-scale (for scaling data values to visual properties)
- topojson-client (for handling TopoJSON data)
- react-tooltip (for tooltips)
- Tailwind CSS (for styling)

## Data Sources

The wealth flow data in this visualization is representative and simplified for demonstration purposes. In a real-world application, this data should be replaced with accurate economic data from reliable sources such as:

- World Bank
- International Monetary Fund (IMF)
- United Nations Conference on Trade and Development (UNCTAD)
- Organization for Economic Cooperation and Development (OECD)

## Customization

You can modify the wealth flow data in the `wealthFlows` array in `GlobalWealthFlow.jsx` to reflect different economic scenarios or more accurate data.
