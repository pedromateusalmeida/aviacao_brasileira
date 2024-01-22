
## O que é SHAP?
<div style="text-align: justify">

SHAP é uma abordagem de interpretação de modelo baseada na teoria dos jogos, que atribui a cada característica um valor que representa sua importância na previsão de cada instância. Os valores SHAP são baseados nos valores de Shapley, um conceito da teoria dos jogos cooperativos que distribui a "recompensa" (ou seja, a previsão do modelo) entre os colaboradores (recursos) de forma justa. O Shap me foi apresentado como uma das sete maravilhas do machine learning e, passados os anos, tenho que concordar, pois ainda é uma ferramenta muito viva na área de ciência de dados. Pessoalmente falando, sou encantado com a robustez do algoritmo. <br />
</div>

## Como Funciona

<div style="text-align: justify">
A interpretação do modelo com SHAP envolve os seguintes passos:<br />
1. Para uma dada instância, o modelo faz uma previsão usando todas as características.<br />
2. Subconjuntos de características são sistematicamente "desligados" (simulando a ausência de informações), e a previsão é feita sem
eles. <br />
3. O impacto de cada característica na mudança da previsão em relação à previsão base (a previsão média para o conjunto de dados) é calculado. Este impacto é o valor SHAP para a característica naquela instância.<br />
4.	Todos os valores possíveis de subconjuntos de características são considerados para calcular o valor SHAP final para cada característica, o que garante uma distribuição justa e consistente de importância entre as características.<br /><br />

O valores SHAP positivos indicam que a característica aumentou a previsão, enquanto valores negativos indicam uma diminuição. A magnitude do valor SHAP reflete a força da contribuição da característica, independente do sinal.<br />
</div>

!!!warning "Calcular o shap demanda recurso computacional"

<div style="text-align: justify">
O Shap é uma ótima ferramenta para interpretar métricas locais e globais do modelo. Baseia-se em uma base teórica sólida (valores de Shapley), garantindo justiça e consistência. E ainda é versátil, pois é aplicável a qualquer modelo de Machine Learning, sendo considerado modelo-agnóstico. Os valores SHAP podem ser facilmente visualizados e interpretados através de gráficos de força, gráficos de resumo, entre outros.<br /><br />

Porém, como mencionado anteriormente, é um cálculo computacionalmente intensivo, especialmente para modelos com um grande número de características e dados e pode ser desafiador para modelos com interações complexas entre as características.<br />
</div>


!!!tips "Dicas"
    •	As bibliotecas de SHAP incluem muitas visualizações úteis que podem ajudar na interpretação, como bee swarm plots, bar plots, e waterfall plots.<br />
    •	Os valores SHAP são consistentes em sua atribuição; se uma característica contribui mais para a previsão do que outra, seu valor SHAP será maior.<br />
<br />


[Aplicação do Shap no Case (feature selection)](https://github.com/pedromateusalmeida/aviacao_brasileira/blob/main/scripts_v2/3_2_analise_exploratoria.ipynb){ .md-button .md-button--primary }
<br />

[Aplicação do Shap no case (análise do modelo)](https://github.com/pedromateusalmeida/aviacao_brasileira/blob/main/scripts_v2/3_2_analise_exploratoria.ipynb){ .md-button .md-button--primary }

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

## Referências

- [Interpretable Machine Learning: A Guide for Making Black Box Models Explainable - SHAPLEY Values](https://christophm.github.io/interpretable-ml-book/shapley.html)
- [SHAP Documentation: API Examples](https://shap.readthedocs.io/en/latest/api_examples.html)
- [SHAP Documentation: Tabular Examples](https://shap.readthedocs.io/en/latest/tabular_examples.html)
