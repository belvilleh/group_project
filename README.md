# Educational Inequality Study

## Project Description

This project addresses inequality of educational opportunity in U.S. high schools. Here we will focus on average student performance on the ACT or SAT exams that students take as part of the college application process.
## Project Overview

This project addresses inequality of educational opportunity in U.S. high schools. Here we will focus on average student performance on the ACT or SAT exams that students take as part of the college application process.

We expect a range of school performance on these exams, but is school performance associated with socioeconomic factors?

This is a broad question that we will make more precise as we consider how we want to answer the question and what data are available. Additionally, each of you will personalize the question by adding a data set to the data I will provide you with.

- **Objective:** Focus on average student performance on the ACT or SAT exams that students take as part of the college application process and determing whether there is a socioeconomic tie.
- **Domain:** Education, Economics, Politics
- **Key Techniques:** Summary statistical and visualization analysis and potentially hypothesis testing and inferences.

---

## Project Structure

```
├── data/                 # Raw and processed data
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Generated reports and visualizations
├── requirements.txt      # Python Dependencies
└── README.md             # Project documentation
```

---

## Data

- **Source:** https://www.edgap.org/#4/37.71/-95.99
- **Description:** data set from 2016 includes information about average ACT or SAT scores for schools and several socioeconomic characteristics of the school district
- **License:** NA


- **Source:** https://nces.ed.gov/ccd/pubschuniv.asp
- **Description:** This data set consists of basic identifying information about schools
- **License:** NA

- **Source:** https://www2.census.gov/geo/pdfs/maps-data/maps/reference/us_regdiv.pdf?utm_source=chatgpt.com
- https://www.census.gov/library/reference/code-lists/ansi.html#state
- **Description:** Maps each U.S. state and D.C. to its Census region and Census division, with state postal abbreviations and FIPS codes. Used to group schools and summarize ACT results by geographic region. This lookup table is derived from the official Census region/division definitions and ANSI/FIPS state codes. No data values were modified beyond formatting into a simple CSV structure for analysis.
- **License:** NA

- **Source:** https://nces.ed.gov/programs/digest/d17/tables/dt17_226.60.asp
- **Description:** Provides average ACT composite scores and percent of graduates tested by state for the class of 2016. Used to add context to regional analysis—recognizing that ACT participation rates differ widely by state (which influences average scores). Values for 2016 (composite and participation) were extracted directly from the NCES table and combined with the Census region/division data for consistency in analysis.
- **License:** NA
---

## Analysis


This project takes data sets containing information on schools, the socioecomonic indicators for those schools, and ACT/SAT scores. The analysis consisted of taking the files and converting into two dataframes. We analyzed the data in those dataframes to ensure that the data was consistant and could give us the answers we were looking to get from the data.

- Education_Analysis.ipynb contains all the code necessary to run and analyze the data files. 
- EdGap_data.xlsx, ccd_sch_029_1617_w_1a_11212017.csv, and XXX located in the data directory are the only files used in the analysis. 
- Some data set will be created as a result of the analysis. 

The 2016 ACT and socioeconomic data were selected intentionally to maintain alignment across all sources used in this project. The EdGap_data.xlsx dataset represents conditions and outcomes from 2016, and the accompanying NCES Common Core of Data file covers the 2016–2017 academic year.
Although more recent ACT data (through 2023) are available from NCES, the 2016 data were retained for three reasons:
- Temporal consistency — All primary data sources describe the same time period, allowing for coherent analysis without cross-year bias.
- Comparability — The 2016 ACT data have been widely used in previous research and coursework, making it easier to compare new findings with established benchmarks.
- Reproducibility — Because the 2016 datasets are well-documented and publicly archived, results can be reproduced and verified by others.

Future iterations of this project could extend the analysis by incorporating more recent ACT data (e.g., 2018–2023) to examine trends over time, but this version focuses on methodological integrity and alignment within the 2016 data scope.

---

## Results

TBD

---

## Authors

- Paul Skentzos - [@gpskentzos](https://github.com/gpskentzos)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- Data sets: 
  - https://www.edgap.org/#4/37.71/-95.99
  - https://nces.ed.gov/ccd/pubschuniv.asp

- Tutorials or papers referenced

- Inspiration or collaborators
	- Seattle University DATA 5100 Course