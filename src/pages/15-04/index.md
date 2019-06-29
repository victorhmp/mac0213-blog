---
title: Recebimento do código da aplicação
date: "2019-04-21"
---

Durante a semana dos dias 14/04 à 20/04, recebi o código da aplicação por email (dia 16/04) e busquei entender como a aplicação estava dividida para poder sugerir qual a melhor maneira de conteinerizá-la.

Basicamente a aplicação está dividida em três módulos: o banco de dados, MariaDB; um back-end que interage com o banco e expõe uma API, feito com Java e Gradle automação de processos; um front-end que serve como cliente da API e interface para interação com o usuário do FATIMA, feito com AngularJS.

O setup do ambiente local para rodar a plataforma está documentada no README do repositório, e no seu estado atual é longo e envolve instalação de algumas dependências no computador do usuário, apesar da presença de scripts que automatizam a subida da plataforma uma vez feito o setup de desenvolvimento, o que deve facilitar a conteinerização.

**Horas**: 5 horas
