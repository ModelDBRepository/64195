NEURON mod-files for stochastic channel gating of Ih and Na channels
for the paper

M.H.P. Kole, S. Hallerman and G.J. Stuart (2006). Single Ih Channels
in Pyramidal Neuron Dendrites: Properties, Distribution, and Impact on
Action Potential Output. The Journal of Neuroscience 26:1677-1687.

Running fig6b.hoc will generate two 25s lasting voltage traces from
the soma and the distal dendrite of a Layer 5 Pyramidal neuron. At
least the first 500ms have to be discarded to allow the cell to reach
steady state.

Running fig7d.hoc will generate a somatic voltage trace with an EPSP
after 500ms that elicits an action potential. To terminate the
simulation during the initialization with larger dt (first 200ms in
fig6b.hoc and first 400ms in fig7d.hoc) you have to kill the kernel
process nrniv manually. Note that due to the stochastic nature of the
mod files, the traces will differ from the published ones.

The mod files ih_stochastic.mod and na_stochastic.mod (see subfolder
Stochastic_Na) are newly generated NMODL files that allow the
incorporation of stochastically gating channels into morphologically
realistic cells. The kinetics of Ih were based on patch clamp data
from Layer 5 pyramidal neurons at 34 degree Celsius (for deterministic
version see Ih.mod in subfolder Stochastic_Na).

All other mod files were adopted unchanged from Mainen and Sejnowski
(1996). Ka.mod and CaT.mod were from Schaefer et al. (2003) and
syn.mod from Geiger et al. (1997). Only the na.mod was changed to
correct for an error in the trap0() function.

6/8/2007 version updated: includes short run demo option for ModelDB
