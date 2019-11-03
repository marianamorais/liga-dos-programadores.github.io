---
title: "Nano #2: Seeds e chaves"
date: 2019-11-03T01:46:19-07:00
author: "@ratsclub"
cover: "ratsclub/nano-2-seeds-e-chaves/cover.jpg"
description: "Como funciona o sistema de chaves do nano?"
tags:
- nano
- p2p
- crypto
draft: true
---

## Resumo

**Nano** utiliza um sistema de **chaves públicas** e **privadas** para mandar e receber blocos, em outras palavras: *"Suas chaves, seu Nano. Não são suas chaves, não é seu Nano"*.

Uma **seed** é um longo número que pode ser usado para gerar diversas chaves privadas, com isso em mente, um **endereço** (leia-se conta) Nano é somente uma chave pública com um checksum que são interligados com a chave privada original.


## O que são chaves públicas e privadas?

Chaves públicas e privadas são parte vitais de uma criptomoeda e provêem um método de posse das moedas e token. **São números únicos e longos demais para ser adivinhados** que funcionam como chaves e dão acesso ao usuários.

*É interessante frisar que seus Nano não são armazenados em sua carteira! Na verdade, eles existem na rede e sua carteira simplesmente possui as chaves para manipulá-los.*

Nano usa um padrão bem estabelecido de chaves públicas e privadas. Uma chave privada é usada para "assinar" transações no bloco. Essa chave privada possui uma chave pública que é diretamente ligada a um endereço. O único método para criar uma transação ligada à uma carteira é assinar esse block com uma **chave privada** — com Nano isso pode ser enviado e recebido.

<center>
![](/ratsclub/nano-2-seeds-e-chaves/fig-1.jpg)
</center>

