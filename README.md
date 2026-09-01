# FOWT Bidirectional TMD Dataset

## Overview

This repository contains the simulation data and supplementary results associated with the manuscript:

**"Evolutionary Optimization of Bidirectional TMDs to Enhance Floating Wind Turbine Stability Under Adverse Offshore Conditions"**

submitted to **IEEE Transactions on Sustainable Energy**.

The dataset supports the numerical investigation of a bidirectional tuned mass damper (TMD) system installed in the nacelle of a floating offshore wind turbine (FOWT) with a barge-type platform.

The proposed control system consists of TMDs acting in the fore-aft and side-to-side directions. Their parameters were optimized using a Genetic Algorithm (GA), and their performance was evaluated through aero-hydro-servo-elastic simulations under turbulent wind and irregular wave conditions.

This repository provides the environmental conditions, relevant optimization settings, simulation input/output files, and supplementary figures associated with the results reported in the manuscript.

---

## Repository Structure

The repository is organized into four main directories:

### 01_Environmental_Conditions

Contains the environmental conditions used in the simulations.

#### Wind_Profile_1

Contains the TurbSim files associated with Wind Profile 1, including:

- TurbSim input file (`.inp`)
- TurbSim summary file (`.sum`)
- Generated turbulent wind field (`.wnd`)

Wind Profile 1 corresponds to the lower wind-speed condition investigated in the study.

#### Wind_Profile_2

Contains the corresponding TurbSim files for Wind Profile 2.

Wind Profile 2 represents the more severe wind condition investigated in the study.

#### Wave_Conditions

Contains a Markdown file describing the irregular wave conditions adopted in the simulations.

The wave conditions are specified directly within the hydrodynamic simulation configuration and are therefore documented separately in this directory.

---

### 02_Optimization_Parameters

Contains information about the Genetic Algorithm configuration used for the optimization of the bidirectional TMD system.

The file:

`Genetic_Algorithm_Configuration.md`

documents the main GA settings, including population size, number of generations, mutation and crossover operators, elitism, constraint tolerance, and parallel processing configuration.

The optimization was originally performed using **MATLAB R2018**.

The complete MATLAB optimization source code is not included in this repository.

---

### 03_Simulation_Data

Contains the numerical simulation input and output files used to evaluate the optimized TMD configurations.

The data are organized according to:

- Wind Profile 1
- Wind Profile 2
- TMD mass configuration (22 t and 42 t)

The corresponding directories contain:

- FAST-SC simulation input files (`.fst`)
- FAST-SC simulation output files (`.out`)

The `.out` files contain the time-domain numerical responses used to evaluate the structural behavior of the FOWT and to generate the processed results and figures.

Directory organization:

    03_Simulation_Data/
    ├── Profile_1/
    │   ├── TMD_Mass_22t/
    │   └── TMD_Mass_42t/
    │
    └── Profile_2/
        ├── TMD_Mass_22t/
        └── TMD_Mass_42t/

---

### 04_Processed_Results

Contains supplementary figures generated from the simulation output data provided in `03_Simulation_Data`.

These figures complement the results presented in the associated manuscript and provide additional visualization of the dynamic behavior of the floating wind turbine.

The figures include responses related to:

- tower fore-aft deflection;
- tower side-to-side deflection;
- platform roll;
- platform pitch;
- platform yaw;
- platform surge;
- platform sway;
- platform heave;
- turbulent wind components; and
- irregular wave elevation.

The results are organized according to the same wind-profile and TMD-mass configurations adopted for the simulation data.

The numerical data underlying these figures are available in the corresponding `.out` files in `03_Simulation_Data`. Therefore, separate copies of the processed numerical data are not provided in this directory.

---

## Environmental Conditions

Two turbulent wind profiles were considered:

- **Wind Profile 1:** mean wind speed of approximately 10 m/s
- **Wind Profile 2:** mean wind speed of approximately 18 m/s

The turbulent wind fields were generated using **TurbSim**.

Irregular waves were considered using a **Pierson-Moskowitz spectrum**, with the principal parameters:

- Significant wave height (Hs): **5.0 m**
- Peak spectral period (Tp): **12.4 s**
- Wave direction: **0°**

Additional environmental parameters are provided in the corresponding files under `01_Environmental_Conditions`.

---

## TMD Configurations

The study investigates a bidirectional TMD system composed of:

- **TMDX:** acting primarily in the fore-aft direction;
- **TMDY:** acting primarily in the side-to-side direction.

The optimized bidirectional configuration is referred to as **TMDXY**.

Two TMD mass configurations considered in the study are represented in this dataset:

- **22 t**
- **42 t**

The remaining optimized parameters and design ranges are reported in the associated manuscript, while the principal Genetic Algorithm settings are documented in `02_Optimization_Parameters`.

---

## Simulation Tools

The dataset was generated using the following computational tools:

- **FAST-SC** – aero-hydro-servo-elastic simulation of the floating offshore wind turbine and structural control system;
- **TurbSim** – generation of turbulent wind fields;
- **MATLAB R2018** – Genetic Algorithm optimization and post-processing of simulation results.

The reference floating wind turbine model is based on the **NREL 5-MW reference wind turbine** coupled to a barge-type floating platform.

---

## File Formats

The repository contains the following main file formats:

| Extension | Description |
|-----------|-------------|
| `.fst` | FAST-SC simulation input file |
| `.out` | FAST-SC time-domain simulation output |
| `.inp` | TurbSim input configuration |
| `.sum` | TurbSim simulation summary |
| `.wnd` | TurbSim-generated turbulent wind field |
| `.png` | Supplementary processed figures |
| `.md` | Dataset documentation |

Most text-based simulation files can be inspected using a standard text editor.

---

## Relationship to the Associated Manuscript

This repository is intended to provide supporting data for the results reported in the associated IEEE manuscript.

The repository does not reproduce every intermediate file generated during the broader research project. Instead, it provides the simulation data, environmental conditions, optimization information, and supplementary results directly relevant to the analyses reported in the manuscript.

Some supplementary figures included in `04_Processed_Results` were not included in the manuscript because of space limitations. They are provided here to offer additional visualization of the simulated FOWT responses.

---

## Data Reuse

Users of this dataset should cite the associated manuscript when using the data, simulation results, or supplementary material in academic work.

Citation information will be updated after publication of the associated manuscript.

---

## Authors

**Thayza Marcela Van Der Laan Melo**  
Centro Federal de Educação Tecnológica Celso Suckow da Fonseca (CEFET/RJ)  
Rio de Janeiro, Brazil

Additional authors and affiliations are provided in the associated manuscript.

L. F. Almeida is with the Electronic Engineering Department, Centro 
Federal de Educação Tecnológica Celso Suckow da Fonseca (CEFET-RJ), Rio 
de Janeiro, RJ, Brazil (e-mail: luciana.almeida@cefet-rj.br). 

J. G. Lazo Lazo is with the Academic Department of Engineering, 
Universidad del Pacífico, Lima, Peru. (e-mail: jg.lazol@up.edu.pe).

## Contact

For questions regarding this dataset, please contact:

**Thayza Marcela Van Der Laan Melo**  
CEFET/RJ  
Rio de Janeiro, Brazil  
Email: thayza.melo@cefet-rj.br