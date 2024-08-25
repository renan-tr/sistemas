---
layout: post
title:  "Propriedades da Convolução"
date:   2024-08-24 18:39:21 -0300
categories: conteúdos
---

## Comutativa

A ordem dos fatores não altera o resultado:

```
x(n) * h(n) = h(n) * x(n)
```

## Distributiva

A convolução de uma sequência com a soma de duas sequências é a mesma que o soma da convolução da primeira sequência com a convolução da segunda:

```
x(n) * (h1(n) + h2(n)) = x(n) * h1(n) + x(n) * h2(n)
```

## Associativa

A convolução de uma sequência com a convolução de duas sequências é a mesma que a convolução da convolução das primeiras duas sequências com a terceira:

```
x(n) * (h1(n) * h2(n)) = (x(n) * h1(n)) * h2(n)
```

## Deslocamento

A convolução de duas sequências deslocadas é a convolução das duas sequências originais deslocadas pela soma dos deslocamentos das sequências individuais:

```
se x(n) * h(n) = y(n) então x(n - l) * h(n - m) = y(n - l - m)
```

