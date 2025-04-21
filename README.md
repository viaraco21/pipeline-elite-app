##Projeto Pipeline de Elite.

Deploy automatico da aplicacao Review-Filmes feito em .Net.

Feito Teste de Unidade, e Validação do codigo com o Trivy.

Criacao de imagem e envio para o repositorio no Docker Hub.

Deploy direto no cluster EKS da AWS.

## Comandos
aws eks describe-cluster --name NOME_DO_SEU_CLUSTER --query "cluster.endpoint" --output text

aws eks update-kubeconfig --name NOME_DO_CLUSTER --region REGIAO

Teste a conectividade de dentro do cluster
kubectl run -it --rm debug --image=appropriate/curl --restart=Never -- sh

apt update && apt install -y postgresql-client   # se curl não tiver o psql
psql -h postgres.cgrcivy6tiia.us-east-1.rds.amazonaws.com -U pipeline_elite -d pipeline_elite