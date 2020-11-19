# Sketch-to-cartoon

This is a hackathon project for StudentHack VII which was built for under 12h.

It uses Conditional GAN (Pix2Pix) to generate cartoon characters from drawings:

![Preview](https://user-images.githubusercontent.com/19142553/99693708-55ec2d80-2a94-11eb-9d1a-5675e16b95bb.png)

The model was trained in Colab, converted to TensorflowJS and deployed in github pages: https://petartonchev.github.io/sketch-to-cartoon/webapp/

## Dataset
The dataset was created based on [Cartoonset Dataset](https://google.github.io/cartoonset/). To produce the sketch of the cartoon character we used Sobel edge detection. 

A major mistake was that we didn't noticed on time that the resulting edges were noisy, whereas, in the GUI the pencil draws solid lines. This majorly impacts the performance of the GAN. An easy solution to this problem might be to perform dilation in order to reduce the noisy edges.

## Ranking

With this project we won **3rd** place in the StudentHack VII hackathon.
