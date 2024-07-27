# Numerical Considerations {#numericalconsiderations}

Several important points must be kept in mind in order for the model to converge with the current formulation.

## Carriers {#section_f4r_cjq_2cc .section}

Currently, the model is set to run with electron and hole solutions. The simulation **will** not converge if set to single carrier only, even if the minority carrier does not contribute to transport.

## Quantum-Corrected Densities {#section_it1_4jq_2cc .section}

As discussed in [quantum confinement correction](implementation_of_quantum_confinement.md), the quantum corrected carrier densities should be truncated at low values to avoid non-convergence issues.

## Doping {#section_blf_yjq_2cc .section}

As discussed in [doping profile](doping_profile.md), a sharp transition of dopant concentration would lead to non-convergence.

## Caughey-Thomas Mobility {#section_n4h_bkq_2cc .section}

The implementation of Caughey-Thomas mobility is a major contribution factor to non-convergence as its formulation highly impacts the linearity of the drift diffusion equations. If the non-linearity of this effect is incorrectly ramped up, non-convergence could occur.

**Parent topic:**[Model](model_0.md)

