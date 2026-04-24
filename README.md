# pymangify
API Rest  para um leitor de mangas e similares

## Estrutura de Diretórios

O projeto segue a seguinte estrutura de diretórios, separando as responsabilidades para garantir escalabilidade e manutenibilidade:

```text
pymangify/
├── app/                      # Diretório principal da aplicação
│   ├── __init__.py
│   ├── main.py               # Ponto de entrada do FastAPI
│   ├── api/                  # Lógica de roteamento da API
│   │   ├── __init__.py
│   │   ├── dependencies/     # Dependências injetáveis do FastAPI (auth, sessões DB, etc.)
│   │   │   └── __init__.py
│   │   └── endpoints/        # Rotas divididas por domínio/recurso (ex: users.py, mangas.py)
│   │       └── __init__.py
│   ├── core/                 # Configurações gerais, variáveis de ambiente e segurança
│   │   └── __init__.py
│   ├── crud/                 # Operações de CRUD no banco de dados
│   │   └── __init__.py
│   ├── db/                   # Configuração do banco de dados (engine, session, base)
│   │   └── __init__.py
│   ├── models/               # Modelos SQLAlchemy (ORM)
│   │   └── __init__.py
│   ├── schemas/              # Schemas Pydantic (validação de entrada/saída)
│   │   └── __init__.py
│   └── services/             # Lógica de negócio e serviços auxiliares
│       └── __init__.py
├── tests/                    # Testes automatizados
│   ├── __init__.py
│   ├── api/                  # Testes de integração das rotas
│   │   └── __init__.py
│   └── crud/                 # Testes das operações de CRUD
│       └── __init__.py
├── docs/                     # Documentação adicional do projeto
├── scripts/                  # Scripts utilitários (seed, migrations, etc.)
├── .env                      # Variáveis de ambiente (não versionado)
├── .env.example              # Exemplo de variáveis de ambiente
├── .gitignore
├── docker-compose.yml        # Compose para serviços locais (PostgreSQL)
├── pyproject.toml            # Configuração do projeto e dependências
└── README.md
```
