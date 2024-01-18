
## O que é Análise de Correlação?
<div style="text-align: justify">
A Análise de Correlação é uma técnica estatística que avalia como as variáveis estão relacionadas entre si. Em termos de seleção de recursos, ela é usada para identificar características que têm forte correlação com a variável alvo. <br /><br />

O coeficiente de correlação (Pearson, Spearman ou Kendall) é calculado entre cada característica e a variável alvo.	Os resultados de alta correlação (positiva ou negativa) com a variável alvo são consideradas importantes. A técnica pode é utilizada para identifica multicolinearidade, se há redundância nas caractéristicas, se são relevantes, além de tudo é uma técnica simples e fácil de ser utilizada. <br /><br />

Existem limitações na correlação que é o fato dela só captar relações lineares entre as variáveis, outros padrões ela não é capaz de identificar. Abaixo temos um gráfico entre duas variáveis X e Y, existe uma correlação entre elas, porém não linear isso não seria captado.<br />
</div>
<center>
[![Image title](correlacao_nao_linear.png)](correlacao_nao_linear.png?data-lightbox="image-1" data-title="My caption")
</center>

!!!warning "Cuidados"
    •	Pode levar à exclusão de características importantes em relações não lineares.<br />
    •	Deve-se considerar o tipo de correlação a ser usado baseado na natureza dos dados.<br />
    •	Não descartar automaticamente características com baixa correlação, pois podem ser úteis em combinação com outras.<br />
    •	Avaliar a presença de outliers é essencial, pois eles podem ter um impacto significativo no coeficiente de correlação.<br />


## Teste de Correlação de Pearson
<div style="text-align: justify">
O coeficiente de correlação de Pearson é uma medida estatística que quantifica a relação linear entre duas variáveis quantitativas. É um dos métodos mais comuns para avaliar a força e a direção da associação linear entre variáveis contínuas.<br />
</div>

### Como Funciona o Teste de Correlação de Pearson
<div style="text-align: justify">
<strong>Cálculo do Coeficiente:</strong> O coeficiente de Pearson (denotado como r) varia entre -1 e 1. Um valor de r = 1 indica uma correlação positiva perfeita, r = -1 indica uma correlação negativa perfeita, e r = 0 significa que não há correlação linear.<br />
<strong>Fórmula:</strong> O coeficiente de Pearson é calculado como a covariância das variáveis dividida pelo produto dos seus desvios padrão.<br />
<strong>Significância Estatística:</strong> Testes estatísticos podem ser usados para avaliar se o coeficiente de correlação é significativamente diferente de zero, indicando uma relação linear significativa.<br />
</div>
!!!tip "Dicas"
    •	rXY é uma estatística adimensional(semunidadede medida);<br />
    •	rXY é apropriadoquandoX e Y sãovariáveisquantitativas;<br />
    •	rXY é o mesmoquer YX(rótulosX e Y intercambiáveis);<br />
    •	Pode ser influenciado por valores atípicos.<br />

<div style="text-align: justify">
O sinal do coeficiente de correlação linear de Pearson afeta diretamente o desenho do gráfico. Abaixo um temos um exemplo dos sinais e qual é a sua localização plano cartesiano de X e Y.<br />
</div>

!!!danger "Cuidados"
    Correlação não implica causalidade. Uma correlação significativa entre duas variáveis não significa que uma causa a outra.

<center>
[![Image title](valor_coef_linear.png)](valor_coef_linear.png?data-lightbox="image-1" data-title="My caption")<br />
Fonte: Material da pós graduação da UFMG. 
</center>

### Quando utilizar?
<div style="text-align: justify">
<strong>Dados Contínuos:</strong> Adequado para dados quantitativos contínuos.<br />
<strong>Relações Lineares:</strong> Utilizado quando se suspeita que a relação entre as variáveis é linear.<br />
<strong>Análise Exploratória:</strong> Comumente usado na análise exploratória de dados para identificar relações potenciais entre variáveis.<br />
</div>


!!!tip "Dicas"
    <center>
    [![Image title](variaveis_medidas_associacao.png)](variaveis_medidas_associacao.png?data-lightbox="image-1" data-title="My caption")<br />
    Fonte: Material da pós graduação da UFMG. 
    </center>

## No case
<div style="text-align: justify">
No case foi utilizado a correlação de pearson na etapa da análise explortatória. Nesse primeiro momento ela foi utilizada com a finalidade de visualizar potenciais correlações entre as colunas. 
</div>

[Aplicação da correlação de pearson no Case](https://github.com/pedromateusalmeida/aviacao_brasileira/blob/main/scripts_v2/3_2_analise_exploratoria.ipynb){ .md-button .md-button--primary }

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

## Referências

- [How can I simply prove that the Pearson correlation coefficient is between -1 and 1? - Math Stack Exchange](https://math.stackexchange.com/questions/564751/how-can-i-simply-prove-that-the-pearson-correlation-coefficient-is-between-1-an)
- [Article on Pearson correlation - SAGE Journals](https://journals.sagepub.com/doi/10.1177/8756479308317006)
- [Correlação Pearson, Spearman, Kendall - Universidade Federal de Santa Catarina](https://www.inf.ufsc.br/~vera.carmo/Correlacao/Correlacao_Pearson_Spearman_Kendall.pdf)
- [Coeficiente de correlação de Pearson - Wikipedia](https://pt.wikipedia.org/wiki/Coeficiente_de_correla%C3%A7%C3%A3o_de_Pearson)

