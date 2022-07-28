# Benchmarking weakly-supervised deep learning pipelines for whole slide classification in computational pathology
> [!info]+ <center>Metadata</center>
> 
> |<div style="width: 5em">Key</div>|Value|
> |--:|:--|
> |文献类型|journalArticle|
> |标题|Benchmarking weakly-supervised deep learning pipelines for whole slide classification in computational pathology|
> |短标题||
> |作者|[[Narmin Ghaffari Laleh]]、 [[Hannah Sophie Muti]]、 [[Chiara Maria Lavinia Loeffler]]、 [[Amelie Echle]]、 [[Oliver Lester Saldanha]]、 [[Faisal Mahmood]]、 [[Ming Y. Lu]]、 [[Christian Trautwein]]、 [[Rupert Langer]]、 [[Bastian Dislich]]、 [[Roman D. Buelow]]、 [[Heike Irmgard Grabsch]]、 [[Hermann Brenner]]、 [[Jenny Chang-Claude]]、 [[Elizabeth Alwers]]、 [[Titus J. Brinker]]、 [[Firas Khader]]、 [[Daniel Truhn]]、 [[Nadine T. Gaisa]]、 [[Peter Boor]]、 [[Michael Hoffmeister]]、 [[Volkmar Schulz]]、 [[Jakob Nikolas Kather]]|
> |期刊名称|[[Medical Image Analysis]]|
> |DOI|[10.1016/j.media.2022.102474](https://doi.org/10.1016/j.media.2022.102474)|
> |存档位置||
> |馆藏目录|13.828 (Q1)|
> |索书号|1|
> |版权||
> |分类|[[202205, 00_Histology]]|
> |条目链接|[My Library](zotero://select/library/items/5JU79F2I)|
> |PDF 附件|[Ghaffari Laleh 等。 - 2022 - Benchmarking weakly-supervised deep learning pipel.pdf](zotero://open-pdf/library/items/R3KNPDTY)|
> |关联文献||
> ^Metadata


> [!example]- <center>本文标签</center>
> 
> `$=dv.current().file.tags`


> [!quote]- <center>Abstract</center>
> 
> Artificial intelligence (AI) can extract visual information from histopathological slides and yield biological insight and clinical biomarkers. Whole slide images are cut into thousands of tiles and classification problems are often weakly-supervised: the ground truth is only known for the slide, not for every single tile. In classical weakly-supervised analysis pipelines, all tiles inherit the slide label while in multiple-instance learning (MIL), only bags of tiles inherit the label. However, it is still unclear how these widely used but markedly different approaches perform relative to each other. We implemented and systematically compared six methods in six clinically relevant end-to-end prediction tasks using data from N=2980 patients for training with rigorous external validation. We tested three classical weakly-supervised approaches with convolutional neural networks and vision transformers (ViT) and three MIL-based approaches with and without an additional attention module. Our results empirically demonstrate that histological tumor subtyping of renal cell carcinoma is an easy task in which all approaches achieve an area under the receiver operating curve (AUROC) of above 0.9. In contrast, we report significant performance differences for clinically relevant tasks of mutation prediction in colorectal, gastric, and bladder cancer. In these mutation prediction tasks, classical weakly-supervised workflows outperformed MIL-based weakly-supervised methods for mutation prediction, which is surprising given their simplicity. This shows that new end-to-end image analysis pipelines in computational pathology should be compared to classical weakly-supervised methods. Also, these findings motivate the development of new methods which combine the elegant assumptions of MIL with the empirically observed higher performance of classical weakly-supervised approaches. We make all source codes publicly available at https://github.com/KatherLab/HIA, allowing easy application of all methods to any similar task.


> [!tldr]- <center>隐藏信息</center>
> 
> itemType:: journalArticle
> title:: Benchmarking weakly-supervised deep learning pipelines for whole slide classification in computational pathology
> shortTitle:: 
> creators:: [[Narmin Ghaffari Laleh]]、 [[Hannah Sophie Muti]]、 [[Chiara Maria Lavinia Loeffler]]、 [[Amelie Echle]]、 [[Oliver Lester Saldanha]]、 [[Faisal Mahmood]]、 [[Ming Y. Lu]]、 [[Christian Trautwein]]、 [[Rupert Langer]]、 [[Bastian Dislich]]、 [[Roman D. Buelow]]、 [[Heike Irmgard Grabsch]]、 [[Hermann Brenner]]、 [[Jenny Chang-Claude]]、 [[Elizabeth Alwers]]、 [[Titus J. Brinker]]、 [[Firas Khader]]、 [[Daniel Truhn]]、 [[Nadine T. Gaisa]]、 [[Peter Boor]]、 [[Michael Hoffmeister]]、 [[Volkmar Schulz]]、 [[Jakob Nikolas Kather]]
> publicationTitle:: [[Medical Image Analysis]]
> journalAbbreviation:: Medical Image Analysis
> volume:: 79
> issue:: 
> pages:: 102474
> language:: en
> DOI:: [10.1016/j.media.2022.102474](https://doi.org/10.1016/j.media.2022.102474)
> ISSN:: 1361-8415
> url:: [https://www.sciencedirect.com/science/article/pii/S1361841522001219](https://www.sciencedirect.com/science/article/pii/S1361841522001219)
> archive:: 2022-07-25
> archiveLocation:: 
> libraryCatalog:: 13.828 (Q1)
> callNumber:: 1
> rights:: 
> extra:: 🏷️ _empahsis、_read、/Done、Artificial intelligence、Computational pathology、Convolutional neural networks、Multiple-Instance Learning、Vision transformers、Weakly-supervised deep learning
> collection:: [[202205, 00_Histology]]
> tags:: #_empahsis #Done #Artificial_intelligence #Computational_pathology #Convolutional_neural_networks #Multiple-Instance_Learning #Vision_transformers #Weakly-supervised_deep_learning
> related:: 
> itemLink:: [My Library](zotero://select/library/items/5JU79F2I)
> pdfLink:: [Ghaffari Laleh 等。 - 2022 - Benchmarking weakly-supervised deep learning pipel.pdf](zotero://open-pdf/library/items/R3KNPDTY)
> qnkey:: 2022_Ghaffari Laleh_Benchmarking weakly-_KEY-5JU79F2I
> date:: 2022-07-01
> dateY:: 2022
> dateAdded:: 2022-05-22
> dateModified:: 2022-07-26
> year:: 2022
> dateCurrent:: 2022-07-27
> time:: 21:04:00
> week:: 星期三
> yearMonth:: 2022-07
> dateWeek:: 2022-07-27 星期三
> dateTime:: 2022-07-27 21:04:00
> dateWeekTime:: 2022-07-27 21:04:00 星期三
> 
> abstract:: Artificial intelligence (AI) can extract visual information from histopathological slides and yield biological insight and clinical biomarkers. Whole slide images are cut into thousands of tiles and classification problems are often weakly-supervised：the ground truth is only known for the slide, not for every single tile. In classical weakly-supervised analysis pipelines, all tiles inherit the slide label while in multiple-instance learning (MIL), only bags of tiles inherit the label. However, it is still unclear how these widely used but markedly different approaches perform relative to each other. We implemented and systematically compared six methods in six clinically relevant end-to-end prediction tasks using data from N=2980 patients for training with rigorous external validation. We tested three classical weakly-supervised approaches with convolutional neural networks and vision transformers (ViT) and three MIL-based approaches with and without an additional attention module. Our results empirically demonstrate that histological tumor subtyping of renal cell carcinoma is an easy task in which all approaches achieve an area under the receiver operating curve (AUROC) of above 0.9. In contrast, we report significant performance differences for clinically relevant tasks of mutation prediction in colorectal, gastric, and bladder cancer. In these mutation prediction tasks, classical weakly-supervised workflows outperformed MIL-based weakly-supervised methods for mutation prediction, which is surprising given their simplicity. This shows that new end-to-end image analysis pipelines in computational pathology should be compared to classical weakly-supervised methods. Also, these findings motivate the development of new methods which combine the elegant assumptions of MIL with the empirically observed higher performance of classical weakly-supervised approaches. We make all source codes publicly available at https：//github.com/KatherLab/HIA, allowing easy application of all methods to any similar task.


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

## 📝 注释笔记 R3KNPDTY

> <span style="font-size: 15px;color: gray">📍 2022-Ghaffari Laleh-Benchmarking weakly-supervised deep learning pipelines for whole slide classification in computational pathology</span>

^KEYrefTitle

> <span class="highlight" style="background-color: #ff666640">To this end, we trained algorithms to predict each of these targets from raw histological whole slide images: (1) Diagnosis of renal cell carcinoma subtype (clear cell RCC, chromophobe RCC, and Papillary RCC); (2) prediction of microsatellite instability (MSI) or mismatch repair deficiency (dMMR) in colorectal cancer; (3) prediction of BRAF mutation in colorectal cancer; (4) prediction of MSI/dMMR in gastric cancer; (5) detection of Epstein-Barr Virus (EBV) presence in gastric cancer and (6) prediction of FGFR3 point mutations in bladder cancer. MSI and dMMR have a very high degree of overlap and are interchangeably used in clinical routines</span>  
> 我们训练算法从原始组织学全玻片图像中预测这些靶标中的每一个：（ 1 ）肾细胞癌亚型（透明细胞 RCC ，恐色 RCC 和状 RCC ）的诊断 ;（2）预测结直肠癌微卫星不稳定（MSI）或错配修复缺陷（dMMR）;（3）预测结直肠癌BRAF突变;（4）胃癌中MSI/dMMR的预测;（5）检测胃癌中EB病毒（EBV）的存在和（6）膀胱癌中FGFR3点突变的预测。MSI和dMMR具有非常高的重叠程度，并且可以在临床常规中互换使用 ([p4](zotero://open-pdf/library/items/R3KNPDTY?page=4&annotation=7Y8969IQ))

^KEY7Y8969IQ







