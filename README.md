# WikiArt-Visual-Recommendation
A Visual Similarity-based Recommendation System using Convolutional AutoEncoders and Embedded Space Cosine-Distance methods with the WikiArt Dataset

# Motivation
Write here

# Dataset

* Official Website: https://www.wikiart.org/

* Wiki Art Dataset Refined Download: (Size = 25.4Gb): https://drive.google.com/file/d/182-pFiKvXPB25DbTfAYjJ6gDE-ZCRXz0/view

In this project we used:
* Train Data: 35.000 images
* Validation Data: 15.000 images

# Project Overview
<p align="center">
<img src="https://user-images.githubusercontent.com/5551460/210288291-2bf85a51-9655-4dca-9f0d-ebcb94f13ebe.png" width=70% height=70%>
<img src="https://user-images.githubusercontent.com/5551460/210288850-43ab6335-60e8-468a-a1ac-7be2039bcd98.png" width=70% height=70%>
<img src="https://user-images.githubusercontent.com/5551460/210288946-53e394f4-1ac5-40f4-8266-412284f7ad51.png" width=70% height=70%>
</p>

# AutoEncoder

Is a type of artificial neural network used to learn efficient codings of unlabeled data (unsupervised learning).

<p align="center">
<img src="https://user-images.githubusercontent.com/5551460/210289180-77ba3b71-c556-4930-93b6-2b6b4cb00a29.png" width=70% height=70%>
</p>
<p align="center">
<em>Image obtained from The Keras Blog 2022</em>
</p> <br />

An autoencoder has two main parts: 
* Encoder: that maps the input into the code, 
* Decoder: that maps the code to a reconstruction of the input.

In our application, we use the same input train image as target image, so the model will learn how to reduce this image features (features extraction) and
reconstruct the same image using only those “small-dimension” features. (512 in our case).

# Model Performance and Evaluation

Evaluating the prediction and performance of this kind of application can be a bit ambiguous. We tried to focus on reducing the image reconstructed validation loss as much as possible while preserving the art style and similarity with the input image when predicting.

Our model reached a val_loss of 0.0029 at the end of the training.
When predicting a separated test set, we can see that the input image is almost perfectly reconstructed.

<p align="center">
<img src="https://user-images.githubusercontent.com/5551460/210289780-5ce9f1d5-9106-4085-b744-cbf159eeb137.png" width=70% height=70%>
</p>


