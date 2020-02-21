---
layout: post
title:  "Projetos CICD e Futuro Openshift"
date:   2020-02-21 08:34:01 -0300
categories: diario
---

# Projetos CICD e Futuro Openshift

Ontem, meu gestor me pediu para acelerar os projetos de CICD, como ja tinha começado a criação de alguns projetos no *Jenkins*, e ainda pensando como será a entrega destes artefatos aos serviços, eu tirei uma duvida com meu amigo * Skeeter X aka Pedim*, ele me indicou o AWX (Ansible Tower opensource), e segui um tutorial para criar em uma VM com docker-compose, ate criar a VM e instalar o `docker` com o `docker-compose` e de quebra o `python3` com o `pip-3`. *Empanquei* com UP do docker-compose do projeto, que o projeto detecta que tem que ter alguns pacotes docker instalado com o pip-3.

Ao tentar subir, me mostrava um erro, ou o `docker-py` tava instalado mas nao condizia com o o python usado, no qual é o python2, ou faltava o `docker sdk for python`.

Revi o codigo do inventory e me mostrou isso, usando este codigo abaixo isso dentro da pasta `installer`
    *grep -v '^#' inventory | grep -v '^$'*

A saída é essa:

    localhost ansible_connection=local ansible_python_interpreter="/usr/bin/env python3"
    [all:vars]
    dockerhub_base=ansible
    awx_task_hostname=awx
    awx_web_hostname=awxweb
    postgres_data_dir=/var/lib/pgdocker
    host_port=80
    host_port_ssl=443
    docker_compose_dir=/tmp/awxcompose
    pg_username=awx
    pg_password=awxpass
    pg_admin_password=admin
    pg_database=awx
    pg_port=5432
    rabbitmq_password=awxpass
    rabbitmq_erlang_cookie=cookiemonster
    admin_user=admin
    admin_password=admin
    create_preload_data=True
    secret_key=ejv9P72oNvD4AtWLhOUTvpxfdIfKIid3skwuK+ES

Qual foi a dica do milhão. Desinstalei docker, docker-compose e docker-py e reinstalei somente o docker-compose usando o pip-3. Após isso `zaz`.

Lembrando, que usar o *AWX* requer uma machine de 2gb em diante. Indico fortemente usar.

*podcast para o post - `Foro de Teresina - #89: As mentiras de Bolsonaro, a caserna no Planalto e os tiros contra Cid Gomes`*