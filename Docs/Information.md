# ReadMe

# Tools

- 文档和代码的版本控制工具： **Git** 
  - [Git官网](https://git-scm.com/)
  - [廖雪峰的Git教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000) （注意：主要学习 pull, commit的使用即可，代码开发可能需要 branch和merge的知识）
- 文档写作 **Markdown**
  - 软件推荐： [Typora:windows,Mac都可以使用的免费Markdown语法编辑器](https://www.typora.io/)
  - 语法：
    - [Markdown简明语法](https://www.jianshu.com/p/191d1e21f7ed)
    - 详细的语法在**Typora** 软件中的 **Help->Markdown Reference** 有详细解答
- Github 的使用

## 2018.10.11. Meeting

+ 11.7. 中期答辩 前期文献调研，方案制定 迅速建立 讨论（和企业导师多进行交流）

## Tasks

+ 简介：[基于信令数据的人口时空分布预测模型构建  任务说明（公司方）](https://github.com/BigDataSystemTHU2018/Project-Unicom/blob/master/IntroBrief.md) 

+ 任务描述：通过历史的人口时空分布数据，来预测未来的人口时空分布~具体说的话，通过北京六环以内，1km网格尺度的分天分小时人口分布数据（历史数据的时间跨度可以拉长到3个月）预测未来一周 相应网格下**每天每小时** 的人口分布（给出的数据是其实是信号的分布数据 不过一般认为一个设备就代表一个人了）（数据量，六环内差不多2000多个网格，但从初始数据量而言不大，但是对于其深入挖掘和处理却是难点）
  + 可能难点：
    + 首先，手机的信号数据（网格是1km）直接对应人口分布是否可以接受 
    + 另外，三个月的时间长度是不是足够预测一周，或者预测一周需要多久的数据（可能需要提出新的数据要求或者调整目标）
    + 对于人口分布的预测，不会只和历史数据有关系，是否需要得到对应的季节和天气的变化等额外会对分布有影响的数据（有哪些数据可能会影响？怎么得到？）
    + 注意：数据 会包含空间信息 单纯考虑时间会有问题 比如西单的人口量跟周围 清华的人口量跟周围之间  会有一定的关系（对于数据的理解角度和维度是否有别的理解）
+ 前期调研
  + 参考文献：
    + [城市计算_微软](https://www.microsoft.com/en-us/research/project/urban-computing/)
    + 代表文献：
      + [Deep Spatio-Temporal Residual Networks for Citywide Crowd Flows Prediction (Code,Slides,Pdf)](https://www.microsoft.com/en-us/research/publication/deep-spatio-temporal-residual-networks-for-citywide-crowd-flows-prediction/)
      + [DNN-Based Prediction Model for Spatio-Temporal Data](https://www.microsoft.com/en-us/research/publication/dnn-based-prediction-model-spatial-temporal-data/) 
    + [一个城市计算的相关资料的汇总](https://www.zhihu.com/question/25359731)

  + 可能分析角度（update on 10.23.）

    [城市异常预测](https://www.microsoft.com/en-us/research/project/%E5%9F%8E%E5%B8%82%E8%AE%A1%E7%AE%97/)  :**基于大数据的人流预测**

    + **城市区域人流预测** 

        ![](https://github.com/BigDataSystemTHU2018/Project-Unicom/blob/master/Media/Pics/pre.png)

      + 将城市通过主干道分成具有语义信息的区域，通过融合交通、气象和事件等各种大数据，预测各个区域内未来几小时人流进入和流出的数量，以便提前启动预警机制，及早疏导人群和车流，保障区域内短时人口密度在安全范围内，从而防范重大交通事故和灾难性城市安全事件（如踩踏）的发生。
      + 论文：[FCCF: Forecasting Citywide Crowd Flows
        Based on Big Data](https://www.microsoft.com/en-us/research/publication/forecasting-citywide-crowd-flows-based-big-data/)

    + **基于深度学习的城市网格人流预测**

      ![](https://github.com/BigDataSystemTHU2018/Project-Unicom/blob/master/Media/Pics/dnn.png)

      + 将城市分割成均匀网格，基于交通、气象、时间和事件等多源信息，采用深度学习（Deep Learning）的方法，来综合预测未来每个网格的进入和流出人流数，以便提前启动预警机制，及早疏导人群和车流，保障区域内短时人口密度在安全范围内，从而防范重大交通事故和灾难性城市安全事件（如踩踏）的发生。在采用深度学习算法时，我们充分考虑的时空数据的属性，设计的更为合理的网络结构来模拟人流数据的周期性、趋势性和时空的邻近性等特征，取得了比简单CNN更好的效果。
      + 论文
        + [Deep Spatio-Temporal Residual Networks for Citywide Crowd Flows Prediction](https://www.microsoft.com/en-us/research/publication/deep-spatio-temporal-residual-networks-for-citywide-crowd-flows-prediction/)
        + [DNN-Based Prediction Model for Spatio-Temporal Data](https://www.microsoft.com/en-us/research/publication/dnn-based-prediction-model-spatial-temporal-data/)

## Schedule

+ 分工

  + 前期（**11.7.** 前完成）
    + 前期文献调研和分析
    + 方案设计和初步实践

+ 组员基本技能情况调研

  + 肖飞宇：熟练掌握**Latex** 可总体负责文档编写，会一定的C++，Python以及机器学习和人工智能的算法可以帮助一些代码构建和分析（负责总体协调）
  + 牛苒: 用Excel处理数据/Tableau数据可视化/PPT和presentation/金融Excel建模和分析
  + 沈磊：比较熟练matlab，会一点linux，c++，python。
  + 荆科: python,scrapy,回归分析，文本分析，各种设计
  + 赵嘉欣：会c++，python以及机器学习等算法
  + 李司棋：python在学，会matlab，c++，群智能相关算法，会一点STATA分析金融数据。也善于撰写报告和pre。
  + 张玉生：matlab，python，c++属于一般水平。机器学习及人工智能初学阶段。
  + 韦承志：会一定的python，Matlab，SQL（MySql），经典人工神经网络。爬虫在学。

# Meeting 10.14.

- 技术层面：几个可能的要点为
  - 信令数据的特征，即需要如何认识这种数据的结构和特点，以及我们可能如何将其和人口分布的预测联系起来
  - 可能采取的算法：基于现有的实现算法？（但是需要对其中有一些认识而不是单纯的按照demo）或者提出一些可能的方法（文献调研，甚至不需要实现，但是或许会对我们的结果分析有帮助）
  - 具体的实现方法
- 任务
  - 代码侧
    - 首先阅读核心文献的代码 尝试实现 并总结技术难点和要点（比如前期数据的转换 后期可视化 如何调库 如何调参）
    - 其他可能的实现方法 的调研和可能的实现（A班同学做？）
    - 相关可能涉及的软件的使用 如数据可视化的方法等（B班同学总结需求 或许A班同学可以做）
  - 调研侧
    - 调研对于信令数据的分析和理解 主要和人口预测的关系
    - **重要** 如何分析数据 对于最后的结果做怎样的迭代 比如 东城区和海淀区的预测结果的精度的比较 不同因素的影响（天气和节日 交通线）
      - 分析 不同区域如交通线在上下班时的预测情况 分析结果
  - **关键点** 
    - 城市计算的整体的背景
    - 算法的关键点
  - 核心文献 A B 班同学共同阅读

