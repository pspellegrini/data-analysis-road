Gerencie a continuidade da sessão de estudo: $ARGUMENTS

Se o argumento for "salvar", "encerrar", "pausa" ou vazio ao fim de uma sessão → **Criar marcador**.
Se o argumento for "retomar", "carregar", "onde parei" ou mencionar uma sessão anterior → **Retomar marcador**.

Responda sempre em pt-BR.

---

## CRIAR MARCADOR (fim de sessão)

Crie o arquivo `.claude/handoffs/YYYY-MM-DD-HH-MM-[tema].md` com a seguinte estrutura. Preencha cada seção com base na conversa atual — não deixe nenhuma seção em branco.

```markdown
# Marcador de Sessão — [data e hora]
**Tema:** [assunto principal estudado]
**Fase do roadmap:** [Fase X — nome da fase]

---

## O que foi estudado hoje
[2-4 frases descrevendo os conceitos ou etapas abordados nesta sessão]

## Código ou exercícios realizados
[Lista dos arquivos criados/modificados ou exercícios feitos, com uma linha de descrição cada]

## Onde exatamente parei
[Frase precisa: "Estava no exercício 3 de 5 sobre loops", "Acabei de entender X mas ainda não pratiquei Y"]

## Dificuldades encontradas
[O que foi difícil, o que gerou dúvida, o que precisou de mais tentativas]

## Próximo passo concreto
[Uma ação específica e imediata para começar na próxima sessão — não genérico]

## Perguntas em aberto
[Dúvidas que ficaram sem resposta ou que surgiram e merecem exploração]
```

Após criar o arquivo, informe:
- O caminho do arquivo salvo
- Um resumo de 2 linhas do que foi capturado
- O próximo passo registrado

---

## RETOMAR MARCADOR (início de sessão)

1. Liste os arquivos em `.claude/handoffs/` ordenados por data (mais recente primeiro)
2. Leia o marcador mais recente (ou o que o aluno indicar)
3. Apresente um resumo de retomada no formato:

```
📚 Retomando sessão de [data]
Tema: [tema]
Fase: [fase do roadmap]

Você parou em: [onde parei — frase exata do marcador]

Próximo passo: [próximo passo concreto do marcador]

Dificuldades que ficaram: [dificuldades registradas]
Perguntas em aberto: [perguntas registradas]

Pronto para continuar? Diga "sim" ou me conte o que quer revisar antes.
```

4. Aguarde confirmação antes de prosseguir com qualquer conteúdo novo.

---

## Regras

- Tom: amigável, como um professor que lembra onde o aluno parou
- Nunca invente informação — use apenas o que está na conversa atual (para criar) ou no arquivo (para retomar)
- Se não houver nenhum marcador salvo, diga isso claramente e sugira criar um ao final da próxima sessão
- Arquivos ficam em: `learning-env/.claude/handoffs/`
