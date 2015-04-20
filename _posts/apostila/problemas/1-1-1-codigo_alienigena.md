---
layout: exercicios
title: Código Alienígena
special: [problemas] 
---

Durante a expedição arqueológica em Marte um artefato foi encontrado: uma placa branca com traços pretos. A placa possui uma mensagem oculta, você descobriu que cada letra do código é formada por linhas em alturas diferentes e que as cinco primeiras letras são relacionadas ao nosso alfabeto pela relação:


	a: 1 linha
	b: 2 linha 
	r: 3 linha
	c: 4 linha
	d: 5 linha

<p> </P>

##Enunciado
Ensine o robô a ler a mensagem usando o sensor de refletância.

##Procedimento
Para decodificar a primeira letra da palavra faça o robô percorrer cada linha de código até encontrar um traço preto. Quando encontrá-lo, associe o valor descoberto da linha com a letra e parta para a letra seguinte, iniciando a procura novamente pela primeira linha.

Será necessário criar uma variável com o tamanho total da palavra e outra para linha em que o robô se encontra, incrementando-a a cada vez que o robô avança uma linha e atribuindo 1 a essa variável sempre que o robô identificar uma letra e voltar para a posição inicial.

<center>
<img src="/assets/img/exercicios/codigo_alienigena.png">
</center>
