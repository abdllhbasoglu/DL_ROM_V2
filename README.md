# DL_ROM_V2
It is DL_ROM application for extended dataset by adding Mach into the parameter domain

The main.py code includes overall routine for training model to predict flow field around NACA0012 Airfoil for varying angle of attacks and Mach Number. The rest flight conditions are fixed. 

The model_XX.py files include CNN_Autoencoder models.

In this case, we try to predict flow field around NACA0012 Airfoil as done in DL_ROM_V1 but this time Mach number also varies next to Angle of Attacks (AoA). Mach Number range includes from 0.5 to 3.0 which covers three flight regimes: Subsonic, Transonic and Supersonic.
A total of 500 samples are simulated by High-fidelity CFD solver (in-house code). Since transonic region has more complicated flight characteristics, we gave more weight while applying sampling approach Latin Hypercube Sampling. Namely, we have more data points on transonic region.
