## Teste Exato de Fisher

## O que é o Teste Exato de Fisher?
O Teste Exato de Fisher é uma técnica estatística usada para determinar se há associações significativas entre duas variáveis categóricas em tabelas de contingência, especialmente útil para amostras de tamanho pequeno. Diferente do teste de Chi-Quadrado, o Teste de Fisher não depende de uma distribuição de amostragem aproximada e é exato. A hipótese adotada pelo teste exato de fisher é:<br />
H0: Assume que não há associação entre as variáveis (hipótese de independência).<br />
Ha: Assume que  há associação entre as variáveis (hipótese de dependência).<br /><br />

Os testes exatos são assim chamados porque usam a distribuição exata da variável que originou os dados observados, com a qual é calculado o valor-p do teste. Ele é frequentemente usado em estudos de caso-controle para avaliar a associação entre a exposição a um fator de risco e a presença de uma determinada doença. Um destaque a ser feito é que em contextos voltados para estudos de caso-controle de doença geralmente há um desbalanceamento na base.<br />


## Interpretação
Em resumo, o teste calcula a probabilidade exata de observar uma tabela de contingência como a dada . Usa a distribuição hipergeométrica para calcular a probabilidade de cada possível distribuição de frequências sob a hipótese de independência e soma essas probabilidades para obter o valor p.O valor p baixo sugere que existe uma associação significativa entre as variáveis, vale lembrar que um valor p significativo não implica causalidade.<br />


## Resumo 
O teste de exato de fisher não requer que as frequências esperadas sejam altas, tornando-o adequado para amostras pequenas, logo é mais preciso que o teste de Chi-quadrado. E pode ser aplicado independentemente da forma da distribuição dos dados. Sua aplicação em alguns casos pode demandar o uso computacionalmente intensivo para tabelas de contingência maiores. O que torna ele menos poderoso que o teste de Chi-Quadrado para amostras maiores.<br />

!!!warning "Cuidados ao utilizar o Teste de Fisher"
    •	Não deve ser usado para amostras grandes devido ao seu custo computacional.<br />
    •	Cuidado ao interpretar tabelas de contingência com muitas células vazias ou com frequências muito baixas.<br />
    •	Considerar o contexto e as hipóteses subjacentes antes de tirar conclusões baseadas apenas no valor p.<br />
    •	Comparação com o Chi-Quadrado: O Teste de Fisher é frequentemente usado quando o teste de Chi-Quadrado não é apropriado devido ao tamanho da amostra ou a frequências esperadas baixas.<br />
    •	Visualizações: Gráficos de barras ou de mosaico podem ser usados para visualizar as relações entre variáveis categóricas antes de aplicar o Teste de Fisher.

## No case
Está técnica não foi aplicada no case

## Referências

- [Wikipedia - Teste Exato de Fisher](https://pt.wikipedia.org/wiki/Teste_exato_de_Fisher)<br />

- [Psicometria Online - Teste Exato de Fisher](https://psicometriaonline.com.br/teste-exato-de-fisher/)<br />

- [UFBA - Teste Exato de Fisher (PDF)](https://est.ufba.br/sites/est.ufba.br/files/kim/matd49-aula04-fisher.pdf)<br />

- [Medium - Estatística: Teste Exato de Fisher e Teste de Qui-Quadrado usando R](https://medium.com/omixdata/estat%C3%ADstica-teste-exato-de-fisher-e-teste-de-qui-quadrado-usando-r-4ee496da37fc)<br />

- [Larissa Matos (UFBA) - Aula sobre Teste Exato de Fisher (PDF)](https://larissamatos.github.io/Disciplinas/ME_111_1s2018/Aula7.pdf)<br />

- Material da especialização da UFMG<br />


