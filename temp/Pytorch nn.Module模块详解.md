torch.nn是专门为神经网络设计的模块化接口. nn构建于autograd之上，可以用来定义和运行神经网络。
nn.Module是nn中十分重要的类，包含网络各层的定义及forward方法。
如何使用pytorch如何定义自己的网络：
    -需要继承nn.Module类，并实现forward方法。继承nn.Module类之后，在构造函数中要调用Module的构造函数, super(Linear, self).init()
    -一般把网络中具有可学习参数的层放在构造函数__init__()中。
    -不具有可学习参数的层（如ReLU）可放在构造函数中，也可不放在构造函数中（而在forward中使用nn.functional来代替）。可学习参数放在构造函数中，并且通过nn.Parameter()使参数以parameters（一种tensor,默认是自动求导）的形式存在Module中，并且通过parameters()或者named_parameters()以迭代器的方式返回可学习参数。
    -只要在nn.Module中定义了forward函数，backward函数就会被自动实现（利用Autograd)。而且一般不是显式的调用forward(layer.forward), 而是layer(input), 会自执行forward().
    -在forward中可以使用任何Variable支持的函数，毕竟在整个pytorch构建的图中，是Varible在流动。还可以使用if, for, print, log等python语法。
    -Pytorch基于nn.Module构建的模型中，只支持mini-batch的Variable输入方式。比如，只有一张输入图片，也需要变成NxCxHxW的形式：
        input_image = torch.FloatTensor(1, 28, 28)
        input_image = Variable(input_image)
        input_image = input_image.unsqueeze(0)     # 1 x 1 x 28 x 28
如何把nn的层连接起来：
    我们发现每一层的输出作为下一层的输入，这种前馈nn可以不用每一层都重复的写forward()函数，通过Sequential()和ModuleList()，可以自动实现forward。这两个函数都是特殊module, 包含子module。ModuleList可以当成list用，但是不能直接传入输入。
Sequential构造方法？
    net1 = nn.Sequential()
    net1.add("conv", nn.Conv2d(3, 3, 5))
    net1.add("batchnorm", nn.BatchNorm2d(3))
    访问方式： net1.conv(input)

参考：
Pytorch nn.Module模块详解：https://blog.csdn.net/weixin_42018112/article/details/90084419