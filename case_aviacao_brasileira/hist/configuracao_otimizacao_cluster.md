## Configuração e Otimização do Cluster

<div style="text-align: justify">
A importância de configurar corretamente um cluster Spark é inegável. Uma configuração adequada é crucial, já que ela impacta diretamente a performance, eficiência e escalabilidade quando se trata de processamento distribuído de dados. Abordaremos os problemas que podem surgir de uma configuração inadequada e também os benefícios de um ajuste correto.
<br />
</div>
<br />
!!! warning "Consequências de uma Má Configuração:"
    - **Queda de Performance:** Performance comprometida pode significar perda de produtividade.
    - **Subutilização de Recursos:** Recursos valiosos, como memória e CPU, podem ser desperdiçados.
    - **Falhas Frequentes:** Configurações inadequadas podem causar instabilidades e falhas constantes.
    - **Aumento dos Custos:** Em ambientes de nuvem, os custos podem escalar rapidamente com má configuração.
    - **Dificuldades no Debug:** Diagnóstico de problemas torna-se mais complicado, levando mais tempo para resolução.
    - **Limitações de Escalabilidade:** Escalar para lidar com mais dados pode se tornar um desafio.



!!! tip "Benefícios de uma Configuração Adequada:"
    - **Performance Otimizada:** Processamento mais ágil e eficiente de grandes volumes de dados.
    - **Utilização Eficiente de Recursos:** Maximização dos recursos disponíveis e evitando desperdícios.
    - **Escalabilidade:** Expansão facilitada do cluster para atender a demandas crescentes.
    - **Confiabilidade:** Maior estabilidade e recuperação ágil após falhas.
    - **Gerenciamento Equilibrado:** Distribuição uniforme da carga de trabalho entre os nós do cluster.
    - **Menor Latência:** Respostas mais ágeis em operações interativas, como consultas SQL.


<div style="text-align: justify">
<strong>Considerações ao Configurar um Cluster:</strong><br />
</div>

- Volume de dados<br />
- Quantidade de memória disponível<br />
- Número de cores de processamento<br />
- Memória alocada para o driver<br />
- Memória alocada para o executor<br />
- Cores alocadas para o executor<br />
- Cores alocadas para o driver<br />
- Decisão sobre armazenamento em disco ou na RAM<br />
- Definição da quantidade e tamanho ideal de partições do RDD<br />
- Configuração de memória para serialização<br />
- Ativação do Adaptive Query Execution (AQE) e do CBO quando necessário<br />
- Ajuste do Compression Block Size<br />


## O que utilizar na configuração do meu sparkSession?

<div style="text-align: justify">
O Spark oferece uma ampla variedade de configurações para otimizar e personalizar a sua sessão conforme as necessidades. Embora existam muitas opções, focaremos em algumas configurações fundamentais e relevantes:
</div>

| Configuração                        | Descrição                                                                                                                                                   |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **.master("local[*]")**             | Determina o modo de execução para local. O [*] indica que o Spark deve usar todos os núcleos disponíveis no sistema.                                        |
| **spark.driver.cores**              | Configura o número de núcleos usados pelo driver do Spark.                                                                                                  |
| **spark.driver.memory**             | Estabelece a quantidade de memória a ser alocada pelo driver do Spark.                                                                                      |
| **spark.default.parallelism**       | Define o paralelismo padrão, o número padrão de partições em operações RDD sem shuffling (como map).                                                        |
| **spark.executor.cores**            | Especifica o número de núcleos a serem utilizados por cada executor.                                                                                        |
| **spark.executor.instances**        | Configura o número de instâncias do executor.                                                                                                               |
| **spark.executor.memory**           | Define a quantidade de memória para cada executor.                                                                                                          |
| **spark.memory.fraction**           | Estabelece a fração da memória total do heap para armazenamento e computação.                                                                               |
| **spark.memory.storageFraction**    | Indica a fração da memória do Spark (baseado na configuração spark.memory.fraction) destinada ao cache de RDD.                                              |
| **spark.memory.offHeap.enabled**    | Ativa o uso de memória off-heap.                                                                                                                            |
| **spark.memory.offHeap.size**       | Define a capacidade da memória off-heap.                                                                                                                    |
| **spark.sql.repl.eagerEval.enabled**| Habilita a avaliação ansiosa de DataFrames no REPL do Spark, útil para visualizações durante o desenvolvimento.                                              |
| **spark.sql.repl.eagerEval.maxNumRows** | Configura o número máximo de linhas exibidas quando a avaliação ansiosa está ativa.                                                                      |
| **.appName()**                      | Determina o nome da aplicação Spark.                                                                                                                        |

<div style="text-align: justify">
<strong>Configurações para GPUs (Nota: é essencial instalar e configurar os drivers da GPU. Informe-se mais antes de usar):</strong>
</div>

| Configuração                               | Descrição                                                                                                               |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| **spark.plugins**                          | Lista os plugins a serem carregados. O **com.nvidia.spark.SQLPlugin** é o plugin SQL da NVIDIA para Spark, possibilitando que o Spark execute operações SQL em GPUs NVIDIA, acelerando consideravelmente operações como joins e agregações. |
| **spark.executor.resource.gpu.amount**     | Define a quantidade de GPUs para cada executor.                                                                         |
| **spark.rapids.memory.pinnedPool.size**    | Estabelece o tamanho do pool de memória "pinned", utilizada para transferências eficientes entre CPU e GPU.              |

