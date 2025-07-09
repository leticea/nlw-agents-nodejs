# NLW Agents

Projeto desenvolvido durante o evento NLW da **Rocketseat** utilizando tecnologias modernas para criação de uma API robusta e eficiente.

- [Front-end - Web](https://github.com/leticea/nlw-agents-react)

## 🚀 Tecnologias

- [Node.js](https://nodejs.org/en/) - v22.16.0
- [Npm](https://www.npmjs.com/) - 10.8.1
- [TypeScript](https://www.typescriptlang.org/) - ~5.8.3
- [Fastify](https://www.fastify.io/) - ^5.4.0
- [PostgreSQL](https://www.npmjs.com/package/postgres) - ^6.5.0
- [Drizzle ORM](https://www.npmjs.com/package/drizzle-orm) - ^6.5.0
- [Zod](https://zod.dev/) - ^3.25.76
- [Docker](https://www.docker.com/get-started/) - ^3.24.2

## 🏗️ Arquitetura

O projeto segue uma arquitetura modular com:

- **Separação de responsabilidades** entre rotas, schemas e conexão com banco
- **Validação de schemas** com Zod para type safety
- **ORM type-safe** com Drizzle para operações de banco de dados
- **Validação de variáveis de ambiente** centralizadas

## ⚙️ Setup e Configuração

### Pré-requisitos

- Node.js (versão com suporte a `--experimental-strip-types`)
- Docker e Docker Compose

### 1. Clone o repositório

```bash
git clone <url-do-repositorio>
cd server
```

### 2. Configure o banco de dados

```bash
docker-compose up -d
```

### 3. Configure as variáveis de ambiente

Crie um arquivo `.env` na raiz do projeto:

```env
PORT=3333
DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
```

### 4. Instale as dependências

```bash
npm install
```

### 5. Execute as migrações do banco

```bash
npx drizzle-kit migrate
```

### 6. (Opcional) Popule o banco com dados de exemplo

```bash
npm run db:seed
```

### 7. Execute o projeto

**Desenvolvimento:**

```bash
npm run dev
```

**Produção:**

```bash
npm start
```

## 📚 Scripts Disponíveis

- `npm run dev` - Executa o servidor em modo de desenvolvimento com hot reload
- `npm start` - Executa o servidor em modo de produção
- `npm run db:seed` - Popula o banco de dados com dados de exemplo

## 🌐 Endpoints

A API estará disponível em `http://localhost:3333`

- `GET /health` - Health check da aplicação
- `GET /rooms` - Lista as salas disponíveis

---

Desenvolvido com ❤️ durante o NLW da Rocketseat
