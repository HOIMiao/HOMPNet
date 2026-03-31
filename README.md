# HOMPNet: A Mutual Perception Network for Hand-Object Interaction Pose Estimation
## Create Dataset Files
### Dataset Directory
```
${ROOT}  
|-- data  
|   |-- HO3D
|   |   |-- data
|   |   |   |-- train
|   |   |   |   |-- ABF10
|   |   |   |   |-- ......
|   |   |   |-- evaluation
|   |   |   |-- train_segLable
|   |   |   |-- ho3d_train_data.json
|   |-- DEX_YCB
|   |   |-- data
|   |   |   |-- 20200709-subject-01
|   |   |   |-- ......
|   |   |   |-- object_render
|   |   |   |-- dex_ycb_s0_train_data.json
|   |   |   |-- dex_ycb_s0_test_data.json
```
### Dataset Download
You need to download the dataset and place them in the corresponding locations according to the dataset directory structure mentioned above. The download of the dataset is as follows:  
Download HO3D(v2) click [here](https://www.tugraz.at/institute/icg/research/team-lepetit/research-projects/hand-object-3d-pose-annotation/)  
Download DexYCB click [here](https://dex-ycb.github.io/)  
Dwonload the process data click [here](https://drive.google.com/drive/folders/1QnggoyWgZLuewWBDh4dTDuvr0UlJILNv)  
## MANO Layer
You need to download the MANO hand model and place it at:  
```
${ROOT}  
| -- assets
|    | -- mano_models
|    |    | -- MANO_RIGHT.pkl
|    |    | -- MANO_LEFT.pkl
```
Click [here](https://mano.is.tue.mpg.de/) dowm `MANO_RIGHT.pkl  MANO_LEFT.pkl`  
## Train
### on HO3D
```
sh sh/train_ho3d.sh
```
### on DexYCB
```
sh sh/train_dex-ycb.sh
```
## Test
### on HO3D
```
sh sh/train_ho3d_test.sh
```
The hand estimation results will be saved in the form of a compressed file of the predicted points. You need to run `eval/eval.py` to obtain the quantitative results.  
### on DexYCB
```
sh sh/train_dex-ycb_test.sh
```
### Visualize
Before running the above test script, you must first set `--visualize` to true.  
## Pretrained Weights
Click [here](https://pan.quark.cn/s/c64c689e04a9) to download the pre-trained weights.  
## Acknowledgements
We thank:  
- [HFL-Net](https://github.com/lzfff12/HFL-Net)  
- [Semi-Hand-Object](https://github.com/stevenlsw/Semi-Hand-Object)  
- [THOR-Net](https://github.com/ATAboukhadra/THOR-Net)  
