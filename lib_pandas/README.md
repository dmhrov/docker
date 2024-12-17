##### a. Create a docker image in which you need to install the Python library pandas version 1.26. 

Create a directory and `Dockerfile`

```
mkdir python-pandas && cd python-pandas

touch Dockerfile
```

 `Dockerfile`:

```
FROM python:3.9-slim
WORKDIR /
RUN pip install pandas==1.2.5
CMD ["bash"]
```

##### b. Run in interactive mode and show all files in workdir.

Build and run the Docker container:

```
docker build -t python-pandas:1.2.5 .

docker run -it python-pandas:1.2.5
```

Inside the container, list files:

```
ls -la
```

> [!NOTE]
> incorrect version of pandas 1.26 - current versions of [pandas](https://github.com/pandas-dev/pandas/releases)
> 
