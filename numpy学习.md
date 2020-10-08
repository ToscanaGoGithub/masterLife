numpy中的zeros(),ones()函数
zeros()返回一个全0的n维数组，一共有三个参数：shape（用来指定返回数组的大小）、dtype（数组元素的类型）、order（是否以内存中的C或Fortran连续（行或列）顺序存储多维数据）。后两个参数都是可选的，一般只需设定第一个参数。
>>> np.zeros(5)
array([ 0.,  0.,  0.,  0.,  0.])

>>> np.zeros((5,), dtype=np.int)
array([0, 0, 0, 0, 0])

>>> np.zeros((2, 1))
array([[ 0.],
       [ 0.]])

>>> s = (2,2)
>>> np.zeros(s)
array([[ 0.,  0.],
       [ 0.,  0.]])

>>> np.zeros((2,), dtype=[('x', 'i4'), ('y', 'i4')]) # custom dtype
array([(0, 0), (0, 0)],
      dtype=[('x', '<i4'), ('y', '<i4')])

ones()返回一个全1的n维数组，同样也有三个参数：shape（用来指定返回数组的大小）、dtype（数组元素的类型）、order（是否以内存中的C或Fortran连续（行或列）顺序存储多维数据）。后两个参数都是可选的，一般只需设定第一个参数。和zeros一样
>>> np.ones(5)
array([ 1.,  1.,  1.,  1.,  1.])

>>> np.ones((5,), dtype=np.int)
array([1, 1, 1, 1, 1])

>>> np.ones((2, 1))
array([[ 1.],
       [ 1.]])

>>> s = (2,2)
>>> np.ones(s)
array([[ 1.,  1.],
       [ 1.,  1.]])

通过安装导入numpy库，矩阵（ndarray）的shape属性可以获取矩阵的形状（例如二维数组的行列），获取的结果是一个元组，因此相关代码如下：
import numpy as np
x = np.array([[1,2,5],[2,3,5],[3,4,5],[2,3,6]])
#输出数组的行和列数
print x.shape  #结果： (4, 3)
#只输出行数
print x.shape[0] #结果： 4
#只输出列数
print x.shape[1] #结果： 3
