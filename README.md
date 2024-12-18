# vit-base
This repository contains a comprehensive Google Colab Notebook for fine-tuning a pre-trained Vision Transformer (ViT) model on the CIFAR-10 dataset. 
## 冻结部分层
为什么冻结部分层？
（1）加快训练速度：
冻结大部分层只训练分类头，可以显著减少需要更新的参数数量，从而加快训练速度。
（2）防止过拟合：
在数据量较小或相似的任务中，冻结预训练的特征提取层可以防止模型过拟合，保留预训练模型的通用特征。
（3）节省计算资源：
冻结层减少了反向传播时需要计算的梯度，节省显存和计算时间。
对于 CIFAR-10 这样规模数据集，首先冻结底层特征提取器，仅训练分类头。这种策略能够快速获得良好的性能，并防止过拟合。
