---
title: Conteinerização (Pt. 4)
date: "2019-05-19"
---

Durante a semana dos dias 12/05 à 18/05, continuei trabalhando na implementação da dockerização da plataforma tentando fazer os diferentes módulos funcionarem nos containeres.

Para o módulo de _back-end_ troquei a imagem base sendo usada para a imagem oficial do Gradle, o que elimina a necessidade de um paço extra no processo de build só para instalar essa ferramenta. Escrevi um Dockerfile para extender a imagem original adicionando a execução dos scripts que precisavam ser executados para compilar e executar todo esse módulo da FATIMA, além da instrução que realiza a configuração inicial do banco de dados por meio do mysql, base do MariaDB.

Com essas alterações consegui finalmente subir o container da API, apenas com uma série de _warnings_ que já eram "esperados" e não vieram de alterações feitas por mim.

**Horas**: 8 horas
