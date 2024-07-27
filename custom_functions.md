# Custom Functions {#custom_functions}

Various custom functions have been implemented to assist the overall implementation of the quantum confinement correction formalism. These functions are defined both globally \(under Global Definitions\) and within the simulator \(under "Variables\_domain" in the simulation component comp1\).

The final function executed in the calculation for the quantum corrected charge ratio is [int196](int196_0.md) and[int 914](int914_0.md). It is suggested that the users start from there in order to understand the full implementation.

-   **[J0](j0_0.md)**  
Implements the sinc\(x\) function with a lower bound
-   **[E\_prime](e_prime_0.md)**  
Calculates as described in the MLDA formalism
-   **[K\_func](k_func_0.md)**  
Implements K as described in the MLDA formalism
-   **[J0Func](j0func_0.md)**  
Implements the integrand of the MLDA formalism with a lower bound.
-   **[fermi](fermi_0.md)**  
Implements the Fermi-Dirac Distribution
-   **[Int\_Di](int_di_0.md)**  
Implements the density of states multiplied by Fermi-Dirac distribution
-   **[lim](lim_0.md)**  
Contained within "Variables\_domain" of the component, limit of integration for charge density integration
-   **[int196](int196_0.md)**  
Contained within "Variables\_domain" of the component, implements the whole MLDA integral with a confinement effective mass of
-   **[int914](int914_0.md)**  
Contained within "Variables\_domain" of the component, implements the whole MLDA integral with a confinement effective mass of

**Parent topic:**[Quantum Confinement Correction](quantum_confinement.md)

**Related information**  


[Implementation of Quantum Confinement](implementation_of_quantum_confinement.md)

[J0](j0_0.md)

[E\_prime](e_prime_0.md)

[K\_func](k_func_0.md)

[J0Func](j0func_0.md)

[fermi](fermi_0.md)

[Int\_Di](int_di_0.md)

[lim](lim_0.md)

[int196](int196_0.md)

[int914](int914_0.md)

