
## O que é RFE?
Recursive Feature Elimination (RFE) é uma técnica de seleção de recursos utilizada para identificar quais variáveis contribuem mais para a previsão da variável de interesse. O processo do RFE envolve a construção de um modelo e a remoção das características menos importantes de forma iterativa, até que o número desejado de características seja alcançado.
## Como Funciona
O RFE realiza os seguintes passos:<br />
1.	Treina um modelo utilizando o conjunto inteiro de características.<br />
2.	Avalia a importância de cada característica.<br />
3.	Remove a característica menos importante.<br />
4.	Refaz o modelo com as características restantes.<br />
5.	Repete os passos 2 a 4 até que o número desejado de características seja atingido.<br />
## Aplicabilidade
O RFE é aplicável quando:<br />
•	Temos um grande número de variáveis e queremos reduzir a dimensionalidade.<br />
•	Precisamos de um modelo simplificado para melhor interpretabilidade.<br />
•	Queremos evitar o overfitting reduzindo a complexidade do modelo.<br />
## Prós e Contras
### Prós
•	Facilita a interpretação do modelo ao reduzir o número de variáveis.<br />
•	Pode melhorar<br />
o desempenho do modelo ao remover características ruidosas ou irrelevantes.
•	Ajuda a mitigar o overfitting e a melhoria da generalização do modelo para dados não vistos.<br />
### Contras 
•	Pode ser computacionalmente intensivo, principalmente com um grande número de características.<br />
•	A escolha de recursos é feita com base no modelo escolhido para o RFE, o que significa que a seleção é específica para esse modelo e pode não ser ideal para outros modelos.<br />
•	A remoção de recursos é um processo irreversível para o modelo específico e pode descartar características que poderiam ser úteis em combinações diferentes ou sob uma perspectiva diferente.<br />
## Interpretação e Cuidados
Ao interpretar os resultados do RFE, é essencial considerar o seguinte:
•	A importância das características está relacionada ao modelo específico utilizado para o RFE.<br />
•	Características removidas cedo no processo são geralmente menos importantes, mas isso pode variar com a mudança do modelo ou dos hiperparâmetros.<br />
•	Sempre valide a performance do modelo após a seleção de recursos para garantir que a redução não afetou negativamente a capacidade preditiva.<br />
## Cuidados ao utilizar RFE:
•	Garanta que o modelo está bem ajustado antes de usar RFE, pois um modelo mal ajustado pode levar à remoção de características importantes.<br />
•	Considere a correlação entre as características, pois o RFE não leva em conta a multicolinearidade.<br />
•	A validação cruzada deve ser usada durante o RFE para garantir que a seleção de recursos seja robusta.<br />
## Informações Adicionais
•	Modelos compatíveis: O RFE pode ser utilizado com qualquer modelo que forneça alguma forma de importância de características, como árvores de decisão, modelos lineares regularizados, entre outros.<br />
•	Variações do RFE: Existem variações como o RFECV que inclui validação cruzada no processo de seleção de recursos para encontrar o número ótimo de características.<br />

<center>
[Repositório do Case](https://github.com/pedromateusalmeida/aviacao_brasileira){ .md-button .md-button--primary }
<center>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;