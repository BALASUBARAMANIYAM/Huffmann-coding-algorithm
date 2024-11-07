# Huffman Compression and Decompression

This project implements Huffman compression and decompression, a lossless data compression algorithm that uses variable-length codes for encoding characters. The algorithm creates a binary tree based on character frequencies in the input file, generating shorter codes for more frequent characters and longer codes for less frequent ones.

## Features

- **Compression**: Efficiently compresses files using Huffman encoding.
- **Decompression**: Accurately decompresses files that were compressed using the same Huffman algorithm.
- **Header Generation**: Includes metadata in the compressed file to facilitate tree reconstruction during decompression.
- **File Size Display**: Provides file size information before and after compression, allowing users to see the effectiveness of the compression.

## Project Structure

### Files

- **`main.cpp`**: The main driver file that handles file input, option parsing, and invokes the relevant functions for compression or decompression.
- **`Utility.cpp` / `Utility.h`**: Provides utility functions such as file size checking, input validation, and other helper functions.
- **`CompressUtility.cpp` / `CompressUtility.h`**: Contains functions specific to compression, including character frequency counting, Huffman tree generation, and storing Huffman values.
- **`DecompressUtility.cpp` / `DecompressUtility.h`**: Manages functions specific to decompression, including tree reconstruction from headers and decoding of compressed data.

## Usage

### Compile

To compile the program, use the following command:
g++ -o huffman main.cpp CompressUtility.cpp DecompressUtility.cpp Utility.cpp

## Run
Run the program with either compression (-c) or decompression (-dc) mode:
./huffman

The program will prompt you to enter the filename and the operation mode:

-c for compression
-dc for decompression

## Example
To Compress a File:
Enter the filename: sample.txt
Enter the mode (-c for compress, -dc for decompress): -c

This will create a compressed file named sample.txt.abiz.

To Decompress a File:

Enter the filename: sample.txt.abiz
Enter the mode (-c for compress, -dc for decompress): -dc

This will create an output file named output_sample.txt.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.


You can copy this content and create a new file on GitHub, such as `README.md`, to document your project. If you need further assistance with GitHub, feel free to ask!
