FROM jupyter/datascience-notebook

ENV TRANSFORMERS_CACHE=/tmp/.cache
ENV TOKENIZERS_PARALLELISM=true

# Add RUN statements to install packages as the $NB_USER defined in the base images.

# Add a "USER root" statement followed by RUN statements to install system packages using apt-get,
# change file permissions, etc.

# If you do switch to root, always be sure to add a "USER $NB_USER" command at the end of the
# file to ensure the image runs as a unprivileged user by default.

USER root

RUN python3 -m pip install --no-cache-dir --upgrade pip && \
    python3 -m pip install --no-cache-dir \
    jupyter \
    tensorflow-cpu \
    torch \
    nltk \
    spacy \
    transformers \
    datasets

RUN python3 -m pip install --no-cache-dir \
    gensim \
    geopandas \
    ggplot \
    more-itertools \
    shapely \
    panel \
    holoviews \
    hvplot

RUN python3 -m pip install --no-cache-dir \
    chardet \
    cuda-python \
    pip install --pre "jupyterlab-git==0.50.0rc0"

# Install pexpect from GitHub
RUN python3 -m pip install --no-cache-dir git+https://github.com/pexpect/pexpect.git@master

# Install PygWalker
RUN python3 -m pip install --no-cache-dir pygwalker

# Configure PygWalker for offline use
RUN pygwalker config --set privacy=offline

USER ${NB_UID}

WORKDIR "${HOME}"
