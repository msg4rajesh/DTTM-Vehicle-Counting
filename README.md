# DTTM-Vehicle-Counting
## Introduction
In this repo, we include the submission to AICity Challenge 2020 Vehicle Counts by Class at Multiple Intersections (Didi Chuxingsubmission).

We propose a robust and fast vehicle turn-counts at intersections via an integrated solution from detection, tracking and trajectory modeling. 
Our team ranks 6th in Public leaderboard and models of our algorithms are not trained with any extra datasets. 

## Installation
Our code is tested on Tesla P40, 24G with following setting:  
1. Linux  
2. Python 3.6 (only test on python 3.6)  
3. PyTorch 1.1 or higher  
4. CUDA 10  
5. NCCL 2  
6. GCC 4.9 or higher  

The fast way to install our code is running commond as follows:
```
pip3 install -r requirements.txt
```
Attention: If there are any errors about mmcv or mmdetection, please refer [Mmdetection](https://github.com/open-mmlab/mmdetection) to install mmdetection first.
## Test
### Get videoes directory of Track1:
After downloading packages of AICity Challenge 2020 Track1, please unzip and **$DirPath\_to\_Track1\_AIC20\_track1** is the final directory after unzip.
### Download detection model:
1. Download our detection model on [RetinaNetNas-FPN](https://drive.google.com/file/d/1ieo-umrILexsytRql6wQEMMHoAVMKQ_d/view?usp=sharinghttps://drive.google.com/file/d/1ieo-umrILexsytRql6wQEMMHoAVMKQ_d/view?usp=sharing) 
2. Put the model in directory **$root/detection/NAS\_FPN/checkpoints**
3. Then our code can be run as follows
### Run test code 
```
python  multi_process.py --video_dir=$DirPath_to_Track1_AIC20_track1
```
The final counting results will be stored in **$root/count_nums/**  

## Reference
[Mmdetection](https://github.com/open-mmlab/mmdetection)

 
