\# Humanitarian GIS Crisis Response Simulation



End-to-end GIS workflow for disaster response. Learn how humanitarian organizations process crisis data: from aerial imagery to field observations to spatial analysis to decision-support maps.



\## Overview



This project simulates a complete GIS response to a humanitarian crisis:



1\. \*\*Aerial Imagery\*\* - Download and process satellite/drone imagery from OpenAerialMap

2\. \*\*Field Data\*\* - Generate realistic field agent damage assessments using AI generated data

3\. \*\*Database\*\* - Store observations in PostGIS (PostgreSQL + spatial extensions)

4\. \*\*Analysis\*\* - Run spatial queries to understand impact and resource needs

5\. \*\*Output\*\* - Create maps, reports, and decision-support visualizations



\## Getting Started



\### Prerequisites

\- Git

\- Docker Desktop

\- Python 3.11+



\### Installation



Clone the repository:

```powershell

git clone https://github.com/jtste/humanitarian-gis-simulation.git

cd humanitarian-gis-simulation

```



Start PostgreSQL in Docker:

```powershell

docker-compose up -d

```



Install Python dependencies:

```powershell

python -m venv venv

venv\\Scripts\\activate

pip install -r requirements.txt

```



Load the database schema:

```powershell

docker exec -it gis-sim psql -U gisadmin -d crisis\_response -f sql/01\_schema.sql

```



\## Project Structure

humanitarian-gis-simulation/

├── README.md                    # This file

├── docker-compose.yml           # PostgreSQL + PostGIS setup

├── requirements.txt             # Python dependencies

├── sql/

│   ├── 01\_schema.sql           # Database schema

│   ├── 02\_sample\_data.sql      # Test data

│   └── 03\_analysis\_queries.sql # Common queries

├── python/

│   ├── load\_osm\_data.py        # Load base layers

│   ├── load\_damage\_reports.py  # Load field data

│   └── export\_geojson.py       # Export for maps

├── data/

│   ├── raw/                    # Imagery, shapefiles (don't commit)

│   ├── processed/              # GeoJSON outputs

│   └── sample/                 # Small test datasets

└── docs/

├── DATABASE\_SCHEMA.md      # Table documentation

└── SETUP.md                # Detailed setup guide



\## Tech Stack



\- \*\*Version Control\*\*: Git + GitHub

\- \*\*Database\*\*: PostgreSQL 16 + PostGIS 3.4 (via Docker)

\- \*\*Data Processing\*\*: Python (geopandas, psycopg2, rasterio)

\- \*\*Base Data\*\*: OpenStreetMap

\- \*\*Imagery\*\*: OpenAerialMap

\- \*\*Output\*\*: GeoJSON (web maps), CSV (reports)



\## Learning Objectives



\- Design spatial databases for crisis response

\- Process multi-source geospatial data

\- Run PostGIS queries for decision support

\- Build reproducible, documented infrastructure

\- Communicate technical GIS work professionally



\## Status



🚧 \*\*In Development\*\*

\- \[x] Git + GitHub setup

\- \[x] Repository cloned

\- \[ ] Docker + PostgreSQL setup

\- \[ ] Database schema

\- \[ ] Data loading

\- \[ ] Spatial analysis

\- \[ ] Web maps and reports



\## Author



Jake Stenson



\## License



MIT - See LICENSE file for details





