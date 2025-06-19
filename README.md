# Quality-Accuracy Tradeoff Data
This repository contains data from experiments conducted as a part of my master thesis project on machine-oriented image compression, along with data from additional experiments conducted after submission in preparation for examination.

Using the MobileNetV2 DNN architecture through PyTorch and the [ImageNet Validation set](https://www.kaggle.com/datasets/titericz/imagenet1k-val), experiments pertaining to the relationship between JPEG's quality factor (QF) values and resulting prediction accuracy were conducted and the data recorded to .txt files. Two different batch-sizes were used, 1 and 50, with the former giving image-level data and the latter class-level data thanks to the sequential nature of the dataset and absence of data shuffling. Experiments were conducted on QF values between 70 and 98.

Directory names in this repository denote the batchsize used for its data, while filenames inside the directories denote the QF value used for the experiment. Directories with a **'_jpeg'** suffix contain data from supplementary experiments using the standard JPEG compression, while directories with no suffix contain data from the original experiments which use *pruning-enhanced* JPEG compression. 

The data fields recorded were batch ID, average batch prediction accuracy (which is either 0 or 1 for batchsize 1), and average batch bitrate (in bits per pixels or BPP). **The files contain no headers or index columns**, with the structure being the following:

|Batch ID| Avg. Acc.| Avg. BPP|
|---|---|---|

So files using batch size 50 will look similar to:

|| | |
|---|---|---|
|0|0.92|1.96...|
|1|0.86|1.29...|
|...|...|...|

while files using batch size 1 will look similar to:

|| | |
|---|---|---|
|0|0.0|1.62...|
|1|1.0|1.74...|
|2|0.0|2.61...|
|...|...|...|


## Change Log
|Date|Changes|
|---|---|
|**01/06/2025**|Data from pruning experiments uploaded|
|**19/06/2025**|Data from additional baseline JPEG experiments uploaded|
