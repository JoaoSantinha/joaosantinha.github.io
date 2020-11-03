---
title: "ESOR Radiomics Workshop"
collection: workshops
excerpt: 'ESOR Radiomics Workshop.'
date: 2020-08-01
venue: 'ESOR'
---

# ESOR Radiomics Workshop

## Overview of the workshop
Duration: 0:05

This workshop will teach you how to develop radiomics models. In this workshop we will use the PROSTATEx dataset (Joint 
SPIE-AAPM-NCI challenge - 2017 SPIE Medical Imaging Symposium) to learn how to perform all the different steps 
constituting the development of radiomics a model:

* Segmentation of Region-of-Interest 
* Image Pre-pocessing
* Radiomics Feature Extraction
* Deep Features Extraction
* Radiomics+Deep Features Model Development
* Development of automatic segmentation model (bonus)

Prerequisites:

* Google account (either personal or institutional)

## Segmentation of Region-of-Interest
Duration: 0:10

Segmentation of regions-of-interest can be done using several tools (e.g., 
<a href="https://www.slicer.org" target="_blank">3D Slicer</a>, 
<a href="https://www.mitk.org/wiki/The_Medical_Imaging_Interaction_Toolkit_(MITK)" target="_blank">MITK</a>, 
<a href="http://www.itksnap.org/pmwiki/pmwiki.php" target="_blank">ITK-SNAP</a>, 
<a href="https://www.osirix-viewer.com" target="_blank">OsiriX</a>, 
<a href="https://horosproject.org" target="_blank">Horos</a>, etc.). In this 
workshop we will use 
<a href="http://htmlsegmentation.s3.eu-north-1.amazonaws.com/index.html" target="_blank">MedSeg</a>, which is a 
web-based solution that does not require you to install any application and works in your browser.

Although prostate MRI is multi-parametric, for simplicity we will use only T2-weighted images. We will perform the 
segmentation of the index lesion in this following examination that you should download to your computer.

Download T2-weighted Prostate Image [add link to image]

and we open MedSeg on your browser

<a href="http://htmlsegmentation.s3.eu-north-1.amazonaws.com/index.html" target="_blank">Open MedSeg</a>

will drag the file you just downloaded (T2w_prostate_example.nii.gz) file to the MedSeg. And lets segment the index 
lesion and save the resulting segmentation file.

These files can either be used to extract radiomics features, as we will see later, or to train deep learning models to 
perform the segmentation automatically.

## Image Pre-processing
Duration: 0:10

A very important part of the whole radiomics model development is the pre-processing of the images to be analyzed. 
Several artifacts (motion, noise, MRI bias field inhomogeneities) may affect images.

We will teach you a way to denoise and correct bias field inhomogeneities.

Lets open the following colab notebook and create your own copy of the notebook that you can run.

Open Image Pre-processing Colab Notebook [add link]

## Radiomics Feature Extraction
Duration: 0:10

Radiomic features are mathematical descriptors of image intensities and texture initially defined for computer vision 
tasks. In the radiological context, the features are not extracted from the whole image but from the region-of-interest,
 which could be an organ, part of an organ or a lesion. For this reason, to extract radiomic features we are required to
 provide pairs of images-masks. 

Depending on the image modality and image acquisition characteristics, several options on the feature extraction may 
vary.

We will make use of PyRadiomics to extract the radiomic features.

So lets open the following colab notebook, create your copy and start running it.

Open Radiomics Feature Extraction Colab Notebook [add link]

## Deep Features Extraction
Duration: 0:10

Another way to extract features is to use pre-trained convolutional neural networks (CNN) for visual object recognition 
trained on over 14 million of images comprising 20000 categories (e.g., cat, dog, car, airplane, etc.). The features are
 obtained from the CNN chosen layer. This approach is part of the transfer learning concept.
 
In this example we will use the a pre-trained [add name of chosen CNN] architecture.

So lets open the following colab notebook, create your copy and start running it.

Open Deep Feature Extraction Colab Notebook [add link]

## Radiomics+Deep Features Model Development
Duration: 0:10

After constructing a dataset which you will use to train/evaluate your model

## Development of automatic segmentation model*
Duration: 0:10

After constructing a dataset which you will use to train/evaluate your model