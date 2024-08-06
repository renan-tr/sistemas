---
layout: post
title:  "Conceitos básicos de sinais"
date:   2024-08-03 18:39:21 -0300
categories: conteúdos
---

## Definições

- **Sinal** - Um sinal representa alguma informação
- **Sistema** - Produz um sinal de saída ou uma ação em resposta a um sinal de entrada

Por exemplo, a temperatura é um __sinal__. Um aquecedor que mantém a temperatura constante em um ambiente é um __sistema__.

Os sinais podem ser elétricos, mecânicos, ou de outras formas. No entanto, são usualmente convertidos para sinais elétricos para facilitar o processamento. Por exemplo, o som é composto por ondas de pressão viajando pelo ar, sendo convertido para um sinal elétrico através de um microfone.

Sinais em sistemas práticos possuem perfil de amplitude arbitrário, isto é, não é definido por uma função matemática ou padrão específico.

## Classificação

### Contínuo x Discreto

Um sinal **contínuo** é especificado em cada valor de sua variável independente, como na figura:

![Sinal contínuo](https://renan-tr.github.io/sistemas/assets/img/continuo.png)

A temperatura de um ambiente, por exemplo, é um sinal contínuo, visto que em qualquer instante de tempo a temperatura pode ser especificada. Um sinal contínuo é representado no domínio do tempo por x(t), onde t é a variável independente.
O gráfico da figura é representado por x(t) = sen(3*t) + sen(9.5*t).

Um sinal **discreto** é especificado apenas em valores discretos de sua variável independente, como ilustrado a seguir.

![Sinal contínuo](https://renan-tr.github.io/sistemas/assets/img/discreto.png)

Por exemplo, o sinal x(t) seria apenas representado nos valores t = n Ts, onde Ts é o tempo de amostragem (constante). Usualmente, o sinal é descrito por x(n), onde n é um número inteiro. A vantagem do sinal discreto é que ele pode ser armazenado e processado de forma eficiente. Como a maioria dos sinais práticos são contínuos, o sinal discreto é obtido pela amostragem do sinal contínuo.

Observação: alguns sinais como vendas mensais são inerentementes discretos.

Em geral, o processamento de um sinal discrete não depende do tempo de amostragem. No entanto, Ts é necessário para converter o sinal discreto novamente em contínuo.

Já em um sinal **digital** os valores do sinal discreto é quantizado, sendo a forma utilizada no processamento digital de sinais.

### Periódicos e Aperiódicos

- O menor inteiro N positivo que satisfaça a condição x(n + N) = x(n), para todo n é o período de um sinal.
- Quando o período se aproxima de infinito, não há repetição do padrão e o sinal é aperiódico.

Por exemplo, qual é o período do sinal a seguir:

![Sinal contínuo](https://renan-tr.github.io/sistemas/assets/img/periodico.png)

Um sinal aperiódico típico é mostrado na figura as seguir:

![Sinal contínuo](https://renan-tr.github.io/sistemas/assets/img/aperiodico.png)

Que sinal é esse?

É mais fácil decompor um sinal arbitrário em termos de sinais periódicos de forma que a relação entrada saída se torna uma operação de multiplicação. Dessa forma, a maiorio das análises de sinais práticos é feita considerando sinais periódicos básicos.

### Energia e Potência

Potência e energia envolvem tanto a amplitude do sinal com sua duração.
Em sistemas de processamento de sinais, o sinal desejado está usualmente misturado com ruído, sendo a qualidade do sistema descrita pela relação de potência sinal ruído.

A potência instantênea dissipada por um resistor de 1 ohms é x²(t), onde x(t) pode ser a tensão ou a corrente através dele. Se a potência for integrada ao longo do tempo, obtém-se a energia dissipada.
De forma análoga, a soma dos quadrados dos valores de um sinal discreto x(n) é um indicador de sua energia, sendo dado por:

![Equação energia do sinal](https://renan-tr.github.io/sistemas/assets/img/eqs/eq_energia_sinal.png)

Sinais aperiódicos com energia finita são chamados de sinais de energia. Por exemplo, qual a energia de x(n) = 4(0.5)^n?

Se a energia do sinal é infinita, é possível caracterizá-lo em termos da potência, definida como

![Equação potência do sinal](https://renan-tr.github.io/sistemas/assets/img/eqs/eq_potencia_sinal.png)

Para um sinal periódico com período N

![Equação potência do sinal periódico](https://renan-tr.github.io/sistemas/assets/img/eqs/eq_potencia_sinal_periodico.png)

Sinais, periódicos ou aperiódicos, com potência média finita são chamados de sinais de potência.
Formas de onda senoidais são típicos exemplos de sinais de potência.
Qual a potência média da onda cos(2πn/4)?

### Simetrias

O processamento e armazenamento de um sinal pode ser simplificado se sua simetria for explorada.

- Um sinal possui simetria par se x(-n) = x(n)
- Um sinal possui simetria ímpar se x(-n) = -x(n)

Exemplo:

![Sinal contínuo](https://renan-tr.github.io/sistemas/assets/img/simetria.png)

A soma de dois sinais com simetria par resulta em outro sinal com simetria par e a soma de dois sinais com simetria ímpar resulta em outro sinal com simetria ímpar.

Um sinal arbitrário pode ser sempre decomposto em termos de suas componentes com simetria par e ímpar, xe(n) e xo(n).

Exemplo:

![Sinal contínuo](https://renan-tr.github.io/sistemas/assets/img/componentes.png)

### Casualidade

Os sinais práticos ocorrem em algum instante finito de tempo, usualmente escolhido como n = 0, sendo considerados nulo antes desse instante. Estes são chamados de sinais casuais (x(n) = 0 para n < 0). Sinais com x(n) diferente de 0 para n < 0 são sinais acasuais.

### Sinais determinísticos ou aleatórios

Sinais cujos valores são conhecidos para qualquer n são chamados de determinísticos. Já aqueles cujos valores não são exatamente conhecido são chamdas de sinais aleatórios. Este tipo de sinal é caracterizado por um modelo de probabilidade ou estatístico. Sinais aleatório são muito importante, pois todos os sinais práticos são aleatórios de alguma forma. por outro lado, a análise de sinais determinísticos é bem mais simples.

A relação entrada saída de um sistema permanece a mesma para sinais aleatórios ou determinísticos.

## Sinais básicos

![Sinal básico](https://renan-tr.github.io/sistemas/assets/img/sinais_basicos.png)

![Sinal básico](https://renan-tr.github.io/sistemas/assets/img/sinais_basicos2.png)

## Teorema da amostragem

Como o processamento de sinal digital é bem mais vantajoso que o de um sinal contínuo, em geral prefere-se converter os sinais contínuos em digitais. Este processo envolve amostrar o sinal no tempo e na amplitude. Amostrar no tempo significa observar o sinal apenas em instantes discretos de tempo. Dessa forma, o número total de amostras é reduzido de infinito (sinal contínuo) para um número finito de valores. Esta redução restringe a habilidade de representar variações rápidas no tempo, reduzindo a faixa de frequências que pode ser representada em um sinal discreto.
Como os sinais práticos possuem uma certa faixa de frequências de interesse, é possível representar um sinal contínuo por um discreto com a precisão requerida, desde que um intervalo de amostragem específico seja respeitado.

O teorema da amostragem especifica que um sinal contínuo x(t) pode ser unicamente determinado a partir de sua versão amostrada x(n) se o intervalo de amostragem Ts for menor que 1/2f, onde f é a frequência da componente de maior frequência que compõe o sinal x(t). Isso implica que deve haver mais que 2 amostras por ciclo do sinal de maior frequência.

A figura a seguir ilustra o efeito do intervalo de amostragem, mostrando o que ocorre quando o teorema não é respeitado.

![Aliasing](https://renan-tr.github.io/sistemas/assets/img/aliasing.png)

## Operações

### Time shifting

O sinal x(n+k) é uma versão deslocada no tempo em relação ao sinal x(n), como ilustrado na figura a seguir:

![Time shifting](https://renan-tr.github.io/sistemas/assets/img/time_shifting.png)

Se k for positivo, o sinal está atrasado.

### Time reversal

Seria o espelhamento do sinal em relação ao eixo vertical, sendo obtido ao substituir x(n) por x(-n).

A figura ilustra a operação time reversal e as operações time reversal e time shifting em conjunto.

![Time shifting](https://renan-tr.github.io/sistemas/assets/img/time_reversal.png)

### Time scaling

Substituindo a variável independente n em x(n) por n/a ou an, com a diferente de 0, resulta em uma versão com a escala modificada do sinal.
O sinal x(an) é uma versão comprimida, enquanto o sinal x(n/a) é uma versão expandida.

A operação é ilustrada na figura a seguir.

![Time shifting](https://renan-tr.github.io/sistemas/assets/img/time_scaling.png)
