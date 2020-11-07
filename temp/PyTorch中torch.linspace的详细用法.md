线性间距向量
torch.linspace(start, end, steps=100, out=None) → Tensor

返回一个1维张量，包含在区间start和end上均匀间隔的step个点。

输出张量的长度由steps决定。
参数：

start (float) - 区间的起始点

end (float) - 区间的终点

steps (int) - 在start和end间生成的样本数

out (Tensor, optional) - 结果张量

应用:#生成0到10的4个数构成的等差数列 a = torch.linspace(0,10,steps=4)