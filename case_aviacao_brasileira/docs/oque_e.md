## Testes paramétricos
### O que são?
<div style="text-align: justify">
Os testes paramétricos são métodos estatísticos que assumem uma distribuição específica dos dados, geralmente a distribuição normal. Eles também pressupõem outras condições, como homogeneidade de variâncias e a relação linear entre variáveis.<br />

Como mencionado anteriormente a distribuição precisa ser conhecida, já que requerem que os dados sigam certas distribuições (frequentemente normal); homocedasticidade, uma vez que pressupõem que as variâncias dos grupos são iguais; e apresentar relações lineares, para as quais são mais eficazes em analisar.Alguns exemplos conhecidos:<br />
•	Teste t (incluindo t de Student para amostras independentes ou pareadas);<br />
•	ANOVA (Análise de Variância);<br />
•	Regressão Linear.<br />

Testes paramétricos são uteis quando os dados são aproximadamente normais e as outras suposições são atendidas. E pode ser utilizado em dados com amostras grandes, onde o Teorema do Limite Central pode justificar a aplicação de testes paramétricos, ou seja, em contextos de Big Data possuem muita aplicabilidade. <br />
</div>

!!!info "Porque Teorema do Limite Central dialogam tanto com Big Data?"
    Em big data, frequentemente lidamos com conjuntos de dados muito grandes para serem processados ou analisados integralmente. O Teorema do Limite Central permite que analistas e cientistas de dados tirem amostras representativas desses grandes conjuntos e façam inferências estatísticas confiáveis.<br />
 
## Testes não paramétricos 
### O que são?
<div style="text-align: justify">
Já os testes não paramétricos não assumem uma distribuição específica dos dados. São métodos mais flexíveis usados quando as suposições dos testes paramétricos não são atendidas.

Como mencionado os teste não paramétricos não requerem a suposição de uma distribuição normal, isso torna eles testes mais flexíveis e adequados para dados ordinais, de classificação ou altamente não normais. E outro ponto positivo é o fato dele ser menos sensíveis a outliers, ou seja, tendem a ser mais robustos em relação a dados com outliers. Alguns exemplos de testes não paramétricos:<br /><br />
•	Teste de Mann-Whitney U (comparação de duas amostras independentes);<br />
•	Teste de Wilcoxon (comparação de duas amostras pareadas);<br />
•	Teste de Kruskal-Wallis (equivalente não paramétrico da ANOVA);<br />
•	Teste de Chi-Quadrado (para independência em tabelas de contingência).<br /><br />


Esses testes são uma boa pedida para quando os dados que não atendem às suposições dos testes paramétricos, como a normalidade. Em amostras pequenas onde a validade das suposições paramétricas não pode ser estabelecida, o teste de Exato de Fisher é ótimo para isso,  ou com dados ordinais ou de classificação.<br />
</div>
## Qual tipo de teste devo escolher?
<div style="text-align: justify">
Devemos começar  a pergunta com qual é o tipo do meu dado, isso afeta diretamente qual vai ser o teste aplicado, por exmeplo:<br />
</div>

| Variável                      | Teste             |
| ----------------------------- | ----------------- |
| Nominal                       | Teste de McNemar's|
| Ordinal (Categorias ordenadas)| Wilcoxon          |
| Quantitativa (Discreta ou não normal) | Wilcoxon  |
| Quantitativa (Normal)       | Teste t-pareado   |


<div style="text-align: justify">
Abaixo temos uma tabela que auxilia qual teste devemos adotar diante o tendo em vista a variável de entrada e a variável de desfecho. 
</div>


| Variável de Entrada \ Variável Desfecho | Nominal                        | Categórico | Ordinal                      | QD                               | QNN                             | QN                              |
| --------------------------------------- | ------------------------------ | ---------- | ---------------------------- | -------------------------------- | ------------------------------- | ------------------------------- |
| Nominal                                 | Chi-2 ou Fisher's              | Chi2       | Chi2-trend ou Mann Whitney   | Mann Whitney                    | Mann Whitney ou log-rank        | Test t de Student               |
| Categórico                              | Chi2                           | Chi2       | Kruskal-Wallis               | Kruskal-Wallis                  | Kruskal-Wallis                  | ANOVA                           |
| Ordinal                                 | Chi2-trend ou Mann Whitney     | *          | Spearman Rank                | Spearman Rank                   | Spearman Rank                   | Spearman Rank ou Regressão Linear|
| Quantitativo Discreto (QD)              | Regressão Logística            | *          | *                            | Spearman Rank                   | Spearman Rank                   | Spearman Rank ou Regressão Linear|
| Quantitativo Não Normal (QNN)           | Regressão Logística            | *          | *                            | *                               | Plot dos dados e Pearson ou Spearman Rank | Regressão Linear              |
| Quantitativo Normal (QN)                | Regressão Logística            | *          | *                            | *                               | Regressão Linear                | Pearson e Regressão Linear      |


