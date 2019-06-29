---
title: Conteinerização (Pt. 5)
date: "2019-05-25"
---

Durante a semana dos dias 19/05 à 25/05, continuei o trabalho de implementação da conteinerização da FATIMA.

Com os resultados obtidos na semana anterior de ter conseguido subir o container da API, ainda não estava conseguindo fazer com que a API se comunicar com o módulo do banco de dados.

Depois de conversar com o time da SMIT, apaguei a Dockerfile que tinha criado para o serviço e decidi utilizar a imagem do MariaDB disponível no Docker Hub sem alterações, movendo a responsabilidade de rodar comandos para iniciar o banco para o módulo do back-end, assim contornando um problema que estava enfrentando ao tentar rodar os scripts de configuração no banco antes mesmo dele ser iniciado.

**Horas**: 8 horas
