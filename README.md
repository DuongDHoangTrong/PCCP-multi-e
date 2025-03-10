# Data Description

## Overview
This dataset contains simulation results for electron dynamics under laser interaction from ***Effects of laser parameters on orbital competition in
high-order harmonic generation from hydrogen cyanide molecule***. Each file is named in the format:

```
I=...-L=...-Np=...
```

where:
- `I` represents the intensity of the laser field.
- `L` represents the wavelength of laser.
- `Np` represents the number of optical cycles.

The data is organized into two folders:
- **HOMO/**: Contains data for the highest occupied molecular orbital (HOMO).
- **HOMO-1/**: Contains data for the second highest occupied molecular orbital (HOMO-1).

Each folder contains `.fort` files with tabular data and `.npy` files representing time-profiles.

## File Formats
### `.fort` Files
Each `.fort` file consists of tabular data with the following columns:

1. **time (a.u.)** - Time in atomic units.
2. **laser (a.u.)** - The electric field of the laser in atomic units.
3. **acc (a.u.)** - The acceleration of the electron.
4. **ion prob** - The ionization probability, calculated according to Eq. (10) in the associated text.
5. **survival** - The survival probability, defined as $$\langle \psi | \psi_0 \rangle$$

### `.npy` Files
Each `.npy` file contains time-profiles. The structure of these files is:
- The **first column** contains the High-Harmonic Generation (HHG) order.
- The **first row** contains the for emission time (in optical cycles).
- The values inside the matrix represent the intensity of the corresponding HHG order at the given emission time.
