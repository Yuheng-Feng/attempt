# 文件说明

## 在My-ZSSBIR文件中存放了代码
 ./model储存模型。其中，tip_model为基于语义交叉模态重建的零样本草图检索方法的模型，ijcai_model为基于视觉特征分解的零样本草图检索方法的模型。  
./checkpoint保存训练过程中得到的最优模型。  
./dataset/data.py处理数据的代码。   
traian_tip.py和train_ijcai.py分别是两个模型的训练代码。  
test_tip.py和test_ijcai.py分别是两个模型的测试代码。  
config.py是实验的参数设置。  

## 在ZS-SBIR文件中存放了草图数据
包括sketchy、TU-Berlin

# 训练和测试
## 将config.py中的“test”参数设置为False，并运行命令：

python ys_ijcai.py --dataset Sketchy    //训练Sketchy数据集并得到最终结果  
python ys_ijcai.py --dataset TU-Berlin //训练TU-Berlin数据集并得到最终结果  
python ys_tip.py --dataset Sketchy     
python ys_tip.py --dataset TU-Berlin  
 
## 将config.py中的“test”参数设置为True，并运行命令：

python ys_ijcai.py --dataset Sketchy    //在Sketchy数据集上，根据得到的最优模型进行测试的结果  
python ys_ijcai.py --dataset TU-Berlin //在TU-Berlin数据集上，根据得到的最优模型进行测试的结果  
python ys_tip.py --dataset Sketchy  
python ys_tip.py --dataset TU-Berlin  
