# 基于Opencv的实时人脸识别
## 1.原理介绍: 
#### 人脸检测利用opencv进行图像处理,借用keras框架搭建卷积神经网络,对图像进行特征提取与特征训练,再利用训练好的分类模型进行预测,再将预测标签实时打在每一帧图片上,实现实时人脸检测与人脸标注.  
## 2.具体步骤:   
#### 2.1数据获取:借由opencv自带的人脸检测haarcascade_frontalface_alt2.xml进行人脸检测划分,构建起2*1000数据集.   
#### 2.2数据处理:利用opencv对图片进行读取,剪切,转为矩阵;划分好图片和标签集   
#### 2.3模型训练与保存: 
> 搭建CNN神经网络模型;  
> 对标签进行one-hot编码(用不同位置数组表示不同类型),对图像矩阵进行归一化;   
> 将处理好的数据分批量fit给模型,进行训练. 保存训练好的模型,以便调用.  
#### 2.4模型预测:调用训练完成的模型进行识别.  
