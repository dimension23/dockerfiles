# Docker for Data Science

### Release 0.1.0 - Minimal Comp Image

Demonstration of **how not to code interactively**
```
# Build
docker build -t gsl docker

# Compile


# Run
docker run -v source-dir:/home gsl /home/bin/bessel
```

### Release 0.2.0 - Interactive Image

Added bessel.py to run using jupyter/scipy-notebook both manually and interactively using python notebook
```
docker pull jupyter/scipy-notebook
docker run -v source-dir:/home/jovyan/work -p 8888:8888 jupyter/scipy-notebook
```
