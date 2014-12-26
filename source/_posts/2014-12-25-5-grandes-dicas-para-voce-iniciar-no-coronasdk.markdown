---
layout: post
title: "5 grandes dicas para você iniciar no coronaSDK"
date: 2014-12-25 22:22:21 -0200
comments: true
author: mauriciokj
categories:
  - Desenvolvimento de Games
  - CoronaSDK
---

Pra você que vai começar a desenvolver jogos para plataformas moveis e decidiu trabalhar com o CoronaSDK, aqui vão algumas dicas pra você já começar com uma boa organização e com uma boa linha pra onde seguir, espero que você já tenha acessado o site http://coronalabs.com e realizado o cadastro pra que possamos começar :)

<!-- more -->
* Sempre manter o corona atualizado

	Se você está iniciando agora, muito provavelmente já vai possuir a ultima versão do corona Sdk, porem, é sempre bom conferir se a sua versão é a mais recente. Mas por que isso? O corona tem atualizações praticamente diárias para quem é um assinante pago, mas para quem é um usuário free, isso muda um pouco, as atualizações tem uma frequência grande, mas não diária. Essas atualizações sempre trazem alguma correção de BUG ou alguma implementação nova, por isso é bom você acessar o site http://coronalabs.com, ir em “download”  e verificar a versão que está disponível para download. Se ela for superior a sua, recomendo que seja feito o download e atualizada a versão.
	Como descubro a versão do meu Corona?
		No menu “Sobre” você vai ter uma janela como essa que irá informar a versão que você possui.

* Use um bom editor

	Quando comecei a desenvolver com o corona SDK, tive vários problemas pra encontrar uma IDE boa pra trabalhar com o lua, como nenhuma delas na época me ajudava muito, e eu trabalhava no windows, eu usava o notepad mesmo, na pura brutalidade, depois de um bom tempo desenvolvendo sem muita ajuda, foi lançado o [corona project manager](http://coronaprojectmanager.com) que agora mudou para [Outlaw Game Tools](http://outlawgametools.com/download), porem era pago e como desenvolvedor iniciante, eu só queria saber de ferramentas gratuitas
	depois de algum tempo migrei para o Mac e na mesma época conheci o editor chamado Sublime Text, demorei um tempo pra acreditar no potencial da ferramenta, porem, depois que você conhece, não quer mais largar :)

	Instalando o Sublime

	Se você ainda não tem o sublime, vc pode baixar em http://www.sublimetext.com/3, o aplicativo também é pago, porem a versão trial dele nunca expira :)
	E quais as vantagens do sublime? 
	Agora que o bicho pega, o sublime tem varias opções que ajudam você a desenvolver, não só com o corona, mas com o que você quiser ;)
	Certo, você instalou o sublime e agora precisa dos auxiliares para o corona e pra linguagem lua. O que temos pra isso? bom, temos o Corona Editor.
	o Corona Editor é um pacote que você instala no Sublime que vai te ajudar, e muito.
	pra fazer isso você precisa instalar o Package control, pra isso, siga os seguintes passos.

	Instalando o Corona Editor

	Vá em no menu Tools, Command Pallet e faça uma busca por Package Control: Install package, vai abrir uma nova janela, nela, você deve procurar por Corona Editor, depois de instalado, reinicie seu sublime e o menu corona editor vai aparecer. se você não possui o Package Control instalado, você precisa acessar https://sublime.wbond.net/installation e seguir as instruções
	Agora que está tudo certo, de uma explorada no novo menu e conheça as opções que ele da pra você e as facilidades que ele cria
		


* Crie seu primeiro projeto de maneira simples

	Se você está começando com o corona e não conhece absolutamente nada, indico que ao criar um novo projeto no coronaSDK, você escolha a opção de criar um projeto em branco (“Blank”).
	Pra quem já teve algum contato com o corona vai achar estranho essa indicação, sendo que é possível criar um novo projeto pela opção ‘’Game” , que vai trazer um projeto com algumas configurações iniciais pronta e com a estrutura de redirecionamento de telas já explicada, porem, esse modelo também traz muito código pronto, que pra quem nunca trabalhou com o corona vai se tornar difícil entender.
	Comece com um projeto em branco e vá pesquisando passo a passo naquilo que você precisa. Com certeza é uma opção mais trabalhosa, porem quando você já entender os principais passos tudo vai fazer sentido e nos próximos você já vai poder pular esse trabalho todo.


* Testes

	Antes de publicar seu jogo, teste ele, mas não apenas uma vez, não apenas com o que se deve fazer, teste seu jogo de todas as maneiras possíveis. Envie ele para seus amigos, peça o feedback deles, tente coisas que não foram planejadas, fazendo esses passos você com certeza irá descobrir pontos fracos em seus jogos e entenderá melhor o que deve ser feito para facilitar a vida do jogador, pois seus amigos vão ajudar indicando o que mudar na jogabilidade, o que tornar mais difícil, o que tornar mais fácil, e varias dicas que poderão ajudar seu jogo a ficar ainda melhor antes de publicar


* Gere seu apk para android

	Hoje sem o android está presente na maioria dos telefones devido a grande quantidade de aparelhos que usa esse sistema operacional, e alem disso, o custo para iniciar o desenvolvimento para android é muito mais baixo do que para qualquer outra plataforma, ou seja, você vai iniciar com baixos custos e terá a chance de atingir muitas pessoas 

	Para comecar, vamos acessar o menu File

	![File](/images/2014-12-25-5-grandes-dicas-para-voce-iniciar-no-coronasdk/menu_file.png)

	Clique em Build e se você estiver usando a opção mais basica do CoronaSDK, você terá essas duas opções
	Selecione a opção Android.

	![Build](/images/2014-12-25-5-grandes-dicas-para-voce-iniciar-no-coronasdk/menu_build.png)

	Antes da proxima tela, uma janela pedindo para comprar o corona ou para passar os dados de sua compra irá aparecer, se você não quiser fazer nada disso, apenas clique em continue.

	![PopUp](/images/2014-12-25-5-grandes-dicas-para-voce-iniciar-no-coronasdk/corona_sdk_starter.png)
	
	Para finalizar, você deve preencher os dados da sua aplicação, e se você já tiver eu cadastro pronto no google, coloque sua chave, preenchar seus dados, os dados da versãodo seu jogo e lembre de sempre manter sua keystore, pois é com ela que você vai conseguir continuar atualizando seu jogo.
	Clique em BUILD e espere o jogo terminar de compilar, o APK vai estar na pasta que você selecionou em 'Save to Folder'

	![PopUp](/images/2014-12-25-5-grandes-dicas-para-voce-iniciar-no-coronasdk/build_for_android.png)
	




