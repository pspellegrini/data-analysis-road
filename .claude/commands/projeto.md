Crie a estrutura completa de um novo projeto de análise de dados chamado: $ARGUMENTS

Antes de criar, explique em pt-BR:
- O que é uma boa estrutura de projeto e por que organização importa
- O que cada pasta e arquivo vai conter

Crie a seguinte estrutura de arquivos e pastas:

```
nome-do-projeto/
├── dados/
│   ├── brutos/          ← dados originais, nunca modificar
│   └── processados/     ← dados após limpeza e transformação
├── notebooks/
│   ├── 01_exploracao.ipynb     ← EDA inicial
│   ├── 02_limpeza.ipynb        ← limpeza e preparação
│   └── 03_analise.ipynb        ← análise principal
├── src/
│   └── helpers.py       ← funções reutilizáveis do projeto
├── outputs/
│   ├── graficos/        ← visualizações exportadas
│   └── relatorios/      ← relatórios finais
├── .gitignore           ← arquivos a ignorar no git
├── requirements.txt     ← bibliotecas necessárias
└── README.md            ← descrição do projeto
```

Para cada arquivo, gere o conteúdo inicial adequado:
- `notebooks/01_exploracao.ipynb` — scaffold completo com seções e células Markdown
- `src/helpers.py` — estrutura básica com exemplos de funções úteis comentadas
- `.gitignore` — configurado para Python e Jupyter
- `requirements.txt` — bibliotecas comuns de análise de dados
- `README.md` — template com seções: Objetivo, Dados, Estrutura, Como executar

Explique como iniciar o git no projeto e fazer o primeiro commit.
