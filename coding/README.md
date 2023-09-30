# Getting Started Tutorial
You should install the Aomalib library first and Openvino should be installed manually only in Raspberry pi

## Step1: Installation

# Installation(on PC)
Install Anomalib
1. Open a terminal and open a folder
2. git clone https://github.com/openvinotoolkit/anomalib.git
3. cd anomalib
4. pip install -e .

# Installation(on Raspberry pi)
Install Anomalib
1. Open a terminal and open a folder
2. git clone https://github.com/openvinotoolkit/anomalib.git
3. cd anomalib
4. pip install -e .

# Download Openvino
1. go to https://storage.openvinotoolkit.org/repositories/openvino/packages/2023.1/linux/
2. download l_openvino_toolkit_debian9_2023.1.0.12185.47b736f63ed_armhf.tgz

# Install Openvino
1. sudo mkdir -p /opt/intel/openvino_2023
2. sudo tar -xf  l_openvino_toolkit_debian9_2023.1.0.12185.47b736f63ed_armhf.tgz --strip 1 -C /opt/intel/openvino_2023
3. sudo apt install cmake
4. source /opt/intel/openvino_2023/bin/setupvars.sh
5. echo "source /opt/intel/openvino_2023/bin/setupvars.sh" >> ~/.bashrc
6. If you input [setupvars.sh], it should say 'OpenVINO environment initialized'

## Step2: Data Collection

Data Collection
1. Put the folders in dataset into your local folder
2. 20,50,80 means different sizes for the datasets
3. Each folder has normal and Abnormal folders and put the images into both of them
4. If you change the location or the name of those datasets then you only need to modify the path in the config file 


## Step3: Model training and testing

# Configuration
1. Padim_config.yaml and Patchcore_config.yamal are configuration files for the ML training and testing.
2. put this into src/anomalib/models/Padim/ and src/anomalib/models/Patchcore/ path respectively
3. for the file themselves, yo can modify the hyperparameter of machine learning training 

For the Coding parts, we have integrated python file 'main.py' and jupyter books file for seperate steps. Both of them are the same. 
You can use the main.py to do employment when you make sure the each steps working correctly with the jupyter book.
# Training and Inference process
1. For python file, just run the file 'main.py'
2. For the Jupyter filer, use it to test and modify the code cause you can check each step there.











