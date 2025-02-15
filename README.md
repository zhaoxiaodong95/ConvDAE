# ConvDAE: convolutional denoising autoencoder
By: zhihong

Email: z_zhi_hong@163.com

## 1. Environments

- python 3.x
- TensorFlow 1.13.1
- numpy and so on



## 2. Networks Structures

- bsc-ConvDAE & L-ConvDAE: 

  ![image](https://github.com/dawnlh/ConvDAE/blob/master/pipeline/L-ConvDAE.png?raw=true)

  - the difference between bsc-ConvDAE and L-ConvDAE: 
    - bsc-ConvDAE use “max_pooling2d” in decoder， while L-ConvDAE use “deconv”

- U-ConvDAE: 
  ![image](https://github.com/dawnlh/ConvDAE/blob/master/pipeline/U-ConvDAE.png?raw=true)



## 3. Directories:

* logs: training logs
* model_data: trained models
* dataset: datasets
* demo: demo results
* predict_res: prediction results
* pipeline: structures of networks
* L-ConvDAE.py, U-ConvDAE.py, bsc_ConvDAE.py: 3 types of network structures
* ConvDAE_pred.py: prediction codes (based on trained models)
* ConvDAE_finetune.py: finetune condes (based on trained models)
* util: utility codes



## 4. Usage

- Modify corresponding parameters like path, epoches, training modes and so on according to your needs, and the trained models will be saved in the directory of "model_data"

- To use the trained models for prediction,  modify and run the "ConvDAE_pred.py", the results will be saved in the directory of "pred_res"
- To use the trained models for further finetuning,  modify and run the "ConvDAE_finetune.py", new models will be saved in the directory of "model_data"



## 5. Demo Results

![image](https://github.com/dawnlh/ConvDAE/blob/master/demo/unsup-ConvDAE_unsup_dots.png?raw=true)

![unsup](https://github.com/dawnlh/ConvDAE/blob/master/demo/sup-U-ConvDAE_N-MNIST-PIC.png?raw=true)

![unsup](https://github.com/dawnlh/ConvDAE/blob/master/demo/unsup-ConvDAE_unsup_N-MNIST-PIC.png?raw=true)



## 6. Notes

- In practice, in the unsupervised mode, bsc-ConvDAE and L-ConvDAE do better. And U-ConvDAE has relatively better performance in the supervised mode.

