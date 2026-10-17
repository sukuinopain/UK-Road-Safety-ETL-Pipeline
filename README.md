# UK Road Safety - Scalable ETL Pipeline

An end-to-end **ETL Pipeline** built with Python, Pandas, and SQLite to process **4.2+ million records** (~1.35 GB) from the UK Road Safety dataset.

## Key Features
- **Memory-Efficient Extraction**: Chunked processing (`100,000` rows per batch) handling `latin1` encoding.
- **Data Sanitization**: Unified missing value labels, decoded vehicle type codes, and filtered extreme numeric outliers in engine capacity and vehicle age.
- **Relational Storage & Indexing**: Loaded into SQLite (`accidents` & `vehicles` tables) with global deduplication and B-Tree indexing (`UNIQUE INDEX` on `Accident_Index`).
- **Automated Reporting & Visualization**: SQL aggregations (`JOIN`, `GROUP BY`, `COUNT DISTINCT`, `CASE WHEN`) exported to multi-sheet Excel, CSVs, and a 4-panel visual dashboard.

## Dataset Source
Raw CSV files exceed GitHub's 100MB limit and are excluded via `.gitignore`. Download from Kaggle:
- [UK Road Safety: Accidents and Vehicles](https://www.kaggle.com/datasets/tsiaras/uk-road-safety-accidents-and-vehicles)

## Generated Outputs Included in Repo
- `UK_Road_Safety_Summary_Report.xlsx` (Multi-sheet Excel report)
- `Yearly_Severity_Summary.csv`
- `Speed_and_Area_Analysis.csv`
- `Vehicles_and_Drivers.csv`
- `Top_Vehicle_Makes.csv`
- `UK_Road_Safety_Dashboard.png`
