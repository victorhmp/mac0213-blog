---
title: Conteinerização (Pt. 2)
date: "2018-05-13"
---

Durante a semana dos dias 05/05 à 11/05, comecei a trabalhar na parte prática da conteinerização do FATIMA. Primeiro, pesquisei artigos com exemplos de como utilizar o MariaDB dentro de um container e fazer _queries_ de um outro container, algo muito comum quando rodando uma instância de um banco de dados com auxílio do _Docker_. Encontrei muitos artigos e tentei reproduzir o que encontrei, porém algo que não encontrei e ainda tentei resolver de diversas formas, ainda sem sucesso, foi como rodar o script de instalação dentro do container antes de deixá-lo rodando.

Minha dificuldade veio do fato de que não quero ter que criar um quarto container apenas para se conectar com o container original de MariaDB e rodar o script de inicialização do banco, pois acredito que essa solução está longe da ideal. Ainda estou buscando um jeito de resolver esse problema, por meio da criação de uma imagem customizada do MariaDB acredito que vou conseguir.

Enquanto não consegui rodar o script que preciso dentro do container com MariaDB, trabalhei em conseguir subir o container da API. Estou utilizando uma imagem base do Gradle para subir a API do FATIMA, e tive alguns problemas relacionados à árvore de repositórios que estava sendo passada para dentro do container e problemas de permissão de alteração dos arquivos, mas esses problemas foram resolvidos. O processo de _build_ da API é demorado e deve ser executado sempre que subo os containers, isso torna a realização de testes mais lenta. Recebo múltiplos _warnings_ ao subir o container da API, mas o erro que ocorre no último passo é referente ao fato de não conseguir subir o container do banco de dados od jeito que devia.

No dia 09/05 (quinta-feira), estive em uma reunião com o time da SMIT responsável pela aplicação e expus os problemas que estava tendo. Conversamos sobre possíveis soluções e sobre um eventual ajuste no cronograma inicial, dado o atraso de três semanas que tivemos na disponibilização do código.

**Horas**: 12 horas
