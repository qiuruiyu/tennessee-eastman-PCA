# tennessee-eastman-PCA-pytorch
a simple example of fault diagnose with TE(tennessee-eastman) dataset, using PCA and pytorch 

## PCA folder 
the pca folder contains all the origin data and **matlab** code with ***.mlx***     
- **test.mlx**   
  achieve the PCA algorithm with eig, and visualize the data with lower dimension in **socre** and **loading** 
- **data_generator.mlx**
  used to combine several conditions of train / test data in a .csv file so that the data could be used in the pytorch code in **classify** folder
  
## Classify folder 
this folder contains the combined data and the pytorch code with JupyterNotebook.
- **train.csv** and **test.csv** contain 5 classes of fault to be classified   
- **train_all.csv** and **test_all.csv** contain all 22 classes of conditions (1 normal + 21 faults) to be classified   
- code contains 3 models:
  - ANN (all fc layers)
  - CNN (conv layers + maxpooling + fc layers)
  - PCA + SVM
  - ***maybe LSTM / Bi-LSTM in later commit***
