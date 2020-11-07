PyTorch的nn.Linear（）是用于设置网络中的全连接层的，需要注意的是全连接层的输入与输出都是二维张量，一般形状为[batch_size, size]，不同于卷积层要求输入输出是四维张量。
in_features指的是输入的二维张量的大小，即输入的[batch_size, size]中的size。
  out_features指的是输出的二维张量的大小，即输出的二维张量的形状为[batch_size，output_size]，当然，它也代表了该全连接层的神经元个数。
  从输入输出的张量的shape角度来理解，相当于一个输入为[batch_size, in_features]的张量变换成了[batch_size, out_features]的输出张量。
用法：
import torch as t
from torch import nn

# in_features由输入张量的形状决定，out_features则决定了输出张量的形状 
connected_layer = nn.Linear(in_features = 64*64*3, out_features = 1)

# 假定输入的图像形状为[64,64,3]
input = t.randn(1,64,64,3)

# 将四维张量转换为二维张量之后，才能作为全连接层的输入
input = input.view(1,64*64*3)
print(input.shape)
output = connected_layer(input) # 调用全连接层
print(output.shape)

