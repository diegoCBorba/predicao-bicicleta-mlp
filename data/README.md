# Bike Sharing Dataset

## Autor
Hadi Fanaee-T  
Laboratory of Artificial Intelligence and Decision Support (LIAAD), University of Porto  
INESC Porto, Campus da FEUP  
Rua Dr. Roberto Frias, 378  
4200 - 465 Porto, Portugal  

## Background
Bike-sharing systems são uma nova geração de aluguel de bicicletas, onde todo o processo, desde a adesão até a devolução, é automatizado. Através desses sistemas, os usuários podem alugar uma bicicleta em um local e devolvê-la em outro.

Atualmente, existem mais de 500 programas de compartilhamento de bicicletas no mundo, com mais de 500 mil bicicletas. Esses sistemas são de grande interesse devido ao seu papel no trânsito, meio ambiente e saúde pública.

Além das aplicações práticas, os dados gerados por esses sistemas são úteis para pesquisa. Diferente de outros transportes, como ônibus e metrô, os sistemas de compartilhamento registram explicitamente a duração das viagens, locais de partida e chegada. Assim, tornam-se uma rede de sensores virtuais que possibilita a análise da mobilidade urbana.

## Conjunto de Dados
O processo de aluguel de bicicletas está altamente correlacionado com fatores ambientais e sazonais, como clima, precipitação, dia da semana, estação do ano e horário do dia.

O conjunto de dados contém registros históricos de 2011 e 2012 do sistema Capital Bikeshare, em Washington D.C., EUA. Os dados foram coletados de forma pública no site [Capital Bikeshare](http://capitalbikeshare.com/system-data). Os registros foram agregados em bases horárias e diárias e complementados com informações climáticas extraídas de [FreeMeteo](http://www.freemeteo.com).

## Tarefas Associadas

### Regressão
Predição da quantidade de bicicletas alugadas por hora ou por dia, baseada em fatores ambientais e sazonais.

### Detecção de Eventos e Anomalias
A contagem de bicicletas alugadas pode estar correlacionada a eventos na cidade, que podem ser verificados por meio de mecanismos de busca. Por exemplo, a busca por "2012-10-30 washington d.c." no Google retorna informações sobre o furacão Sandy. Alguns eventos importantes estão listados na referência [1]. Assim, o conjunto de dados pode ser utilizado para validar algoritmos de detecção de eventos e anomalias.

## Arquivos Disponíveis
- `Readme.txt` - Informações sobre o conjunto de dados.
- `hour.csv` - Contagem de bicicletas alugadas por hora (17.379 registros).
- `day.csv` - Contagem de bicicletas alugadas por dia (731 registros).

## Características do Conjunto de Dados
Os arquivos `hour.csv` e `day.csv` possuem os seguintes campos (exceto `hr`, que não está presente em `day.csv`):

- `instant`: índice do registro
- `dteday`: data
- `season`: estação do ano (1: primavera, 2: verão, 3: outono, 4: inverno)
- `yr`: ano (0: 2011, 1: 2012)
- `mnth`: mês (1 a 12)
- `hr`: hora do dia (0 a 23, apenas em `hour.csv`)
- `holiday`: indica se o dia é feriado (dados obtidos de [dchr.dc.gov](http://dchr.dc.gov/page/holiday-schedule))
- `weekday`: dia da semana
- `workingday`: indica se é um dia útil (1: dia útil, 0: fim de semana ou feriado)
- `weathersit`: situação climática:
  - 1: Céu limpo, poucas nuvens, parcialmente nublado
  - 2: Neblina + nublado, neblina + poucas nuvens
  - 3: Neve leve, chuva leve + trovoada + nuvens dispersas
  - 4: Chuva forte + tempestade, neve + neblina
- `temp`: temperatura normalizada (valores divididos por 41, temperatura máxima em Celsius)
- `atemp`: temperatura aparente normalizada (valores divididos por 50)
- `hum`: umidade normalizada (valores divididos por 100)
- `windspeed`: velocidade do vento normalizada (valores divididos por 67)
- `casual`: contagem de usuários ocasionais
- `registered`: contagem de usuários registrados
- `cnt`: total de bicicletas alugadas (casual + registered)

## Licença
O uso deste conjunto de dados em publicações deve ser citado conforme a seguinte referência:

[1] Fanaee-T, Hadi, and Gama, Joao, "Event labeling combining ensemble detectors and background knowledge", *Progress in Artificial Intelligence* (2013): pp. 1-15, Springer Berlin Heidelberg, [doi:10.1007/s13748-013-0040-3](http://dx.doi.org/10.1007/s13748-013-0040-3).

### Citação em formato acadêmico:
```bibtex
@article{
  year={2013},
  issn={2192-6352},
  journal={Progress in Artificial Intelligence},
  doi={10.1007/s13748-013-0040-3},
  title={Event labeling combining ensemble detectors and background knowledge},
  url={http://dx.doi.org/10.1007/s13748-013-0040-3},
  publisher={Springer Berlin Heidelberg},
  keywords={Event labeling; Event detection; Ensemble learning; Background knowledge},
  author={Fanaee-T, Hadi and Gama, Joao},
  pages={1-15}
}
```

## Contato
Para mais informações sobre este conjunto de dados, entre em contato com:
**Hadi Fanaee-T** - hadi.fanaee@fe.up.pt

