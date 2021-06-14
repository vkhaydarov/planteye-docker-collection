# PlantEye/Docker-Collection

This repository contains dockerfiles and docker-compose files of Nebula for PEAs within the P2O-Lab.

## Usage
Before usage please ensure the proper content of the configuration file (config.yaml)

### Local compilation
To create image and container locally execute the following command:
```bash
sudo docker-compose up
```

### Push on dockerhub
To reduce effort of deploying docker image can be uploaded onto dockerhub by means of the following command:

```bash
sudo docker build --no-cache -t "nebula_xxx" .
docker tag nebula_xxx vkhaydarov/planteye-nebula-xxx
docker push vkhaydarov/planteye-nebula-xxx
```
where xxx denotes the identifier of the module, i.e. "m01" for the Feed-Module.

### Pull from dockerhub
To deploy the dockerhub-image please execute the following:
```bash
sudo docker pull "vkhaydarov/planteye-nebula-xxx"
sudo docker run --rm -it "vkhaydarov/planteye-nebula-xxx"
```
where xxx denotes the identifier of the module, i.e. "m01" for the Feed-Module.

## Requirements
docker and docker-compose (see official manual)

## License
Valentin Khaydarov (valentin.khaydarov@tu-dresden.de)\
Process-To-Order-Lab\
TU Dresden
