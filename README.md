# ResFungi
Profile of Hidden Markov Models (HMM) specific for antifungal resistance genes (ResFungi.hmm).


This repository contains an HMM profile for fungal genes that contain known mutations that confer resistance to antifungal drugs.
This profile contains information for genes with mutations that confer resistance to:
Caspofungin, Micafungin, Fluconazole, Itraconazole, Voriconazole.


As more antifungal genes are described, this database will be updated.


# How to use
If you want to narrow down genes that might contain mutations related to antifungal resistance, you can perform your analyses using ResFungi. 
Here's a step-by-step explanation to perform analyses using ResFungi:

  
## 0 - Downloading the proteome file


Before you start your analysis, make sure the target species you want to study has a sequenced genome with a proteome file available. The ResFungi search is performed on the fasta file that contains all of the protein amino acid sequences.

  
## 1 - Installing HMMER


To use the ResFungi HMM profile, you need to install HMMER (http://hmmer.org/documentation.html). Their documentation shows how to perform the installation in all Operational Systems (Windows, Linux, OS/X and Anaconda).

  
## 2 - Preparing ResFungi to be used


Once HMMER is installed, run _hmmpress_ to generate the compressed files required by HMMER in the next step.
Here's an example of the command:


> hmmpress ResFungi.hmm


After running this command, HMMER will generate other files, meaning your ResFungi.hmm file was successfully compressed.

  
## 3 - Searching for candidate antifungal resistance genes


After compressing the .hmm file, run the software hmmscan to identify genes in the proteome of the species you want to analyze. Here's an example command


> hmmscan  --noali --domtblout ResFungi.hmm your_proteome_file.fasta


For further explanation of usage and outputs from hmmscan, please check their user's guide (http://eddylab.org/software/hmmer/Userguide.pdf).

  
## 4 - Understanding the results


The _hmmscan_ output shows you the protein sequences from your fasta file with hits to domains possibly belonging to genes that have known mutations related to antifungal resistance. Once you find those genes, you can test them in the wet lab. 


That is, you can sequence those specific genes in resistant strains you cultivate in your lab to check if those genes, in fact, exhibit mutations with the potential to confer resistance to the drugs you're testing.


# If you use ResFungi, please cite us!
Santana de Carvalho, D., Bastos, R. W., Rossato, L., Teixeira de Aguiar Peres, N., & Assis Santos, D. (2024). ResFungi: A Novel Protein Database of Antifungal Drug Resistance Genes Using a Hidden Markov Model Profile. ACS omega, 9(28), 30559-30570.


https://pubs.acs.org/doi/epdf/10.1021/acsomega.4c02198
