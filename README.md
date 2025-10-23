# Computational Practice: Model 3D protein structure from a primary peptide sequence using SWISS-MODEL

##  Lab Overview
Accurate prediction of protein tertiary structure from primary amino acid sequence would have massive impacts in our ability to describe and engineer biological systems.  There are three main approaches to tertiary structure prediction:

## Method 1: Homology Modeling
Builds structural prediction based on known structure template with significant sequence similarity.

The described process outlines the main steps involved in homology modeling, a computational technique used to predict the three-dimensional (3D) structure of a protein based on an experimentally determined structure of a related homologous protein (the template). [1, 2, 3, 4, 5] . The steps of homology modeling include:

## Step 1: Template Recognition and Initial Alignment
This initial stage involves finding one or more suitable homologous proteins with known structures from databases like the Protein Data Bank (PDB). An initial alignment between the target protein's amino acid sequence and the template's sequence is then generated using bioinformatics tools like BLAST. The goal is to identify a template that is structurally similar to the target protein. [1, 2, 6, 7, 8]  
## Step 2: Correction of Initial Alignment
The initial sequence alignment often requires manual correction or refinement, especially for remote homologs with low sequence identity. This step ensures that important functional or conserved residues are correctly aligned, as alignment errors can introduce significant inaccuracies into the final model. Multiple sequence alignment programs like CLUSTALW can also be used to aid in this process. [1, 9, 10, 11, 12]  
## Step 3: Generation of the Backbone
In this step, the core backbone of the protein model is constructed based on the structure of the aligned template. The coordinates for the backbone atoms (the peptide chain) are transferred directly from the template structure, effectively building a rough skeleton of the target protein. [13, 14, 15, 16, 17]  
## Step 4: Modeling of Inserted Loops
Proteins often have insertions or deletions relative to their templates, particularly in loop regions. These loops cannot be modeled directly from the template and must be built de novo or with specific loop-modeling algorithms. These computational methods generate and evaluate possible loop conformations to find the most sterically and energetically favorable one. [1, 18, 19, 20, 21]  
## Step 5: Modeling of the Sidechains
After the protein backbone is in place, the amino acid sidechains are added. The placement of sidechains is often done using rotamer libraries, which contain a set of common, low-energy sidechain conformations. The algorithm must consider both the backbone conformation and potential clashes with neighboring atoms when placing the sidechains. [1, 22, 23, 24, 25]  
## Step 6: Optimization of the Model by an Energy Minimization Experiment
The final, full-atom model may contain minor steric clashes or unfavorable bond geometries. Energy minimization is used to resolve these issues by making small adjustments to atomic positions to improve the overall stereochemistry and reduce the potential energy of the model. [1, 26, 27, 28, 29]  
## Step 7: Model Validation
After generating and optimizing the model, its quality must be assessed. This can be done by hand or with specific servers and programs that evaluate structural properties. Common validation methods include: 

- Ramachandran plots: Analyzing the distribution of backbone dihedral angles to check for energetically unfavorable conformations. 
- Checking stereochemistry: Ensuring proper bond lengths and angles. 
- Comparing against the template: Assessing the root-mean-square deviation (RMSD) between the model and template. 
- Checking packing and clashes: Making sure the model's atoms are well-packed and do not have unfavorable steric contacts. [1, 30, 31, 32, 33]  

## Step 8: Iteration to Correct Mistakes
Model validation often reveals flaws that require correction. This can involve repeating earlier steps, such as refining the alignment, re-building loops, or performing further optimization, until a structurally and energetically sound model is achieved. [1, 34, 35]  

## Method 2: Threading (Fold Recognition)
Builds structural prediction based on known structure template with or without any sequence similarity.

## Method 3: Ab initio (Free modeling)
Based on molecular simulation and predicts structures based on physicochemical principles without a structural template.

In this lab, you will predict tertiary structure of the SARs-CoV-2 spike protein using the SWISS-MODEL service.

