# conversao-temperatura

## Como usar? (sem kubernetes)

1. vá ate a pasta conversao-temperatura, onde estar o Dockerfile e rode:
   1. `docker image build -t felippedeiro/conversao-temperatura:v1 .`
   1. `docker container run -d -p 8080:8080 felippedeiro/conversao-temperatura:v1`
1. abra o navegador cole a url `localhost:8080`

## Como usar? (com kubernetes)

1. caso não tenha um cluster criado, rode `kind create cluster --name meucluster --config cluster.yaml `
1. vá ate a pasta do k8s `cd k8s`, suba os objetos `kubectl apply -f deployment.yaml`
1. espere todos os objetos do kubernetes estarem funcionando (pode usar o comando `watch kubectl get all`), abra o navegador cole a url `localhost:8080`
