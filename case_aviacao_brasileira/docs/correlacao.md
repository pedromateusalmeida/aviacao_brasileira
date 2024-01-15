!!!warning
    O conteúdo foi produzido com o Chatgpt. Eu passei alguns materiais e passei alguns direcionamentos. Ainda é necessário inserir bibliografia e aprofundar nos tópicos. 
## O que é Análise de Correlação?
A Análise de Correlação é uma técnica estatística que avalia como as variáveis estão relacionadas entre si. Em termos de seleção de recursos, ela é usada para identificar características que têm forte correlação com a variável alvo.<br />
## Como Funciona
•	Calcula-se um coeficiente de correlação (como Pearson, Spearman ou Kendall) entre cada característica e a variável alvo.<br />
•	Características com alta correlação (positiva ou negativa) com a variável alvo são consideradas importantes.<br />
## Aplicabilidade
•	Útil em conjuntos de dados com muitas variáveis numéricas.<br />
•	Pode ser usada para eliminar características redundantes ou pouco informativas.<br />
## Prós e Contras
### Prós
•	Simples de entender e fácil de implementar.<br />
•	Ajuda na redução de dimensionalidade e na melhoria da eficiência do modelo.<br />
## Contras
•	Só capta relações lineares entre as variáveis.<br />
•	Não detecta interações complexas entre características.<br />
•	Pode levar à exclusão de características importantes em relações não lineares.<br />
## Cuidados
•	Deve-se considerar o tipo de correlação a ser usado baseado na natureza dos dados.<br />
•	Não descartar automaticamente características com baixa correlação, pois podem ser úteis em combinação com outras.<br />


## Teste de Correlação de Pearson
O coeficiente de correlação de Pearson é uma medida estatística que quantifica a relação linear entre duas variáveis quantitativas. É um dos métodos mais comuns para avaliar a força e a direção da associação linear entre variáveis contínuas.<br />

### Como Funciona o Teste de Correlação de Pearson
Cálculo do Coeficiente: O coeficiente de Pearson (denotado como r) varia entre -1 e 1. Um valor de r = 1 indica uma correlação positiva perfeita, r = -1 indica uma correlação negativa perfeita, e r = 0 significa que não há correlação linear.<br />
Fórmula: O coeficiente de Pearson é calculado como a covariância das variáveis dividida pelo produto dos seus desvios padrão.<br />
Significância Estatística: Testes estatísticos podem ser usados para avaliar se o coeficiente de correlação é significativamente diferente de zero, indicando uma relação linear significativa.<br />

### Aplicabilidade do Teste
Dados Contínuos: Adequado para dados quantitativos contínuos.<br />
Relações Lineares: Utilizado quando se suspeita que a relação entre as variáveis é linear.<br />
Análise Exploratória: Comumente usado na análise exploratória de dados para identificar relações potenciais entre variáveis.<br />

### Prós e Contras
#### Prós
Simplicidade e Facilidade de Interpretação: O coeficiente de Pearson é fácil de calcular e interpretar, fornecendo uma medida clara da força e direção da relação linear.<br />
Amplamente Utilizado e Aceito: É um método estatístico padrão, amplamente reconhecido e utilizado em diversas áreas.<br />
#### Contras
Apenas para Relações Lineares: Limita-se a capturar relações lineares, não sendo adequado para relações não lineares.<br />
Sensível a Outliers: Pode ser fortemente influenciado por outliers, o que pode distorcer os resultados.<br />
Pressupõe Distribuição Normal: Para inferência estatística sobre o coeficiente, é ideal que as variáveis sigam uma distribuição normal.<br />

### Interpretação e Cuidados
O valor de r deve ser interpretado no contexto do tamanho da amostra; correlações mais baixas podem ser significativas em grandes amostras.<br />
Correlação não implica causalidade. Uma correlação significativa entre duas variáveis não significa que uma causa a outra.<br />
Avaliar a presença de outliers é essencial, pois eles podem ter um impacto significativo no coeficiente de correlação.<br />

<center>
[Repositório do Case](https://github.com/pedromateusalmeida/aviacao_brasileira){ .md-button .md-button--primary }
<center>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;