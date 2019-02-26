# 云吸狗也有啊哈时刻_WeRateDogs推文数据清洗与分析

## 综述

​	这个项目是[优达学城(Udacity)](https://cn.udacity.com/)数据分析师（进阶）纳米学位的第二个项目。以数据清洗的演练为主要目的，并附带了额外的分析部分。

​	我们整理的数据集是推特用户 [@dog_rates](https://twitter.com/dog_rates) 的推特记录，推特昵称为 [WeRateDogs](https://en.wikipedia.org/wiki/WeRateDogs)。WeRateDogs 是一个推特主，他以诙谐幽默的方式对人们的宠物狗评分。这些评分通常以 10 作为分母。但是分子则一般大于 10：11/10、12/10、13/10 等等。为什么会有这样的评分？因为 "[They're good dogs Brent.](http://knowyourmeme.com/memes/theyre-good-dogs-brent)" WeRateDogs 拥有四百多万关注者，曾受到国际媒体的报道。

​	我们在原始数据集中发现了14个问题，其中12个是质量问题，2个是整洁度问题。随后我们进行了一系列清洗操作。清洗操作完成后，我们为数据集手工添加了5个新的特征。在以点赞量和转赞比为核心指标，进行了推文受欢迎程度的主题探索后，我们发现以下三个现象：

- 人们对不同品种的狗的喜爱程度没有统计学意义上显著的区别；

- WeRateDogs推文中，关于小狗的没有关于大狗的受欢迎；

- 推主打出的低分和高分推文在受欢迎方式上有区别：低分推文的转赞比较高，而高分推文的平均点赞量更高。

  ​	我们自信，截至2019年2月底，这个项目数据所作清洗的细致程度和后续分析的深度，在全球这一项目的所有公开作品中都能排在前列。

## Repo文件说明

- 原始数据：
  - `twitter_archive_enhanced.csv`：包含推文内容，推文id和使用编写糟糕的程序提取的一些特征。
  - `tweet.json`：每条推特的附加数据，包含了推文的转发和点赞情况（因此也是此项目的核心数据集）。此数据集我们直接使用了优达学城提供的版本，没有选择通过Twitter API获取。
  - `image-predictions-download.tsv`：包含对推文图片中狗狗品种的预测。按照项目要求，这个文件使用了`Requst`库获取。
- 清洗后用于数据分析的主数据集：`twitter_archive_master.csv`
- 项目完整代码，探索过程及代码运行结果：`wrangle_act.ipynb`和`wrangle_act.html`
- 按照优达学城项目审阅要求整理的报告文件：
  - `act_report.md`，`act_report.pdf`, `act_report.html`：最终报告（不含代码)
  - `wrangle_report.md`和`wrangle_report.pdf`： 技术报告(记录数据处理方法等技术细节，不含代码)