Mercari Price Suggestion Challenge-基于文本特征的价格模型

操作步骤：
1、首先应该对数据集进行分类，可以分为两个类型：数值（连续）特性，例如商品的价格，类别特征，商品是否包邮等。
2、对数据进行可视化，如果出现数据特别倾斜或者有长尾现象

如何处理商品的类目
如何处理数据中缺失的信息
如何处理商品描述

总结：
1、用正则或NLTK对句子分句然后分词，另外根据需求涉及stopwords，词型还原等.
2、用sklearn的TfidfTransformer及CountVectorizer或keras的一些工具将句子向量化，再加上一些其他统计特征.
3、使用NB,GBDT,FM,LR,NN等方法模型建模,融合.

ps:
1、NLTK:NLTK是Python上著名的自然语义处理库 https://zhuanlan.zhihu.com/p/98808960




参考链接：https://blog.csdn.net/Yasin0/article/details/89476618
如何构建商品定价模型？Mercari Price Suggestion Challenge 最佳方案出炉  https://cloud.tencent.com/developer/article/1075804
Mercari Price Suggestion in Kaggle  https://www.cnblogs.com/onemorepoint/p/11087155.html
Kaggle 商品定价预测最优方案出炉，如何从两千多支队伍中脱颖而出？  https://www.sohu.com/a/225705246_114877