---
layout: dev
title: Documentação Superficial
special: [subv1]
---

## Estrutura de um fluxograma
O principal componente de armazenamento de dados do JIFI é o fluxograma. Cada programa criado no JIFI possui apenas a função principal, que é definida por uma classe própria. A ordem hierárquica dos elementos constituintes do fluxograma é mostrada na figura a baixo.

![](/assets/img/dev/jifi/v1/diagrama.png)

Todos os elementos herdam as propriedades da classe procedimento, blocos são definidos como um conjunto de elementos, tanto o elemento responsável pelo laço de repetição quanto o que representa a função principal são fundamentalmente similares aos blocos de comando. O elemento divisor do fluxo, o condicional, é composto por dois blocos distintos, um para cada valor booleano gerado ao avaliar a expressão.

A estrutura em que os comandos são organizados dentro do fluxograma define a forma que o interpretador irá executar o programa e quais suas possíveis limitações de desempenho e memória. O fluxograma é construído como um conjunto de comandos e blocos de comandos,  definidos como listas duplamente encadeadas. Cada comando possui a referencia do elemento anterior, posterior e o pai, que indica qual bloco contém o dado elemento.

![](/assets/img/dev/jifi/v1/lista.png)

No diagrama acima é apresentado o relacionamento entre os comandos A, B e C, respectivamente, na forma de uma lista duplamente encadeada, assim como encontrados dentro de um bloco de comandos, porém sem mostrar a referencia para o elemento pai, que neste caso seria o bloco formando por esses elementos. Foi escolhido uma lista duplamente encadeada como estrutura de dados padrão dos blocos pois permite que cada elemento acesse o elemento é anterior e posterior ao mesmo, útil ao desenhar o bloco. Utilizando essa estrutura os elementos podem ser acessados sequencialmente em um elemento de bloco ou uma função pode ser percorrida como uma árvore dependendo do contexto (desenho, verificação de variáveis declaradas, otimizações, etc.). 

![](/assets/img/dev/jifi/v1/função.png)

## Comandos
O funcionamento interno dos comandos utiliza um sistema de execução que necessita de duas funções para funcionar. `public void begin()` é responsável por inicializar o comando, em seguida `public boolean perform()` indica se o comando foi executado com sucesso, retornando `false` enquanto o comando estiver em execução, uma pausa de aproximadamente 5 ms é inserida entre as chamadas desta função até que a mesma retorne `true`, ou uma exceção seja lançada. Ambas as funções recebem recursos globais armazenados pelo interpretador, esses recursos permitem que cada comando possa ser autônomo durante sua execução, simplificando o interpretador e tornando o JIFI modular, com suporte a comandos intercambiáveis.

#### Bloco de comandos
O JIFI, durante a execução do código, utiliza escopo dinâmico, onde o final do bloco de comandos ou função, indica o fim da vida útil dos identificadores (variáveis) declarados dentro do mesmo. Essa técnica foi implementada adicionado-se um comando que marca o final da lista duplamente encadeada, este elemento tem o papel de reiniciar o escopo de nomes de variáveis.
![](/assets/img/dev/jifi/v1/bloco.png)

Este método permite a verificação de escopo de forma automática durante a execução, onde uma exceção é lançada caso um estado inválido seja identificado. Laços de repetição também se beneficiam dessa estrutura, que torna simples a construção dos mesmos, durante a chamada da função `public void begin()` o fluxo de execução é direcionado à sub-lista de acordo com o resultado da expressão booleana, e redirecionado ao comando de repetição pelo comando delimitador final.

O elemento condicional, como representado a baixo, é composto de dois blocos, verdadeiro e falso, e possui funcionamento análogo aos laços de repetição.

![](/assets/img/dev/jifi/v1/condicional.png)

## Interpretador
O interpretador da linguagem visual é responsável por executar cada comando no tempo apropriado e com os devidos recursos, de acordo com os parâmetros definidos. Também permite que os comados tenham acesso à cronômetros, conexões seriais, objetos simulados, entre outros. 

Como motor para executar expressões matemáticas e armazenar variáveis, o interpretador utiliza uma biblioteca externa chamada JEP (Java Expression Parser),  versão 2.4.1 GPL, que possui suporte à expressões logicas e aritméticas, cadeias de caracteres, vetores e pode otimizar determinados tipos de expressões. Assim o interpretador disponibiliza o parser para que os comandos possam resolver suas expressões e mantém um registro das variáveis declaras e seus valores.

## Parser
![](/assets/img/dev/jifi/v1/parser.png)

## Sistema de controle

O sistema de controle utilizado nos robôs simulados no JIFI ou utilizado em projetos baseados em Arduino (RobôF), foi projetado para permitir que múltiplas tarefas sejam realizadas de forma aparentemente simultânea, sem interromper a comunicação do sistema com outros periféricos durante o processamento dos comandos, ações ou ao atualizar os sensores. Isso foi realizado utilizando um escalonador, onde pequenas partes de diferentes processos sejam realizadas sequencialmente, passando a impressão de paralelismo.

## Componentes

Existem três tipos de componentes diferente que constituem o sistema de controle, cada um com uma função especifica: Dispositivos representam sensores e atuadores, ações executam algum algoritmo utilizando recursos do sistema de modo paralelo e as conexões são utilizadas para receber/enviar mensagens de controle/status para outros sistemas.

## Suporte a Arduino e a outros sistemas microcontrolados

O JIFI, apesar de possuir um simulador, foi desenvolvido para trabalhar com um robô real, baseado em Arduino, chamado Robô F. A comunicação é feita sem fio utilizando módulos [nrf24l01](http://blog.iteadstudio.com/wp-content/uploads/image/2010_05/nrf24l01-wireless-module-with-arduino_1.jpg), um que utiliza um Arduino para se comunicar com um computador e outro integrado ao robô.

A descrição técnica do protocolo encontra-se na página [Comunicação](https://github.com/anderson-/JIFI/wiki/Comunica%C3%A7%C3%A3o).

## Visão geral

![](/assets/img/dev/jifi/v1/oldsimulator.png)

## Próximos passos

A segunda versão do JIFI, ainda em desenvolvimento, é baseada em um novo Framework, o S3F, uma das principais características desse Framework é criação plugins em pacotes JAR facilmente acessíveis pelo programa principal e de módulos em JavaScript, escritos e interpretados em tempo de execução, tornado o JIFI uma ferramenta para desenvolvimento e simulação de sistemas genéricos, podendo ser utilizada em varias áreas e disciplinas acadêmicas.
