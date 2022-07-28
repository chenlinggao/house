# WSISA: Making Survival Prediction from Whole Slide Histopathological Images
> [!info]+ <center>Metadata</center>
> 
> |<div style="width: 5em">Key</div>|Value|
> |--:|:--|
> |文献类型|conferencePaper|
> |标题|WSISA: Making Survival Prediction from Whole Slide Histopathological Images|
> |短标题|WSISA|
> |作者|[[Xinliang Zhu]]、 [[Jiawen Yao]]、 [[Feiyun Zhu]]、 [[Junzhou Huang]]|
> |DOI|[10.1109/CVPR.2017.725](https://doi.org/10.1109/CVPR.2017.725)|
> |存档位置||
> |馆藏目录||
> |索书号||
> |版权||
> |分类|[[202204, 202206, 00_Histology]]|
> |会议名称|2017 IEEE Conference on Computer Vision and Pattern Recognition (CVPR)|
> |地点||
> |条目链接|[My Library](zotero://select/library/items/KD32LQW3)|
> |PDF 附件|[IEEE Xplore Full Text PDF](zotero://open-pdf/library/items/VH5HCI6M)|
> |关联文献||
> ^Metadata


> [!example]- <center>本文标签</center>
> 
> `$=dv.current().file.tags`


> [!quote]- <center>Abstract</center>
> 
> Image-based precision medicine techniques can be used to better treat cancer patients. However, the gigapixel resolution of Whole Slide Histopathological Images (WSIs) makes traditional survival models computationally impossible. These models usually adopt manually labeled discriminative patches from region of interests (ROIs) and are unable to directly learn discriminative patches from WSIs. We argue that only a small set of patches cannot fully represent the patients survival status due to the heterogeneity of tumor. Another challenge is that survival prediction usually comes with insufficient training patient samples. In this paper, we propose an effective Whole Slide Histopathological Images Survival Analysis framework (WSISA) to overcome above challenges. To exploit survival-discriminative patterns from WSIs, we first extract hundreds of patches from each WSI by adaptive sampling and then group these images into different clusters. Then we propose to train an aggregation model to make patient-level predictions based on cluster-level Deep Convolutional Survival (DeepConvSurv) prediction results. Different from existing state-of-the-arts image-based survival models which extract features using some patches from small regions of WSIs, the proposed framework can efficiently exploit and utilize all discriminative patterns in WSIs to predict patients survival status. To the best of our knowledge, this has not been shown before. We apply our method to the survival predictions of glioma and non-small-cell lung cancer using three datasets. Results demonstrate the proposed framework can significantly improve the prediction performance compared with the existing state-of-the-arts survival methods.


> [!tldr]- <center>隐藏信息</center>
> 
> itemType:: conferencePaper
> title:: WSISA: Making Survival Prediction from Whole Slide Histopathological Images
> shortTitle:: WSISA
> creators:: [[Xinliang Zhu]]、 [[Jiawen Yao]]、 [[Feiyun Zhu]]、 [[Junzhou Huang]]
> proceedingsTitle:: 2017 IEEE Conference on Computer Vision and Pattern Recognition (CVPR)
> conferenceName:: 2017 IEEE Conference on Computer Vision and Pattern Recognition (CVPR)
> place:: 
> publisher:: 
> issue:: 
> pages:: 6855-6863
> language:: 
> DOI:: [10.1109/CVPR.2017.725](https://doi.org/10.1109/CVPR.2017.725)
> ISBN:: 
> url:: []()
> archive:: 2022-07-25
> archiveLocation:: 
> libraryCatalog:: 
> callNumber:: 
> rights:: 
> extra:: 🏷️ _顶会、_read、/Done、Cancer、Computational modeling、Feature extraction、Lungs、Training、Tumors
> collection:: [[202204, 202206, 00_Histology]]
> tags:: #_顶会 #Done #Cancer #Computational_modeling #Feature_extraction #Lungs #Training #Tumors
> related:: 
> itemLink:: [My Library](zotero://select/library/items/KD32LQW3)
> pdfLink:: [IEEE Xplore Full Text PDF](zotero://open-pdf/library/items/VH5HCI6M)
> qnkey:: 2017_Zhu_WSISA：Making Surviva_KEY-KD32LQW3
> date:: 2017-07
> dateY:: 2017
> dateAdded:: 2022-04-19
> dateModified:: 2022-07-26
> year:: 2022
> dateCurrent:: 2022-07-27
> time:: 21:04:02
> week:: 星期三
> yearMonth:: 2022-07
> dateWeek:: 2022-07-27 星期三
> dateTime:: 2022-07-27 21:04:02
> dateWeekTime:: 2022-07-27 21:04:02 星期三
> 
> abstract:: Image-based precision medicine techniques can be used to better treat cancer patients. However, the gigapixel resolution of Whole Slide Histopathological Images (WSIs) makes traditional survival models computationally impossible. These models usually adopt manually labeled discriminative patches from region of interests (ROIs) and are unable to directly learn discriminative patches from WSIs. We argue that only a small set of patches cannot fully represent the patients survival status due to the heterogeneity of tumor. Another challenge is that survival prediction usually comes with insufficient training patient samples. In this paper, we propose an effective Whole Slide Histopathological Images Survival Analysis framework (WSISA) to overcome above challenges. To exploit survival-discriminative patterns from WSIs, we first extract hundreds of patches from each WSI by adaptive sampling and then group these images into different clusters. Then we propose to train an aggregation model to make patient-level predictions based on cluster-level Deep Convolutional Survival (DeepConvSurv) prediction results. Different from existing state-of-the-arts image-based survival models which extract features using some patches from small regions of WSIs, the proposed framework can efficiently exploit and utilize all discriminative patterns in WSIs to predict patients survival status. To the best of our knowledge, this has not been shown before. We apply our method to the survival predictions of glioma and non-small-cell lung cancer using three datasets. Results demonstrate the proposed framework can significantly improve the prediction performance compared with the existing state-of-the-arts survival methods.


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

## 📝 注释笔记 VH5HCI6M

> <span style="font-size: 15px;color: gray">📍 2017-Zhu-WSISA: Making Survival Prediction from Whole Slide Histopathological Images</span>

^KEYrefTitle

> <span class="highlight" style="background-color: #ff666640">we train separate deep convolutional survival model (DeepConvSurv) on each cluster.</span> ([p6858](zotero://open-pdf/library/items/VH5HCI6M?page=6858&annotation=ATK3MHBL))

^KEYATK3MHBL

> <span class="highlight" style="background-color: #ff666640">By randomly sampling and setting a large enough sampling ratio</span>  
> 关键 ([p6859](zotero://open-pdf/library/items/VH5HCI6M?page=6859&annotation=NFZXYF89))

^KEYNFZXYF89







