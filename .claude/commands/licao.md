Extraia a lição de aprendizado do que acabou de acontecer nesta sessão: $ARGUMENTS

Se um argumento for fornecido, use-o como foco da análise (ex: "sobre o erro de indentação", "sobre a query SQL", "sobre a lista").
Se não houver argumento, analise o momento mais significativo da conversa atual.

Responda sempre em pt-BR.

---

## O que fazer

### Passo 1 — Identificar o momento

Olhe para a conversa atual e identifique **um** momento de aprendizado concreto:

- Um erro que foi cometido e corrigido
- Um conceito que ficou mais claro após tentativa e erro
- Uma solução que funcionou depois de várias tentativas
- Uma boa prática que foi aplicada (mesmo sem erro)
- Uma dúvida que foi resolvida

**Se não houver nada significativo**, diga honestamente: "Essa parte foi direta — sem lição profunda aqui, só boa execução."

### Passo 2 — Apresentar a lição

Use este formato:

```
## Lição: [Nome do princípio em 3-6 palavras]

**O que aconteceu:**
[1-2 frases descrevendo o erro ou situação concreta — referencie o código ou contexto real]

**O princípio:**
[1-2 frases explicando o conceito de programação ou análise de dados por trás disso]

**Por que isso importa:**
[1 frase sobre o que vai errado se esse princípio for ignorado no futuro]

**Próxima vez:**
[Uma ação concreta e específica que o aluno pode aplicar na próxima situação similar]
```

Se houver uma segunda lição menor que vale mencionar:

```
---

### Também vale notar: [Nome]
**No código:** [1 frase]
**O princípio:** [1 frase]
**Próxima vez:** [1 frase]
```

---

## Regras de tom

- **Reflexivo, não prescritivo** — use "o que aconteceu aqui mostra que..." em vez de "você deveria ter..."
- **Específico, não genérico** — cada afirmação deve apontar para algo real da conversa
- **Reconheça o que funcionou** — nem toda lição é sobre erro; reforçar boas práticas é igualmente valioso
- **Máximo 2 lições** — uma bem fundamentada vale mais que cinco vagas
- **Linguagem acessível** — explique o princípio como se o aluno nunca tivesse ouvido o nome antes

---

## Exemplos de princípios aplicáveis

| Situação | Princípio |
|---|---|
| Variável com nome `x` ou `temp` causou confusão | Nomes descritivos economizam debugs futuros |
| Loop que poderia ser list comprehension | Expressividade reduz erros de leitura |
| `except` vazio que escondeu o erro real | Exceções precisam de contexto para ajudar |
| Query sem `WHERE` que retornou tudo | Filtros explícitos protegem contra surpresas |
| Célula do notebook dependia de outra não executada | Notebooks devem rodar do zero sem surpresas |
| Variável reutilizada com valor diferente | Uma variável, um propósito |
| Função de 40 linhas difícil de entender | Funções pequenas são mais fáceis de testar e corrigir |
| Dado não validado antes de processar | Validação na entrada evita erro no meio do caminho |
