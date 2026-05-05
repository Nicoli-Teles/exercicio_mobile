# HABIT - Portal de Conteúdo e Administração

Este projeto consiste na implementação de uma interface web completa (front-end) para um portal de notícias e gestão de conteúdo chamado **HABIT**. O desenvolvimento foi baseado em wireframes estáticos, com foco total em **semântica HTML5**, **CSS modular**, **responsividade mobile-first** e **acessibilidade**.


## 📑 Telas Implementadas

O projeto foi estruturado em 12 páginas funcionais para cobrir toda a experiência do utilizador e do administrador:

### Área Pública
* **Início (`inicio.html`):** Homepage com destaques, categorias e curadoria do editor.
* **Destaques (`Destaques.html`):** Galeria de conteúdos em evidência.
* **Categorias (`categoria_techno.html`):** Listagem de posts com sistema de etiquetas/tags para filtragem.
* **Pesquisa (`pesquisa.html`):** Interface de resultados com cards detalhados.
* **Newsletter (`assinar.html`):** Página de captura para subscrição de e-mails.

### Autenticação e Utilizador
* **Login (`login.html`):** Acesso ao sistema com suporte a login social.
* **Criar Conta (`criar_conta.html`):** Fluxo de registo de novos utilizadores.
* **Perfil (`perfil.html`):** Dashboard pessoal com histórico de posts e edição de biografia.

### Painel Administrativo (Dashboard)
* **Admin (`admin.html`):** Gestão central de categorias do portal.
* **Fila de Revisão (`fila_de_revisao.html`):** Interface de moderação para aprovação/reprovação de conteúdos.
* **Gestão de Utilizadores:** Listagem e controlo de status (Ativo/Bloqueado).

## 🛠️ Decisões de Layout e Tecnologia

* **Arquitetura CSS Modular:** O estilo foi dividido em múltiplos ficheiros (ex: `header.css`, `tabela.css`, `botões.css`) para garantir escalabilidade e facilitar a manutenção.
* **Sistemas de Posicionamento:**
    * **Flexbox:** Utilizado na navegação (`navbar`) e componentes de alinhamento simples.
    * **CSS Grid:** Utilizado na `highlights-grid` para os cards e na `tabela-grid` para gerir dados administrativos.
* **Mobile-First:** A estilização foi pensada primeiro para dispositivos móveis, utilizando `media queries` para adaptar o conteúdo a ecrãs maiores.
* **Tabelas Responsivas:** No dashboard, as tabelas convertem-se em "cards" no telemóvel através de atributos `data-label` e pseudo-elementos CSS, mantendo a legibilidade.

## 🎨 Design Tokens (Variáveis CSS)

As configurações visuais estão centralizadas no `global.css`:
* **Cores Principais:**
    * `--primary-teal: #127a73;` (Ajustada para contraste AA).
    * `--text-main: #222222;` (Legibilidade otimizada).
* **Tipografia:** Escala proporcional baseada em `rem` (de `0.875rem` a `2.5rem`).

## 📱 Responsividade (Breakpoints)

* **Mobile (Base):** Até 767px (layout em coluna única).
* **Tablet (768px):** Transição de menus para horizontal e grids para 2 ou 3 colunas.
* **Desktop (1024px+):** Otimização de margens e expansão do container principal (`max-width: 2500px`).

## ♿ Acessibilidade (WCAG)

* **Navegação por Teclado:** Estados de `:focus` claramente visíveis em todos os elementos interativos.
* **Semântica:** Uso correto de tags como `<header>`, `<main>`, `<nav>` e `<aside>`.
* **Leitores de Ecrã:** Implementação de `aria-label` e textos alternativos (`alt`) em imagens críticas.
* **Contraste:** Paleta de cores testada para garantir legibilidade de acordo com os padrões WCAG AA.

## 📂 Estrutura de Pastas

```text
/
├── assets/             # Imagens e recursos visuais
├── css/                # Ficheiros de estilo segregados
│   ├── global.css      # Variáveis e reset
│   ├── responsividade.css
│   ├── tabela.css
│   └── ...
├── [ficheiros].html    # Páginas do projeto
└── README.md           # Documentação
