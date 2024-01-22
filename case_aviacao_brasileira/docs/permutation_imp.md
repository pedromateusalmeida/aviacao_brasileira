## O que é Importância de Permutação?
A Importância de Permutação (Permutation Importance) é uma técnica de interpretabilidade de modelo que mede a importância de uma característica pela observação de como a pontuação do modelo de predição diminui quando os dados da característica são embaralhados aleatoriamente. Este processo quebra a relação entre a característica e a verdadeira saída, indicando o quanto o modelo depende da característica.<br />

## Como Funciona
A Importância de Permutação envolve os seguintes passos:<br />
1.	Um modelo é treinado no conjunto de dados original e a métrica de desempenho é calculada.<br />
2.	Uma característica individual é aleatoriamente embaralhada e a métrica de desempenho é recalculada.<br />
3.	A importância é dada pela redução na métrica de desempenho devido ao embaralhamento. Uma característica é considerada importante se o embaralhamento piora significativamente o desempenho do modelo.<br />
4.	O processo é repetido para todas as características para obter uma medida de importância para cada uma.<br />


Útil para modelos agnósticos é fácil de calcular e entender. E não demanda saber ou fazer suposições sobre a distribuição dos dados ou a forma do modelo. Porém, pode ser uma técnica computacionalmente cara, pois requer várias reavaliações do modelo e não leva em conta as interações entre características.
<br />

As características com importância alta são aquelas cuja permutação (embaralhamento) leva a uma piora no desempenho do modelo. Uma importância próxima de zero indica que a característica não tem um impacto significativo no desempenho do modelo. Por fim, a Importância de Permutação é uma técnica que, em conjunto com outras de interpretabilidade, como SHAP ou LIME, auxilia bastante no processo de análise e compreensão do modelo.<br />

!!!warning "Cuidados"
    •	Assegure-se de usar um número suficiente de permutações para obter estimativas estáveis.<br />
    •	Considerar a possibilidade de usar a média de várias rodadas de permutação para cada característica para reduzir a variabilidade.<br />
    •	Lembre-se de que a importância de permutação não captura a interação entre características.<br />

[Aplicação do Permutation Importance no Case](https://github.com/pedromateusalmeida/aviacao_brasileira/blob/main/scripts_v2/4_3_feature_selection.ipynb){ .md-button .md-button--primary }

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;