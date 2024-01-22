

## O que é SelectFromModel (SFM)?
SelectFromModel é uma técnica de seleção de recursos que utiliza os pesos de importância atribuídos aos recursos por um modelo treinado. É comumente usada com modelos que atribuem importância aos recursos, como árvores de decisão e modelos lineares regularizados. Essa técnica seleciona os recursos com importâncias (ou coeficientes) maiores do que o valor de limiar especificado.<br />


Apesar DE ambas as técnicas, RFE e SFM, buscarem o mesmo objetivo, o RFE remove recursos menos significativos em iterações. Basicamente, ele primeiro remove alguns recursos que não são importantes e depois ajusta, remove e, novamente, ajusta. Ele repete esta iteração até atingir um número adequado de recursos. Já o SelectFromModel é um pouco menos potente, pois apenas remove recursos menos importantes com base em um limite fornecido como parâmetro.

SelectFromModel é útil quando queremos um método rápido e simples para reduzir a dimensionalidade do seu conjunto de dados.<br />

## Como Funciona
A técnica realiza os seguintes passos:<br />
1.	Treinar um modelo em todo o conjunto de dados.<br />
2.	Obter os pesos ou importâncias das características a partir do modelo.<br />
3.	Estabelecer um limite (por exemplo, a média das importâncias) para selecionar as características.<br />
4.	Manter somente as características que têm uma importância acima desse limite.<br /><br />
Esse limiar pode ser um valor absoluto definido pelo usuário ou pode ser derivado de uma estratégia, como a mediana ou a média das
importâncias dos recursos.<br />




!!!warning "Cuidados ao utilizar SelectFromModel"
    •	Avalie a importância das características com cautela se o modelo base tiver um desempenho ruim.<br />
    •	Pode ser necessário experimentar diferentes modelos e limiares para encontrar a seleção ideal.<br />
    •	A seleção de características deve ser revalidada se o conjunto de dados ou o problema sofrer alterações significativas.<br />
    •	O SelectFromModel permite ajustar o limiar para a seleção de recursos, seja através de um valor fixo, um percentual, ou utilizando estatísticas baseadas em modelos específicos.<br />
    •	Estar ciente de que o limiar para seleção de características é arbitrário e pode precisar de ajuste fino.<br />


[Aplicação do SelectFromModel no Case](https://github.com/pedromateusalmeida/aviacao_brasileira/blob/main/scripts_v2/4_3_feature_selection.ipynb){ .md-button .md-button--primary }

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;


## Referências

- [Medium - Feature Elimination Examples for Logistic Regression](https://darigak.medium.com/feature-elimination-examples-for-logistic-regression-7293462e197b)

- [Medium - Como selecionar as melhores features para seu modelo de Machine Learning](https://medium.com/data-hackers/como-selecionar-as-melhores-features-para-seu-modelo-de-machine-learning-faf74e357913)

- [Scikit-Learn - Documentação do SelectFromModel](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectFromModel.html)

- [Scikit-Learn - Exemplo de SelectFromModel com o conjunto de dados de Boston](https://scikit-learn.org/0.19/auto_examples/feature_selection/plot_select_from_model_boston.html)



