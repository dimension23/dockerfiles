# Docker for Data Science

### Release 0.1.0 - Minimal Comp Image

Demonstration of **how not to code interactively**
```
# Build
docker build -t gsl docker

# Compile
docker run -v source-dir:/home gsl gcc -I /usr/include -L /usr/lib/ -lgsl -lgslcblas /home/src/bessel.c -o /home/bin/bessel

# Run
docker run -v source-dir:/home gsl /home/bin/bessel
```

### Release 0.2.0 - Interactive Image

Demonstrates the use of jupyter/scipy-notebook image to run calculations using Python, both using python command and interactively with python notebook.
```
docker pull jupyter/scipy-notebook
docker run -v source-dir:/home/jovyan/work -p 8888:8888 jupyter/scipy-notebook
```

### Release 0.3.0 - Base Python image using Miniconda 3 on Debian

```
# Build
docker build -t miniconda3 miniconda3

# Run
docker run -it miniconda3 python
Python 3.7.3 (default, Mar 27 2019, 22:11:17)
[GCC 7.3.0] :: Anaconda, Inc. on linux
Type "help", "copyright", "credits" or "license" for more information.
```

### Release 0.4.0 - ipython Image

A layer on top of Miniconda 3
```
# Build
docker build -t ipython ipython

# Run
docker run -it ipython
```
