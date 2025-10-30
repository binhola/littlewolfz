---
title: Binh's Hidden Universe 🤫
tags:
  - "#physics"
---
## About me 
My name is **Binh**, and I’m from **Vietnam**.  
I’m currently a **Master 2 student** in [_Nuclei, Particles, Astroparticles and Cosmology_](https://npac.ijclab.in2p3.fr/), and I previously studied _General Physics_ at the **University of Paris-Saclay** in France.

I’m passionate about **cosmology** and **astrophysics**, with a soft spot for **mathematics**. I love exploring the intersection between **theoretical and observational cosmology**, especially through **Bayesian statistics** and **deep learning**. Running simulations, making cool plots, and understanding more about the **universe** are the parts of my work that excite me the most.

In my free time, I enjoy **reading manga**, **watching movies** (Christopher Nolan is my cinematic hero 🎬), and **swimming**. I also love **cats**, and while I like cooking, **onions** and **raw tomatoes** are my Kryptonite.

This little corner of the internet is just to **back up some of my projects and notes** (if I’m not too lazy 😅) from my Master’s and Bachelor’s.
## Projects
### *M1 internship: Galaxy Deblending with VAE-Deblender* 
**Context.** The upcoming data from the Legacy Survey of Space and Time (LSST) at the Vera C. Rubin Observatory is expected to be affected by blending in about two-thirds of galaxies—where light from physically separate galaxies overlaps. This blending reduces the number of galaxies usable for weak lensing studies, making deblending a critical challenge. 

**Aim.** Deblending algorithms aim to address this challenge using pixel-level, multi-band image data and to recover the weak lensing parameters. 

**Method.** We use deep neural networks, including a generative model–Variational Autoencoder (VAE) and a regressor. The autoencoder reduces high-dimensional image data into a low-dimensional latent space and reconstructing the image from this space. While the regressor extracts weak lensing parameters from latent space. 

**Result.** Using six-band simulated data for an LSST-like survey, we successfully developed a VAE to reconstruct isolated galaxies from blended scenes, along with a regressor that learns ellipticities from the latent space. The regressor outperforms the reconstruction by significantly reducing the bias toward round shapes that is present in the reconstructed images. We also applied the trained VAE and regressor to real DES data for evaluation.
- Final Report: [[VAE_deblender_final_report_M1_GP_2025.pdf|Galaxy Deblending with VAE-Deblender]]
- _Presented the talk_ "[Inference of Weak Lensing Parameters from Blended Galaxies using Generative Neural Networks](http://vietnam.in2p3.fr/2025/Cosmology/transparencies/3_wednesday/1_morning/5_nguyen_binh.pdf)" _at the Rencontres du Vietnam 2025 Cosmology Conference.
### Bachelor thesis: Characterization of Instrumental Effects for B-Mode Polarization Measurements of Cosmic Microwave Background.

The Cosmic Microwave Background (CMB) polarization is a crucial tool for probing the mysteries of cosmic inflation through the measurement of primordial B-modes. Achieving this requires meticulous control over instrumental systematic effects. In this research, we present an instrumental model that focuses on two primary effects: intensity-to-polarization leakage and cross-polarization within a parametric component separation framework. 

We estimate the upper limits for each parameter to meet the scientific requirements for next-generation CMB measurement. Using Markov Chain Monte Carlo (MCMC) methods to optimize the $\chi^2$ log-likelihood function, we constrain the parameters and estimate the data volume needed to reduce statistical errors within the upper limits of the parameters. We analyze unpolarized atmospheric data with and without the use of a half-wave plate (HWP). 

Our findings indicate that polarized data is essential for fully characterizing and calibrating all parameters in the HWP model. We further explore the potential of using drone-based fully polarized data for parameter constraints.
-  Bachelor thesis: [[Bachelor_thesis_Binh.pdf|Instrumental systematic effects on CMB B-modes measurement]]
- Presentation: [CMB Polarization Instrumental Systematic effects Presentation](https://docs.google.com/presentation/d/1z_uaC2ccFqmAQg6wQufI4w79JdhqdG58MkLrqlmWHV8/edit?usp=sharing)
### *Supermassive Black Hole Feedback on Galaxy Formation in IllustrisTNG Simulations*
Supermassive black holes (SMBHs) with masses exceeding millions of solar masses are typically found at the centers of most galaxies in the local Universe (Kormendy & Ho 2013; Saglia et al. 2016). Acting as engines for feedback from Active Galactic Nuclei (AGN), accreting SMBHs release significant energy (~10²⁰ erg/s per gram), impacting galaxy formation and evolution. This SMBH feedback is integral to cosmological simulations of galaxy formation (Vogelsberger et al. 2019).

In this project, we will analyze SMBH feedback effects on galaxy evolution using IllustrisTNG simulations (TNG). TNG's cosmological magnetohydrodynamical framework has demonstrated the role of SMBH feedback in producing realistic galaxy properties, including stellar and gas components (Pillepich et al. 2019; Truong 2020; Ayromlou et al. 2023). Our analysis will focus on SMBH feedback’s influence on star formation rates, baryon mass fractions, gas halo temperatures, and SMBH-halo mass relationships.
- [[SMBH_feedback_report.pdf|Report smbh feedback on galaxy formation]]
- [[SMBH_presentation.pdf|Presentation smbh feedback on galaxy formation]]
### *Carina Keyhole*
A strong ionization source can dissociate and ionize molecular hydrogen, creating an HII region around it. Thus, it is unexpected for molecules with lower ionization and dissociation potentials to survive in the proximity of an ionization source. Interestingly, previous observations reported the existence of several clumpy regions with emission from carbon monoxide molecules (CO)  in the Keyhole region, next to one of the most luminous massive stars $\eta$ Carina belonging to the Trumpler 16 cluster in the Carina nebula. 

We revisit the keyhole region in the Carina nebula with velocity-resolved observations of rotational transitions of CO and its isotopologues and of hyperfine atomic structure lines from the far infrared and millimeter bands taken from APEX and SOFIA with the aim of studying the physical and chemical properties in the regions where molecular gas is located.
- [[Final_Report_GroupProjectB3_Carina.pdf|Report Carina Keyhole]]
- [[Presentation_carina_keyhole.pdf|Presentation Carina Keyhole]]
### *Other works*
-  [[GroupB-hardwarecamp.pdf|The second Hardware camp for Fast and Low-Light detection]]
## M1 General Physics notes
### Semester 1
#### Universe
###### Astrophysics
1. [[Fundamental Concepts]]
2. [[Interstellar medium]]
3. [[Jeans criteria]]
4. [[Stellar structure]]
5. [[M1 General Physics/Universe/Exercise/Tutorial 1|Star Tutorial]]
###### Cosmology
1. [[Introduction to Cosmology]]
2. [[Introduction to Cosmology 2]]
3. [[Friedmann Equations]]
4. [[Models of universe]]
5. [[Cosmological Horizon]]
6. [[content/M1 General Physics/Universe/Cosmo/Exercise|Exercise]]
#### Particles
1. [[Hyperbolic function]]
2. [[Simple harmonic oscillator]]
3. [[Special relativity]]
#### Nuclei
1. [[State of matter]]
2. [[Dimensionless study of many-body systems]]
3. [[Nuclear shell model]]
4. [[Midterm 2021-2022]]
5. [[Final exam notes]]
#### Plasma
1. [[Debye Length]]
2. [[Plasma Oscillation]]
3. [[Fluid model of plasma]]
4. [[Kinetic theory]]
5. [[Magnetic confinement]]
6. [[content/M1 General Physics/Universe/Exercise/Tutorial 1|Tutorial 1]]
#### Mathematical and Statistical Physics
1. [[Principle Component Analysis]]
#### Sensors, Measurement and Signal Processing
1. [[Measurement]]
2. [[Fourier Transform]]
#### Experimental Physics: 
1. [[Cosmology_Data_Analysis_M1_GP.pdf|Cosmology Data Analysis]]
### Semester 2
#### General Relativity And Cosmology
1. [[From Special Relativity to General Relativity]]
#### Group Theory
1. [[Advanced_Mathematics_for_Physics.pdf|Group Theory Full Notes]]
#### Astroparticles & Astrophysics
#### Quantum Field Theory

## M2 NPAC notes
1. Experimental Physics: CMB Temperature Measurement Using Atmospheric Zenith-Angle Dependence
2. Detector physics
3. Astroparticles and Cosmology







