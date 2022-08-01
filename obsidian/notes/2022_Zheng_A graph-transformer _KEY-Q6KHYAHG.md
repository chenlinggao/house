# A graph-transformer for whole slide image classification
> [!info]+ <center>Metadata</center>
> 
> |<div style="width: 5em">Key</div>|Value|
> |--:|:--|
> |文献类型|journalArticle|
> |标题|A graph-transformer for whole slide image classification|
> |短标题||
> |作者|[[Yi Zheng]]、 [[Rushin H. Gindra]]、 [[Emily J. Green]]、 [[Eric J. Burks]]、 [[Margrit Betke]]、 [[Jennifer E. Beane]]、 [[Vijaya B. Kolachalama]]|
> |期刊名称|[[IEEE Transactions on Medical Imaging]]|
> |DOI|[10.1109/TMI.2022.3176598](https://doi.org/10.1109/TMI.2022.3176598)|
> |存档位置||
> |馆藏目录|11.037 (Q1)|
> |索书号|1|
> |版权||
> |分类|[[00_Histology]]|
> |条目链接|[My Library](zotero://select/library/items/Q6KHYAHG)|
> |PDF 附件|[IEEE Xplore Full Text PDF](zotero://open-pdf/library/items/ETZQZCL2)|
> |关联文献||
> ^Metadata


> [!example]- <center>本文标签</center>
> 
> `$=dv.current().file.tags`


> [!quote]- <center>Abstract</center>
> 
> Deep learning is a powerful tool for whole slide image (WSI) analysis. Typically, when performing supervised deep learning, a WSI is divided into small patches, trained and the outcomes are aggregated to estimate disease grade. However, patch-based methods introduce label noise during training by assuming that each patch is independent with the same label as the WSI and neglect overall WSI-level information that is significant in disease grading. Here we present a Graph-Transformer (GT) that fuses a graph-based representation of an WSI and a vision transformer for processing pathology images, called GTP, to predict disease grade. We selected 4; 818 WSIs from the Clinical Proteomic Tumor Analysis Consortium (CPTAC), the National Lung Screening Trial (NLST), and The Cancer Genome Atlas (TCGA), and used GTP to distinguish adenocarcinoma (LUAD) and squamous cell carcinoma (LSCC) from adjacent non-cancerous tissue (normal). First, using NLST data, we developed a contrastive learning framework to generate a feature extractor. This allowed us to compute feature vectors of individual WSI patches, which were used to represent the nodes of the graph followed by construction of the GTP framework. Our model trained on the CPTAC data achieved consistently high performance on three-label classification (normal versus LUAD versus LSCC: mean accuracy= 91.2 ± 2.5%) based on five-fold cross-validation, and mean accuracy = 82.3 ± 1.0% on external test data (TCGA). We also introduced a graph-based saliency mapping technique, called GraphCAM, that can identify regions that are highly associated with the class label. Our findings demonstrate GTP as an interpretable and effective deep learning framework for WSI-level classification.


> [!tldr]- <center>隐藏信息</center>
> 
> itemType:: journalArticle
> title:: A graph-transformer for whole slide image classification
> shortTitle:: 
> creators:: [[Yi Zheng]]、 [[Rushin H. Gindra]]、 [[Emily J. Green]]、 [[Eric J. Burks]]、 [[Margrit Betke]]、 [[Jennifer E. Beane]]、 [[Vijaya B. Kolachalama]]
> publicationTitle:: [[IEEE Transactions on Medical Imaging]]
> journalAbbreviation:: IEEE T Med Imaging
> volume:: 
> issue:: 
> pages:: 1-1
> language:: 
> DOI:: [10.1109/TMI.2022.3176598](https://doi.org/10.1109/TMI.2022.3176598)
> ISSN:: 1558-254X
> url:: []()
> archive:: 2022-07-25
> archiveLocation:: 
> libraryCatalog:: 11.037 (Q1)
> callNumber:: 1
> rights:: 
> extra:: 🏷️ _empahsis、/Done、📒、Deep learning、Digital pathology、Feature extraction、Graph convolutional network、Lung、Lung cancer、Pathology、Training、Transformers、Tumors、Vision transformer
> collection:: [[00_Histology]]
> tags:: #_empahsis #Done #Deep_learning #Digital_pathology #Feature_extraction #Graph_convolutional_network #Lung #Lung_cancer #Pathology #Training #Transformers #Tumors #Vision_transformer
> related:: 
> itemLink:: [My Library](zotero://select/library/items/Q6KHYAHG)
> pdfLink:: [IEEE Xplore Full Text PDF](zotero://open-pdf/library/items/ETZQZCL2)
> qnkey:: 2022_Zheng_A graph-transformer _KEY-Q6KHYAHG
> date:: 2022
> dateY:: 2022
> dateAdded:: 2022-06-08
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
> abstract:: Deep learning is a powerful tool for whole slide image (WSI) analysis. Typically, when performing supervised deep learning, a WSI is divided into small patches, trained and the outcomes are aggregated to estimate disease grade. However, patch-based methods introduce label noise during training by assuming that each patch is independent with the same label as the WSI and neglect overall WSI-level information that is significant in disease grading. Here we present a Graph-Transformer (GT) that fuses a graph-based representation of an WSI and a vision transformer for processing pathology images, called GTP, to predict disease grade. We selected 4; 818 WSIs from the Clinical Proteomic Tumor Analysis Consortium (CPTAC), the National Lung Screening Trial (NLST), and The Cancer Genome Atlas (TCGA), and used GTP to distinguish adenocarcinoma (LUAD) and squamous cell carcinoma (LSCC) from adjacent non-cancerous tissue (normal). First, using NLST data, we developed a contrastive learning framework to generate a feature extractor. This allowed us to compute feature vectors of individual WSI patches, which were used to represent the nodes of the graph followed by construction of the GTP framework. Our model trained on the CPTAC data achieved consistently high performance on three-label classification (normal versus LUAD versus LSCC：mean accuracy= 91.2 ± 2.5%) based on five-fold cross-validation, and mean accuracy = 82.3 ± 1.0% on external test data (TCGA). We also introduced a graph-based saliency mapping technique, called GraphCAM, that can identify regions that are highly associated with the class label. Our findings demonstrate GTP as an interpretable and effective deep learning framework for WSI-level classification.


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

## 📝 注释笔记 ETZQZCL2

> <span style="font-size: 15px;color: gray">📍 2022-Zheng-A graph-transformer for whole slide image classification</span>

^KEYrefTitle

> <span class="highlight" style="background-color: #ffd40040">patch-based methods introduce label noise during training by assuming that each patch is independent with the same label as the WSI and neglect overall WSI-level information that is significant in disease grading.</span>  
> 觉得之前的算法噪声太大 ([p1](zotero://open-pdf/library/items/ETZQZCL2?page=1&annotation=A7SWIC4E))

^KEYA7SWIC4E

> <span class="highlight" style="background-color: #ff666640">4, 818 WSIs</span> ([p1](zotero://open-pdf/library/items/ETZQZCL2?page=1&annotation=3L5SMDIX))

^KEY3L5SMDIX

> <span class="highlight" style="background-color: #ff666640">a contrastive learning framework to generate a feature extractor</span> ([p1](zotero://open-pdf/library/items/ETZQZCL2?page=1&annotation=333FWIVG))

^KEY333FWIVG

> <span class="highlight" style="background-color: #ffd40040">An image patch must be connected to other patches and can be surrounded by at most 8 adjacent patches, so the sum of each row or column of A is at least one and at most 8.</span> ([p3](zotero://open-pdf/library/items/ETZQZCL2?page=3&annotation=CJHYYCHU))

^KEYCJHYYCHU

> <span class="highlight" style="background-color: #5fb23640">The expectation is that the derived feature vector provides an efficient representation of the node and also serves as a robust means by which to define a uniform representation of an image patch for graph-based classification.</span>  
> 表达挺好 ([p3](zotero://open-pdf/library/items/ETZQZCL2?page=3&annotation=R8VJW5RU))

^KEYR8VJW5RU

> <span class="highlight" style="background-color: #ffd40040">The pair of two augmented patches from the same patch is denoted as a positive pair. For a mini-batch of K patches, there are 2K augmented patches in total. Given a positive pair, the other 2K − 1 augmented patches are considered as negative samples.</span>  
> 定义正负样本对 ([p3](zotero://open-pdf/library/items/ETZQZCL2?page=3&annotation=PZ4H6EI9))

^KEYPZ4H6EI9

> <span class="highlight" style="background-color: #ffd40040">Note that N is variable since different WSIs contain different numbers of patches.</span>  
> 没有对数据进行零填充 ([p5](zotero://open-pdf/library/items/ETZQZCL2?page=5&annotation=RUFL8X6V))

^KEYRUFL8X6V

> <span class="highlight" style="background-color: #ffd40040">If patch i is a neighbor of patch j on the WSI (Fig. 1(B)), then GTP creates an edge between node i and node j as well as set Aij = 1 and Aji = 1, otherwise Aij = 0 and Aji = 0. GTP uses feature node matrix F and adjacent matrix A to construct a graph to represent each WSI.</span>  
> 定义图 ([p5](zotero://open-pdf/library/items/ETZQZCL2?page=5&annotation=HLGV4RUW))

^KEYHLGV4RUW

> <span class="image#ffd400">null</span> ([p5](zotero://open-pdf/library/items/ETZQZCL2?page=5&annotation=SRS6NQR9))

^KEYSRS6NQR9

> <span class="highlight" style="background-color: #ff666640">However, it is not trivial for a model to learn hierarchical features that are crucial for graph representation and classification.</span> ([p5](zotero://open-pdf/library/items/ETZQZCL2?page=5&annotation=S38JJS88))

^KEYS38JJS88

> <span class="highlight" style="background-color: #5fb23640">Briefly, the standard qkv self-attention [34] is a mechanism to find the words of importance for a given query word in a sentence, and it receives as input a 1D sequence of token embeddings.</span> ([p5](zotero://open-pdf/library/items/ETZQZCL2?page=5&annotation=8RDLMCRK))

^KEY8RDLMCRK

> <span class="highlight" style="background-color: #ffd40040">The attention weights Aij</span> ([p5](zotero://open-pdf/library/items/ETZQZCL2?page=5&annotation=DTK8RDL9))

^KEYDTK8RDL9

> <span class="highlight" style="background-color: #ffd40040">The goal of the transformer layer is to learn the mapping: H → T, where H is the graph space, and T is the transformer space.</span> ([p5](zotero://open-pdf/library/items/ETZQZCL2?page=5&annotation=YQAIKWFP))

^KEYYQAIKWFP

> <span class="highlight" style="background-color: #ffd40040">In order to learn the mapping T → Y</span> ([p5](zotero://open-pdf/library/items/ETZQZCL2?page=5&annotation=2I7CQ96Z))

^KEY2I7CQ96Z

> <span class="highlight" style="background-color: #ffd40040">This is because the number of patches that can be extracted can vary among different WSIs.</span>  
> 由于每个wsi的patch数量不同，导致位置编码的数量不同，所以不能讲位置编码直接应用在上面 ([p5](zotero://open-pdf/library/items/ETZQZCL2?page=5&annotation=U58GQY3T))

^KEYU58GQY3T

> <span class="highlight" style="background-color: #ffd40040">Rather, we used position embedding in the form of an adjacency matrix for the graph convolutional layers. The adjacency matrix of the WSI graph accounts for the spatial information and interconnectivity of the nodes, which is preserved when performing graph convolutions.</span> ([p5](zotero://open-pdf/library/items/ETZQZCL2?page=5&annotation=GNYZNRAW))

^KEYGNYZNRAW

> <span class="highlight" style="background-color: #ff666640">We therefore added a mincut pooling layer [38] between the GC and transformer layers that reduced the number of inputs from thousands to hundreds of nodes.</span>  
> 减少内存占用 ([p6](zotero://open-pdf/library/items/ETZQZCL2?page=6&annotation=4UQ3CQT2))

^KEY4UQ3CQT2

> <span class="highlight" style="background-color: #ffd40040">Min-cut pooling could preserve the local information of neighboring nodes and reduce the number of nodes at the same time.</span> ([p6](zotero://open-pdf/library/items/ETZQZCL2?page=6&annotation=J63MC7XC))

^KEYJ63MC7XC

> <span class="highlight" style="background-color: #ffd40040">the pooling layer learns to find min-cut clusters on any given graph and aggregates the clusters to reduce the graph size.</span>  
> 中间加了个min-cut聚类，以降维 ([p6](zotero://open-pdf/library/items/ETZQZCL2?page=6&annotation=9HWIZATN))

^KEY9HWIZATN

> <span class="highlight" style="background-color: #ffd40040">Our technique was inspired by the recent work by Chefer and colleagues [39], who used the deep Taylor decomposition principle to assign local relevance scores and propagated them through the layers by maintaining the total relevancy across layers.</span> ([p6](zotero://open-pdf/library/items/ETZQZCL2?page=6&annotation=ZPIRDJY4))

^KEYZPIRDJY4

> <span class="highlight" style="background-color: #ff666640">The GTP model was trained in batches of 8 examples for 150 iterations</span> ([p9](zotero://open-pdf/library/items/ETZQZCL2?page=9&annotation=8ADZUYUC))

^KEY8ADZUYUC

> <span class="highlight" style="background-color: #a28ae540">ning speed was about 2.4 iterations/s, and it took less than a day to reach convergence. The inference speed was &lt; 1 s per WSI with a batch size of 2.</span> ([p9](zotero://open-pdf/library/items/ETZQZCL2?page=9&annotation=92PRPDFP))

^KEY92PRPDFP







