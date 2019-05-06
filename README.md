# Docker for Data Science

### Release 0.1.0 - Minimal Comp Image

Demonstration of **how not to code interactively**
```
# Build
docker build -t gsl docker

# Compile
docker run -v source:/home gsl gcc -I /usr/include -L /usr/lib/ -lgsl -lgslcblas /home/src/bessel.c -o /home/bin/bessel

# Run
docker run -v source-dir:/home gsl /home/bin/bessel
```

### Release 0.2.0 - Interactive Image

Demonstrates the use of jupyter/scipy-notebook image to run calculations using Python, both using python command and interactively with python notebook.
```
docker pull jupyter/scipy-notebook
docker run -v source-dir:/home/jovyan/work -p 8888:8888 jupyter/scipy-notebook
```
