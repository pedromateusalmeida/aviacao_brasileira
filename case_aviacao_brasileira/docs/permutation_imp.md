## O que é Importância de Permutação?
A Importância de Permutação é uma técnica de interpretabilidade de modelo que mede a importância de uma característica pela observação de como a pontuação do modelo de predição diminui quando os dados da característica são embaralhados aleatoriamente. Este processo quebra a relação entre a característica e a verdadeira saída, indicando o quanto o modelo depende da característica.<br />
## Como Funciona
A Importância de Permutação envolve os seguintes passos:<br />
1.	Um modelo é treinado no conjunto de dados original e a métrica de desempenho é calculada.<br />
2.	Uma característica individual é aleatoriamente embaralhada e a métrica de desempenho é recalculada.<br />
3.	A importância é dada pela redução na métrica de desempenho devido ao embaralhamento. Uma característica é considerada importante se o embaralhamento piora significativamente o desempenho do modelo.<br />
4.	O processo é repetido para todas as características para obter uma medida de importância para cada uma.<br />
## Aplicabilidade
A Importância de Permutação é útil quando:<br />
•	Precisamos de uma medida de importância de característica que seja independente do modelo.<br />
•	Queremos avaliar a importância de características em modelos não lineares ou complexos.<br />
•	Desejamos uma técnica que possa ser aplicada após o modelo ser treinado.<br />
## Prós e Contras
### Prós
•	Modelo agnóstico: pode ser aplicado a qualquer modelo.<br />
•	Fácil de calcular e entender.<br />
•	Não faz suposições sobre a distribuição dos dados ou a forma do modelo.<br />
### Contras
•	Pode ser computacionalmente caro, pois requer várias reavaliações do modelo.<br />
•	Não leva em conta as interações entre características.<br />
•	Pode ser afetada pela aleatoriedade no embaralhamento, especialmente se o número de permutações não for suficientemente grande.<br />
## Interpretação e Cuidados
### Ao interpretar os resultados de Importância de Permutação:
•	Características com importância alta são aquelas cuja permutação (embaralhamento) leva a uma piora no desempenho do modelo.<br />
•	Uma importância próxima de zero indica que a característica não tem um impacto significativo no desempenho do modelo.<br />
### Cuidados ao utilizar Importância de Permutação
•	Assegure-se de usar um número suficiente de permutações para obter estimativas estáveis.<br />
•	Considerar a possibilidade de usar a média de várias rodadas de permutação para cada característica para reduzir a variabilidade.<br />
•	Lembre-se de que a importância de permutação não captura a interação entre características.<br />
## Informações Adicionais
•	Interpretabilidade Adicional: A importância de permutação pode ser complementada com outras técnicas de interpretabilidade, como SHAP ou LIME, para uma análise mais aprofundada.<br />


<center>
[Repositório do Case](https://github.com/pedromateusalmeida/aviacao_brasileira){ .md-button .md-button--primary }
<center>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;