# Contextualização

## A Problemática
O Brasil enfrenta um desafio significativo com as queimadas, que têm consequências devastadoras para a biodiversidade, os ecossistemas, e as comunidades humanas. Estas queimadas são influenciadas por uma complexa interação de fatores naturais e antrópicos, tornando-se uma questão ambiental, social e econômica de grande importância. Neste contexto, surge o Projeto para Análise de Dados Históricos de Queimadas no Brasil, uma iniciativa dedicada a desvendar as dinâmicas e impactos desses eventos ao longo do tempo.

## Descrição do projeto
Neste contexto, o presente projeto se propõe a realizar uma análise detalhada dos focos de queimadas e das áreas afetadas. O escopo geográfico abrange todos os estados brasileiros e biomas, oferecendo uma visão ampla e detalhada das tendências, padrões e anomalias relacionadas às queimadas ao longo dos anos.

## Objetivo
O principal objetivo do projeto é fornecer uma compreensão abrangente do cenário histórico das queimadas no país, identificando padrões temporais e espaciais, variações sazonais e influência de fatores humanos e naturais. Além de traçar um panorama histórico, o projeto visa gerar insights estratégicos para o desenvolvimento de políticas e medidas eficazes de prevenção e controle de incêndios.

## Justificativa
A justificativa para tal empreitada reside na urgência em combater as queimadas no Brasil, mitigar seus impactos negativos e proteger os recursos naturais vitais para o bem-estar das futuras gerações. Ao fornecer uma base de dados sólida e análises profundas, o projeto busca embasar decisões políticas e ações comunitárias, direcionando esforços para a conservação ambiental e a sustentabilidade.

# Base de Dados

## Fontes dos dados {.tabset .tabset-fade}

Este projeto utiliza dois conjuntos de dados primários para analisar historicamente as queimadas no Brasil, cada um oferecendo perspectivas únicas sobre a frequência de queimadas e a extensão das áreas afetadas. A seguir, detalhamos cada um desses conjuntos de dados em termos de sua natureza, cobertura e fonte. A utilização destes dados permite:<br>
**Análise Temporal:** Acompanhar a evolução das queimadas ao longo de mais de três décadas, identificando tendências, padrões sazonais e variações ano a ano.<br>
**Análise Espacial:** Observar como as queimadas se distribuem geograficamente entre diferentes estados e biomas, revelando áreas mais vulneráveis ou afetadas.<br>
**Impacto Ambiental:** Estudar as consequências das queimadas nos ecossistemas, na biodiversidade e na cobertura do solo, apoiando ações de conservação e recuperação.<br>
**Fundamentação de Políticas:** Basear decisões políticas e estratégias de mitigação em dados concretos, visando reduzir a incidência e os impactos das queimadas.<br>
Esses conjuntos de dados, com sua riqueza de informações e cobertura abrangente, são essenciais para conduzir uma análise detalhada e fundamentada sobre as queimadas no Brasil, servindo de alicerce para este projeto e suas conclusões.

### Focos Queimadas

Os dados de fontes de **focos de queimadas** foram extraídos do **BD Queimadas** é uma base de dados mantida pelo Instituto Nacional de Pesquisas Espaciais (INPE), destinada ao monitoramento de focos de queimadas em todo o território brasileiro. Este conjunto de dados contém registros de focos de incêndio identificados por satélites, catalogados mensalmente e distribuídos por estado e bioma. A abrangência temporal vai de 1988 até 2024, fornecendo uma visão longitudinal da incidência de queimadas no país. <br>

Instituto Nacional de Pesquisas Espaciais (INPE). O INPE é uma entidade pública brasileira dedicada à pesquisa espacial e climática, reconhecida mundialmente por seu trabalho em monitoramento ambiental via satélite. O BD Queimadas é acessível publicamente, refletindo o compromisso do INPE com a transparência e a disseminação de informações ambientais cruciais.

### Áreas Queimadas

