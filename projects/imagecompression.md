---
layout: project
type: project
image: img/babyyoda.png
title: "PCA Image Compression"
date: 2024
published: true
labels:
  - Python
  - Data Science
  - Jupyter Notebook
summary: "A program which utilizes Principal Component Analysis in analyzing and converting an image into a compressed version of itself. This program was developed for my ICS 235 course."
---
<p align = "left">
This program gives a very shallow, visual example of how Principal Component Analysis works and how it can be used to compress an image into a smaller size. This program *should* work with different images as long as the code is changed to the location of the new photo. Python libraries numpy, PIL (Python Imaging Library), and pyplot are used alongside the scikit-learn machine learning library to produce the results. By combining these libraries the program could produce outputs such as this:
</p>
  <img class = "img-fluid" align = "right" width="400" src = "../img/explainedVariance.png">

<p>
This project allowed me to see the workflow of data science in terms of analyzing and retrieving data, and the steps taken to get to the goal which in this case, is to visualize and acquire useful data using PCA on image compression. Going step by step in Jupyter Notebook is similar yet different compared to coding, say a program to sort a list. Developing this felt more like analyzing data and computing something useful out of it compared to other projects I have done.
</p>

<br>

It took quite some time to learn and understand what exactly PCA is but through countless hours of studying and googling I could somewhat wrap my head around what its uses are. Besides learning how PCA works, I also learned how the python libraries worked as well by reading the documentation as well as outside research. It was a challenging objective to get to but seeing the final result made everything make sense just through one graphic visual of how different number of components used can change the image quality:

<p align = "center">
<img class = "img-fluid" width= "500" src = "../img/compressedgraphic.png">
</p>
    
<hr>

Source code: <a href="https://github.com/BryanNak/PCA-Image-Compression"><i class="large github icon "></i>BryanNak/PCA-Image-Compression</a>
