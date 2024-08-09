# Image Steganography

This project is a Python-based implementation of image steganography, allowing you to hide text data within an image file. The goal is to encode secret messages into images in such a way that the alterations are imperceptible to human vision.

## Features

- **Data Embedding**: Embed text data within image files without significantly altering the image.
- **Data Extraction**: Extract the hidden text data from a steganographed image.
- **Robustness**: The hidden data is resistant to minor image processing operations.
- **Support for Various Image Formats**: Works with common image formats such as PNG, JPEG, and BMP.

## Installation

To use this project, clone the repository and install the necessary dependencies:

```bash
git clone https://github.com/yourusername/image-steganography.git
cd image-steganography
pip install -r requirements.txt
```

## Usage

### Embedding Data

To embed text data into an image, use the following command:

```bash
python steganography.py --embed --input <input_image> --output <output_image> --message <text_message>
```

### Extracting Data

To extract the hidden text data from an image, use:

```bash
python steganography.py --extract --input <steganographed_image>
```

### Parameters

- `--input`: The input image file.
- `--output`: The output image file where the hidden data will be embedded (used with the `--embed` option).
- `--message`: The text message to embed in the image (used with the `--embed` option).
- `--extract`: Flag to extract the hidden message from a steganographed image.
- `--embed`: Flag to embed a message into the image.

## Examples

### Embedding Example

```bash
python steganography.py --embed --input example.png --output stego.png --message "Secret Message"
```

### Extraction Example

```bash
python steganography.py --extract --input stego.png
```

## Dependencies

- Python 3.x
- PIL (Pillow)
- Numpy

Install the dependencies using:

```bash
pip install pillow numpy
```

## How It Works

Image steganography works by modifying the least significant bits (LSB) of the pixel values in the image. The LSB modification is subtle enough that it does not significantly change the appearance of the image, making the hidden data virtually invisible to the naked eye.

### Limitations

- The size of the message that can be embedded is limited by the size and format of the image.
- The process is sensitive to image modifications such as resizing, cropping, or reformatting, which can destroy the hidden data.


## Contributing

Contributions are welcome! Please fork this repository and submit a pull request with your changes.

## Acknowledgements

- This project was inspired by the need for secure communication in a digital world.
- Thanks to all the contributors who have made this project possible.

---
