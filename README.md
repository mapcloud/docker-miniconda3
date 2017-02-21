# Modified from official docker image (forked by jobel-aqua)

[ContinuumIO docker-images miniconda3] (https://github.com/ContinuumIO/docker-images/tree/master/miniconda3)

**Current version**: Miniconda3-4.2.12-Linux-x86_64

# docker-anaconda

Docker container with a bootstrapped installation of [Anaconda](http://continuum.io/downloads) (based on Python 3.5) that is ready to use.

The Anaconda distribution is installed into the `/opt/conda` folder and ensures that the default user has the `conda` command in their path.

Anaconda is the leading open data science platform powered by Python. The open source version of Anaconda is a high performance distribution and includes over 100 of the most popular Python packages for data science. Additionally, it provides access to over 720 Python and R packages that can easily be installed using the conda dependency and environment manager, which is included in Anaconda.

Usage
-----

You can download and run this image using the following commands:

    docker pull continuumio/anaconda3
    docker run -i -t continuumio/anaconda3 /bin/bash

Alternatively, you can start a Jupyter Notebook server and interact with Anaconda via your browser:

    docker run -i -t -p 8888:8888 continuumio/anaconda3 /bin/bash -c "/opt/conda/bin/conda install jupyter -y --quiet && mkdir /opt/notebooks && /opt/conda/bin/jupyter notebook --notebook-dir=/opt/notebooks --ip='*' --port=8888 --no-browser"

You can then view the Jupyter Notebook by opening `http://localhost:8888` in your browser, or `http://<DOCKER-MACHINE-IP>:8888` if you are using a Docker Machine VM.
