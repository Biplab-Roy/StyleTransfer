Development of an Adaptable Deep Learning Model for Artistic Style Transfer
===================

- - - - 

I'm excited to discuss the Neural Style Transfer system that I've developed. This project involves using deep learning techniques to merge the content of one image with the artistic style of another, producing visually appealing stylized images.

Neural Network Architecture: I chose to base my NST system on the VGG-19 pre-trained convolutional neural network. VGG-19 is known for its good balance between model complexity and performance in image-related tasks.

Selected Layers: To extract meaningful features for content and style, I identified specific layers from the VGG-19 model. These layers include `conv1_1`, `conv2_1`, `conv3_1`, `conv4_1`, `conv4_2`, and `conv5_1`. These layers capture both low-level and high-level features necessary for effective style transfer.

Loss Function: The core of the system involves defining a loss function that combines content and style losses. The content loss measures the difference between the content features of the content image and the generated image. Simultaneously, the style loss quantifies the difference in style features between the style image and the generated image. This loss function guides the optimization process. We have used `content_wt = 100`` and `style_wt = 1e8`

Training Process: During training, the system iteratively adjusts the pixels of the generated image to minimize both content and style differences. The goal is to create a stylized image that retains the content of the input image while incorporating the artistic style of another. For the particular example we have used `epochs = 500` and `learning_rate = 0.007`

Successful Implementation: I'm pleased to report that the NST system is currently working well, producing satisfactory stylized images. It's a testament to the effectiveness of the chosen neural network architecture and the careful selection of layers for feature extraction.

Potential improvements: While the current system is performing admirably, there's always room for improvement. I've considered fine-tuning hyperparameters, exploring different neural network architectures like ResNet or Inception, experimenting with regularization techniques, and optimizing aspects such as memory usage and speed.

## Dependecies
---
```
torch=2.1.1
torchvision=0.16.1
numpy=0.16.1
pillow>=5.3.0
tqdm=4.65.0
```

## Run The Notebook
---
The content.jpg and style.jpg can be replaced with own files. Jupyter notebook can run in a environment satifying the dependencies with python >= 3.10