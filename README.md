# Two projects for Zero-Shot Sketch-Based Image Retrieval
We put them into one.

## Paper Address
### Progressive Domain-Independent Feature Decomposition Network for Zero-Shot Sketch-Based Image Retrieval
the paper received by IJCAI20 can be obtained from [arXiv](https://arxiv.org/abs/2003.09869) or [pdf](https://www.ijcai.org/Proceedings/2020/0137.pdf).

### Progressive Cross-Modal Semantic Network for Zero-Shot Sketch-Based Image Retrieval
the paper received by TIP20 can be obtained from [pdf](https://ieeexplore.ieee.org/document/9194144).



## The version used in this project
python 3.7.5  
torch 1.3.0+cu100  
Cuda compilation tools, release 10.1, V10.1.243



## File directory annotation

###  `./My-ZSSBIR` contsins the code and models
 `./model`contains models.   
 `./model/tip_model.py` is Progressive Cross-Modal Semantic Network.   
 `./model/ijcai_model.py` is Progressive Domain-Independent Feature Decomposition Network.   
`./checkpoint` saves the best model during training.  
`./dataset/data.py` is the code to process the data.  
`./traian_tip.py` and `./My-ZSSBIR/train_ijcai.py` are training code of two models.  
`./test_tip.py` and `./My-ZSSBIR/test_ijcai.py`are test code of two models.  
`./config.py` contains the experiment setting parameters.  
You have to notice <strong>the path</strong> in `ys_ijcai.py` and ` ys_tip.py` , if you need to change.  

### `./ZS-SBIR` contains datasets
The size of `./ZS-SBIR` is about 9.7G, which contains Sketchy(5.1G) and TU-Berlin(4.7G).  

File directory structure as follow：  
- Sketchy
  - extebded_photo
  - hed
  - photo
  - sketch
- TU-Berlin
  - hed
  - images
  - sketches



## Train and Test
### set the parameter `'test'` in `config.py` as `False` and run:

`python ys_ijcai.py --dataset Sketchy`    // train Sketchy and get a final result.  
`python ys_ijcai.py --dataset TU-Berlin` // train TU-Berlin and get a final result.  
`python ys_tip.py --dataset Sketchy`  
`python ys_tip.py --dataset TU-Berlin`   

### set the parameter `'test'` in `config.py` as `True` and run:

`python ys_ijcai.py --dataset Sketchy`   // test the best model trained on Sketchy to get result.  
`python ys_ijcai.py --dataset TU-Berlin`// test the best model trained on TU-Berlin to get result.  
`python ys_tip.py --dataset Sketchy`   
`python ys_tip.py --dataset TU-Berlin`  
