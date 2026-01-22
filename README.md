
# Huffman-Image-Compression

This project implements a simple Huffman encoding and decoding algorithm for compressing and decompressing BMP images using the Python Imaging Library (PIL). The program compresses the RGB channels of an image separately and then reconstructs the image from the compressed data.

## Prerequisites

- Python 3.x
- `Pillow` library

## Usage

1. Place your BMP image in a folder named `sample` in the same directory as the script.
2. Ensure the image is named `tiger.bmp`.

### Output

- The script prints the original size of the image (in pixels) and the encoded size (in bits).
- The compression ratio is also printed.
- The compressed image is saved as `Compressed_image.jpg`.

## Code Explanation

### Modules and Classes

- **Imports**:
  - `PIL.Image`: For image processing.
  - `heapq`: For priority queue implementation.
  - `collections.defaultdict`: For frequency table.

- **Node Class**: Represents a node in the Huffman tree.
  - `__init__`: Initializes the node with frequency, symbol, left child, and right child.
  - `__lt__`: Less than comparison for priority queue.

### Functions

- **build_huffman_tree(freq_table)**:
  - Builds the Huffman tree from the frequency table.
  - Returns the root of the Huffman tree.

- **generate_huffman_codes(root)**:
  - Generates Huffman codes from the Huffman tree.
  - Returns a dictionary of codes.

- **huffman_encoding(data)**:
  - Encodes the input data using Huffman coding.
  - Returns the Huffman codes and encoded data.

- **huffman_decoding(encoded_data, huffman_codes)**:
  - Decodes the encoded data using Huffman codes.
  - Returns the decoded data.

- **process_channel(channel)**:
  - Processes an image channel (R, G, or B).
  - Returns the decoded data and encoded data.

- **save_image_as_jpeg(image, filename)**:
  - Saves the image as a JPEG file with specified quality.

### Main Function

- Loads the BMP image.
- Splits the image into RGB channels.
- Processes each channel separately using Huffman encoding and decoding.
- Calculates and prints the original and encoded sizes, and the compression ratio.
- Merges the decoded channels back into an image.
- Saves the final decompressed image as `Compressed_image.jpg`.

## Notes

- Input image can be in any format like jpg/jpeg ,bmp ,png.
- Adjust the image path and name as needed.

## Author

Kanishka Dhanai
