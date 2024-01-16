## Extração dos dados

<div style="text-align: justify"><br />
Foram desenvolvidas três funções para extrair os dados de forma prática, eficiente e sem sobrecarga dos servidores que os disponibilizam.<br />
</div>

## Download de Arquivos CSV de Dados Históricos de Voos (Função download_csv_files)
<div style="text-align: justify"><br />
Objetivo: Essa função foca no download de dados históricos de voos para um ano específico a partir do site da ANAC.<br /><br />
Processo: Inicia-se configurando uma sessão de requests com políticas de retry para lidar com falhas de conexão ou timeouts. Após isso, realiza-se uma requisição GET para o site da ANAC, analisando o conteúdo HTML para localizar os links de download. Os arquivos CSV são, então, baixados mês a mês, com uma pausa entre cada download para não sobrecarregar o servidor.<br /><br />
Resultado: Os arquivos CSV são salvos localmente, proporcionando um conjunto de dados detalhados sobre voos no ano especificado.<br /><br />
</div>

## Download e Conversão de Dados Complementares (Função download_dados_complementares)
<div style="text-align: justify"><br />
Objetivo: Essa função é responsável pelo download de arquivos complementares relacionados a dados de voos, como glossários de aeródromos e empresas aéreas.<br /><br />
Processo: O método inclui a definição das URLs para download, a criação de diretórios para armazenamento e a execução do download. Além disso, há uma etapa de conversão de arquivos .xls para o formato .csv, com ajustes nas colunas quando necessário.<br /><br />
Resultado: Os arquivos baixados e convertidos são armazenados localmente, enriquecendo a base de dados com informações adicionais relevantes para a análise.<br /><br />
</div>

## Download e Extração de Dados Climáticos (Função download_and_extract_climate_data)
<div style="text-align: justify"><br />
Objetivo: Focada em dados climáticos, esta função busca coletar informações do clima de um ano específico do portal do INMET.<br /><br />
Processo: Similarmente à primeira função, configura-se uma sessão de requests com regras de retry. A função constrói a URL do arquivo ZIP desejado, faz o download e, em seguida, extrai seu conteúdo em um diretório especificado.<br /><br />
Resultado: Os dados climáticos são disponibilizados localmente em formato descompactado, agregando uma camada de informação ambiental para a análise.<br /><br />
Essas funções, em conjunto, formam a espinha dorsal do processo de extração de dados do projeto, garantindo uma coleta de dados abrangente, sistemática e eficiente. Com dados históricos de voos, informações complementares e dados climáticos em mãos, vamos para o tratamento e limpeza de dados. <br /><br />
</div>

<center>
[Repositório com as funções](https://github.com/pedromateusalmeida/aviacao_brasileira/blob/main/scripts_v2/1_extracao_dados.ipynb){ .md-button .md-button--primary }
<center>