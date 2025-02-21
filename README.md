# Customer Data Analysis Report with CrewAI

![Project Image](project-image-url)

> A data analysis project using CrewAI to generate insights and visualizations from customer data.

---

### Table of Contents

- [Description](#description)
- [Technologies](#technologies)
- [How To Use](#how-to-use)
- [API Reference](#api-reference)
- [References](#references)
- [License](#license)
- [Author Info](#author-info)

---

## Description

This project utilizes CrewAI to analyze customer data and generate visual insights. The pipeline consists of:

1. Extracting customer data from a CSV file.
2. Performing analysis and generating charts.
3. Compiling the analysis and charts into a comprehensive report.

#### Key Features

- Automated data extraction and cleaning
- Data visualization with Matplotlib and Seaborn
- AI-powered data analysis using CrewAI
- Markdown report generation

#### Objectives

- Identify the professional profile of each gender.
- Calculate the average annual income by profession, weighted by spending score.
- Analyze the relationship between per capita income and years of professional experience.

[Back To The Top](#customer-data-analysis-report-with-crewai)

---

## Technologies

- **Python**
- **CrewAI**
- **LangChain**
- **Matplotlib**
- **Seaborn**
- **Pandas**

[Back To The Top](#customer-data-analysis-report-with-crewai)

---

## How To Use

### Installation

Clone this repository and run the project, the dependencies will automatically install

### Running the Project

```bash
python main.py
```

[Back To The Top](#customer-data-analysis-report-with-crewai)

---

## API Reference

#### Data Extraction

```python
@tool("Load data from csv.")
def read_csv() -> str:
    try:
        df = pd.read_csv("Customers.csv")
        return df.to_string()
    except Exception as e:
        return f"Error fetching data: {str(e)}"
```

#### Chart Generation

```python
@tool("Generates and saves charts.")
def plot_charts() -> List[str]:
    df = pd.read_csv("Customers.csv")
    if not df.empty:
        df = df.dropna()
        # Generate charts...
        return chart_paths
    return ["No valid data."]
```

[Back To The Top](#customer-data-analysis-report-with-crewai)

---

## References

- [CrewAI Documentation](https://crewai.com/docs)
- [LangChain](https://python.langchain.com/)
- [Matplotlib](https://matplotlib.org/)

[Back To The Top](#customer-data-analysis-report-with-crewai)

---

## License

MIT License

Copyright (c) 2024 Otávio Lira Neves

Permission is hereby granted, free of charge, to any person obtaining a copy of this software...

[Back To The Top](#customer-data-analysis-report-with-crewai)

---

## Author Info

- **LinkedIn** - [Otávio Lira Neves](https://www.linkedin.com/in/otavioliraneves/)
- **Gmail** - [otavioliraneves@gmail.com](mailto:otavioliraneves@gmail.com)

[Back To The Top](#customer-data-analysis-report-with-crewai)

