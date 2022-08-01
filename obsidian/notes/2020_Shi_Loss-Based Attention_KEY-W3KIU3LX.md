# Loss-Based Attention for Deep Multiple Instance Learning
> [!info]+ <center>Metadata</center>
> 
> |<div style="width: 5em">Key</div>|Value|
> |--:|:--|
> |文献类型|journalArticle|
> |标题|Loss-Based Attention for Deep Multiple Instance Learning|
> |短标题||
> |作者|[[Xiaoshuang Shi]]、 [[Fuyong Xing]]、 [[Yuanpu Xie]]、 [[Zizhao Zhang]]、 [[Lei Cui]]、 [[Lin Yang]]|
> |期刊名称|[[Proceedings of the AAAI Conference on Artificial Intelligence]]|
> |DOI|[10.1609/aaai.v34i04.6030](https://doi.org/10.1609/aaai.v34i04.6030)|
> |存档位置||
> |馆藏目录||
> |索书号||
> |版权|Copyright (c) 2020 Association for the Advancement of Artificial Intelligence|
> |分类|[[00_Histology, 202204, MIL]]|
> |条目链接|[My Library](zotero://select/library/items/W3KIU3LX)|
> |PDF 附件|<ul><li><a href="zotero://open-pdf/library/items/3P7B674A">Full Text PDF</a></li><li><a href="zotero://open-pdf/library/items/EKX2QURQ">zhao2020.pdf</a></li></ul>|
> |关联文献|[[2018_Ilse_Attention-based Deep_KEY-GMXKWTZJ]]、 [[2020_Lu_Data Efficient and W_KEY-R8BCS375]]|
> ^Metadata


> [!example]- <center>本文标签</center>
> 
> `$=dv.current().file.tags`


> [!quote]- <center>Abstract</center>
> 
> Although attention mechanisms have been widely used in deep learning for many tasks, they are rarely utilized to solve multiple instance learning (MIL) problems, where only a general category label is given for multiple instances contained in one bag. Additionally, previous deep MIL methods firstly utilize the attention mechanism to learn instance weights and then employ a fully connected layer to predict the bag label, so that the bag prediction is largely determined by the effectiveness of learned instance weights. To alleviate this issue, in this paper, we propose a novel loss based attention mechanism, which simultaneously learns instance weights and predictions, and bag predictions for deep multiple instance learning. Specifically, it calculates instance weights based on the loss function, e.g. softmax+cross-entropy, and shares the parameters with the fully connected layer, which is to predict instance and bag predictions. Additionally, a regularization term consisting of learned weights and cross-entropy functions is utilized to boost the recall of instances, and a consistency cost is used to smooth the training process of neural networks for boosting the model generalization performance. Extensive experiments on multiple types of benchmark databases demonstrate that the proposed attention mechanism is a general, effective and efficient framework, which can achieve superior bag and image classification performance over other state-of-the-art MIL methods, with obtaining higher instance precision and recall than previous attention mechanisms. Source codes are available on https://github.com/xsshi2015/Loss-Attention.


> [!tldr]- <center>隐藏信息</center>
> 
> itemType:: journalArticle
> title:: Loss-Based Attention for Deep Multiple Instance Learning
> shortTitle:: 
> creators:: [[Xiaoshuang Shi]]、 [[Fuyong Xing]]、 [[Yuanpu Xie]]、 [[Zizhao Zhang]]、 [[Lei Cui]]、 [[Lin Yang]]
> publicationTitle:: [[Proceedings of the AAAI Conference on Artificial Intelligence]]
> journalAbbreviation:: 
> volume:: 34
> issue:: 04
> pages:: 5742-5749
> language:: en
> DOI:: [10.1609/aaai.v34i04.6030](https://doi.org/10.1609/aaai.v34i04.6030)
> ISSN:: 2374-3468
> url:: [https://ojs.aaai.org/index.php/AAAI/article/view/6030](https://ojs.aaai.org/index.php/AAAI/article/view/6030)
> archive:: 2022-07-25
> archiveLocation:: 
> libraryCatalog:: 
> callNumber:: 
> rights:: Copyright (c) 2020 Association for the Advancement of Artificial Intelligence
> extra:: 🏷️ _顶会、/Done、📒
> collection:: [[00_Histology, 202204, MIL]]
> tags:: #_顶会 #Done 
> related:: [[2018_Ilse_Attention-based Deep_KEY-GMXKWTZJ]]、 [[2020_Lu_Data Efficient and W_KEY-R8BCS375]]
> itemLink:: [My Library](zotero://select/library/items/W3KIU3LX)
> pdfLink:: <ul><li><a href="zotero://open-pdf/library/items/3P7B674A">Full Text PDF</a></li><li><a href="zotero://open-pdf/library/items/EKX2QURQ">zhao2020.pdf</a></li></ul>
> qnkey:: 2020_Shi_Loss-Based Attention_KEY-W3KIU3LX
> date:: 2020-04-03
> dateY:: 2020
> dateAdded:: 2022-04-25
> dateModified:: 2022-07-25
> year:: 2022
> dateCurrent:: 2022-08-01
> time:: 10:34:17
> week:: 星期一
> yearMonth:: 2022-08
> dateWeek:: 2022-08-01 星期一
> dateTime:: 2022-08-01 10:34:17
> dateWeekTime:: 2022-08-01 10:34:17 星期一
> 
> abstract:: Although attention mechanisms have been widely used in deep learning for many tasks, they are rarely utilized to solve multiple instance learning (MIL) problems, where only a general category label is given for multiple instances contained in one bag. Additionally, previous deep MIL methods firstly utilize the attention mechanism to learn instance weights and then employ a fully connected layer to predict the bag label, so that the bag prediction is largely determined by the effectiveness of learned instance weights. To alleviate this issue, in this paper, we propose a novel loss based attention mechanism, which simultaneously learns instance weights and predictions, and bag predictions for deep multiple instance learning. Specifically, it calculates instance weights based on the loss function, e.g. softmax+cross-entropy, and shares the parameters with the fully connected layer, which is to predict instance and bag predictions. Additionally, a regularization term consisting of learned weights and cross-entropy functions is utilized to boost the recall of instances, and a consistency cost is used to smooth the training process of neural networks for boosting the model generalization performance. Extensive experiments on multiple types of benchmark databases demonstrate that the proposed attention mechanism is a general, effective and efficient framework, which can achieve superior bag and image classification performance over other state-of-the-art MIL methods, with obtaining higher instance precision and recall than previous attention mechanisms. Source codes are available on https：//github.com/xsshi2015/Loss-Attention.


👣➿👣


## ✏️ 笔记区

>[!inbox]- <center>📫 笔记简报</center>
>
> ⏰ importDate:: 2022-07-26

> [!IMPORTANT]+ <center>🌱 研读印象</center>  
>
>📌 comment::  

> [!WARNING]+ <center>🐣 总结</center>  
>
>🎯 研究问题::  
🔎 研究背景::  
🚀 研究方法::  
🐔 研究思路::  
📺 主要内容::  
🎉 研究结论::  
🗝️ 创新点::  
💩 研究局限::  
🐾 研究展望::  
✏️ 备注::  



👣➿👣

## 📝 注释笔记 3P7B674A

> <span style="font-size: 15px;color: gray">📍 2020-Shi-Loss-Based Attention for Deep Multiple Instance Learning</span>

^KEYrefTitle

> <span class="highlight" style="background-color: #ff666640">Additionally, previous deep MIL methods firstly utilize the attention mechanism to learn instance weights and then employ a fully connected layer to predict the bag label, so that the bag prediction is largely determined by the effectiveness of learned instance weights.</span>  
> 之前的attentionMIL很大程度上会受到学习到的instance有效权重的影响 ([p5742](zotero://open-pdf/library/items/3P7B674A?page=5742&annotation=PRIEBFY8))

^KEYPRIEBFY8

> <span class="highlight" style="background-color: #ff666640">simultaneously learns instance weights and predictions</span>  
> 同时学习instance的权重和预测 ([p5742](zotero://open-pdf/library/items/3P7B674A?page=5742&annotation=9A6LZ95E))

^KEY9A6LZ95E

> <span class="highlight" style="background-color: #ff666640">Additionally, a regularization term consisting of learned weights and crossentropy functions is utilized to boost the recall of instances, and a consistency cost is used to smooth the training process of neural networks for boosting the model generalization performance.</span> ([p5742](zotero://open-pdf/library/items/3P7B674A?page=5742&annotation=6H47CFN2))

^KEY6H47CFN2

> <span class="highlight" style="background-color: #ffd40040">The main goal of MIL</span>  
> MIL的主要目标 ([p5742](zotero://open-pdf/library/items/3P7B674A?page=5742&annotation=KGIX4RXE))

^KEYKGIX4RXE

> <span class="highlight" style="background-color: #ffd40040">expectation-maximization (EM) methods</span> ([p5743](zotero://open-pdf/library/items/3P7B674A?page=5743&annotation=XJ2TGMBX))

^KEYXJ2TGMBX

> <span class="highlight" style="background-color: #ffd40040">n bags</span> ([p5744](zotero://open-pdf/library/items/3P7B674A?page=5744&annotation=64RBM3KD))

^KEY64RBM3KD

> <span class="highlight" style="background-color: #ffd40040">ni instances</span> ([p5744](zotero://open-pdf/library/items/3P7B674A?page=5744&annotation=PZQ9UKZV))

^KEYPZQ9UKZV

> <span class="highlight" style="background-color: #ff666640">hL−1 i is obtained by a mean operator</span>  
> 对所有的instance的特征输出做了个mean，然后再用 ([p5744](zotero://open-pdf/library/items/3P7B674A?page=5744&annotation=DZQJUZBN))

^KEYDZQJUZBN

> <span class="highlight" style="background-color: #ffd40040">exp(zi,j,k) ≈ ∑K−1 c=0 exp(zi,j,c).</span> ([p5745](zotero://open-pdf/library/items/3P7B674A?page=5745&annotation=RHBIVZ7A))

^KEYRHBIVZ7A

> <span class="highlight" style="background-color: #ffd40040">the popular maxpooling operator in Theorem 1</span> ([p5745](zotero://open-pdf/library/items/3P7B674A?page=5745&annotation=SMM5393S))

^KEYSMM5393S

> <span class="highlight" style="background-color: #ff666640">Theorem 1</span>  
> 对比attention和max操作，尽管效果是一样的，但是attention的会平滑 ([p5745](zotero://open-pdf/library/items/3P7B674A?page=5745&annotation=77K5DVL4))

^KEY77K5DVL4







