The dataset is private hence can not be shared here. You can download the dataset from OASIS official website."https://www.oasis-brains.org"

The Report is Published in the STEM Fellowship Journal 2023 publication

<img width="664" alt="Screenshot 2023-12-13 at 4 24 32 AM" src="https://github.com/SinghJagpreet096/Alzheimer-s-Diagnostic/assets/104114729/c3a543bc-a2a0-421f-9c20-d2c4c3947d45">

<img width="664" alt="Screenshot 2023-12-13 at 4 25 25 AM" src="https://github.com/SinghJagpreet096/Alzheimer-s-Diagnostic/assets/104114729/1e148c1b-88d1-4d5e-ba32-4f3025ed23cc">



### Abstract
`Alzheimer` is a nervous system disease that affects memory and thinking abilities of humans. Doctors do not consider it to be curable but if detected at early stage its progression can be slowed.

`Open Access Series of Imaging Studies (OASIS)` brain data which can be used for Alzheimer's disease detection. It includes `MRI(Magnetic Resonance Imaging)` scans of the brain, which can help in detecting change of structural in brain of person diagnosed with Alzheimer's disease.

The aim of the project is to detect Alzheimer's disease at early stage using OASIS brain data set. This project involves using implementing `machine learning techniques` and exploring different algorithms and methods to accurately `detect the disease` through the given data. This model will detect change of structure is specific part of `brain and abnormalities` that leads to Alzheimer's disease. 

The results of the projects have a potential for the improvement in development of tools for diagnostics of the disease and further understand about the disease in details.


### Introduction
An estimated 40 million people, mostly older than 60 years, have `dementia` worldwide, and this figure is projected to double every 20 years, until at least 2050\cite{SCHELTENS2016505}. `Dementia of Alzheimer's Type (DAT)` is the most common form of dementia, affecting 1 in 9 people over the age of 65 years and as many as 1 in 3 people over the age of 85 \cite{popuri2020using}. Thus, its a major health concern among all the other modern health issues.

OASIS contains MRI scans of brain imaging with `neuroimaging and related clinical data` which is publicly available for research and analysis. It contains data to understand brain and helps in developing treatment approaches for various brain related diseases including Alzheimer's disease.

Currently, diagnostics of Alzheimer's disease diagnosis relies on a combination of `clinical evaluations, cognitive assessments, and neuroimaging` techniques. However, the accuracy and reliability of existing diagnostic methods can be limited, especially in the early stages of the disease.

Diagnostic the disease through machine learning models by utilizing the OASIS data set would be a better and much more effective way as the model will classify if the person's brain is normal or have `some patterns` that reflects presence of Alzheimer's disease.

### Materials & Methods
The data set consists of `MRI of 150 individuals` aged 60 to 96 years, all scanned in a similar environment. Everyone was scanned on two or more visits, separated by at least one year for 373 imaging sessions \cite{10.1162/jocn.2009.21407}. This data set contains brain images and demographic data of the person being scanned.

 

Implemented `Convolution Neural Network (CNN)` for image recognition and applied Transfer Learning on pre-trained `VGG16(Visual Geometry Group 16)` CNN model. VGG16 has 16 hidden layers and 14,714,688 parameters. The model has been trained on 1000 images of 1000 different categories with coloured images. The layers of the VGG16 model are freezed; so that the weights will not get updated in further training, the input layer is chopped off, and a new input layer is added for the current input data. After the pre-defined model(VGG16), the output is flattened and sent to a fully connected layer with 64 neurons with Leaky ReLU (alpha = 0.1) as the activation function. The final output layer consists of three neurons (One for each class) with softmax as the activation function.


### Results 
The data set has MRI images of `3-dimensional black-and-white images with shape (256, 256, 128)`. But, the pre-trained model used has been trained on images of `shape (224,224,3)`. Hence the data set was transformed into a shape in the format required for the model, and `specific frames (i.e., 75th, 100th and 125th)` were selected. The labels/target column (i.e., demented, non-demented and converted) were extracted from each `subject's Demographic (DM) data` for the respective images. These labels, along with the MRI images, were combined and used for training the model.  

### Discussion 

`Convolution Neural Network(CNN)` is a popular algorithm for `image recognition` because it can detect patterns and objects in the image. We specifically decided to move ahead with VGG16, a pre-trained CNN model, as we had limited data sources, which would not have been enough to train a CNN from scratch due to its complex structure. 

 

