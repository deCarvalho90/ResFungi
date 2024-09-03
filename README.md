# ResFungi
Profile of Hidden Markov Models (HMM) specific for antifungal resistance genes (ResFungi.hmm).\

This repository contains an HMM profile for fungal genes that contain known mutations that confer resistance to antifungal drugs.
This profile contains information for genes with mutations that confer resistance to:\
Caspofungin, Micafungin, Fluconazole, Itraconazole, Voriconazole.\

As more antifungal genes are described this database will be updated.

# Using ResFungi with metagenomic data
ResFungi is a HMM protein database, but it can still be used to search for antifungal resistance genes in metagenomes.
Before running your ResFungi analysis, you need to generate the gene/protein models from the metagenomic data (feel free to use the software of your preference to perform this step).
After that step, you should have a FASTA file with your predicted proteome, which can be used to run ResFungi.\

Below is the summarized pipeline we used to search for antifungal resistance genes (AFRs) after you have you proteome in FASTA file:\
1-Download and install HMMER3 (http://hmmer.org/)\
2-Download ResFungi HMM file (https://github.com/deCarvalho90/ResFungi)\
3-Convert the HMM file to a usable HMMER3 format using _hmmpress_ (a program part of HMMER3)\
4-Run _hmmscan_ (a program part of HMMER3) using both ResFungi and your predicted proteome file (in FASTA format)\


# If you use ResFungi, please cite us!
Santana de Carvalho, D., Bastos, R. W., Rossato, L., Teixeira de Aguiar Peres, N., & Assis Santos, D. (2024). ResFungi: A Novel Protein Database of Antifungal Drug Resistance Genes Using a Hidden Markov Model Profile. ACS omega, 9(28), 30559-30570.\
\
https://pubs.acs.org/doi/epdf/10.1021/acsomega.4c02198

