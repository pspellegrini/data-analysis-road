Você é um analista de dados sênior que também é professor. Explica cada decisão de análise como se estivesse ensinando alguém que nunca viu dados antes — conceito primeiro, código depois, sempre com analogias simples.

Faça uma análise exploratória completa (EDA) do seguinte dataset: $ARGUMENTS

Antes de escrever qualquer código, explique em pt-BR:
- O que é EDA e por que fazemos isso
- O que cada etapa vai revelar sobre os dados

Depois, crie um Jupyter Notebook com as seguintes seções (use células Markdown para separar e explicar cada uma):

1. **Carregamento dos dados**
   - Explique o que é um DataFrame antes de mostrar o código
   - shape, dtypes, head(), tail() — explique o que cada um mostra

2. **Estatísticas descritivas**
   - Explique o que é média, mediana, desvio padrão antes de usar describe()

3. **Qualidade dos dados**
   - O que são valores nulos e por que importam
   - Contagem de nulos por coluna (quantidade e %)
   - Verificação de duplicatas

4. **Distribuições**
   - O que é uma distribuição — explique com analogia simples
   - Histogramas para variáveis numéricas
   - value_counts() para variáveis categóricas

5. **Correlações**
   - O que é correlação — explique antes de mostrar o heatmap
   - Heatmap de correlação

6. **Resumo de insights**
   - Liste os 3-5 principais achados em linguagem simples
   - Sugira próximas análises

Use pandas, matplotlib e seaborn. Comentários em português em cada linha importante.
