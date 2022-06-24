---
title: workflow_of_C_and_O_adsorption_energy_prediction
created: '2022-06-14T09:43:26.939Z'
modified: '2022-06-23T08:45:34.935Z'
---

## Step 1: Using DFT to prepare database  
The database is provided in [C](./database_C.dat)  
and [O](./database_O.dat) for C and O adsorption, especially.  
  
## step 2. Use database_DNN.dat to train DNNs
run: python [kerasNN.py](https://github.com/kechangming/DL-accelerated-catalysis-design/blob/main/kerasNN.py)   
output: trained_model_file for [C](https://github.com/kechangming/DL-accelerated-catalysis-design/blob/main/model_file_C.h5) and [O](https://github.com/kechangming/DL-accelerated-catalysis-design/blob/main/model_file_O.h5) 
### Training error:
<img src="./error_in_training.png" width="50%"> </span>
### Training results:
<p> <img src="./validation_of_O.png" width="50%"><img src="./validation_of_C.png" width="50%"> </p>

## Step 3. using trained model to predict O and C adsorption energy of alloys
run: python NNPredict.py (inputs include properties_of_alloys.txt and model_file.h5)
![figure]()

