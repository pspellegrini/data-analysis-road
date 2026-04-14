# Setup Para Codar 10x Mais Rápido Com IA — Status

> Arquivo de referência para continuidade do projeto.
> Atualizar sempre que uma camada for concluída ou alterada.

---

## Visão Geral do Setup

Objetivo: configurar um ambiente completo de vibe coding com Claude Code para a jornada do zero ao Analista de Dados.

Diretório principal (via OneDrive — compartilhado entre as duas máquinas):
`OneDrive\Documentos\Data Analysis Road\vibe-coding\`

### Máquinas configuradas

| Identificador | Uso | Usuário Windows |
|---|---|---|
| **Máquina Pessoal** | Acesso em casa | `&lt;usuario-pessoal&gt;` |
| **Máquina Corporativa** | Acesso no trabalho | `&lt;usuario-corporativo&gt;` |

> Os arquivos do projeto (`CLAUDE.md`, slash commands, hooks) ficam no OneDrive e são automaticamente compartilhados. O que difere entre as máquinas são as configurações locais de cada usuário (`~/.claude/settings.json`, extensões do VSCode, Python instalado).

---

## Camadas do Setup

### Camada 1 — VSCode Extensions

Extensões essenciais para data analysis + vibe coding:

| Extensão | Função | Pessoal (`&lt;usuario-pessoal&gt;`) | Corporativa (`&lt;usuario-corporativo&gt;`) |
|---|---|---|---|
| `ms-python.python` | Suporte a Python | ✅ | ✅ |
| `ms-toolsai.jupyter` | Notebooks Jupyter | ✅ | ✅ |
| `ms-python.pylance` | Autocomplete Python | ✅ | ✅ |
| `ms-python.debugpy` | Debugger Python | ✅ | ✅ |
| `github.copilot-chat` | IA no editor (unificado) | ✅ | ✅ (requer login com licença) |
| `streetsidesoftware.code-spell-checker` | Corretor ortográfico | ✅ | ✅ |
| `miguelsolorio.min-theme` | Tema visual | ✅ | ✅ |
| `natqe.reload` | Botão de reload rápido | ✅ | ✅ |
| `pkief.material-icon-theme` | Ícones de arquivo | ✅ | ✅ |
| `grapecity.gc-excelviewer` | Visualizar CSVs/Excel | ✅ | ✅ |

Obs: `github.copilot` e `github.copilot-chat` foram unificados em uma única extensão (`github.copilot-chat`).

---

### Camada 2 — Claude Code Setup ✅ Concluída (ambas as máquinas)

#### 2a. CLAUDE.md
Arquivo: `learning-env/CLAUDE.md`

Contexto persistente carregado automaticamente a cada sessão. Contém:
- Perfil do usuário (absoluto zero)
- Roadmap completo (6 fases, 20 etapas)
- Regras de comportamento do Claude
- Convenções de código
- O que evitar
- **Monitoramento de sessão** — ao final de cada resposta, sinalizar quando aplicável:
  - `[SESSÃO LONGA]` — sessão longa, risco de perda de contexto. Apresenta comando pronto para nova sessão continuar a discussão.
  - `[DESVIO DE CONTEXTO]` — assunto saiu do foco original. Apresenta comando para nova sessão explorar o desvio.
  - `[RISCO DE ALUCINAÇÃO]` — resposta com detalhes não confirmados. Distingue certeza de suposição.

#### 2b. Slash Commands Customizados
Diretório: `learning-env/.claude/commands/`

| Comando | Arquivo | Função |
|---|---|---|
| `/eda` | `eda.md` | EDA completo com explicações antes do código |
| `/conceito` | `conceito.md` | Explica qualquer conceito do zero com analogias |
| `/exercicio` | `exercicio.md` | 5 exercícios progressivos (fácil ao desafio) |
| `/explain` | `explain.md` | Explica código linha por linha |
| `/notebook` | `notebook.md` | Cria notebook Jupyter completo de aprendizado |
| `/sql` | `sql.md` | Gera SQL comentado com explicações |
| `/revisar` | `revisar.md` | Revisão de código com feedback didático |
| `/debug` | `debug.md` | Interpreta erros e explica a causa |
| `/viz` | `viz.md` | Cria visualizações com justificativa do tipo de gráfico |
| `/projeto` | `projeto.md` | Scaffold de projeto de análise completo |
| `/cheatsheet` | `cheatsheet.md` | Folha de referência rápida sobre qualquer tema |
| `/comparar` | `comparar.md` | Compara duas tecnologias/abordagens |
| `/plano` | `plano.md` | Plano de estudos semana a semana |
| `/qualidade` | `qualidade.md` | Checklist de qualidade para notebooks, scripts e queries |
| `/agentes` | `agentes.md` | Explica como agentes de IA e o Claude Code funcionam por baixo |
| `/continuar` | `continuar.md` | Salva marcador de sessão ou retoma de onde parou |
| `/licao` | `licao.md` | Extrai a lição de aprendizado do que aconteceu na sessão |

Uso: `/comando argumento` — ex: `/conceito o que é um DataFrame?` — ex: `/conceito o que é um DataFrame?`

#### 2c. Hooks (settings.json)
Arquivo: `learning-env/.claude/settings.json`

- **PostToolUse (Write)**: avisa para commitar após salvar arquivo
- **Stop**: mensagem de encerramento de sessão

---

### Camada 3 — MCP Servers ✅ Concluída (ambas as máquinas)

Configuração global em: `~/.claude/settings.json` (específica por máquina)

#### MCPs configurados em ambas as máquinas

| MCP | Pacote | Função |
|---|---|---|
| `context7` | `@upstash/context7-mcp` | Documentação atualizada de bibliotecas |
| `filesystem` | `@modelcontextprotocol/server-filesystem` | Acesso direto a arquivos do projeto |
| `fetch` | `@modelcontextprotocol/server-fetch` | Buscar URLs e páginas da web |
| `sequential-thinking` | `@modelcontextprotocol/server-sequential-thinking` | Raciocínio analítico estruturado |
| `sqlite` | `mcp-server-sqlite` | Consultar bancos SQLite diretamente |
| `github` | `@modelcontextprotocol/server-github` | Gerenciar repositório e portfólio |

#### Status por máquina

| MCP | Pessoal (`&lt;usuario-pessoal&gt;`) | Corporativa (`&lt;usuario-corporativo&gt;`) |
|---|---|---|
| `context7` | ✅ | ✅ |
| `filesystem` | ✅ | ✅ |
| `fetch` | ✅ | ✅ |
| `sequential-thinking` | ✅ | ✅ |
| `sqlite` | ✅ | ✅ |
| `github` | ✅ Token configurado | ✅ Token configurado |
| `duckduckgo` | ✅ | ✅ |
| `context-mode` | ✅ | ✅ |

Para verificar MCPs ativos: rodar `/mcp` no Claude Code.

---

### Camada 3b — Skills Externas: highermind-code-skills ✅ Disponível (instalação pendente)

Skills profissionais de engenharia de software localizadas em:
`OneDrive\Documentos\Data Analysis Road\highermind-code-skills-main\`

Estas skills adicionam modos de execução especializados ao Claude Code para auditar código, validar qualidade, segurança e deploy. São complementares aos slash commands de ensino do `vibe-coding` — não substituem, mas aprofundam.

#### Skills disponíveis

| Skill | Comando | Função |
|---|---|---|
| hm-engineer | `/hm-engineer` | Auditoria de código (arquitetura, performance, segurança OWASP) |
| hm-qa | `/hm-qa` | Qualidade e testes (inclui segurança, infra, dados) |
| hm-designer | `/hm-designer` | Validação de interface (UI, dark mode, tipografia) |
| hm-init | `/hm-init` | Inicialização de projetos com padrões profissionais |
| hm-deploy | `/hm-deploy` | Validação de deploy e infraestrutura Docker |
| hm-security | `/hm-security` | Auditoria de segurança aprofundada (L1/L2/L3) |

#### Quando ativar cada skill (por fase do roadmap)

| Fase | Skill | Gatilho |
|---|---|---|
| Fases 1–4 (Python, SQL, pandas, visualização) | `/hm-engineer`, `/hm-qa` | Ao querer feedback profissional em projetos de análise |
| Fase 4 (Plotly, Streamlit) | `/hm-designer` | Ao criar dashboards ou visualizações interativas |
| Fase 5 (Django, Web) | `/hm-init`, `/hm-deploy` | Ao iniciar o projeto web e preparar para deploy |
| Fase 6 (Projeto final, ML) | `/hm-engineer`, `/hm-security` | Auditoria completa do projeto antes de publicar no portfólio |

**GitHub**: https://github.com/rodrigohighermind/highermind-code-skills

#### Como instalar (uma vez por máquina)

No Git Bash, dentro do diretório `highermind-code-skills-main/`:

```bash
chmod +x setup && ./setup
```

O script cria **symlinks** em `~/.claude/skills/` apontando para os arquivos dentro do diretório local.

> ⚠️ **Importante sobre o diretório local**: o setup cria symlinks — se o diretório for deletado antes de instalar, os comandos `/hm-*` não funcionarão. Se quiser usar as skills e depois deletar o diretório, copie os arquivos `.md` de cada skill para `~/.claude/skills/` como arquivos reais (não links). Ou re-clone do GitHub quando necessário.

> Obs: o `CLAUDE.md.template` do highermind foi usado como referência para aprimorar o `learning-env/CLAUDE.md`, mas NÃO deve ser copiado diretamente — o tom para iniciante deve ser preservado.

---

### Camada 4 — Hooks Avançados ✅ Documentada (aplicar quando necessário)

Hooks básicos já ativos (Camada 2c). Hooks avançados prontos para adicionar em `learning-env/.claude/settings.json`:

#### Hook 1 — Aviso ao salvar arquivos `.py` (formatação automática com ruff)

Adicionar dentro do array `PostToolUse`, ao lado do hook de Write já existente:

```json
{
  "matcher": "Write",
  "hooks": [
    {
      "type": "command",
      "command": "python -c \"import sys,json,subprocess; d=json.load(sys.stdin); f=d.get('file_path',''); f.endswith('.py') and subprocess.run(['ruff','format',f],capture_output=True)\""
    }
  ]
}
```

> Pré-requisito: `pip install ruff`. Se não instalado, o hook falha silenciosamente.

#### Hook 2 — Aviso antes de comandos Bash com exclusão

Adicionar uma nova chave `PreToolUse` no objeto `hooks`:

```json
"PreToolUse": [
  {
    "matcher": "Bash",
    "hooks": [
      {
        "type": "command",
        "command": "python -c \"import sys,json; d=json.load(sys.stdin); cmd=d.get('command',''); 'rm ' in cmd and print('⚠️  Comando de exclusão detectado:', cmd)\""
      }
    ]
  }
]
```

> Este hook imprime um aviso no terminal quando detecta `rm ` no comando — não bloqueia, apenas alerta.

---

### Camada 5 — Git e Portfólio ✅ Documentada (executar quando pronto para publicar)

#### Inicializar o repositório

```bash
# Dentro de learning-env/
git init
git branch -M main
```

#### Criar `.gitignore` ✅ Concluído

O arquivo `learning-env/.gitignore` já existe com o conteúdo:

```
# Python
__pycache__/
*.py[cod]
*.egg-info/
.env
.venv/
venv/

