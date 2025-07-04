# teste_codex

Este repositório contém um exemplo simples de uma API em Laravel utilizando
SQLite como banco de dados e preparada para execução em Docker.

## Como executar

```bash
docker build -t laravel-api .
docker run --rm -p 8000:8000 laravel-api
```

A aplicação ficará disponível em `http://localhost:8000`.
