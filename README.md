# Migratory Bird Tracking & Visualization

This project visualizes the flight paths of greater white-fronted geese using GPS tracking data. The data is cleaned, processed, and displayed on an interactive map with **Folium**. The project features color-coded paths for each bird based on their unique identifier, allowing users to trace individual bird flights over time.

## Features

- **Flight Paths Visualization**: Displays the birds' migration patterns using PolyLines that connect consecutive GPS coordinates based on the timestamp.
- **Interactive Map**: Hover over a point to see detailed bird information (e.g., ID, speed, altitude, etc.).
- **Color-Coded Bird Paths**: Flight paths are color-coded based on the unique tag-local-identifier of each bird.
- **CircleMarkers for GPS Points**: Markers are added for individual GPS points, making it easy to view the birds' locations at specific times.

## Data

The dataset contains GPS tracking data for individual birds with attributes such as:

- `timestamp`: Date and time of recorded location
- `location-lat`: Latitude of the bird's location
- `location-long`: Longitude of the bird's location
- `individual-local-identifier`: Unique bird ID (Tag identifier)
- `ground-speed`: Speed of the bird in km/h
- `heading`: Direction the bird is flying (in degrees)
- `height-above-msl`: Altitude in meters above mean sea level
- `study-name`: Name of the study from which the data originates

The GPS data was collected from a tracking study of greater white-fronted geese, and the paths are visualized based on their individual `tag-local-identifier`.

The data was sourced from [Movebank](https://www.movebank.org/cms/webapp?gwt_fragment=page=search_map), a platform for animal tracking data.

## Installation & Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/migratory-bird-tracking.git
   cd migratory-bird-tracking
   ```

2. Install required dependencies:
   ```bash
   pip install pandas folium
   ```

3. Place your cleaned GPS data (`data_cleaned.csv`) in the project directory, ensuring it follows the format shown in the provided dataset example.

4. Run the Python script to generate the map:
   ```bash
   python generate_migration_map.py
   ```

5. Open `migration_map.html` in a web browser to view the interactive map.

## Usage

- **View Flight Paths**: The map displays individual bird paths using color-coded lines (PolyLines) based on the unique `tag-local-identifier`.
- **Hover over Points**: Hover over a CircleMarker to see detailed information about each bird's location at that point, including speed, altitude, and timestamp.
- **Interactive Controls**: The map allows users to zoom in and out and interact with the bird locations.

## Example Output

A sample interactive map is generated and saved as `migration_map.html`. Open it in any browser to interact with the visualization.

## Contributions

Contributions are welcome! Feel free to open an issue or submit a pull request if you'd like to improve this project.

## License

This project is open-source and available under the [MIT License](LICENSE).
