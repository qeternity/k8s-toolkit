FROM debian:buster

RUN apt-get update &&\
    apt-get install -y curl &&\
    curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.18.0/bin/linux/amd64/kubectl &&\
    chmod +x ./kubectl &&\
    mv ./kubectl /usr/local/bin/ &&\
    curl -LO https://get.helm.sh/helm-v3.2.0-linux-amd64.tar.gz &&\
    tar -zxf helm-v3.2.0-linux-amd64.tar.gz &&\
    mv linux-amd64/helm /usr/local/bin/ &&\
    rm -rf linux-amd64 helm-v3.2.0-linux-amd64.tar.gz &&\
    apt-get clean && apt-get autoclean 
