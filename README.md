
# 🚀 API Node.js
![Node.js](https://img.shields.io/badge/Node.js-18.x-green?logo=node.js)
![Fastify](https://img.shields.io/badge/Fastify-5.x-black?logo=fastify)
![Docker](https://img.shields.io/badge/Docker-🐳-blue)

API desenvolvida com **Node.js + Fastify** para estudos e prática de desenvolvimento backend, incluindo autenticação JWT, integração com banco de dados PostgreSQL usando **Drizzle ORM**, testes automatizados com **Vitest** e documentação via Swagger.

💡 O projeto também inclui um arquivo [`requests.http`](requests.http) para testar requisições diretamente no **VS Code** usando a extensão [REST Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client).

## ⚙️ Pré-requisitos
- [Node.js 18+](https://nodejs.org/)
- [Docker](https://www.docker.com/)
- [npm](https://www.npmjs.com/)

## 📦 Instalação
```bash
# Clonar repositório
git clone https://github.com/lucas-bardeli/api-nodejs.git

# Entrar na pasta
cd api-nodejs

# Instalar dependências
npm install
```

## 🚀 Rodando o Projeto

### Modo desenvolvimento
```bash
npm run dev
```

### Executar seeds no banco
```bash
npm run db:seed
```

## 🐳 Rodando com Docker
```bash
# Subir containers
docker-compose up --build

# Derrubar containers
docker-compose down

# Iniciar containers já existentes
docker compose start

# Parar containers sem remover
docker compose stop
```

Isso irá subir:
- **API** (Node.js + Fastify)
- **PostgreSQL** (Banco de dados)
- **Drizzle Studio** (Interface para o banco)

## 🛠️ Scripts Disponíveis
| Script                              | Descrição |
|-------------------------------------|-----------|
| `npm run dev`                       | Rodar a API em modo desenvolvimento |
| `npm run db:generate`               | Gerar migrações do banco a partir do schema |
| `npx drizzle-kit generate --custom` | Gerar migração customizada manualmente |
| `npm run db:migrate`                | Rodar migrações no banco |
| `npm run db:studio`                 | Abrir interface do Drizzle Studio |
| `npm run db:seed`                   | Popular banco com dados iniciais |
| `npm test`                          | Rodar testes automatizados |

## 📡 Rotas Principais
- `POST /login` — Autenticação de usuários
- `POST /courses` — Criar um novo curso
- `GET /courses` — Listar cursos
- `GET /courses/:id` — Buscar curso por ID

#### Documentação Swagger disponível em `/docs` quando a API está rodando.

## 🧪 Testes
```bash
npm test
```

Utiliza **Vitest** + **Supertest** para testes de integração.

## 🛠️ Tecnologias Utilizadas
- **Node.js**
- **Fastify**
- **Drizzle ORM**
- **PostgreSQL**
- **Docker**
- **Vitest**
- **Swagger**