<div style="text-align: justify">
O Teste de Kruskal-Wallis é não paramétrico. É uma alternativa não-paramétrica à Análise de Variância. É usado para determinar se há diferenças estatisticamente significativas entre as medianas de dois ou mais grupos independentes. Ele testa a hipótese nula de que as populações de onde vieram as amostras são idênticas, e isso pode ser feito com dados de nível ordinal. <br /><br />
Hipóteses: <br />
H0: as populações de onde vieram as amostras são idênticas.<br />
Ha: as populações de onde vieram as amostras são diferentes.<br /><br />

Se as populações são idênticas (H0 verdadeira), a estatística H assumirá um valor pequeno. Caso contrário, H tende a assumir valores grandes. Segue aproximadamente a distribuição Qui-quadrado com (k-1) de liberdade<br /><br />

Uma condição para aplicar o teste - porém para o contexto de Big Data não chega a ser um obstáculo - é ter ao menos cinco observações (para se usar a distribuição Qui-quadrado como distribuição de referência). O teste de Kruskal-Wallis tem aplicabilidade quando temos três ou mais grupos independentes para comparar e quando as suposições do teste ANOVA (normalidade e homogeneidade das variâncias) não forem satisfeitas.<br />
</div>

!!!info "Dicas importantes"
    •	Adequado para comparar medianas entre dois ou mais grupos independentes.<br />
    •	Pode ser aplicado a dados ordinais ou contínuos que não seguem uma distribuição normal.<br />
    •	Particularmente útil para amostras pequenas.<br />

## O que observar no Teste de Kruskal-Wallis
<div style="text-align: justify">
Para começar, o K (K-Statistic), essa é a estatística do teste que mede a diferença entre os grupos. Um valor alto de K sugere diferenças significativas entre as medianas dos grupos. Já o p-valor indica a probabilidade de observar uma estatística K tão extrema quanto a observada sob a hipótese nula de que todas as medianas dos grupos são iguais. Um p-valor baixo (geralmente menor que 0,05) sugere a rejeição da hipótese nula. Um valor p baixo (geralmente <0.05) indica que pelo menos um grupo difere significativamente dos outros. <br />
</div>

!!!warning "Cuidados"
    •	O teste assume que as observações em cada grupo são independentes. Deve-se garantir que essa suposição seja válida.<br />
    •	Embora o teste de Kruskal-Wallis não exija normalidade dos dados, é importante que as distribuições de cada grupo sejam similares. Distribuições muito diferentes podem afetar a validade do teste.<br />
    •	Um resultado significativo indica apenas que pelo menos um dos grupos difere dos outros em termos de mediana, mas não especifica quais grupos são diferentes. Testes post hoc podem ser necessários para investigações adicionais.<br />

## Resumo
<div style="text-align: justify">
A significância estatística não especifica quais grupos são diferentes; testes post hoc são necessários para essas comparações. Verificar a adequação das suposições do teste e a independência dos grupos é crucial. O p-valor é um o indicador mais importante, valores abaixo de 0,05 indica diferenças significativas entre as medianas dos grupos.<br /><br />

É um teste flexivel, ou seja, ele permite ser utilizado com dados que não são normalmente distribuídos e é menos sensível a outliers, como é o ANOVA. Em contrapartida, tem menos poder estatístico do que ANOVA para dados que atendem às suposições paramétricas e tem uma limitação na sua interpretação que é não indicar qual grupo difere dos outros; análises adicionais são necessárias para investigações mais profundas<br />
</div>

## No Case
<div style="text-align: justify">
Como é possível visualizar na análise exploratória, mais especificamente nos boxplots dos dados meteorológicos, podemos ver que os dados seguem uma distribuição com poucos casos de outliers. Temos uma média e uma mediana com valores próximos e um desvio padrão pequeno. Um cenário adequado para ANOVA, mas isso não quer dizer que não possa ser utilizado como ténica de seleção de recursos ou até como complemento de validação.  <br />
</div>
<br />
<center>
[Aplicação do Kruskal-Wallis no Case](https://github.com/pedromateusalmeida/aviacao_brasileira/blob/main/scripts_v2/4_3_feature_selection.ipynb){ .md-button .md-button--primary }
<center>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

## Referências

- [UFSC - Teste Não Paramétrico Kruskal-Wallis (PDF)](https://www.inf.ufsc.br/~vera.carmo/Testes_de_Hipoteses/Teste_Nao_parametrico_Kruskal-Wallis.pdf)<br />

- [Wikipedia - Teste de Kruskal-Wallis](https://pt.wikipedia.org/wiki/Teste_de_Kruskal-Wallis)<br />

- [Ermontoro - Teste de Kruskal-Wallis](https://www.ermontoro.com/post/teste-de-kruskal-wallis)<br />

- [USP - Teste de Kruskal-Wallis (PDF)](https://edisciplinas.usp.br/pluginfile.php/1064940/mod_resource/content/2/Teste%20de%20KW.pdf)<br />

- [Teste de Kruskal-Wallis ](https://sites.google.com/site/qualidadeeprodutividade/six-sigma/analyze/2-1-3-4-analise-de-variancia-anova/2-3-4-4-an%C3%A1lise-n%C3%A3o-param%C3%A9trica-de-dois-ou-mais-grupos/2-3-4-4-1-teste-de-kruskal-wallis)<br />

- Material da especialização da UFMG<br />


