# PlotLedger

The Future of Parcel Intelligence

PlotLedger is an open-source AI-powered platform that aggregates, analyzes, and visualizes large land parcels (9+ acres) across the United States. It connects ownership records, sale history, zoning classifications, permits, and special privileges, providing a single, comprehensive view for developers, planners, researchers, and enthusiasts.

Features

National Parcel Directory

Identify all parcels ≥9 acres in every U.S. state.

Merge contiguous parcels owned by the same entity.

Ownership & Sale History

Track current and historical owners.

View past sales, transaction dates, and prices.

Zoning & Special Privileges

Compare parcels against local zoning laws.

Detect special allowances, variances, density bonuses, and conditional use approvals.

Permits & Applications

Connect each parcel to historical permits and active applications.

Flag deviations from standard zoning rules.

AI Analysis

Automatically parse zoning codes and permit text.

Score parcels for development potential and legal deviations.

Predict opportunities for future permits and special privileges.

Interactive Map Visualization

Explore parcels with Mapbox/Leaflet.

Color-code by zoning, privilege tier, or development score.

Search and filter by state, county, owner, or parcel size.

State-by-State Modular Design

Each state is a module: easily add, update, or expand.

Supports future global expansion.

Installation
# Clone the repository
git clone https://codeberg.org/RoxanneA/PlotLedger.git
cd PlotLedger

# Install dependencies
pip install -r requirements.txt

# Initialize database (PostGIS recommended)
python initialize_db.py

# Start backend server
python app.py

# Open frontend in browser
# Default: http://localhost:3000
Usage

Load parcel data for your state via the GIS ingestion scripts.

Merge contiguous parcels and verify ownership data.

Run AI analysis to detect zoning deviations, special privileges, and permits.

Visualize parcels in the interactive map.

Export parcel reports or share datasets with collaborators.

Data Sources

County GIS portals for parcel boundaries

County property appraisers for ownership and sale history

Municipal permit and zoning portals

Public legal records for special district and variance documentation

Note: Ensure compliance with local open-data licenses. Personal contact info is not included to protect privacy.

Contributing

PlotLedger is fully open-source under the GNU Affero General Public License v3.0+ (AGPL-3.0+). Contributions are welcome:

Add new county/state datasets

Improve AI algorithms for zoning analysis

Enhance frontend map features

Add predictive scoring models

Please submit pull requests and issues via Codeberg.

License

GNU Affero General Public License v3.0+
See LICENSE
 for full details.

Contact & Community

Project repository: Codeberg/PlotLedger

Join discussions, share datasets, and contribute improvements.

Follow updates on AI-powered parcel analysis and national zoning insights.

PlotLedger — The Future of Parcel Intelligence.