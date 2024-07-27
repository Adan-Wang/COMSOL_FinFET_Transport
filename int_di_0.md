# Int\_Di {#int_di_0}

Implements the density of states multiplied by Fermi-Dirac distribution

**Syntax**

Int\_Di\(*gi*,*mi\_x*,*mi\_y*,*mi\_z*,*mi\_q*,*tb*,*E*,*nu*,*Vth*\)

**Variables**

|Parameter|Description|
|---------|-----------|
|gi|Valley degeneration parameter \(2 is used to account for both spins\)|
|mi\_x|x-direction effective mass|
|mi\_y|y-direction effective mass|
|mi\_z|z-direction effective mass|
|mi\_q|Confinement effective mass for the ith direction|
|tb|FinFET fin width|
|E|Energy to be integrated over|
|nu|Distance between fermi level and conduction band edge|
|Vth|Thermal voltage kBT \(~25 meV at room temperature\)|

**Parent topic:**[Custom Functions](custom_functions.md)

**Related information**  


[Custom Functions](custom_functions.md)

[Implementation of Quantum Confinement](implementation_of_quantum_confinement.md)

