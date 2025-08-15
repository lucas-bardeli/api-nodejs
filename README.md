
# 🚀 API Node.js
![Node.js](https://img.shields.io/badge/Node.js-18.x-green?logo=node.js)
![Fastify](https://img.shields.io/badge/Fastify-5.x-black?logo=fastify)
![Docker](https://img.shields.io/badge/Docker-🐳-blue)
![Status](https://img.shields.io/badge/status-Em_desenvolvimento-yellow)

API desenvolvida com **Node.js + Fastify** para estudos e prática de desenvolvimento backend, incluindo autenticação JWT, integração com banco de dados PostgreSQL usando **Drizzle ORM**, testes automatizados com **Vitest** e documentação via Swagger.

## 📂 Estrutura do Projeto
```
.
├── docker-compose.yml       # Configuração dos serviços Docker
├── Dockerfile               # Build da aplicação
├── drizzle.config.ts        # Configuração do Drizzle ORM
├── package.json             # Dependências e scripts
├── src/
│   ├── app.ts               # Configuração do servidor Fastify
│   ├── server.ts            # Inicialização da API
│   ├── database/            # Conexão, schema e seed
│   ├── routes/              # Rotas da aplicação
│   └── @types/              # Tipos TypeScript
└── tests/                   # Testes automatizados
```
## ⚙️ Pré-requisitos
- [Node.js 18+](https://nodejs.org/)
- [Docker](https://www.docker.com/)
- [npm](https://www.npmjs.com/) ou [yarn](https://yarnpkg.com/)

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
```

Isso irá subir:
- **API** (Node.js + Fastify)
- **PostgreSQL** (Banco de dados)
- **Drizzle Studio** (Interface para o banco)

## 🛠️ Scripts Disponíveis
| Script              | Descrição |
|---------------------|-----------|
| `npm run dev`       | Rodar a API em modo desenvolvimento |
| `npm run db:seed`   | Popular banco com dados iniciais |
| `npm run db:migrate`| Rodar migrações no banco |
| `npm run db:studio` | Abrir interface do Drizzle Studio |
| `npm test`          | Rodar testes automatizados |

## 📡 Rotas Principais
- `POST /login` — Autenticação de usuários
- `POST /courses` — Criar um novo curso
- `GET /courses` — Listar cursos
- `GET /courses/:id` — Buscar curso por ID

> Documentação Swagger disponível em `/docs` quando a API está rodando.

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
