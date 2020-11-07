class torch.optim.SGD(params, lr=, momentum=0, dampening=0, weight_decay=0, nesterov=False)[source]
实现随机梯度下降算法（momentum可选）。

Nesterov动量基于On the importance of initialization and momentum in deep learning中的公式.

如何使用optimizer：要使用torch.optim，您必须构造一个optimizer对象。这个对象能保存当前的参数状态并且基于计算梯度更新参数。


参数：

params (iterable) – 待优化参数的iterable或者是定义了参数组的dict
lr (float) – 学习率
momentum (float, 可选) – 动量因子（默认：0）
weight_decay (float, 可选) – 权重衰减（L2惩罚）（默认：0）
dampening (float, 可选) – 动量的抑制因子（默认：0）
nesterov (bool, 可选) – 使用Nesterov动量（默认：False）