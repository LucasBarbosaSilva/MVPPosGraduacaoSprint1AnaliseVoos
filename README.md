<h1 align="center"> MVP - Pós-Graduação PUC RJ - Sprint 1 </h1>
<h2 align="center">Análise dos Microdados da Agência Nacional de Aviação Civil (Anac) </h2>
<p align="center">Projeto desenvolvido durante a Sprint 1 - Engenharia de Dados da Pós Graduação em Ciência de Dados da PUC Rio. Consiste em uma análise feita em cima da base de microdados disponibilizada pela Agência Nacional de Aviação Civil (Anac)</p>

### Objetivo:
Para este projeto iremos explorar 3 indicadores:
- Quantidade de voos realizado por empresa aérea, por rota e variando por mês, semestre e ano;
- Total de passageiros transportados por empresa aérea, por rota e variando por mês, semestre e ano;
- Quais as rotas com maior custo benefício baseado na relação entre passageiros pagantes e consumo de combustível, variando por mês, semestre e ano;

### Plataforma:
A plataforma utilizada para o desenvolvimento deste projeto foi o [Databricks Free Edition](https://dbc-e2e6cd1f-62ba.cloud.databricks.com/?o=2179636621597322).

### Base de dados:
A Anac disponibiliza arquivos csv com dados de cada voo feito no espaço aéreo brasileiro disponível nesse [link](https://www.gov.br/anac/pt-br/assuntos/regulados/empresas-aereas/Instrucoes-para-a-elaboracao-e-apresentacao-das-demonstracoes-contabeis/descricao-de-variaveis). 
Além dos dados brutos, a Anac também disponibiliza uma descrição detalhada destas variáveis [aqui](https://www.gov.br/anac/pt-br/assuntos/regulados/empresas-aereas/Instrucoes-para-a-elaboracao-e-apresentacao-das-demonstracoes-contabeis/descricao-de-variaveis).
A base de dados já está dividida em duas dimensôes: etapa básica e etapa combinada. Para este trabalhado, utilizaremos apenas a etapa básica. 

> Etapa Básica (flight stage): As etapas básicas são aquelas realizadas pela aeronave desde a sua decolagem até o próximo pouso, independentemente de onde tenha ocorrido o embarque ou o desembarque do objeto de
> transporte. Os dados estatísticos das etapas básicas representam o status da aeronave em cada etapa do voo, apresentando a movimentação de cargas e passageiros entre os aeródromos de origem e destino da aeronave.
> É a operação de uma aeronave entre uma decolagem e o próximo pouso, a ligação entre dois aeródromos.

### Coleta:
A coleta, inicialmente, será realizada utilizando um notebook python e para baixar os registros e salvar no ambiente do Databricks. Como os dados disponibilizados pela Anac variam desde o ano 2000 até o ano atual, para facilitar a análise, iremos internalizar apenas dados dos últimos cinco anos.
