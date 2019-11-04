---
title: "Conhecendo o IPFS"
date: "2019-10-22"
author: "ratsclub"
cover: "ratsclub/conhecendo-ipfs/st-peters-basilica.jpg"
description: "Conhecendo o IPFS e seus conceitos"
tags:
- ipfs
- p2p
---

## IPFS? É de comer?

[IPFS](https://ipfs.io/) é a sigla para ***Inter-Planetary File System***. Trata-se de um sistema distribuído ([Peer-to-Peer](https://pt.wikipedia.org/wiki/Peer-to-peer)) para armazenamento e acesso de arquivos, websites, aplicações e dados.

Mas o que isso quer dizer, exatamente? Imagine que você está fazendo uma pesquisa na internet sobre Vincent Van Gogh. Você provavelmente começará pela página de Vincent Van Gogh na [Wikipedia](https://pt.wikipedia.org/) que será algo como:

> [https://en.wikipedia.org/wiki/Vincent_Van_Gogh](https://en.wikipedia.org/wiki/Vincent_Van_Gogh)

Quando você colocar essa URL no seu navegador, você está pedindo para que um computador da Wikipedia lhe forneça a página sobre Vincent Van Gogh. Entretanto, essa não é a única opção para você saber mais sobre Vincent Van Gogh. Se você usa o IPFS, seu computador requisitará a página assim:

> /ipfs/QmXoypizjW3WknFiJnKLwHCnL72vedxjQkDDP1mXWo6uco/wiki/Vincent_Van_Gogh.html

O IPFS sabe onde buscar essa informação pelo seu conteúdo, não sua localização. A versão IPFS do artigo sobre Vincent Van Gogh é representada por aquele texto de letras e números no meio da URL (*QmXoy*...), e invés de pedir a um computador da Wikipedia por aquela página, seu computador utilizará o IPFS para pedir a página a todos os computadores do mundo que possuem essa página. Ele lhe trará as informações sobre Vincent Van Gogh de todas as pessoas que as tenha, não só dos computadores da Wikipedia.

## Por que isso importa?

Tornar possível baixar um arquivo de muitos locais que não são gerenciados por uma única organização.

- **Uma internet resiliente.** Se alguém derrubar os servidores da Wikipedia ou um engenheiro comete um grande erro que cause a queda dos servidores, você ainda conseguirá visualizar a página a partir de outra pessoa.

- **Dificulta a censura de conteúdo.** Como os arquivos no IPFS podem vir de diversos lugares, é bem difícil para que qualquer um (mesmo que sejam estados, corporações ou qualquer outra pessoa) bloquear coisas. Em 2017, a Turquia bloqueou a Wikipedia e a Espanha bloqueou websites relacionados ao movimento de independência da Catalunha.

- **Pode acelerar a web quando você está distante ou desconectado.** Se você consegue um arquivo de alguém próximo ao invés de alguém a milhares de quilômetros de distância, claramente tornará o processo mais rápido. Isso é especialmente valioso se sua comunidade tem uma rede local (os computadores são interligados), mas não possue uma boa conexão à internet. (Organizações com grande poder aquisitivo e conhecimento técnico fazem isso hoje em dia utilizando múltiplos bancos de dados e servidores que fornecem conteúdos estáticos (fotos, vídeos, textos...). IPFS quer tornar isso possível para todos.)

## Mas de onde saiu esse nome?

De acordo com o projeto, há o esforço de construir um sistema que funcione através de lugares tão desconectados ou tão distantes quanto planetas. Por isso o nome ***Inter-Planetary File System***.

## Chega de enrolação! Quero saber como funciona!

Você viu um pouco sobre os conceitos e ideias do IPFS. Agora abordaremos alguns dos princípios básicos do sistema.

## Links não mudam no IPFS

Sobre o link da página do Vincent Van Gogh que vimos acima. Parece meio estranho, não?

> /ipfs/QmXoypizjW3WknFiJnKLwHCnL72vedxjQkDDP1mXWo6uco/wiki/Vincent_Van_Gogh.html

Esse amontoado de letras após */ipfs/* é chamado de **identificador de conteúdo** e é como o IPFS consegue conteúdos de diversos lugares.

URLS e caminhos de arquivos tradicionais como...

- [https://en.wikipedia.org/wiki/Vincent_Van_Gogh](https://en.wikipedia.org/wiki/Vincent_Van_Gogh)
- /Users/Joao/Documents/file.doc
- C:\Users\Joao\My Documents\apresentacao.ppt

...identificam um arquivo onde está localizado - em qual computador e em qual pasta de seu disco rígido ele está. Isso não funciona se o arquivo está em diversos lugares como o computador do seu vizinho ou daquele seu amigo de outro estado.

Entretanto, o IPFS não se baseia na localização do arquivo e, sim no conteúdo do arquivo. O identificador de conteúdo nada mais é do que um identificador único do conteúdo do arquivo. Todavia, como o endereço de um arquivo é criado a partir de seu conteúdo, links no IPFS não podem ser alterados.

Claro que pessoas querem atualizar arquivo e mudar seus conteúdos o tempo todo. Contudo, não querem ter que enviar um novo link toda vez que o arquivo fora alterado. Isso é totalmente possível no universo IPFS, mas esse artigo não entrará em detalhes sobre isso.

É importante lembrar que usar o IPFS é completamente participativo e colaborativo. Se ninguém que utiliza o IPFS tem um arquivo com certo identificador para os outros acessarem, você não poderá obtê-lo. No entanto, nada pode ser removido do IPFS enquanto alguém tenha interesse o bastante de mantê-lo disponível.

## É tudo sobre posse e participação

Enquanto há muita coisa complexa por debaixo do capô do IPFS, as ideias fundamentais são sobre mudar como as redes de pessoas e computadores se comunicam. Hoje a internet é estruturada em cima de propriedade e acesso, isso é, você obtém arquivos de quem os possui - isso se eles te garantirem o acesso. IPFS é baseado na idea de posse e participação, ou seja, muitas pessoas possuem os arquivos uns dos outros e participam em mantê-los disponíveis.

Isso significa que IPFS só funciona bem quando pessoas estão participando de forma ativa. Se você usa o seu computador para compartilhar arquivos usando o IPFS, ao desligá-lo, outras pessoas não serão capazes de obter esses arquivos de você. Porém o IPFS já dispõe desse tipo de compartilhamento, você pode combinar com amigos ou fazer parcerias com instituições (por exemplo: museus e bibliotecas podem vir a trabalhar em conjuto) para compartilhar os arquivos uns dos outros.

## Ainda tenho dúvidas

Sinta-se à vontade para me mandar uma mensagem no [Twitter](https://twitter.com/ratsclub) ou para ler mais em [IPFS Documentation](https://docs.ipfs.io/).

---

## Me ajude com um café ☕

**BTC**: [bc1qkc3yruufzkqxyvq5exe50lwrmtc00pmnf4wua0](bitcoin:bc1qkc3yruufzkqxyvq5exe50lwrmtc00pmnf4wua0)

**BCH**: [qqgtmvglvrr6297d6m2z3634pr0a6m77p5ke9lg03k](bitcoincash:qqgtmvglvrr6297d6m2z3634pr0a6m77p5ke9lg03k)

**ETH**: [0xbff1fFA9D91f81100E801120d03eA6C74F7dA87E](ethereum:0xbff1fFA9D91f81100E801120d03eA6C74F7dA87E)

**NANO**: [nano_1g4xrbrqd9axxdjjetkzxk9djinotbuqpbe9ccz3btscctjqyz4m6s5qxbiw](nano:nano_1g4xrbrqd9axxdjjetkzxk9djinotbuqpbe9ccz3btscctjqyz4m6s5qxbiw)