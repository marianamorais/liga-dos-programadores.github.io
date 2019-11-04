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
*Fig. 1 Assinando blocos - draw.io*
</center>

Como a chave privada é única, quando com o bloco é criada uma única assinatura. A chave pública correspondente pode ser usada para verificar se a assinatura está correta, entretanto, se você tentar criar um bloco assinado com uma chave privada incorreta, será fácil para a rede rejeitar esse bloco.

Isso significa que os usuários não precisam dar suas chaves privadas para a verificação, somente as chaves públicas.

<center>
![](/ratsclub/nano-2-seeds-e-chaves/fig-2.jpg)
*Fig. 2 Checando se um bloco assinado é válido - draw.io*
</center>

## O que é uma seed?

Uma **seed** (ou semente) é uma forma fácil de gerenciar diversas chaves privadas. Ao invés de termos muitas e muitas chaves privadas, você possui um longo número chamado seed que será executado contra outro algorítmo que será responsável por gerar outras chaves privadas (e suas correspondentes chaves públicas). As chaves privadas são geradas em sequência, ou seja, sua primeira chave sempre será a primeira, a segunda sempre será a segunda e assim em diante.

Esse processo permite que você recupere suas chaves e seus Nano com uma única seed.

<center>
![](/ratsclub/nano-2-seeds-e-chaves/fig-3.jpg)
*Fig. 3 Uma seed sempre produzirá as mesmas chaves privadas em ordem - draw.io*
</center>

## Como endereços Nano são gerados?

Seu endereço Nano — começados nano_ — são suas chaves públicas e um checksum. O checksum torna fácil o processo de verificação de autenticação da conta, ou seja, verificar se é uma conta válida ou não. É possível ver uma conta através de uma chave pública e vice-versa. Em resumo:

- Um endereço é ligado à uma chave pública através uma chave privada
- Em um bloco Nano, cada endereço possui seu próprio blockchain. Isso que permite a reutilização de seu interesse.

## Mais informações

- https://nanoo.tools/key-guide
- https://en.wikipedia.org/wiki/Public-key_cryptography
- https://docs.nano.org/integration-guides/the-basics/#account-key-seed-and-wallet-ids
- https://nanoo.tools/key-address-seed-converter

**Esse guia foi totalmente traduzido a partir do seguinte [post](https://amp-reddit-com.cdn.ampproject.org/c/s/amp.reddit.com/r/nanocurrency/comments/aoe0me/nano_how_1_seeds_and_keys/) do usuário u/jayycox no reddit. Todos os créditos são dele.*

---

## Me ajude com um café ☕

**BTC**: [bc1qkc3yruufzkqxyvq5exe50lwrmtc00pmnf4wua0](bitcoin:bc1qkc3yruufzkqxyvq5exe50lwrmtc00pmnf4wua0)

**BCH**: [qqgtmvglvrr6297d6m2z3634pr0a6m77p5ke9lg03k](bitcoincash:qqgtmvglvrr6297d6m2z3634pr0a6m77p5ke9lg03k)

**ETH**: [0xbff1fFA9D91f81100E801120d03eA6C74F7dA87E](ethereum:0xbff1fFA9D91f81100E801120d03eA6C74F7dA87E)

**NANO**: [nano_1g4xrbrqd9axxdjjetkzxk9djinotbuqpbe9ccz3btscctjqyz4m6s5qxbiw](nano:nano_1g4xrbrqd9axxdjjetkzxk9djinotbuqpbe9ccz3btscctjqyz4m6s5qxbiw)
