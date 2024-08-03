---
layout: page
title: Sinais
permalink: /sinais/
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

# FIGURA!!!

A temperatura de um ambiente, por exemplo, é um sinal contínuo, visto que em qualquer instante de tempo a temperatura pode ser especificada. Um sinal contínuo é representado no domínio do tempo por x(t), onde t é a variável independente.
O gráfico da figura é representado por $x(t) = sen(3*t) + sen(9.5*t)$.

Um sinal **discreto** é especificado apenas em valores discretos de sua variável independente, como ilustrado a seguir.

# FIGURA!!!

Por exemplo, o sinal x(t) seria apenas representado nos valores $t = n T_s$, onde "T_s" é o tempo de amostragem (constante). Usualmente, o sinal é descrito por x(n), onde $n$ é um número inteiro. A vantagem do sinal discreto é que ele pode ser armazenado e processado de forma eficiente. Como a maioria dos sinais práticos são contínuos, o sinal discreto é obtido pela amostragem do sinal contínuo.

Observação: alguns sinais como vendas mensais são inerentementes discretos.

Em geral, o processamento de um sinal discrete não depende do tempo de amostragem. No entanto, $T_s$ é necessário para converter o sinal discreto novamente em contínuo.

Já em um sinal **digital** os valores do sinal discreto é quantizado, sendo a forma utilizada no processamento digital de sinais.

### Periódicos e Aperiódicos

