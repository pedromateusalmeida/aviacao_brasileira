## Teste Exato de Fisher
!!!warning
    O conteúdo foi produzido com o Chatgpt. Eu passei alguns materiais e passei alguns direcionamentos. Ainda é necessário inserir bibliografia e aprofundar nos tópicos. 
## O que é o Teste Exato de Fisher?
O Teste Exato de Fisher é uma técnica estatística usada para determinar se há associações significativas entre duas variáveis categóricas em tabelas de contingência, especialmente útil para amostras de tamanho pequeno. Diferente do teste de Chi-Quadrado, o Teste de Fisher não depende de uma distribuição de amostragem aproximada e é exato.<br />
## Como Funciona
•	O teste calcula a probabilidade exata de observar uma tabela de contingência como a dada, assumindo que não há associação entre as variáveis (hipótese de independência).<br />
•	Usa a distribuição hipergeométrica para calcular a probabilidade de cada possível distribuição de frequências sob a hipótese de independência e soma essas probabilidades para obter o valor p.<br />
## Aplicabilidade
•	Ideal para tabelas de contingência 2x2, mas pode ser estendido para tabelas maiores.<br />
•	Útil quando as frequências esperadas são muito baixas para o teste de Chi-Quadrado ser válido.<br />
## Prós e Contras
### Prós
•	Não requer que as frequências esperadas sejam altas, tornando-o adequado para amostras pequenas.<br />
•	Mais preciso que o teste de Chi-Quadrado para amostras pequenas.<br />
•	Pode ser aplicado independentemente da forma da distribuição dos dados.<br />
### Contras
•	Computacionalmente intensivo para tabelas de contingência maiores.<br />
•	Menos poderoso que o teste de Chi-Quadrado para amostras maiores.<br />
•	Não tão amplamente conhecido ou utilizado quanto o teste de Chi-Quadrado.<br />
## Interpretação e Cuidados
•	Um valor p baixo sugere que existe uma associação significativa entre as variáveis.<br />
•	Como qualquer teste estatístico, um valor p significativo não implica causalidade.<br />
•	Importante verificar a adequação do tamanho da amostra e a independência das observações.<br />
## Cuidados ao utilizar o Teste de Fisher:
•	Não deve ser usado para amostras grandes devido ao seu custo computacional.<br />
•	Cuidado ao interpretar tabelas de contingência com muitas células vazias ou com frequências muito baixas.<br />
•	Considerar o contexto e as hipóteses subjacentes antes de tirar conclusões baseadas apenas no valor p.<br />
## Informações Adicionais
•	Comparação com o Chi-Quadrado: O Teste de Fisher é frequentemente usado quando o teste de Chi-Quadrado não é apropriado devido ao tamanho da amostra ou a frequências esperadas baixas.<br />
•	Visualizações: Gráficos de barras ou de mosaico podem ser usados para visualizar as relações entre variáveis categóricas antes de aplicar o Teste de Fisher.<br />


<center>
[Repositório do Case](https://github.com/pedromateusalmeida/aviacao_brasileira){ .md-button .md-button--primary }
<center>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;