# Jupyter
.ipynb_checkpoints/
*.ipynb_checkpoints

# Dados (nunca versionar dados brutos)
*.csv
*.xlsx
*.parquet
*.db
*.sqlite

# Sistema
.DS_Store
Thumbs.db

# Claude Code (auto-gerado por máquina — não compartilhar)
.claude/settings.local.json
```

#### Convenção de commits

Prefixos para o histórico do projeto de aprendizado:

| Prefixo | Quando usar | Exemplo |
|---|---|---|
| `feat:` | Novo slash command ou recurso | `feat: adiciona comando /eda` |
| `learn:` | Conclui exercício ou fase | `learn: conclui GROUP BY (Fase 2)` |
| `fix:` | Corrige erro em notebook ou script | `fix: importação do pandas no notebook 02` |
| `docs:` | Atualiza SETUP_STATUS ou CLAUDE.md | `docs: camada 5 concluída` |
| `config:` | Altera hooks ou MCPs | `config: adiciona hook de formatação ruff` |

#### Vincular ao GitHub

```bash
git remote add origin https://github.com/<seu-usuario>/vibe-coding.git
git add .
git commit -m "feat: setup inicial do vibe-coding"
git push -u origin main
```

> Criar o repositório no GitHub antes de executar o `push`. Recomendado: repositório **privado** (contém configurações pessoais).

---

### Camada 6 — Referências para Fases Avançadas 📚 Disponível (leitura futura)

Projetos de referência localizados em `OneDrive\Documentos\Data Analysis Road\`. Não requerem instalação — são fontes de aprendizado e consulta em fases específicas do roadmap.

#### 12-factor-agents-main

**GitHub**: https://github.com/humanlayer/12-factor-agents

**O que é**: guia de 12 princípios de engenharia para construir aplicações LLM confiáveis em produção. Criado por Dex Horthy (HumanLayer). Conteúdo em markdown puro, independente de linguagem.

**Contribuição para o vibe-coding**: base conceitual do comando `/agentes` — que desmistifica como o Claude Code funciona por baixo (loop de agente, context window, ferramentas, controle de fluxo).

| Quando consultar | O quê |
|---|---|
| Qualquer fase | Leitura conceitual: `content/factor-01` a `content/factor-12` (~15 min cada) |
| Fase 6 (avançado) | Workshop em Python: `workshops/2025-07-16/` — construir um agente do zero |

> Fatores mais relevantes para o aluno agora: **Factor 2** (por que o CLAUDE.md importa), **Factor 3** (context window), **Factor 4** (como ferramentas funcionam), **Factor 8** (código determinístico vs. LLM).

#### agentcontrolplane-main (ACP)

**GitHub**: https://github.com/humanlayer/agentcontrolplane

**O que é**: Kubernetes operator em Go para orquestração de agentes LLM com durabilidade, sub-agentes, aprovações humanas e observabilidade completa. Desenvolvido pela equipe HumanLayer. Atualmente em alpha.

**Contribuição para o vibe-coding**: nenhuma prática — muito avançado para as fases atuais.

| Quando consultar | O quê |
|---|---|
| Pós-roadmap (após Fase 6) | `docs/getting-started.md` — tutorial de deploy de agentes em Kubernetes |

> Requer conhecimento de Go, Kubernetes e infraestrutura cloud. Não é parte do roadmap Data Analyst.

---

## Estrutura de Arquivos Atual

```
learning-env/
├── CLAUDE.md                    # Contexto persistente do Claude Code
├── ENVIRONMENT.md               # Este arquivo — status e continuidade
├── .gitignore                   # Ignorar dados, venv, checkpoints, settings locais
├── .claude/
│   ├── settings.json            # Hooks configurados
│   ├── settings.local.json      # Permissões auto-geradas (por máquina)
│   └── commands/                # 17 slash commands customizados
│       ├── eda.md
│       ├── conceito.md
│       ├── exercicio.md
│       ├── explain.md
│       ├── notebook.md
│       ├── sql.md
│       ├── revisar.md
│       ├── debug.md
│       ├── viz.md
│       ├── projeto.md
│       ├── cheatsheet.md
│       ├── comparar.md
│       ├── plano.md
│       ├── qualidade.md
│       ├── agentes.md
│       ├── continuar.md
│       └── licao.md
├── .vscode/
│   └── settings.json            # Spell checker pt-BR + EN
└── notebooks/                   # Notebooks de estudo por fase
    └── phase-01-fundamentals/
        ├── 01-programming-logic/
        │   ├── 01_algorithms.ipynb
        │   ├── 02_variables_and_types.ipynb
        │   └── 03_control_flow.ipynb
        └── 02-python-basics/
            ├── 01_syntax.ipynb
            ├── 02_conditionals.ipynb
            ├── 03_loops.ipynb
            └── 04_functions.ipynb
