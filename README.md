# srcnn-tensorflow2
Tensorflow implementation of Convolutional Neural Networks for super-resolution. The original Matlab and Caffe from official website can be found [here](http://mmlab.ie.cuhk.edu.hk/projects/SRCNN.html).
## Prepare Data
Download training and test data from [baiduyun](https://pan.baidu.com/s/1QuIx2FlxowxAzr_-rrPGYQ) code: dtvj
Then create a new profile named 'checkpoint' and put data into it.
### Don't need download the data anymore, i have achive make own datasets by use a function 'input_setup', just put image in profile 'Train' and 'Test' is OK.
## pretrain
Set 'load_weights' 'last' or model filename to continue the previously interrupted training.
## Prerequisites
 * Tensorflow 2.1
 * Scipy version > 0.18 ('mode' option from scipy.misc.imread function)
 * h5py
 * matplotlib

This code requires Tensorflow. Also scipy is used instead of Matlab or OpenCV. Especially, installing OpenCV at Linux is sort of complicated. So, with reproducing this paper, I used scipy instead. For more imformation about scipy, click [here](https://www.scipy.org/).

## Usage
For training, `run train.py`set '--is_train == True'
For training, `run train.py`set '--is_train == False'

## Result
working！
My desktop performance is Intel I7-8750H CPU, GTX1060, and 24GB RAM.<br><br>

## References
* [tegg89/SRCNN-Tensorflow](https://github.com/tegg89/SRCNN-Tensorflow) 
  * - I referred to this repository which is same implementation using Matlab code and Caffe model.



scp -P 9922 ./train.py root@10.10.145.59:/train/ocr/all_model/srcnn-tensorflow2

git add . && git commit -m 'sadfasfd' && git push

nohup tensorboard --logdir=logs/ --port=8098 --bind_all >> tensorboard8098.log &
http://10.10.145.59:8098
nohup tensorboard --logdir=log/ --port=8097 --bind_all >> tensorboard8097.log &
http://10.10.145.59:8097
