# Python Flask Docker WebApp#

Build the image using the following command,  Note this is for Singularity Ltd,  to deploy to dockerhub 

```bash
$ docker build -t singularityltd/singularity-flask-webapp:latest .
```

And to push the docker to dockerhub :
```bash
$ docker login -u <username>
$ docker push singularityltd/singularity-flask-webapp:latest 
```



To Just Build it Locally,  Use:

```bash
$ docker build -t singularity-flask-webapp:latest .
```

Run the Docker container using the command shown below.

```bash
$ docker run -d -p 8080:5000 singularity-flask-webapp 
```

The application will be accessible at http://127.0.0.1:8080 
