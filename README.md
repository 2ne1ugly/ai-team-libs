docker 커맨드
```sh
helm repo add datahub https://helm.datahubproject.io/
helm pull datahub/datahub-prerequisites --version 0.1.15
helm pull datahub/datahub --version 0.5.1
helm repo add bitnami https://charts.bitnami.com/bitnami
helm pull bitnami/schema-registry --version 23.1.1
helm pull bitnami/mysql --version 12.2.1
helm pull bitnami/kafka --version 31.2.0
helm pull bitnami/zookeeper --version 13.7.2
helm pull bitnami/neo4j --version 0.2.2

docker pull --platform=linux/amd64 acryldata/datahub-gms:v0.15.0
docker pull --platform=linux/amd64 acryldata/datahub-frontend-react:v0.15.0
docker pull --platform=linux/amd64 acryldata/datahub-actions:v0.15.0
docker pull --platform=linux/amd64 acryldata/datahub-mae-consumer:v0.15.0
docker pull --platform=linux/amd64 acryldata/datahub-mce-consumer:v0.15.0
docker pull --platform=linux/amd64 acryldata/datahub-ingestion:v0.15.0
docker pull --platform=linux/amd64 acryldata/datahub-elasticsearch-setup:v0.15.0
docker pull --platform=linux/amd64 acryldata/datahub-kafka-setup:v0.15.0
docker pull --platform=linux/amd64 acryldata/datahub-mysql-setup:v0.15.0
docker pull --platform=linux/amd64 acryldata/datahub-postgres-setup:v0.15.0
docker pull --platform=linux/amd64 acryldata/datahub-upgrade:v0.15.0
docker pull --platform=linux/amd64 bitnami/schema-registry:7.8.0
docker pull --platform=linux/amd64 bitnami/mysql:8.4.3
docker pull --platform=linux/amd64 bitnami/kafka:3.9.0
docker pull --platform=linux/amd64 bitnami/zookeeper:3.9.3
docker pull --platform=linux/amd64 bitnami/neo4j:5.26.1

docker save -o datahub.tar acryldata/datahub-gms:v0.15.0 acryldata/datahub-frontend-react:v0.15.0 acryldata/datahub-actions:v0.15.0 acryldata/datahub-mae-consumer:v0.15.0 acryldata/datahub-mce-consumer:v0.15.0 acryldata/datahub-ingestion:v0.15.0 acryldata/datahub-elasticsearch-setup:v0.15.0 acryldata/datahub-kafka-setup:v0.15.0 acryldata/datahub-mysql-setup:v0.15.0 acryldata/datahub-postgres-setup:v0.15.0 acryldata/datahub-upgrade:v0.15.0
docker save -o schema-registry.tar bitnami/schema-registry:7.8.0
docker save -o mysql.tar bitnami/mysql:8.4.3
docker save -o kafka.tar bitnami/kafka:3.9.0
docker save -o zookeeper.tar bitnami/zookeeper:3.9.3
docker save -o neo4j.tar bitnami/neo4j:5.26.1
```
