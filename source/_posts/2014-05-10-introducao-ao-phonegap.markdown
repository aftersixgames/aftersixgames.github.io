---
layout: post
title: "Introdução ao PhoneGap"
date: 2014-05-10 18:59:10 -0200
comments: true
author: mauriciokj
categories:
  - Mobile
  - HTML5
  - JavaScript
  - PhoneGap
---
Boa noite pessoal, como falei antes, vou comentar um pouco sobre tecnologias que tenho estudado, e hoje vou fazer uma pequena introdução ao PhoneGap

O PhoneGap é um framework para o desenvolvimento de aplicações para dispositivos móveis, open source, multiplataforma, com sendo que com ele você pode desenvolver aplicações utilizando JavaScript, CSS3 e HTML5, ou seja, mesmo código para IOS, Android, WindowsPhone, BlackBerry e Symbian, etc.

Hoje o PhoneGap está na versão 3.4 e você pode encontrar tudo que procura sobre ele na sua página oficial PhoneGap.

Para quem já está no mundo de desenvolvimento WEB, se torná até repetitivo falar sobre as vantagens de se trabalhar com esse conjunto (JS, HTML5 e CSS3), então vamos começar com o processo de desenvolvimento usando PhoneGap, hoje vou ajudar vocês a instalar e configurar o PhoneGap, para que na próxima semana possamos iniciar o desenvolvimento de um aplicativo real usando PhoneGap, minha ideia para esse nosso exemplo é criar um aplicativo onde você digite seu código de rastreamento dos correios e por esse aplicativo ele te retorno o histórico desse objeto.

Então, vamos começar.

<!-- more -->

Instalando o Phonegap

Para instalar a versão 3.5, caso você já possua o Node-JS instalado, abra seu terminal e digite o seguinte comando:

```
$ sudo npm install -g phonegap
```

quando terminar a instalação, através do comando “phonegap” você pode ter mais ajuda.

Usando:

```
$ phonegap create minha_encomenda
$ cd minha_encomenda
$ phonegap run android
```

com esses comandos básicos você já terá uma aplicação rodando usando o phonegap
semana que vem vamos começar a colocar a mão na massa e produzir, qualquer duvida ou recomendação nos avise nos comentários
