# image-captioning

This repo implements Google's Show and Tell image captioning model using Tensorflow.

In order to run image_captioning.py, you will need VGG-16 image embeddings for the Flickr-30K dataset. These image embeddings are available [here](https://drive.google.com/file/d/0B5o40yxdA9PqTnJuWGVkcFlqcG8/view?usp=sharing).

You will also need the corresponding captions for these images, which can be downloaded from [here](https://drive.google.com/file/d/0B2vTU3h54lTydXFjSVM5T2t4WmM/view?usp=sharing).

You will also need to download a pretrained TensorFlow model for VGG-16 generated from the original Caffe model from the VGG-16 paper from [here](https://drive.google.com/file/d/0B2vTU3h54lTyaDczbFhsZFpsUGs/view?usp=sharing).

Place all of these downloads in the ./data/ directory.

For training a new image captioning model and then generating caption for an image, do:

	from image_captioning import generate_image_caption
	print generate_image_caption(image_path='image_path', train_model=True)

For generating caption for an image using pre-trained image captioning model, do:

	from image_captioning import generate_image_caption
	print generate_image_caption(image_path='image_path', train_model=False)

All pre-trained models should be put in the ./models/ directory.
