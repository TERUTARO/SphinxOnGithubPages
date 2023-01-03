FROM python:3.9-buster

ENV PIPENV_INSTALL_TIMEOUT=5000
ENV PIPENV_VENV_IN_PROJECT=1

RUN mkdir /var/{src, build, config}
WORKDIR /var/config


RUN apt-get update && \
    apt-get install -y \
            python-pip

# RUN apt-get update \
#     && apt-get install -y texlive-latex-extra \
#     latexmk \
#     texlive-lang-japanese



COPY ../requirements.txt /code/
RUN pip install -r requirements.txt


RUN pip install \
    --upgrade pip

RUN pip install \
        pipenv \
        sphinx 
    