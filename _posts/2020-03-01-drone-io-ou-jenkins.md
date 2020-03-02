---
layout: post
title:  "Drone.io ou Jenkins"
date:   2020-03-01 23:11:01 -0300
categories: diario
---

# Drone.io ou Jenkins

Post pos-carnaval e como o post anterior eu estava num rumo para saber qual a melhor ferramenta para `CICD`, no qual o meu gestor pediu, como já havia implatado `Jenkins` mas estou com um pequeno receio em usar, devido como está a infraestrutura atual. Com isso, pesquisei alguma ferramenta com otimo desempenho e de quebra maleavel. Encontrei (drone.io)[https://drone.io] e curte PA CARALHO, primeiro, feito em GO, segundo baseado em pipelines, e por ultimo, seu manifesto é em yaml. CHUPA.

Maioria das ferramentas hoje usam yaml. Porque não se adaptar a isso.

Hoje em um pequeno lab usando (GCP-Google Cloud Platform)[https://cloud.google.com], usei drone em docker e como não tenho dominio, usei Gogs, outra ferramenta em GO. Sistema de Controle de Versionamento like Github, Gitlab. Que tambem foi *dockerizado*.

No proximo post, coloco tudo que foi feito e de quebra vejo se consigo colocar como é feito o CI usando o Drone.

*podcast para o post - `The Cloudcast - Cloud Computing - CI/CD and Drone.io`*