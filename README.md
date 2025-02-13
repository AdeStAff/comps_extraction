# Data and AI Regulation

## I. General context

In their advisory roles, tax lawyers may need to conduct market studies to understand the profitability of companies within a specific industry.

In such cases, tax lawyers perform searches for comparable companies (commonly referred to as "benchmarking studies") using information available in databases such as Orbis or TP Catalyst (owned by Moody's). These analyses are conducted in two key steps:
- Extraction of data (Step 1): Information related to a sample of target comparable companies is retrieved using the search engines within the databases.
- Manual analysis (Step 2): The data for each company is analyzed manually using Excel to determine which companies are comparable. Companies are included or excluded based on their activity descriptions and websites, as provided in the databases.

## II. Objectives
- Understand the primary challenges faced by legal service providers when integrating AI technologies.
- Identify AI methods that align with responsible AI principles for deployment in legal operations.
Design a high-level solution (POC) for a case study within the field of tax law.

## III. Task 
Currently, most organizations perform Step 1 using search engines provided by database vendors, which deliver reliable and efficient results. However, Step 2 remains labor-intensive and time-consuming, mainly due to the manual review of each company's website.

Your objective is to propose an approach that aligns with responsible AI principles to optimize Step 2 of the benchmarking process. This step involves analyzing company information extracted from the database to improve both efficiency and accuracy.

## IV. Instructions and Material
You have access to an Excel file extracted from the TP Catalyst database. This file contains a list of 490 independent (uncontrolled) companies1 operating in the "clothing sales" sector across Europe, North Africa, and the Middle East. The Excel file includes three tabs:

**1st Tab**: "Research Steps" – This tab summarizes the research process conducted in TP Catalyst, which resulted in the selection of 490 companies.

**2nd Tab**: "Results and Filters" – This tab presents the list of companies along with qualitative information (e.g., address, activity code, activity description, website) and quantitative data (e.g., operating results and turnover). The last three columns in the table apply quantitative filters to exclude companies lacking sufficient financial data or those that reported losses during the 2019–2021 period.

**3rd Tab**: "Revised Sample" – This tab contains the 407 companies that remain after applying the quantitative filters.

Your analysis will focus on the 407 companies in the "Revised Sample" tab. Your objective is to identify a reduced sample of approximately 40 companies that are primarily engaged in luxury clothing sales. These companies may also, as a secondary activity, operate in luxury shoes, watches, jewelry, and bags. Companies that do not meet these criteria should be excluded based on objective factors, such as:
-  **Product comparability**: Companies focused on sportswear or mid-range clothing may be excluded.
- **Functional comparability**: Companies involved in manufacturing or designing clothing may also be excluded.

You are free to define the selection criteria as long as they are justified, and the rejected companies are clearly documented. The key aspect of this exercise is to develop a reliable and explainable selection process, independently of the results obtained.

At the end of the exercise, we will then compare your results with those obtained through our own manual review to discuss the results together.

# Run notebook

Run the following in your terminal before anything
```bash
uv venv aireg_env --python=3.12
source aireg_env/bin/activate # Activate it
uv pip install -e . # Use the pyproject.toml to install dependencies
```

Then run the [data_extraction notebook](data_extraction.ipynb).