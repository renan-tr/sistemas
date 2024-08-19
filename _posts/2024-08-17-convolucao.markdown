---
layout: post
title:  "Convolução"
date:   2024-08-17 18:39:21 -0300
categories: conteúdos
---

## Convolução

É um operador linear que representa matematicamente como um sistema opera sobre um sinal.
O sinal de saída é o resultado da convolução do sinal de entrada com a resposta ao impulso do sistema.
Pode ser interpretada da seguinte forma: a cada instante um impulso é aplicado à entrada do sistema, resultando em uma dada resposta. O sinal de entrada pode ser representado como uma somatória de impulsos deslocados no tempo. Assim, o sinal de saída será a somatória das respostas de todos os impulsos deslocados. Essa somatória é a convolução.

### Exemplo

Vamos considerar um sistema com resposta ao impulso descrita por {h(m), m = 0,1,2,3} = {1,2,0,1} no qual é aplicada uma entrada {x(m), m = 0} = {2,3,1,0}. 

A figura a seguir ilustra a operação da convolução, que seria o somatório do produto entre as duas funções (entrada e resposta), ao longo da região em que elas se sobrepõem.

![Exemplo de convolução](https://renan-tr.github.io/sistemas/assets/img/convolucao_exemplo.png)

### Matematicamente

Formalmente, a convolução pode ser representada por:

![Exemplo de convolução](https://renan-tr.github.io/sistemas/assets/img/eq_conv.png)

