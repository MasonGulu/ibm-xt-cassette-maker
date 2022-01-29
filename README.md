# The C++ Version functions!

This project has been ported to C++. Inside the python directory is the python3 version, details are below.
This will convert binary and ascii files into a format that can be loaded over the IBM PC's cassette port.

Usage:
ibmwriter (bin, bas, raw) [input file] [output name] [segment] [offset]

* bin - write a binary file with a basic header to be loaded directly into RAM
* bas - write a txt BASIC file with a basic header to be loaded by BASIC and executed
* raw - write a binary file without a basic header, for use by advanced users

As far as I can tell the segment and offset are absolutely pointless. I tend to just set both to 0.

### Python version

This is a project written in python that will allow you to create wav audio files that can be loaded through cassette basic on the IBM 5150.

The only requirement should be python 3.

Usage:
asciiwrite.py [ascii file] [tape filename]

This takes in a text file with an ascii basic listing in it, and creates a file that can then be loaded using load.
Known issues:
None.

Usage:
binwrite.py [binary file] [tape filename] [segment] [offset]

This takes in a binary file and converts it to a memory dump file that can be loaded using bload.
Known issues:
* The segment and offset seem to do nothing, so I tend to just set them to 0 0.
* To return from ASM programs simply retf with the stack in the same state it was originally.
