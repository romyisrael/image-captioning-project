# image-captioning-project
📘 Project Questions & Answers
1. How can we connect the two domains: image and text?

Image captioning combines vision and language by using:

A CNN image encoder (e.g., ResNet50) to convert an image into a numerical feature vector.

An RNN text decoder (LSTM) that takes the image feature vector and generates a caption word-by-word.

The CNN understands the picture.
The LSTM uses this information to write the sentence.

2. Which pretrained model will we use to understand images?

We use ResNet50, a pretrained convolutional neural network trained on ImageNet.
It extracts high-level visual features from the image and outputs a 2048-dimensional feature vector.

3. How does the input enter the model?

Although the input is a file (e.g., .jpg), deep learning models require tensors.
We must:

Load the image from disk

Resize and normalize it

Convert it to a tensor

Pass it through the CNN encoder

The CNN outputs a feature vector that represents the image.

4. What is the output of the initial CNN model?

The output is a feature embedding — for ResNet50, typically a vector of size 2048.
This vector summarizes the visual content and is fed into the LSTM decoder.

5. Running initial examples

To test the pipeline, we:

Load an image in Google Colab

Preprocess it

Feed it into the CNN

Print the shape of the output feature vector

This confirms our preprocessing and encoder work correctly before training the full model.

6. Which dataset will we use?

We use Flickr8k, containing:

8,000 images

5 captions per image

It is small enough to train on Google Colab and ideal for student projects.

7. What text-generation architectures are possible?

Several options exist:

LSTM (classic, used in Show & Tell)

GRU

Transformer decoder

Pretrained models (BLIP, ViT-GPT2)

Given our compute limitations, we choose LSTM for our decoder.

8. Why choose LSTM?

Because:

It is lightweight and trainable on Google Colab

Works well with small datasets such as Flickr8k

Matches the architecture used in Vinyals et al. (2015)

Easy to implement and understand

☑️ Final Result

Once you paste this in, your README will contain:

All questions the instructor asked

All correct explanations

Everything formatted neatly

This is exactly what your instructor wants to see.
