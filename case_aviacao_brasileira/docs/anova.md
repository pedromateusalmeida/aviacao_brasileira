## O que é ANOVA?
<div style="text-align: justify">
ANOVA (Análise de Variância) é uma técnica estatística usada para comparar as médias de duas ou mais amostras independentes, determinando se existe uma diferença significativa entre elas. Em termos de seleção de recursos, ANOVA pode ser usada para avaliar se a média de uma variável numérica é significativamente diferente entre diferentes categorias de uma variável categórica.<br />
</div>
## Como Funciona
<div style="text-align: justify">
•	ANOVA testa a hipótese nula de que todas as médias de grupo são iguais contra a hipótese alternativa de que pelo menos uma média de grupo é diferente.<br />
•	Calcula-se a variância dentro dos grupos (variabilidade devido ao erro) e a variância entre os grupos (variabilidade devido ao efeito real).<br />
•	A razão dessas variâncias (F-ratio) é usada para determinar se as diferenças entre as médias são significativas.<br />
</div>
## Aplicabilidade
<div style="text-align: justify">
•	Quando Usar: O ANOVA é usado quando você quer comparar as médias de três ou mais grupos independentes. Por exemplo, comparar os efeitos de diferentes tratamentos ou condições em uma variável contínua.<br />
•	Quando Não Usar: Não use ANOVA se suas variáveis são dependentes, se tem menos de três grupos para comparar, ou se suas variáveis não são quantitativas. Além disso, não use ANOVA se as suposições do teste não forem atendidas.<br />
</div>
## Prós e Contras
### Prós
<div style="text-align: justify">
•	Permite a comparação de mais de dois grupos simultaneamente.<br />
•	Robusto contra pequenos desvios da normalidade na distribuição dos dados.<br />
•	Fornece um método sistemático para avaliar a influência de variáveis categóricas sobre uma variável contínua.<br />
</div>
### Contras
<div style="text-align: justify">
•	Pressupõe que os dados de cada grupo são normalmente distribuídos e têm variações iguais (homocedasticidade).<br />
•	Não identifica quais grupos são significativamente diferentes entre si; testes adicionais são necessários para essas comparações.<br />
•	Sensível a outliers, que podem distorcer os resultados do teste.<br />
</div>
## Interpretação e Cuidados
<div style="text-align: justify">
•	Um valor F alto e um valor p baixo indicam que há diferença significativa entre as médias dos grupos.<br />
•	A significância estatística não implica necessariamente em relevância prática; é importante considerar a magnitude das diferenças.<br />
•	Deve-se verificar os pressupostos da ANOVA antes de aplicar o teste.<br />
</div>
## O que Observar no ANOVA
<div style="text-align: justify">
•	F-Statistic (Estatística F): Esta é a razão entre a variância explicada pelo modelo (entre os grupos) e a variância não explicada (dentro dos grupos). Um valor alto de F indica que há uma diferença significativa entre as médias dos grupos.<br />
•	P-valor (PR(>F)): Indica a probabilidade de observar um valor de F tão extremo quanto o observado, assumindo que a hipótese nula é verdadeira (ou seja, que todas as médias dos grupos são iguais). Um p-valor baixo (geralmente menor que 0,05) sugere que você deve rejeitar a hipótese nula.<br />
•	Sum_sq (Soma dos Quadrados): Reflete a variância total, dividida em variância devido ao modelo (variância entre os grupos) e variância residual (variância dentro dos grupos).<br />
•	df (Graus de Liberdade): Refere-se ao número de categorias nos dados menos um para a variância do modelo e ao número total de observações menos o número de categorias para a variância residual.<br />
</div>
## O que Prestar Atenção
<div style="text-align: justify">
•	P-valor: É o indicador mais importante para a significância estatística. Um p-valor menor que 0,05 geralmente indica que há diferenças significativas entre as médias dos grupos.<br />
•	Tamanho do Efeito: O valor de F por si só não diz tudo. Um grande valor de F pode ser significativo, mas é importante considerar também o tamanho do efeito, que pode ser verificado por medidas como a "Eta squared" (η²).<br />
•	Suposições do ANOVA: O teste ANOVA assume que os dados são normalmente distribuídos dentro de cada grupo e que os grupos têm variâncias iguais (homocedasticidade). Essas suposições devem ser testadas antes de aplicar o ANOVA.<br />
Cuidados<br />
•	Normalidade: Verifique a normalidade dos dados. Se os dados não forem normalmente distribuídos, outras abordagens, como transformações ou testes não paramétricos (por exemplo, Kruskal-Wallis), podem ser necessárias.<br />
•	Homogeneidade das Variâncias: Use testes como Levene ou Bartlett para verificar a homogeneidade das variâncias. Se as variâncias não forem homogêneas, considere usar ANOVA Welch.<br />
•	Independência das Observações: O ANOVA assume que as observações são independentes. Garanta que esta suposição seja válida para seus dados.<br />
</div>
<div style="text-align: justify">
</div>
<center>
[Repositório do Case](https://github.com/pedromateusalmeida/aviacao_brasileira){ .md-button .md-button--primary }
<center>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;