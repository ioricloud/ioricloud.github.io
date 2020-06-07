---
layout: post
title:  "Openshift - PaaS"
date:   2020-06-06 21:27:01 -0300
comments: true
categories: diario
---

# Openshift - Paas

É amigos, voltei, tava meio F&%$ atualizar aqui devido que o projeto Openshift na empresa que trabalho entrou no ar, com isso fiquei totalmente dedicado para a subir, configurar aplicações e adicionar tools para o esqueleto da nova arquitetura das aplicações. Durante este tempo tivemos muitos contratempos e o que digo amigos, foi um pouco dificil. Detalharei mais a seguir.

Primeira parte disso, deixar a nuvem pronta para receber o cluster Openshift que por padrão precisa que esteja liberado 15 ips validos, segundo liberação para que possa ser criado as maquinas com o tamanho apropriado para o Control Plane, mínimo de 3 servidores de um tamanho *parrudo*. Sem esquecer que se nós aumentarmos o cluster Kubernetes, de quebra, teremos que aumentar o Control Plane, `em pensar que o dolar está caro, está em tempos que custo teremos que sempre pensar quando se fala de Nuvem`, e eu como analista de Cloud Computing me preocupo bastante com Finanças.

Segunda parte, o Openshift por si, é bom e ao mesmo tempo confuso. Ele tem uma engenharia que para desenvolvedores que não querem perder o tempo de deployar a aplicação em um **Container** e digo, ele ajuda porque ele tem um sistema de `build` e `deploy`, que usando uma imagem preparada com o sistema **S2I**, você encapsula seu codigo lá dentro e entrega legal. Legal e muito interessante, mas nao sabe o que está sendo colocado lá dentro. Ainda estou tentando entender como este sistema de imagem funciona. A [Getup Cloud](https://blog.getupcloud.com) tem um post interessante sobre esta forma de criar esta imagem pre-pronta.

Terceiro e ultimo, nós la da empresa, demos uma parada no *Jenkins* e eu adotei o [Drone](drone.io), e assim, passei um belo dia, deployando de todas as formas, mas não tive êxito. Não desisti, mas vou dedicar a entrega das minhas tasks diarias e verei isso quando tudo passar. Mas ai, se alguem deployou ele no Kubernetes, manda infos de como deployou. Enquanto isso, vi que no proprio ecossistema do Openshift tem por padrao no seu modo Builder, adoção do **Jenkinsfile**, amanhã, tentarei ver como é a forma de CICD usando o *ele* para que eu possa já adotar nas aplicações que ja estão deployadas.

Conclusão, tenho mais uma nova batalha para ganhar. Mas não desistirei fácil e vou deixar este nosso ambiente totalmente à altura da Cultura.

De quebra, este post foi com um bom som ao fundo.

*musica para post - `Red Hot Chilli Pepper - Dark Necessities`*
