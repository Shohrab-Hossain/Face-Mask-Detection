# Face Mask detection using CNN


<p align=center>
   <img src="readme-lib\Detection 03.png" alt="Logo" width="70%" style="min-width:150px;" />
</p>

</br>
</br>

The phrase **“novel coronavirus”** cites a `newly discovered`, `never-before-seen` coronavirus in humans. *Coronaviruses* are a sort of virus that can cause everything from the common cold to life-threatening diseases such as *Severe-Acute-Respiratory-Syndrome* and *Middle-East-Respiratory-Syndrome*. **COVID-19** is an `inhaling illness` that causes severe *pneumonia* in those who are infected. 

Wearing a **mask** is required in several nations during this *COVID-19 epidemic*, and it does cut *death rates*. Wearing a mask is essential inasmuch as the vaccination is not widely used and does not fully protect everyone. *Preventing the transmission* of infection is critical. Authorities require a method of monitoring public spaces such as subway stations and shopping malls. As a result, masked and unmasked `face recognition` is required. Using a combination of *video analysis*, *image classification*, *object tracking*, and *object identification*, a system like this can recognize persons wearing face masks in `photos` and `videos`. **Face mask recognition** may be done with a variety of *machine learning tools*. `Deep convolutional neural networks` have recently been successfully used to recognise face masks.

</br>
</br>

> Topics of this study are listed below:

