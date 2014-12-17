---
layout: wiki
title: Problemas Difíceis
tagline: por Anderson Antunes
tags: [exercicio, dificil]
---

#Problemas Difíceis

##Desenho pela Trajetória
**Objetivo:** Aprender os comandos básicos do robô e o uso de funções

**Conhecimentos envolvidos:** ângulos (matemática)

**Enunciado:** Mova o robô fazendo que sua trajetória forme uma pétala de flor parecida com a da figura abaixo

**Provocação:** Crie uma função com o código anterior e usando esta função faça o seguinte desenho.

![](desenho_pela_trajetoria.png)

##Robô Seguidor
**Objetivo:** aprender laços condicionais, laços infinitos, tomada de decisão, leitura de sensores.

**Conhecimentos envolvidos:** lógica

**Enunciado:** O RobôF deve encontrar o objeto mais próximo no seu entorno e, ao encontrá-lo, se posicionar de frente ao objeto ajustando sua distância para 30cm. Você deve dar uma margem de erro de 2 cm, ou seja, um valor entre 28 e 32cm é aceitável. Tal margem de erro serve para corrigir a imprecisão do sensor. Você deve verificar se, após parar, a distância é a desejada e, caso contrário, calibrá-la. Após ter se posicionado, o objeto pode ser movido (apenas para frente e para trás) e o RobôF deverá manter a mesma distância de 30 cm do objeto.

**Provocação:** faça o robô conhecer o ambiente ao redor e tomar decisões.

![](robo_seguidor_1.png)

![](robo_seguidor_2.png)

##Gato e Rato
**Objetivo:** aprender as dificuldades de iteração em tempo real, loops.

**Conhecimentos envolvidos:** operações com ângulos, busca.

**Enunciado:** esse problema consiste em uma perseguição entre dois robôs, o gato perseguindo o rato. O rato é mais devagar que o gato, por isso está sempre mudando a sua trajetória para despistar o gato. O gato, apesar de ser mais rápido, tem dificuldades em fazer curvas e é facilmente despistado pelo rato. Por isso, a cada mudança de direção do rato ele tem que parar e buscar em que direção ele foi. O seu papel é programar o gato.

![](gato_e_rato.png)

##Robô Motorista
**Objetivo:** aprender laços condicionais e laços de número fixo

**Conhecimentos envolvidos:**  lógica e leis de trânsito

**Enunciado:** Imagine a figura a seguir como uma cidade, os quadrados verdes são as quadras (casas). O robô faria o percurso desenhado pela linha amarela repetidamente, variando as direções em que escolhe em cada cruzamento. Quando chegasse ao cruzamento central deve parar por um instante na “faixa de pedestres” representada por 2 linhas pretas paralelas(cor preta indica quando o robô deve parar) e só poderia andar novamente quando não detectasse nenhum pedestre a sua frente(provavelmente algum objeto colocado na faixa). 

**Provocação:** Esse problema poderia tornar-se mais desafiador ao introduzir mais  robôs na “cidade” fazendo o percurso em amarelo e seguindo as mesmas regras citadas anteriormente, porém agora além de cuidar com os pedestres o robô deve dar a preferência nos cruzamentos  ao robô que vai virar a direita e manter uma distância mínima do robô que segue a sua frente.

![](robo_motorista.png)

###Lógica utilizada
Este problema possivelmente envolve todos os sensores do robô e exige que seja dividida em problemas menores mais fácies de resolver. Por exemplo: inicialmente faz-se o robô seguir a linha amarela e parar nas linhas pretas utilizando os sensores de refletância e **lógica condicional** (IF), separadamente cria-se uma lógica para fazer o robô parar caso algum objeto esteja a uma distância mínima dele. Em seguida combinar esses dois procedimentos dentro de um **laço de repetição**  para que ele fique percorrendo a cidade. Futuramente se o robô for capaz de medir a distância percorrida e juntando essa informação com a orientação da bússola é possível montar um mapa na interface de programação com o percurso a ser seguido e predeterminar a rotina do robô, este só a alteraria caso surgisse algum pedestre ou outro robô a sua frente.

##Aplicação Eletrônica 5
**Objetivo:** trabalhar com variações de luminosidade

**Conhecimentos envolvidos:** funcionamento de LDR, lógica condicional, acionamento de LEDs

**Enunciado:** Equipe cada robô que trafega na cidade com um par de LEDs de alto brilho na parte traseira (lanternas traseiras) e um LDR na parte dianteira, dessa forma o robô que seguir o percurso atrás de outro deve manter uma distância em relação ao robô da frente baseado em certo nível de luminosidade. Por exemplo: se a luminosidade detectada pelo LDR for muito alta isso significa que o robô a sua frente está muito próximo e então é preciso reduzir a velocidade para evitar uma batida. 

