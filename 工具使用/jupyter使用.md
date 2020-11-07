1 kernel报错 主要原因可能是一个包冲突了 未解决
2/ AttributeError: type object 'IOLoop' has no attribute 'initialized' 说是 tornado版本过高，不支持jupyter notebook. 但是降低版本后还是不行
3/根本原因 jupyter notebook 环境中python版本不对应。该ipynb是基于python2环境，但是启动jupyter notebook 是在conda python3虚拟环境下打开的，故报错。 要是解决的话，应该安装对应python版本的notebook