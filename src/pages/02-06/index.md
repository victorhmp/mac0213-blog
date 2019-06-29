---
title: Conteinerização (Pt. 7)
date: "2019-06-09"
---

Durante a semana dos dias 02/06 à 08/06, consegui focar meu trabalho no módulo de _front-end_.

Num primeiro momento criei um Dockerfile para o módulo de _front-end_ usando como base a imagem oficial do NodeJS disponível no _Docker Hub_. Durante o processo de _build_ da imagem, instalava todas as dependências necessárias e por fim utilizava o _Gulp_ para subir um servidor de desenvolvimento.

Esperava que a dockerização desse módulo fosse bem rápida, porém tive problemas com o passo final de subida do servidor de teste, pois o comando `gulp serve` não estava funcionando corretamente.

Levei o problema para o time da SMIT no final da semana e aguardo um retorno.

**Horas**: 6 horas
