## O que é Importância Baseada em Modelo?
A Importância Baseada em Modelo é uma abordagem onde se utiliza um modelo de aprendizado de máquina, como uma árvore de decisão ou floresta aleatória, para estimar a importância de cada recurso. Os modelos baseados em árvores fornecem um valor de importância para cada recurso, que reflete quão útil ou valioso cada recurso foi na construção das árvores de decisão dentro do modelo.<br />
## Como Funciona
Para modelos baseados em árvores, como árvores de decisão e florestas aleatórias, a importância é calculada da seguinte maneira:<br />
1.	Durante a construção da árvore, é possível calcular o quanto cada característica contribui para a redução da impureza em cada divisão. Esta contribuição é somada para cada característica e normalizada no final do treinamento.<br />
2.	Para florestas aleatórias, esta medida é calculada para cada árvore e depois é feita uma média para obter a importância de cada característica.<br />
## Aplicabilidade
A Importância Baseada em Modelo é particularmente útil quando:<br />
•	Usamos modelos baseados em árvores e queremos entender quais recursos são mais informativos.<br />
•	Desejamos uma interpretação rápida e integrada da importância dos recursos que vem diretamente do modelo de aprendizado de máquina.<br />
## Prós e Contras
### Prós
•	Fornecida diretamente pelo modelo, sem necessidade de cálculos adicionais.<br />
•	Leva em conta a interação entre recursos, já que a árvore de decisão considera várias variáveis ao fazer divisões.<br />
•	Pode ser calculada rapidamente e é intuitiva.<br />
### Contras
•	Específica para modelos baseados em árvores e pode não se generalizar para outros tipos de modelos.<br />
•	Em modelos de árvores complexos ou florestas aleatórias, a importância pode favorecer características com mais categorias ou valores numéricos contínuos.<br />
•	Pode ser enganosa se houver variáveis correlacionadas, pois a importância pode ser distribuída entre elas.<br />
## Interpretação e Cuidados
Quando interpretamos a Importância Baseada em Modelo:<br />
•	Devemos olhar para as características mais importantes como aquelas que têm mais influência nas decisões do modelo.<br />
•	É importante considerar o contexto do modelo e se as características importantes fazem sentido para o problema em questão.<br />
Cuidados ao utilizar a Importância Baseada em Modelo:<br />
•	A importância pode ser afetada se as características estiverem em escalas diferentes; por isso, às vezes é recomendável padronizar ou normalizar os dados.<br />
•	A presença de características correlacionadas pode distorcer a importância real e deve ser tratada com cautela.<br />
•	Não assuma que as características menos importantes não têm nenhum valor; elas podem ser importantes em modelos diferentes.<br />
## Informações Adicionais
•	Interpretação Adicional: O uso de visualizações como gráficos de barras pode ajudar na interpretação e apresentação das importâncias dos recursos.<br />
•	Modelos compatíveis: Enquanto a importância baseada em modelo é mais comum em árvores de decisão e florestas aleatórias, outros modelos baseados em árvores, como gradient boosting machines (GBMs), também fornecem métricas de importância semelhantes.<br />
<center>
[Repositório do Case](https://github.com/pedromateusalmeida/aviacao_brasileira){ .md-button .md-button--primary }
<center>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;