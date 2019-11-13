---
title: "Criptografia #1 - XOR"
date: 2019-11-04T22:23:52Z
cover: "ratsclub/criptografia-1/cover.jpg"
author: ratsclub
description: "XOR é uma operador boolean binário que é verdadeiro somente quando uma das entradas é verdadeira."
tags:
- crypto
- criptografia
draft: true
---

# Sumário

- [Sumário](#sum%c3%a1rio)
- [Algumas propriedades do XOR](#algumas-propriedades-do-xor)
- [Operador lógico XOR](#operador-l%c3%b3gico-xor)
- [One-time pad (cifra de uso único)](#one-time-pad-cifra-de-uso-%c3%banico)

XOR, também chamado de *exclusive or*, é um operador boolean[^1] binário[^2] que é verdadeiro somente quando uma das entradas é verdadeira. Podemos pensar no XOR como um "*invertedor programável*". Uma das entradas decidirá se a outra será invertida ou não. O termo "*inverter*" bits também é chamado de "*flipar*" bits.



Em matemárica e trabalhos sobre criptografia, o operador XOR é representado por uma cruz num círculo: ⊕. Utilizaremos a mesma notação.

<center>
![](/ratsclub/criptografia-1/fig-1.png)
</center>

As entradas e saídas aqui estão nomeadas como se estivéssemos utilizando XOR como uma operação de criptografia. Na esquerda nós temos o bit em texto-plano *Pi*. O *i* é só um índice, pois normalmente vamos trabalhar com mais do que um bit. Em cima nós temos o bit chave *ki* que decide se inverteremos ou não *Pi*. Na direita nós temos o bit cifrado, *Ci*, que é o resultado da operação XOR.

# Algumas propriedades do XOR

Veremos com mais detalhes algumas de suas propriedades.
Nós vimos que a saída do XOR é 1 quando uma ou outra entrada (não as duas) é 1:

```
0 ⊕ 0 = 0       1 ⊕ 0 = 1

1 ⊕ 1 = 0       0 ⊕ 1 = 1
```

<center>
</center>

Podemos usar alguns macetes aritméticos que podemos derivar disso.

1. Você pode aplicar o XOR em qualquer ordem: a ⊕ (b ⊕ c) = (a ⊕ b) ⊕ c
2. Você pode *flipar* os operadores: a ⊕ b = b ⊕ a
3. Qualquer bit que XOR ele mesmo é 0: a ⊕ a = 0. Se *a* é 0, então 0 ⊕ 0 = 0; se *a* é 1, então  1 ⊕ 1 = 0.
4. Qualquer bit que for XOR 0 é ele novamente: a ⊕ 0 = a. Se *a* é 0, então é 0 ⊕ 0 = 0; se *a* é 1, então é  1 ⊕ 0 = 1.

Essas regras também implicam que a ⊕ b ⊕ a = b:


```
a ⊕ b ⊕ a = a ⊕ a ⊕ b (segunda regra)

= 0 ⊕ b (terceira regra)

= b (quarta regra)
```


Nós usaremos com frequência essa propriedade quando usando XOR para criptografar. Você pode pensar no primeiro XOR com *a* como criptografando, e o segundo como descriptografar.

# Operador lógico XOR

XOR, como o definimos, opera somente em bit únicos ou valores booleanos. Entretanto, como nós normalmente lidamos com valores compostos de muitos bits, a maioria das linguagens de programação nos provê um operador lógico XOR: um operador que aplica XOR nos respectivos bits em um valor.

Python, por exemplo, provê o operador ^ (til) para XOR em inteiros. Ele faz isso ao expressar esses dois números inteiros em binário[^3], e então fará um XOR nos seus respectivos bits. Por isso o nome, operador lógico XOR.


```
73 ⊕ 87 = 0b1001001 ⊕ 0b1010111

---------------
  1 0 0 1 0 0 1 (esqueda)
  ⊕⊕⊕⊕⊕⊕⊕
  1 0 1 0 1 1 1 (direita)
= 0 0 1 1 1 1 0
= 0b0011110
= 30
```

# One-time pad (cifra de uso único)



[^1]: Usa somente "verdadeiro" e "falso" como entrada e saída de valores.
[^2]: Recebe dois parâmetros.
[^3]: Normalmente, numéros já são armazenados em binário, então isso não traz nenhum trabalho a mais. Ao ver um número com o prefixo "0b", os digitos restantes serão uma representação binária.