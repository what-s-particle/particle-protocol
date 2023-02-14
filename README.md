# What

This repository is used to build the `Particle framework`, and it defines using the [Protocol Buffers](https://protobuf.dev/).

# Why

The protocol definition will not be affected by the business and the coding language of the implementation.
So separate it into a repository, please note that this is a repository containing only `.proto` files, we do not provide scripts to generate corresponding languages.

BUT: Considering that the defined  `.proto` files can be quickly used by the caller(backend, web, mobile), we provide a script(`gennerate.py`) that will merge all `*.proto` into one file.
I'll come back to the reason for this, I did do some research and this is the best solution I can think of for quickly generating code for a variety of languages.

# How

The protocol files have a clear directory structure. If you observe it carefully, it will be easy to get started with adding and modifying protocol files.
As mentioned above, the end integrating this protocol needs to clone this repository to the latest, and refer to the provided script to generate the corresponding programming language file.

# Addition

Please note that if you use IDEA to open this project, you need to install the `protocol buffer` plug-in and configure some `source file path`s to ensure that the IDE can successfully recognize and support import jumps, which is very useful for you to modify this warehouse.
You can easily find the answer on the Internet, I won't repeat it.


