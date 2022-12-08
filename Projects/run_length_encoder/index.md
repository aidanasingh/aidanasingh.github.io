| [Homepage](https://aidanasingh.github.io) | [**Projects**](https://aidanasingh.github.io/Projects/) | [Music](https://aidanasingh.github.io/published_music/) | [Experience](https://aidanasingh.github.io/experience/) | 

# Run Length Encoder

[This program](https://github.com/aidanasingh/operating-systems-exercises/blob/main/run_length_encoder/multithreaded_encoder.c) compresses text files by encoding repeated characters as a character and its run length (e.g. aaaaaa -> a6). This program utilizes parallelization to make the encoding task faster, using the pthread c library. The use of mutexes is not necessary as there are no race conditions, though their current placement is necessary for the program to satisfy Valgrind Helgrind and Valgrind DRD thread error detection.

This program is a command line tool that takes arguments for any number of files to be encoded into one output file, and one argument for the number of threads following -j.