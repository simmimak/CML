# The Good Doctor

This README covers the steps to launch the two application tool to aid the training of a doctor. 

Application 1 : The Interactive Patient Simulator
Application 2 : The Diagnosis Tool

## Requirements 

Make sure to use **Python3** when running the scripts. The package requirements can be obtained by running `pip install -r requirements.txt`.

------------------------------------------
***Folder Description*** :point_left:
------------------------------------------
~~~

./application 1 deployment code --> Contains the deployment code to launch the gradio application 1.
./application 2 deployment code --> Contains the deployment code to launch the gradio application 2.
./application 2 model checkpoint --> Contains the relevant checkpoints to load the encoders: text and image for running the application 2.
./application 2 training code --> Training /Finetuning code of application 2. 
~~~

------------------------------------------
***Implementation Steps***
------------------------------------------
# 1. To deploy application 1

Run `python3 ./application 1 deployment code/gradio_application_1.py`.

This command can be run on a VM instance created on GCP and also locally, as it does not require heavy computation. 

# 1. For finetuning required for application 2. 

Run the SBATCH files located at "./application 2 training code/Sbatch-files for running on HPC"

These files can be run on HPC and any platform with GPU support.

# 2. To deploy application 2

Run `python3 ./application 1 deployment code/gradio_application_2.py`.

Please note that Application 2 involves inference on  GPUs, so ensure proper hardware availability or adapt the system based on your specific requirements

