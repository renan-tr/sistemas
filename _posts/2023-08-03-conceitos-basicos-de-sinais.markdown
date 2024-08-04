---
layout: post
title:  "Conceitos básicos de sinais"
date:   2023-08-03 18:39:21 -0300
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
O gráfico da figura é representado por $x(t) = sen(3*t) + sen(9.5*t)$.

Um sinal **discreto** é especificado apenas em valores discretos de sua variável independente, como ilustrado a seguir.

![Sinal contínuo](https://renan-tr.github.io/sistemas/assets/img/discreto.png)

Por exemplo, o sinal x(t) seria apenas representado nos valores $t = n T_s$, onde "T_s" é o tempo de amostragem (constante). Usualmente, o sinal é descrito por x(n), onde $n$ é um número inteiro. A vantagem do sinal discreto é que ele pode ser armazenado e processado de forma eficiente. Como a maioria dos sinais práticos são contínuos, o sinal discreto é obtido pela amostragem do sinal contínuo.

Observação: alguns sinais como vendas mensais são inerentementes discretos.

Em geral, o processamento de um sinal discrete não depende do tempo de amostragem. No entanto, $T_s$ é necessário para converter o sinal discreto novamente em contínuo.

Já em um sinal **digital** os valores do sinal discreto é quantizado, sendo a forma utilizada no processamento digital de sinais.

### Periódicos e Aperiódicos

- O menor inteiro N positivo que satisfaça a condição x(n + N) = x(n), para todo n é o período de um sinal.
- Quando o período se aproxima de infinito, não há repetição do padrão e o sinal é aperiódico.

Por exemplo, qual é o período do sinal a seguir:

# FIGURA!!!

Um sinal aperiódico típico é mostrado na figura as seguir:

# FIGURA!!!

Que sinal é esse?

è mais fácil decompor um sinal arbitrário em termos de sinais periódicos de forma que a relação entrada saída se torna uma operação de multiplicação. Dessa forma, a maiorio das análises de sinais práticos é feita considerando sinais periódicos básicos.

### Energia e Potência

Potência e energia envolvem tanto a amplitude do sinal com sua duração.
Em sistemas de processamento de sinais, o sinal desejado está usualmente misturado com ruído, sendo a qualidade do sistema descrita pela relação de potência sinal ruído.

A potência instantênea dissipada por um resistor de 1 ohms é $$x²(t)$$, onde x(t) pode ser a tensão ou a corrente através dele. Se a potência for integrada ao longo do tempo, obtém-se a energia dissipada.
De forma análoga, a soma dos quadrados dos valores de um sinal discreto x(n) é um indicador de sua energia, sendo dado por:

$$  E = \sum_{n=-\infty}^{\infty} \left| x(n) \right|^2 $$

Sinais aperiódicos com energia finita são chamados de sinais de energia. Por exemplo, qual a energia de $$x(n) = 4(0.5)^n$$?

Se a energia do sinal é infinita, é possível caracterizá-lo em termos da potência, definida como

$$ P = \lim_{N \rightarrow \infty} \frac{1}{2N+1} \sum_{n=-N}^{N} \left| x(n) \right|^2 $$

Para um sinal periódico com período N

$$ P = \frac{1}{N} \sum_{n=0}^{N-1} \left| x(n) \right|^2 $$

Sinais, periódicos ou aperiódicos, com potência média finita são chamados de sinais de potência.
Formas de onda senoidais são típicos exemplos de sinais de potência.
Qual a potência média da onda $$cos(2πn/4)$$?

### Simetrias

O processamento e armazenamento de um sinal pode ser simplificado se sua simetria for explorada.

- Um sinal possui simetria par se x(-n) = x(n)
- Um sinal possui simetria ímpar se x(-n) = -x(n)

Exemplo:

# FIGURA!!!

A soma de dois sinais com simetria par resulta em outro sinal com simetria par e a soma de dois sinais com simetria ímpar resulta em outro sinal com simetria ímpar.

Um sinal arbitrário pode ser sempre decomposto em termos de suas componentes com simetria par e ímpar, xe(n) e xo(n).

Exemplo:

# FIGURA!!!

### Casualidade

