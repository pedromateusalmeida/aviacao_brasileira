## O que é Teste de Chi-Quadrado (χ²)
<div style="text-align: justify">
O teste de Chi-Quadrado é uma técnica estatística usada para determinar se existe uma associação significativa entre duas variáveis categóricas. É frequentemente usado na seleção de recursos para identificar quais características são relevantes para a variável alvo. As hipóteses testadas pelo chi-quadrado é:
H0: As variáveis categóricas são independentes <br />
Ha: As variáveis categóricas são dependentes <br />
</div>
!!!tip "Utilizado em variáveis categóricas para testar a independência entre elas."

<div style="text-align: justify">
O teste compara a distribuição observada das variáveis com a distribuição esperada se não houvesse relação entre elas (independência). O teste calcula um valor de χ² que quantifica a discrepância entre as frequências observadas e esperadas. Quanto maior o valor de χ², maior a evidência contra a hipótese de independência entre as variáveis. É aplicado em tabelas de contingência para avaliar se a distribuição de uma variável é afetada pela presença de outra.<br /><br />
</div>

!!!info "Cuidados"
    •	Um valor de χ² alto sugere que as variáveis não são independentes, ou seja, existe uma relação entre elas.<br />
    •	O valor p associado ao teste indica a probabilidade de observar um valor de χ² tão extremo quanto o calculado, assumindo que as variáveis são independentes.<br />
    •	É importante usar um teste de χ² corrigido (como o de Yates) para tabelas de contingência 2x2 ou quando as frequências esperadas são muito baixas.<br />
    •	Variações: Existem variações do teste de χ², como o Teste de Fisher, que pode ser mais adequado para pequenos tamanhos de amostra.<br />
    •	Visualizações: Gráficos de barras ou de mosaico podem ser úteis para visualizar a relação entre variáveis categóricas antes e após realizar o teste de χ².<br />

## Resumo
<div style="text-align: justify">
O teste de chi-quadrado é simples e fácil de aplicar em dados categóricos, ele pode ser usado mesmo quando os dados não seguem uma distribuição normal e é muito útil para identificar relações entre características que podem ser importantes para a classificação ou previsão (feature selection). Em contrapartida, só é aplicável a variáveis categóricas. Não é adequado para pequenos tamanhos de amostra, pois as estimativas podem ser imprecisas. E por fim vale mencionar que não identifica o tipo de relação entre as variáveis, apenas a existência de uma associação.<br />
</div>

## No Case
<div style="text-align: justify">
No case foi foram utilizadas as variaveis categóricas independentes relacionadas aos voos, por exemplo, cidade de origem, cidade destino, UF origem e destino, aeroporto origem e destino e a variável categórica dependente foi o status do voo (pontual/atrasado).<br />
</div>
<center>
[Aplicação do Chi-Quadrado (χ²) no Case](https://github.com/pedromateusalmeida/aviacao_brasileira/blob/main/scripts_v2/4_3_feature_selection.ipynb){ .md-button .md-button--primary }
<center>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

