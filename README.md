# PrivBayes

建立基于贝叶斯网络的差分隐私的保护数据发布模型，使得结构化数据同时兼备隐私性与效用性，模型主要步骤为： 

1.数据预处理：使用UCI的公开数据集Adult。构建二分k均值算法对连续型属性数据进行离散化处理，输出经处理后数据集；

2.设置差分隐私预算ε1，使用指数机制构建k度的贝叶斯网络，并输出d（d为数据集属性个数）对AP对以及对应的概率分布；

3.设置差分隐私预算ε2，在步骤2中生成的AP的概率分布中加入拉普拉斯噪声，从而形成具有噪声的概率分布；

4.利用贝叶斯网络祖先采样的方法，从步骤3中生成的具有的噪声的概率分布中进行采样，从而生成与原数据集具有同样的元组个数和属性个数的合成数据集；

5.采用α-边际分布和SVM分类器来验证原始数据集和合成的数据集的相似程度，从而验证合成数据集的隐私性和效用性。

# Reference
[1] Zhang J , Cormode G , Procopiuc C M , et al. PrivBayes: private data release via bayesian networks[M]. 2014.
