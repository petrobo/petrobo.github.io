---
layout: dev
title: Eletrônica
special: [subrobof]
---

A parte eletrônica foi baseada na plataforma [Arduino](http://arduino.cc/), devido a sua facilidade de uso, ao extenso suporte de sua comunidade e as suas possibilidades de expansão. Uma visão geral é mostrada no digrama em blocos abaixo.

<center><img src="/assets/img/dev/robof/DiagramaEletronico.png" alt="" height="550"></center>


## Placas de circuito impresso

O projeto Robô F é composto por cinco placas de circuito impresso:

- **Robô F:** é a placa principal, responsável por ler os sensores, comandar os motores e receber e executar comandos.
- **Ponte H:** ou driver dos motores, é a placa que faz a interface entre o microcontrolador (baixa potência) e os motores (alta potência), além de ser capaz de inverter o sentido de rotação dos motores.
- **Sensor de linha:** contém cinco pares de emissores e receptores infravermelhos que, quando posicionados paralelo ao chão, são capazes de detectar diferentes o grau de reflexão do chão. Usualmente é utilizada para detectar uma linha preta em um chão branco.
- **Encoder:** placa contendo duas chaves ópticas, projetada para ser encaixada entre as engrenagens da caixa de redução e medir a velocidade das rodas. No entanto, devem ser feitos furos nas engrenagens.
- **Radio base:** é responsável pela comunicação, via rádio, do robô com o PC e não faz parte do robô.

<center><img src="/assets/img/dev/robof/pciss.png" alt="" height="500"></center>

As placas foram desenvolvidas utilizando o software [Eagle](http://www.cadsoftusa.com/). Todos os arquivos, assim como os diagramas esquemáticos em pdf, estão disponíveis na página de [Downloads](https://github.com/anderson-/JIFI/wiki/Downloads).

## Mapeamento dos pinos

Arduino Uno/Duemilanove  | Robô F
:----------------------: | :-----:
D0                       | RX
D1                       | TX
D2                       | ENCODER MOTOR A
D3#                      | ENCODER MOTOR B
D4                       | DEMUX SEL A
D5#                      | MOTOR A1
D6#                      | MOTOR A2
D7                       | RADIO CE
D8                       | RADIO CSN
D9#                      | MOTOR B1
D10#                     | MOTOR B2
D11#                     | MOSI
D12                      | MISO
D13                      | SCK
A0                       | DEMUX IN/OUT
A1                       | DEMUX SEL B
A2                       | DEMUX SEL C
A3                       | SENS. DISTÂNCIA
A4                       | SDA
A5                       | SCL
