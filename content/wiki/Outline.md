How to prepare a protein!

https://nicolas-van.github.io/easy-markdown-to-github-pages/
http://markdownpad.com/faq.html#livepreview-directx
https://guides.github.com/features/mastering-markdown/
https://www.gatsbyjs.com/tutorial/part-zero/

1. Obtain structure (crystal --> resolution, other metrics like Bfactors, cryo-em, NMR https://www.creative-biostructure.com/comparison-of-crystallography-nmr-and-em_6.htm) --> bin of structures, PDB vs new PDB formatting). Make sure to save this initial structure as-is for reference, and to make a fresh copy for editing.
2. Check for nonstandard residues (list of common amino acids, list of common DNA bases, list of common crystallization compounds, list of common cofactors, header of PDB breakdown, CONECT nonsense)
3. Check for alternative configurations (ANISOU, rotamers, A/B/C chains, cocrystal repeats)
4. Check for missing residues (Tails vs. inner, debate of what's important, standard linkers, Modeller/Chimera, homology modeling, missing cofactors)
5. Check for "important" crystal waters (active site, ions, surface vs. inner, HOH vs WAT)
6. Protonate (H++/propKA, MolProbity, constant pH)
7. Check for intentionally deprotonated residues, e.g. His, Cys, Asp, Glu (HID, HIE, HIP, CYX, ASX, GLX) esp in active sites, check literature and read crystal paper
8. Check for force field parameters for nonstandard residues (lipid14, glycam, Manchester DB, /dat/leap/parm, GAFF for small organics, previously published work in this group, literature)
	1. Chromophores can have unusual structural features that require tuning (e.g. GFP chromophore paper, etc)
	2. All "new" forcefield params require regeneration of charges at a min (RESP fitting, RED development server, TeraChem RESP parameters)
	3. Not all force fields are transferrable, must check formulation of FF beforehand (ex: can't take CHARMM directly to AMBER)
	4. Can "hack" together existing parameters, e.g. glycolipid = GLYCAM + lipid14. (parmchk2, atom typing)
	5. Generating residues in a chain, e.g. modified AA/modified DNA/RNA 
	6. Alternative solvents might need extra parametrization
	7. sanity check for generating partial charges
8. Check for disulfide bonds
9. Check for metal ion orientation, especially planar tetrahedral (e.g. zinc)
10. Check for mislabeled residues (3 letter codes are NOT universal, TER codes are not properly applied much of the time)
11. Check for structural clashes and possible rotameric solutions (Chimera)
12. Addions (Cl-, Na+ vs K+, saltcon, VDW/water model dependence)
13. Add water (size, shape, water type/parameters, setbox vdw, solvent type)
14. Add other solvent (packmol, mixtures, XBOX, membranes)

Things you may need to do:
1. Mutate residues (Chimera, tleap)
2. Dock substrates/cofactors (AutoDock, FlexX)
3. Homology model (Modeller, Rosetta)
4. Overlay protein families (Chimera)
5. Check sequence alignments (BLAST/UniProt, TCOFFEE)
6. Covalent linkages (dimers/trimers, missing sequences, drugs)
7. Replace "HETATM" with "ATOM  " and add TER

General knowledge:

1. Force field basics
	1. AMBER vs CHARMM
2. Atom typing 
