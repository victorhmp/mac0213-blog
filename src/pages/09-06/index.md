---
title: Conteinerização (Pt. 8)
date: "2019-06-16"
---

Durante a semana dos dias 09/06 à 15/06, dei os passos finais para concluir a conteinerização da FATIMA.

O time da SMIT no nosso servidor do Slack e eles me passaram instruções de como utilizar o Apache HTTP Server e decidi que seria melhor como base a imagem oficial no _Docker Hub_.

Escrevi uma Dockerfile nova que usa a Apache HTTP server como base, instala Node.js e NPM no contêiner e depois usa o próprio NPM para instalar o Gulp, que então executa o build e por fim coloca o resultado no diretório /usr/local/apache2/htdocs/ do container para ser servida pela porta 3001.

Com os três módulos funcionando, atualizei o arquivo `docker-compose.yml` que lida com o processo de criação e build dos três contêineres, cria os volumes necessários para persistência de cada um e cria a network que eles precisam para se comunicar.

Em uma reunião com o time da SMIT, testamos o funcionamento completo da plataforma já completamente dockerizada e vimos que tudo estava funcionando como devia, menos a funcionalidade de geração de PDFs de forma persistente. Esse problema foi resolvido com a criação de mais um volume no docker-compose.yml que é mapeado e compartilhado pelos contêineres do _front-end_ e do _back-end_.

**Horas**: 5 horas
