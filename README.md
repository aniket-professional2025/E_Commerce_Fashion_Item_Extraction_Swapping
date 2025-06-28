# E_Commerce_Fashion_Item_Extraction_Swapping
This project is my third project in my journey. This projects contains two sub-projects. One is extraction of saree from a given image and the second part is building a robust VTON model with out own saree images without training a complete model.

## Contents:
This repository contains the ipynb files to extract the images (Saree, Bags, Watch, Jewellery, Specs). The images are read via image urls using the request library in python. Since, the dataset (in Json format) is confidential, so it can not be provided. 

## Process:
The process of each file is:
- Use GroundedSAM to detect and then segment our required objects (like saree, bags, watch, jewellery, specs etc)
- Once the object is segmented out, we use its binary mask and use bitwise operation (cv2) to get the original image
- Since, we want the images in a transparent background, we use either the remove function (from rembg) or the mask itself to do that.
- Oneb can try different approaches to remove the background

## Limitations:
Currently, the code that is given in this repository, extracts good quality images only for dark edge images. For example, if a spectacle frame is of a color close to white, then it will extract the frame but it also will make the frame transparent to some extent.
