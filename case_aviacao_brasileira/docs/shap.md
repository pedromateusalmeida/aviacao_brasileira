##SHAP (SHapley Additive exPlanations)
## O que é SHAP?
SHAP é uma abordagem de interpretação de modelo baseada na teoria dos jogos que atribui a cada característica um valor que representa sua importância na previsão de cada instância. Os valores SHAP são baseados nos valores de Shapley, um conceito da teoria dos jogos cooperativos que distribui a "recompensa" (ou seja, a previsão do modelo) entre os colaboradores (recursos) de forma justa.<br />
## Como Funciona
A interpretação do modelo com SHAP envolve os seguintes passos:<br />
1.	Para uma dada instância, o modelo faz uma previsão usando todas as características.<br />
2.	Subconjuntos de características são sistematicamente "desligados" (simulando a ausência de informações), e a previsão é feita sem
eles. <br />
3. O impacto de cada característica na mudança da previsão em relação à previsão base (a previsão média para o conjunto de dados) é calculado. Este impacto é o valor SHAP para a característica naquela instância.<br />
4.	Todos os valores possíveis de subconjuntos de características são considerados para calcular o valor SHAP final para cada característica, o que garante uma distribuição justa e consistente de importância entre as características.<br />
## Aplicabilidade
SHAP é útil quando:<br />
•	É necessário explicar as previsões de um modelo em um nível individual, isto é, para uma instância específica.<br />
•	Queremos entender o modelo de forma global, observando a importância média das características em todas as instâncias.<br />
•	Precisamos de uma interpretação consistente e justa da contribuição das características, baseada na teoria dos jogos.<br />
## Prós e Contras
### Prós
•	Fornece interpretações locais e globais do modelo.<br />
•	Baseia-se em uma base teórica sólida (valores de Shapley), garantindo justiça e consistência.<br />
•	Aplicável a qualquer modelo de Machine<br />
Learning, sendo considerado modelo-agnóstico.<br />
•	Os valores SHAP podem ser facilmente visualizados e interpretados através de gráficos de força, gráficos de resumo, entre outros.<br />
### Contras
•	Computacionalmente intensivo, especialmente para modelos com um grande número de características e dados.<br />
•	A interpretação dos valores SHAP pode ser complexa devido à sua natureza distributiva e ao grande número de subconjuntos de características possíveis.<br />
•	Pode ser desafiador para modelos com interações complexas entre as características.<br />
## Interpretação e Cuidados
### Ao interpretar os valores SHAP
•	Valores SHAP positivos indicam que a característica aumentou a previsão, enquanto valores negativos indicam uma diminuição.<br />
•	A magnitude do valor SHAP reflete a força da contribuição da característica, independente do sinal.<br />
•	É importante analisar tanto os valores SHAP individuais (interpretação local) quanto a distribuição dos valores SHAP em todo o conjunto de dados (interpretação global).<br />
### Cuidados ao utilizar SHAP
•	Deve-se estar ciente do custo computacional e considerar o uso de aproximações ou um número menor de subconjuntos para modelos grandes.<br />
•	É importante compreender as limitações do modelo de Machine Learning subjacente, pois os valores SHAP refletem a estrutura do modelo.<br />
•	Ao interpretar os resultados, deve-se ter em mente que a soma dos valores SHAP para todas as características aproxima a diferença entre a previsão para uma instância específica e a previsão média do modelo.<br />
## Informações Adicionais
•	Visualizações com SHAP: As bibliotecas de SHAP incluem muitas visualizações úteis que podem ajudar na interpretação, como bee swarm plots, bar plots, e waterfall plots.<br />
•	Consistência com Atribuição de Importância: Os valores SHAP são consistentes em sua atribuição; se uma característica contribui mais para a previsão do que outra, seu valor SHAP será maior.<br />

<br />

</div>
<center>
[Repositório do Case](https://github.com/pedromateusalmeida/aviacao_brasileira){ .md-button .md-button--primary }
<center>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;