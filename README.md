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
```bash
g++ -o huffman main.cpp
