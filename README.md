# Computational Practice: Model 3D protein structure from a primary peptide sequence using SWISS-MODEL

##  Lab Overview
Accurate prediction of protein tertiary structure from primary amino acid sequence would have massive impacts in our ability to describe and engineer biological systems.  There are three main approaches to tertiary structure prediction:

* Homology Modeling
Builds structural prediction based on known structure template with significant sequence similarity.

As described at http://www3.cmbi.umcn.nl/hvensela/START/index.html, the main steps for homology modelling are Step 1: Recognition of the correct template and initial alignment. Step 2: Correction of this initial alignment. Step 3: Generation of the backbone. Step 4: Modeling of inserted loops. Step 5: Modeling of the sidechains. Step 6: Optimization of the model by an energy minimization experiment. Step 7: Model validation (by hand or using different servers). Step 8: Iteration to correct mistakes (if any). 

* Threading (Fold Recognition)
Builds structural prediction based on known structure template with or without any sequence similarity.

* Ab initio (Free modeling)
Based on molecular simulation and predicts structures based on physicochemical principles without a structural template.

In this lab, you will predict tertiary structure of the SARs-CoV-2 spike protein using the SWISS-MODEL service.

##  Lab Objectives:
* Model a primary protein sequence at Swiss-Model

Follow these lab instructions:

###  Task A: 
Model a primary protein sequence using Swiss-Model.
#### Step A. 
Find the SARS-Cov-2 Spike protein by searching the NCBI proteindatabasewith this PDB identifier: ‘7C01_B’.  Grab the FASTA sequence and save on the Linux desktop in a text file.  Call it something like ‘7C01_B.fasta’.
#### Step B. 
Go to SWISS-MODEL at  https://swissmodel.expasy.org/ . Paste you’re your sequence and start a model build.  Once complete, examine your model and paste the ‘Model Results’ into a LibreOffice writer file with your first and last name in the filename.  
