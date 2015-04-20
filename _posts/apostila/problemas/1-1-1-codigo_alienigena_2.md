---
layout: exercicios
title: Código Alienígena 2
special: [problemas]
---

##Material
(Robô F; barreiras de papelão ou qualquer outro objeto sólido; trena)

Você está em uma expedição arqueológica em marte no ano de 2044 e seu grupo acaba de encontrar vestígios de uma civilização alienígena pré-histórica. Após vários estudos, foi descoberto que certos padrões alienígenas podem ser decodificados para a linguagem humana. Será possível? O que será que esse padrões podem nos informar? Um aviso de perigo? Vamos descobrir!

##Enunciado
Um dos vestígios encontrados na expedição parece com uma engrenagem. Esta engrenagem é uma mensagem alienígena à ser decodificada. Sabendo que cada seção ("dente da engrenagem") deve ser convertida para uma letra da linguagem humana, decodifique a mensagem de acordo com as regras abaixo:

-	A mensagem deve ser lida no sentido horário.
-	As distâncias estão em centímetros.
-	Letra "P":  Se a distância medida for > 40cm e < 60cm.
-	Letra "S":  Se a distância medida for > 60cm e < 70cm.
-	Letra "C":  Se a distância medida for > 70cm e < 90cm.
-	Letra "M":  Se a distância medida for > 90cm e < 100cm.
-	Letra "R":  Se a distância medida for > 100cm e < 120cm.
-	Letra "I":  Se a distância medida for > 120cm e < 130cm.
-	Letra "O":  Se a distância medida for > 130cm.

##Procedimento
Primeiramente, no ambiente de simulação desenhe as paredes ("dentes da engrenagem"). Logo depois inicie um procedimento no ambiente de programação, que enquanto o robô gira em torno de seu próprio eixo fique medindo as distâncias em relação aos dentes da engrenagem. Juntamente, utilize de condicionais para verificar qual letra a distância medida corresponde e então imprima a mensagem na tela.

##Conhecimentos envolvidos
Variáveis, condicionais aninhados, laços de repetição, sensores

<center>
<img src="/assets/img/exercicios/codigo_alienigena_2.png">
</center>
