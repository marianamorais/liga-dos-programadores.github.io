---
title: "Rodando IPFS com Docker"
date: "2019-10-19"
author: "@ratsclub"
cover: "ratsclub/rodando-ipfs-no-docker/cover.jpg"
description: "Como rodar IPFS com Docker em menos de 5 minutos"
tags:
- ipfs
- p2p
---

Esse tutorial fora escrito utilizando o Debian na versão 10.

Muitas vezes quero utilizar o [IPFS](https://ipfs.io/ipns/ipfs.io/), entretanto não quero me preocupar em instalar a linguagem [Go](https://golang.org/) e muito menos em com a ferramenta ``ipfs_version``.

## Instalando o Docker

A instalação do docker é bem simples e pode ser feita através do seguinte [link](https://docs.docker.com/install/linux/docker-ce/debian/).

## Configurando o container

1. Crie diretórios para o IPFS
```bash
$ mkdir -p ~/.ipfs/staging
```

2. Crie o seguinte script onde preferir
```bash
#!/bin/bash

export ipfs_staging=/home/[SEU DIRETORIO HOME]/.ipfs/staging
export ipfs_data=/home/[SEU DIRETORIO HOME]/.ipfs

docker run -d --init \
        --restart unless-stopped \
        --name ipfs_host \
        -v $ipfs_staging:/export \
        -v $ipfs_data:/data/ipfs \
        -w /export \
        -p 4001:4001 \
        -p 127.0.0.1:8080:8080 \
        -p 127.0.0.1:5001:5001 \
        ipfs/go-ipfs:v0.4.18
```
Vamos entender esses comandos.

- ``-d``: Roda o container no estado "avulso".

- ``--restart unless-stopped``: Esse comando habilita o restart automático do container quando não parado, mas também nos tráz o recurso da inicialização do container no boot.

- ``--name ipfs_host``: Determina o nome do container. Você pode colocar o nome que desejar.

- ``-v $ipfs_staging:/export`` e ``-v $ipfs_data:/data/ipfs``: Montam volumes. Esse comando mapeia os diretórios ``$ipfs_staging`` e ``$ipfs_data`` da sua máquina local para os diretórios ``~/.ipfs`` e ``/export`` do container.

- ``-w /export``: O diretório de "trabalho" dentro do container.

- ``-p 4001:4001``: Expõe a porta 4001 - necessária para o swarming - para o mundo.

- ``-p 127.0.0.1:8080:8080`` e ``-p 127.0.0.1:5001:5001``: Expõem as portas 8080 (gateway) e 5001 (API) somente de forma local.

- ``ipfs/go-ipfs:latest``: O nome da imagem do container.

## O que é esse diretório "staging"?

O diretório staging é como um sandbox para você rodar comandos IPFS. Esse diretório é compartilhado entre a máquina host e o container. Veja a seção a seguir para ver como rodar comandos como ``ipfs add`` e ``ipfs get``.

## Usando o Container

Adicione essa função para o seu arquivo ``~/.bash_aliases`` file, or similar:

```bash
function ipfs() {
  docker exec ipfs_host ipfs "$@"
}
```
Então você poderá rodar comandos como ``ipfs add`` e ``ipfs_get``.

***Nota****: Se você alterou o nome do seu container, altere-o aqui também.*

## Removendo o container

```bash
$ docker stop ipfs_host # ou o nome que você colocou em seu container
$ docker rmi ipfs/go-ipfs
$ rm -rf ~/.ipfs
```

---

## Me ajude com um café ☕

**BTC**: [bc1qkc3yruufzkqxyvq5exe50lwrmtc00pmnf4wua0](bitcoin:bc1qkc3yruufzkqxyvq5exe50lwrmtc00pmnf4wua0)

**BCH**: [qqgtmvglvrr6297d6m2z3634pr0a6m77p5ke9lg03k](bitcoincash:qqgtmvglvrr6297d6m2z3634pr0a6m77p5ke9lg03k)

**ETH**: [0xbff1fFA9D91f81100E801120d03eA6C74F7dA87E](ethereum:0xbff1fFA9D91f81100E801120d03eA6C74F7dA87E)

**NANO**: [nano_1g4xrbrqd9axxdjjetkzxk9djinotbuqpbe9ccz3btscctjqyz4m6s5qxbiw](nano:nano_1g4xrbrqd9axxdjjetkzxk9djinotbuqpbe9ccz3btscctjqyz4m6s5qxbiw)