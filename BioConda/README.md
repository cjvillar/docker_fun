# Bioconda Image

Here is a bioconda image example with a short exercise


build:
```bash
docker build -t bioconda_image .
```

# Test creation of container with Bioconda
run with interactive shell:
```bash
docker run -it bioconda_image
```
run smatools help
```bash
samtools
```
stop container. open up another terminal and run:
```bash
Docker ps
```
get container id and run:
```bash
Docker stop <container_id>
```


## Exercise (WIP)
access local files in container:

```bash
docker run -it -v $(pwd)/local_file.txt:/path/in/container/local_file.txt bioconda_image
```