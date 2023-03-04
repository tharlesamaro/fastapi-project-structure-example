## Sugestão de estrutura de pastas para um projeto FastAPI

Se você está iniciando um novo projeto com FastAPI, uma estrutura de pastas adequada pode ajudá-lo a organizá-lo de forma eficiente. Abaixo está uma sugestão de estrutura de pastas que pode ser usada em projetos FastAPI:

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

Clique [aqui](STRUCTURE.md) para ver a estrutura de pastas em detalhes.

Lembre-se de que essa é apenas uma sugestão e você pode modificar a estrutura de pastas de acordo com as necessidades do seu projeto. Além disso, o uso de uma estrutura de pastas não é obrigatório e você pode usar o FastAPI em qualquer estrutura de pastas que desejar, incluindo projetos que usam apenas um único arquivo Python.

Por fim, observe que este repositório é apenas um exemplo de como organizar uma árvore de pastas de projeto FastAPI, e não contém exemplos de código.

Espero que isso ajude você a organizar seu projeto FastAPI de forma eficiente.