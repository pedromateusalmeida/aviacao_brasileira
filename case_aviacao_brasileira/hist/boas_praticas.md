Boas Práticas de Uso do Spark
<div style="text-align: justify">
A otimização do uso do Spark é fundamental para garantir o desempenho, a eficiência e a confiabilidade do processamento. A seguir, são apresentadas algumas práticas recomendadas:
</div>
Uso de UDFs (User Defined Functions): Evite o uso excessivo de UDFs. Eles podem ser menos otimizados do que as funções nativas do Spark, reduzindo o desempenho.<br />
Compreensão do Lazy Evaluation: O Spark utiliza o conceito de "Lazy Evaluation". Esteja ciente dessa característica para evitar surpresas durante a execução.<br />
Uso de Cache: Utilize .cache() para armazenar objetos, como DataFrames, na memória. Use o cache sabiamente e evite cache excessivo.<br />
Configurações para Otimização de Memória: Ative spark.sql.inMemoryColumnarStorage.compressed para armazenamento colunar comprimido em memória.<br />
Otimizações de Join: Utilize "Broadcast Join" quando uma das tabelas em sua operação join for pequena o suficiente para caber na memória.<br />
Ativação de Otimizadores: Ative o Otimizador Baseado em Custo (CBO) e o Adaptive Query Execution (AQE) para otimizar o processamento.<br />
Gerenciamento de Partições: Encontre um equilíbrio entre o número de partições e a quantidade de dados em cada partição.<br />
Evite Operações Custosas: Reduza operações que necessitam de embaralhamento e ordene dados apenas quando estritamente necessário.<br />