Os **dados de áreas queimadas** foram extraídos do **MapBiomas Fogo**, parte da iniciativa mais ampla do MapBiomas, fornece dados anuais sobre a extensão das áreas queimadas no Brasil. Este conjunto de dados é resultado de uma colaboração entre organizações de pesquisa, universidades e ONGs, que empregam imagens de satélite e algoritmos avançados para mapear as cicatrizes deixadas pelas queimadas em diferentes biomas, estados e classes de cobertura do solo. A série histórica cobre o período de 1985 a 2022.<br>

MapBiomas Fogo é um esforço colaborativo que envolve várias instituições, incluindo universidades, ONGs ambientais e institutos de pesquisa. O projeto é parte do MapBiomas, uma iniciativa interinstitucional que busca mapear as transformações na cobertura e uso do solo no Brasil ao longo das décadas, fornecendo dados valiosos para a compreensão e gestão dos recursos naturais e impactos ambientais.

## Legenda dos Dados


# Metodologia
## Descrição das Etapas
A análise de dados históricos de queimadas no Brasil adotada neste projeto segue uma metodologia rigorosa e estruturada, composta por várias etapas críticas que, juntas, garantem uma abordagem sistemática para descobrir insights valiosos e informar decisões estratégicas. Este processo metodológico começa com o carregamento de pacotes essenciais para a análise, seguido pela leitura dos dados, manipulação, análise exploratória e, finalmente, análise gráfica. Embora cada etapa tenha sua função específica, juntas, elas formam uma abordagem coesa que maximiza o potencial dos dados disponíveis.<br>

Adotar esta metodologia estruturada e integrada potencializa a capacidade de extrair conhecimento significativo dos dados, permitindo uma compreensão detalhada das dinâmicas de queimadas no Brasil. A abordagem permite identificar não apenas os padrões existentes, mas também prever tendências futuras e informar ações preventivas. Além disso, a metodologia suporta a transparência e a replicabilidade da análise, aspectos fundamentais para a validação e confiança nos resultados obtidos.<br>

Em suma, essa abordagem metodológica não apenas assegura a rigorosidade científica e a precisão analítica necessárias para um estudo dessa natureza, mas também oferece uma estrutura através da qual insights complexos podem ser desvendados e comunicados de forma eficaz, contribuindo para a gestão efetiva e sustentável das queimadas no Brasil.<br>

**Carregamento dos Pacotes**<br>
O primeiro passo envolve a preparação do ambiente de análise de dados, o que inclui a instalação e o carregamento de pacotes e bibliotecas necessários. Para este projeto, utilizamos linguagens de programação estatística como R e Python, que possuem vastas bibliotecas para manipulação de dados, análise estatística, e visualização de dados, tais como pandas, numpy, matplotlib, seaborn para Python e dplyr, ggplot2, tidyr para R. Essas ferramentas são essenciais para manipular conjuntos de dados grandes e complexos, permitindo análises detalhadas e a criação de visualizações avançadas.<br>

**Leitura dos Dados**<br>
Após preparar o ambiente, procedemos com a leitura dos dados dos conjuntos de dados do BD Queimadas do INPE e do MapBiomas Fogo. Nesta etapa, os dados são carregados para o ambiente de programação a partir de seus formatos originais, que podem ser CSV, Excel ou diretamente de uma API. A leitura eficaz dos dados é crucial para garantir a integridade e a precisão das análises subsequentes.<br>

**Análise Exploratória**<br>
A análise exploratória dos dados oferece a oportunidade de mergulhar profundamente nas características intrínsecas dos dados, identificando padrões, tendências, e possíveis anomalias. Esta etapa é fundamental para formular hipóteses bem informadas e direcionar a análise subsequente de forma mais focada e eficiente.<br>

**Análise Gráfica**<br>
Por fim, a análise gráfica não apenas sintetiza e destaca os resultados das análises de forma visualmente acessível, mas também revela insights que poderiam ser menos óbvios em uma análise puramente numérica. A representação gráfica dos dados facilita a compreensão dos fenômenos analisados, permitindo uma interpretação mais intuitiva e imediata dos resultados.

