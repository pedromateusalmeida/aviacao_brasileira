O Teste de Kruskal-Wallis é um método não paramétrico usado para determinar se há diferenças estatisticamente significativas entre as medianas de dois ou mais grupos independentes. É uma alternativa ao teste ANOVA quando as suposições deste último não são satisfeitas. <br />

## O que Observar no Teste de Kruskal-Wallis
•	Estatística K (K-Statistic): Esta é a estatística do teste, que mede a diferença entre os grupos. Um valor alto de K sugere diferenças significativas entre as medianas dos grupos.<br />
•	P-valor: Indica a probabilidade de observar uma estatística K tão extrema quanto a observada sob a hipótese nula de que todas as medianas dos grupos são iguais. Um p-valor baixo (geralmente menor que 0,05) sugere a rejeição da hipótese nula.<br />
## O que Prestar Atenção
•	P-valor: É o indicador mais importante. Um p-valor abaixo de 0,05 indica diferenças significativas entre as medianas dos grupos.<br />
•	Tamanho da Amostra: O Teste de Kruskal-Wallis pode ser aplicado a amostras de tamanhos diferentes, mas é importante estar atento a tamanhos de amostra muito pequenos, que podem afetar a confiabilidade dos resultados.<br />
## Cuidados
•	Independência das Observações: O teste assume que as observações em cada grupo são independentes. Garanta que essa suposição seja válida.<br />
•	Distribuição dos Dados: Embora o teste de Kruskal-Wallis não exija normalidade dos dados, é importante que as distribuições de cada grupo sejam similares. Distribuições muito diferentes podem afetar a validade do teste.<br />
•	Interpretação: Um resultado significativo indica apenas que pelo menos um dos grupos difere dos outros em termos de mediana, mas não especifica quais grupos são diferentes. Testes post hoc podem ser necessários para investigações adicionais.<br />
## Aplicabilidade
•	Quando Usar: Use o teste de Kruskal-Wallis quando você tiver três ou mais grupos independentes para comparar e quando as suposições do teste ANOVA (normalidade e homogeneidade das variâncias) não forem satisfeitas.<br />
•	Grupos Independentes: Adequado para comparar medianas entre dois ou mais grupos independentes.<br />
•	Dados Ordinais ou Contínuos: Pode ser aplicado a dados ordinais ou contínuos que não seguem uma distribuição normal.<br />
•	Amostras Pequenas: Particularmente útil para amostras pequenas.<br />
## Prós e Contras
### Prós:
•	Flexibilidade: Pode ser usado com dados que não são normalmente distribuídos.<br />
•	Robustez: Menos sensível a outliers do que testes paramétricos.<br />
### Contras:
•	Poder Estatístico: Geralmente tem menos poder estatístico do que ANOVA para dados que atendem às suposições paramétricas.<br />
•	Limitações na Interpretação: Não indica qual grupo difere dos outros; análises adicionais são necessárias para investigações mais profundas.<br />
### Interpretação e Cuidados
•	Um valor p baixo (geralmente <0.05) indica que pelo menos um grupo difere significativamente dos outros.<br />
•	A significância estatística não especifica quais grupos são diferentes; testes post hoc são necessários para essas comparações.<br />
•	Verificar a adequação das suposições do teste e a independência dos grupos é crucial.<br />


<center>
[Repositório do Case](https://github.com/pedromateusalmeida/aviacao_brasileira){ .md-button .md-button--primary }
<center>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;