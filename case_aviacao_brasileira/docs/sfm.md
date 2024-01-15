## O que é SelectFromModel?
SelectFromModel é uma técnica de seleção de recursos que utiliza os pesos de importância atribuídos aos recursos por um modelo treinado. É comumente usada com modelos que atribuem importância aos recursos, como árvores de decisão e modelos lineares regularizados. Essa técnica seleciona os recursos com importâncias (ou coeficientes) maiores do que o valor de limiar especificado.<br />
## Como Funciona
A técnica realiza os seguintes passos:<br />
1.	Treinar um modelo em todo o conjunto de dados.<br />
2.	Obter os pesos ou importâncias das características a partir do modelo.<br />
3.	Estabelecer um limite (por exemplo, a média das importâncias) para selecionar as características.<br />
4.	Manter somente as características que têm uma importância acima desse limite.<br /><br />
Esse limiar pode ser um valor absoluto definido pelo usuário ou pode ser derivado de uma estratégia como a mediana ou a média das
importâncias dos recursos.<br />
## Aplicabilidade
SelectFromModel é particularmente útil quando:<br />
•	Você quer um método rápido e simples para reduzir a dimensionalidade do seu conjunto de dados.<br />
•	O modelo que você está usando para seleção de recursos fornece uma maneira confiável de determinar a importância dos recursos.<br />
•	Você deseja manter apenas os recursos mais significativos para o modelo em questão.<br />
## Prós e Contras
### Prós
•	Método direto e fácil de entender.<br />
•	Reduz a complexidade do modelo e o risco de overfitting ao descartar recursos irrelevantes.<br />
•	Flexível e pode ser usado com qualquer estimador que exponha um atributo coef_ ou feature_importances_.<br />
### Contras
•	A seleção de recursos é intrínseca ao modelo utilizado, portanto, os recursos selecionados podem não ser ideais para outros modelos.<br />
•	O limiar de importância é subjetivo e pode precisar de ajuste fino para obter o melhor conjunto de recursos.<br />
•	Se o modelo base não for bem escolhido ou ajustado, pode levar à seleção de recursos inadequada.<br />
## Interpretação e Cuidados
## Ao utilizar SelectFromModel, é importante
•	Entender que o modelo base utilizado para a seleção de recursos pode ter um grande impacto nas características selecionadas.<br />
•	Verificar se o modelo base é adequado para os dados e para a tarefa em questão.<br />
•	Realizar validação cruzada para avaliar a estabilidade da seleção de características.<br />
•	Estar ciente de que o limiar para seleção de características é arbitrário e pode precisar de ajuste fino.<br />
### Cuidados ao utilizar SelectFromModel
•	Avalie a importância das características com cautela se o modelo base tiver um desempenho ruim.<br />
•	Pode ser necessário experimentar diferentes modelos e limiares para encontrar a seleção ideal.<br />
•	A seleção de características deve ser revalidada se o conjunto de dados ou o problema sofrer alterações significativas.<br />
## Informações Adicionais
•	Modelos compatíveis: Modelos com métodos de penalização como Lasso (L1), Ridge (L2), modelos de árvores como Random Forest, Gradient Boosting, entre outros.<br />
•	Limiar de Seleção: O SelectFromModel permite ajustar o limiar para a seleção de recursos, seja através de um valor fixo, um percentual, ou utilizando estatísticas baseadas em modelos específicos.<br />

<center>
[Repositório do Case](https://github.com/pedromateusalmeida/aviacao_brasileira){ .md-button .md-button--primary }
<center>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;