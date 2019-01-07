# Clustering（聚类，文本聚类）

## 思路

* 构建vocab
* 构造每个文本段的tf-idf表示
* 使用聚类算法（sklearn）
> * K-means
> * Affinity propagation
> * Mean-shift
> * Spectral-clustering
> * Ward hierachical clustering
> * Agglomeractive clustering
> * DBSCAN
> * Gaussian Mixture

* 使用NMI(Normalized Mutual Information)评价指标

## 结果
* 在 至强E5 + DDR3 16G内存 + 2472 样本 +  5097维度表示向量的聚类结果
|        | time(s)   | NMI   |
| ------ | ------ |-------|
| K-means    | 77.46   | 0.794  |
| Affinity propagation   | 32.05   | 0.785  |
| Mean-shift   | 22.53  | 0.699  |
| Spectral-clustering   | 8.39   | 0.671  |
| Ward hierachical clustering   | 16.14   | 0.775  |
| Agglomeractive clustering   | 15.97   | 0.900  |
| DBSCAN  |  11.40  |  0.702 |
| Gaussian Mixture   |  302.2  | 0.702 |

* 结论： Agglomeractive（凝聚聚类）模型更加适合本次实验（稀疏文本向量表示的聚类问题）
