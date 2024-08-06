---
layout: post
title:  "Python - Sinais"
date:   2024-08-03 20:39:21 -0300
categories: python
---

### Bibliotecas

```python
import matplotlib.pyplot as plt # biblioteca para fazer gráficos
import numpy as np # biblioteca para trabalhar com arrays
import scipy as sp # biblioteca para processamento de sinais
import scipy.io.wavfile # para trabalhar com arquivos wav
```

### Trabalhando com som

Para ler um arquivo wav:
```python
taxa_amostragem, audio = scipy.io.wavfile.read('teste.wav')
```
A função retorna duas variáveis: a frequência de amostragem e o som.


Se for verificar a dimensão do audio com o comando
```python
audio.shape
```
tem-se dois valores: a quantidade de pontos e o número de canais.


Podemos traçar o gráfico de um dois canais (esquerdo):
```python
plt.plot(audio[:,0]) #gráfico de linha
plt.stem(audio[:,0]) #gráfico stem
plt.scatter(audio[:,0]) #gráfico de ldispersão
```
Como só foi passado um parâmetro para cada comando acima, os gráficos estão sendo traçados em função do númeor da amostra.


Para tocar o som:
```python
from IPython.display import Audio
Audio(audio[:,0], rate=taxa_amostragem)
```

Como podemos fazer para alterar a quantização?


### Criando uma senóide

```python
Fs = 44100
T = 10
t = np.linspace(0,T,Fs*T+1)
audio_1k = np.sin(2*np.pi*1e3*t)
Audio(audio_1k, rate=Fs)
```

Como podemos fazer para alterar a frequência de amostragem?

Para fazer uma varredura em uma faixa de frequências, podemos usar o
```python
from scipy.signal import chirp, spectrogram
Fs = 20000
T = 10
t = np.linspace(0,T,Fs*T+1)
w = chirp(t, f0=1, f1=20e3, t1=T, method='linear')
Audio(w, rate=Fs)
```