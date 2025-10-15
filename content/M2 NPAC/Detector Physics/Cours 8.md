
Signal formation $\rightarrow$ Data treatments

particles (p, n, $\gamma$, $\pi$, K) $\rightarrow$ DET (Active conversion) $\rightarrow$ Amplifier $\rightarrow$ Discriminator
- Conversion ($X \rightarrow e^-$)
- Collection ($e^- \rightarrow I$ )
- What you collect is not current but voltage $V(t)$
- Resistance and impedance ($R$ vs $Z$)?
	- Resistance is only use for resistor $R$
	- Impedance is the collection of resistor, inductor and capacitor $Z$
	- A pulse is non-constant current $\rightarrow$ $Z$
	- Impedance: low (50 $\ohm$) and high (1 $M\ohm$)
		- Scope: DC coupling and AC coupling (50 $\ohm$ and 1 $M\ohm$)
		- Coupling to another impedance, if the coupling impedance is much larger the current will only run inside the DET (which have its own impedance). Important to not have the attenuation. To filter out some parts (frequency)
		- RLC has some resonance frequency (f = 1/\tau, \tau = RC). Bandwidth -> define a f_cutoff that Iout/Iw is a constant at 95% level. 
	- Scintillator + PMT: 10 cm vacuum $\rightarrow$ high $Z$
		- In photocathode (In scintillator) 1 $e^-$ to 1 photon
		- $C \sim \mu F$ 
	- MWPC: gas (Ar + CO$_2$) $\rightarrow$ low $Z$. Why ?  
		- $e^-$ goes into MWPC, ionizing the gas, electrons drift 
		- $C \sim pF$ 
		- $n_T = \Delta E / W_i$
	- Gain $G = I_{out}/n_{prim}$ . number of primary e
	- 1 GeV muon is a MIP, so nT ~ 10^2 10^3 . Wi ~ eV. G ~ 10^5 - 10^7 
	- rise time: ns. decay time: 10^2 ns. Why the time is different ? 
		- To descriminate the particles
	- Bipolar and unipolar and crossover
	- What are the electromagnetic perturbations -> Induction from AC 
