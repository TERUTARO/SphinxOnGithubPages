FROM python:3.9-buster

ENV PIPENV_INSTALL_TIMEOUT=5000
ENV PIPENV_VENV_IN_PROJECT=1

# dir settings
RUN mkdir /var/{src, build, config}
WORKDIR config

# apt package install 
RUN apt-get update && \
    apt-get install -y \
            python-pip \
            texlive-latex-extra \
            latexmk \
            texlive-lang-japanese

# python package install 
COPY ./infrastructure/docker/config/requirements.conf /config
RUN pip install -r requirements.conf