# Project Name

 car brand project > 

![image](https://github.com/SunYuhan0310/my_project/assets/141064414/bbc943ed-1037-491b-a17b-4cc15f1faec3)


## The Algorithm

Add an explanation of the algorithm and how it works. Make sure to include details about how the code works, what it depends on, and any other relevant info. Add images or other descriptions for your project here. 

cd jetson-inference
./docker/run.sh
cd python/training/classification
python3 train.py --model-dir=models/car_model data/car_data
python3 onnx_export.py --model-dir=models/car_model
Ctl + D
cd jetson-inference/python/training/classification
ls models/car_model
NET=models/car_model
DATASET=data/car_data

## Running this project

1. Add steps for running this project.
   imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/lamborghini/1.jpg lamborghini.jpg
2. Make sure to include any required libraries that need to be installed for your project to run.
sudo apt-get update
sudo apt-get install git cmake
git clone --recursive https://github.com/dusty-nv/jetson-inference
cd jetson-inference
git submodule update --init
sudo apt-get install libpython3-dev python3-numpy
mkdir build
cd build
cmake ../
make
sudo make install
sudo ldconfig

##video

https://youtu.be/YR3PfJABHnc
