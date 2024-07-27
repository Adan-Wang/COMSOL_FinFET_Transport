# Simulation Execution {#simulations}

There are two studies in embedded in this model, "DC Solution" and "SS Perturbation", corresponding to a general DC sweep and a DC small-signal perturbation around a bias point. This section will describe basic settings used in setting up these simulations. These settings are mostly common across both studies, but settings specific to a single study will be described where applicable.

The typical run time for a DC sweep is ~18 hours, the run time for a small-signal perturbation simulation can be up to 20+ hours. Simulations of a full Ids-Vds family of curves could take up to one week. These simulations cannot be paused, hence, an always-on computer is recommended. One component that contributes heavily to the long run time is the custom modified local density approximation formulation – if the simulator is re-formed using the newer density gradient approximation available in COMSOL 5.5 or above, it may be possible to have a much faster simulation.

## Sweeps {#section_krd_jgq_2cc .section}

Each solver utilizes sweeps that gradually increases voltage and other parameters from the equilibrium, with each step using the previous step as an initial guess. This scheme allows for the simulations to properly converge.

The DC study utilizes two sweep. The first sweep is used to achieve a desired drain voltage, and the second sweep obtains data at all gate desired gate voltages for the single desired drain voltage. This scheme is used as usually the Ids-Vgs curves are desired.

The small signal perturbation study simply runs five sequential points around a central bias point, each with a perturbed drain or gate voltage of dV.

Common to both studies, there is a final sweep of the parameter CT\_P, this gradually ramps up the effect of the Caughey-Thomas mobility model, which is necessary for the convergence of the simulation, as this model causes the governing equations to become extremely non-linear.

**Warning:** Small ramp steps of the CT\_P parameter near 1 is needed to ensure solution accuracy. The current ramp is set to 0.1, 0.5, 0.8, and 1 and it is not recommended to use ramps that are coarser than what is currently set. One symptom of faulty data from too large of a ramp step are spikes in the output conductance as a function of gate voltage.

## Solver Setup {#section_gfr_lhq_2cc .section}

A direct-segregated approach was taken to minimize RAM usage and allow for more simulations to be executed in parallel. A scaling factor of 1e-10 was used to aid the convergence, and can be found under "Dependent Variable" settings. Beyond these default scaling, the scaling for the quantum correction variable is set to 1, which can be found under the **** tab that is a sub-component to "Dependent Variables" for each solver.

The CT\_P parameter ramp is implemented under "Previous Solution", which is nested under "Parametric 1" for each solver.

**Warning:** Ensure this value is present in all simulations that needs to ramp up the Caughey-Thomas mobility. The simulation would not converge despite seemingly-correct setup in COMSOL 5.4 if this was not set.

The segregated solver first solves for charge and electrical driving force for the Caughey-Thomas mobility, followed by the quantum correction factor , and finally followed by overall electrical potential. The maximum number of iterations have been changed to 100 for each step to allow for convergence in some extreme cases.

**Parent topic:**[Model](model_0.md)

