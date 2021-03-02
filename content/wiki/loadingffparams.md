Command cheatsheet for tleap/xleap

Loading files:

leaprc file: source leaprc.forcefield
lib file: loadoff res.lib
prepi file: loadamberprep res.prepi
frcmod file: loadamberparams res.frcmod
mol2: loadmol2 RES res.mol2

Saving files:

savepdb UNIT unit.pdb (note that this saves the pdb in Amber's format and renumbers residues. Can be useful for cleaning/testing complex systems.)
savamberparams UNIT unit.prmtop unit.rst7
savemol2 UNIT unit.mol2

Creating structure name:

UNITNAME = unitstructure
UNITNAME = loadpdb unitstructure.pdb 
UNITNAME = loadmol2 unitstructure.mol2

Helpful commands

Check UNIT - checks unit for charge, clashes, and missing parameters
list - lists all currently loaded parameters by RES 3 letter code

Building structures:

bond UNIT.res#.atom UNIT.res#.atom 
deletebond UNIT.res#.atom UNIT.res#.atom

xleap:

It's good to check structures in xleap, because it shows the actual bonds it thinks your structure has. Most GUIs bond based on distance between atoms, not on forcefield parameters. If you have a nonstandard residue and your simulation will not proceed, incorrect bonding is often the cause. It can display anything in the list. 

edit UNIT - Displays structure in GUI. 
select UNIT.res# - Selects residue in GUI.
deselect UNIT.res# - Deselects residue in GUI. 