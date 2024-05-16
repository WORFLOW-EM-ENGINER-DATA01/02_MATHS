```bash
docker build -t env-python .
docker run -it --rm --name env-running-python -v ./:/usr/src/app env-python /bin/bash

# Une image de Jupyter
# docker pull jupyter/datascience-notebook
docker run -it --rm -p 10000:8888 -v "${PWD}":/home/jovyan/work quay.io/jupyter/datascience-notebook:2024-04-29

# Token et mot de passe
jupyter server list
# récupération du token et définition du mot de passe
```
