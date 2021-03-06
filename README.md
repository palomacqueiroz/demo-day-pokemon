# Data Lovers

## Índice

- [1. Preâmbulo](#1-preâmbulo)
- [2. Resumo](#2-resumo)
- [3. Tema](#3-tema)
- [4. Como funciona?](#4-como-funciona)
- [5. Protótipos](#5-protótipos)
- [6. Histórias de Usuário](#6-histórias-de-usuário)
- [7. Testes de Usabilidade](#7-testes-de-usabilidade)
- [8. Checklist](#8-checklist)

---

## 1. Preâmbulo

Segundo a [Forbes](https://www.forbes.com/sites/bernardmarr/2018/05/21/how-much-data-do-we-create-every-day-the-mind-blowing-stats-everyone-should-read) 90% dos dados que existem hoje foram gerados durante os últimos dois anos. A cada dia geramos 2.5 milhões de terabytes de dados, uma cifra sem precedentes.

Apesar disso, os dados por si só são de pouca utilidade. Para que essas grandes quantidades de dados se convertam em **informação** compreensível para os usuários, precisamos entender e processar estes dados. Uma forma simples de fazer isso é criando _interfaces_ e _visualizações_.

Na imagem seguinte, você pode ver como os dados que estão na parte esquerda podem ser usados para construir a interface amigável e compreensível que está na parte direita.


## 2. Resumo

Aplicação desenvolvida como segundo projeto da SAP006 da Laboratória, com o objetivo de exibir as informações fornecidas de acordo com o tema em uma interface pensando nas necessidades do usuário.

## 3. Tema

O tema escolhido para a aplicação foi o popular jogo mobile Pokemon Go em que o jogador pode viver a experiência de tornar-se um treinador Pokemon e aventurar-se nesse universo, participando de batalhas com outros jogadores enquanto interage com o mundo ao seu redor.

## 4. Como funciona?

As informações dos pokemons estão distribuídas pela interface em cards enfileirados que possuem as seguintes informações: nome, número, HP (health points), CP (combat points), imagem, peso, altura, ataques especiais, tipos dos ataques especiais, fraquezas e resistências do pokemon. O principal modo de navegação da aplicação é uma dashboard lateral onde estão localizadas as funcionalidades que definirão o modo como os cards são exibidos na tela. As seguintes funcionalidades foram implementadas: 

- O usuário pode filtrar os pokemons pelo tipo por meio de uma barra de pesquisa. Os pokemons serão ordenados de acordo com a sequência das letras inseridas.

<img src="filtrar-por-nome.gif" alt="Barra de pesquisa para filtrar pokemons pelo nome">

- Ordenar os cards numericamente de 001-251 ou de 251-001.

<img src="ordem-numerica.gif" alt="Botão para selecionar a ordem númerica">

- Ordenar os cards alfabeticamente de A-Z ou de Z-A.

<img src="ordem-alfabetica.gif" alt="Botão para selecionar a ordem afabética">

- Ordenar o CP dos pokemons em ordem crescente ou decrescente.

<img src="ordem-cp.gif" alt="Botão para selecionar a ordem do CP">

- Exibir os pokemons filtrados pelo tipo e a porcentagem de pokemons do tipo selecionado.

<img src="filtrar-por-tipo.gif" alt="Botão para filtrar pelo tipo">

- Além da possibilidade de utilizar um slider superior em que os pokemons são exibidos de acordo com a geração selecionada pelo usuário.

<img src="filtrar-por-geracao.gif" alt="Botão para filtrar pelas gerações">

## 5. Protótipos e layout final

Utilizamos a ferramenta Figma para produzir os protótipos. Inicialmente a exibição dos cards era feita em apenas um grande carrossel na interface, porém, optamos por exibi-los listados na página para favorecer a usabilidade da aplicação. 

### Protótipo inicial de baixa fidelidade:

<img src="protótipo-1.png" alt="Protótipo inicial de baixa fidelidade">

### Segundo protótipo de baixa fidelidade:

<img src="prototipo-2.png" alt="Segundo protótipo de baixa fidelidade">

### Protótipo dos cards:

<img src="prototipo-card.png" alt="Protótipo dos cards">

### Resultado final dos cards:

<img src="resultadofinal-card.png" alt="Cards finais">

### Aplicação para desktop:

<img src="versao-desktop.png" alt="Versão desktop">

### Aplicação para tablet:

<img src="versao-tablet.png" alt="Versão tablet">

### Aplicação mobile:

<img src="versao-mobile.png" alt="Versão mobile">

## 6. Histórias de usuário

Nossa concepção inicial foi criar uma aplicação focada no público adulto com o objetivo de provocar uma sensação nostálgica ao usuário que já teve contato com o universo pokemon durante a infância/adolescência, portanto fizemos uso de uma estética mais clássica e nostálgica. Tal estética foi implementada nos cards fortemente inspirados nos cards antigos de pokemon lançados nas décadas de 90 e inicio dos anos 2000, além do uso de elementos "pixelados" na interface.

### 1. Primeira História de Usuário

Implementamos funcionalidades baseadas no usuário que precisa visualizar os pokemons mais fortes e adequados para suas batalhas. A partir disso selecionamos três atributos específicos dos Pokemons para serem exibidos na tela: o CP(combat power), as fraquezas (weaknesses) e as resistências(resistance). Portanto, desenvolvemos a funcionalidade de organizar o CP dos pokemons e exibi-los em ordem crescente ou decrescente de acordo com o desejo do usuário, além de fornecer a possibilidade de filtrar os pokemons pelo tipo.

### 2. Segunda História de Usuário

Implementamos funcionalidades baseadas no usuário que deseja visualizar os pokemons de um modo mais informativo e padrão, portanto o usuário pode optar por visualizar os cards em ordem númerica ou alfabética. Para complementar a essa história, desenvolvemos um pequeno carrossel (slider) no topo da tela que exibe os pokemons de acordo com as gerações presentes no Pokemon Go.

### 3. Terceira História de Usuário

Implementamos como cálculo agregado obrigatório a aplicação, a exibição da porcentagem de pokemons de determinado tipo selecionado pelo usuário. Assim, exibimos uma das informações mais relevantes ao usuário baseada no desenvolvimento das histórias anteriores.

## 7. Testes de Usabilidade

Realizamos um rápido teste de usabilidade com três usuários e constatamos que:

- Os botões laterais estavam pequenos, o que dificulta a leitura das funcionalidades pelo usuário, logo a dashboard precisa ser mais larga e possuir os botões centralizados.

- O carrosel com os pokemons filtrados por geração deveria ter uma posição mais centralizada na interface.

- O exagerado espaço livre causou incômodo em alguns dos usuários.

- É necessário implementar algo (uma animação ou funcionalidade) na pokebola decorativa localizada ao lado da dashboard.

Por fim, algumas dessas constatações já foram implementadas e outras estão sendo planejadas para serem desenvolvidas em updates futuros.

## 8. Checklist

- [x] Usar VanillaJS.
- [x] Não utilizar `this`.
- [x] Passa pelo linter (`npm run pretest`)
- [x] Passa pelos testes (`npm test`)
- [x] Testes unitários cobrem um mínimo de 70% de statements, functions, lines e branches.
- [x] Inclui uma _definição de produto_ clara e informativa no `README.md`.
- [x] Inclui histórias de usuário no `README.md`.
- [x] Inclui rascunho da solução (protótipo de baixa fidelidade) no `README.md`.
- [x] Inclui uma lista de problemas detectados nos testes de usabilidade no `README.md`.
- [x] UI: Mostra lista/tabela/etc com dados e/ou indicadores.
- [x] UI: Permite ordenar dados por um ou mais campos (asc e desc).
- [x] UI: Permite filtrar dados com base em uma condição.
- [x] UI: É _responsivo_.
