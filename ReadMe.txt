Zürich, 30. July 2026, Salome Bachmann

**************** Master-Thesis GitHub Repo ****************

This document explains the structure and purpose of the GitHub repository Master-Thesis and the files contained. All code, text and figures were produced by me, unless stated otherwise and were used for the IDEA-League Joint Master's in Applied Geophysics Master Thesis. If there are any questions, please email me sbachmann@student.ethz.ch .


**************** Miscellaneous Files ****************

** environment.yml **: Environment required to run SALVUS

** master thesis.bib & master_thesis.bib **: Bibliography files used for writing the final thesis document. Two versions in order to avoid errors because of the name in certain Latex compilers. 


**************** Meeting Slides ****************

Contains Latex-slides used for intermediate meetings with supervisors as well as presentation given to peers and final defense presentation. 


**************** Report ****************

Contains literature review study done at beginning of thesis.

** thesis-idea **: Contains all sections, style files and final pdf of thesis.



**************** Test Simulations ****************

Contains all code written for thesis. All files marked with --** contain code / results which are contained in the final thesis document. All other codes were written as tests, preliminary studies or are irrelevant

** comparison_plots.ipynb **: (OUTDATED) Contains plotting code used to compare different simulation cases with each other in terms of receiver depth, propagation speed, velocity, displacement and also traces at different receiver locations. 

** custom_stf.ipynb **: Contains code to set up two-layer (snow-air) model in SALVUS with a ticker-wavelet source time function that can be weighted. Manual propagation speed input as target_vprop, manual source spacing, depth and rupture length. 

** functions.ipynb **: (INCOMPLETE) Contains functions for the commands and workflows used in other notebooks in an attempt to simplify and streamline the workflow of setup, plotting etc. 

** moving_source.ipynb & moving_source_copy.ipynb **:  Setup of moving sources via individual time delay of each source 

** moving_source_simpler **: Simpler source setup ?

** mpm_custom_stf_simulation.ipynb **: contains loading code of the moment tensors obtained from the mpm simulation. The sources are injected in a two-layer model.

** multiple_src_like_tutorial.ipynb **: Source setup like in MONDAIC tutorial, using for-loop for source assignment and injecting stfs to event configuration

--** new_comparison_plots.ipynb **--: Used for results in the thesis. Contains plotting and extraction code. Extracts velocity and displacement data, calculates velocity by deriving displacement and calculates strain, simulates DAS data using pyber gauge length class. All plots set up for 2 layer model, 2 plotting depths (snow bottom and crack depth). 

--** rupture_test copy & rupture_test **--: Cohesive zone model with capability for mixed-mode crack propagation using mode_mix parameter. Modified to take custom stf, also contains plotting code

** simple_test.ipynb **: Code written to test simpler source setup (calculating time delay of sources from rupture speed, injecting into simulation)

** topo_test.csv ** : Topography data used in topography notebook, this is taken from map.geo.admin.ch

** topography_test.ipynb ** : Reads topography data from .csv, creates layers of equal thickness following topography and sets up point-sources in snow layer 

** wavefield_layered_multi.ipynb **: contains code for three layer model: old snow, fresh snow, air with simple point source setup

** wavefield_test.ipynb **: simple 2 layer model with one point source

** wavefield_test_momentt.ipynb **: simple 2 layer model with one point source, uses SALVUS moment tensor STF 

** wavefield_test_momentt_larger.ipynb **: same setup for 2 layered model with moment tensor stf, but larger domain extent

--** weighted_custom_stf.ipynb **--: Two layer model setup with custom stf input according to user-defined equation (ricker here). Source spacing can be defined manually as well as source extent, time delay between sources calculated from rupture speed (can also be defined). Uses zero-padding of stfs so all stfs have same length. Also uses taper of first and last wavelet so there is no injection noise. Plotting code contained as well, also contains code to animate velocity wave fields (output over time). STFS can also be weigthed using per-component weighting arrays (one for mxx etc)

** weigthed_custom_stf copy **: Same setup as above, but loads data from moment tensor .npz instead of user-defined equation. 

** weighted_custom_stf copy-2 **: Same, but with tail and head taper (spatial)

** weighted_custom_stf_original_domain.ipynb **: Loads moment tensor data, sets up 4 layer model (bed, snow, weak layer, air. Spatial taper of STF components, also plotting code

--** weighted_custom_stf_original_domain copy.ipynb **--: Loads moment tensor data, sets up 5 layer model (bed, snow, wl, snow, air). Temporal taper of stfs, as well as plotting, incl gauge length DAS simulation plotting

--** weighted_custom_stf_original_domain copy-2.ipynb **--: Same as model as above (5 layer model), but with simple STF (ricker wavelet)



**************** Wave propagation GIFS ****************

Contains animations of the wavfield, which are also contained in thesis appendix. 

** custom_sub_wavefiled_2d_moving_vx_crack.gif **: Animation of the two-layer case sub-rayleigh horizontal velocity wavefield.


** custom_sub_wavefiled_2d_moving_vy_crack.gif **: Animation of the two-layer case sub-rayleigh vertical velocity wavefield.

** mpm_wavefield_2d_moving_vx.gif **: Animation of MPM-5-layer horizontal velocity wavefield. 

** mpm_wavefield_2d_moving_vy.gif **: Animation of MPM-5-layer vertcial velocity wavefield. 


**************** thesis_salome_bachmann_from_particles_to_waves ****************

Contains final version of thesis, compiled in overleaf 
 