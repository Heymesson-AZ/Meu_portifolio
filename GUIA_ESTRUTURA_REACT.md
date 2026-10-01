# 🚀 Guia Simples: Estrutura React e Principais Bibliotecas

Este guia foi feito de forma direta e prática para você entender:
1. Como criar a estrutura do projeto do zero no terminal.
2. O que é e para que serve cada pasta criada.
3. Quais são as principais bibliotecas, como instalar e o que cada uma faz.
4. Os comandos básicos para rodar o projeto.

---

## 🛠️ 1. Comandos de Instalação (Passo a Passo)

Abra o terminal na pasta onde deseja criar o projeto e siga os passos abaixo:

### Passo 1: Criar o projeto React com Vite
O **Vite** é a ferramenta padrão e mais rápida para projetos React modernos.
```bash
npm create vite@latest meu-portfolio -- --template react
```
* **O que esse código faz:** Cria uma nova pasta chamada `meu-portfolio` já com o React configurado.

---

### Passo 2: Entrar na pasta do projeto
```bash
cd meu-portfolio
```
* **O que esse código faz:** Entra na pasta do seu projeto para executar os próximos comandos no lugar certo.

---

### Passo 3: Criar as pastas da estrutura organizada
No terminal do Windows (PowerShell), execute:
```powershell
mkdir src\components, src\pages, src\hooks, src\services, src\styles, src\utils
```
* **O que esse código faz:** Cria as 6 pastas recomendadas dentro de `src/` para manter o código limpo, separado e profissional.

---

### Passo 4: Instalar as dependências base
```bash
npm install
```
* **O que esse código faz:** Baixa e instala todos os pacotes essenciais do React para que o projeto possa funcionar no seu computador.

---

### Passo 5: Instalar as principais bibliotecas do ecossistema
Execute este comando para instalar as bibliotecas mais importantes:
```bash
npm install lucide-react react-router-dom axios
```
* **O que esse código faz:** Instala 3 ferramentas muito usadas:
  * `lucide-react`: ícones modernos e prontos para usar.
  * `react-router-dom`: permite ao site ter várias páginas/rotas (ex: `/sobre`, `/projetos`).
  * `axios`: faz conexões e busca dados de APIs na internet.

---

### Passo 6: Iniciar o projeto no navegador
```bash
npm run dev
```
* **O que esse código faz:** Inicia o servidor local de desenvolvimento. Ele mostrará um link (ex: `http://localhost:5173`). Segure `Ctrl` e clique no link para ver seu site rodando!

---

## 📂 2. O que é e para que serve cada pasta?

Abaixo está o mapa das pastas e a explicação simples de cada uma:

```text
meu-portfolio/
├── public/                 # Arquivos públicos e estáticos
├── src/                    # O coração da aplicação (onde você programa)
│   ├── assets/             # Imagens, fotos, logos e arquivos SVG
│   ├── components/         # Blocos visuais reutilizáveis (botões, cards, menu)
│   ├── hooks/              # Lógicas e funções especiais do React
│   ├── pages/              # As páginas/telas completas do site
│   ├── services/           # Conexão com APIs e dados da internet
│   ├── styles/             # Arquivos de estilo visual, cores e temas CSS
│   ├── utils/              # Funções simples de ajuda (formatar datas, textos)
│   ├── App.jsx             # O componente principal que junta tudo
│   ├── index.css           # Estilos globais do site
│   └── main.jsx            # Arquivo que conecta o React com o HTML
├── index.html              # O HTML único que carrega seu React
└── package.json            # Lista com o nome do projeto e as bibliotecas instaladas
```

### Explicação detalhada de cada pasta em `src/`:

* **`src/assets/`**  
  Guarda todos os arquivos visuais locais do seu site: sua foto de perfil, prints dos seus projetos, logos e ícones em SVG.

* **`src/components/`**  
  Guarda pedaços de tela que você pode reaproveitar em qualquer lugar.  
  *Exemplos:* um menu no topo (`Navbar.jsx`), um rodapé (`Footer.jsx`), um botão padronizado (`Button.jsx`) ou o cartão de um projeto (`ProjectCard.jsx`).

* **`src/pages/`**  
  Guarda as páginas ou telas inteiras do site. Cada página costuma juntar vários componentes.  
  *Exemplos:* `Home.jsx` (página inicial), `Sobre.jsx`, `Contato.jsx`.

* **`src/hooks/`**  
  Guarda funções customizadas do React para reaproveitar lógica entre componentes.  
  *Exemplos:* um hook para saber se o usuário desceu a barra de rolagem (scroll) ou para alternar entre modo claro e escuro.

* **`src/services/`**  
  Guarda os arquivos que conversam com servidores externos.  
  *Exemplos:* um arquivo que busca seus repositórios direto da API pública do GitHub para listar no portfólio.

* **`src/styles/`**  
  Guarda as configurações visuais globais, como suas variáveis de cores (ex: cor primária, cor de fundo), fontes e estilos compartilhados.

* **`src/utils/`**  
  Guarda funções pequenas e úteis em JavaScript puro que não têm relação direta com visual.  
  *Exemplos:* uma função para formatar data (`01/10/2026`) ou limitar o tamanho de um texto com `...`.

---

## 📚 3. Principais Bibliotecas: Para que serve cada uma?

### 1. `lucide-react` (Ícones)
* **Comando:** `npm install lucide-react`
* **Para que serve:** Adiciona ícones elegantes e personalizáveis em qualquer componente com uma linha de código.
* **Exemplo de uso:**
  ```jsx
  import { Github, Mail, ExternalLink } from 'lucide-react';

  function Contato() {
    return (
      <div>
        <Github size={24} color="#6366f1" />
        <Mail size={24} color="#38bdf8" />
      </div>
    );
  }
  ```

---

### 2. `react-router-dom` (Navegação entre Páginas)
* **Comando:** `npm install react-router-dom`
* **Para que serve:** Permite criar links e rotas para mudar de página (ex: de `/` para `/sobre`) instantaneamente, sem que a página inteira precise recarregar na tela (conceito de SPA - *Single Page Application*).

---

### 3. `axios` (Requisições e Conexão com APIs)
* **Comando:** `npm install axios`
* **Para que serve:** Facilita buscar ou enviar dados através da internet de forma rápida e segura.
* **Exemplo de uso:** Buscar os seus projetos direto da API do GitHub para não precisar cadastrá-los manualmente no código.

---

### 4. `framer-motion` (Animações Visuais)
* **Comando:** `npm install framer-motion`
* **Para que serve:** Deixa seu portfólio com visual de alto nível, criando animações suaves ao abrir o site, rolar a página ou passar o mouse sobre botões e cartões.

---

### 5. `Tailwind CSS` (Estilização Rápida por Classes)
* **Para que serve:** Permite estilizar seus componentes escrevendo classes diretamente nas tags (como `className="flex items-center text-blue-500 font-bold"`), agilizando a criação do layout.

---

## ⚡ 4. Comandos do Dia a Dia

| Comando | Quando usar? |
|---|---|
| `npm run dev` | **Para programar:** Inicia o servidor local com atualização instantânea no navegador assim que você salva o código. |
| `npm run build` | **Para publicar:** Compila e otimiza todo o seu projeto gerando a pasta `dist/` pronta para ir ao ar (Vercel, Netlify, GitHub Pages). |
| `npm run preview` | **Para testar a versão final:** Abre no navegador a versão compilada exatamente como ficará na internet. |
