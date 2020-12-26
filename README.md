# **Eigen Face with python - jupyter**

first i make a dir for datasets. you can use your images. just replace your images with my images in **"Images"** folder.
then in **pre processing** section it automaticly convert in 50*50 gray scale image. you also can change size in this section if you hope have bigger or smaller images in your **Dataset** folder.

then you have choose your main image as a image that you want to have at the end. for example if you choose "12.jpeg", 13th image is your main image.

then we start the process:

  - vectorizing image
  - calculate PCA
  - find coefficients for next step
  - calculate the formula: orginalImage =  a1 * eigenFace1 + a2 * eigenFace2 + ... + ak * eigenFacek

## vectorizing image:
save images vector in reshaped version as rows in an array. this will help us in calculating **PCA** for Eigen Faces.

## calculate PCA:
with **openCV**'s PCA we must calculate the Eigen Faces. then I plot them to show 30 Eigen Faces.

## find coefficients for next step:
with dot producting Eigen Faces and Main Image we can calculate the coefficients and save them in an array.

## calculate the formula: orginalImage =  a1 * eigenFace1 + a2 * eigenFace2 + ... + ak * eigenFacek:
this is final step. we can make our main image based on other Eigen Faces. **you also can resive an input to now how many eigen faces do you want to use**. for example if you have 100 pictures and you choose 50 of them, then your final image is less similar to main image but if you use all of them it will most similar to main image

Libraries in use:

  - > numpy
  - > openCv (cv2)
  - > glob
  - > os
  - > matplotlib.pyploty
