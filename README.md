# BiQUIC

This work is done as a part of my ANU-FRT 2024 project with the He*-BEC group under the supervision of Prof. Andrew Truscott and Dr. Sean Hodgman.

Contains a simulation of the BiQUIC trap along with plotting the atom distribution and photon scattering rates for atoms in the modeled trap. Traps are simulated using the 'magpylib' python package. 

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

helix-BiQUIC-final:

This notebook uses helical coils to simulate the BiQUIC trap. It also considers an extra 2/3rd turn along with input wires in each coil. \
As of now, the model has been tested for quad current = 2.919A and bias current = 4.014A. \
The trap frequencies and bottom for this configuration as measured in the lab are - 25, 62(+/-5), 61(+/-5); trap bottom = 1.38G. \
The x-axis is along the -ve direction of propagation of the LVIS beam (same as the x-axis considered in the lab). \
The y and z axes for the lab and the simulation are interchanged. \
In this model, the z-axis is through the axis of the quad coils. The x-axis is parallel to the line joining the centers of the quad and bias coils. 

Improvements needed:

Measure the bias field more accurately. (not very feasible) \
Alternatively, add the nuller coils to the simulation. \
As of now, the trap frequencies along the y and z axes fit within the uncertainty. \
Test if the simulation works for other sets of quad and bias currents + external bias fields. 

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

atom distribution:

The magnetic field magnitudes by BiQUIC along the three axes, and other required information are imported directly from the helix-BiQUIC-final notebook using 'pickle' to save time by avoiding re-calculation of the fields. \
A maxwell-boltzmann distribution of 4He atoms is defined at 10 micro-Kelvin. \
The photon scattering rate for a Gaussian laser beam in wavelength range scanned close to the resonant frequency of the atoms in the trap is plotted. \
The total detuning accounts for doppler shift, laser detuning, and zeeman shift. \

Improvements needed:

How to sample atom positions from the earlier defined MB distribution for the photon scattering calculation using the Monte-Carlo method. \
How to select only the x component of the atom velocity. (Right now, the velocities are sampled randomly from a MB distribution) \
Can introduce intermediate plots for velocity distribution, sampled atom positions etc. as a cross-check. \
Increase the wavelength divisions and the number of samplings in the Monte-Carlo simulation. \

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

 
