Valide a qualidade do seguinte código/notebook/script de análise de dados: $ARGUMENTS

Percorra cada item abaixo em ordem. Se o item não for aplicável ao código analisado, pule-o. Para cada problema encontrado, explique o que é, por que importa e como corrigir — sempre de forma didática, em pt-BR.

---

## 1. Segurança básica (verifique primeiro, sempre)

- [ ] Há credenciais, senhas, tokens ou chaves de API no código?
  - Se sim: PROBLEMA CRÍTICO. Explique como usar variáveis de ambiente com `python-dotenv` ou `os.environ`
- [ ] Há caminhos absolutos hardcoded que expõem estrutura de pastas do sistema?

---

## 2. Reprodutibilidade do notebook (se for .ipynb)

- [ ] O notebook executa completamente do zero sem erros? (simule um `Restart & Run All`)
- [ ] As células estão em ordem lógica — sem dependência de execução fora de sequência?
- [ ] Imports estão todos na primeira célula?
- [ ] O caminho para leitura de arquivos funciona em outra máquina?

---

## 3. Qualidade do código Python

- [ ] Há `except` genérico ou vazio? Mostre como capturar exceções com contexto
- [ ] Há loops `for` em DataFrames onde `apply` ou operações vetorizadas resolveriam? Explique a diferença de performance
- [ ] Variáveis têm nomes descritivos em inglês (`snake_case`)? Ex: `df_vendas`, não `x` ou `temp`
- [ ] Há prints de debug que deveriam ser removidos ou comentados?
- [ ] Há código duplicado que poderia ser uma função?

---

## 4. Qualidade das queries SQL (se houver)

- [ ] Todas as queries têm `WHERE` ou `LIMIT` explícito?
- [ ] Há `SELECT *` onde colunas específicas seriam mais seguro e eficiente?
- [ ] Nomes de colunas e tabelas estão claros e seguem uma convenção?

---

## 5. Documentação e clareza

- [ ] Notebook tem células Markdown explicando o que cada seção faz?
- [ ] Funções têm docstrings ou comentários explicando o propósito?
- [ ] Visualizações têm título, rótulos nos eixos e legenda quando necessário?

---

## 6. Dados e persistência

- [ ] O código modifica o DataFrame original quando deveria trabalhar em uma cópia? (risco de efeitos colaterais)
- [ ] Há operações destrutivas (deletar linhas/colunas) sem confirmação ou backup?

---

## Resultado final

Ao final, apresente:
- **Aprovado** — código está pronto para continuar o aprendizado
- **Melhorias sugeridas** — lista priorizada dos pontos a corrigir (do mais importante ao menos importante)
- **O que estudar** — conceito(s) que o código revela que merecem atenção
