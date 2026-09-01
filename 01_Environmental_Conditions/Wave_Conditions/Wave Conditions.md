# Wave Conditions

This directory documents the irregular wave conditions used in the
FAST-SC simulations associated with this dataset.

Unlike the turbulent wind fields, which were generated externally
using TurbSim, the wave conditions were defined directly within the
FAST-SC simulation environment. Therefore, no separate wave input
file is provided in this directory.

## Wave Model

The simulations considered irregular waves represented by the
Pierson-Moskowitz spectrum.

The following parameters were used:

| Parameter | Value | Description |
|---|---:|---|
| Water density (`WtrDens`) | 1025.0 kg/m³ | Water density |
| Water depth (`WtrDpth`) | 150.0 m | Water depth |
| Wave model (`WaveMod`) | 2 | Irregular wave spectrum |
| Wave analysis time (`WaveTMax`) | 3630.0 s | Analysis time for incident wave calculations |
| Wave time step (`WaveDT`) | 0.25 s | Time step for incident wave calculations |
| Significant wave height (`WaveHs`) | 5.0 m | Significant wave height |
| Peak spectral period (`WaveTp`) | 12.4 s | Peak spectral period |
| Peak shape parameter (`WavePkShp`) | 1.0 | Corresponds to the Pierson-Moskowitz spectrum |
| Wave direction (`WaveDir`) | 0.0° | Incident wave propagation direction |
| Random seed 1 (`WaveSeed(1)`) | 123456789 | First random seed |
| Random seed 2 (`WaveSeed(2)`) | 1011121314 | Second random seed |

## FAST-SC Input Files

The complete FAST-SC input files corresponding to the final
simulation cases are provided in the `03_Simulation_Data` directory.

These files contain the complete simulation configuration and can be
consulted for additional model and numerical parameters not reproduced
here.

For further information regarding the environmental conditions and
simulation methodology, please refer to the associated manuscript.