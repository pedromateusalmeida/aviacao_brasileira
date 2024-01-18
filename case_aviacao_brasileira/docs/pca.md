<div style="text-align: justify">

A Análise de Componentes Principais (PCA) é uma técnica de redução de dimensionalidade que transforma os dados originais em um novo conjunto de variáveis, denominadas componentes principais. Os elementos que compõem uma componente são ortogonais (não correlacionados e independentes). Estas componentes são obtidas de forma que a primeira capture a maior variação possível nos dados, e cada componente subsequente tenha a maior variação possível sob a restrição de ser ortogonal às componentes anteriores.<br /><br />

O PCA segue os seguintes passos:<br />
1. Padronizar os dados (média zero e variação unitária).<br />
2. Calcular a matriz de covariância dos dados padronizados.<br />
3. Calcular os autovalores e autovetores da matriz de covariância.<br />
4. Ordenar os autovetores pelo seu autovalor correspondente, em ordem decrescente.<br />
5. Selecionar os N primeiros autovetores para formar o conjunto de componentes principais, onde N é o número de componentes desejado.<br />
6. Transformar os dados originais usando este conjunto de autovetores para obter os dados projetados sobre os componentes principais.<br />

</div>

!!!tip "Aplicabilidades"
    • Quando existe a necessidade de reduzir a quantidade de variáveis, mas manter a maior parte da informação.<br />
    • Quando há dados com muitas variáveis correlacionadas (multicolinearidade).<br />
    • Quando se deseja visualizar a estrutura de alta dimensão dos dados em um espaço de menor dimensão.<br />
    • Quando se deseja criar um índice.<br />
    • Para realizar feature selection (aspecto considerado polêmico).<br />

<div style="text-align: justify">

O PCA tem a capacidade de reduzir a dimensionalidade, diminuindo o espaço de armazenamento e o tempo de computação. Ele pode reduzir a multicolinearidade, ou seja, variáveis que possuem uma grande correlação e medem coisas semelhantes podem ser reduzidas a um vetor numérico que represente essas variáveis. No caso aplicado, a técnica do PCA é usada nos elementos meteorológicos de vento e umidade, onde cada um desses elementos possui três métricas relacionadas a eles no dataset. Uma redução é aplicada, criando uma nova coluna chamada componente_umidade e componente_vento, cujos valores desses vetores passam a ser os valores referentes aos elementos meteorológicos de vento e umidade.<br /><br />

A análise de componentes realiza combinações lineares das variáveis originais, o que pode dificultar a interpretabilidade das componentes. No entanto, temos os pesos de cada variável para aquela componente. Assim, ao pegarmos a componente com a maior variância (explicabilidade), geralmente a primeira, podemos observar a carga de cada variável para a componente (component loadings). Apesar de auxiliar no processo de feature selection, o PCA não é adequado para ser utilizado sozinho.<br />

</div>

!!!warning "Cuidados que se deve ter ao interpretar os resultados do PCA."
    • Considerar a variação total explicada pelas componentes selecionadas.<br />
    • A análise de carga dos componentes pode ajudar a entender como as variáveis originais contribuem para cada componente.<br />
    • O PCA é sensível a outliers, que podem distorcer a direção dos componentes principais.<br />
    • A escolha do número de componentes a serem mantidos deve ser feita com base na quantidade de variação que se deseja capturar.<br />
    • Em contextos supervisionados, é importante usar o PCA de maneira que não incorpore informações do conjunto de teste durante o treinamento.<br />
    • Variação Explicada: A proporção de variação explicada por cada componente principal é uma peça-chave para decidir quantos componentes reter.<br />
    • A perda de informação pode ocorrer se um número muito limitado de componentes for selecionado.<br />

## No case
No case, o PCA foi utilizado para reduzir as dimensões de vento e umidade, sendo também aplicado como técnica de feature selection.<br />

[Aplicação do PCA no Case](https://github.com/pedromateusalmeida/aviacao_brasileira/blob/main/scripts_v2/4_3_feature_selection.ipynb){ .md-button .md-button--primary }

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

## Referências

- [Stack Exchange - Usando Análise de Componentes Principais (PCA) para seleção de recursos](https://stats.stackexchange.com/questions/27300/using-principal-component-analysis-pca-for-feature-selection)<br/>
- [Towards Data Science - PCA não é seleção de recursos](https://towardsdatascience.com/pca-is-not-feature-selection-3344fb764ae6)<br/>
- [Hastie et al. - Artigo sobre Análise Espectral de Componentes Principais (PDF)](https://hastie.su.domains/Papers/spc_jcgs.pdf)<br/>
- [UTSA - Análise de Componentes Principais: Uma Abordagem para a Engenharia de Recursos (PDF)](https://rrpress.utsa.edu/server/api/core/bitstreams/014f44f9-d16c-4000-95c2-dcb8e983c474/content)<br/>
- [Medium - Análise de Componentes Principais: Técnica de Extração de Recursos](https://medium.com/@mayureshrpalav/principal-component-analysis-feature-extraction-technique-3f480d7b9697)<br/>
- [Medium - Análise de Componentes Principais (PCA) na Engenharia de Recursos](https://medium.com/geekculture/principal-component-analysis-pca-in-feature-engineering-472afa39c27d)<br/>
- Material da especialização da UFMG <br/>

