# Análise Exploratória: Por trás das cortinas do catálogo Netflix
O que há por trás das recomendações da Netflix? Por que uma série de comédia, por exemplo, parece ter mais destaque que um drama épico? No mundo do streaming, onde os dados são a moeda principal, entender as tendências de produção e o comportamento da audiência é o segredo do sucesso.
Nesta análise, vamos mergulhar no vasto catálogo da Netflix para ir além das sinopses e dos pôsteres. Usando a ciência de dados, vamos desvendar padrões e responder a perguntas cruciais:

- A Netflix investe mais em filmes ou séries?
- Quais gêneros são os mais populares?
- Quem são os atores e diretores que dominam a plataforma?

Prepare-se para descobrir os segredos que os dados guardam sobre o gigante do streaming.

# 1. Visão Geral dos Dados
O catálogo da netflix é vasto, mas qual é sua composição? O dataset que iremos utilizar, que inclui títulos até o ano de 
2021, conta com 8806 registros.

- ```dF_netflix.shape``` mostra ```(8807,12)```, indicando 8807 linhas e 12 colunas
- ```df_netflix.info()``` revela que as colunas ```director```, ```cast```, ```country```, ```date_added```, ```rating``` e ```duration``` possuem valores ausentes.

# 2. Tratamento e Limpeza de Dados
A qualidade de uma análise de dados depende diretamente da qualidade dos dados que a alimentam. Por isso, antes de qualquer visualização ou cálculo, é fundamental identificar e tratar os valores ausentes.

## Identificação de Valores Ausentes.
Ao verificar e quantidade e a proporção de dados ausentes por coluna, descobrimos:
- ```director```: 2634 valores ausentes, representando cerca de 29,9% dos registros.
- ```cast```: 825 valores ausentes, representando certca 9,3%.
- ```country```: 831 valores ausentes, representando 9,4%.
- As outras colunas com valores ausentes (```date_added```, ```rating```, ```duration```) representam menos de 1% do total.

## Estratégia de Tratamento
Para não perdermos um número considerável de registros, optamos por uma estratégia híbrida:
- Preenchemos os valores ausentes nas colunas ```director```, ```cast``` e ```country``` com um valor categórico 'Unknow'.
- Removendo os valores ausentes restantes, que representavam menos de 1% do dataset.

# 3. Análise Exploratória de Dados (EDA)
Com os dados limpos e prontos para serem explorados, é hora de mergulhar na Análise Exploratória de Dados (EDA).

## Distribuição de Conteúdo: Filmes vs. Séries de TV
A primeira pergunta que queremos responder é: o catálogo da Netflix é composto por mais filmes ou séries de TV? Os dados revelam que a Netflix tem uma clara preferência por filmes, que representam mais de 69% de todo o catálogo do streaming.


- Filmes: 6.126 títulos (69.7%).



- Séries de TV: 2.664 títulos (30.3%).


## Crescimento do Catálogo ao Longo do Tempo
A Netflix de hoje é muito diferente daquela de 20 anos atrás. Sua estratégia de conteúdo evoluiu drasticamente. Com base nos dados, podemos ver uma clara aceleração na produção, especialmente após 2010. Este pico coincide com a decisão da empresa de investir pesado em conteúdo original e se transformar de uma distribuidora de filmes em uma potência de produção.


Podemos notar um crescimento exponencial, com um volume de lançamentos que atingiu seu auge por volta de 2019 e 2020. Isso reflete a consolidação da empresa no mercado global.

## Duração Média dos Filmes e Séries
Ao analisar a coluna 

```duration``` para todos os filmes, descobrimos que a duração média dos filmes na plataforma é de aproximadamente 99,58 minutos. Essa média indica que a Netflix segue o padrão da indústria, oferecendo filmes de longa-metragem que se encaixam no tempo de tela tradicional.



Ao filtrar os dados, encontramos as 5 séries de TV com o maior número de temporadas no catálogo:

- Grey's Anatomy: 17 temporadas.

- Supernatural: 15 temporadas.

- NCIS: 15 temporadas.

- Heartland: 13 temporadas.

- COMEDIANS of the world: 13 temporadas.

## A Origem Global do Conteúdo
A análise da produção por país revela muito sobre a estratégia de conteúdo da plataforma. O resultado confirma o domínio de alguns mercados, mas também destaca a ascensão de novas potências de produção.


- Os Estados Unidos dominam a lista.

- A forte presença de países como Índia, Reino Unido e Canadá demonstra a estratégia da Netflix de investir em mercados regionais.

## Classificação Indicativa: Para Quem a Netflix Produz?
A análise dos dados revela que a classificação mais comum no catálogo da Netflix é o "TV-MA", que indica conteúdo para audiências maduras. Esse resultado aponta para um investimento significativo em dramas complexos, comédias ácidas e produções que exploram temas mais adultos.


# 4. Conclusão: Os Principais Insights da Análise
Esta jornada pelo catálogo da Netflix nos permitiu ir além da superfície, transformando a simples curiosidade em insights concretos.


1. **O Dominante Global:** A Netflix tem uma clara preferência por filmes (69% do catálogo). A liderança do gênero "International Movies" e a predominância dos "Estados Unidos" como maior produtor reforçam a estratégia da plataforma em ser uma potência global.



2. **O Ciclo de Expansão:** Houve um crescimento exponencial, com um pico notável entre 2019 e 2020. Após esse período, os dados indicam uma desaceleração, sugerindo uma possível mudança de prioridade de "quantidade" para uma abordagem mais focada em "qualidade".



3. **Padrões de Produção:** Os filmes da plataforma têm uma duração média que se alinha com o padrão de Hollywood (aproximadamente 99 minutos).


4. **Público-Alvo Definido:** A distribuição da classificação indicativa revela um investimento significativo em conteúdo para um público maduro (classificações "TV-MA" e "TV-14").


5. **Foco nos Pilares do Catálogo:** "Dramas", "Comédias" e "Filmes Internacionais" são os pilares do catálogo da Netflix. A tendência de ascensão e queda observada no gráfico mostra que a estratégia de investimento da plataforma não é estática.


No fim das contas, a "mágica" por trás das recomendações da Netflix não é mágica; é uma ciência de dados complexa e fascinante. Espero que esta análise tenha te dado uma nova perspectiva sobre a sua plataforma de streaming favorita.
