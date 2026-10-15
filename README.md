# 🐉 App Dragon Ball Next

Aplicação web feita com **React + TypeScript + Vite** que consome a **Dragon Ball API** para exibir personagens e planetas do universo. A interface foi construída com **PrimeReact** e o projeto está preparado para produção com **Docker + NGINX**.

---

## 🚀 Tecnologias Utilizadas

- [React](https://reactjs.org/)
- [TypeScript](https://www.typescriptlang.org/)
- [Vite](https://vitejs.dev/)
- [PrimeReact](https://primereact.org/)
- [PrimeIcons](https://primefaces.org/primeicons/)
- [Axios](https://axios-http.com/)
- [Docker](https://www.docker.com/)
- [NGINX](https://www.nginx.com/)

---

## 📷 Demonstração

```bash
Acesse: http://localhost:5173 (localmente via Vite ou após rodar o contêiner Docker)
```

---

## ⚙️ Instalação Local

### Pré-requisitos

- [Node.js](https://nodejs.org/) (versão 18 ou superior)
- npm

### Passos

```bash
# Clone o repositório
git clone https://github.com/odavid062/app-dragon-ball-next-main.git

# Acesse a pasta
cd app-dragon-ball-next-main

# Instale as dependências
npm install

# Inicie o servidor de desenvolvimento
npm run dev
```

### 📜 Scripts Disponíveis

- `npm run dev`: Inicia o servidor de desenvolvimento local com Vite.
- `npm run build`: Executa a verificação de tipos com TypeScript (`tsc -b`) e compila para produção (`vite build`).
- `npm run lint`: Executa a análise estática de código com ESLint.
- `npm run preview`: Inicia o servidor local para pré-visualização da build de produção.

---

## 🐳 Docker

### ✅ Build da imagem
```bash
docker build -t dragon-ball-app .
```

### ✅ Execução da imagem
```bash
docker run -d -p 5173:80 dragon-ball-app
```

### 🌐 Acesse:
```
http://localhost:5173
```

---

## 📁 Estrutura de Pastas

```
src/
├── assets/              # Recursos estáticos (ex.: SVG do React)
├── character/           # Modelos e interfaces TypeScript dos personagens
├── components/          # Diretório para componentes compartilhados
├── planets/             # Componentes e tipos de planetas (PlanetsTable.tsx, planets.ts)
├── service/             # Serviços de requisição com Axios (personagens e planetas)
├── App.tsx              # Componente principal com tabela de personagens
├── index.css            # Estilos globais e utilitários de layout
├── main.tsx             # Ponto de entrada da aplicação e estilos do PrimeReact
```

---

## 🧱 Dockerfile multi-stage

A imagem foi construída com duas etapas:

1. **Build (Node 18 Alpine)**: Compila o projeto com `npm run build` (`tsc -b && vite build`)
2. **Produção (NGINX)**: Serve a aplicação estática via `/usr/share/nginx/html`

---

## 📄 Licença

Este projeto está licenciado sob a **MIT License**.

---

## 🤝 Contribuindo

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests.

---

Feito  por [odavid062](https://github.com/odavid062)
