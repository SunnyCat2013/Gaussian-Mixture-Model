# Learning Gaussian Mixture Model

# Illustration for updating sigma
## before updating sigma
![before_sigma](https://user-images.githubusercontent.com/4412909/50443115-cf2c8580-093c-11e9-89b8-7840e2fd05bf.png)
## after updating sigma
![after_sigma](https://user-images.githubusercontent.com/4412909/50443116-d2277600-093c-11e9-8198-4bea0e6a1a69.png)



# Questions
1. 在训练高斯混合模型的时候，每个模型的权重有几个？
是每个数据点对每个模型就有一个权重？
还是每个模型只有一个权重，所有的样本点对该模型使用相同的权重？

根据《统计学习方法》，应该是每个模型对应一个权重。这样确实可以使新数据有更好的适应性。


# Problems
1. 在计算高斯函数的时候，出现溢出现象。
原因是 `exp((digit - self.miu) ** 2 / (2 * (self.sigma ** 2))) / (sqrt(2 * pi) * self.sigma)` 因为加上了指数，很容易出现上溢的情况。
而这里我记错了 `exp` 里面的变量是因为加上负号的。


# 参考
《统计学习方法》
