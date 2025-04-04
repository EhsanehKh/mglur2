# mglur2
Analysis Scripts Used for mGluR2 Dynamics in Bilayer and Micelle Environments
RMSD Calculation (rmsd_all.tcl, rmsd_helix_individual.tcl)
These VMD scripts calculate the root mean square deviation (RMSD) of the receptor backbone (Cα atoms) across the trajectory.

rmsd_all.tcl aligns the protein to a reference structure (e.g., the inactive state when simulating active-to-inactive transition) and measures the total RMSD per frame to evaluate structural stability and convergence.

rmsd_helix_individual.tcl isolates individual transmembrane helices (TM1–TM7) in both protomer A and B, calculating per-helix RMSD values to assess local fluctuations and conformational shifts.

RMSF Calculation (rmsf_TM_loops.tcl)
This VMD script calculates root mean square fluctuation (RMSF) for all residues in the trajectory. Focus is given to transmembrane helices and loop regions to detect local flexibility and dynamic motion throughout the simulation.

Inter-Protomer Distance (protomer_com_distance.tcl)
This script measures the center-of-mass (COM) distance between protomer A and protomer B across the simulation.

The COM is calculated using VMD’s measure center command, and the output represents the magnitude of the vector between the two protomer centers.

This measurement helps quantify conformational separation between subunits in different CHS environments.

Inter-Protomer Angle (protomer_inertia_angle.tcl)
This VMD script calculates the angle between the principal axes of inertia of protomers A and B using Cα backbone atoms.

The second principal axis is used to capture the longest dimension of the protomers.

The angle is calculated as θ = arccos(v1·v2 / |v1||v2|) and symmetrized with 180° − θ for angles >90°, to ensure consistent interpretation.

This angle represents relative orientation changes between protomers over time.

Hydrogen Bond Analysis (hbond_analysis.tcl)
Hydrogen bonds were analyzed using the VMD HBond plugin with a 3.5 Å distance and 30° angle cutoff.

The script identifies hydrogen bonds between specific transmembrane segments or loops.

Formation and loss of key hydrogen bonds across conditions (bilayer vs. micelle, different CHS %) provide insight into local interactions and receptor stability.

Salt Bridge Analysis (saltbridge_analysis.tcl)
Salt bridges were detected using the VMD Timeline plugin with a 4.0 Å cutoff between donor and acceptor atoms.

The script tracks salt bridge formation and disruption across frames.

This analysis was used to identify CHS-dependent electrostatic interactions between transmembrane helices and loop regions, as well as inter-protomer contacts.
