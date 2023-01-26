# CASPER-PerCom
This repo contains the work of the demo paper presented in **The 21st International Conference on Pervasive Computing and Communications (PerCom 2023)**.

Initial steps:

1. Download the dataset from IEEEDataPort: https://ieee-dataport.org/documents/casper-context-aware-anomaly-detection-system-industrial-robotic-arms
2. Extract the `casper.zip` file.

The dataset contains four files:
    * A .csv file that consists of accelerometer, gyroscope, and magnetometer data of an arm that accomplishes a repetitive task, captured via Nicla Sense ME.
    * Two .csv files (one per industrial arm) that consist of built-in arm parameters such as joint current, and velocity values etc.
    * A .pcap file that contains the TCP/IP traffic between the arms and the controller PC.

For this work, you will only need `right_arm.csv` and `nicla.csv`.

The whole test is around 24 hours.

We modify the joint velocity of the **right arm** after 14.4 hours (corresponding to 60%).

You should replace the `file paths` with your own paths.

The cells starts with `%%time` are expected to take longer running times depending on your setup. As the training, takes long time, we provide the saved model for convenience.

We run this experiment on a data science workstation with **NVIDIA RTX A6000**.

We provide a conda environment to test the work. 

Please check the following guide to install `conda`: https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html

After installing `conda`, create our environment via (set the path accordingly):

`conda env create -f environment.yml -p /home/user/anaconda3/envs/env_name`

Then follow the `casper.ipynb` to recreate the work.
