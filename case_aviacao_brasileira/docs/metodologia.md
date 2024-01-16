## Metodologia de trabalho

<center>
[![Image title](metodologia.png)](metodologia.png?data-lightbox="image-1" data-title="My caption")
</center>

<div style="text-align: justify"><br />
Quando lido com um problema, gosto de resolvê-lo colocando-o em uma “esteira”. A esteira pode ser mais curta ou mais longa, vai depender se o problema é uma demanda ou um projeto. Dito isso, a primeira etapa consiste em receber a demanda, fazer uma grooming com a equipe de dados e depois com a equipe que realizou a demanda. Essa etapa pode ser feita em conjunto, para economizar tempo, ou separadamente, visando promover maior alinhamento entre a equipe e aumentar o campo de possibilidades de resolução para o problema, através de um brainstorm. <br /> 
<br /> 
Após atribuir contexto ao problema e entendê-lo melhor, iniciamos a fase de pesquisar sobre o assunto, buscar informações, notícias, artigos científicos e outros dados que possam contribuir para o entendimento ou resolução do problema. Em seguida, levantamos potenciais hipóteses para o problema e possíveis soluções. Abaixo uma imagem que ilustra essas primeiras etapas: <br /></div>

<center>
[![Image title](metod_1.png)](metod_1.png?data-lightbox="image-1" data-title="My caption")
<br /> Fig: Fluxograma da metodologia de trabalho utilizada no case
</center>

<div style="text-align: justify"><br />
Após a execução dessas etapas, inciamos a documentação do projeto. Criamos um card na ferramenta de Kanbam com a demanda apresentada e, dentro dele, alguns subcards com etapas necessárias para atingir o sucesso do card principal. Nesse card, é feito o registro do andamento do projeto, das decisões tomadas até a sua conclusão. Posteriormente, o que está sendo escrito poderá ser utilizado na produção da documentação final do projeto ou case. <br />
<br />
Devemos, então, criar um repositório em uma ferramenta de versionamento para armazenar o progresso desse projeto a nível de código. A etapa seguinte é localizar os dados. Nesse momento, é hora de olhar para os dados que estão disponíveis internamente no data lake da empresa e para outros dados disponibilizados na internet, neste caso, por exemplo, no próprio site da ANAC. Importante refletir se os dados de acesso facilitado na internet são confiáveis e se o seu consumo, extração e utilização esatrão em conformidade com as regras da LGPD.<br />
<br />
Localizados os dados, chega o momento de extrai-los e tratá-los. A etapa de tratamento é crucial para garantir qualidade nos dados que serão utilizados na análise e/ou no treinamento do modelo. Nessa etapa também identificamos as informações que demandarão tratamento contínuo e que precisarão ser disponibilizadas na feature store. Abaixo, uma imagem que ilustra essas etapas.<br /></div>
<center>
[![Image title](metod_2.png)](metod_2.png?data-lightbox="image-1" data-title="My caption")
<br /> Fig: Fluxograma da metodologia de trabalho utilizada no case
</center>
<div style="text-align: justify"><br />
Iniciamos, então, a análise exploratória, em que realizamos diversas análises descritivas e de inferências. Nessa etapa, já buscamos responder algumas hipóteses. Há situações em que o resultado da análise exploratória é de que não seria necessário um modelo e que um dashboard resolveria o nosso problema. <br />
<br />
Se o problema demandar uma resolução que utilize um modelo de aprendizado de máquina, devemos proceder uma seleção de variáveis/feature selection. Nesse momento, aplicamos diversas técnicas que nos auxilia na escolha das melhores variáveis para o modelo. É o momento de aplicar técnicas de redução de dimensionalidade para sintetizar uma dimensão. Abaixo, uma imagem que representa esse fluxo<br /></div>

<center>
[![Image title](metod_3.png)](metod_3.png?data-lightbox="image-1" data-title="My caption")
<br /> Fig: Fluxograma da metodologia de trabalho utilizada no case
</center>
<div style="text-align: justify"><br />
Passado isso, chega o momento de treinar o modelo e analisar sua performance. Dentro da etapa de treinamento do modelo, temos algumas subetapas importantes para o processo, como one hot enconding, balanceamento de variável preditiva (SMOTE), normalização dos dados, hypertunning, cross-validation e pitras. E na etapa de análise, olhamos a performance do modelo, analisamos se faz sentido, quais os pesos das variáveis para predizer a variável y do modelo, se o modelo não está cometendo nenhuma infração (por exemplo, se não está gerando nenhum viés discriminatório) e outras análises. <br />
<br />
Após o desenvolvimento do modelo, análise de performance e apresentação para o time ou stakeholder interessado no projeto, algumas perguntas precisam ser respondidas, por exemplo: <br />
i. o resultado apresentado atingiu o objetivo? <br />
ii. é necessário automatizar o modelo? <br />
iii. o objetivo final do modelo é automatizar um processo ou auxiliar no processo de uma tomada de decisão mais inteligente? <br />
Essas perguntas ajudarão a compreender a necessidade e a urgência de se colocar um modelo em produção.  <br />
<br />
Indo ou não o modelo para produção, será necessário criar uma documentação para ele. Se for para produção, seria importante já elaborar algumas métricas que ajudem a medir o sucesso do modelo e sua performance, documentar o ambiente necessário para o modelo funcionar. Essas informações são necessárias para o engenheiro de MLops colocar o modelo em produção. Abaixo uma imagem que ilustra essas etapas: <br /></div>
<center>
[![Image title](metod_4.png)](metod_4.png?data-lightbox="image-1" data-title="My caption")
<br /> Fig: Fluxograma da metodologia de trabalho utilizada no case
</center>
<br />

## Referências

- [Introducing MLOps How to Scale Machine Learning in the Enterprise - Editora O'Reilly](https://www.oreilly.com/library/view/introducing-mlops/9781492083290/)
- [Pratical MLops - Editora O'Reilly](https://www.oreilly.com/library/view/practical-mlops/9781098103002/)
- [A Construção do Saber (Manual de metodologia de pesquisa em ciência humanas)[ Christian Laville e Jean Diome]]()
- 