# nnUNet_NonLocal_WS
A modification code based on nnUNet (https://github.com/MIC-DKFZ/nnUNet)

# How to use our code
- Preproccesing [0_NNUNET_Preprocess.ipynb](https://github.com/kevinkwshin/nnUNet_NonLocal_WS/blob/main/0_NNUNET_Preprocess.ipynb)
base = "nnUNet_base/"
preprocessing_output_dir = "nnUNet_preprocessed/"
network_training_output_dir_base = "RESULTS_FOLDER/"

- Training [1_NNUNET_Training.ipynb](https://github.com/kevinkwshin/nnUNet_NonLocal_WS/blob/main/1_NNUNET_Training.ipynb)
  Construct the training and validation datasets with 5 folds, we trained each with 5 segmentation models to run the voting ensemble.
- Prediction [2_NNUNET_Prediction.ipynb](https://github.com/kevinkwshin/nnUNet_NonLocal_WS/blob/main/2_NNUNET_Prediction.ipynb)
  We applied the testset to 5 trained models and saved the results in a separate folder for each.
- Evaluation [3_NNUNET_Ensemble.ipynb](https://github.com/kevinkwshin/nnUNet_NonLocal_WS/blob/main/3_NNUNET_Ensemble.ipynb)
  We performed a pixel-wise 2/5 voting ensemble on the segmentation results of 5 models.

# Code modified from original nnUNet
generic_Unet.py Non_Local

