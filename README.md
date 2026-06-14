# Neon Quarter

Landing page para o bar fictício de arcade e pinball **Neon Quarter**.

**Demo:** https://neon-quarter.pages.dev

---

## Como Reproduzir com AI Workflow

Este site foi gerado usando o [AI Workflow](https://ai-workflow-kit-site.pages.dev/), um kit de ferramentas para desenvolvimento assistido por IA. Abaixo estão os passos detalhados para reproduzir este projeto.

### Pré-requisitos

- Node.js (v18 ou superior)
- Conta no GitHub
- Acesso ao AI Workflow (CLI ou interface integrada)

### Passo 1: Instalar o AI Workflow

```bash
# Instalar o AI Workflow CLI globalmente
npm install -g ai-workflow

# Verificar instalação
ai-workflow --version
```

### Passo 2: Configurar o Repositório

```bash
# Criar novo repositório no GitHub
# Ou clonar um existente
git clone https://github.com/seu-usuario/landing-neon-quarter.git
cd landing-neon-quarter

# Inicializar o AI Workflow no projeto
ai-workflow init
```

### Passo 3: Usar o Prompt

O arquivo [`prompt.md`](prompt.md) contém o prompt completo usado para gerar esta landing page. Para reproduzir:

**Opção A: Via CLI**
```bash
# Enviar o prompt para o AI Workflow
ai-workflow run --prompt prompt.md --mode standard
```

**Opção B: Via Interface Web**
1. Acesse o painel do AI Workflow
2. Cole o conteúdo do `prompt.md` no campo de entrada
3. Selecione o modo **Standard**
4. Clique em **Executar**

**Opção C: Copiar e Colar**
1. Abra o arquivo [`prompt.md`](prompt.md)
2. Copie todo o conteúdo
3. Cole em qualquer agente de IA (Claude, GPT, etc.) com capacidade de gerar código
4. Solicite a implementação completa

### Passo 4: Fluxo de Trabalho do AI Workflow

O AI Workflow segue este processo automatizado:

```
1. Discovery/Specification
   └── Análise do prompt e extração de requisitos

2. Branch Recovery
   └── Criação de branch feature: neon-quarter-landing

3. Implementation
   └── Geração do index.html com CSS e JS inline
   └── Implementação de todas as 11 secções
   └── Adição de interatividade (modal, tabs, lightbox)

4. Validation
   ├── Lighthouse Audit (Accessibility, Best Practices, SEO)
   ├── Testes de Responsividade (375px, 768px, 1024px, 1440px)
   ├── Validação de Acessibilidade (ARIA, keyboard, focus)
   └── Verificação de Performance

5. Remediation
   └── Correção de issues encontrados (contrast, roles, etc.)

6. Finalization
   └── Commit com mensagem descritiva
   └── Push para a branch feature
   └── Coleta de evidências
```

### Passo 5: Comandos Manuais (se necessário)

Se precisar fazer ajustes manuais após a geração:

```bash
# Criar branch para alterações
git checkout -b minha-alteracao

# Editar o index.html
# ...

# Validar com Lighthouse
ai-workflow audit --url http://localhost:8000

# Testar responsividade
ai-workflow test --responsive

# Commit e push
git add index.html
git commit -m "feat: ajustes na landing page"
git push origin minha-alteracao

# Finalizar task
ai-workflow collect-evidence --mode standard --task=neon-quarter-landing
```

### Passo 6: Deploy

**GitHub Pages (Recomendado)**
```bash
# Configurar no GitHub
# Settings > Pages > Source > Branch: main

# Ou via CLI
ai-workflow deploy --target github-pages
```

**Outras opções**
```bash
# Netlify
ai-workflow deploy --target netlify

# Vercel
ai-workflow deploy --target vercel

# Manual (qualquer host estático)
# Fazer upload do index.html
```

---

## Deploy no Cloudflare Pages (Passo a Passo)

Este projeto está configurado para rodar perfeitamente no **Cloudflare Pages**. Como é um site estático (apenas HTML/CSS/JS), o deploy é direto e gratuito.

### Método 1: Via Dashboard (Mais Simples)

1. **Acesse o Cloudflare Dashboard**
   - Vá para [dash.cloudflare.com](https://dash.cloudflare.com)
   - Faça login com sua conta

2. **Criar um novo projeto**
   - No menu lateral, clique em **Pages**
   - Clique em **Create a project**
   - Selecione **Connect to Git**

3. **Conectar o repositório**
   - Autorize o Cloudflare a acessar sua conta do GitHub
   - Selecione o repositório: `landing-neon-quarter`
   - Clique em **Begin setup**

4. **Configurar o build**
   - **Project name:** `neon-quarter` (ou outro nome de sua preferência)
   - **Production branch:** `main`
   - **Framework preset:** `None` (ou `Static HTML`)
   - **Build command:** Deixe em branco (não precisa compilar nada)
   - **Build output directory:** `/` (raiz do projeto)
   - Clique em **Save and Deploy**

5. **Deploy concluído**
   - O Cloudflare vai clonar o repo, fazer o deploy e fornecer um link
   - O link será algo como: `https://neon-quarter.pages.dev`
   - Você pode configurar um **Custom Domain** em **Custom domains** se quiser

### Método 2: Via Wrangler CLI (Para Desenvolvedores)

1. **Instalar o Wrangler**
   ```bash
   npm install -g wrangler
   ```

2. **Autenticar no Cloudflare**
   ```bash
   wrangler login
   ```
   - Isso abrirá o navegador para você autorizar o acesso

3. **Deploy direto**
   ```bash
   # Na pasta do projeto
   cd /caminho/para/landing-neon-quarter
   
   # Fazer deploy
   wrangler pages deploy . --project-name neon-quarter
   ```

4. **Configurar deploy automático (opcional)**
   Crie um arquivo `wrangler.toml` na raiz:
   ```toml
   name = "neon-quarter"
   compatibility_date = "2026-06-14"
   
   [site]
   bucket = "."
   ```

### Método 3: Drag & Drop (Mais Rápido)

1. **Acesse o Cloudflare Pages**
   - [dash.cloudflare.com/pages](https://dash.cloudflare.com/pages)

2. **Criar projeto via upload**
   - Clique em **Create a project**
   - Selecione **Upload assets**
   - Arraste a pasta do projeto (ou zip) para a área indicada
   - Clique em **Deploy site**

### Configurações Recomendadas

Depois do deploy, configure estas opções no dashboard:

| Configuração | Valor | Por que? |
|-------------|-------|---------|
| **Build command** | *(vazio)* | Não precisa build, é HTML estático |
| **Root directory** | `/` | O `index.html` está na raiz |
| **Branch** | `main` | Deploy automático ao fazer push na main |
| **Preview deployments** | `Enabled` | Cada PR gera uma URL de preview |

### DNS e Custom Domain (Opcional)

Se quiser usar um domínio próprio (ex: `neonquarter.com`):

1. Vá em **Custom domains** no projeto
2. Clique em **Set up a custom domain**
3. Digite seu domínio
4. Siga as instruções de DNS do Cloudflare
5. O Cloudflare gerencia automaticamente o SSL (HTTPS)

### Preview Deployments

Cada vez que você fizer push para uma branch que não seja a `main`, o Cloudflare cria automaticamente uma **URL de preview**:
- Ex: `https://abc123.neon-quarter.pages.dev`
- Útil para revisar mudanças antes de fazer merge para a `main`

### Como funciona o deploy automático

```
1. Você faz push para a branch main
   ↓
2. Cloudflare detecta a mudança via webhook
   ↓
3. Cloudflare clona o repo e faz o deploy
   ↓
4. Site atualizado em ~30-60 segundos
   ↓
5. URL: https://neon-quarter.pages.dev
```

### Dica: Redirecionar para a URL correta

Se você já publicou o site antes em outro lugar (GitHub Pages, etc.), adicione um redirect no `index.html` (já configurado nas meta tags do projeto):

```html
<meta property="og:url" content="https://neon-quarter.pages.dev">
```

---

## Estrutura do Projeto

```
landing-neon-quarter/
├── index.html          # Landing page completa (HTML + CSS + JS)
├── prompt.md           # Prompt original usado para gerar o site
└── README.md           # Este arquivo
```

**Nota:** Este projeto é intencionalmente um arquivo único (`index.html`) para facilitar deploy em qualquer host estático sem dependências.

---

## Funcionalidades Implementadas

| Secção | Descrição |
|--------|-----------|
| **Header** | Sticky, transparente sobre hero, fundo escuro no scroll |
| **Hero** | Full viewport, gradient overlay, stats animados |
| **Promoções** | 3 cards com hover effects e neon glow |
| **What You Can Do** | 6 feature cards com ícones SVG |
| **Explore** | Grid de 6 zonas com hover zoom e glow |
| **Menu Preview** | Tabs (Cocktails, Beer, Food, Alcohol-Free) |
| **Eventos** | Filtros por categoria (All, Arcade, Pinball, Parties) |
| **Social Proof** | Stats e 3 reviews com avatares |
| **Galeria** | Grid assimétrico, lightbox acessível |
| **Visit** | Horários, contacto, mapa placeholder |
| **Footer** | Newsletter, social links, AI Workflow signature |

### Interatividade

- **Modal de Reserva** — Formulário com validação, focus trap, Escape para fechar
- **Menu Tabs** — Navegação por categoria com ARIA roles
- **Filtros de Eventos** — Filtragem dinâmica por categoria
- **Lightbox** — Galeria com navegação por teclado
- **Mobile Menu** — Hamburger com animação e scroll lock
- **Scroll Animations** — IntersectionObserver para fade-in
- **Header Scroll** — Mudança de fundo ao fazer scroll

---

## Tech Stack

- **HTML5** — Semântico, acessível, SEO-friendly
- **CSS3** — Custom properties, Grid, Flexbox, Animations, backdrop-filter
- **JavaScript** — Vanilla, zero dependências, modular functions
- **Google Fonts** — Orbitron (display) + Inter (body)
- **Unsplash** — Imagens de referência (arcade, pinball, cocktails)

---

## Performance

- **Zero bibliotecas externas** — Tudo inline
- **Lazy loading** — Imagens fora do hero com `loading="lazy"`
- **Preconnect** — Otimização de fontes
- **Minificação** — CSS e JS inline (sem HTTP requests extra)
- **Lighthouse Scores** — Accessibility 95, Best Practices 100, SEO 83

---

## Acessibilidade

- Skip link para navegação rápida
- Semantic HTML (header, nav, main, section, article, footer)
- ARIA labels e roles (tab, tabpanel, dialog)
- Keyboard navigation (Tab, Escape, focus trap)
- `prefers-reduced-motion` support
- WCAG AA color contrast
- Form labels e error messages
- Alt text em todas as imagens

---

## Créditos

Feito com [AI Workflow](https://ai-workflow-kit-site.pages.dev/) — O kit de desenvolvimento assistido por IA para criar produtos digitais de forma rápida e profissional.

**Autor:** [williambeto](https://github.com/williambeto)
**Repositório:** https://github.com/williambeto/landing-neon-quarter
