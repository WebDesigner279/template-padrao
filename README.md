# 🌐 Estrutura Base - Next.js + TypeScript + Docker
> 🚀 Base moderna, escalável e pronta para produção com Next.js 14+, SCSS, PWA, Docker e Docker Compose

<p align="center">
  <img src="https://a.imagem.app/BKaHX1.png" alt="Banner Estrutura Base Next.js" style="max-width: 100%; height: auto;" />
</p>

## 📚 Sumário

- [✨ Funcionalidades](#-funcionalidades)
- [✅ Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [📁 Estrutura de Pastas](#-estrutura-de-pastas)
- [🐳 Docker e Docker Compose](#-docker-e-docker-compose)
- [🚀 Como Executar o Projeto](#-como-executar-o-projeto)
- [⚙️ Scripts Disponíveis](#️-scripts-disponíveis)
- [📦 Deploy](#-deploy)
- [📱 Suporte a PWA](#-suporte-a-pwa)
- [✍️ Estilização](#️-estilização)
- [💡 Boas Práticas](#-boas-práticas)
- [📄 Licença](#-licença)
- [👨‍💻 Autor](#-autor)

---

![Next.js](https://img.shields.io/badge/Next.js-14+-black?logo=nextdotjs)
![TypeScript](https://img.shields.io/badge/TypeScript-4.x-blue?logo=typescript)
![SCSS Modules](https://img.shields.io/badge/SCSS-Modules-pink?logo=sass)
![Docker](https://img.shields.io/badge/Docker-Containers-blue?logo=docker)
![PWA Ready](https://img.shields.io/badge/PWA-Ready-green?logo=googlechrome)
![MIT License](https://img.shields.io/badge/license-MIT-brightgreen)

---

## ✨ Funcionalidades

- ✅ Next.js 14+ com suporte nativo a App Router
- ✅ Suporte completo a PWA (offline, instalação mobile e desktop)
- ✅ Componentização com SCSS Modules
- ✅ SEO otimizado
- ✅ Docker e Docker Compose configurados para desenvolvimento e produção
- ✅ Deploy simples na Vercel ou qualquer plataforma compatível com Docker
- ✅ Estrutura limpa, escalável e de fácil manutenção

---

## ✅ Tecnologias Utilizadas

- ⚙️ [Next.js 14+](https://nextjs.org/)
- ⚛️ [React](https://react.dev/)
- 📘 [TypeScript](https://www.typescriptlang.org/)
- 🎨 [SCSS Modules](https://sass-lang.com/)
- 🐳 [Docker](https://www.docker.com/)
- 🐙 [Docker Compose](https://docs.docker.com/compose/)
- 🔥 [PWA](https://web.dev/progressive-web-apps/)
- 🛠️ [ESLint + Prettier](https://prettier.io/)

---

## 📁 Estrutura de Pastas

```bash
estrutura-base-1/
│
├── .dockerignore                       # Arquivos ignorados no build Docker
├── docker-compose.dev.yml              # Compose para ambiente de desenvolvimento
├── docker-compose.prod.yml             # Compose para ambiente de produção
├── Dockerfile                          # Dockerfile para produção
├── Dockerfile.dev                      # Dockerfile para desenvolvimento
│
├── .next/                              # Pasta gerada automaticamente (ignorada no Git)
├── .vscode/                            # Configurações do VSCode (opcional)
│
├── app/
│   ├── components/
│   │   ├── Footer/
│   │   │   ├── Footer.module.scss
│   │   │   ├── Footer.tsx
│   │   │   └── index.ts
│   │   ├── InstallButton/
│   │   │   ├── InstallButton.module.scss
│   │   │   ├── InstallButton.tsx
│   │   │   └── index.tsx
│   │   ├── Navbar/
│   │   │   ├── Navbar.module.scss
│   │   │   ├── Navbar.tsx
│   │   │   └── index.ts
│   ├── contato/
│   │   ├── Contato.module.scss
│   │   └── page.tsx
│   ├── home/
│   │   ├── Home.module.scss
│   │   └── page.tsx
│   ├── sobre/
│   │   ├── Sobre.module.scss
│   │   └── page.tsx
│   ├── styles/
│   │   └── globals.scss
│   └── layout.tsx
│
├── public/
│   ├── icons/
│   ├── images/
│   ├── manifest.json
│   ├── sw.js
│   ├── sw.js.map
│   ├── workbox-e43f5367.js
│   └── workbox-e43f5367.js.map
│
├── next-env.d.ts
├── next.config.js
├── package-lock.json
├── package.json
├── README.md
├── tsconfig.json
└── .gitignore
```

---

🐳 Docker e Docker Compose

🔧 Arquivos Docker
Dockerfile.dev → Ambiente de desenvolvimento (hot reload)

Dockerfile → Build de produção otimizado

.dockerignore → Evita subir arquivos desnecessários

docker-compose.dev.yml → Orquestração local para desenvolvimento

docker-compose.prod.yml → Orquestração local ou deploy em produção

▶️ Executar com Docker
Ambiente de Desenvolvimento:

```bash  
docker compose -f docker-compose.dev.yml up --build
```
Acesse em: http://localhost:3000

---

Ambiente de Produção (Local ou Deploy):

```bash
docker compose -f docker-compose.prod.yml up --build
```

---

🚀 Build Manual com Docker (Produção):

```bash 
docker build -t nextjs-app .
docker run -d -p 3000:3000 nextjs-app
```
---

🚀 Como Executar o Projeto (Sem Docker)

1️⃣ Clone o projeto

```bash
git clone https://github.com/seu-usuario/estrutura-base-1.git
cd estrutura-base-1
```
---

2️⃣ Instale as dependências

```bash
npm install
# ou
yarn
```
---

3️⃣ Rode em desenvolvimento

```bash
npm run dev
# ou
yarn dev
```
Acesse: http://localhost:3000

---

⚙️ Scripts Disponíveis

| Comando  | Descrição                            |
| -------- | ------------------------------------ |
| `dev`    | Inicia o ambiente de desenvolvimento |
| `build`  | Cria a build de produção             |
| `start`  | Roda a build em ambiente de produção |
| `lint`   | Executa o ESLint                     |
| `format` | Formata o código com Prettier        |

---

📦 Deploy

✅ Vercel (Recomendado)
Projeto 100% compatível com deploy na Vercel

Detecta automaticamente Next.js, sem necessidade de configuração extra

✅ Deploy via Docker
Servidores como AWS, Railway, Render, GCP, DigitalOcean, Heroku, etc.

Utilize docker-compose.prod.yml ou Dockerfile para ambientes de produção

---

📱 Suporte a PWA

✅ manifest.json configurado

✅ sw.js e workbox operando

✅ Permite instalação como app mobile e desktop

✅ Funciona offline

---

✍️ Estilização

🎨 SCSS Modules com escopo isolado por componente

🎨 Arquivo global: app/styles/globals.scss

---

💡 Boas Práticas

🔥 Componentização limpa

🚀 SEO-ready

📦 Deploy simplificado (Vercel ou Docker)

🔧 ESLint + Prettier

🐳 Containers isolados para desenvolvimento e produção

🔥 Arquivo .dockerignore otimizado para reduzir imagem Docker

---

📄 Licença

Este projeto está sob a licença MIT License.

---

👨‍💻 Autor

Valter Vieira Gomes Junior

💼 Desenvolvedor Front-End

📧 valtervieira.dev@gmail.com

🌐 portfolio-valter-dev.vercel.app

📱 WhatsApp: (11) 9 7756-7993