```

---

### Camada 7 — Bibliotecas de Skills e Referências Externas 📚

Projetos de referência adicionais localizados em `OneDrive\Documentos\Data Analysis Road\`. Organizados por relevância para o roadmap.

#### Claude-Skills-main ⭐ Alta relevância
**GitHub**: https://github.com/borghei/Claude-Skills

**O que é**: biblioteca universal com 245 skills em 14 domínios, 653 ferramentas Python, 32 agentes. Inclui domínio `data-analytics/` com 5 skills profissionais diretamente alinhadas ao roadmap.

| Skill | Quando usar |
|---|---|
| `data-analytics/data-analyst` | Fase 2–4 — SQL avançado, visualizações, métricas de negócio, framework "What/So What/Now What" |
| `data-analytics/data-scientist` | Fase 3+ — testes de hipótese, modelagem preditiva, experimentos |
| `data-analytics/business-intelligence` | Fase 4+ — dashboards, KPIs, self-service analytics |
| `data-analytics/analytics-engineer` | Fase 5–6 — pipelines de dados, dbt, data warehouse |
| `data-analytics/ml-ops-engineer` | Fase 6 — deploy de modelos ML, monitoramento |

> **Não instalar**: 245 skills são demais para um iniciante. Consultar os SKILL.md individualmente quando o tema for relevante à fase atual.

#### agent-toolkit-main ⭐ Alta relevância
**GitHub**: https://github.com/softaworks/agent-toolkit

**O que é**: 47 skills por Leonardo Couy. As skills `session-handoff` e `lesson-learned` foram a base dos comandos `/continuar` e `/licao` do vibe-coding.

| Skill original | Adaptação no vibe-coding | Status |
|---|---|---|
| `session-handoff` | `/continuar` | ✅ Implementado |
| `lesson-learned` | `/licao` | ✅ Implementado |
| `database-schema-designer` | Referência para Fase 2 (SQL) | 📋 Referência futura |
| `mermaid-diagrams` | Diagramas de fluxo de dados | 📋 Referência futura |
| `gepetto` | Planejamento antes de codar | 📋 Referência futura |

#### skills-main (Anthropic oficial) — Média relevância
**GitHub**: https://github.com/anthropics/skills

**O que é**: 19 skills de produção da Anthropic cobrindo API, documentos, design e testing.

| Skill | Fase | Uso |
|---|---|---|
| `xlsx` | Fase 3+ | Leitura e escrita de Excel com Python |
| `pdf` | Fase 3+ | Extração de dados de PDFs |
| `claude-api/python` | Fase 6 | Usar a API Claude em projetos Python |
| `mcp-builder` | Fase 6+ | Construir MCP servers próprios |
| `webapp-testing` | Fase 5 | Testes automatizados com Playwright (Django) |
| `frontend-design` | Fase 5–6 | Princípios de design para Streamlit/Django |

#### fusengine — Baixa relevância
**GitHub**: https://github.com/fusengine/agents

**O que é**: ecossistema de 18 plugins para Claude Code com 82 hooks e 125 skills. Focado em Next.js, Laravel, React, Swift — fora do stack Python/dados.

> Único conceito aproveitável: metodologia **APEX** — framework mental para abordar qualquer problema antes de escrever código:
> - **A**nalyze — entender o problema completamente antes de agir
> - **P**lan — planejar a solução e seus passos
> - **E**xecute — implementar o que foi planejado
> - e**L**icit — colher feedback e observar o resultado
> - e**X**amine — revisar, melhorar e consolidar o aprendizado
>
> Aplicável a qualquer fase do roadmap. Nada a instalar — só o framework mental.

#### vercel-labs — Baixa relevância (Fase 5–6)
**GitHub**: https://github.com/vercel-labs/agent-skills

**O que é**: skills de React/Next.js/React Native da equipe Vercel. Stack errada para o roadmap atual.

| Skill | Fase | Uso |
|---|---|---|
| `web-design-guidelines` | Fase 5–6 | Boas práticas de UI para dashboards Streamlit |

#### agent-skills-main — Baixa relevância (Fase 2+)
**GitHub**: https://github.com/supabase/agent-skills

**O que é**: 2 skills oficiais da Supabase — Supabase e PostgreSQL best practices.

| Skill | Fase | Uso |
|---|---|---|
| `supabase-postgres-best-practices` | Fase 2+ | Referência de boas práticas PostgreSQL |

> Supabase não está no roadmap. PostgreSQL best practices são úteis como leitura complementar na Fase 2.

#### humanlayer-main — Muito baixa relevância (pós-roadmap)
**GitHub**: https://github.com/humanlayer/humanlayer

**O que é**: IDE CodeLayer open-source construído sobre Claude Code, com daemon em Go, UI Tauri+React e aprovações humanas. Infraestrutura de produção para times que escalam agentes.

> Sem aplicação prática até o final do roadmap. Referência futura para engenharia de plataformas de IA.

---

## Próximas Ações (em ordem de prioridade)

1. ✅ ~~Remover diretórios de referência~~ — diretórios da Camada 7 já removidos
2. ✅ ~~Criar token do GitHub~~ — token configurado em `~/.claude/settings.json`
3. ✅ ~~Configurar MCPs pendentes na máquina pessoal~~ — todos os MCPs ativos
4. ✅ ~~Verificar MCPs ativos~~ — concluído
5. **Inicializar Git** — `.gitignore` ✅ já criado. Pendente: `git init`, criar repo no GitHub e primeiro commit (Camada 5)
6. **Continuar Fase 1** — Python básico (Fase 1.2) criado com 4 notebooks. Próximo: Python intermediário — Fase 1.3 (`listas`, `dicionários`, `tuplas`, `conjuntos`)

---

## Notas Técnicas

### Máquina Pessoal (`&lt;usuario-pessoal&gt;`)
- **Node.js instalado em**: `C:/Program Files/nodejs/`
- **Node.js não está no PATH do Git Bash** — usar sempre `cmd /c npx` nos MCPs
- **Python**: a confirmar
- **Configuração global do Claude Code**: `C:\Users\&lt;usuario-pessoal&gt;\.claude\settings.json`

### Máquina Corporativa (`&lt;usuario-corporativo&gt;`)
- **Node.js**: acessível via `cmd` (não está no PATH do Git Bash)
- **Python 3.14.4** instalado em: `C:\Users\&lt;usuario-corporativo&gt;\AppData\Local\Python\pythoncore-3.14-64\`
- **Python no PATH do usuário**: adicionado via registro (nova sessão necessária para ativar)
- **Restrições**: máquina gerenciada — instalações podem exigir aprovação de TI
- **Configuração global do Claude Code**: `C:\Users\&lt;usuario-corporativo&gt;\.claude\settings.json`

### Compartilhado entre as duas máquinas
- **Configuração local do Claude Code**: `learning-env/.claude/settings.json` (via OneDrive)
- **Permissões locais**: `learning-env/.claude/settings.local.json` (auto-gerenciado por máquina)
