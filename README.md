# Hi fellow starter (clueless people according to Dawn)!
Rosetta is now downloaded and compiled on the Mac in L502, which also has a PYMOL installed. To access Rosetta, get into the terminal (aka. the black square next to the trash can), then type
```
cd Dowloads/rosetta_bin_mac_2019.35.60890_bundle/
```
## clean pdb (November 7th, 2019)
1. download the pdb file from https://www.rcsb.org/structure/2RH1, and duplicate it called 2rh1_ISOLATED.pdb
2. open the 2rh1_ISOLATED.pdb with a text editor and remove the lines between 230 to 263 (like A1002 to A1161) manually in 2rh1_ISOLATED.pdb
```
ATOM   1603  CG  LEU A 230     -23.526  46.346  19.805  1.00 63.55           C  
ATOM   1604  CD1 LEU A 230     -23.659  45.401  21.017  1.00 56.14           C  
ATOM   1605  CD2 LEU A 230     -24.867  46.998  19.398  1.00 63.01           C  
ATOM   1606  N   ASN A1002     -21.745  50.645  19.298  1.00 65.96           N  
ATOM   1607  CA  ASN A1002     -20.959  51.846  19.632  1.00 68.64           C  
.
.
.
ATOM   2879  CZ  TYR A1161     -27.470  51.366  25.980  1.00 73.12           C  
ATOM   2880  OH  TYR A1161     -27.695  52.436  26.850  1.00 77.23           O  
ATOM   2881  N   LYS A 263     -27.193  44.468  23.289  1.00 68.62           N  
ATOM   2882  CA  LYS A 263     -27.211  43.302  22.437  1.00 68.39           C  
ATOM   2883  C   LYS A 263     -28.617  42.992  22.039  1.00 68.68           C  
```
3. if the pdb file and your Rosetta bundle are both in the Downloads directory, get into Downloads on terminal with
```
cd Downloads
```
then run the clean_pdb.py program with
```
cd ./rosetta_bin_mac_2019.35.60890_bundle/tools/protein_tools/scripts/clean_pdb.py 2rh1_ISOLATED.pdb A
```
note that the name [rosetta_bin_mac_2019.35.60890_bundle] differs from version to version, and you should type in the name of the rosetta you downloaded. Here's the command-line output
```
Found existing PDB file at 2rh1_ISOLATED.pdb
2rh1_ISOLATED A   282 --- --- MOD --- OK
>2rh1_ISOLATED_A
DEVWVVGMGIVMSLIVLAIVFGNVLVITAIAKFERLQTVTNYFITSLACADLVMGLAVVPFGAAHILMKMWTFGNFWCEFWTSIDVLCVTASIETLCVIAVDRYFAITSPFKYQSLLTKNKARVIILMVWIVSGLTSFLPIQMHWYRATHQEAINCYAEETCCDFFTNQAYAIASSIVSFYVPLVIMVFVYSRVFQEAKRQLKFCLKEHKALKTLGIIMGTFTLCWLPFFIVNIVHVIQDNLIRKEVYILLNWIGYVNSGFNPLIYCRSPDFRIAFQELLCL
```
