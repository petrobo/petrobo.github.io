---
layout: dev
title: Comunicação
special: [subrobof]
---

## Protocolo de comunicação

Foi elaborado um simples protocolo para a comunicação entre a interface de programação (JIFI) e o Robô F. O protocolo é baseado no modelo "mestre-escravo". A interface (mestre) faz requisições ao robô (escravo), que executa e responde.

### Comandos

O protocolo contém os seguintes comandos, representados pelos respectivos códigos.

| COMANDO   | CÓDIGO |
|-----------|:------:|
| STOP	    | 1      |
| ECHO	    | 2      |
| PRINT	    | 3      |
| GET	    | 4      |
| SET	    | 5      |
| ADD	    | 6      |
| RESET	    | 7      |
| DONE	    | 8      |
| NO_OP	    | 9      |
| ALL	    | 222    |
| FREE_RAM  | 223    |

### Formato das mensagens

Há dois formatos de mensagem, um para a comunicação mestre->escravo e outro para a comunicação escravo->mestre, conforme a figura abaixo.

<center><img src="/assets/img/dev/robof/Protoco_comunicacao.png" alt=""></center>

A tabela abaixo mostra o formato e tamanho das mensagens para cada tipo de comando.

<!-- ## Documentação das Classes do Software RobotLib

[http://petrobo.github.io/RobotLib/index.html](http://petrobo.github.io/RobotLib/index.html) -->

<style type="text/css">
table.tableizer-table {
border: 1px solid #CCC;
}
.tableizer-table td {
padding: 8px;
margin: 6px;
border: 1px solid #ccc;
}
.tableizer-table th {
padding: 8px;
background-color: #EEE;
}
</style>

<center>
<table class="tableizer-table">
<tr class="tableizer-firstrow"><th colspan="7">FORMATO DOS COMANDOS</th></tr>
 <tr><th rowspan="4">STOP</th><td rowspan="2">Recebe</td><td colspan="2" align="center">2</td><td>&nbsp;</td><td>&nbsp;</td></tr>
 <tr><td>STOP</td><td>id</td><td>&nbsp;</td><td>&nbsp;</td></tr>
 <tr><td rowspan="2">Envia</td><td colspan="3" align="center">3</td><td>&nbsp;</td></tr>
 <tr><td>DONE</td><td>STOP</td><td>id</td><td>&nbsp;</td></tr>
 <tr><th rowspan="4">ECHO</td><td rowspan="2">Recebe</td><td colspan="3" align="center">2+length</td><td>&nbsp;</td></tr>
 <tr><td>ECHO</td><td>length</td><td>msg</td><td>&nbsp;</td></tr>
 <tr><td rowspan="2">Envia</td><td align="center">length</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
 <tr><td>msg</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
 <tr><th rowspan="4">PRINT</td><td rowspan="2">Recebe</td><td colspan="4" align="center">3+length</td></tr>
 <tr><td>PRINT</td><td>id</td><td>length</td><td>msg</td></tr>
 <tr><td rowspan="2">Envia</td><td colspan="4" align="center">4</td></tr>
 <tr><td>DONE</td><td>PRINT</td><td>id</td><td>length</td></tr>
 <tr><th rowspan="6">GET</td><td rowspan="2">Recebe</td><td colspan="4" align="center">3+length</td></tr>
 <tr><td>GET</td><td>id</td><td>length</td><td>msg</td></tr>
 <tr><td rowspan="4">Envia</td><td colspan="4" align="center">3+sizeof(int)</td></tr>
 <tr><td>SET</td><td>FREE_RAM</td><td>sizeof(int)</td><td>free_ram</td></tr>
 <tr><td colspan="4" align="center">3+tmpLen</td></tr>
 <tr><td>SET</td><td>ALL</td><td>tmpLen</td><td>data</td></tr>
 <tr><th rowspan="4">SET</td><td rowspan="2">Recebe</td><td colspan="4" align="center">3+length</td></tr>
 <tr><td>SET</td><td>id</td><td>length</td><td>data</td></tr>
 <tr><td rowspan="2">Envia</td><td colspan="4" align="center">4</td></tr>
 <tr><td>DONE</td><td>SET</td><td>id</td><td>length</td></tr>
 <tr><th rowspan="4">ADD</td><td rowspan="2">Recebe</td><td colspan="4" align="center">3+length</td></tr>
 <tr><td>ADD</td><td>id</td><td>length</td><td>data</td></tr>
 <tr><td rowspan="2">Envia</td><td colspan="4" align="center">4</td></tr>
 <tr><td>DONE</td><td>ADD</td><td>id</td><td>length</td></tr>
 <tr><th rowspan="4">RESET</td><td rowspan="2">Recebe</td><td colspan="2" align="center">2</td><td>&nbsp;</td><td>&nbsp;</td></tr>
 <tr><td>RESET</td><td>id</td><td>&nbsp;</td><td>&nbsp;</td></tr>
 <tr><td rowspan="2">Envia</td><td colspan="3" align="center">3</td><td>&nbsp;</td></tr>
 <tr><td>DONE</td><td>RESET</td><td>id</td><td>&nbsp;</td></tr>
 <tr><th rowspan="2">DONE</td><td rowspan="2">Recebe</td><td align="center">1</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
 <tr><td>DONE</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
 <tr><th rowspan="2">NO_OP</td><td rowspan="2">Recebe</td><td align="center">1</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
 <tr><td>NO_OP</td><td>&nbsp;</td><td>&nbsp;</td><td></td></tr>
</table>
</center>
