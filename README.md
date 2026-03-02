# ANN-Instructions

## How to run
After downloading the folder from github, follow the steps bellow to run the ANN.

### Install Conda
If you do not have Conda installed on your computer, make sure to install as we will need to create a Conda environment to run the ANN

### Install Tensorflow
The ANN only runs in a tensorflow (tf) environment, so tensorflow must be installed before doing anythign else.  
`conda install tf`

### Create a New Environment
The ANN will only run if a specifalized python environment is created. Attempting to run the ANN is the base environment will result in errors. Firsy, create this environment by running the command:  
`conda create --name tf tensorflow`  
After creating the environment, make sure that you are operating out of it by running:  
`conda activate tf`  
You will know if you are successful if the blue dot switched from the base environment to the tf environment.


### Install Additional Libraries
Install any additional libraries within the tf environment. The following were libraries I had to install, but you may need to install more:
`conda install conda-forge::pymatgen`  
`conda install anaconda::scikit-learn`

### Run!
To test that the ANNN is working run the following line of code:  
`python predict_from_formula.py --formula TiNbZr`  
If the ANN is working properly it should output:  
```
Phase code: Single phase: 0.0; multi phase: 1.0

Prediction(s) from ANN: 0.049 0.047 1.000
Prediction(s) from SVM: 0.000 0.000 1.000
```


## Common Errors
-make sure to run the code from the tensorflow environment instead of the base environment. You know you are doing this correctly when the dot next to the tf environment is blue.  
-if you encounter this error when running the ANN:  
```
TypeError: this __dict__ descriptor does not support '_DictWrapper' objects
```  
run this instead:  
`WRAPT_DISABLE_EXTENSIONS=true python predict_modify.py --formula TiNbZr`

## Questions?
contact me at emals2@illinois.edu  
also, thank you Wenwen for showing me how to run the code!
