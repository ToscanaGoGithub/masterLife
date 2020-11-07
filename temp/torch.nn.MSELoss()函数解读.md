函数作用
torch.nn.MSELoss() 求predict和target之间的loss。
代码示例
单个求其loss：
import torch
import torch.nn as nn
>>> crit=nn.MSELoss()
>>> target=torch.Tensor(1)
>>> target[0]=10
>>> res=torch.Tensor(1)
>>> res[0]=17.6
>>> cost=crit(res,target)
>>> cost                          #(10-17.6)^2=57.76
tensor(57.7600)

多个求其loss（结果为求平均loss）
>>> res=torch.Tensor(2)
>>> res[0]=1
>>> res[1]=2
>>> target=torch.Tensor(2)
>>> target[0]=2
>>> target[1]=3
>>> cost=crit(res,target)
>>> cost                            #（1+1）/2=1
tensor(1.)