##  Lab Objectives:
- Model a primary protein sequence at Swiss-Model

## Lab instructions:

###  Task A: 
Model a primary protein sequence using Swiss-Model.
#### Step A. 
Find the SARS-Cov-2 Spike protein by searching the NCBI protein database with this PDB identifier: ‘7C01_B’.  Grab the FASTA sequence and save on the Linux desktop in a text file.  Call it something like ‘7C01_B.fasta’.
#### Step B. 
Go to SWISS-MODEL at  https://swissmodel.expasy.org/ . Paste you’re your sequence and start a model build.  Once complete, examine your model. Does it make sense?  

## References
[1] https://www.sciencedirect.com/topics/biochemistry-genetics-and-molecular-biology/class-architecture-topology-homology
[2] https://sgt.cnag.cat/services/BBibTeX/pdfs/20071110_Eswar_etal_CPPS2007.pdf
[3] https://pubmed.ncbi.nlm.nih.gov/33659566/
[4] https://pmc.ncbi.nlm.nih.gov/articles/PMC4301084/
[5] https://www.creative-biostructure.com/protein-structure-prediction-evolution-homology-modeling-to-alphafold.htm
[6] https://pmc.ncbi.nlm.nih.gov/articles/PMC5943704/
[7] https://www.researchgate.net/figure/The-eight-steps-of-homology-modelling-The-first-step-involves-finding-a-suitable_fig2_26778257
[8] https://pmc.ncbi.nlm.nih.gov/articles/PMC10700664/
[9] https://www.scribd.com/document/890276731/Template-recognition-and-initial-alignment
[10] https://pmc.ncbi.nlm.nih.gov/articles/PMC1175081/
[11] https://www.researchgate.net/figure/The-eight-steps-of-homology-modelling-The-Wrst-step-involves-Wnding-a-suitable_fig8_26778257
[12] https://pmc.ncbi.nlm.nih.gov/articles/PMC8244228/
[13] https://www.researchgate.net/publication/26778257_Homology_modelling_and_spectroscopy_a_never-ending_love_story
[14] https://www.researchgate.net/figure/The-eight-steps-of-homology-modelling-The-Wrst-step-involves-Wnding-a-suitable_fig8_26778257
[15] https://www.sciencedirect.com/topics/biochemistry-genetics-and-molecular-biology/homology-modeling
[16] https://www.pnas.org/doi/10.1073/pnas.0606822104
[17] https://link.springer.com/chapter/10.1007/978-981-97-7123-3_8
[18] https://pmc.ncbi.nlm.nih.gov/articles/PMC4125323/
[19] https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2887047/
[20] https://www.sciencedirect.com/science/article/pii/S0958166999000373
[21] https://pmc.ncbi.nlm.nih.gov/articles/PMC7544562/
[22] https://www.ebi.ac.uk/training/online/courses/alphafold/inputs-and-outputs/a-high-level-overview/
[23] https://pmc.ncbi.nlm.nih.gov/articles/PMC2253276/
[24] https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-12-S14-S10
[25] https://academic.oup.com/bioinformatics/article/27/20/2836/202852
[26] https://www.sciencedirect.com/science/article/pii/S0094576520306263
[27] https://onlinelibrary.wiley.com/doi/pdfdirect/10.1002/prot.21759
[28] https://www.sciencedirect.com/science/article/pii/S1093326322000134
[29] https://www.drugdiscoverynews.com/structure-based-drug-design-15997
[30] https://www.bonvinlab.org/education/molmod_online/modelling/
[31] https://www.sciencedirect.com/science/article/pii/S0882401022000602
[32] https://www.tandfonline.com/doi/full/10.1080/07391102.2024.2425839
[33] https://www.sciencedirect.com/science/article/pii/B9780128161098000155
[34] https://www.intechopen.com/chapters/74588
[35] https://www.researchgate.net/figure/The-eight-steps-of-homology-modelling-The-first-step-involves-finding-a-suitable_fig25_238609063
