# Water Quality Analysis Using Remote Sensing

**Independent Study Project - September 2025**

This repository documents an independent exploration of water quality monitoring using satellite remote sensing techniques. Inspired by discussions with Dr. Bihu Suchetana about the SiDCReW (Satellite Imagery-informed Decision Support System for Climate Resilient Drinking Water Treatment) project at IIT Roorkee, this work demonstrates practical implementation of remote sensing for water quality parameter estimation using Sentinel-2 imagery, Google Earth Engine, and Python.

## Project Overview

Traditional in-situ water quality monitoring faces limitations in spatial coverage, temporal resolution, and cost-effectiveness, particularly across large river systems. This project addresses these challenges by leveraging satellite remote sensing to monitor key water quality parameters across multiple study sites in North India.

### Objectives

- Demonstrate capabilities in satellite-based water quality parameter estimation
- Analyze seasonal variations in water quality (pre-monsoon and post-monsoon)
- Develop reproducible workflows using open-source tools and data
- Build understanding of the intersection between remote sensing and water resource management

## Repository Structure

```
Water-Quality-Index-Analysis/
├── 01-Siliguri/                    # Mahananda River study site
├── 02-Ganga/                       # Ganga River study sites
│   ├── 02-01-Premonsoon/          # Pre-monsoon analysis
│   └── 02-02-Postmonsoon/         # Post-monsoon analysis
└── 99-Archive/                     # Archived experimental work
```

## Study Sites

### Mahananda River, Siliguri
- **Location:** Near Fulbari Barrage, Siliguri, West Bengal
- **Focus:** Water quality parameter estimation and time series analysis
- **Data Source:** Sentinel-2 Surface Reflectance (2024)

### Ganga River - Three Locations
Analysis conducted at three major sites along the Ganga River with seasonal variations:
- **Varanasi** - Water quality index analysis with water body extraction
- **Kanpur** - Comprehensive WQI parameter estimation  
- **Srerampur** - Multi-parameter water quality assessment

Each site includes both pre-monsoon and post-monsoon analyses to capture seasonal dynamics.

## Implemented Methodologies

### Data Acquisition and Processing
- **Platform:** Google Earth Engine (Python API)
- **Satellite Data:** Sentinel-2 MSI Level-2A Surface Reflectance
- **Temporal Coverage:** 2024 seasonal imagery (Winter, Summer, Monsoon, Post-monsoon)
- **Preprocessing:** Cloud masking, atmospheric correction, seasonal compositing

### Water Body Detection
Multiple indices implemented for robust water body extraction:
- **NDWI (Normalized Difference Water Index)** - Primary water body identification
- **MNDWI (Modified Normalized Difference Water Index)** - Enhanced detection in urban areas
- **AEWI (Automated Water Extraction Index)** - Automated extraction with threshold optimization

### Water Quality Parameters Estimated

**Completed Implementations:**
- **Turbidity** - Water clarity measurement using empirical relationships with reflectance
- **Total Dissolved Solids (TDS)** - Dissolved impurities quantification
- **Salinity** - Dissolved salt concentration estimation
- **NDTI (Normalized Difference Turbidity Index)** - Turbidity index calculation

### Analysis and Visualization
- Interactive mapping using Geemap
- Statistical analysis and visualization (Matplotlib, Seaborn)
- Temporal trend analysis across seasons
- Spatial distribution mapping

## Technical Stack

### Core Technologies
- **Python 3.x** - Primary programming language
- **Google Earth Engine** - Cloud-based geospatial processing platform
- **Jupyter Notebooks** - Interactive development environment

### Python Libraries
- **ee (Earth Engine Python API)** - Satellite data access and processing
- **geemap** - Interactive GEE mapping and visualization
- **geopandas** - Geospatial data operations
- **matplotlib & seaborn** - Data visualization
- **numpy** - Numerical computations

### Data Sources
- **Sentinel-2 MSI** - Primary satellite imagery (10-20m resolution)
- **Google Earth Engine Data Catalog** - Processed surface reflectance products

## Implemented Notebooks

### Siliguri Site (`01-Siliguri/`)
1. `1-Water_Quality_Index_Analysis-Test_Site_Siliguri.ipynb` - Initial visualization and parameter exploration
2. `2-Water_Quality_Index_Analysis-Site-Siliguri-Final.ipynb` - Turbidity and TDS estimation workflow
3. `3-WQI-Timeseries-Site-Siliguri.ipynb` - Temporal analysis of water quality parameters

### Ganga River - Pre-Monsoon (`02-Ganga/02-01-Premonsoon/`)
4. `04-Water_Quality_Index-Ganga_River-Varanasi.ipynb` - Pre-monsoon WQI analysis (Varanasi)
5. `05-Water_Quality_Index-Ganga_River-Kanpur.ipynb` - Pre-monsoon parameter estimation (Kanpur)
6. `06-Water_Quality_Index-Ganga_River-Srerampur.ipynb` - Pre-monsoon assessment (Srerampur)

