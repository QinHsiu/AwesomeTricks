- 参数初始化
  - 使用参数初始化主要有两种方式（使用预训练的模型的参数作为微调模型的初始参数，起到知识迁移的作用；随机初始化，但是限定了分布或者范围），使用第一种方式进行参数初始化可以起到知识迁移的效果，使得模型的初始位置在一个比较好的地方，这样更容易逃离鞍点；使用第二种方法进行参数初始化主要是为了限定参数的范围，加快模型的收敛速度；
  - 第一种使用预训练模型的参数进行初始化，需要注意参数大小必须一致；第二种一般将bais初始化为0，其他参数可以使用分布（均匀分布、高斯分布等）来限定参数的取值；
- 标准化
  - 深度学习模型假设模型的输入和输出都服从均值为0方差为1的分布，这样主要是为了公平对待每一个特征，使得优化的过程变得平稳，另外可以消除不同特征的数量级差别大带来的量纲影响；
  - 常用的技术有z-score、min-max、decimal scaling等，scale控制特征的重要性，大的scale的输出产生更大的误差，大的scale的输入特征可以主导网络对此特征的重视程度，产生更大的更新，一些特征本来取范围很小需要注意避免产生NaNs，在没有进行标准化时训练模型可能会增加模型的复杂程度，降低模型的收敛速度；
- 正则化
  - 使用正则化技术一方面可以缓解模型出现的过拟合现象，一方面可以加快模型的收敛速度，常用的正则化方法有Dropout、随机过程、噪音、数据增强等；
- 机器学习
  - [XGBoost中常见的10个参数](https://mp.weixin.qq.com/s/OWkde_9FAT6TxoSr9AzlQw)
- 神经网络
  - 单一的线性层网络结构
    一般的线性层网络可以看作对标量做了一个线性变换，其表达式如下所示，主要需要更新的参数包括两部分：权重和偏置
      $$f(x)=w^{T}\cdot x + b$$
  - 多层感知机(MLP)
    多层感知机在线性层的基础上引入了激活函数，而且使得层数加深，其目标是通过激活函数引入非线性变换，使得模型具有更好的鲁棒性，其表达式如下所示
      $$f(x)=mlp(x)=w^{T}\cdot (\sigma (w^{T}\cdot x + b_{0}))+b_{1}$$
  - 循环神经网络(RNN)
  - 卷积神经网络(CNN)
  - 自注意力机制(Self-Attention)
    - [MQA与GQA](https://mp.weixin.qq.com/s/B3Uv0tD4y-zCvclxx0_mOA)
  - 双向transformer(BERT)
    - [BERT上分tricks](https://mp.weixin.qq.com/s/3FftA8jM2e-BkMMin3sywg)
  - 自编码器
    - [如何通俗理解扩散模型](https://mp.weixin.qq.com/s/sUJcphngRGqPOsEUPq8-ig)     
  - 图神经网络(GNN)
  - 模型的应用
    - [时间序列预测中的深度学习算法简介](https://mp.weixin.qq.com/s/Ry3GKwasWwnrYumiSKKdyA)
