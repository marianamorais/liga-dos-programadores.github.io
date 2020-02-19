+++
title = "Indrodução ao Java"
date = "2019-10-30"
author = "@alvarofilho"
cover = "alvarofilho/indroducao-ao-java/post1.png"
description = "Indrodução a linguagem Java"
draft = true
+++

# Introdução

[Java](https://www.java.com/pt_BR/) é uma linguagem orientada a objetos que utiliza uma máquina virtual para a execução dos seus códigos.

# Instalação
Para poder programar em Java precisamos baixar o [Java Development Kit](https://www.oracle.com/technetwork/java/javase/overview/index.html) ou mais conhecido como [JDK](https://www.oracle.com/technetwork/java/javase/overview/index.html)

### Windows
No Windows precisamos entrar no site da oracle para poder baixar o [JDK](https://www.oracle.com/technetwork/java/javase/downloads/index.html)

### Linux
No Linux basta rodar esses comandos:

Debian/Ubuntu
```sh
sudo add-apt-repository ppa:openjdk-r/ppa
sudo apt-get update
sudo apt-get install openjdk-12-jdk
```
CentOS
```sh
sudo yum update
sudo yum install java-12-openjdk-devel
```

## Depois de ter instalar o JDK precisamos agora instalar um [Ambiente de desenvolvimento integrado](https://pt.wikipedia.org/wiki/Ambiente_de_desenvolvimento_integrado) ou como é mais conhecido IDE, eu vou está listado alguns IDES que você podera está utilizando ao logo desse curso.

- [Netbens](https://netbeans.org/)
- [Eclipse](https://www.eclipse.org/)
- [IntelliJ](https://www.jetbrains.com/idea/)

E para quem quiser utilizar o Visual Studio Code também é possível, bastar a [documentação](https://code.visualstudio.com/docs/languages/java) dele. 
Eu vou está utilizando o Netbens e recomendo que você também utlize para não ficar perdido.

# Programando

Agora podemos ir para a melhor parte desse tutorial a programação. Iremos abrir o IDE e logo em seguida devemos clica em **Arquivo > Novo Projeto**

Se tudo ocorrer bem é para uma arquivo similar a esse.

```Java

public class JavaApplication {

    public static void main(String[] args) {
      //Code
    }
    
}
```

Dentros do **//Code** será escrito o nosso código primeiro código, dentro dele deveremos digital `System.out.println("Olá, Liga dos Programadores!");`

O resultado final será esse:
```Java

public class JavaApplication {

    public static void main(String[] args) {
        System.out.println("Olá, Liga dos Programadores!");
    }
    
}
```

Podemos clica em **Executar > Executar Projeto** ou **CTRL + F11**

e teremos na **Saida**:
```
run:
Olá, Liga dos Programadores!
```

`System.out.println();` é uma instruções que imprimir o argumento passado a ela, esse argumento precisar está dentro de uma aspa dupla e precisar ser um texto.

#### Embreve você ira entende mais o porquer disso.

Por hoje chegamos ao final, no próximo tutorial vamos aborda Variáveis e Operadores Matemáticos.
