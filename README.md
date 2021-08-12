# 因果推断方法小结
因果推断主要分类两类统计模型，一个是以Rubin为代表的潜在结果模型，另一个是以Pearl为代表的因果网络模型。
## 潜在结果模型
大多数潜在结果模型方法都属于计量经济学范畴，常用于评估政策效应，具体有以下几类。
### 断点回归

断点回归的主要原理是：存在一个变量，如果该变量大于这个临界值时，接受处置效应，小于临界值时，不接受处置效应，可以视作是对照组。经典案例有Chen et al.（2013）观察到的一条天然的分割线——秦岭淮河线，即以秦岭淮河线作为临界线，其中：淮河以北地区，政府用燃煤的方式提供暖气，视为接受政策干预；而淮河以南地区，并没有供应暖气，视为未接受政策干预。淮河两岸十分接近的两个地区，理论上其他各变量可以看作是连续的，也就是说其他的影响变量在南北两岸没有较大差异，而南北两岸唯一的区别就是有没有通过燃煤供暖，所以淮河以南可以作为很好的对照组，通过与实验组比较，识别政策干预效应。  

断点回归主要分为两类：

- 确定型（Sharp RDD）实线

- 模糊型（Fuzzy RDD）虚线
![RDD1](C:/Users/41558/Desktop/因果推断/RDD1.png)