## O que é PCA?
A Análise de Componentes Principais (PCA) é uma técnica de redução de dimensionalidade que transforma os dados originais em um novo conjunto de variáveis, denominadas componentes principais. Estas componentes são obtidas de forma que a primeira capture a maior variação possível nos dados, e cada componente subsequente tenha a maior variação possível sob a restrição de ser ortogonal às componentes anteriores.<br />
## Como Funciona
O PCA segue os seguintes passos:<br />
1.	Padronizar os dados (média zero e variação unitária).<br />
2.	Calcular a matriz de covariância dos dados padronizados.<br />
3.	Calcular os autovalores e autovetores da matriz de covariância.<br />
4.	Ordenar os autovetores pelo seu autovalor correspondente, em ordem decrescente.<br />
5.	Selecionar os N primeiros autovetores para formar o conjunto de componentes principais, onde N é o número de componentes desejado.<br />
6.	Transformar os dados originais usando este conjunto de autovetores para obter os dados projetados sobre os componentes principais.<br />
## Aplicabilidade
O PCA é aplicável quando:
•	Existe necessidade de reduzir a quantidade de variáveis, mas manter a maior parte da informação.<br />
•	Os dados têm muitas variáveis correlacionadas (multicolinearidade).<br />
•	Deseja-se visualizar a estrutura de alta dimensão dos dados em um espaço de menor dimensão.<br />
## Prós e Contras
### Prós 
•	Reduz a dimensionalidade, diminuindo o espaço de armazenamento e o tempo de computação.<br />
•	Remove a multicolinearidade entre as variáveis.<br />
•	Facilita a visualização dos dados.<br />
### Contras 
•	A seleção de componentes não é baseada na variável de resposta, e sim na variação explicada, o que pode excluir variáveis importantes para a previsão.<br />
•	A interpretabilidade das componentes pode ser difícil, já que elas são combinações lineares das variáveis originais.<br />
•	A perda de informação pode acontecer se um número muito limitado de componentes for selecionado.<br />
## Interpretação e Cuidados
### Na interpretação do PCA 
•	Deve-se considerar a variação total explicada pelas componentes selecionadas.<br />
•	Cada componente é uma mistura das características originais, e o significado dessas misturas pode não ser intuitivamente claro.<br />
•	A análise de carga dos componentes (component loadings) pode ajudar a entender como as variáveis originais contribuem para cada componente.<br />
### Cuidados ao utilizar PCA 
•	A padronização dos dados é crucial, especialmente quando as variáveis têm diferentes unidades de medida.<br />
•	A escolha do número de componentes a serem mantidos deve ser feita com base na quantidade de variação que se deseja capturar.<br />
•	PCA é sensível a outliers, que podem distorcer a direção dos componentes principais.<br />
•	Em contextos supervisionados, é importante usar o PCA de maneira que não incorpore informações do conjunto de teste durante o treinamento.<br />
## Informações Adicionais
•	Interpretabilidade: Ferramentas como o biplot podem ser úteis para interpretar PCA, pois mostram os componentes principais e as contribuições das variáveis originais simultaneamente.<br />
•	Variação Explicada: A proporção de variação explicada por cada componente principal é uma peça-chave para decidir quantos componentes reter.<br />

<br />

</div>
<center>
[Repositório do Case](https://github.com/pedromateusalmeida/aviacao_brasileira){ .md-button .md-button--primary }
<center>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;