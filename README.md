# Retail-Expansion-and-Inventory-Intelligence-Platform

# Retail Analytics Suite

##  Table of Contents
- [Features](#-features)
- [Installation](#-installation)
- [Configuration](#-configuration)
- [Usage](#-usage)
- [Testing & Debugging](#-testing--debugging)
- [File Structure](#-file-structure)
- [Dependencies](#-dependencies)
- [API Keys](#-api-keys)
- [Troubleshooting](#-troubleshooting)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)
<img width="1770" height="749" alt="image" src="https://github.com/user-attachments/assets/3692124b-ff33-48bc-b844-d976a06e6994" />


##  Features

###  Site Selector Pro
- AI-powered location analysis for optimal new store placement
- Demographic profiling with US Census data integration
- Competitor mapping within customizable radius (1-50 miles)
- Financial modeling with break-even calculations
- Interactive Folium maps with top candidate locations

###  Demand Shock Simulator
- Festival impact modeling (Diwali, Thanksgiving, etc.)
- Weather condition analysis (snow, heatwave, rain)
- Discount impact projections
- State-specific demand patterns
- Visualization of demand changes

###  Inventory Prediction
- LightGBM machine learning forecasting
- Time-series analysis with lag features
- Store clustering based on demographics
- Interactive Plotly dashboards
- Excel/CSV report generation

###  Debugging Tools
- API connection testers (Gemini, Census)
- End-to-end system debug script
- Map visualization inspection
- Sample test cases with known-good parameters

##  Installation

```bash
# Clone repository
git clone https://github.com/yourusername/walmart-analytics-suite.git
cd walmart-analytics-suite

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

⚙ Configuration
1 Create config.yaml with:
apis:
  census:
    key: "your_census_api_key_here"
  gemini:
    key: "your_gemini_api_key_here"
analysis:
  budget: 80               # $/sqft
  break_even_months: 36    # 3 years
  search_radius_miles: 15  # Default radius
2 Or set environment variables:
export CENSUS_KEY="your_key"
export GEMINI_KEY="your_key"

```
Run code:
```bash
streamlit run enhancedintegratedapp.py
```
DEBUG TOOLS:
# Test Gemini API
python debug_gemini.py

# Test Census API
python test_census.py

# Full system test
python debug.py  # Generates debug_map.html


 Testing & Debugging
Script	Purpose	Output
debug.py	Full system test	HTML map, console log
debug_gemini.py	Gemini API test	Connection status
test_census.py	Census API test	Sample demographic data


Sample debug output:
 Starting DEBUG TEST V3
1. Testing Engine Initialization... 0.45s
2. Testing Location Generation... 5 locations
3. Testing Analysis... 3 valid locations
4. Testing Visualization... Map saved


 File Structure
```bash
walmart-analytics-suite/
├── core/
│   ├── analysis_engine.py       # Main analysis logic
│   ├── data_fetcher.py          # API data fetching
│   └── model_utils.py           # ML utilities
├── utils/
│   ├── geo_utils.py             # Mapping functions
│   └── visualization.py         # Plotting tools
├── tests/
│   ├── debug.py                 # System test
│   ├── debug_gemini.py          # API test
│   └── test_census.py           # Census test
├── enhancedintegratedapp.py     # Streamlit app
├── config.yaml                  # Configuration
└── requirements.txt             # Dependencies

Dependencies:
Python==3.8+
streamlit==1.29.0
pandas==2.0.3
numpy==1.24.3
folium==0.14.0
plotly==5.15.0
lightgbm==4.1.0
scikit-learn==1.3.0
geopy==2.3.0
requests==2.31.0
pyyaml==6.0
```
 API Keys Required:	

-US Census	Demographic data	

-Gemini AI	Location explanations

-OpenStreetMap	Competitor locations	



 Troubleshooting

Problem: Gemini API not responding

-Run python debug_gemini.py

-Verify key in config.yaml and Google Cloud Console


Problem: No locations found

-Increase search_radius_miles in config

-Check debug.py for working parameters

Problem: Map not displaying

-Verify Folium version matches requirements

-Inspect generated debug_map.html


 Contributing
Fork the repository

Create feature branch (git checkout -b feature/improvement)

Commit changes (git commit -m 'Add amazing feature')

Push to branch (git push origin feature/improvement)

Open Pull Request

 Contact
Arya
aryarsoni2020@gmail.com

Screenshots:
<img width="1907" height="989" alt="image" src="https://github.com/user-attachments/assets/17c333ac-fdc4-479f-ae97-ff1753369726" />
<img width="1883" height="866" alt="image" src="https://github.com/user-attachments/assets/cee079ca-d6e4-457a-ab9f-46f805e195b4" />
NOTE:The screenshots below highlight a few of the core features of the project. However, the project includes several additional features that are not shown here.

