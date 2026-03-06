# Trafego

Kit de skills para gestao e analise de trafego pago e organico usando Claude Code.

## O que e isso?

Este repositorio contem **42 skills** prontas para uso com o [Claude Code](https://claude.ai). Cada skill e um conjunto de instrucoes especializadas que transforma o Claude em um especialista naquela area — sem precisar explicar contexto toda vez.

Basta clonar, abrir o Claude Code neste diretorio, e voce tem acesso a um time completo de marketing digital.

## Skills disponiveis

### Trafego Pago

| Skill | O que faz |
|-------|-----------|
| `paid-ads` | Cria, otimiza e escala campanhas em Meta, Google, LinkedIn, TikTok e X |
| `analytics-tracking` | Configura e audita tracking (GA4, GTM, eventos, conversoes, UTMs) |
| `google-analytics-automation` | Gera relatorios automatizados do GA4 |

### SEO (12 skills)

| Skill | O que faz |
|-------|-----------|
| `seo-fundamentals` | Base tecnica de SEO |
| `seo-audit` | Auditoria tecnica completa de um site |
| `seo-keyword-strategist` | Pesquisa e estrategia de palavras-chave |
| `seo-content-planner` | Cria calendario editorial otimizado para SEO |
| `seo-content-writer` | Escreve conteudo otimizado para ranqueamento |
| `seo-content-auditor` | Audita conteudo existente e sugere melhorias |
| `seo-content-refresher` | Atualiza conteudos antigos para recuperar posicoes |
| `seo-cannibalization-detector` | Identifica paginas competindo pela mesma keyword |
| `seo-meta-optimizer` | Otimiza titles, descriptions e meta tags |
| `seo-structure-architect` | Planeja arquitetura de informacao e silos de conteudo |
| `seo-snippet-hunter` | Estrategias para conquistar featured snippets |
| `seo-authority-builder` | Link building e construcao de autoridade |
| `programmatic-seo` | SEO programatico em escala |

### CRO — Otimizacao de Conversao (6 skills)

| Skill | O que faz |
|-------|-----------|
| `page-cro` | Otimiza landing pages para aumentar taxa de conversao |
| `ab-test-setup` | Configura testes A/B com hipoteses e metricas claras |
| `signup-flow-cro` | Otimiza fluxos de cadastro e registro |
| `form-cro` | Otimiza formularios (campos, layout, UX) |
| `popup-cro` | Otimiza popups (timing, copy, segmentacao) |
| `onboarding-cro` | Otimiza onboarding de novos usuarios |
| `paywall-upgrade-cro` | Otimiza conversao de free para pago |
| `free-tool-strategy` | Cria ferramentas gratuitas como canal de aquisicao |

### Marketing e Conteudo

| Skill | O que faz |
|-------|-----------|
| `content-marketer` | Estrategia completa de content marketing |
| `content-creator` | Cria conteudo para diferentes canais e formatos |
| `social-content` | Conteudo otimizado para redes sociais |
| `copywriting` | Redacao persuasiva para ads, landing pages e emails |
| `email-sequence` | Cria sequencias de email marketing automatizadas |
| `marketing-ideas` | Gera ideias e estrategias de marketing |
| `marketing-psychology` | Aplica principios de psicologia em marketing |

### Estrategia e Competitividade

| Skill | O que faz |
|-------|-----------|
| `competitor-alternatives` | Analisa concorrentes e alternativas de mercado |
| `competitive-landscape` | Mapeia cenario competitivo completo |
| `pricing-strategy` | Define estrategia de precificacao |
| `launch-strategy` | Planeja lancamentos de produtos e campanhas |

### Data e Analytics

| Skill | O que faz |
|-------|-----------|
| `data-storytelling` | Transforma dados em narrativas claras e acionaveis |
| `data-scientist` | Analise estatistica e modelagem de dados |

### Pesquisa e Inteligencia

| Skill | O que faz |
|-------|-----------|
| `deep-research` | Pesquisa aprofundada sobre qualquer tema |
| `tavily-web` | Busca na web via Tavily API |
| `exa-search` | Busca semantica na web via Exa |
| `firecrawl-scraper` | Web scraping estruturado de qualquer site |
| `prompt-engineering` | Cria e otimiza prompts para LLMs |

## Como usar

### 1. Clone o repositorio

```bash
git clone https://github.com/marcelokarval/trafego.git
cd trafego
```

### 2. Abra o Claude Code neste diretorio

```bash
claude
```

### 3. Use as skills

Peca ao Claude para carregar qualquer skill antes de executar uma tarefa:

```
"carregue a skill paid-ads e analise minhas campanhas do Meta Ads"
"use a skill seo-audit e faca uma auditoria do site example.com"
"com a skill copywriting, escreva 5 variacoes de headline para meu anuncio"
```

Ou use o Skill tool diretamente:

```
Skill tool -> "paid-ads"
Skill tool -> "seo-audit"
```

## Estrutura

```
trafego/
├── README.md           # Este arquivo
├── CLAUDE.md           # Configuracao do projeto para o Claude Code
└── .claude/
    └── skills/         # 42 skills especializadas
        ├── paid-ads/
        ├── seo-*/
        ├── *-cro/
        └── ...
```

## Requisitos

- [Claude Code](https://claude.ai) instalado
- Conta Claude com acesso ao Claude Code

## Licenca

Uso interno.
