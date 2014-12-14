#Problemas Fáceis

##Avançar em metros
**Objetivo:** aprender funções, condicionais básicas.

**Conhecimentos envolvidos:** movimento retilíneo uniforme (Física)

**Enunciado:** Faça uma função chamada 'andar_metros', que recebe como argumento uma distancia, contendo a distância em metros que o robô irá percorrer. Considerando uma velocidade fixa de 0.1 m/s, calcule o tempo necessário, em segundos, de execução do comando avancar(v,t) para os valores de distancia.

**Provocação:** verifique através do sensor de distância se é possível andar a quantidade de metros armazenada em distancia.

##Aplicação eletrônica
**Objetivo:** Utilizar funções de movimento.

**Conhecimentos envolvidos:** Nenhum 

**Enunciado:** Você está desenvolvendo um robô que limpa o chão (como a imagem acima), o robô possui cerdas limpadoras e um aspirador de pó, ele deve andar pela casa e recolher o máximo de sujeira que encontrar. Como seu primeiro desafio nesse projeto ensine o robô a andar em zigue-zague:

![](aplicacao_eletronica.png)

##Aplicação eletrônica 2
**Objetivo:** aprender o funcionamento de um LED 

**Conhecimentos envolvidos:** corrente e tensão em um LED

**Enunciado:** adicione um LED vermelho e um verde no robô. Deixe o LED vermelho aceso enquanto o robô não estiver na posição final desejada. Quando o robô alcançar a posição final, apagar o LED vermelho e acender o LED verde.

##Aplicação eletrônica 3
**Objetivo:** aprender o funcionamento de um LED 

**Conhecimentos envolvidos:** corrente e tensão em um LED

**Enunciado:** Faça um indicador de distância usando três LEDs que varie de 10 em 10 centímetros.  Coloque três LEDs enfileirados. Quando o robô estiver a uma distância de 40 cm ou mais, acender um LED. Acender mais um LED a cada 10 cm aproximados do obstáculo.

* 3 LEDs: de 20 a 29 cm

* 2 LEDs: de 30 a 39 cm

* 1 LED: 40 cm ou mais

##Saia da Minha Frente
**Objetivo:** aprender laços infinitos, tomada de decisão, leitura de sensores e laços de repetição.

**Conhecimentos envolvidos:** lógica.

**Enunciado:** O Robô F deve executar os seguintes procedimentos: 

1. se o leitor de distância não detectou nenhum objeto, o robô anda em frente; 

2. se o leitor de distância detectou algo a menos de 40 cm, então o robô deve virar 90 graus e recomeçar o algoritmo do procedimento 1.

**Comportamento:** Este algoritmo deve fazer com que o robô ande pelo ambiente desviando de todos os obstáculos encontrados por ele.

![](saia_da_minha_frente.png)


