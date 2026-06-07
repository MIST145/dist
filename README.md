# Admin Dashboard — Navbar & Sidebar

<div align="center">

**[🇵🇹 Português](#-português) · [🇬🇧 English](#-english)**

</div>

---

## 🇵🇹 Português

### Descrição

Dashboard administrativo com navbar fixa e sidebar multi-nível, construído com HTML, CSS e JavaScript puro. Inclui um sistema de carregamento de aplicações internas via iframe, permitindo abrir ferramentas da pasta `apps/` diretamente dentro da interface sem sair da página.

### Demonstração

🔗 **[Ver online](https://mist145.github.io/NOME-DO-REPO/)**

### Estrutura do projeto

```
📁 /
├── index.html          ← Página principal (navbar + sidebar + área de conteúdo)
├── style.css           ← Estilos globais
└── 📁 apps/
    ├── GPT-texture_autocrop_dark.html   ← AutoCrop PRO (processador de texturas)
    └── analisador.html                  ← Lua Analyzer (divisor de scripts Lua)
```

### Funcionalidades

- **Navbar fixa** com megamenu, notificações e dropdown de utilizador
- **Sidebar de 3 níveis** com hover cascading (ícone → submenu → sub-submenu)
- **Categoria Apps** — abre ferramentas HTML dentro da própria página via iframe
- **Barra de retorno** ao carregar uma app, com botão para voltar ao conteúdo principal
- Layout totalmente responsivo via Bootstrap 4

### Tecnologias

| Tecnologia | Versão | Uso |
|---|---|---|
| Bootstrap | 4.0.0-alpha.6 | Layout e componentes |
| Font Awesome | 4.7.0 | Ícones |
| jQuery | 3.1.1 | Dependência do Bootstrap |
| Google Fonts | — | Open Sans |

### Apps incluídas

#### AutoCrop PRO
Processador de texturas com interface futurista. Faz crop automático de imagens (remoção de fundo escuro ou transparente), redimensiona para resolução quadrada configurável (256 / 512 / 1024 px), e exporta em batch via ZIP.

- Drag & drop ou seleção múltipla de ficheiros
- Modos: Dark Detection, Alpha Transparency, Hybrid Smart
- Threshold e padding configuráveis
- Download individual ou ZIP de todas as texturas

#### Lua Analyzer
Analisador e divisor de scripts Lua usando a API do Gemini. Divide automaticamente ficheiros grandes em partes com limite configurável de caracteres, respeitando a integridade sintática (nunca corta no meio de uma função).

- Suporte a upload de ficheiros `.lua`
- Saída em JSON estruturado com nome por convenção (`client_part-X_Y.lua`)
- Comentários de cabeçalho automáticos em cada parte
- Download individual de cada parte gerada

### Como adicionar uma nova app

1. Colocar o ficheiro `.html` na pasta `apps/`
2. Abrir `index.html` e encontrar o comentário `NEW CATEGORY: Apps / Tools`
3. Duplicar o bloco `<li>` existente e alterar os atributos:

```html
<li class="list-group-item pl-4">
  <a href="#"
     class="app-link"
     data-app="apps/NOME_DO_FICHEIRO.html"
     data-title="Nome visível no sidebar">Nome visível no sidebar</a>
</li>
```

### GitHub Pages — Deployment

O repositório está configurado para ser servido via GitHub Pages diretamente da raiz do branch `main`.

Para ativar num repositório novo:
1. **Settings → Pages**
2. Source: `main` branch, pasta `/ (root)`
3. Clicar **Save** e aguardar ~1 minuto

---

## 🇬🇧 English

### Description

Administrative dashboard with a fixed navbar and multi-level sidebar, built with plain HTML, CSS and JavaScript. Features an internal app loader via iframe, allowing tools from the `apps/` folder to open directly inside the interface without leaving the page.

### Live Demo

🔗 **[View online](https://mist145.github.io/NOME-DO-REPO/)**

### Project structure

```
📁 /
├── index.html          ← Main page (navbar + sidebar + content area)
├── style.css           ← Global styles
└── 📁 apps/
    ├── GPT-texture_autocrop_dark.html   ← AutoCrop PRO (texture processor)
    └── analisador.html                  ← Lua Analyzer (Lua script splitter)
```

### Features

- **Fixed navbar** with megamenu, notifications and user dropdown
- **3-level sidebar** with hover cascading (icon → submenu → sub-submenu)
- **Apps category** — opens HTML tools inside the page via iframe
- **Back bar** when an app is loaded, with button to return to main content
- Fully responsive layout via Bootstrap 4

### Technologies

| Technology | Version | Usage |
|---|---|---|
| Bootstrap | 4.0.0-alpha.6 | Layout and components |
| Font Awesome | 4.7.0 | Icons |
| jQuery | 3.1.1 | Bootstrap dependency |
| Google Fonts | — | Open Sans |

### Included apps

#### AutoCrop PRO
Texture processor with a futuristic interface. Automatically crops images (removes dark or transparent backgrounds), resizes to a configurable square resolution (256 / 512 / 1024 px), and batch-exports via ZIP.

- Drag & drop or multi-file selection
- Modes: Dark Detection, Alpha Transparency, Hybrid Smart
- Configurable threshold and padding
- Individual download or ZIP of all textures

#### Lua Analyzer
Lua script analyzer and splitter powered by the Gemini API. Automatically splits large files into parts with a configurable character limit, respecting syntactic integrity (never cuts in the middle of a function).

- Supports `.lua` file upload
- Structured JSON output with naming convention (`client_part-X_Y.lua`)
- Automatic header comments in each part
- Individual download for each generated part

### How to add a new app

1. Place the `.html` file in the `apps/` folder
2. Open `index.html` and find the comment `NEW CATEGORY: Apps / Tools`
3. Duplicate the existing `<li>` block and update the attributes:

```html
<li class="list-group-item pl-4">
  <a href="#"
     class="app-link"
     data-app="apps/YOUR_FILE.html"
     data-title="Label shown in sidebar">Label shown in sidebar</a>
</li>
```

### GitHub Pages — Deployment

The repository is configured to be served via GitHub Pages directly from the root of the `main` branch.

To enable on a new repository:
1. **Settings → Pages**
2. Source: `main` branch, folder `/ (root)`
3. Click **Save** and wait ~1 minute

---

<div align="center">
<sub>Built with HTML · CSS · JavaScript · Bootstrap 4</sub>
</div>
