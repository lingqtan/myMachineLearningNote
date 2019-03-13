# 06 支持向量机

## 6.1 SVM 的基本型

- 在多个可能的划分超平面中，应选择"最中间"的那个，因为其对训练样本局部扰动的"容忍"性最好
  <div align="center"><img src="./_images/6.1.0-1.png" height="900px" /></div>
  <div align="center"><img src="./_images/6.1.0-2.png" height="200px" /></div>

## 6.2 对偶问题

- 利用拉格朗日乘子法可得到 SVM 基本型的对偶问题，即对每条约束添加拉格朗日乘子 α_i >= 0
- 对偶问题揭示了 SVM 的一个重要性质：**训练的最终模型仅与支持向量有关，大部分训练样本不需要保留**
  <div align="center"><img src="./_images/6.2.0-1.png" height="350px" /></div>
  <div align="center"><img src="./_images/6.2.0-2.png" height="250px" /></div>

## 6.3 核函数

- 对于不能线性可分的问题，可从样本从原始空间映射到更高维的特征空间，使样本在这个特征空间内线性可分
- φ(x) 表示 x 映射后的特征向量，SVM 基本型和对偶问题中的 x_i 换成 φ(x_i)
- 核函数: 高维向量的内积计算 `<φ(x_i), φ(x_j)>` 转化为关于低维向量的函数 `κ(x_i, x_j)`
  <div align="center"><img src="./_images/6.3.0-1.png" height="500px" /></div>
- 通常不知道φ(x)的具体形式，"核函数选择"成为 SVM 的最大变数

## 6.4 软间隔与正则化

