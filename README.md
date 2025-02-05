커맨드
바탕화면의 ai-team-resources 경로에서 실행합니다.
```bash
pushd binaries
wget https://cloud-images.ubuntu.com/wsl/jammy/20250203/ubuntu-jammy-wsl-amd64-ubuntu22.04lts.rootfs.tar.gz
wget https://rpm.rancher.io/k3s/latest/common/centos/7/noarch/k3s-selinux-0.2-1.el7_8.noarch.rpm
popd
pushd charts
helm repo update
helm pull bitnami/keycloak --version 24.4.8
helm pull bitnami/kube-prometheus --version 11.0.0
popd
pushd images
docker pull --platform=linux/amd64 bitnami/keycloak-config-cli:6.2.1
docker pull --platform=linux/amd64 bitnami/keycloak:26.1.0
docker pull --platform=linux/amd64 bitnami/prometheus-operator:0.79.2
docker pull --platform=linux/amd64 bitnami/blackbox-exporter:0.25.0
docker save bitnami/keycloak-config-cli:6.2.1 -o bitnami-keycloak-config-cli-6.2.1.tar
docker save bitnami/keycloak:26.1.0 -o bitnami-keycloak-26.1.0.tar
docker save bitnami/prometheus-operator:0.79.2 -o bitnami-prometheus-operator-0.79.2.tar
docker save bitnami/blackbox-exporter:0.25.0 -o bitnami-blackbox-exporter-0.25.0.tar
popd
```