1. [Face Detection](#face-detection)
2. [Face Mask Recognition](#face-mask-recognition)
3. [Introduction to Research Planning](#introduction-to-research-planning)
   - [Methodology](#methodology)
     - [Preprocessing](#preprocessing)
     - [Training](#training)
     - [Detection](#detection)
4. [Design of CNN](#design-of-cnn)
5. [Result Analysis](#result-analysis)
6. [Conclusion](#conclusion)



</br>
</br>
</br>

# Face Detection

In the field of computer vision, face perception is the most common study topic.It is a computer technology that predicts human faces in digital photos and is utilized in a range of applications. Face detection is one of the hottest topics in technology right now. The primary and preliminary stage in the study of face prediction is the localization of human faces. For instance, video surveillance in the home. Face localization is the process of extracting face features utilizing a pattern recognition algorithm. Face detection methods that are now available are as follows:

- Haar Cascade(`Haarcascade_frontalface_default.xml`)
- Local Binary Patterns Histograms(`createLBPHFaceRecognizer()`)
- Fisher Faces (`createFisherFaceRecognizer()`)
- Eigenfaces (`createEigenFaceRecognizer()`)




<p align=center>
   <img src="readme-lib\Haar.png" alt="Haar Cascade Features" width="40%" style="min-width:90px;" />
</p>


> Figure 01. Haar Cascade Features


</br>
</br>
</br>

# Face Mask Recognition

Nowadays, one of the most essential technologies is face mask detection. For this, a variety of machine learning tools can be used. For this type of Detection, `Deep Learning` is the ideal option. Following the detection of a face in an image or video, a deep learning network, such as a Convolutional Neural Network, can be employed for detection. When compared to other machine learning technologies, CNN has a few advantages in image processing.


<p align=center>
   <img src="readme-lib\Face Detection.jpg" alt="Face Detection" width="70%" style="min-width:110px;" />
</p>


> Figure 02. Face Mask Detection


</br>
</br>
</br>


# Introduction to Research Planning

This study confides in **Face Mask Detection** utilizing `Convolutional Neural Network`. In this review, a framework will be planned that will recognize facial covering. To prepare the model, a dataset of pictures will be gathered from an `online cloud repository`. The gathered raw dataset will be processed. The faces of people will be *cropped*, and from the `annotation XML` document, the labels for each cropped face will be stored in a data frame. Utilizing the *cropped pictures* and the *labels*, the **CNN model** will be *`trained`*. Subsequent to preparation the model will be utilized to distinguish facial covering. A sample picture will be imported from the `dataset`. The face of the people will be identified by utilizing a face classifier. Then, at that point, these faces will be utilized to anticipate facial covering by the trained CNN model. Contingent upon the expectation, the `class` will be anticipated: **with-mask**, **without-mask**, or **incorrectly-worn-mask**.


</br>
</br>


## Methodology

This study aims to design a CNN structure for Face Mask Detection. The methodology of this exploration is displayed in Figure 06. There are three stages in this exploration: Preprocess, Training, and Detection.




<p align=center>
   <img src="readme-lib\Methodology.png" alt="Methodology" width="85%" style="min-width:150px;" />
</p>
  

> Figure 03. Methodology


</br>
</br>
</br>


## Preprocessing

In **preprocessing stage**, the raw dataset will be processed first. There are pictures in this `dataset` and an `annotation XML` document with attributes of this large number of pictures. The `annotation` document will be analyzed, and the `coordinates` of the faces will be extracted. Utilizing these *coordinates*, the faces from each picture will be cropped and stored locally.




<p align=center>
   <img src="readme-lib\Preprocessing.png" alt="Preprocessing" width="90%" style="min-width:150px;" />
</p>


> Figure 04. Preprocessing Flow Chart




</br>
</br>
</br>


## Training

In the **training stage**, the `labels` are separated from the `annotation file`. The annotation document contains data of the labels of each face: *with-mask*, *without-mask*, *incorrectly-worn-cover*. After **label extraction**, a `data frame` will be created containing the *cropped faces* and the *label* for each face. A **CNN model** is designed then, at that point. With the *generated data frame*, the **CNN model** will be *trained* for `facial covering identification`.




<p align=center>
   <img src="readme-lib\Training.png" alt="Training" width="90%" style="min-width:150px;" />
</p>


> Figure 05. Training Flow Chart


</br>
</br>
</br>


## Detection

In the detection stage, a sample picture will be imported from the dataset. Then the faces in the picture will be distinguished by utilizing a face classifier. Haar Cascade Face Classifier will be utilized for this arrangement. Each recognized face of the picture will be utilized to anticipate by the prepared CNN model. In light of the forecast, the class will be identified for facial covering recognition.




<p align=center>
   <img src="readme-lib\Detection.png" alt="Detection" width="90%" style="min-width:150px;" />
</p>


> Figure 06. Detection Flow Chart


</br>
</br>
</br>


## Design of CNN

CNN, like other neural networks, has input and output layers. There are many hidden layers between these two tiers. There are a classification layer and some hidden layers for extracting features. Two Convolution Layers are followed by a Max Pooling Layer in the planned CNN model. Then there are two more Convolution layers and a Max pooling layer. Then there’s a Dense Layer and a Flatten Layer. The output class of the Dense Layer is three, which is the same as the number of labels in the dataset.




<p align=center>
   <img src="readme-lib\Design of CNN.png" alt="Design of CNN" width="95%" style="min-width:150px;" />
</p>


> Figure 07. Design of CNN



Details about each of these layers can be found [here](https://uk.mathworks.com/discovery/convolutional-neural-network-matlab.html).



</br>
</br>
</br>

# Result Analysis

The *training machine* contains `8.00 GB` of **RAM**, a `64-bit` **operating system**, and an `Intel(R) Core(TM) i7-4500U` **CPU** with speeds of `2.40 GHz` and `1.80 GHz`.


</br>


<p align=center>
   <img src="readme-lib\Result plot.png" alt="Result plot" width="70%" style="min-width:100px;" />
</p>


> Figure 08. Result of Training


</br>
</br>



When tested with test data, the trained model had an `accuracy` of **92.00 %**. The model’s performance is depicted in Figure 09.


<p align=center>
   <img src="readme-lib\Model Performance.png" alt="Model Performance" width="80%" style="min-width:120px;" />
</p>


> Figure 09. Model Performance

</br>
</br>

Some of the predicted images are shown below,


<p align=center>
   <img src="readme-lib\Detection 01.png" alt="Detection 01" width="40%" style="min-width:80px;" />
</p>

</br>

<p align=center>
   <img src="readme-lib\Detection 02.png" alt="Detection 02" width="25%" style="min-width:80px;" />
</p>
   
</br>

<p align=center>
   <img src="readme-lib\Detection 04.png" alt="Detection 04" width="40%" style="min-width:80px;" />
</p>


> Figure 10. Predicted Images

</br>
</br>
</br>


# Conclusion

**Face mask detection** is accomplished using a `CNN` in this study. `Python` was utilized to implement the model in the study. This study makes use of **NumPy**, **Pandas**, **OpenCV**, and **TensorFlow**. The CNN model is *trained* using cropped faces from training photos, and the trained model subsequently accurately predicted **single** and **multi-facial** *face masks*. When tested with `validation data`, the trained model had a **high prediction accuracy**.



</br>
</br>




---

</br>


# Important Links

1. Documentation of Convolution Neural Network :  [Link](https://uk.mathworks.com/discovery/convolutional-neural-network-matlab.html)
2. Cloud repository of Face Mask Dataset : [Link](https://www.kaggle.com/datasets/andrewmvd/face-mask-detection?select=images) 


</br>
</br>
</br>
