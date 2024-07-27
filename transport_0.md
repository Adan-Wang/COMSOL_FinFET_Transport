# Transport and Electrostatics {#transport_0}

The transport simulation is split up into domain that handles both transport and electrostatics \(the source, channel, and drain regions\), and domains that handles only electrostatics \(spacer and oxide regions\).

Internal boundary conditions uses the insulator interface boundary condition between the semiconductor \(source, drain, and channel\) and the spacer and oxide, and the continuity boundary condition at the interface that lies between the channel and the source and drain. All contacts have been realized using the metal contact boundary conditions, with the outside of the air domain handled using homogeneous Neumann boundary conditions, which is the default boundary for COMSOL.

Fermi-Dirac statistics along with finite-element quasi-formulation discretization method was used for the transport module.

-   **[Doping Profile](doping_profile.md)**  

-   **[Mobility](mobility.md)**  


**Parent topic:**[Simulation Setup](simulation_setup.md)

