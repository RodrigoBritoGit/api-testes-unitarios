# API de Autenticação

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)

Este projeto é uma API construída usando **Java, Java Spring e H2 como banco de dados.**

## Tabela de Conteúdos

- [Instalação](#instalação)
- [Configuração](#configuração)
- [Uso](#uso)
- [Endpoints da API](#endpoints-da-api)
- [Banco de Dados](#banco-de-dados)

## Instalação

1. Clone o repositório:

```bash
git clone https://github.com/RodrigoBritoGit/api-testes-unitarios.git
```

2. Instale as dependências com Maven

## Uso

1. Inicie a aplicação com Maven
2. A API estará acessível em http://localhost:8080


## Endpoints da API
A API fornece os seguintes endpoints:

**GET USUÁRIOS**
```markdown
GET /users - Recupere uma lista de todos os usuários.
```
```json
[
    {
        "id": 1,
        "firstName": "Pedro",
        "lastName": "Silva",
        "documento": "123456787",
        "email": "pedro@example.com",
        "senha": "senha",
        "saldo": 20.00,
        "tipoDeUsuário": "COMERCIANTE"
    },
    {
        "id": 4,
        "firstName": "Luckas",
        "lastName": "Silva",
        "documento": "123456783",
        "email": "luckas@example.com",
        "senha": "senha",
        "saldo": 0.00,
        "tipoDeUsuário": "COMUM"
    }
]
```

**POST USUÁRIOS**
```markdown
POST /users - Registre um novo usuário no aplicativo
```
```json
{
    "firstName": "Lucas",
    "lastName": "Silva",
    "senha": "senha",
    "documento": "123456783",
    "email": "lucas@example.com",
    "tipoDeUsuário": "COMUM",
    "saldo": 10
}
```

**POST TRANSAÇÕES**
```markdown
POST /transactions - Registre uma nova transação entre usuários (COMUM para COMUM ou COMUM para COMERCIANTE)
```

```json

{
  "senderId": 4,
  "receiverId": 1,
  "valor": 10
}
```

## Banco de Dados
O projeto utiliza o [H2 Database](https://www.h2database.com/html/tutorial.html) como banco de dados.