<div style="text-align: justify">
<strong>QD (Quantitativo Discreto):</strong> Variáveis quantitativas discretas são aquelas que assumem valores contáveis. Por exemplo, o número de filhos em uma família, a quantidade de carros passando por um pedágio, ou o número de clientes entrando em uma loja são todos exemplos de variáveis discretas.<br />
<strong>QNN (Quantitativo Não Normal):</strong> Refere-se a variáveis quantitativas que não seguem uma distribuição normal. A distribuição normal é uma distribuição simétrica onde a maioria das observações se agrupa em torno da média, diminuindo em frequência à medida que se afastam dela. Se os dados estão inclinados ou têm uma distribuição com múltiplos picos, eles seriam considerados não normais.<br />
<strong>QN (Quantitativo Normal):</strong> São variáveis quantitativas que seguem uma distribuição normal. Em muitos contextos estatísticos, assume-se que os dados são normalmente distribuídos, o que permite o uso de vários testes estatísticos paramétricos.<br /><br />

Por fim existem alguns testes paramétricos que possui seu equivalente no não paramétrico<br />
</div>

| Teste Paramétrico | Teste Não-Paramétrico Equivalente  |
| ----------------- | ---------------------------------- |
| Teste-t Pareado   | Teste da soma de Wilcoxon Rank     |
| Teste-t Não Pareado | Teste de Mann-Whitney            |
| Correlação de Pearson | Correlação de Spearman          |
| ANOVA             | Teste de Kruskal Wallis            |


## Conclusão<br />
<div style="text-align: justify">
A escolha entre um teste paramétrico e um não paramétrico depende da natureza dos seus dados e das suposições que você pode razoavelmente fazer sobre eles. Em geral, testes paramétricos têm maior poder estatístico e são preferíveis se suas suposições forem atendidas. No entanto, quando essas suposições são violadas, os testes não paramétricos oferecem uma alternativa valiosa e muitas vezes necessária.
</div>

!!!tips "Aplicações do testes paramétricos e não paramétricos"
    :ballot_box_with_check:  Estimar quantidades populacionais <br />
    :ballot_box_with_check:  Testar hipóteses <br />
    :ballot_box_with_check:  Comparar grupos <br />
    :ballot_box_with_check:  Estimar distribuições <br />
    :ballot_box_with_check:  Estimar curvas <br />

## Referências

- [UFBA - Aula sobre Estatística Não Paramétrica (PDF)](https://est.ufba.br/sites/est.ufba.br/files/kim/matd49-aula01.pdf)<br />
- [UFMG - Relatório Técnico sobre Estatística Não Paramétrica (PDF)](https://www.est.ufmg.br/portal/wp-content/uploads/2023/01/RTE_02_2018.pdf)<br />
- [Wikipedia - Estatística Não Paramétrica](https://pt.wikipedia.org/wiki/Estat%C3%ADstica_n%C3%A3o_param%C3%A9trica#M%C3%A9todos)<br />
- [UFPR - Resumo sobre Estatística Não Paramétrica (PDF)](https://docs.ufpr.br/~vayego/pedeefes/resumo_12.pdf)<br />
- [FGV - Teste dos Sinais, Wilcoxon e Mann-Whitney (PDF)](https://epge.fgv.br/we/Graduacao/Estatistica1/2009/2?action=AttachFile&do=get&target=teste-dos-sinais-wilcoxon-e-mann-whitney.pdf)<br />
- [Minitab Blog - Como escolher entre um teste não paramétrico e um teste paramétrico](https://blog.minitab.com/pt/como-escolher-entre-um-teste-nao-parametrico-e-um-teste-parametrico)<br />
- [Parametric and Non-parametric tests for comparing two or more groups](https://www.healthknowledge.org.uk/public-health-textbook/research-methods/1b-statistical-methods/parametric-nonparametric-tests#:~:text=Parametric%20tests%20are%20those%20that,used%20for%20non%2DNormal%20variables.)<br />


