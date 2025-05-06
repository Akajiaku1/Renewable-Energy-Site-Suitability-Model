# Renewable Energy Site Suitability Model

This project is a GIS-based Streamlit application for identifying optimal sites for renewable energy development (solar, wind, hydro) using a weighted raster overlay model.

## Features
- Upload and process raster layers such as solar radiation, slope, distance to roads, and land use.
- Normalize input layers and apply user-defined weights.
- Compute a composite suitability map using Multi-Criteria Decision Analysis (MCDA).
- Visualize the output suitability map interactively.
- Option to save the output as a GeoTIFF raster.

## Installation
```bash
pip install streamlit rasterio numpy matplotlib geopandas
```

## Folder Structure
```
Renewable-Energy-Site-Suitability-Model/
├── data/                        # Folder for input raster files
├── output/                      # Folder to save output maps
├── model.py                     # Main Streamlit app
└── README.md                    # Project documentation
```

## Usage
Run the Streamlit app:
```bash
streamlit run model.py
```

Adjust the weights and paths in the UI to run the suitability model. Ensure all input rasters are spatially aligned.

## Example Layers
- `solar_radiation.tif`: Solar potential (higher is better)
- `slope.tif`: Slope data (lower is better)
- `roads_distance.tif`: Distance from roads (lower is better)
- `landuse.tif`: Land use classification (e.g., grassland or barren is suitable)

## Notes
- Extendable to wind or hydro energy by replacing the solar input with wind speed or water flow potential.
- Land use reclassification can be adjusted in the script.

## License
MIT License

## Authors
- Akajiaku – Project Development

## Future Work
- Incorporate vector data (e.g., protected areas)
- Add support for cloud-based data sources
- Export reports or dashboards
