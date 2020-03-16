---
layout: post
title:  "Drone.io - Um Overview"
date:   2020-03-15 23:11:01 -0300
comments: true
categories: diario
---

# Drone.io - Um Overview

Como tinha falado no post anterior, eu ia dar um feedback apurado sobre a ferramenta. Estou a duas semanas usando ela e posso dizer, curti *pa caralho*. Leve, simples, e rapida, essa é alguns dos adjetivos para a ferramenta. Antes de concluir com essa opiniao pessoal (que fique claro), eu procurei alguma ferramenta que fosse tanto para ambientes distintos, já que onde trabalho hoje estamos fazendo migração de monolito para microserviços, com isso, eu estou realizando essa migração juntamente com meu colega de trabalho. Como somos os responsavéis sobre a Cloud, temos esta tarefa de fazer algo que não ultrapasse os custos e que tenhamos uma performance significativa. Vamos para o post.

[Drone.io](https://drone.io), ferramenta de CI - *Continuous Integration* - feito em Go, que está na sua versão acima de 1. Sobre documentação, gostei, explica bastante, bastante exemplos, fora seu forum e um canal no Gitter. Gostei bastante dele porque o deploy já em docker, tambem existe para service em kubernetes. Seus arquivos para realizar os CIs é em YAML *bem mais facil que um Groovy da vida* e também tem os `Runner` dockers auxiliares para realizar as tarefas das Pipelines. A `Runner`que uso atualmente é a de docker, mas tem, SSH, Kubernetes, Exec.

Sobre a Pipeline, eu fiquei um pouco com duvidas porque o arquivo manifesto nas versões anteriores, você não declarava o tipo da pipeline, na versão atual, você declara tipo e ainda dar um nome, bem mais didatico e organizado. Vou dar um exemplo abaixo:
```
kind: pipeline
type: docker
name: python.app

steps:
- name: build
  image: golang
  commands:
  - go build
  - go test

trigger:
  branch:
  - master
  event:
  - push
```

Este exemplo é so um no qual coloquei, mas existem varias formas de realizar o seu CI com o Drone. 

Espero que surja mais adeptos para usar esta maravilhosa ferramenta. Sintam-se a vontade para me contactar sobre. Twitter ou Email.

*Música para o post - `Chico Science e Nação Zumbi - Manguetown`*