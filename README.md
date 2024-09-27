# Stratification of Pediatric Patients with Myocarditis using Radiomic Signatures in Late Gadolinium Enhancement Cardiovascular MRI

This code accompanies the publication 

```
Laube A, Hüllebrand M, Ter-Minassian L, Uden T, et.al. Stratification of Pediatric Patients with Myocarditis using Radiomic Signatures in Late Gadolinium Enhancement Cardiovascular MRI. (Submitted). 2024.
```

#### Phantom Analysis
Radiomic features extracted using pyradiomics v3.0.1 are provided in the `phantom_data` directory. The associated phantom images and corresponding label masks (myocardium and AHA) are availabe via the [Zenodo repository](https://doi.org/10.5281/zenodo.13739772) [1].
We analyse the dependence of radiomic features on myocardial diameter and voxel size in `phantom_resampling.ipynb`. The feature selection procedures are found in `phantom_feature_selection.ipynb`. 

#### Patient Clustering
To stratify a patient dataset, Non-negative matrix factorization is applied to the set of selected radiomic features extracted from patient LGE CMR images.
NMF is carried out in R, see `nmf.ipynb`.

#### Requirements
We recommend installing the dependencies in `requirements.txt` in a virtual environment. The analysis for the paper was done using python v3.8.0, and R v4.4.0.

#### Image Segmentation
To obtain the segmentation mask for a new case, we provide a nnUNet segmentation model [2]. 

#### References
[1] Laube A, Hüllebrand M. LGE CMR SAX Phantom Images and Segmentation Masks. Zenodo; 2024. doi: [10.5281/zenodo.13739772](https://doi.org/10.5281/zenodo.13739772).

[2] Laube A, Hüllebrand M, Ter-Minassian L, Uden T, Seidel F, Hennemuth A. Pediatric LGE SAX CMR nnU-Net Segmentation Model. Zenodo; 2024. doi: [10.5281/zenodo.13744548](https://doi.org/10.5281/zenodo.13744548).

