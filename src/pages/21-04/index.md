---
title: Conteinerização (Pt. 1)
date: "2018-05-01"
---

Durante a semana dos dias 21/04 à 27/04, busquei encontrar qual seria a melhor maneira de dividir e orquestrar os serviços e módulos que compõem o FATIMA em containers utilizando _Docker_ e _Compose_.

Num primeiro momento, pensei em criar dois containers, sendo um deles rodando uma imagem baseada na imagem original do NodeJS para rodar o front-end do FATIMA e o outro rodando uma imagem customizada que rodaria uma instância do MariaDB e instalaria as dependências necessárias para utilizar Java e Gradle.

Depois de pesquisar sobre a imagem padrão do MariaDB e do Gradle no Docker Hub, descobri que talvez não fosse uma boa ideia misturar num container só dois serviços diferentes, o banco de dados e a API, e ainda seria necessária a criação de uma imagem muito mais complexa. Com isso, decidi que seria melhor utilizar 3 containers no lugar de 2: um container para executar o front-end; um container para rodar o back-end e servir a API; e um container com a função exclusiva de rodar um banco de dados MariaDB como servidor.

Através do _Compose_, vou conseguir gerenciar a subida desses containers, como um definido como um _service_.

**Horas**: 6 horas
