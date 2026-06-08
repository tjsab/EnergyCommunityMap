Energy Community Eligibility Map (Final Package)

What this package contains
- Tract overlay: Coal-closure eligible tracts (from coal_closure_tracts.csv)
- County overlay: FFE eligible counties (from the 'June 2025 FFE' sheet)
- Hover tooltips + click-to-zoom + search (tract GEOID or county FIPS)

FILES
- index.html, style.css, app.js
- data/tracts.json (your tract boundaries)
- data/coal_closure_geoids.json (deduped 11-digit tract GEOIDs)
- data/ffe_county_fips.json (deduped 5-digit county FIPS)
- data/counties.geojson (placeholder: replace with county GeoJSON)

HOW TO RUN (important)
Browsers block fetch() from local files. Run a tiny local web server:

Option 1 (Python, recommended)
1) Open a terminal in this folder
2) Run:  python -m http.server 8000
3) Open: http://localhost:8000

Option 2 (VS Code)
- Install 'Live Server' extension and click 'Go Live'

COUNTY FILE NOTE
To see county shading, replace data/counties.geojson with a county GeoJSON that includes:
- properties.GEOID  (5-digit county FIPS)
- properties.NAME   (county name)
- optional properties.STUSPS

If you only have cb_2024_us_county_5m.zip (shapefile), you can use mapshaper.org:
1) Upload cb_2024_us_county_5m.zip
2) Export -> GeoJSON -> save as counties.geojson
3) Drop into data/ (overwrite placeholder)

