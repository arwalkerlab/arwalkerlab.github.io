List of previously developed parameters

***Just because these parameters exist doesn't mean they're what you need. Many of them also have different options. Evaluate them first.***

***You can build new parameters from existing ones, e.g. adding a Glycam sugar to a Lipid14 tail to make a glycolipid. These should also be carefully evaluated.***

Parameters that are native to Amber can be found in $AMBERHOME/dat/leap/parm and/or $AMBERHOME/dat/leap/lib. 

Parameters compatible with source leaprc.xxx are in:
$AMBERHOME/dat/leap/lib

These include:
Standard amino acids (leaprc.protein.ff14SB, leaprc.protein.ff14ipq)
Phosphorylated amino acids (source leaprc.phosaa10)
Standard nucleic acids (leaprc.RNA.OL3, leaprc.DNA.OL3)
Modified RNA (leaprc.modrna08, includes all 107 known mods)
Water models/associated ions (leaprc.water.tip3p, leaprc.water.spce)
8M urea model
Solvents (solvents.lib)
Lipids (leaprc.lipid17)
Sugars (leaprc.GLYCAM_06j-1 *note that this includes links to lipids)
Dyes (leaprc.amberdyes)
Fluorescent chromophores (leaprc.xFPchromophores)
Atomic ions (atomicions.lib,ions94.lib)
Constant pH residues (leaprc.constph)
Small organic molecules/general parameters (leaprc.gaff, leaprc.gaff2)

Other parameter databases/literature parameters:
Manchester
Chlorophyll

Our group has computed parameters for:
GFP chromophore
HPTS
FAD
Flavin
Fatty acids
Carotenoids
Glycolipids