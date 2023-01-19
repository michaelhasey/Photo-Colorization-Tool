# READ ME FILE

## Assignment #1 - Colorizing the Projudin-Gorskii Photo Collection

Class: 16-726 Learning-Based Image Synthesis
Instructor: Jun-Yan Zhu
Term: Spring 2021

Name: Michael Hasey
Andrew ID: mhasey


## Description

This study proposes a computational method to autonomously colorize the Prokudin-Gorskii Photo Collection, which is a series of black and white photographs of the Russian Empire taken by Sergei Mikhailovich Prokudin-Goirskii in the early 20th century.  In addition to being grayscale, each photograph is in fact a montage of three copies of the same image stacked one above the other.  Each copy within the montage represents one of the three channels of the RGB color spectrum.  The images are stacked with the blue channel image on top,  the green channel image in the middle, and the red channel on the bottom.  

The aim of this study is to use image processing techniques to autonomously and efficiently split the image into its three parts, align the images using numpy.roll() function and a normalized cross-correlation image similarity scoring, stack them correctly to produce a color image, and apply recursive coding methodologies and techniques such as image pyramiding to complete this task in a very short period of time when applied to very large images.


## Websites

1. Personal website

    - www.michaelhasey.com/prokudin-gorskii-colorization-algorithm

2. Andrew File System (AFS)

    - www.andrew.cmu.edu/course/16-726/projects/mhasey/proj1/


## Folder Structure: 

folder name: mhasey_code_proj1

- Data (folder)
    - plates_original_size (folder)
        - village.tif (image - 75 MB)
    - plates_reduced_size (folder)
        - village.tif (image - 4.5 MB)
- output (folder)
    - output_village_single_scale.jpg (image - 99 kb)
    - output_village_multi_scale.jpg (image - 983 kb)
- main_single_scale.ipynb (Jupyter notebook code for running single scale colorization)
- main_multi_scale.ipynb (Jupyter notebook code for running multi-scale colorization)
- website_record.pdf (pdf record of personal website)


## Data

- Two original Prokudin-Gorskii photos

    - reduced size image "village.tiff", 4.5 MB
    - original size image "village.tiff", 75 MB

- Two colorized Prokudin-Gorskii photos

    - output_village_single_scale.jpg, 99 kb
    - output_village_multi_scale.jpg, 983 kb


## Code (Jupyter Notebooks)

1. main_single_scale.ipynb

    - Algorithm for single scale image alignment & colorization
    - Normalized Cross-Correlation (NCC) for alignment scoring
    - numpy
        - np.roll for exhaustive search over window of possible displacements
    - matplot lib
    - cv2
    - skimage

2. main_multi_scale.ipynb

    - Algorithm for multi scale image alignment & colorization
    - Uses image pyramid to reduce run time on larger, full-size images
    - Normalized Cross-Correlation (NCC) for alignment scoring
    - numpy
        - np.roll for exhaustive search over window of possible displacements
    - matplot lib
    - cv2
    - skimage