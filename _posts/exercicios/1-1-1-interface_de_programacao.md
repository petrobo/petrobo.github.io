#Interface de Programação do Robô F

##Definições Básicas
A linguagem de programação visual é composta de:

1. Comandos disponíveis na API de programação dos robôs (ver abaixo)

2. Bloco de comandos sequenciais;

3. Loop: assumir que para o módulo 1 só existe while

4. Função com argumentos;

5. Variáveis sem tipificação;

6. Variáveis vetoriais;

7. Operadores

    1. Aritméticos básicos (4 operações)

    2. Relacionais (maior, menor, maior ou igual, menor ou igual, diferente).

    3. Lógicos (and, or).

##Comandos da API do Robô F

|---|---|---|---|
|move|wait|rotate|var|
|read|print|if...else|while|

###move
```
move(r1, r2);
```

Move o robô, sendo r1 e r2 a roda esquerda e direita respectivamente. Cada roda recebe um valor inteiro de velocidade relativa, sendo 0 a roda parada, 100 a velocidade máxima para  frente e  -100 a velocidade máxima para trás do motor.

Exemplo:

```
move (100, 100); 
```

Move o robô em linha reta para frente com velocidade máxima.

![](comando_move.png)

###wait
```
wait ( t );
```
wait ( t ) serve para controlar o tempo de um comando. O tempo é regulado pelo parâmetro inteiro t, e é medido em milissegundos.

Exemplo

```
move (100, 100);
wait (1000);
move (0, 0);
```

Faz o robô acionar os motores em velocidade máxima para frente por 1 segundo e depois parar.

###rotate
```
rotate ( a );
```

Rotaciona o robô em torno de seu próprio eixo ao fazer as rodas girarem em sentidos opostos na mesma velocidade. Recebe o parâmetro angular inteiro a (-360 a 360). Valores positivos rotacionam o robô no sentido horário e valores negativos rotacionam o robô no sentido anti-horário.

Exemplo

```
rotate (90);
```

Rotaciona o robô 90º no sentido horário.

![](comando_rotate.png)

###var
```
var <nome>;
```

Cria uma variável , ou seja, reserva um espaço de memória para guardar uma variável de qualquer tipo (números inteiros, reais, caracteres, etc.). O comando também aceita vetores de tamanho variável.

Exemplo
```
var x = 0;
```

Cria uma variável de nome x e atribui o valor zero a ela.

```
var v;
v = [10,20];
```

Cria um vetor com 2 posições preenchidas com 10 e 20.

![](comando_var.png)

###read

```
read ( Device, var );
```

Comando usado para guardar  valor de uma variável lida pelo sensor. Recebe um parâmetro Device, que é um dos dispositivos do robô (bússola, sensor de distância e sensores de refletância) e guarda o valor recebido na variável var.

Exemplo

```
var y;
read (Bussola, y);
```

Cria uma variável y e guarda o valor lido da bússola em y, no caso um número inteiro representando um ângulo (0 a 359º).

![](comando_read.png)

###print
```
print ( <formato>, [var1, ..., varN] )
```

Exibe uma mensagem na tela. O formato é delimitado por aspas duplas (“”) e pode conter a expressão %v, que será substituída pela variável fornecida como parâmetro.

Exemplo

```
var x = 5;
print (“O valor de x é: %x”, x);
```

Exibe a mensagem: “O valor de x é: 5”.

![](comando_print.png)

###if...else

```
if (condição ) { ... } else { ... }
```

O comando if (Se),serve para fazer um caminho alternativo . Irá executar um bloco de comandos apenas se determinada condição for satisfeita. O comando else (Senão) executa um bloco caso a condição não seja satisfeita

Exemplo

```
if (x >= 120)
{
x = 0;
}
else
{ 
x = x + 10;
}
```

O valor da variável x será zerado se a variável apresentar um valor maior ou igual a 120. Caso contrário a variável é incrementada em 10 unidades.

![](comando_if_else.png)

###while

```
while ( condição )
```
Comando de loop de repetição. Irá executar um bloco de comandos enquanto uma determinada condição for satisfeita.

Exemplo

```
while (x < 120)
{
x = x + 10;
}
```

Enquanto o valor da variável x é menor que 120 a variável tem seu valor incrementado em 10 unidades.

![](comando_while.png)

##Exemplo de Utilização da Interface

Pequeno texto tutorial de como usar o programa

IMAGENS COM LEGENDA DOS BOTOES E DESCIRÇÃO DE SUAS FUNÇÕES

