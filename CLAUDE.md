# CLAUDE.md - Trafego Project

Projeto de gestao e analise de trafego pago e organico.
Foco: Meta Ads, Google Ads, SEO, CRO, Analytics.

## Memoria Persistente

O arquivo `claude/memory/MEMORY.md` armazena contexto entre sessoes.

### Como funciona
- O Claude DEVE ler `claude/memory/MEMORY.md` no inicio de cada sessao para recuperar contexto anterior.
- Ao longo da sessao, o Claude DEVE atualizar o arquivo com novos aprendizados, decisoes e insights relevantes.
- Ao final de uma sessao ou apos concluir uma tarefa importante, o Claude DEVE salvar o que aprendeu.

### O que salvar na memoria
- Contas de anuncio descobertas e seus IDs
- Padroes de performance observados (ex: "campanha X tem CPA alto por causa de Y")
- Preferencias do usuario (formato de relatorio, metricas preferidas, etc)
- Decisoes de projeto tomadas
- Erros encontrados e como foram resolvidos
- Tokens e credenciais NAO devem ser salvos (seguranca)

### O que NAO salvar
- Tokens de acesso, senhas ou credenciais
- Dados temporarios de uma unica sessao que nao serao reutilizados
- Informacoes que ja estao documentadas nas skills

### Como melhorar a memoria
- Organize por topicos (contas, aprendizados, preferencias, decisoes)
- Mantenha conciso — remova informacoes desatualizadas
- Se a memoria ficar grande, crie arquivos separados em `claude/memory/` (ex: `contas-meta.md`, `insights-seo.md`) e referencie no MEMORY.md
- Atualize em vez de duplicar — se uma informacao ja existe, edite-a

## Localizacao das Skills

Todas as skills estao em `claude/skills/` na raiz do projeto.
Para carregar uma skill, leia o arquivo `claude/skills/{nome-da-skill}/SKILL.md`.

## Skills Disponiveis

### Trafego Pago
- `paid-ads` — Criacao, otimizacao e escala de campanhas (Meta, Google, LinkedIn, TikTok, X)
- `analytics-tracking` — Measurement strategy, GA4, GTM, eventos, conversoes, UTMs
- `google-analytics-automation` — Automacao de relatorios GA4 (requer Rube MCP)

### SEO / Trafego Organico
- `seo-fundamentals` — Base de SEO
- `seo-audit` — Auditoria tecnica completa
- `seo-keyword-strategist` — Pesquisa e estrategia de palavras-chave
- `seo-content-planner` — Planejamento editorial SEO
- `seo-content-writer` — Redacao otimizada para SEO
- `seo-content-auditor` — Auditoria de conteudo existente
- `seo-content-refresher` — Atualizacao de conteudos antigos
- `seo-cannibalization-detector` — Detectar canibalizacao de keywords
- `seo-meta-optimizer` — Otimizacao de meta tags
- `seo-structure-architect` — Arquitetura de informacao e silos
- `seo-snippet-hunter` — Conquistar featured snippets
- `seo-authority-builder` — Link building e autoridade
- `programmatic-seo` — SEO programatico em escala

### CRO / Conversao
- `page-cro` — Otimizacao de taxa de conversao em landing pages
- `ab-test-setup` — Setup de testes A/B
- `signup-flow-cro` — Otimizacao de fluxo de cadastro
- `onboarding-cro` — Otimizacao de onboarding
- `form-cro` — Otimizacao de formularios
- `popup-cro` — Otimizacao de popups
- `paywall-upgrade-cro` — Otimizacao de paywalls e upgrades
- `free-tool-strategy` — Estrategia de ferramentas gratuitas para aquisicao

### Marketing e Conteudo
- `content-marketer` — Estrategia de content marketing
- `content-creator` — Criacao de conteudo + otimizacao social
- `social-content` — Conteudo para redes sociais
- `marketing-ideas` — Ideias e estrategias de marketing
- `marketing-psychology` — Psicologia aplicada a marketing
- `copywriting` — Redacao persuasiva
- `email-sequence` — Sequencias de email marketing

### Estrategia e Competitividade
- `competitor-alternatives` — Analise de alternativas competitivas
- `competitive-landscape` — Mapeamento de cenario competitivo
- `pricing-strategy` — Estrategia de precificacao
- `launch-strategy` — Estrategia de lancamento

### Data e Analytics
- `data-storytelling` — Transformar dados em narrativas
- `data-scientist` — Analise estatistica de dados

### Pesquisa e Inteligencia
- `deep-research` — Pesquisa aprofundada
- `tavily-web` — Web search via Tavily
- `exa-search` — Semantic web search via Exa
- `firecrawl-scraper` — Web scraping estruturado
- `prompt-engineering` — Engenharia de prompts

## Uso

Antes de executar qualquer tarefa, leia a skill correspondente:
```
Read claude/skills/paid-ads/SKILL.md
Read claude/skills/seo-audit/SKILL.md
```

Ou via Skill tool se disponivel:
```
Skill tool -> "paid-ads"
Skill tool -> "seo-audit"
```

## Meta Ads API

Para acessar dados do Meta Ads, usar a Graph API v21.0:
- Endpoint base: `https://graph.facebook.com/v21.0/`
- Contas de anuncio: `/me/adaccounts`
- Campanhas: `/act_{id}/campaigns`
- Ad Sets: `/act_{id}/adsets`
- Ads: `/act_{id}/ads`
- Insights: `/act_{id}/insights`

Campos uteis de insights:
`spend,impressions,clicks,ctr,cpc,cpm,reach,frequency,actions,cost_per_action_type,conversions,cost_per_conversion`

Breakdowns disponiveis:
`age,gender,country,region,publisher_platform,platform_position,device_platform`
