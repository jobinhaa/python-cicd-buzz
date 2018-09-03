# Creating a test enviroment 

    pip install virtualenv

    virtualenv lab

    source lab/Scripts/activate

    pip install -r requirements.txt


### Creating tests modules
    python -m pytest -v tests/test_generator_py

## Travis (SAAS) - Software as a Service
    - no install
    - consome como SVC
    * segurança

## Jenkins (Offline)
    * require install 
    * disponibilidade
    - controles de segurança
    - open source


## Config travis.yml

Create Travis.yml in the root
This will be a *declarative file*

## Create Docker file
Packing files for production

    FROM alpine:3.5
    RUN apk add --update python py-pip
    COPY requirements.txt /src/requirements.txt
    RUN pip install -r /src/requirements.txt
    COPY app.py /src
    COPY buzz /src/buzz
    CMD python /src/app.py
