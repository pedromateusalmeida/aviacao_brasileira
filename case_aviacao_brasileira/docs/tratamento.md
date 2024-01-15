## Documentação do Processo de Tratamento de Dados de Voos
<div style="text-align: justify"><br />
1. Introdução<br />
Nesta documentação, detalhamos as operações realizadas no script para carregar, transformar, padronizar e analisar dados de voos de companhias aéreas.<br />
2. Detecção de Codificação de Arquivos<br />
•	A função detect_encoding identifica a codificação dos arquivos de texto, garantindo uma leitura correta dos dados.<br />
3. Determinação de Atraso de Voos<br />
•	A função is_delayed é usada para determinar se um voo está atrasado. Um voo é considerado atrasado se a diferença entre a partida real e a prevista for maior que 15 minutos.<br />
4. Padronização de Nomes de Colunas<br />
•	A função padronizar_nome_coluna limpa e padroniza os nomes das colunas, similar ao primeiro script.<br />
5. Cálculo de Diferença de Tempo<br />
•	As funções calculate_time_delta e calculate_time_int são usadas para calcular a diferença de tempo entre dois eventos, como a partida prevista e a real.<br />
6. Encontrar Coluna Similar<br />
•	A função encontrar_coluna_similar compara nomes de colunas com um conjunto padrão e identifica a coluna mais similar usando a distância de Levenshtein.<br />
7. Detecção de Delimitador de Arquivo<br />
•	A função detectar_delimitador identifica o delimitador mais adequado para arquivos CSV.<br />
8. Carregamento e Mesclagem de Dados<br />
•	O script carrega dados de diferentes fontes (aeroportos, companhias aéreas, histórico de voos) e os mescla para criar um conjunto de dados unificado.<br />
•	Durante a mesclagem, renomeia colunas para evitar conflitos e garante que apenas registros relevantes sejam incluídos.<br />
9. Conversão de Datas e Horas<br />
•	O script converte colunas de datas e horas para o formato datetime, facilitando a manipulação e análise temporal.<br />
10. Limpeza e Padronização de Nomes<br />
•	Funções de limpeza são aplicadas para padronizar e limpar nomes de cidades, aeroportos e descrições.<br />
11. Criação de Variáveis Adicionais<br />
•	Novas variáveis são criadas, como 'rota', para análises mais detalhadas, como identificação de rotas com mais problemas de atraso e cancelamento.<br />
12. Salvamento dos Dados<br />
•	O DataFrame final é salvo em um arquivo CSV para uso posterior.<br />
</div>

[Script com o tratamento dos dados de voos](){ .md-button .md-button--primary }


## Documentação do Processo de Tratamento de Dados Meteorológicos
<div style="text-align: justify"><br />
1. Introdução<br />
Nesta seção, descrevemos as operações realizadas para carregar, transformar e padronizar dados meteorológicos a partir de arquivos CSV.<br />
2. Carregamento e Transformação de Dados<br />
O processo começa com a função process_file, que executa as seguintes tarefas:<br />
•	Carregamento de Dados: O DataFrame é criado pulando as primeiras 8 linhas do arquivo CSV, que contêm informações da estação.<br />
•	Extração de Informações da Estação: As primeiras 8 linhas são carregadas separadamente para extrair informações como latitude, longitude e altitude.<br />
•	Conversão de Coordenadas: As coordenadas são convertidas para o formato float, substituindo vírgulas por pontos para padronização.<br />
3. Detecção de Codificação de Arquivos<br />
A função detect_encoding é usada para identificar a codificação de arquivos de texto, garantindo a leitura correta dos dados.<br />
4. Padronização de Nomes de Colunas<br />
A função padronizar_nome_coluna realiza a limpeza e padronização dos nomes das colunas, removendo acentos, transformando em minúsculas e substituindo caracteres especiais.<br />
5. Conversão de Coordenadas DMS para Decimal<br />
A função dms_to_decimal é aplicada para converter coordenadas do formato DMS (graus, minutos, segundos) para graus decimais.<br />
6. Limpeza e Padronização de Nomes de Aeródromos<br />
A função clean_name_aero é utilizada para limpar e padronizar nomes de aeródromos, removendo conteúdos entre parênteses, acentos e convertendo para maiúsculas.<br />
7. Processamento e Concatenação dos Dados<br />
Os arquivos CSV são processados individualmente e concatenados em um único DataFrame. Nomes de colunas são renomeados e ajustados para uniformidade.<br />
8. Conversão de Tipos de Dados<br />
Algumas colunas são convertidas para tipos específicos (como float64) para garantir consistência nos dados.<br />
9. Agrupamento e Resumo dos Dados<br />
Os dados são agrupados por certas colunas-chave (data, hora, estação etc.) e resumidos para análise posterior.<br />
10. Salvamento dos Dados<br />
Os DataFrames tratados são salvos em formatos específicos (como Parquet e CSV) para uso posterior.<br />
</div>

[Script com o tratamento dos dados de meteorológicos](){ .md-button .md-button--primary }


## Documentação do Processo de Tratamento e Análise de Dados de Voos com PySpark
<div style="text-align: justify"><br />
1. Configuração do Ambiente Spark<br />
Inicialmente, o script configura o ambiente Spark, definindo parâmetros como número de núcleos, memória do driver, paralelismo padrão, e outras configurações relevantes para otimizar o desempenho do Spark.<br />
2. Leitura dos Dados Meteorológicos<br />
Os dados meteorológicos previamente tratados são lidos do formato Parquet, com uma repartição inicial de 12 partições. Alterações são feitas em colunas específicas, como a conversão do tipo de 'hora_utc' e a renomeação da coluna 'estacao' para 'cidade'.<br />
3. Preparação dos DataFrames de Origem e Destino<br />
O script prepara dois DataFrames separados para aeroportos de origem e destino, renomeando colunas de forma adequada para diferenciar os dados de origem e destino.<br />
4. Leitura dos Dados de Voos<br />
Dados de voos históricos são lidos de um arquivo CSV, com repartição inicial de 6 partições. As colunas de datas de partida e chegada são convertidas para o tipo de dados 'datetime'.<br />
5. Transformações e Renomeações de Colunas<br />
Transformações adicionais são aplicadas, incluindo a renomeação de colunas para padronizar nomes e a conversão de colunas de data para strings.<br />
6. Mesclagem dos Dados<br />
Realiza a mesclagem (join) dos dados de voos com os dados meteorológicos de destino e origem, utilizando colunas chave como critérios de junção.<br />
7. Eliminação de Duplicatas e Reparticionamento<br />
O DataFrame resultante é limpo para remover duplicatas e é reparticionado para uma única partição.<br />
8. Salvamento dos Dados Finais<br />
Finalmente, os dados combinados e tratados são salvos em um arquivo CSV para análises futuras.<br />
</div>

[Script de unificação dos dados meteorológicos + voos](){ .md-button .md-button--primary }
