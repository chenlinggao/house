# Context Autoencoder for Self-Supervised Representation Learning
> [!info]+ <center>Metadata</center>
> 
> |<div style="width: 5em">Key</div>|Value|
> |--:|:--|
> |文献类型|preprint|
> |标题|Context Autoencoder for Self-Supervised Representation Learning|
> |短标题||
> |作者|[[Xiaokang Chen]]、 [[Mingyu Ding]]、 [[Xiaodi Wang]]、 [[Ying Xin]]、 [[Shentong Mo]]、 [[Yunhao Wang]]、 [[Shumin Han]]、 [[Ping Luo]]、 [[Gang Zeng]]、 [[Jingdong Wang]]|
> |期刊名称|[[]]|
> |DOI|[10.48550/arXiv.2202.03026](https://doi.org/10.48550/arXiv.2202.03026)|
> |存档位置||
> |馆藏目录||
> |索书号||
> |版权||
> |分类|[[00_Histology]]|
> |条目链接|[My Library](zotero://select/library/items/KJESY44U)|
> |PDF 附件|[arXiv Fulltext PDF](zotero://open-pdf/library/items/UK9GCBM9)|
> |关联文献|[[2021_He_Masked Autoencoders _KEY-MAC94JRI]]|
> ^Metadata


> [!example]- <center>本文标签</center>
> 
> `$=dv.current().file.tags`


> [!quote]- <center>Abstract</center>
> 
> We present a novel masked image modeling (MIM) approach, context autoencoder (CAE), for self-supervised representation pretraining. The goal is to pretrain an encoder by solving the pretext task: estimate the masked patches from the visible patches in an image. Our approach first feeds the visible patches into the encoder, extracting the representations. Then, we make predictions from visible patches to masked patches in the encoded representation space. We introduce an alignment constraint, encouraging that the representations for masked patches, predicted from the encoded representations of visible patches, are aligned with the masked patch presentations computed from the encoder. In other words, the predicted representations are expected to lie in the encoded representation space, which empirically shows the benefit to representation learning. Last, the predicted masked patch representations are mapped to the targets of the pretext task through a decoder. In comparison to previous MIM methods (e.g., BEiT) that couple the encoding and pretext task completion roles, our approach benefits the separation of the representation learning (encoding) role and the pretext task completion role, improving the representation learning capacity and accordingly helping more on downstream tasks. In addition, we present the explanations about why contrastive pretraining and supervised pretraining perform similarly and why MIM potentially performs better. We demonstrate the effectiveness of our CAE through superior transfer performance in downstream tasks: semantic segmentation, and object detection and instance segmentation.


> [!tldr]- <center>隐藏信息</center>
> 
> itemType:: preprint
> title:: Context Autoencoder for Self-Supervised Representation Learning
> shortTitle:: 
> creators:: [[Xiaokang Chen]]、 [[Mingyu Ding]]、 [[Xiaodi Wang]]、 [[Ying Xin]]、 [[Shentong Mo]]、 [[Yunhao Wang]]、 [[Shumin Han]]、 [[Ping Luo]]、 [[Gang Zeng]]、 [[Jingdong Wang]]
> publicationTitle:: [[]]
> journalAbbreviation:: 
> volume:: 
> issue:: 
> pages:: 
> language:: 
> DOI:: [10.48550/arXiv.2202.03026](https://doi.org/10.48550/arXiv.2202.03026)
> ISSN:: 
> url:: [http://arxiv.org/abs/2202.03026](http://arxiv.org/abs/2202.03026)
> archive:: 2022-07-25
> archiveLocation:: 
> libraryCatalog:: 
> callNumber:: 
> rights:: 
> extra:: 🏷️ _empahsis、_read、Computer Science - Computer Vision and Pattern Recognition
> collection:: [[00_Histology]]
> tags:: #_empahsis #Done #Computer_Science_-_Computer_Vision_and_Pattern_Recognition
> related:: [[2021_He_Masked Autoencoders _KEY-MAC94JRI]]
> itemLink:: [My Library](zotero://select/library/items/KJESY44U)
> pdfLink:: [arXiv Fulltext PDF](zotero://open-pdf/library/items/UK9GCBM9)
> qnkey:: 2022_Chen_Context Autoencoder _KEY-KJESY44U
> date:: 2022-05-30
> dateY:: 2022
> dateAdded:: 2022-07-03
> dateModified:: 2022-07-26
> year:: 2022
> dateCurrent:: 2022-08-01
> time:: 10:34:17
> week:: 星期一
> yearMonth:: 2022-08
> dateWeek:: 2022-08-01 星期一
> dateTime:: 2022-08-01 10:34:17
> dateWeekTime:: 2022-08-01 10:34:17 星期一
> 
> abstract:: We present a novel masked image modeling (MIM) approach, context autoencoder (CAE), for self-supervised representation pretraining. The goal is to pretrain an encoder by solving the pretext task：estimate the masked patches from the visible patches in an image. Our approach first feeds the visible patches into the encoder, extracting the representations. Then, we make predictions from visible patches to masked patches in the encoded representation space. We introduce an alignment constraint, encouraging that the representations for masked patches, predicted from the encoded representations of visible patches, are aligned with the masked patch presentations computed from the encoder. In other words, the predicted representations are expected to lie in the encoded representation space, which empirically shows the benefit to representation learning. Last, the predicted masked patch representations are mapped to the targets of the pretext task through a decoder. In comparison to previous MIM methods (e.g., BEiT) that couple the encoding and pretext task completion roles, our approach benefits the separation of the representation learning (encoding) role and the pretext task completion role, improving the representation learning capacity and accordingly helping more on downstream tasks. In addition, we present the explanations about why contrastive pretraining and supervised pretraining perform similarly and why MIM potentially performs better. We demonstrate the effectiveness of our CAE through superior transfer performance in downstream tasks：semantic segmentation, and object detection and instance segmentation.


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

## 📝 注释笔记 UK9GCBM9

> <span style="font-size: 15px;color: gray">📍 2022-Chen-Context Autoencoder for Self-Supervised Representation Learning</span>

^KEYrefTitle

> <span class="image#ffd400">null</span> ([p2](zotero://open-pdf/library/items/UK9GCBM9?page=2&annotation=BGJXVVB2))

^KEYBGJXVVB2

> <span class="highlight" style="background-color: #ffd40040">We form the latent contextual regressor H using a series of transformer blocks that are based on cross-attention.</span> ([p3](zotero://open-pdf/library/items/UK9GCBM9?page=3&annotation=Y62PEYMH))

^KEYY62PEYMH







