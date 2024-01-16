## Documentação do processo de tratamento de dados de voos
<div style="text-align: justify"><br />
1. Introdução<br />
Nesta documentação, detalhamos as operações realizadas no script para carregar, transformar, padronizar e analisar dados de voos de companhias aéreas.<br /><br />

2. Detecção de codificação de arquivos<br />
A função detect_encoding identifica a codificação dos arquivos de texto, garantindo uma leitura correta dos dados.<br /><br />

3. Determinação de atraso de voos<br />
A função is_delayed é usada para determinar se um voo está atrasado. Um voo é considerado atrasado se a diferença entre a partida real e a prevista for maior que 15 minutos.<br /><br />

4. Padronização de nomes de colunas<br />
A função padronizar_nome_coluna limpa e padroniza os nomes das colunas, similar ao primeiro script.<br /><br />

5. Cálculo de diferença de tempo<br />
As funções calculate_time_delta e calculate_time_int são usadas para calcular a diferença de tempo entre dois eventos, como a partida prevista e a real.<br /><br />

6. Encontrar coluna similar<br />
A função encontrar_coluna_similar compara nomes de colunas com um conjunto padrão e identifica a coluna mais similar usando a distância de Levenshtein.<br /><br />

7. Detecção de delimitador de arquivo<br />
A função detectar_delimitador identifica o delimitador mais adequado para arquivos CSV.<br /><br />

8. Carregamento e mesclagem de dados<br />
O script carrega dados de diferentes fontes (aeroportos, companhias aéreas, histórico de voos) e os mescla para criar um conjunto de dados unificado.<br />
Durante a mesclagem, renomeia colunas para evitar conflitos e garante que apenas registros relevantes sejam incluídos.<br /><br />

9. Conversão de datas e horas<br />
O script converte colunas de datas e horas para o formato datetime, facilitando a manipulação e análise temporal.<br /><br />

10. Limpeza e padronização de nomes<br />
Funções de limpeza são aplicadas para padronizar e limpar nomes de cidades, aeroportos e descrições.<br /><br />

11. Criação de variáveis adicionais<br />
Novas variáveis são criadas, como 'rota', para análises mais detalhadas, como identificação de rotas com mais problemas de atraso e cancelamento.<br /><br />

12. Salvamento dos dados<br />
O DataFrame final é salvo em um arquivo CSV para uso posterior.<br />
</div>

[Script com o tratamento dos dados de voos](https://github.com/pedromateusalmeida/aviacao_brasileira/blob/main/scripts_v2/2_2_tratamento_dados.ipynb){ .md-button .md-button--primary }


## Documentação do processo de tratamento de dados meteorológicos
<div style="text-align: justify"><br />
1. Introdução<br />
Nesta seção, descrevemos as operações realizadas para carregar, transformar e padronizar dados meteorológicos a partir de arquivos CSV.<br /><br />

2. Carregamento e transformação de dados<br />
O processo começa com a função process_file, que executa as seguintes tarefas:<br />
- Carregamento de dados: O DataFrame é criado pulando as primeiras 8 linhas do arquivo CSV, que contêm informações da estação.<br />
- Extração de informações da estação: As primeiras 8 linhas são carregadas separadamente para extrair informações como latitude, longitude e altitude.<br />
- Conversão de coordenadas: As coordenadas são convertidas para o formato float, substituindo vírgulas por pontos para padronização.<br /><br />

3. Detecção de codificação de arquivos<br />
A função detect_encoding é usada para identificar a codificação de arquivos de texto, garantindo a leitura correta dos dados.<br /><br />

4. Padronização de nomes de colunas<br />
A função padronizar_nome_coluna realiza a limpeza e padronização dos nomes das colunas, removendo acentos, transformando em minúsculas e substituindo caracteres especiais.<br /><br />

5. Conversão de coordenadas DMS para decimal<br />
A função dms_to_decimal é aplicada para converter coordenadas do formato DMS (graus, minutos, segundos) para graus decimais.<br /><br />

6. Limpeza e padronização de nomes de aeródromos<br />
A função clean_name_aero é utilizada para limpar e padronizar nomes de aeródromos, removendo conteúdos entre parênteses, acentos e convertendo para maiúsculas.<br /><br />

7. Processamento e concatenação dos dados<br />
Os arquivos CSV são processados individualmente e concatenados em um único DataFrame. Nomes de colunas são renomeados e ajustados para uniformidade.<br /><br />

8. Conversão de tipos de dados<br />
Algumas colunas são convertidas para tipos específicos (como float64) para garantir consistência nos dados.<br /><br />

9. Agrupamento e resumo dos dados<br />
Os dados são agrupados por certas colunas-chave (data, hora, estação etc.) e resumidos para análise posterior.<br /><br />

10. Salvamento dos dados<br />
Os DataFrames tratados são salvos em formatos específicos (como Parquet e CSV) para uso posterior.<br />
</div>

[Script com o tratamento dos dados de meteorológicos](https://github.com/pedromateusalmeida/aviacao_brasileira/blob/main/scripts_v2/2_1_tratamento_dados_meterologicos.ipynb){ .md-button .md-button--primary }


## Documentação do processo de tratamento e análise de dados de voos com PySpark
<div style="text-align: justify"><br />
1. Configuração do ambiente Spark<br />
Inicialmente, o script configura o ambiente Spark, definindo parâmetros como número de núcleos, memória do driver, paralelismo padrão, e outras configurações relevantes para otimizar o desempenho do Spark.<br /><br />

2. Leitura dos dados meteorológicos<br />
Os dados meteorológicos previamente tratados são lidos do formato Parquet, com uma repartição inicial de 12 partições. Alterações são feitas em colunas específicas, como a conversão do tipo de 'hora_utc' e a renomeação da coluna 'estacao' para 'cidade'.<br /><br />

3. Preparação dos dataFrames de origem e destino<br />
O script prepara dois DataFrames separados para aeroportos de origem e destino, renomeando colunas de forma adequada para diferenciar os dados de origem e destino.<br /><br />

4. Leitura dos dados de voos<br />
Dados de voos históricos são lidos de um arquivo CSV, com repartição inicial de 6 partições. As colunas de datas de partida e chegada são convertidas para o tipo de dados 'datetime'.<br /><br />

5. Transformações e renomeações de colunas<br />
Transformações adicionais são aplicadas, incluindo a renomeação de colunas para padronizar nomes e a conversão de colunas de data para strings.<br /><br />

6. Mesclagem dos dados<br />
Realiza a mesclagem (join) dos dados de voos com os dados meteorológicos de destino e origem, utilizando colunas chave como critérios de junção.<br /><br />

7. Eliminação de duplicatas e reparticionamento<br />
O DataFrame resultante é limpo para remover duplicatas e é reparticionado para uma única partição.<br /><br />

8. Salvamento dos dados finais<br />
Finalmente, os dados combinados e tratados são salvos em um arquivo CSV para análises futuras.<br />
</div>

[Script de unificação dos dados meteorológicos + voos](https://github.com/pedromateusalmeida/aviacao_brasileira/blob/main/scripts_v2/2_4_tratamento_voos_meteorologia.ipynb){ .md-button .md-button--primary }