Further, it's very interesting to note that in the `OASIS2 brain dataset`, we have 72 subjects who identified as nondemented throughout the study, 64 subjects as demented in the initial visit and throughout the study, which also includes 51 subjects with mild to moderate Alzheimer's. The remaining 14 subjects were determined as non-demented in the initial visit and marked as demented in the later visits (converted). `These 14 subjects (converted) data is crucial for the problem statement, i.e., early detection, as their MRI samples tend to have patterns of the disease that looks like or develops in the early stages.`
#### Evaluation 

    The model tends to classify the images as `demented, non-demented and converted with an accuracy of 94 percent`. Still, accuracy alone cannot give us the whole picture as accuracy metrics only considers the correctly predicted(True Positive + True Negative) output with respect to total outputs. Hence, it can give a false perception in case of unbalanced data. 

     

    To overcome the limitation of accuracy score and as a requirement for the defined problem statement, we want to emphasize on reducing False Negative results, i.e. where a subject suffers from Alzheimer's, but the model detects otherwise. Therefore, the metrics we will focus on to evaluate the model are `Recall and F1 Score`. Recall, the fraction of the items of interest to the user retrieved by the system \cite{alvarez2002exact}. The harmonic mean of precision and recall, F1 score, is widely used to measure the success of a classifier when one class is rare \cite{lipton2014thresholding}. 

    `The Recall and F1 score for the given model is 95 percent and 92 percent, respectively. `  

 #### Limitation 

 The OASIS2 brain dataset consists of only 150 subjects and 373 MR sessions, all the subjects are aged between 60 and 96, and all the subjects are right-handed. We can see bias in the data as we do not have samples from young and left-handed subjects. 


Moreover, due to the data's complexity and large size(3d images), we could only train the model on limited subjects, as training the model on the whole data set would require greater computational power. 

#### Future Scope 
The future scope of the study would be to work with the latest `OASIS4 dataset`, which has more than `600 subjects and MR sessions`. But then, to process extensive data, we require robust systems that can process and transform the data. Further, we would like to collaborate with subject matter experts as they can assist us better in decision-making and understanding the problem. 

 ### Conclusions 

In conclusion, the `study focuses on Alzheimer's disease detection at an early stage using image recognition with CNN.` This study can be used in the development of robust diagnostics tools. Additionally, it can further improve Alzheimer's disease detection and highlights the potential of machine learning and neuroimaging techniques in the advanced understanding of structural change in the brain.  

### References
- Data were provided by OASIS [Longitudinal: Principal Investigators: D. Marcus, R, Buckner, J. Csernansky, J. Morris; P50 AG05681, P01 AG03991, P01 AG026276, R01 AG021910, P20 MH071616, U24 RR021382](https://doi.org/10.1162/jocn.2009.21407)
- Philip Scheltens, Ka j Blennow, Monique M B Breteler, Bart de Strooper, Giovanni B Frisoni, Stephen Salloway, and Wiesje Maria Van der Flier. Alzheimer’s disease. The Lancet, 388(10043):505–517, 2016.
- Karteek Popuri, Da Ma, Lei Wang, and Mirza Faisal Beg. Using machine learn- ing to quantify structural mri neurodegen- eration patterns of alzheimer’s disease into dementia score: Independent validation on 8,834 images from adni, aibl, oasis, and miriad databases. Human Brain Mapping, 41(14):4127–4147, 2020.
- Daniel S. Marcus, Anthony F. Fotenos, John G. Csernansky, John C. Morris, and Randy L. Buckner. Open Access Se- ries of Imaging Studies: Longitudinal MRI Data in Nondemented and Demented Older Adults. Journal of Cognitive Neuroscience, 22(12):2677–2684, 12 2010.
- Sergio A Alvarez. An exact analytical re- lation among recall, precision, and classi- fication accuracy in information retrieval. Boston College, Boston, Technical Report BCCS-02-01, pages 1–22, 2002.
- Zachary Chase Lipton, Charles Elkan, and Balakrishnan Narayanaswamy. Threshold- ing classifiers to maximize f1 score. arXiv preprint arXiv:1402.1892, 2014.

## Contributors

[Devender Kumar](https://www.linkedin.com/in/dev1ender/),
[Diljit Singh](https://github.com/Diljitsingh14/),
[Karman Singh Bains](https://github.com/bainskarman/)
