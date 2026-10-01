# 🚀 Guia Prático: Estrutura React e Principais Bibliotecas

Este guia foi criado para ensinar de forma simples e direta como estruturar um projeto moderno em **React** utilizando **Vite**, além de apresentar as bibliotecas mais importantes do ecossistema front-end.

---

## 📌 1. Como Criar essa Estrutura do Zero

## Passo 1: Pré-requisito

Certifique-se de ter o **Node.js** instalado na sua máquina (versão 18 ou superior).  
Você pode verificar abrindo o terminal e digitando:

```bash

node -v
npm -v
```

### Passo 2: Criar o Projeto com Vite

O [Vite](https://vitejs.dev/) é a ferramenta padrão e mais veloz da atualidade para criar projetos React. No terminal, execute:

```bash

npm create vite@latest nome-do-projeto -- --template react
```

### Passo 3: Acessar a pasta e instalar dependências

```bash
cd nome-do-projeto
npm install
```

### Passo 4: Rodar o projeto localmente

```bash
npm run dev
```

O terminal exibirá um link local (geralmente `http://localhost:5173/`). Ao abrir esse link no navegador, sua aplicação React já estará funcionando em tempo real!

---

## 📂 2. Entendendo a Arquitetura de Pastas

Organizar o projeto em pastas bem definidas evita bagunça e faz seu código crescer de forma limpa e profissional:

```text
meu-portfolio/
├── public/                 # Arquivos públicos estáticos (ex: favicon, robots.txt)
├── src/                    # Código-fonte da aplicação
│   ├── assets/             # Imagens, vetores SVG e mídias visuais
│   ├── components/         # Blocos visuais reutilizáveis (Navbar, Footer, Card, Botão)
│   ├── hooks/              # Custom Hooks (funções de lógica React reutilizável)
│   ├── pages/              # Telas inteiras ou seções principais (Home, Sobre, Contato)
│   ├── services/           # Comunicação com APIs, bancos ou dados simulados
│   ├── styles/             # Estilos globais, temas e variáveis de cores
│   ├── utils/              # Funções utilitárias puras (formatar moeda, datas, etc.)
│   ├── App.jsx             # Componente raiz que orquestra a aplicação
│   ├── index.css           # Estilos globais e resets CSS
│   └── main.jsx            # Ponto de entrada que conecta o React ao HTML
├── index.html              # HTML base onde o React injeta o conteúdo
├── package.json            # Lista de dependências e comandos do projeto
└── vite.config.js          # Configurações do Vite
```

### Para que serve cada pasta de `src/`

| Pasta | Descrição | Exemplo |

|---|---|---|

| **`components/`** | Pedaços visuais isolados que podem ser usados em vários lugares. | `Navbar.jsx`, `Footer.jsx`, `ProjectCard.jsx` |
| **`pages/`** | Visualizações completas compostas por componentes. | `Home.jsx`, `Projects.jsx` |
| **`hooks/`** | Encapsula comportamentos React (como detecção de scroll ou tema). | `useScrollPosition.js`, `useTheme.js` |
| **`services/`** | Funções para buscar ou enviar dados para um servidor. | `api.js`, `githubService.js` |
| **`styles/`** | Paleta de cores, tipografia e regras visuais globais. | `theme.css` |
| **`utils/`** | Funções simples do JavaScript sem interface gráfica. | `formatters.js`, `validators.js` |

---

## 📚 3. Principais Bibliotecas para Desenvolver em React

Aqui estão as bibliotecas mais usadas pelo mercado para enriquecer qualquer projeto:

### 🎨 1. Ícones e Visual

* **`lucide-react`** *(já instalada no seu projeto)*:
  * Biblioteca com centenas de ícones modernos, leves e fáceis de customizar.
  * **Comando:** `npm install lucide-react`
  * **Exemplo de uso:**

    ```jsx
    import { Code2, ExternalLink } from 'lucide-react';
    <Code2 size={24} color="#6366f1" />
    ```

* **`react-icons`**:
  * Reúne ícones de diversos pacotes famosos (FontAwesome, Material Design, Feather, etc.).
  * **Comando:** `npm install react-icons`

---

### 🗺️ 2. Navegação de Páginas (Roteamento)

* **`react-router-dom`**:
  * Essencial se você quiser que sua aplicação tenha várias rotas com URLs diferentes (ex: `/`, `/sobre`, `/contato`) sem recarregar a página.
  * **Comando:** `npm install react-router-dom`
  * **Exemplo:**

    ```jsx
    import { BrowserRouter, Routes, Route } from 'react-router-dom';
    // Permite navegar entre páginas instantaneamente (SPA - Single Page Application)
    ```

---

### 💅 3. Estilização Moderna

* **`Tailwind CSS`**:
  * O framework de CSS mais popular do mundo. Permite estilizar escrevendo classes utilitárias diretamente nos elementos HTML/JSX (`className="flex justify-between p-4 bg-slate-900"`).
* **`styled-components`**:
  * Escreve estilos CSS diretamente dentro de componentes JavaScript com suporte a propriedades dinâmicas.
  * **Comando:** `npm install styled-components`

---

### ✨ 4. Animações e Transições

* **`framer-motion`**:
  * A melhor biblioteca de animação para React. Permite criar efeitos suaves de fade, arrastar, menus que abrem e animações ao rolar a página.
  * **Comando:** `npm install framer-motion`
  * **Exemplo:**

    ```jsx

    import { motion } from 'framer-motion';
    <motion.div initial={{ opacity: 0 }} animate={{ opacity: 1 }}>Olá!</motion.div>
    ```

---

### 🌐 5. Requisições e Integrações com APIs

* **`axios`**:
  * Cliente HTTP simples para consumir dados de APIs (como dados do GitHub, formulários, etc.).
  * **Comando:** `npm install axios`
* **`@tanstack/react-query`**:
  * Gerencia o carregamento de dados remotos, cache automático e atualizações de tela sem esforço.

---

### 🧠 6. Gerenciamento de Estado Global

* **`zustand`**:
  * Biblioteca super leve e intuitiva para compartilhar dados entre vários componentes sem precisar passar propriedades de pai para filho (prop drilling).
  * **Comando:** `npm install zustand`

---

## ⚡ 4. Comandos Essenciais do Projeto

No terminal dentro da pasta do projeto:

| Comando | O que faz |

|---|---|
| `npm run dev` | Inicia o servidor de desenvolvimento com **Hot Reload** (as alterações no código aparecem instantaneamente no navegador). |
| `npm run build` | Cria a pasta otimizada e minificada `dist/` pronta para ser hospedada na Vercel, Netlify ou GitHub Pages. |
| `npm run preview` | Permite testar no seu navegador a versão final compilada de produção. |

---

## 💡 Dica para o seu Portfólio

Você já tem uma base sólida criada e configurada com:

-- Componentes organizados (`Navbar`, `Hero`, `ProjectCard`, `Footer`).

-- Custom hook de scroll implementado (`useScrollPosition`).

-- Camada de dados mockados em `services/api.js`.

-- Estilização com variáveis globais em `src/styles/theme.css`.

Agora basta editar os textos, adicionar seus projetos e personalizar as cores para ter um portfólio incrível no ar! 🚀
