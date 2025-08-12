# Investigating NYC's Suppliers of Tropical Hardwood

In this repo, I analyze various data for my master's thesis in the Columbia Journalism School - Data Journalism Program on New York City's use of tropical hardwood. These include:
- U.S. imports data for New York City tropical hardwood contractors and their suppliers from [ImportGenius](https://www.importgenius.com/)
- All greenheart and ekki wood imports between 2006 and 2025 from [ImportGenius](https://www.importgenius.com/)
- [Guyana Forestry Commission Allocation map](https://cadasta.maps.arcgis.com/apps/webappviewer/index.html?id=e543e1d1d8f04bc29e16b448cd0beb76)
- [Cameroon Forest Atlas](https://data-minfof.opendata.arcgis.com/search?groupIds=c710d96159e14e79934236191bc61121)
- [Gabon Forest Atlas](https://gab.forest-atlas.org/pages/maps)
- Cameroon export reports between 2009 and 2021 (excluding 2019) produced by Cameroon’s Ministry of Forestry and Wildlife
- Guyana and Cameroon timber trade data downloaded from the [International Tropical Timber Organization Biennial Review Statistics](https://www.itto.int/biennal_review/)
- Global Land Cover and Land Use Change, 2000-2020 raster data: Layers ‘Forest height, 2020’ and ‘Forest height, 2000’ from [this page](https://glad.umd.edu/dataset/GLCLUC2020) and ‘2000-2020 change’ layer from [this page](https://storage.googleapis.com/earthenginepartners-hansen/GLCLU2000-2020/v2/download.html)
- TREES Act lobbying records from the [New York State Commission on Ethics and Lobbying in Government](https://reports.ethics.ny.gov/publicquery)

I scrape the Guyana map data in notebook 'Scraping Guyana Forestry Commission Forest Allocation Map,' Gabon map in 'Scraping Gabon Forest Atlas - Timber Concessions' and the lobbying data in 'Scraping New York Lobbying Data.' Folders 'cameroon concessions map' and 'guyana concessions map' contain geographical files ad notebooks filtering concessions linked to New York contractors' suppliers.

Imports data was downloaded from [ImportGenius](https://www.importgenius.com/) between Nov. 1, 2006 and mid-2025 and analyzed in various Jupyter notebooks in the 'Ekki:greenheart imports and NY agency importers analyses' folder. Fuzzy matching was used to clean names of importers. Data on species vulnerability from the International Union for Conservation of Nature (IUCN) was merged. An LLM (Gemini) was used in Python to extract out species names from product descriptions.

The folder 'guyana exporters data' contains individual data files with imports from each supplier of post-2013 New York City tropical hardwood contractors. 'US importers data' contains individual imports data for each city contractor, as well as all greenheart and ekki imports to the U.S. 

Raster data on land use change, specificially tree height in 2000 and 2020, was analyzed for Guyana and Cameroon forest concessions in the folder 'tree height satellite analysis - guyana and cameroon.' This folder contains .qgz files from my analysis in QGIS and Jupyter notebooks with my analysis of the unique values tables in Python. 

ITTO data is analyzed in the folder 'ITTO data analysis.'

Additional data was analyzed in Google Sheets.

The full methodology and explanation of calculations behind this project is in the file 'Methodology.'

## Languages, Libraries, and Applications Used:
- Python
- pandas
- geopandas
- requests
- Regular expressions
- Fuzzy matching
- OpenAI
- matplotlib
- numpy
- BeautifulSoup
- Playwright
- mapshaper
- QGIS
- Raster unique values analysis
- Google Sheets



