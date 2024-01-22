## O que é RFE?
<div style="text-align: justify">
Recursive Feature Elimination (RFE) é uma técnica de seleção de recursos utilizada para identificar quais variáveis contribuem mais para a previsão da variável de interesse. O processo do RFE envolve a construção de um modelo e a remoção das características menos importantes de forma iterativa, até que o número desejado de características seja alcançado.
</div>
## Como Funciona
<div style="text-align: justify">
O RFE realiza os seguintes passos:<br />
1.	Treina um modelo utilizando o conjunto inteiro de características.<br />
2.	Avalia a importância de cada característica.<br />
3.	Remove a característica menos importante.<br />
4.	Refaz o modelo com as características restantes.<br />
5.	Repete os passos 2 a 4 até que o número desejado de características seja atingido.<br /><br />

Algum destaque merece ser feito sobre o RFE, ele é um algoritmo que pode ser computacionalmente intensivo, principalmente com um grande número de características. A escolha de recursos é feita com base no modelo escolhido para o RFE, o que significa que a seleção é específica para esse modelo e pode não ser ideal para outros modelos.	A remoção de recursos é um processo irreversível para o modelo específico e pode descartar características que poderiam ser úteis em combinações diferentes ou sob uma perspectiva diferente.<br />

Diversos modelos de machine learning são compativeis com o uso do RFE, ele pode ser utilizado com qualquer modelo que forneça alguma forma de importância de características, como árvores de decisão, modelos lineares regularizados, entre outros.<br />
</div>

## Interpretação

<div style="text-align: justify">
Ao interpretar os resultados do RFE, é essencial considerar que a importância das características está relacionada ao modelo específico utilizado para o RFE. Outro destaque é que as características removidas cedo no processo são geralmente menos importantes, mas isso pode variar com a mudança do modelo ou dos hiperparâmetros. 
</div>
!!!tip "Sempre valide a performance do modelo após a seleção de recursos para garantir que a redução não afetou negativamente a capacidade preditiva."
!!!warning "Cuidados ao utilizar RFE"
    •	Garanta que o modelo está bem ajustado antes de usar RFE, pois um modelo mal ajustado pode levar à remoção de características importantes.<br />
    •	Considere a correlação entre as características, pois o RFE não leva em conta a multicolinearidade.<br />
    •	A validação cruzada deve ser usada durante o RFE para garantir que a seleção de recursos seja boa.<br />






[Aplicação do RFE no Case](https://github.com/pedromateusalmeida/aviacao_brasileira/blob/main/scripts_v2/4_3_feature_selection.ipynb){ .md-button .md-button--primary }

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;


## Referências

- [Scikit-Learn - Documentação do RFE](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.RFE.html)

- [Medium - Seleção de Features com Recursive Feature Elimination (RFE)](https://k3ybladewielder.medium.com/sele%C3%A7%C3%A3o-de-features-com-recursive-feature-elimination-rfe-5effad69590b)

- [Machine Learning Mastery - RFE Feature Selection in Python](https://machinelearningmastery.com/rfe-feature-selection-in-python/)

- [Medium - Recursive Feature Elimination: Uma Técnica Poderosa para Seleção de Recursos em Machine Learning](https://medium.com/@evertongomede/recursive-feature-elimination-a-powerful-technique-for-feature-selection-in-machine-learning-89b3c2f3c26a)

- [Caret - Recursive Feature Elimination](https://topepo.github.io/caret/recursive-feature-elimination.html)

- [Springer - Artigo sobre RFE (Link Springer)](https://link.springer.com/article/10.1023/A:1012487302797)

- [ScienceDirect - Artigo sobre RFE (ScienceDirect)](https://www.sciencedirect.com/science/article/pii/S000437029700043X)

- [Simplilearn - Artigo sobre Recursive Feature Elimination](https://www.simplilearn.com/recursive-feature-elimination-article)

