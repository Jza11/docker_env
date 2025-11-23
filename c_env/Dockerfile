# Dockerfile to setup a stable environment for my C++ Development 
# Author: Jza11 (josemiguelcaceb@gmail.com)

FROM ubuntu:24.04

RUN apt update 

# Install g++ from build-essential
RUN apt install -y build-essential

# Install clang 
RUN apt install -y clang clang-tidy clang-format

# Install cpplint
RUN apt install -y cpplint

# Install Doxygen and graphviz for graphs
RUN apt install -y doxygen graphviz

# Install Cmake 
RUN apt install -y cmake cmake-gui

# Install Google Test Framework
RUN apt install -y libgtest-dev 

# Build Google Test Framework
RUN cd /usr/src/googletest && \
    cmake . && \
    make && \
    cp lib/*.a /usr/lib/ || \
    (mkdir -p build && cd build && cmake .. && make && cp lib/*.a /usr/lib/)

# Make image size smaller
RUN rm -rf /var/lib/apt/lists/*

# Set working directory 
WORKDIR /project/
