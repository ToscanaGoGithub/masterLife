1 什么是张量 Tensor
    --Pytorch里面处理的最基本的操作对象就是Tensor（张量），它表示的其实就是一个多维矩阵，并有矩阵相关的运算操作。在使用上和numpy是对应的，它和numpy唯一的不同就是，pytorch可以在GPU上运行，而numpy不可以。所以，我们也可以使用Tensor来代替numpy的使用。当然，二者也可以相互转换。
    --Tensor的基本数据类型有五种：32位浮点型：torch.FloatTensor（default）；64位整型：torch.LongTensor；32位整型：torch.IntTensor；16位整型：torch.ShortTensor；64位浮点型：torch.DoubleTensor
    --如何进行定义：定义方式类似numpy，直接传入相应的矩阵就可以 a = torch.Tensor([[1, 2], [3, 4], [5, 6]])，不过在项目中，大多是以随机值或者特殊值进行初始化一个矩阵
        # 定义一个3行2列的全为0的矩阵
        b = torch.zeros((3, 2))
        # 定义一个3行2列的随机值矩阵
        c = torch.random((3, 2))
        # 定义一个3行2列全为1的矩阵
        d = torch.ones((3, 2))
    --tensor和numpy如何进行转换
        Numpy转化为Tensor：torch.from_numpy(numpy矩阵)
        Tensor转化为numpy：Tensor矩阵.numpy()
    -- 如何使torch在GPU上运行：只需要调用CUDA函数就可以

2、什么是变量 Variable？
    Pytorch里面的Variable类型数据功能更加强大，相当于是在Tensor外层套了一个壳子，这个壳子赋予了前向传播，反向传播，自动求导等功能，在计算图的构建中起的很重要的作用。其中最重要的两个属性是：data和grad。Data表示该变量保存的实际数据，通过该属性可以访问到它所保存的原始张量类型，而关于该 variable（变量）的梯度会被累计到.grad 上去。在使用Variable的时候需要从torch.autograd中导入。
    使用流程：定义变量-对函数自动求导，计算梯度-得到该函数各个变量的梯度


参考：PyTorch基础入门一：PyTorch基本数据类型 https://blog.csdn.net/out_of_memory_error/article/details/81258809

