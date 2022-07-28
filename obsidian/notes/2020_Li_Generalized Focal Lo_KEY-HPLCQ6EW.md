# Generalized Focal Loss: Learning Qualified and Distributed Bounding Boxes for Dense Object Detection
> [!info]+ <center>Metadata</center>
> 
> |<div style="width: 5em">Key</div>|Value|
> |--:|:--|
> |文献类型|conferencePaper|
> |标题|Generalized Focal Loss: Learning Qualified and Distributed Bounding Boxes for Dense Object Detection|
> |短标题|GeneralizedFocalLoss|
> |作者|[[Xiang Li]]、 [[Wenhai Wang]]、 [[Lijun Wu]]、 [[Shuo Chen]]、 [[Xiaolin Hu]]、 [[Jun Li]]、 [[Jinhui Tang]]、 [[Jian Yang]]|
> |DOI|[](https://doi.org/)|
> |存档位置||
> |馆藏目录||
> |索书号||
> |版权||
> |分类|[[202207]]|
> |会议名称||
> |地点||
> |条目链接|[My Library](zotero://select/library/items/HPLCQ6EW)|
> |PDF 附件|[Full Text PDF](zotero://open-pdf/library/items/RYNIHFV8)|
> |关联文献|[[2022_Zhang_Dynamic Label Assign_KEY-QPWZ4MJ6]]、 [[2021_Li_Generalized Focal Lo_KEY-U3NPQRC2]]|
> ^Metadata


> [!example]- <center>本文标签</center>
> 
> `$=dv.current().file.tags`


> [!quote]- <center>Abstract</center>
> 
> One-stage detector basically formulates object detection as dense classification and localization (i.e., bounding box regression). The classification is usually optimized by Focal Loss and the box location is commonly learned under Dirac delta distribution. A recent trend for one-stage detectors is to introduce an \emph{individual} prediction branch to estimate the quality of localization, where the predicted quality facilitates the classification to improve detection performance. This paper delves into the \emph{representations} of the above three fundamental elements: quality estimation, classification and localization. Two problems are discovered in existing practices, including (1) the inconsistent usage of the quality estimation and classification between training and inference, and (2) the inflexible Dirac delta distribution for localization. To address the problems, we design new representations for these elements. Specifically, we merge the quality estimation into the class prediction vector to form a joint representation, and use a vector to represent arbitrary distribution of box locations. The improved representations eliminate the inconsistency risk and accurately depict the flexible distribution in real data, but contain \emph{continuous} labels, which is beyond the scope of Focal Loss. We then propose Generalized Focal Loss (GFL) that generalizes Focal Loss from its discrete form to the \emph{continuous} version for successful optimization. On COCO {\tt test-dev}, GFL achieves 45.0\% AP using ResNet-101 backbone, surpassing state-of-the-art SAPD (43.5\%) and ATSS (43.6\%) with higher or comparable inference speed.


> [!tldr]- <center>隐藏信息</center>
> 
> itemType:: conferencePaper
> title:: Generalized Focal Loss: Learning Qualified and Distributed Bounding Boxes for Dense Object Detection
> shortTitle:: GeneralizedFocalLoss
> creators:: [[Xiang Li]]、 [[Wenhai Wang]]、 [[Lijun Wu]]、 [[Shuo Chen]]、 [[Xiaolin Hu]]、 [[Jun Li]]、 [[Jinhui Tang]]、 [[Jian Yang]]
> proceedingsTitle:: Advances in Neural Information Processing Systems
> conferenceName:: 
> place:: 
> publisher:: Curran Associates, Inc.
> issue:: 
> pages:: 21002–21012
> language:: 
> DOI:: [](https://doi.org/)
> ISBN:: 
> url:: [https://proceedings.neurips.cc/paper/2020/hash/f0bda020d2470f2e74990a07a607ebd9-Abstract.html](https://proceedings.neurips.cc/paper/2020/hash/f0bda020d2470f2e74990a07a607ebd9-Abstract.html)
> archive:: 
> archiveLocation:: 
> libraryCatalog:: 
> callNumber:: 
> rights:: 
> extra:: 
> collection:: [[202207]]
> tags:: #_empahsis #unread 
> related:: [[2022_Zhang_Dynamic Label Assign_KEY-QPWZ4MJ6]]、 [[2021_Li_Generalized Focal Lo_KEY-U3NPQRC2]]
> itemLink:: [My Library](zotero://select/library/items/HPLCQ6EW)
> pdfLink:: [Full Text PDF](zotero://open-pdf/library/items/RYNIHFV8)
> qnkey:: 2020_Li_Generalized Focal Lo_KEY-HPLCQ6EW
> date:: 2020
> dateY:: 2020
> dateAdded:: 2022-07-17
> dateModified:: 2022-07-26
> year:: 2022
> dateCurrent:: 2022-07-27
> time:: 21:03:16
> week:: 星期三
> yearMonth:: 2022-07
> dateWeek:: 2022-07-27 星期三
> dateTime:: 2022-07-27 21:03:16
> dateWeekTime:: 2022-07-27 21:03:16 星期三
> 
> abstract:: One-stage detector basically formulates object detection as dense classification and localization (i.e., bounding box regression). The classification is usually optimized by Focal Loss and the box location is commonly learned under Dirac delta distribution. A recent trend for one-stage detectors is to introduce an \emph{individual} prediction branch to estimate the quality of localization, where the predicted quality facilitates the classification to improve detection performance. This paper delves into the \emph{representations} of the above three fundamental elements：quality estimation, classification and localization. Two problems are discovered in existing practices, including (1) the inconsistent usage of the quality estimation and classification between training and inference, and (2) the inflexible Dirac delta distribution for localization. To address the problems, we design new representations for these elements. Specifically, we merge the quality estimation into the class prediction vector to form a joint representation, and use a vector to represent arbitrary distribution of box locations. The improved representations eliminate the inconsistency risk and accurately depict the flexible distribution in real data, but contain \emph{continuous} labels, which is beyond the scope of Focal Loss. We then propose Generalized Focal Loss (GFL) that generalizes Focal Loss from its discrete form to the \emph{continuous} version for successful optimization. On COCO {\tt test-dev}, GFL achieves 45.0\% AP using ResNet-101 backbone, surpassing state-of-the-art SAPD (43.5\%) and ATSS (43.6\%) with higher or comparable inference speed.


👣➿👣


## ✏️ 笔记区

>[!inbox]- <center>📫 笔记简报</center>
>
> ⏰ importDate:: 2022-07-27

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