# Brain-Tumor-in-MRI-Segmentation-using-U-NET
 This is a project for tumor segmentation in 2D MRI brain scans using a convolutional neural network with U-NET architecture.
 In this document, one can find the instructions on how to operate modules used in this model.
 
 All codes can be found in the Python notebook attached.
 
 ## Set-up and initialization
 The three first block codes provide initial set-up for the project.
 The first block is optional since it just provide connection to the Google Drive directory storing the training data.
 The second block is used for introducing libraries used in this project.
 The third block is to initalize constants to be used in the project.
 The NUM_TRAIN and NUM_TEST are to be found with your own dataset using some upcoming modules.
 Meanwhile, the NUM_OF_EPOCHS constant is to be set with your own preferences.
 Inside this block, the paths to the directories storing the training sets are also set.
 You can change these paths using your storing paths.
 
 ## Modules
 From the fourth block till the end are modules defined and used for the segmentation, predictions, evaluations and printing results.
 Starting with two generators defined for the data generation of training and testing data.
 The "display" module is used for general purpose of defining a function to be called for various result printing purposes.
 The "show_data" module will provide a glance on the slices available in the datasets.
 
 The architecture of the U-NET model is defined in the "unet" module. 
 Please find the paper of Ronneberger on the introduction of U-NET architecture for better understanding about this module.
 The following block is to calculate the steps in 1 given epoch.
 Furthermore, it also initializes a model using the "unet" module.
 The ckpt_path block is for loading the checkpoints you saved during the training to continue the process.
 So you can ignore this block during the first initialization of the model.
 The summary block is to provide a glance on how many weights are to be trained in the model.
 The next block of codes is to conduct the training with the desired epochs, batch size and steps.
 Along with this training, each updated weights set will be saved to the corresponding path.
 And then the model is saved, you can change the name and the saving directory with your own preferences.
 
 The next section which consists of 3 modules: "show_prediction", "evaluation" and "print_evaluation" is dedicated for displaying and evaluating predictions made by the model.
 For further understanding on the evaluation module, you could find the method of evaluation using True Positive, True Negative, False Positive and False Negative parameters.
 
 
 
