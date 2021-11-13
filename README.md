# Build a machine learning model to identify *Candida albicans* essential genes

## About The Project

This repository maintains the Python program of a pipeline for training, optimizing, and testing a random forest-based machine learning model in order to identify the essentiality of 6,638 *Candida albicans* genes. It manages the supplementary datasets and serves as a supplement to Xiang Zhang's Computer Science PhD Preliminary Exam at University of Minnesota.

Updates on 11/11/2021: this computational analysis contributed to a larger project that was published on *Nature Communications*. (Fu, C., Zhang, X., Veri, A.O. *et al.* Leveraging machine learning essentiality predictions and chemogenomic interactions to identify antifungal targets. *Nat Commun* **12,** 6497 (2021). https://doi.org/10.1038/s41467-021-26850-3)

## Getting Started

To run this program, please make sure your environment meets the prerequisites and has the input data "*Calbicans_13Features_6638genes_beforeImputation_210302.tsv*" in the same directory as the code. The output files (i.e. the predictions and figures) will all be located in the same directory as well.

You can utilize the functions provided in this program to generate figures such as PR/ROC curves and distribution plots based on the supplementary data. We provide the optimal random forest classifier trained from 5-fold cross-validation (*rf_clf_optimal.joblib*) so that you can load it directly, fit it with the whole GRACE gene set, and make predictions on all genes. Note that every time you fit this model, it is a new training process and the results may vary slightly in terms of prediction results. One version of reasonable output is reported in the manuscript.

### Prerequisites & Installation

1. Packages essential to the random forest pipeline and the versions that work:
   * sklearn (0.23.2)
   * numpy (1.16.2)
   * pandas (1.0.2)
   * joblib (0.14.1)
   * shap (0.35.0)
   
   Packages essential to generating relevant figrues and the versions that work:
   
   * matplotlib (3.0.3)
   * sns (0.10.0)
   
2. Clone the repo

   ```sh
   git clone https://github.com/Karashan/C.albicans-ml-pipeline-data.git
   ```

3. Run the Python program (this program was built under Python 3.6.7 and should be able to run by a Python3 command)

   ```sh
   Python3 rf_pipeline.py
   ```



## Supplementary datasets

This repository manages supplementary datasets for the preliminary exam report under the directory `Supplementary Data`.



## License

Distributed under the MIT License. See `LICENSE` for more information.



## Contact

Please email to Xiang Zhang (zhan6668@umn.edu) if you have any questions, comments, or suggestions regarding this program.

Project Link: https://github.com/Karashan/C.albicans-ml-pipeline-data
