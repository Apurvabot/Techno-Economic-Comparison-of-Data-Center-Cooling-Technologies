# Techno-Economic-Comparison-of-Data-Center-Cooling-Technologies
Hourly techno-economic modeling of data center cooling using magnetic bearing chillers, water-side economizers, and aquifer thermal energy storage (ATES).

# Techno-Economic Comparison of Data Center Cooling Using Magnetic Bearing Chillers and Aquifer Thermal Energy Storage

This repository contains the modeling framework, data, and supporting materials developed for the published research paper:

**"Techno-Economic Comparison of Data Center Cooling Using Magnetic Bearing Chillers and Aquifer Thermal Energy Storage"**

**Authors:** Apurva Malpure, Andrew Stumpf, Upasana Pandey, Yu-Feng Lin, and Craig Bradshaw

**Journal:** *Energies*, 2026

**Published Paper:**  
https://doi.org/10.3390/en19173947

---

## Overview

This research evaluates the energy and economic performance of alternative data center cooling technologies under different climatic conditions.

An hourly simulation framework is used to compare three cooling configurations:

1. Conventional water-cooled centrifugal chiller
2. Magnetic bearing chiller (MBC)
3. Magnetic bearing chiller integrated with aquifer thermal energy storage (MBC + ATES)

The analysis is performed for **Phoenix, Arizona** and **Fairbanks, Alaska**, representing contrasting U.S. cooling climates.

The model evaluates the interaction between data center cooling load, outdoor weather conditions, water-side economizer operation, chiller performance, auxiliary equipment, and ATES-assisted cooling.

---

## Key Features

- 8,760-hour annual cooling-system simulation
- Climate-sensitive cooling performance
- Hourly dry-bulb, relative humidity, and wet-bulb calculations
- Water-side economizer (free-cooling) modeling
- Temperature- and part-load-dependent chiller COP
- Centrifugal and magnetic bearing chiller comparison
- Screening-level ATES dispatch model
- CRAH, pump, cooling-tower, and ATES pumping loads
- Cooling-only PUE analysis
- Annual energy consumption and peak-demand comparison
- Capital and operating cost analysis
- NPV, IRR, discounted savings, and simple payback calculations

---

## Study Locations

### Phoenix, Arizona
Represents a hot and dry climate with greater dependence on mechanical cooling.

### Fairbanks, Alaska
Represents a cold continental climate with substantially greater water-side economizer/free-cooling availability.

The same IT load profile and cooling-system capacity are used for both locations so that the effect of climate and cooling-system operation can be compared consistently.

---

## Modeling Framework

The hourly cooling dispatch follows the general sequence:

**Cooling Load → Water-Side Economizer → ATES (when applicable) → Mechanical Chiller**

The model calculates hourly:

- IT and cooling load
- Outdoor wet-bulb temperature
- Cooling-tower water temperature
- Water-side economizer contribution
- ATES discharge
- Remaining mechanical chiller load
- Chiller COP and electricity consumption
- CRAH fan power
- Pump power
- Cooling-tower fan power
- Total cooling-system electricity consumption
- Cooling-only PUE

Hourly results are aggregated to calculate annual energy, peak demand, and financial performance.

---

## Main Findings

Under the modeled assumptions, magnetic bearing chillers reduced annual cooling electricity consumption relative to the conventional centrifugal chiller baseline in both climates.

The reduction was greater in Phoenix because mechanical cooling was required for substantially more hours during the year.

The MBC + ATES configuration was evaluated as a **screening-level, discharge-assisted cold-storage scenario**. It should not be interpreted as a complete seasonal ATES design because seasonal charging, cyclic storage operation, and site-specific hydrogeological modeling were outside the scope of this study.

The results demonstrate that the performance and economics of advanced data center cooling technologies depend strongly on climate, free-cooling availability, electricity prices, equipment performance, storage assumptions, and operating strategy.

---

## How to Use the Repository

The required input data files are included in this repository.

Before running the notebooks, update the input file paths in the Python code so that they point to the appropriate data files on your local computer.

Make sure all Python packages imported by the notebooks are installed in your Python environment.

Run the notebooks in the following order:

### 1. `Clean CRAH Financial Comparison Model.ipynb`

Runs the primary hourly cooling-system model and compares the conventional centrifugal chiller and magnetic bearing chiller configurations.

The notebook calculates cooling loads, water-side economizer operation, chiller performance, auxiliary equipment electricity consumption, annual cooling electricity use, peak demand, cooling-only PUE, and financial performance.

### 2. `Fin model with ATES.ipynb`

Extends the cooling-system model to include the screening-level ATES configuration.

The notebook models ATES discharge, storage state of charge, pumping requirements, remaining chiller load, and the resulting energy and economic performance.

### 3. `chapter4_plots.ipynb`

Processes the simulation results and generates the figures and comparative plots used to analyze the cooling configurations across Phoenix and Fairbanks.

---

## Report and Manuscript

The repository includes a **Reports** folder containing research outputs and supporting documentation.

The LaTeX source files used to prepare the research report/manuscript are also included and can be compiled to reproduce the formatted document.

For the final peer-reviewed publication, please refer to:

https://doi.org/10.3390/en19173947

---

## Citation

If you use this model, code, or results in academic work, please cite the published paper:

**Malpure, A.; Stumpf, A.; Pandey, U.; Lin, Y.-F.; Bradshaw, C.**  
*Techno-Economic Comparison of Data Center Cooling Using Magnetic Bearing Chillers and Aquifer Thermal Energy Storage.*  
Energies, 2026.

https://doi.org/10.3390/en19173947



## Research Scope

The ATES implementation in this repository represents a screening-level model rather than a site-specific seasonal ATES design.

Future extensions of this work include sensitivity analysis, seasonal ATES charging and discharging, operational optimization, time-of-use electricity pricing, demand charges, and site-specific hydrogeological constraints.


## Contact

**Apurva Malpure**

For questions regarding the model, methodology, or research, please connect with me through LinkedIn:

https://www.linkedin.com/in/apurva-malpure01
