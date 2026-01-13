# 🏦 Santander Dev Week 2024 - Java API

<p align="center">
  <img src="https://img.shields.io/badge/Status-Concluido-blue" alt="Status">
  <img src="https://img.shields.io/badge/Java-17+-orange" alt="Java">
  <img src="https://img.shields.io/badge/Spring_Boot-3.x-green" alt="Spring Boot">
  <img src="https://img.shields.io/badge/Deploy-Railway-lightgrey" alt="Railway">
</p>

## 📖 Descrição do Projeto
API RESTful desenvolvida durante o bootcamp **Santander Backend Java** em parceria com a **DIO**. O projeto simula o backend de uma aplicação bancária, focando em boas práticas de desenvolvimento, modelagem de dados rigorosa e publicação em ambiente de produção.

O grande diferencial deste projeto é a utilização do **Railway** para o deploy e o banco de dados **PostgreSQL** em nuvem.

---

## 🚀 Funcionalidades
- `Modelagem de Usuários`: Sistema completo de cadastro de usuários com contas, cartões e funcionalidades.
- `API REST`: Endpoints documentados para criação e busca de dados.
- `Tratamento de Exceções`: Camada global para capturar erros e retornar mensagens amigáveis.
- `Arquitetura em Camadas`: Separação clara entre Controller, Service, Repository e Model.

---

## 📊 Diagrama de Classes
```mermaid
classDiagram
    class User {
        - String name
        - Account account
        - Card card
        - List~Feature~ features
        - List~News~ news
    }
    class Account {
        - String number
        - String agency
        - float balance
        - float limit
    }
    class Feature {
        - String icon
        - String description
    }
    class Card {
        - String number
        - float limit
    }
    class News {
        - String icon
        - String description
    }
    User "1" *-- "1" Account
    User "1" *-- "N" Card
    User "1" *-- "N" Feature
    User "1" *-- "N" News
