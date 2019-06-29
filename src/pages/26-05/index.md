---
title: Conteinerização (Pt. 6)
date: "2019-06-02"
---

Durante a semana dos dias 26/05 à 01/06, trabalhei em alguns ajustes finais nos módulo de _back-end_ e do banco de dados.

Fiz modificações procurando evitar a cópia de arquivos desnecessários para o container e tentar deixar o processo de _build_ e _up_ mais rápido. Pra isso modifiquei o script de inicialização da API quebrando-o em dois, sendo um deles responsável por compilar o código dos diferentes serviços que compõem o _back-end_ e o outro responsável por subir o servidor da aplicação e inicializar o banco de dados.

Com essas modificações, o processo de subida da aplicação ficou muito mais rápido, pois o código não seria compilado sempre, e o banco de dados não precisaria ser criado novamente.

Durante a semana também tive problema com o dump do banco de dados que tinha recebido, que resultavam em erro quando tentava popular o BD. Levei esse problema para o time da SMIT e eles me mandaram um dump mais recente, com esse consegui inicializar o BD.

**Horas**: 8 horas
