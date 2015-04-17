---
layout: exercicios
title: Jogos olímpicos
tagline: 
tags: [intermediario, real, geometria]
special: [problemas]
use_math: true
deficuldade: 2
tempo: 25
mapa: ""
virtual: true
---

Você foi selecionado para as Olimpíadas Mundiais de Róbotica na modalidade "dança sincronizada". Você deverá programar o seu robô de forma que ele execute a tarefa pedida e assim deixar o seu país orgulhoso com o ouro.

##Enunciado
A dança sincronizada consiste basicamente em receber do usuário um número N, que deverá ser representado numa variável no seu programa. O programa deverá mandar o robô andar descrevendo um polígono regular (que tem todos os lados iguais) com o número de lados igual a N. O seu robô não poderá passar da velocidade 80 pois se não ele será desclassificado. O seu robô deve andar dois segundos em cada lado do polígono. Caso N seja menor que dois, seu programa não deverá fazer nada.

##Procedimento
Para saber em quantos graus o robô deverá virar a cada 2 segundos, deve-se utilizar a fórmula que calcula o ângulo interno de um polígono regular.

$$ AnguloInterno=((N-2)×180°)/N $$

Com o robô virando com esse ângulo calculado, ele irá descrever o polígono desejado.
