## Estrutura de pastas
Esta é a estrutura de pastas para um Prjeto FastAPI. A estrutura de pastas é baseada no [The Clean Architecture](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html) e no [FastAPI](https://fastapi.tiangolo.com/).

Foram feitas modificações para adequar a estrutura de pastas para um melhor uso a minha realidade. Sinta-se livre para sugerir melhorias e alterar essa estrutura para atender a realidade do seu projeto.

```bash
.
├── app
│   ├── dependencies
│   ├── domain
│   │   ├── exceptions
│   │   ├── models
│   │   │   └── tables
│   │   └── schemas
│   │       ├── request_schemas
│   │       └── response_schemas
│   ├── presentation
│   │   ├── exception_handlers
│   │   ├── middlewares
│   │   └── routes
│   ├── services
│   │   ├── connectors
│   │   ├── emails
│   │   └── repositories
│   │       ├── interfaces
│   │       └── sqlalchemy
│   └── usecases
├── config
├── database
│   └── migrations
├── scripts
├── storage
│   ├── app
│   └── logs
└── tests
```

<a name="app"></a>

### app

Pasta que contém o código principal da aplicação.

<a name="app-dependencies"></a>

### app/dependencies

Pasta que contém os arquivos que lidam com as dependências da aplicação.

Depends no FastAPI são funções que recebem uma dependência e retornam um valor. Eles são usados ​​para declarar dependências de outras funções.

Por exemplo, se você tiver uma função que precisa do usuário atualmente autenticado, você pode declarar uma dependência que receba o usuário atualmente autenticado e retorne o usuário.

Leia mais sobre [Depends](https://fastapi.tiangolo.com/tutorial/dependencies/).

<a name="app-domain"></a>

### app/domain

Pasta que contém as entidades e os objetos de valor da aplicação.

<a name="app-domain-exceptions"></a>

### app/domain/exceptions

Pasta que contém as exceções personalizadas da aplicação.

<a name="app-domain-models"></a>

### app/domain/models

Pasta que contém os modelos da aplicação.

Modelos são classes que representam as tabelas do banco de dados da aplicação. Eles são usados ​​para criar, ler, atualizar e excluir dados do banco de dados.

Leia mais sobre [Modelos](https://fastapi.tiangolo.com/tutorial/sql-databases/#models).

<a name="app-domain-models-tables"></a>

### app/domain/models/tables

Pasta que contém arquivos que são usados para criar tabelas intermediárias em relacionamentos muitos-para-muitos.

<a name="app-domain-schemas"></a>

### app/domain/schemas

Pasta que contém os esquemas da aplicação.

Esquemas são classes que representam os dados que são enviados e recebidos pela API. Eles são usados ​​para validar os dados que são enviados e recebidos pela API. Eles também são usados ​​para documentar a API.

Leia mais sobre [Esquemas](https://fastapi.tiangolo.com/tutorial/schema/).

<a name="app-domain-schemas-request_schemas"></a>

### app/domain/schemas/request_schemas

Pasta que contém os esquemas de solicitação da aplicação. Esquemas de solicitação são usados ​​para validar os dados que são enviados para a API.

<a name="app-domain-schemas-response_schemas"></a>

### app/domain/schemas/response_schemas

Pasta que contém os esquemas de resposta da aplicação. Esquemas de resposta são usados ​​para validar os dados que são recebidos da API.

<a name="app-presentation"></a>

### app/presentation

Pasta que contém o código de apresentação da aplicação. O código de apresentação é responsável por receber solicitações HTTP e enviar respostas HTTP. Ele também é responsável por lidar com erros e exceções.

<a name="app-presentation-exception_handlers"></a>

### app/presentation/exception_handlers

Pasta que contém os arquivos que lidam com os erros e exceções da aplicação.

Leia mais sobre [Tratamento de erros e exceções](https://fastapi.tiangolo.com/tutorial/handling-errors/).

<a name="app-presentation-middlewares"></a>

### app/presentation/middlewares

Pasta que contém os arquivos que lidam com os middlewares da aplicação. Middlewares são funções que são executadas antes de uma solicitação HTTP ser enviada para uma rota.

Leia mais sobre [Middlewares](https://fastapi.tiangolo.com/tutorial/middleware/).

<a name="app-presentation-routes"></a>

### app/presentation/routes

Pasta que contém os arquivos que lidam com as rotas da aplicação. Rotas são funções que são executadas quando uma solicitação HTTP é enviada para uma rota específica.

Leia mais sobre [Rotas](https://fastapi.tiangolo.com/tutorial/path-params/).

<a name="app-services"></a>

### app/services

Pasta que contém os arquivos que lidam com os serviços e infraestrutura da aplicação.

<a name="app-services-connectors"></a>

### app/services/connectors

Pasta que contém os arquivos que lidam com os conectores da aplicação. Conectores são classes que são usadas para se conectar a serviços externos.

<a name="app-services-emails"></a>

### app/services/emails

Pasta que contém os arquivos que lidam com os emails da aplicação. Emails são classes que são usadas para enviar emails.

<a name="app-services-repositories"></a>

### app/services/repositories

Pasta que contém os arquivos que lidam com os repositórios da aplicação. Repositórios são classes que são usadas para criar, ler, atualizar e excluir dados do banco de dados.

<a name="app-services-repositories-interfaces"></a>

### app/services/repositories/interfaces

Pasta que contém os arquivos que lidam com as interfaces dos repositórios da aplicação. Interfaces são classes que são usadas para definir os métodos que devem ser implementados pelos repositórios.

<a name="app-services-repositories-sqlalchemy"></a>

### app/services/repositories/sqlalchemy

Pasta que contém os arquivos que lidam com os repositórios do SQLAlchemy da aplicação. Repositórios do SQLAlchemy são classes que são usadas para criar, ler, atualizar e excluir dados do banco de dados usando o SQLAlchemy.

Leia mais sobre [SQLAlchemy](https://fastapi.tiangolo.com/tutorial/sql-databases/#sqlalchemy).

<a name="app-usecases"></a>

### app/usecases

Pasta que contém os arquivos que lidam com os casos de uso da aplicação. Casos de uso são classes que são usadas para executar a lógica da aplicação.

<a name="config"></a>

### config

Pasta que contém os arquivos de configuração da aplicação.

<a name="database"></a>

### database

Pasta que contém os arquivos que lidam com o banco de dados da aplicação.

<a name="database-migrations"></a>

### database/migrations

Pasta que contém os arquivos de migração do banco de dados da aplicação. Migrações são arquivos que são usados para criar, atualizar e excluir tabelas do banco de dados. Nesse projeto estamos usando o [Alembic](https://alembic.sqlalchemy.org/en/latest/).

<a name="scripts"></a>

### scripts

Pasta que contém os arquivos de scripts utilitários da aplicação.

<a name="tests"></a>

### tests

Pasta que contém os arquivos de testes da aplicação. Nesse projeto estamos usando o [Pytest](https://docs.pytest.org/en/stable/).

<a name="storage"></a>

### storage

Pasta que contém arquivos gerados pela aplicação. Os arquivos gerados não são versionados no Git.

<a name="storage-app"></a>

### storage/app

Pasta que contém arquivos gerados pela aplicação.

<a name="storage-logs"></a>

### storage/logs

Pasta que contém os arquivos de log da aplicação.

<a name="tests"></a>

### tests

Pasta que contém os arquivos de testes da aplicação. Nesse projeto estamos usando o [Pytest](https://docs.pytest.org/en/stable/).

### utils

Pasta que contém os arquivos de utilitários da aplicação. Contém funções ou classes que são utilizadas em toda a aplicação, mas não se encaixam em nenhuma das outras camadas.
