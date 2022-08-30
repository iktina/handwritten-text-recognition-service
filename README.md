# Handwritten Text Recognition

## Welcome

The service receives an image file of the line English handwritten text and uses it as input for a pre-trained model.

## What’s the point?

The service performs handwritten text recognition on images using machine learning techniques. The service retrieves the image file and outputs a text string as a result of image recognition.

## Model details:

The service receives an English-language image of a handwritten text line and uses it as input for a [TrOCR](https://github.com/microsoft/unilm/tree/master/trocr) model based on the Transformer architecture trained on the [IAM dataset](https://fki.tic.heia-fr.ch/databases/iam-handwriting-database), and outputs the result of image recognition as a text sequence. There are no limitations on the maximum size of the images, as they are scaled up to 384x384 pixels before the input.

## Important information

The service works only with images of handwritten text lines. If there are several lines of handwritten text in the input or if the text is printed, the service will not work correctly.

## How does it work?

The user must provide the following inputs in order to start the service and get a response:

Inputs:

 -   `endpoint`: -
 -   `method`: -
 -   `input_path`: Path to '\*.txt' file containing JSON representation of input argument 'file@data' and its value - path to '\*.[image format extension]' input image file.

Example of input file content:

```
{"file@data": "examples/ocr_image.jpg"}
```

## What to expect from this service?

Input image: examples/ocr_image.jpg
[![imageban](https://i2.imageban.ru/out/2022/08/30/ad7e6a890af86debd1ebc2480ba48cc6.jpg)](https://imageban.ru)

Response: text: "optical character recognition"