# VivaMemory 

Desafio para aplicantes a vaga de pessoa desenvolvedora frontend nível Júnior.

<img src="/readme/tela-nivel-dificil.png">

## Tabela de conteúdos

  * [:warning: Instruções para entrega do projeto](#-warning--instruções-para-entrega-do-projeto)
  * [Sobre o Viva Decora:](#sobre-o-viva-decora-)
  * [Sobre o projeto: VivaMemory](#sobre-o-projeto--vivamemory)
  * [VivaMemory: Requisitos do MVP.](#vivamemory--requisitos-do-mvp)
  * [Funcionamento do jogo](#funcionamento-do-jogo)
    + [Logo do jogo](#logo-do-jogo)
    + [Tabuleiro e cartas](#tabuleiro-e-cartas)
    + [Contador de movimentos](#contador-de-movimentos)
    + [Botão de recomeçar](#bot-o-de-recomeçar)
    + [Indicador de nível](#indicador-de-nível)
    + [Escolher carta inicial](#escolher-carta-inicial)
    + [Escolher carta equivalente](#escolher-carta-equivalente)
    + [Recomeçar o jogo](#recomeçar-o-jogo)
  * [Tela inicial](#tela-inicial)
  * [Jogo Nível Fácil](#jogo-nível-fácil)
  * [Jogo Nível Normal](#jogo-nível-normal)
  * [Jogo Nível Difícil](#jogo-nível-difícil)
  * [Tela de Parabéns](#tela-de-parabéns)
  * [Assets e emojis](#assets-e-emojis)
  * [Critérios de avaliação](#critérios-de-avaliação)


## :warning: Instruções para entrega do projeto 

* Desenvolva e versione esse projeto usando git.
* Utilize o serviço de hospedagem de código de sua preferência: GitHub, Bitbucket, Gitlab ou outro.
* **Não faça um fork desse projeto.** Projetos forkeados sofrerão penalização na classificação.
* Crie um README com instruções claras sobre como executar seu projeto.
* Envie um email com o link para seu código para "jose.maciel [arroba] vivadecora.com.br "
* Dúvidas sobre esse projeto podem ser perguntadas nas [issues](https://github.com/vivadecora/desafio-frontend-jr/issues)

## Sobre o Viva Decora:

O Viva Decora é uma empresa fundada em 2014, partiu da necessidade de completar o ciclo do consumidor de móveis online.

O Viva Decora iniciou as atividades com o apoio da estrutura de back-office do VivaReal e depois ganhou equipes independentes de marketing B2B e B2C, operações, produto e engenharia, atualmente com 30 profissionais.  

Nossa plataforma de arquitetura e decoração online é voltada para ajudar os usuários a criar e comprar móveis e objetos para ambientes, baseado em recomendações e inspirações de diferentes arquitetos e designers. Temos mais de 5 milhões de visitas por mês  em nosso site e aplicativos e mais de 3 mil profissionais cadastrados. 

O Viva Decora quer ajudar o consumidor em três fases distintas: inspiração, informação e compra. 

**Em Dezembro de 2017 recebemos investimento do Grupo Duratex, para expandir nossas operações e nos consolidarmos como o maior marketplace de Decoração do Brasil**.

**Em Maio de 2019 a Viva Decora lançou seu marketplace de decoração e reforma com mais de 2 mil categorias diferentes de produtos.**

## Sobre o projeto: VivaMemory

Dia desses em uma videoconferência com pessoas de vários times diferentes, o Teles surgiu com o seguinte assunto.

> Temos alguns papais e mamães aqui, não seria legal criar um joguinho para nossas filhas e filhos? É um jeito a mais de interagirmos com eles nesses dias de home office.

O Adriano, que é papai, respondeu: 

> Acho que poderia ser bem legal, acho que podemos começar criando um jogo da memória bem colorido.

E Teles respondeu:

> Legal! Podemos usar só emojis, tenho um sobrinho que adora emojis! Acho que da para fazer algo simples que funcione pra computadores e celulares.

Todos gostaram da ideia. Os requisitos do MVP "VivaMemory" foram definidos a seguir.

## VivaMemory: Requisitos do MVP.

<img src="/readme/mockup-android.png" width="250" align="left">

* Apenas código front-end será escrito para esse projeto: HTML5, CSS e JavaScript.
* Pré-processadores de CSS ou HTML podem ser usados à vontade.
* As telas do projeto não precisam de urls próprias.
* A utilização de bibliotecas JavaScript é opcional, fique livre para fazer o desafio em JavaScript puro, VueJS, React, Angular ou outra tecnologia a sua escolha.
* As telas devem ser responsivas;
* O desafio consiste em 5 telas: **"Tela inicial"**, **"Jogo Nível Fácil"**, **"Jogo Nível Normal"**, **"Jogo Nível Difícil"**, **" Tela de Parabéns"**.

## Funcionamento do jogo

O VivaMemory adota o funcionamento típico de um jogo da memória. As telas **"Jogo Nível Fácil"**, **"Jogo Nível Normal"**, **"Jogo Nível Difícil"** são compostas por:

* Logo do jogo
* Tabuleiro e cartas
* Contador de movimentos
* Botão de recomeçar
* Indicador de nível

O fundo de todas as telas é um:

> linear-gradient(-45deg, ![#ff1c1c](https://placehold.it/15/ff1c1c/000000?text=+)#ff1c1c, ![#ff5656](https://placehold.it/15/ff5656/000000?text=+ )#ff5656);

### Logo do jogo
Logo do jogo é o único asset presente nesse desafio, para baixá-lo visite a sessão **Assets e emojis**.
Ele sempre deve ficar centralizado horizontalmente.

### Tabuleiro e cartas
O tabuleiro está sempre centralizado verticalmente e horizontalmente. Sua altura e largura não mudam independentemente do nível de dificuldade escolhido.

Os tamanhos das cartas devem variar de acordo com o nível de dificuldade selecionado.

O fundo de toda carta coberta é cinza ![#d8d8d8](https://placehold.it/15/d8d8d8/000000?text=+).

A utilização de padrão no *background* das cartas cobertas é opcional, mas se você desejar fazê-lo pode adicionar o seguinte CSS no elemento de cada carta:

```CSS
background: linear-gradient(135deg, #eceddc 25%, transparent 25%),
    linear-gradient(225deg, #eceddc 25%, transparent 25%),
    linear-gradient(315deg, #eceddc 25%, transparent 25%),
    linear-gradient(45deg, #eceddc 25%, transparent 25%); 
background-size: 30px 30px;
```

Cada novo jogo deve conter cartas com emojis aleatórios. 
Toda carta deve ter um par equivalente para que o jogo seja válido.

### Contador de movimentos

O contador de movimentos registra e exibe a quantidade de movimentos feitos no jogo.
É importante que singular e plural sejam respeitados no jogo, assim:

* 0 movimentos 
* 1 movimento
* 2 movimentos
* ...
* `N` movimentos

### Botão de recomeçar 

Um emoji que funciona como botão. Ao clicar nesse botão o jogo é reiniciado.

### Indicador de nível

Um texto abaixo do tabuleiro indicando o nível de dificuldade atual. As cores do texto mudam dependendo do nível escolhido:

* Fácil ![#00b335](https://placehold.it/15/00b335/000000?text=+)
* Normal ![#333](https://placehold.it/15/333/000000?text=+)
* Difícil ![#ff424e](https://placehold.it/15/ff424e/000000?text=+)

As ações que podem ser executadas nessas telas são:

* Escolher carta inicial
* Escolher carta equivalente
* Recomeçar o jogo


## Escolher carta inicial

O jogador inicia um movimento ao selecionar uma carta qualquer não revelada.
Ao clicar em cima da carta, o emoji escondido nela é revelado e o fundo da carta fica na cor azul ![#00b1f4](https://placehold.it/15/00b1f4/000000?text=+).

![Carta inicial](/readme/carta-inicial.png)

## Escolher carta equivalente

Após escolher a carta inicial e ver seu emoji o jogador deve escolher a outra carta do tabuleiro com o mesmo emoji.
Assim, o jogador clica em outra carta.

Se a carta equivalente estiver correta, ambas cartas selecionadas no movimento ficam com os emojis revelados por todo o resto do jogo e com o fundo na cor verde ![#00b335](https://placehold.it/15/00b335/000000?text=+)

![Carta equivalente correta](/readme/carta-equivalente-correta.png)

Se a carta equivalente for diferente, ambas as cartas selecionadas no movimento ficam com cor de fundo vermelho ![#ff424e](https://placehold.it/15/ff424e/000000?text=+) durante 2 segundos. Em seguidas ambas as cartas são cobertas, isto é, seus emojis deixam de aparecer e voltam a sua cor de fundo original.

![Carta equivalente incorreta](/readme/carta-equivalente-incorreta.png)
  
Em ambos os casos, após escolher a carta equivalente o contador de movimentos conta um movimento a mais.
O jogo prossegue até que todas as cartas tenham sido reveladas.
  
## Recomeçar o jogo

Ao clicar no botão de reiniciar o jogo as seguintes ações ocorrem:

* Todas as cartas são cobertas
* As cartas do tabuleiro são sorteadas novamente
* O contador de movimentos é zerado

O emoji usado para essa função é o 🔄

## Tela inicial

![Tela inicial](/readme/tela-inicial.png)

A tela inicial apresenta 3 botões com os textos:
* 👶 Fácil
* 👦 Normal
* 🤯 Difícil

Ao clicar em um dos botões é revelada a tela do nível correspondente. As características das telas são exibidas a seguir:

## Jogo Nível Fácil

O jogo no nível fácil, segue as regras explicadas em "Funcionamento do jogo".
O tabuleiro nesse nível de jogo contém:

* Duas colunas
* Duas linhas
* Quatro cartas
* Cada carta tem pelo menos 90px de largura/altura

![Tela nível fácil](/readme/tela-nivel-facil.png)

A imagem acima deve ser usada como referência para o design da tela.

## Jogo Nível Normal

O jogo no nível normal, segue as regras explicadas em "Funcionamento do jogo".
O tabuleiro nesse nível de jogo contém:

* Duas colunas
* Duas linhas
* Oito cartas
* Cada carta tem pelo menos 60px de largura/altura

![Tela nível normal](/readme/tela-nivel-normal.png)

A imagem acima deve ser usada como referência para o design da tela.

## Jogo Nível Difícil

O jogo no nível difícil, segue as regras explicadas em "Funcionamento do jogo".
O tabuleiro nesse nível de jogo contém:

* Quatro colunas
* Quatro linhas
* Dezesseis cartas
* Cada carta tem pelo menos 30px de largura/altura

![Tela nível difícil](/readme/tela-nivel-dificil.png)

A imagem acima deve ser usada como referência para o design da tela.

## Tela de Parabéns

A Tela de Parabéns consiste de:

* Um emoji ✅ em tamanho grande
* Logo do jogo
* Texto de parabéns
* Texto contendo a quantidade de movimentos necessárias para finalização do jogo
* Botão com texto "Jogar novamente"

Ao clicar no botao "Jogar novamente" um novo jogo é iniciado no mesmo nível do jogo que foi finalizado.

![Tela Parabéns](/readme/tela-parabens.png)

## Assets e emojis

Esse desafio possui um único asset, que é o [logo do jogo que pode ser baixado aqui](/assets/logo-vivamemory.svg).
  
Todas as outras imagens são proveninentes de emojis. Por ser um jogo voltado para crianças restringimos os emojis usados a uma lista específica logo abaixo. 

Outra vantagem dos emojis é que eles irão aparecer em cada dispositivo já com o estilo do dispositivo e por isso provavelmente podem ser imagens mais familiares.

Essa lista contém os emojis que consideramos mais atrativos e os códigos decimais e hexadecimais para usá-los no HTML.
**Exemplo:** Se você desejar imprimir um &#128063; pode usar no html  `&#128063;` ou `&#1F43F;`.

| Emoji        | Decimal           | Hexadecimal  |
| ------------- |:-------------:| -----:|
|⏰| 9200| 23F0|
| ⚡   |9889 |26A1 |
| ⚽ |9917 |26BD |
| ⛄ |9924 |26C4 |
| ⭐ |11088  |2B50 |
| 🌚 |127770 |1F31A |
| 🌞 |127774 |1F31E |
| 🌟 |127775 |1F31F |
| 🌵 |127797 |1F335 |
| 🌸 |127800 |1F338 |
| 🌼 |127804 |1F33C |
| 🍉 |127817 |1F349 |
| 🍍 |127821 |1F34D |
| 🍌 |127820 |1F34C |
| 🍒 |127826 |1F352 |
| 🍞 |127838 |1F35E |
| 🍦 |127846 |1F366 |
| 🍬 |127852 |1F36C |
| 🍫 |127851 |1F36B |
| 🍼 |127868 |1F37C |
| 🎃 |127875 |1F383 |
| 🎅 |127877 |1F385 |
| 🎈 |127880 |1F388 |
| 🎉 |127881 |1F389 |
| 🎒 |127890 |1F392 |
| 🎹 |127929 |1F3B9 |
| 🏀 |127936 |1F3C0 |
| 🏐 |127952 |1F3D0 |
| 🏠 |127968 |1F3E0 |
| 🐁 |128001 |1F401 |
| 🐈 |128008 |1F408 |
| 🐒 |128018 |1F412 |
| 🐊 |128010 |1F40A |
| 🐖 |128022 |1F416 |
| 🐛 |128027 |1F41B |
| 🐜 |128028 |1F41C |
| 🐝 |128029 |1F41D |
| 🐧 |128039 |1F427 |
| 🐷 |128055 |1F437 |
| 🐸 |128056 |1F438 |
| 🐻 |128059 |1F43B |
| 🐿 |128063 |1F43F |
| 👻 |128123 |1F47B |
| 💚 |128154 |1F49A |
| 💙 |128153 |1F499 |
| 💜 |128156 |1F49C |
| 🔥 |128293 |1F525 |
| 😀 |128512 |1F600 |
| 😎 |128526 |1F60E |
| 🚀 |128640 |1F680 |
| 🚗 |128663 |1F697 |
| 🚲 |128690 |1F6B2 |
| 🤖 |129302 |1F916 |
| 🥕 |129365 |1F955 |
| 🥦 |129382 |1F966 |
| 🦁 |129409 |1F981 |
| 🦋 |129419 |1F98B |
| 🧙 |129497 |1F9D9 |
| 🦖 |129430 |1F996 |
| 🦄 |129412 |1F984 |

## Critérios de avaliação

* Fidelidade ao layout solicitado;
* Fidelidade às funcionalidades solicitadas;
* Criação de componentes;
* Clareza de nomenclatura do CSS;
* HTML estruturado de forma semântica;
* Adesão ao mobile first.
