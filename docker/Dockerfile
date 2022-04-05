FROM python:3.6
MAINTAINER Andrew Howell "ahowell@singularity.ltd.uk" 
COPY . /webapp
WORKDIR /webapp
RUN pip install -r requirements.txt
ENTRYPOINT ["python"]
CMD ["webapp.py"]