## KPIs, índices e indicadores
**1. Número Anual de Focos de Queimadas**<br>
Descrição: Total de focos de queimadas identificados por satélite em uma área específica por ano.
Utilidade: Permite avaliar a frequência das queimadas ao longo do tempo, identificar tendências e avaliar a eficácia das medidas de prevenção.<br>
**2. Área Total Queimada Anualmente**
Descrição: Superfície total afetada por queimadas em hectares ou quilômetros quadrados, por ano.
Utilidade: Fornece uma medida do impacto das queimadas, essencial para avaliar a severidade e a extensão dos danos ao ecossistema e à biodiversidade.<br>
**3. Taxa de Variação Anual dos Focos de Queimadas**
Descrição: Variação percentual no número de focos de queimadas de um ano para o outro.
Utilidade: Ajuda a identificar aumentos ou reduções significativas na frequência das queimadas, indicando tendências e a necessidade de investigação ou ação.<br>
**4. Índice de Sazonalidade**
Descrição: Medida da variação sazonal dos focos de queimadas, calculada como a proporção de queimadas em diferentes épocas do ano.<br>
Utilidade: Crucial para entender padrões sazonais, planejar ações preventivas e alocar recursos de forma eficaz em períodos de alto risco.<br>
**5. Distribuição Espacial de Queimadas**
Descrição: Localização geográfica dos focos de queimadas, normalmente apresentada através de mapas de calor ou análises de hotspots.
Utilidade: Permite a identificação de áreas críticas, facilitando ações direcionadas e a gestão de territórios vulneráveis.<br>
**6. Taxa de Recorrência de Queimadas**
Descrição: Frequência com que determinadas áreas experimentam queimadas repetidas ao longo do tempo.
Utilidade: Indica áreas com alta susceptibilidade a queimadas recorrentes, sugerindo a necessidade de estratégias de manejo específicas.<br>
**7. Comparação entre Áreas Protegidas e Não Protegidas**
Descrição: Análise do número de focos de queimadas e da área queimada em regiões protegidas versus não protegidas.
Utilidade: Avalia a eficácia das áreas protegidas na prevenção de queimadas e na conservação da biodiversidade.<br>
**8. Impacto das Queimadas por Bioma**
Descrição: Avaliação específica do número de focos de queimadas e da área queimada em cada bioma brasileiro.
Utilidade: Permite análises direcionadas para a conservação de biomas específicos e a implementação de políticas ambientais adaptadas.<br>
**9. Efetividade de Políticas Públicas e Ações de Mitigação**
Descrição: Avaliação do impacto de políticas e ações de mitigação na redução do número de focos de queimadas e na área queimada.
Utilidade: Fornece feedback sobre a eficácia de estratégias implementadas, orientando ajustes e melhorias.

# Análise dos Dados

## Carregamento dos Pacotes
Para realizar análises de dados no R, é essencial carregar pacotes específicos que fornecem funções e ferramentas necessárias. O processo inicia com a utilização do comando `library` para cada pacote desejado. Iniciamos carregando `readr` para leitura eficiente de dados, seguido por `dplyr` para manipulação de dados e `ggplot2` para visualizações avançadas. `patchwork` permite combinar gráficos, enquanto `tidyr` ajuda na organização dos dados. `lubridate` facilita o trabalho com datas, e `ggthemes` oferece temas adicionais para gráficos. `psych`, `car`, e `qqplotr` são úteis para análises estatísticas, `hexbin` para visualizações hexagonais, e `zoo` para séries temporais. `plotly` permite criar gráficos interativos. Para a documentação e apresentação dos resultados, `rmarkdown`, `knitr`, e `kableExtra` são fundamentais, permitindo a criação de relatórios dinâmicos e tabelas avançadas. Este conjunto de pacotes equipa o analista com uma gama abrangente de ferramentas para executar desde a leitura de dados até a apresentação de análises complexas de forma eficiente e eficaz.
```{r Carregamento dos Pacotes, warning=F, message=F}
library(readr)
library(dplyr)
library(ggplot2)
library(patchwork)
library(tidyr)
library(lubridate)
library(ggthemes)
library(psych) 
library(car) 
library(qqplotr)
library(hexbin)
library(zoo)
library(plotly)



library(rmarkdown)
library(knitr)
library(kableExtra)
```

