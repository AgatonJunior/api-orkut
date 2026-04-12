# Documentação da API

# 🌐 Api Orkut

API RESTful desenvolvida com **Node.js**, **Express** e **PostgreSQL**, criada com o objetivo de demonstrar na prática a construção de um backend completo, do zero até um padrão próximo do mercado.

---

## 🚀 Funcionalidades

- 🔐 Autenticação com **JWT**
- 🔒 Senhas seguras com **bcrypt**
- 📝 **CRUD completo** de posts
- 👥 Relacionamento entre **usuários e posts**
- ✅ Validação de dados com **Joi**

---

## 🛠️ Tecnologias

| Tecnologia | Descrição |
|---|---|
| Node.js | Runtime JavaScript no servidor |
| Express | Framework web para Node.js |
| PostgreSQL | Banco de dados relacional |
| JWT | Autenticação via token |
| bcrypt | Hash seguro de senhas |
| Joi | Validação de dados |

---

## 📦 Instalação

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/api-orkut.git

# Entre na pasta do projeto
cd api-orkut

# Instale as dependências
npm install
```

---

## ⚙️ Variáveis de Ambiente

Crie um arquivo `.env` na raiz do projeto com as seguintes variáveis:

```env
DATABASE_URL=postgresql://usuario:senha@host:porta/banco
JWT_SECRET=sua_chave_secreta
PORT=3000
```

---

## ▶️ Como rodar

```bash
# Modo desenvolvimento
npm run dev

# Modo produção
npm start
```

---

## 🌍 Base URL

```
https://api-orkut-3318.onrender.com
```

---

## 📋 Endpoints

### Usuários

| Método | Rota | Descrição | Auth |
|---|---|---|---|
| `POST` | `/usuarios` | Cadastrar novo usuário | ❌ |
| `GET` | `/usuarios` | Listar todos os usuários | ❌ |
| `POST` | `/login` | Autenticar usuário e obter token | ❌ |

### Posts

| Método | Rota | Descrição | Auth |
|---|---|---|---|
| `GET` | `/posts` | Listar todos os posts | ❌ |
| `POST` | `/posts` | Criar novo post | ✅ |
| `PUT` | `/posts/:id` | Atualizar post | ✅ |
| `DELETE` | `/posts/:id` | Deletar post | ✅ |

> ✅ Requer token JWT no header: `Authorization: Bearer <token>`

---

## 🔑 Autenticação

As rotas protegidas exigem um token JWT no header da requisição:

```http
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...
```

Para obter o token, faça login em `POST /login` com email e senha.

---

## 📚 Documentação completa

Consulte o arquivo `API_REFERENCE.md` para ver exemplos detalhados de requisições e respostas de cada endpoint.

---

## 💡 Proposta do Projeto

Este projeto serve como **base de aprendizado para iniciantes**, evoluindo passo a passo até um padrão mais próximo do mercado. Ideal para quem quer entender como um backend real é construído e estruturado.

---

## 👨‍💻 Autor - Agaton Junior

Desenvolvido durante aula prática de deploy e backend com Node.js.

