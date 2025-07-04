# teste_codex

Este repositório contém um exemplo simples de uma API em Laravel utilizando
SQLite como banco de dados. A aplicação oferece duas rotas para teste e pode
ser executada facilmente em um contêiner Docker.

## Como executar

```bash
docker build -t laravel-api .
docker run --rm -p 8000:8000 laravel-api
```

Após a inicialização, a aplicação ficará disponível em `http://localhost:8000`.

### Endpoints

- `GET /api/items` - lista os itens cadastrados
- `POST /api/items` - cria um novo item
