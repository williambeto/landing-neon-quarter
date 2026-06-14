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
