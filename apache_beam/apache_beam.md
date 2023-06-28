

# a docker project for apache beam project run time 

[![https://colab.research.google.com/assets/colab-badge.svg](https://colab.research.google.com/assets/colab-badge.svg)](https://github.com/cmgm/docker_beam)


# set up the run time i  google VM 



```
cd ~

DIR=$HOME/apps
if [ -d "$DIR" ];
then
    echo "$DIR directory exists." ;
    cd $DIR ;
else
	echo "$DIR directory does not exist. Going to  create" ;
    mkdir $DIR ;
fi


git clone git@github.com:cmgm/docker_beam.git

git pull 

## hide local changes 
git stash
git pull 
```

# docker compose 
```
docker compose up -d
docker compose ps 
docker compose down

```




#  links

https://beam.apache.org/documentation/
https://beam.apache.org/get-started/an-interactive-overview-of-beam/


https://github.com/apache/beam
https://beam.apache.org/get-started/an-interactive-overview-of-beam/

https://github.com/mikeroyal/Apache-Beam-Guide


https://beam.apache.org/documentation/sdks/python/

https://beam.apache.org/get-started/wordcount-example/

https://beam.apache.org/documentation/programming-guide/


https://github.com/apache/beam/tree/master
https://github.com/apache/beam/tree/master/sdks/python/apache_beam/examples



##  colab examples fo apache beam 
https://beam.apache.org/get-started/an-interactive-overview-of-beam/

https://colab.research.google.com/github/apache/beam/blob/master/examples/notebooks/interactive-overview/getting-started.ipynb



# some code 
https://github.com/GoogleCloudPlatform/dataflow-geobeam/blob/main/Dockerfile



# run some code 
https://beam.apache.org/get-started/quickstart-py/
https://github.com/apache/beam/tree/master/sdks/python/apache_beam/examples
https://beam.apache.org/get-started/an-interactive-overview-of-beam/

cd ~
python3 -m venv $HOME/apps/beam
. $HOME/apps/beam/bin/activate
pip3.10 install apache-beam


python -m apache_beam.examples.wordcount --input ./my-document.txt --output ./counts




####  outros tutoriais
https://ndeepak.com/posts/2022-07-07-local-beam/

https://github.com/mikeroyal/Apache-Beam-Guide

https://events19.linuxfoundation.org/wp-content/uploads/2017/11/Apache-Beam-The-Solution-for-Portable-and-Evolutive-Data-intensive-Applications-Ismael-Mejia-Talend.pdf


https://github.com/davidgasquez/apache-beam-jupyter-notebook/tree/master





# Beam in docker ------------------------------------------
https://github.com/davidgasquez/apache-beam-jupyter-notebook/tree/master


## Apache Beam On Jupyter Notebooks

[![https://colab.research.google.com/assets/colab-badge.svg](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/davidgasquez/apache-beam-jupyter-notebook/blob/master/Notebook.ipynb)

A simple Apache Beam pipeline running in a Jupyter Notebook. Useful for developing Apache Beam Pipelines.

## Getting Started

The easiest way to get started is running the Notebook in Google Colab. If you can to run it locally, clone this repository and run `make`. Once the Docker container is running you can play with the notebook at [`http://localhost:8888`](http://localhost:8888).


# ------------------------------------------------

https://github.com/apache/beam/blob/master/examples/notebooks/get-started/learn_beam_basics_by_doing.ipynb

https://play.beam.apache.org/?path=SDK_PYTHON_WordCountWithMetrics&sdk=python

https://beam.apache.org/get-started/an-interactive-overview-of-beam/


https://github.com/apache/beam/blob/master/examples/notebooks/get-started/learn_beam_basics_by_doing.ipynb


# Dockerize  the apache beam on jupiter DirectRun 


### Docker File 

```
FROM python:3

RUN apt-get -y update

RUN  pip3 install "apache-beam[interactive,dataframe]" 
RUN pip3 install jupyter
RUN pip3 install jupyterlab

WORKDIR /

CMD ["jupyter",  "lab", "--NotebookApp.token='cmgm'", "--NotebookApp.notebook_dir=$HOME" , "--ip=0.0.0.0", "--port=8888", "--allow-root"]
```


> ! pip install "apache-beam[gcp,interactive,dataframe]"


```
cd proj_dir

export IMAGE_NAME=apache-beam-on-jupyter-notebook:1.0.0

docker build -t $IMAGE_NAME .

docker run   -d  --rm --name jupyter_beam -p 8889:8888  -e JUPYTER_TOKEN=cmgm   -v $(pwd):/app  
$IMAGE_NAME
```



docker run -it -p 8888:8888  --rm -v $(pwd):/work/ $IMAGE_NAME  bash


docker run -it -p 8888:8888  --rm -v $(pwd):/work/ apache-beam-on-jupyter-notebook:   /bin/bash

jupyter notebook --NotebookApp.token='cmgm'  "--NotebookApp.notebook_dir=$HOME"    --ip=0.0.0.0" --port=8888" --allow-root 


c.NotebookApp.notebook_dir =


# code 
https://colab.research.google.com/github/apache/beam/blob/master/examples/notebooks/interactive-overview/reading-and-writing-data.ipynb

# examples 
https://beam.apache.org/documentation/ml/overview/#data-processing

https://beam.apache.org/get-started/an-interactive-overview-of-beam/

