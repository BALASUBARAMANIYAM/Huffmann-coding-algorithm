# Huffman Compression and Decompression

This project implements Huffman compression and decompression, a lossless data compression algorithm that uses variable-length codes for encoding characters. The algorithm creates a binary tree based on character frequencies in the input file, generating shorter codes for more frequent characters and longer codes for less frequent ones.

## Features

- **Compression**: Compresses files using Huffman encoding.
- **Decompression**: Decompresses files that were compressed using the same Huffman algorithm.
- **Header Generation**: Includes metadata for reconstruction during decompression.
- **File Size Display**: Provides file size information before and after compression.

## Files

- `main.cpp`: The main driver file to handle file input, option parsing, and calling relevant functions for compression or decompression.
- `Utility`: Provides utility functions like file size checking and code generation.
- `CompressUtility`: Handles functions specific to compression such as character frequency counting, tree generation, and storing Huffman values.
- `DecompressUtility`: Handles functions specific to decompression, including tree reconstruction from headers and decoding.

## Usage

### Compile
To compile the program:
bash
g++ -o huffman main.cpp
Run
Run the program with either compression (-c) or decompression (-dc) mode:

bash
Copy code
./huffman
The program will prompt you to enter the filename and the operation mode:

-c for compression
-dc for decompression
Example
plaintext
Copy code
Enter the filename: example.txt
Enter the mode (-c for compress, -dc for decompress): -c
How It Works
Compression:

Reads the file to determine character frequencies.
Builds a Huffman tree based on character counts.
Encodes each character based on its position in the tree.
Writes a header with metadata for decompression.
Outputs a compressed file with the .abiz extension.
Decompression:

Reads the file header to rebuild the Huffman tree.
Decodes the binary data back into characters.
Outputs a decompressed file with the output prefix.
Example
To compress a file:

plaintext
Copy code
./huffman
Enter the filename: sample.txt
Enter the mode (-c for compress, -dc for decompress): -c
This will create a compressed file named sample.txt.abiz.

To decompress:

plaintext
Copy code
./huffman
Enter the filename: sample.txt.abiz
Enter the mode (-c for compress, -dc for decompress): -dc
This will create an output file named outputsample.txt.

Performance
The program provides feedback during compression and decompression, including progress and time taken.

License
