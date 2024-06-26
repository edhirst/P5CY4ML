# P5CY4ML
This is the repository for arXiv: 2311.17146, containing:   
- Statistical analysis and machine learning applied to the dataset of Calabi-Yau four-folds as hypersurfaces in weighted projective spaces; including symbolic regression.   
- Statistical analysis and machine learning applied to the list of co-prime six-weight weight systems, partitioned according to reflexivity, IP, intradivisibility and Calabi-Yau property; including principal component analysis.   
- A new approximation/lower-bound formula for Calabi-Yau's Hodge numbers in weighted projective spaces.   
- Databases of transverse weight systems consisting of 7 and 8 weights respectively, for sum of weights $\leq$ 200. Data format: $[[w_1,w_2,...,w_n],\sum_i w_i, [h^{1,1},h^{1,2},...,h^{1,n-3},h^{2,2},...],\chi]$    

------------------------------------------------------------------------
The folder `Data` contains the analysed datasets in this work. Note the original file format for the Transverse weight systems of 6-weights `5dTransWH.all.gz` as a gzip is maintained (and the respective code scripts read this data directly from the gzip file, so no need to unzip). The other datasets are zipped text files, and should be unzipped after download (replacing the zip files in these folders). The datasets include transverse weight systems with sum of weights $\leq$ 200 consisting of 7 weights, and of 8 weights (split into 2 zip files at sum of weights $<$ 150). The `Partition` subfolder contains the subdatasets of weight systems with each possible combination of the properties: {IP, reflexivity, intradivisibility, transverse (i.e. Calabi-Yau)}; again split into 2 zip files.    

The `Example_notebook.ipynb` illustrates a general code functionality, allowing a user to compute exact and approximate Hodge numbers for an input weight system with any number of weights, as well as compute the exact Euler number, and check the intradivisibility property. The respective functions for this general functionality are provided in the `Definitions.py` file. We recommend users new to this repository start with this notebook.        

The files `Data_Analysis_Fourfolds.py`, `Machine_Learning_Fourfolds.py`, and `SR.py` respectively analyse the clustering behaviour, then regress the Hodge numbers of the transverse Calabi-Yau weight systems (of 6 weights), as provided in `5dTransWH.all.gz`, using either neural networks or symbolic regression. The `WeightClassification.py` file provides code to classify the subdatasets of weight systems available in the `Data/Partition` subfolder, whilst the `PCA.py` code computes the respective principal component analysis.    

------------------------------------------------------------------------
# BibTeX Citation
``` 
@article{Hirst:2023kdl,
    author = "Hirst, Edward and Gherardini, Tancredi Schettini",
    title = "{Calabi-Yau four-, five-, sixfolds as $\mathbb{P}_w^n$ hypersurfaces: Machine learning, approximation, and generation}",
    eprint = "2311.17146",
    archivePrefix = "arXiv",
    primaryClass = "hep-th",
    reportNumber = "QMUL-PH-23-25",
    doi = "10.1103/PhysRevD.109.106006",
    journal = "Phys. Rev. D",
    volume = "109",
    number = "10",
    pages = "106006",
    year = "2024"
}
```
