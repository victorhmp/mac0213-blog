---
title: Teste de configuração (GitLab CI/CD)
date: "2019-06-23"
---

Durante a semana dos dias 16/06 à 22/06, criei um repositório privado no GitLab chamado `fatima-test` na minha conta pessoal para hospedar o código-fonte da aplicação já dockerizado e escrevi o arquivo `.gitlab-ci.yml` que configura os diferentes passos do continuous integration a serem executados.

Configurei os passos de _build_ e _stage_, que são executados por Runners que executam comandos de Docker e preparam a aplicação para ser lançada.

Infelizmente não consegui implementar o passo final no GitLab CI/CD que seria o deploy da aplicação, pois isso só pode ser feito no repositório oficial da FATIMA e terá que ser implementado pelo time da SMIT.

**Horas**: 5 horas
