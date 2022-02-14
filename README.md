# shipping_predictions
Projeto que utiliza dados em painel para prever as remessas de uma empresa de comércio para diversas regiões

## Objetivos

O objetivo do projeto é utilizar dados de painel de reemessas de diversos clusters distintos de modo a
conseguir prever o a quantidade de remessas de cada um desses cluster para o período de setembro de 2020.
Os dados disponíveis para o treinamento do modelo são referentes ao período de 01/10/2019 a 31/08/2020.
Além das informações de cluster e data, também possuímos informações rereferentes ao volume e ao dropsize.
O dropsize é a razão entre volume e remessa.

Mais especicamente desenvolvemos três modelos distintos:
  1. No primeiro fazemos projeções de remessas a partir da utilização de uma função de distribuição de probabilidade que seja representativa do processo de geração de dados. Essa função de distribuição é condicionada ao cluster e ao dia da semana.
  2. No segundo modelo, introduzimos análise intertemporal para realizar um modelo de regressão linear. Dessa forma introduzimos a tendência ao longo do tempo como um preditor das remessas futuras.
  3. No terceiro modelo, continuamos com os mesmos preditores do segundo, porém utilizamos uma modelagem de regressão por árvore, dessa forma conseguimos explorar melhor as interações entre os atributos preditores e a não linearidade da ocorrência de remessas ao longo do tempo.