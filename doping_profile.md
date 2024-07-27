# Doping Profile {#doping_profile}

Doping in the channel is specified using analytic doping models following a Gaussian profile from values in the source and drain to the background doping of the channel. Specific settings can be found in the modules named "Source Doping" and "Drain Doping" in the model.

**Warning:** The sharpness of the Gaussian is controlled by the junction depth parameter in the doping profile. Too sharp of a doping profile \(low junction depth\) could cause convergence issues.

|Region|Type|Doping Concentration|
|------|----|--------------------|
|Source|n+||
|Channel|p||
|Drain|n+||

**Parent topic:**[Transport and Electrostatics](transport_0.md)

