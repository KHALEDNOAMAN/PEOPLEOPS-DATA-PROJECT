# PeopleOps Data Project - Pipeline Guide

## Pipeline Architecture
```
Raw CSV --> Python ETL --> Data Cleaning --> SQLite Warehouse --> Analysis
              |               |                   |
         Pandas           Null Handling      SQL Queries
         Validation       Type Casting       Aggregations
```

## Data Transformations
| Step | Tool | Description |
|------|------|-------------|
| Extract | pandas.read_csv | Load raw HR data |
| Clean | pandas | Handle nulls, fix types |
| Transform | pandas | Derive metrics, normalize |
| Load | sqlite3 | Insert into warehouse |
| Analyze | SQL | Query insights |

## HR Metrics
| Metric | Description |
|--------|-------------|
| Headcount | Total employees over time |
| Turnover Rate | Attrition percentage |
| Tenure | Average employment duration |
| Department Stats | Per-department analytics |

## Quick Start
```bash
git clone https://github.com/MrAbdulSamadDEV/PEOPLEOPS-DATA-PROJECT.git
pip install pandas
python main.py
```