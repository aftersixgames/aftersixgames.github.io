---
layout: post
title: "CoronaSDK - 3 Coisas que você precisa saber sobre Graphics 2.0"
date: 2015-02-18 21:36:41 -0200
comments: true
categories:
---
Olá pessoal recentemente o pessoal do Corona Labes trouxeram a [engine Grafica 2.0.](http://coronalabs.com/blog/2013/11/14/new-public-release-and-graphics-2-0/)

E enquanto nos foi dado muita coisa nova para brincar – tanto quanto enormes melhorias na engine grafica – nós também temos que adotar uma certa quantidade de mudanças, estas novas melhorias não vieram sem custo sobre o SDK básico.

Aqui estao as top 3 coisas que você precisa estar ciente a respeito da nova engine grafica no Corora SDK, sendo um iniciante ou mesmo migrando um projeto existente.

## Anchor Points (Pontos Ancoras)

A mais importante das mudanças no Corona SDK é **display:SetReferencePoint()** sendo substituido pelos mais flexiveis pontos ancoras.

->**Anchor points são os novos pontos de referências para mostrar objetos.**<-

Quando usando o antigo reference points, nos eramos capazes de setar um ponto em uma das nove posições, o que está bom na maioria dos casos, mas com o anchor points nós podemos posicionar em qualquer ponto em um espaço de objetos coordenados.( display objects coordinate space ) Antes de olharmos aos aspectos novos do anchor points, vamos primeiro olhar como traduzir o velho sistema reference point para o novo anchor points, os quais agora são baseados em porcentagem. A porcentagem sendo baseada na largura e altura do display do objeto.

**display.TopLeftReferencePoint**
```
--Velho
obj:setReferencePoint( display.TopLeftReferencePoint )
--Novo
obj.anchorX, obj.anchorY = 0, 0
```
**display.TopCenterReferencePoint**
```
--Velho
obj:setReferencePoint( display.TopCenterReferencePoint )
--Novo
obj.anchorX, obj.anchorY = .5, 0
```
**display.TopRightReferencePoint**
```
--Velho
obj:setReferencePoint( display.TopRightReferencePoint )
--Novo
obj.anchorX, obj.anchorY = 1, 0
```
**display.CenterLeftReferencePoint**
```
--Velho
obj:setReferencePoint( display.CenterLeftReferencePoint )
--Novo
obj.anchorX, obj.anchorY = 0, .5
```
**display.CenterReferencePoint**
```
--Velho
obj:setReferencePoint( display.CenterReferencePoint )
--Novo
obj.anchorX, obj.anchorY = .5, .5
```
**display.CenterRightReferencePoint**
```
--Velho
obj:setReferencePoint( display.CenterRightReferencePoint )
--Novo
obj.anchorX, obj.anchorY = 1, .5
```
**display.BottomLeftReferencePoint**
```
--Velho
obj:setReferencePoint( display.BottomLeftReferencePoint )
--Novo
obj.anchorX, obj.anchorY = 0, 1
```
**display.BottomCenterReferencePoint**
```
--Velho
obj:setReferencePoint( display.BottomCenterReferencePoint )
--Novo
obj.anchorX, obj.anchorY = .5, 1
```
**display.BottomRightReferencePoint**
```
--Velho
obj:setReferencePoint( display.BottomRightReferencePoint )
--Novo
obj.anchorX, obj.anchorY = 1, 1
```

Como comentado anteriormente, o posicionamento é baseado em porcentagem.

Visualmente fica assim:

->![alt Desenvolvimento de Games com CoronaSDK anchor2](/images/2015-02-18-coronasdk-3-coisas-que-voce-precisa-saber-sobre-graphics-2-dot-0/anchor1.png)<-


Isto nos permite setar um “ponto de referencia” em qualquer ponto no objeto display. Se precisarmos rotacionar do centro, mas um pouquinho para a esquerda, então podemos fazer assim:

```
obj.anchorX, obj.anchorY = .25, .5
```

->![alt Desenvolvimento de Games com CoronaSDK anchor2](/images/2015-02-18-coronasdk-3-coisas-que-voce-precisa-saber-sobre-graphics-2-dot-0/anchor2.png)<-


Esta nova maneira de trabalhar com reference points será de grande beneficio para dynamic UI e mostrar objetos que precisam se transformar em um ponto especifico.

O “anchor” helper Apesar de ser completamente opcional, você pode colocar o código seguinte no seu main.lua, ou globals mod para alguns atalhos para ponts de ancora que operam como constante no antigo reference point:
```
-- main.lua or globals.lua
anchor = { TopLeft = function(t) t.anchorX, t.anchorY = 0, 0; end,
           TopCenter = function(t) t.anchorX, t.anchorY = .5, 0; end,
           TopRight = function(t) t.anchorX, t.anchorY = 1, 0; end,
           CenterLeft = function(t) t.anchorX, t.anchorY = 0, .5; end,
           Center = function(t) t.anchorX, t.anchorY = .5, .5; end,
           CenterRight = function(t) t.anchorX, t.anchorY = 1, .5; end,
           BottomLeft = function(t) t.anchorX, t.anchorY = 0, 1; end,
           BottomCenter = function(t) t.anchorX, t.anchorY = .5, 1; end,
           BottomRight = function(t) t.anchorX, t.anchorY = 1, 1; end, }
```
Para usar esta funcionalidade, você faria assim:
```
-- some.lua

local r = display.newRect( 0, 0, 200, 300 )

anchor.Center( r ) -- seta a ancora para o centro
 
r.x = display.contentCenterX
r.y = display.contentCenterY
 
anchor.TopLeft( r ) -- seta a anchora para o topo / esquerda
 
r.x = 0
r.y = 0

```

## Valores de Cores
Outra grande modificação é a maneira de especificar a cor. Cores agora também são baseadas em porcentagem. Neste caso o valor que precisamos especificar é a porcentagem do padrão 255 que estamos acostumados.

Onde antes representavamos uma cor, como verde, assim:

**0, 255, 0**

Agora representamos assim:

**0, 1, 0**

Ou, 0% vermelho, 100% verde, 0% azul

Os valores de colres que usavamos previamente variavam de 0 a 255. Podemos usar este fato para rapidamente calcular a porcentagem da cor.
Por exemplo, para setar a cor para azul ardósia – que é 106, 90,205 – nós podemos fazer assim:
```
obj:setFillColor( 106/255, 90/255, 205/255 )
```
Você pode também ajustar o alpha. Que é facil representar com porcentagem.
```
obj:setFillColor( 106/255, 90/255, 205/255, .6 )
```
Isto proverá a porcentagem requerida para qualquer setFillColor() método de objeto.
Novamente, completamente opcional, mas aqui uma simples função helper para cores. Coloque este codigo em global mod ou no topo do seu arquivo:
```
color = function(r,g,b) return (r/255), (g/255), (b/255); end
```
Você pode usar assim:
```
txtObj:setFillColor( color( 128, 128, 128 ) )
```

## Text Color (Cor de texto)

Agora que nos familiarizamos com os novos valores de cores, deve ser percebido que o metodo **setTextColor()** do TextObject tornou-se obsoleto e agora usa o universal **setFillColor()**. Novamente você deve fornecer os valores de cor usando o novo método como mostrado a baixo:
```
--Velho
textObj:setTextColor( 128, 128, 128 )
--Novo
textObj:setFillColor( 128/255, 128/255, 128/255 )
```

Ainda tem muito a aprender sobre o novo Corona SDK graphics engine, mas eu dou as boas vindas para as possibilidades que vem com ele. Espero que este artigo tenha ajudado você a entender um pouco mais sobre a nova engine, e que ajude a começar a fazer algumas apps e jogos incriveis no [Corona SDK.](http://www.coronalabs.com/)

A tradução do [Artigo original](http://www.develephant.net/3-things-you-need-to-know-about-corona-sdk-graphics-2-0/) foi feita pela [Franciele Andre](br.linkedin.com/pub/franciele-andre/97/963/107/pt)

*Se você achou esta informação util, outros poderão também, então por favor compartilhe. Obrigado.*
