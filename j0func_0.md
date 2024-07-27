# J0Func {#j0func_0}

Implements the integrand of the MLDA formalism with a lower bound.

**Syntax**

J0Func\(*E*,*z*, *mi\_q*,*tb*\)

**Note:** If the output of this function is smaller than 1e-10, it is rounded to 1e-10

**Variables**

|Parameter|Description|
|---------|-----------|
|E|Energy to be integrated over|
|z|Distance from a semiconductor-insulator interface at z=0|
|mi\_q|Confinement effective mass for the ith direction|
|tb|FinFET fin width|

**Parent topic:**[Custom Functions](custom_functions.md)

**Related information**  


[Custom Functions](custom_functions.md)

[Implementation of Quantum Confinement](implementation_of_quantum_confinement.md)

