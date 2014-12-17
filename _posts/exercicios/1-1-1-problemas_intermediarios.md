---
layout: alunos
title: Problemas Intermediários
tagline: por Anderson Antunes
tags: [exercicio, dificil]
---

#Problemas Intermediários

##Código Alienígena

**Objetivo:** Utilizar arrays e sensor de refletância.

**Conhecimentos envolvidos:** Váriaveis, arrays, condicionais aninhadas, laços de repetição

**Enunciado:**
Durante a expedição arqueológica em marte outro artefato foi encontrado: Uma placa branca com traços pretos. A placa possui uma mensagem oculta, você descobriu que cada letra do código é formada por linhas em alturas diferentes e que as cinco primeiras letras são relacionadas ao nosso alfabeto pela relação:

|---|---|
|a|1ª linha|
|b|2ª linha|
|r|3ª linha|
|c|4ª linha|
|d|5ª linha|

Ensine o robô a ler a mensagem usando os sensores de refletância.

![](codigo_alienigena.png)

##Codigo Alienígena 2
**Objetivo:** Utilizar sensor de distância.

**Conhecimentos envolvidos:** Variáveis, condicionais aninhados, laços de repetição, sensores

**Enunciado:**
Você está em uma expedição arqueológica em marte no ano de 2044 e seu grupo acaba de encontrar vestígios de uma civilização alienígena pré histórica. Um dos artefatos parece uma mensagem codificada com o formato de uma engrenagem. Estudos foram feitos e descobriu-se que cada seção ("dente da engrenagem") representa uma letra, onde a  distancia do centro até a borda as tornam diferentes, e que o artefato deve der lido em sentido horário. Decodifique a mensagem por meio do código das regras abaixo:

|---|---|
|o | > 130|
|i | > 120|
|r | > 100|
|m | > 90|
|c | > 70|
|s | > 60|
|p | > 40|

(as distancias estão em cm)

![](codigo_alienigena_2.png)

##Ajudante de Bombeiro
**Objetivo:** Movimentos complexos

**Conhecimentos envolvidos:** Variáveis (flags), laços de repetição

**Enunciado:**
No caso de incendios é comum que as pessoas tenham pouca visibilidade por causa da fumaça e se percam em locais que não conheçam. Seu robô possui uma lanterna e vai ajudar as pessoas a saírem do prédio com segurança, mas * **antes deve encontra-las** *. Ensine o robô a chegar ao fim do caminho proposto onde estão as vitimas, lembrando que ele não conhece o terreno.

![](ajudante_de_bombeiro.png)

##Jogos Olímpicos
**Conhecimentos:**  Geometria básica, estruturas de repetição, estruturas condicionais.

**Enunciado:** Você foi selecionado para as Olimpíadas Mundiais de Róbotica na modalidade "dança sincronizada". Você deverá programar o seu robô de forma que ele execute a tarefa pedida e assim deixar o seu país orgulhoso com o ouro.

A dança sincronizada consiste basicamente em receber um número N, que deverá ser representado numa variável no seu programa, e mandar o robô andar descrevendo um polígono regular (que tem todos os lados iguais) com o número de lados igual a N. O seu robô não poderá passar da velocidade 80 pois senão ele será desclassificado. O seu robô deve andar dois segundos em cada lado do polígono. Caso N seja melhor que dois, seu programa não deverá fazer nada.

A sua equipe precisa de você para ganhar o ouro!

##Triângulo Equilátero
**Objetivo:** comandos avançar, recuar e ler bússola. Verificar se o aluno aprendeu a realizar uma sequência de comandos simples.

**Conhecimentos envolvidos:** geometria

**Enunciado:** Faça um programa que, ao receber um número inteiro a, faça o Robô F andar em um triângulo equilátero imaginário de a centímetros de aresta. Recordar-se que um triângulo equilátero possui ângulos internos de 60o. O robô começa a percorrer o triângulo imaginário na direção para a qual estiver apontando.

**Provocação:** o aluno pode, ao invés de repetir o código três vezes, criar um laço condicional para fazer as tarefas de girar 60º e percorrer a distância a.