## Leitura dos Dados {.tabset .tabset-fade}
### Script
Para definir o diretório de trabalho no R e ler os dados de um arquivo CSV, primeiramente usamos a função `setwd()` para especificar o caminho do diretório onde os arquivos estão localizados. Isso facilita o acesso aos arquivos sem a necessidade de especificar o caminho completo a cada vez que precisamos abrir um arquivo. Em seguida, utilizamos a função `read_csv2()` do pacote readr para carregar os dados do arquivo `focos_queimadas.csv` em um dataframe chamado `dados.bruto`. Essa função é particularmente útil para ler arquivos CSV que usam `;` como separador, comum em muitos países que não usam a vírgula como delimitador decimal. Por fim, a função `iconv()` é aplicada à coluna `ESTADO` para converter a codificação de caracteres de `"latin1"` para `"UTF-8"`, garantindo que os caracteres especiais sejam exibidos corretamente no R. Este processo é essencial para a manipulação e análise adequadas dos dados em projetos de análise de dados.
```{r Leitura dos Dados, warning=F, message=F}
setwd('C:/Users/Alysson Santos/Desktop/DRIVE/ESTUDOS/ENG. AMBIENTAL/CURSO LINGUAGEM R/PRATICAS R/bases dados')
dados.bruto <- read_csv2('focos_queimadas.csv')
dados.bruto$ESTADO <- iconv(dados.bruto$ESTADO, from = "latin1", to = "UTF-8")

```

### Base de Dados

Análise de Dados Históricos de Focos de Queimadas nos Biomas Brasileiros. Utilizando dados históricos e padrões temporais, esses sistemas podem mitigar os impactos dos incêndios, protegendo a biodiversidade e os meios de subsistência das comunidades locais. Cada um dos 06 biomas apresentam características distintas e enfrentam desafios específicos relacionados a incêndios.

```{r Visualização dos Dados, warning=F, message=F, echo =F}

kable(head(dados.bruto, 10)) %>% 
  kable_styling(bootstrap_options = c('hover', 'responsive'))

```

## Manipulação dos Dados {.tabset .tabset-fade}
### Script
Neste trecho de código R, os dados brutos são primeiramente transformados para um formato mais longo utilizando a função `pivot_longer` do pacote `tidyr`, especificamente nas colunas que representam os meses, criando duas novas colunas: `'MESES'` para os nomes dos meses e `'FOCOS'` para os valores correspondentes de focos de queimadas. Posteriormente, é feita uma correspondência entre os nomes dos meses e seus respectivos números com a função `match`, e uma nova coluna `'DATA'` é criada usando `make_date` para combinar o ano e o mês em uma única entrada de data.<br>

Os dados são então divididos em dois conjuntos distintos com a função filter do pacote `dplyr:` um contendo apenas os dados relacionados a biomas `(dados.bioma)` e outro contendo dados referentes ao Brasil, excluindo os biomas `(dados.brasil)`. Para cada um desses conjuntos de dados, é calculada uma nova variável `foco.area`, que representa a densidade de focos de queimadas por quilômetro quadrado, através da divisão do número de focos pela área. Este processo de manipulação de dados permite uma análise mais detalhada e específica tanto para diferentes regiões do Brasil quanto para seus biomas, facilitando a compreensão da distribuição e intensidade das queimadas.

```{r Manipulação dos Dados, warning=F, message=F}
dados.bruto <- pivot_longer(dados.bruto, cols=c(5:16), names_to='MESES', values_to='FOCOS') %>% 

mutate(MES=match(MESES, c('jan', 'fev', 'mar', 'abr', 'mai', 'jun',
                          'jul', 'ago', 'set', 'out', 'nov', 'dez')),
  DATA = make_date(ANO, MES, 1))

dados.bioma <- filter(dados.bruto, REGIAO=='Bioma')

dados.brasil <- filter(dados.bruto, REGIAO!='Bioma')

dados.bioma <- dados.bioma %>%

  mutate(foco.area=FOCOS/`AREA(km2)`)

dados.brasil <- dados.brasil %>%
  
  mutate(foco.area=FOCOS/`AREA(km2)`)

```

### Base Brasil

