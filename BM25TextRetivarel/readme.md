# BM25 Model

## 解析

### 建模query与doc之间的相关度

![BM25](https://i.loli.net/2018/11/30/5c0147e798b97.png)

### MAP（Mean Average Precision）
* 只有1和0,1 代表相关 ， 0代表不相关
* Ap 某一次查询前 k 个里面查准率（precision）的均值（最终除以所有该类别的正确文档）
* MAP 所有qury的均值

### NDCG（Normalized Discounted Cumulative Gain）
* DCG 考虑不同的relevace值，并且计算rank值加权
* DCG = ri/log(i) 其中ri代表从上到下第i个返回doc的相关度，i代表位置
* NDCG 使用最大可能性进行归一化

## 过程

* 数据预处理（符号，停用词，token）
* 建立到排索引
* 实现OR操作
* 实现f(q,d）核函数
* 查询操作返回topK relevance 结果
* 使用map,NDCG进行评测

## 结果
* 取 topk = 200

|  | mymodel  | 给定result
| ------ | ------ |-------|
| Map | 0.56 | 0.76 |
| NDCG | 0.67 | 0.78 |