![](triangulo_equilatero.png)

##Desenhar Polígonos Regulares
**Objetivo:** Aprender os comandos básicos do robô, o uso de funções e lógica de programação.

**Conhecimentos envolvidos:** ângulos (matemática), geometria

**Enunciado:** adapte o código usado para desenhar um triângulo equilátero para desenhar um quadrado. Depois use o código recém-criado para desenhar um pentágono. Depois um hexágono, ou seja, faça uma função que receba o número de lados que o polígono regular deve ter e desenhe a figura.

##Virando com ajuda
**Objetivo:** aprender funções, condicionais simples, loop, recursão simples.

**Conhecimentos envolvidos:** ângulos retos (matemática)

**Enunciado:** Faça uma função virando que recebe como argumento um inteiro virar. Se virar == 1, o robô vira 90 graus a direita, se virar == 2, o robô anda 10 cm, vira 90 graus a direita, anda 10 cm, vira 90 graus a direita, e depois anda mais 10 cm e vira 90 graus a direita.

**Provocação:** chame a própria função com virar == 1 dentro de um loop para fazer as conversões à direita no segundo caso.

##Barreiras Ortogonais
**Objetivo:** aprender laços condicionais e laços de número fixo

**Conhecimentos envolvidos:** ângulos retos (matemática)

**Enunciado:** o RobôF deve sair da origem (ponto circular), avançar em direção às barreiras (se aproximar o máximo possível - 20 cm) na sequência indicada na figura e parar a frente da última das barreiras.

**Provocação:** caso o programa que fez tenha mais que 8 linhas, tente reduzi-la para o mínimo que conseguir.

#Não consegui copiar uma imagem!!!

##Aplicação de eletrônica
Implementar a mesma aplicação eletrônica do problema “Saia da minha frente”

##Acelerando e Reduzindo
**Objetivo:** aprender laços de repetição, contadores, comando avançar e recuar.

**Conhecimentos envolvidos:** lógica

**Enunciado:** Faça um programa no qual dado um i, que inicialmente é zero e vai até 255, acelere o robô usando este i como velocidade. Para cada i o robô deve andar por 10 ms. Depois de alcançar 255 o i deve decrescer novamente até zero fazendo com que o robô desacelere. Repita a operação, mas desta vez ao invés de avançar o robô deve recuar.

**Comportamento:** Este algoritmo deve fazer com que o robô acelere gradualmente até o seu máximo e depois desacelere até zero. Depois o robô acelerará na marcha ré e depois desacelerará até zero.

![](acelerando_e_reduzindo.png)

**Provocação:** O problema é resolvido com no máximo 4 Whiles.

##Aplicação de Eletrônica
**Objetivo:** trabalhar com variações de frequência

**Conhecimentos envolvidos:** funcionamento de buzzer, sinais periódicos.

**Enunciado:** Utilize um buzzer para simular o “som do motor” do robô, variando a frequência do som emitido de acordo com a velocidade do motor, quando o motor estiver de vagar o som deve ser grave e conforme acelera o som torna-se mais agudo.

##Race Day
**Objetivo:** aprender laços condicionais infinitos, operadores lógicos, resolução de problemas práticos.

**Conhecimentos envolvidos:** conjuntos (matemática), lógica booleana.

**Enunciado:** o Robô F está treinando para uma competição de seguidores de linha. A competição é composta por três etapas, com três circuitos diferentes. O objetivo principal é dar duas voltas completas no circuito sem perder a linha. A primeira etapa é um circuito é um circuito oval simples. Na segunda etapa, o circuito contém uma pista interna em cada reta, similar a um pit-stop, e o robô deve passar pelo menos uma vez por uma delas. Na terceira, e última, etapa são adicionadas duas linhas no centro do circuito original, formando um oito “deitado”. Nessa etapa o robô deve passar pelo menos uma vez pelas linhas centrais e deve seguir reto no cruzamento.

|---|---|
| 1 | ![](race_day_1.png)|
| 2 | ![](race_day_2.png)|
| 3 | ![](race_day_3.png)|
