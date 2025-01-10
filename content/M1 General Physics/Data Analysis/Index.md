---
longform:
  format: scenes
  title: Data Analysis
  sceneFolder: /
  scenes: []
  ignoredFiles: []
---
## Intro microwave sky
- Signals in the sky, from different sources and redshift 
- Component separation from different signals of different frequencies
- Data from Planck
- Python tools to use the data are available
- around 100 Hz

- Cosmic Microwave Background

All the sources emitted microwaves:
- Galatic dust from our galaxy: emission from interstellar dust grains mostly made of graphites, silicatess and PAHs
- Free free emission from our Galaxy: emission of electrons when deflected by massive ions
- Synchrotron from our Galaxy: emission of relativistic electron gyrating in magnetic field
- Emission from extra-galactic sources (AGN, galaxies)
- Sunyaev Zeld's ovich effect
- Cosmic infrared background
- Detector noise

### Goal
We want to remove everythings before CMB
1. Reproduce the SED maps
2. Build the final CMB maps from 9 frequency maps

### Planck
Planck satellite
- Launched in 2009. Observed the sky 5 times: 2.5 years (no coolant anymore)
- HFI: 100 143 217 353 545 857 (much more sensitive)
- LFI: 30 44 70 (more noise -> not use in exercise)

So we have 6 maps in HFI

### PSF
Point Spread Function (PSF)
- Problem with Airy diffraction disk
- FWHM ~ $\lambda / D$
- Not the same resolution for all bands

## Healpix
- A map is a vector 
- Number of pixels = 12  * Nside * Nside
- Projection = Mollwide
- Nside is the number of cut
- Healpy

1. low
2. Remove the dipole 
3. Same resolution


