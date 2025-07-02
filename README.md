# BASE DE DADOS AVANÇADAS - Project 08

## Authors
- Afonso Baptista - fc58213
- Miguel Borges - fc58187
- Miguel Dinis - fc58198
- Rafael Correia - fc58256

---

## Project Description
This project explores advanced database concepts by comparing the performance and design of MongoDB and MySQL databases for football match data. The project covers data cleaning, schema design, data insertion, query optimization, and performance benchmarking. Both basic and optimized database schemas are implemented, and the impact of indexes is analyzed.

---

## Project Structure
- `BDAProject_08.ipynb`: Main Jupyter notebook with all code, analysis, and results
- `goalscorers.csv`, `results.csv`, `shootouts.csv`: Raw data files
- `docs/`: Documentation and reports
    - `report.pdf`: Full project report
    - `BDAP2__UML.pdf`: UML diagrams
    - `BDAReportCheckpoint1.docx`: Checkpoint report

---

## Requirements

### Python Packages
- pandas
- pymongo
- sqlalchemy
- mysql-connector-python
- bson

You can install all requirements with:
```bash
pip install pandas pymongo sqlalchemy mysql-connector-python bson
```

### Database Requirements
- **MongoDB**: Running locally on default port (27017)
- **MySQL**: Running locally on default port (3306), with a user `root` and password as set in the notebook (e.g., `olaolaola`)

---

## How to Run the Project

1. **Install all Python dependencies** (see above).
2. **Start MongoDB and MySQL servers** on your machine.
3. **Open `BDAProject_08.ipynb` in Jupyter Notebook or VS Code**.
4. **Run all cells sequentially**. The notebook will:
    - Clean and preprocess the data
    - Create and populate MongoDB and MySQL databases (basic and optimized schemas)
    - Run and time a set of queries (simple and complex)
    - Apply indexes and compare performance
    - Print results and performance tables

---

## Project Details

### Data Cleaning
- Handles missing values and data types in all CSVs
- Ensures referential integrity between matches, goalscorers, and shootouts

### MongoDB Implementation
- **Basic Schema**: All match data in a single collection
- **Optimized Schema**: Separate collections for matches, goalscorers, and shootouts
- **Indexes**: Created for query optimization
- **Queries**: Simple (e.g., matches with Portugal), complex (e.g., update based on aggregate conditions)

### MySQL Implementation
- **Basic Schema**: Single table for matches, with related tables for goalscorers and shootouts
- **Optimized Schema**: Normalized tables for locations, details, matches, goalscorers, and shootouts
- **Indexes**: Created for query optimization
- **Queries**: Simple and complex, including updates and inserts based on aggregate conditions

### Performance Comparison
- All queries are timed and results are compared in tabular format
- The impact of schema optimization and indexes is analyzed

---

## References
- See `docs/report.pdf` for a detailed explanation, results, and discussion
- See `docs/BDAP2__UML.pdf` for database diagrams

---

## Notes
- Make sure your database servers are running before executing the notebook
- If you change database credentials or ports, update them in the notebook accordingly
- The notebook is self-contained and will recreate databases as needed

---

For any questions, refer to the report or contact the project authors.