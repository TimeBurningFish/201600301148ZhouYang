# 布尔查询与倒排索引

## 解析
### 倒排索引（Inverted Index）
简单讲可以理解为一种结构：term - freq - [docIDi] <i from len(docs)> <br>
这种结构组成了vocab

### 布尔查询
对用户输入的query结构化成为一个布尔表达式<br>
布尔表达式的结果是topk个相关document<br>
关键操作即 and or not 三种对有序链表（list）的逻辑操作


## 任务清单
- 数据预处理 √ 
- 建立到排索引 √ 
- 实现query的AND，NOT，OR逻辑 √ 
- 查询操作返回topK结果 √ 
- 实现（）运算 优先级运算 √ 
- 实现中缀表达式 后缀表达式的转换 √ 
- 实现top_k的加强可视化