### Ganga River - Post-Monsoon (`02-Ganga/02-02-Postmonsoon/`)
7. `04-Water_Quality_Index-Ganga_River-postm-Varanasi.ipynb` - Post-monsoon analysis (Varanasi)
8. `05-Water_Quality_Index-Ganga_River-postm-Kanpur.ipynb` - Post-monsoon analysis (Kanpur)
9. `06-Water_Quality_Index-Ganga_River-postm-Srerampur.ipynb` - Post-monsoon analysis (Srerampur)

## Key Findings and Insights

- Demonstrated feasibility of satellite-based water quality monitoring across multiple river systems
- Identified significant seasonal variations in turbidity and TDS between pre-monsoon and post-monsoon periods
- Established reproducible workflows for operational water quality monitoring
- Validated the utility of Sentinel-2 data for inland water quality applications

## Future Directions

Building on this foundation, the following enhancements are planned to advance capabilities in water resource monitoring:

### Advanced Machine Learning Applications
- **Supervised Learning Models:** Random Forest, XGBoost, Support Vector Machines for improved parameter estimation
- **Deep Learning Frameworks:** 
  - Convolutional Neural Networks (CNN) for spatial pattern recognition
  - Recurrent Neural Networks (RNN) and LSTM for time-series forecasting
  - Multi-step water quality parameter prediction models
- **Feature Engineering:** Integration of spectral indices, texture features, and temporal patterns

### Expanded Remote Sensing Capabilities
- **Multi-source Data Integration:**
  - SAR imagery (Sentinel-1) for all-weather monitoring
  - Landsat time-series for long-term trend analysis
  - Higher resolution imagery (PlanetScope) for detailed studies
- **Additional Satellite Missions:**
  - GRACE/GRACE-FO for terrestrial water storage
  - GPM for precipitation monitoring
  - SWOT for river discharge estimation

### Hydrological Modeling Integration
- **SWAT (Soil and Water Assessment Tool):** Watershed-scale water quality modeling
- **WRF (Weather Research and Forecasting):** Climate impact assessment
- **InVEST:** Ecosystem services valuation for water resources
- **Integrated Modeling Frameworks:** Coupling remote sensing with process-based models

### Advanced Analytical Techniques
- **Data Assimilation:** Ensemble Kalman Filter (EnKF), 3DVAR for improved state estimation
- **Climate Change Analysis:** Projection of water quality changes under future climate scenarios
- **Real-time Monitoring Systems:** Development of operational decision support tools

### Expanded Parameter Coverage
- **Optically Active Parameters:** Chlorophyll-a, CDOM, suspended particulate matter
- **Optically Inactive Parameters:** Dissolved oxygen, pH, nutrients (nitrogen, phosphorus)
- **Validation Framework:** Ground-truthing campaigns for robust accuracy assessment

### Scalability and Operational Deployment
- **Cloud Computing Optimization:** Leverage GEE for large-scale analysis
- **Automated Monitoring Pipelines:** Scheduled updates and alert systems
- **Web-based Dashboards:** Interactive visualization for stakeholders
- **Multi-basin Analysis:** Extend methodology to other river systems

## Limitations and Considerations

- **Spatial Resolution:** Sentinel-2 (10-20m) may miss small-scale features
- **Cloud Cover:** Optical imagery limited in monsoon season
- **Algorithm Validation:** Empirical relationships require site-specific calibration
- **Temporal Resolution:** 5-day revisit may miss short-term events
- **Parameter Limitations:** Some water quality parameters cannot be directly detected optically

## Usage

### Prerequisites
```bash
pip install earthengine-api geemap geopandas matplotlib seaborn numpy
```

### Authentication
```python
import ee
ee.Authenticate()
ee.Initialize()
```

### Running Notebooks
Open any notebook in Jupyter and execute cells sequentially. Modify study area coordinates and date ranges as needed.

## Contributing

This is an independent study project, but suggestions and improvements are welcome. Feel free to open issues or submit pull requests.

## Acknowledgments

This work was inspired by discussions about the SiDCReW project with Dr. Bihu Suchetana, Department of Civil Engineering, IIT Roorkee. The project demonstrates practical applications of remote sensing for climate-resilient water resource management.

Special appreciation to:
- Google Earth Engine team for providing cloud-based geospatial processing infrastructure
- ESA Copernicus programme for open-access Sentinel-2 data
- The open-source geospatial Python community

## Contact

**Sohan Nag**  
Email: workspacesohan@gmail.com  
LinkedIn: [Sohan Nag](https://www.linkedin.com/in/sohan-nag)  
GitHub: [@sohan23](https://github.com/sohan23)

---

*Last Updated: October 2025*
