# GamerStore 🎮🛒

<p align="center">
  <img src="https://raw.githubusercontent.com/Whuanderson/GamerStore/refs/heads/main/public/logo.png" alt="GamerStore logo" height="120"/>
</p>

<p align="center">
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/Whuanderson/GamerStore">
  <a href="https://www.linkedin.com/in/whuanderson-de-sousa-porto-marinho-a07204216/" target="_blank">
    <img alt="Made by Whuanderson" src="https://img.shields.io/badge/Made%20by-Whuanderson-blue">
  </a>
  <img alt="License" src="https://img.shields.io/badge/License-MIT-blue">
</p>

Monorepo **full‑stack** para um e‑commerce de jogos digitais.  
Backend, frontend web e app mobile vivem no mesmo repositório graças ao **Turborepo**, compartilhando pacotes de UI, configuração e lógica.

---

## 📸 Visão Geral

  <img src="https://raw.githubusercontent.com/Whuanderson/GamerStore/refs/heads/main/.github/a1.png" width="410" alt="Home" />  
  <img src="https://raw.githubusercontent.com/Whuanderson/GamerStore/refs/heads/main/.github/a2.png" width="410" alt="Catálogo" />
  <img src="https://raw.githubusercontent.com/Whuanderson/GamerStore/refs/heads/main/.github/a3.png" width="410" alt="Carrinho" />

---

## 🗂️ Estrutura

```
.
├─ apps
│  ├─ backend    # API NestJS + Prisma
│  ├─ frontend   # Web Next.js
│  └─ mobile     # React Native (Expo)
├─ packages
│  ├─ ui         # biblioteca de componentes
│  ├─ config     # ESLint, TSConfig, etc.
│  └─ hooks      # hooks compartilhados
└─ turbo.json    # pipeline Turborepo
```

---

## ✨ Funcionalidades

- **Catálogo** de jogos com categorias, busca e filtros  
- **Carrinho** e cálculo de frete/impostos  
- **Checkout** com Stripe  
- **Autenticação** JWT + refresh token  
- **Painel admin** para produtos e pedidos  
- **Sincronização** em tempo real via WebSocket  
- **Design system** compartilhado entre web & mobile  

---

## 🚀 Tecnologias

| Camada   | Stack |
|----------|-------|
| **Backend** | NestJS · Prisma ORM · PostgreSQL · Zod · Swagger |
| **Frontend** | Next.js 14 · React 18 · TypeScript · TailwindCSS · TanStack Query |
| **Mobile** | React Native (Expo) · TypeScript · NativeWind · Zustand |
| **Infra** | Turborepo · Docker Compose · Husky & lint‑staged |

---

## 💻 Executando localmente

> Requer **Node.js 18+** e **Yarn** (workspaces) ou **pnpm**.

```bash
git clone https://github.com/Whuanderson/GamerStore
cd GamerStore

# instalar dependências de todos os workspaces
yarn             # ou pnpm install
```

### Iniciar com Turborepo

```bash
yarn turbo run dev   # inicia backend, web e mobile em paralelo
```

### Iniciar manualmente

```bash
# API
cd apps/backend
yarn dev            # http://localhost:3333

# Web
cd ../../apps/frontend
yarn dev            # http://localhost:3000

# Mobile
cd ../../apps/mobile
npx expo start
```

> Configure variáveis de ambiente em `apps/*/.env.example` antes de iniciar.

---

## 📝 Licença

Distribuído sob **MIT**. Veja [LICENSE](./LICENSE) para detalhes.

<p align="center">
  Feito por <a href="https://github.com/Whuanderson">Whuanderson Marinho</a> — deixe uma ⭐️ se este projeto te ajudou!
</p>
