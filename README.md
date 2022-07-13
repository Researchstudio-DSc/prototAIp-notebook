# prototAIp-notebook

prototAIp-notebook is a community maintained 
[Jupyter Docker Stack](https://jupyter-docker-stacks.readthedocs.io/en/latest/) image. 
The image is preloaded with the most important libraries for data scientists. 
The collection of these libraries and the implementation of the stack image is part of the 
[prototAIp](https://www.netidee.at/prototaip) project.

## Installation with Docker Hub
- [Docker Hub repo](https://hub.docker.com/r/michaelbochrsa/prototaip-notebook)

Pull the docker image from Docker Hub and run a container with the following commands
```
docker pull michaelbochrsa/prototaip-notebook
docker run -p 10000:8888 michaelbochrsa/prototaip-notebook 
```

## Installation with GitHub

You can clone this repository and run it on you local machine. Just switch to the `/image`
folder to build and run the container. 
```
cd image/
docker build -t prototaip .
docker run -p 10000:8888 prototaip 
```
## Community Stack

Created with instructions found on 
[Community Stacks](https://jupyter-docker-stacks.readthedocs.io/en/latest/contributing/stacks.html)

Based on [jupyter/datascience-notebook](https://github.com/jupyter/docker-stacks/tree/master/datascience-notebook) 
and [ToluClassics/transformers_notebook](https://github.com/ToluClassics/transformers_notebook)