```{r Base Brasil, warning=F, message=F, echo =F}

kable(head(dados.brasil, 10)) %>% 
  kable_styling(bootstrap_options = c('hover', 'responsive'))

```

### Base Biomas

```{r Base Biomas, warning=F, message=F, echo =F}

kable(head(dados.bioma, 10)) %>% 
  kable_styling(bootstrap_options = c('hover', 'responsive'))

```

## Análise Exploratória  {.tabset .tabset-fade}
### Brasil

Análise de Dados Históricos de Focos de Queimadas nos Biomas Brasileiros. Utilizando dados históricos e padrões temporais, esses sistemas podem mitigar os impactos dos incêndios, protegendo a biodiversidade e os meios de subsistência das comunidades locais. Cada um dos 06 biomas apresentam características distintas e enfrentam desafios específicos relacionados a incêndios.

```{r Estatistica Descritiva  Brasil, warning=F, message=F, echo =F}
kable(describe(dados.brasil)) %>% 
  kable_styling(bootstrap_options = c('hover', 'responsive'))
```
### Biomas

Análise de Dados Históricos de Focos de Queimadas nos Biomas Brasileiros. Utilizando dados históricos e padrões temporais, esses sistemas podem mitigar os impactos dos incêndios, protegendo a biodiversidade e os meios de subsistência das comunidades locais. Cada um dos 06 biomas apresentam características distintas e enfrentam desafios específicos relacionados a incêndios.

```{r Estatistica Descritiva  Bioma, warning=F, message=F, echo =F}
kable(describe(dados.bioma)) %>% 
  kable_styling(bootstrap_options = c('hover', 'responsive'))

```

## Análise Gráfica

4.1 Gráfico da Distribuição Histórica Anual
Gráfico Colunas N° Focos total X Ano por Bioma

```{r grafico1, warning=F, message=F, echo =F}
ggplotly(ggplot(dados.bioma, aes(x = ANO, y =FOCOS)) + 
  geom_bar(stat = "summary", fun = sum, col=NA, fill='red')+
  facet_wrap(~ESTADO)+
  #scale_x_date(date_breaks = "1 year", date_labels = '%Y')+
  theme(axis.text.x = element_text(angle = 90, hjust = 1))+
  theme_clean()

)
```

```{r grafico11, warning=F, message=F, echo =F}
ggplot(dados.bioma, aes(x = ANO, y =FOCOS)) + 
  geom_bar(stat = "summary", fun = sum, col=NA, fill='red')+
  facet_wrap(~ESTADO)+
  #scale_x_date(date_breaks = "1 year", date_labels = '%Y')+
  theme(axis.text.x = element_text(angle = 90, hjust = 1))+
  theme_clean()
```

Gráfico Colunas N° Focos/Área X Ano por Bioma

```{r grafico2, warning=F, message=F, echo =F}
ggplotly(ggplot(dados.bioma, aes(x = ANO, y =foco.area)) + 
  geom_bar(stat = "summary", fun = sum, col=NA, fill='red')+
  facet_wrap(~ESTADO)+
  #scale_x_date(date_breaks = "1 year", date_labels = '%Y')+
  theme(axis.text.x = element_text(angle = 90, hjust = 1))+
  theme_clean()

)
```

Gráfico Colunas N° Focos médio X Mês por Bioma

```{r grafico3, warning=F, message=F, echo =F}
ggplotly(ggplot(dados.bioma, aes(x = month(DATA, label=T), y =FOCOS)) + 
  geom_bar(stat = "summary", fun = mean, col=NA, fill='salmon')+
  facet_wrap(~ESTADO)+
  theme_clean()
)
```

Gráfico Colunas N° Focos/Área X Mês por Bioma

```{r grafico4, warning=F, message=F, echo =F}
ggplotly(ggplot(dados.bioma, aes(x = month(DATA, label=T), y =foco.area)) + 
  geom_bar(stat = "summary", fun = sum, col=NA, fill='salmon')+
  facet_wrap(~ESTADO)+
  #scale_x_date(date_breaks = "2 year", date_labels = '%Y')+
  #theme(axis.text.x = element_text(angle = 90, hjust = 1))+
  theme_clean()
)
```
