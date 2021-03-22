# ResidualBind package overview

The ResidualBind is a python package that uses TensorFlow for DNN training and model interpretability with global importance analysis. This repository contains scripts to reproduce results from "Global Importance Analysis: A Method to Quantify Importance of Genomic Features in Deep Neural Networks" by Koo et al.


#### Dependencies
- Python 3.5 or greater
- Pandas, NumPy, SciPy, Matplotlib, H5py
- TensorFlow 1.15 or greater
- Logomaker (Tareen and Kinney)

#### Source files
- residualbind.py - class for ResidualBind and GlobalImportance 
- helper.py - functions to file handling
- explain.py - functions for in silico mutagenesis and k-mer alignments for motif visualization
- E_RNAplfold, H_RNAplfold, I_RNAplfold, M_RNAplfold - RNAplfold scripts to calculate probability of external loop, hairpin loop, internal loop, and multi-loop, respectively

#### Example files
- generate_rnacompete_2013_dataset.py - script to process the RNAcompete dataset
- train_rnacompete_2013.py - train a ResidualBind model on all RNAcompete experiments
- test_rnacompete_2013.py - test each ResidualBind model on all RNAcompete experiments
- global_importance_analysis.py - run GIA experiments systematically across all RNAcompete
- Figure1_performance_analysis.ipynb - jupyter notebook that generates Figure 1 in (Koo et al.)
- Figure2_RBFOX1_analysis.ipynb - jupyter notebook that generates Figure 2 in (Koo et al.)
- Figure3_VTS1_analysis.ipynb - jupyter notebook that generates Figure 3 in (Koo et al.)
- Figure4_GC-bias_analysis.ipynb - jupyter notebook that generates Figure 4 in (Koo et al.)

#### Data
- Raw data can be downloaded from: Ray et al. Nature, 20013.
- Data from this study was downloaded from: http://tools.genes.toronto.edu/deepbind/nbtcode/nbt3300-supplementary-software.zip
- Final processed data (i.e. rnacompete2013.h5 <-- from running generate_rnacompete_2013_dataset.py) can be downloaded from:  Koo, Peter (2021), “Processed RNAcompete data”, Mendeley Data, V1, doi: 10.17632/m2yzh6ktzb.1
