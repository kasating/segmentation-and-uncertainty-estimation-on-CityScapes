# Bayesian Segmentation and Uncertainty estimation on CityScapes

<div align="center"><p>
    <a href="https://github.com/kasating/segmentation-and-uncertainty-estimation-on-CityScapes/pulse">
      <img src="https://img.shields.io/github/last-commit/kasating/segmentation-and-uncertainty-estimation-on-CityScapes?color=%4dc71f&label=Last%20Commit&logo=github&style=flat-square"/>
    </a>
    <a href="https://github.com/kasating/segmentation-and-uncertainty-estimation-on-CityScapes/blob/main/LICENSE">
      <img src="https://img.shields.io/github/license/kasating/segmentation-and-uncertainty-estimation-on-CityScapes?label=License&logo=GNU&style=flat-square"/>
</p>
</div>

​             

1. Implement **Bayesian SegNet** for semantic segmentation with **Pytorch**, and also generate estimates of **aleatoric and epistemic uncertainties** associated with the segmentation. Relevant codes and files are stored in `./Bayesian`,	

2. Implement **UNet** for semantic segmentation with **TensorFlow**. Stop  training due to a lack of GPUs. Relevant codes and files are stored in `./UNet`.		

   For more information on the dataset please refer to: [CityScapes dataset](https://www.cityscapes-dataset.com/). 
   This is also a team project for Deep Learning for Computer Vision course, lectured by MIT Prof. Alexander Amini.

   ​                      

## Table of Contents

- [Install](#install)
- [Usage](#usage)
- [Results](#Results)
- [Contributing](#contributing)
- [License](#license)

  ​                       

## Install

```
git clone git@github.com:kasating/Bayesian-Segmentation-and-Uncertainty-estimation-on-CityScapes.git
```

​                   

## Usage(Bayesian SegNet)

### 1. Requirements

``` shell 
pip install -r requirements.txt   
```

​                     

### 2. Pre-train Weights

Downloaded `vgg16_bn-6c64b313.pth` from https://download.pytorch.org/models/vgg16_bn-6c64b313.pth and put it in the same folder as `'./BayesianSegNet/'`.

​                

### 3. Dataset

Put `lab2_train_data.h5`  and `lab2_test_data.h5`  in `'./BayesianSegNet/'`.

​                   

### 4. Training and Testing

- **`./BayesianSegNet/main_segnet.ipynb` is the main file of this software lab.**

- Ignore the  first 4 cells in `./BayesianSegNet/main_segnet.ipynb` if you're not using Google Colab.

- To train the model, change the parameter `MODE` to `'TRAIN'` and run all cells in `./BayesianSegNet/main_segnet.ipynb`.
- To test the model only, change the parameter `MODE` to `TEST` and run all cells in `./BayesianSegNet/main_segnet.ipynb`. Model parameters are stored in `./BayesianSegNet/weights/model.pth`.

  ​                 

## Results(Bayesian SegNet)

![image.png](https://s2.loli.net/2022/02/16/GEJz4xvSHy2aRwO.png)

​                   

## Contributing

| Team Member | Contribution                                                 |
| ----------- | ------------------------------------------------------------ |
| Yitong  | Implement UNet for segmentation, including training and testing. |
| Zhuoyuan| Provide code of the UNet model structure. |
| Kaiang  | Generate and visualize estimates of aleatoric and epistemic uncertainties. |
| Wentao  | Implement Bayesian SegNet for segmentation, and generate the estimates of aleatoric and epistemic uncertainties. |
| Yaqi    | Help train UNet and write comments for it. |
| ALL     | Check through the team project. |

## License

[MIT License](https://github.com/kasating/Bayesian-Segmentation-and-Uncertainty-estimation-on-CityScapes/blob/main/LICENSE)

