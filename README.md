# [ZonasPMF](http://arthurmo.github.io/zonaspmf)

Informa um endereço e ele retorna a zona definida pelo plano diretor de Fortaleza.

## Limitações

O sistema é todo client-side. Os dados são enviados para o browser e processados lá. Desta forma, arquivos muito pesados (de 8mb para o zoneamento e de 11mb para a hidrografia) são enviados para o navegador sempre. Isso torna o processamento lento. Como solução poderiamos ter os dados todos armazenados num banco de dados Postgree com o PostGIS e receber apenas a informação específica da zona de interesse.

Outra limitação é o fato de usarmos o sistema de [geocoding do Google] (https://developers.google.com/maps/documentation/geocoding/?hl=pt-br) que tem um limite de consultas de 2.500 solicitações de geolocalização por dia. Esse valor sobe para 1000.000 solicitações caso utilize o Google Maps para Empresas. Criar um algorítmo de geocoding não é dificil, mas é necessário um grande trabalho contínuo de atualização de base e adaptação dos dados. Por enquanto, mesmo não sendo possível tornar esse um sistema massivo, é a melhor opção.

## Possibilidades

Já havia pensando em um sistema que pudesse dar todos os índices urbanísticos para quem for construir. E fazer mais, como por exemplo possibilitar o usuário de desenhar o próprio terreno. O sistema calcularia por exemplo o índice de aproveitamento (IA) do terreno, e todos os outros índices disponíveis. Em um segundo momento a pessoa poderia desenhar dentro do terreno, os limites da edificação que pretende construir e o sistema iria mostrar onde ele poderia construir, desenhando os recuos automaticamente e abatendo o IA e TO (taxa de ocupação) a medida que fosse fazendo o desenho.
