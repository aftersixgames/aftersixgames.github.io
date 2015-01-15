---
layout: post
title: "CoronaSDK - Por que você não deve usar"
date: 2015-02-13 12:56:10 -0200
comments: true
author: mauriciokj
categories:
  - Desenvolvimento de Games
  - CoronaSDK
---

Pra você que gosta do CoronaSDK e ficou indignado com o titulo, não se assuste. Vou apenas expressar minha opinião como desenvolvedor, e é claro, espero que possamos conversar sobre isso nos comentários.
Bom, eu iniciei no mundo do desenvolvimento de jogos pelo corona, meu jogo mais baixado, o [SkateBoardAttack](https://play.google.com/store/apps/details?id=aftersixgames.com) foi todo desenvolvido com o corona, e por que agora eu resolvo dizer pra você não usar?
Inicialmente ele realmente é muito bom, a linguagem LUA ajuda os iniciantes por ser uma linguagem de fácil aprendizado, seu emulador é muito bom, e se tudo estiver configurado corretamente, sempre que você salvar uma modificação no seu game, o corona simulator vai reiniciar o jogo já com as mudanças aplicadas.
Porém, existem algumas coisas que foram extremamente ruins para mim.

<!-- more -->

## Organização 

Por padrão, o corona tem uma estrutura organizacional muito ruim. todos os arquivos estão no mesmo diretório, você não consegue mudar essas coisas com facilidade, não existe nenhum tipo de configuração padrão nem um tipo de padrão de projeto que seja condizente com as nossas necessidades como desenvolvedores. Tudo fica na mesma pasta.

## build.settings

Acredito que a maioria dos desenvolvedores, mesmo os mais antigos com o corona tenham problemas com o build.settings.
nesse arquivo você define todas as opções básicas para todos os tipos de dispositivos que você quer usar, define todas as permissões que você vai precisar, ícones pra cada tipo de plataforma, opções como a orientação que seu dispositivo vai ter para aquela aplicação, definições de plugins, etc.
Ou seja, tudo numa grande tripa de código e que até o momento onde eu estava escrevendo esse post, ainda não possuíam nenhum tipo de auxilio visual, o negócio é abrir o editor e meter a mão na massa.
	
## config.lua

Outro arquivara configurações do seu jogo, aqui você define a escala pra ele e dependendo do jogo se ele vai fazer “Push notifications”, até agora a única coisa que vi que é gerada automaticamente, porém a gerencia disso poderia ser mais fácil.O arquivo é gerado sozinho quando você cria um novo jogo com as definições de “content” sendo colocadas ali sozinhas, porém, qualquer modificação que vc precise fazer, ou que o jogo precise, deve ser feita na mão.

## Atualizações 

Ta, pera ai, isso não é realmente uma coisa ruim, foi só uma experiência ruim que eu tive.
Em uma das atualizações do Corona, meu jogo ficou todo quebrado, levei algum tempo pra arrumar, mas claro, depois ficou muito melhor
se eu tivesse uma maneira melhor de organizar as coisas, tenho certeza que isso não teria acontecido.

## Concluindo
Esses foram os problemas que eu vi para se trabalhar com o corona, ainda acredito que seja uma das melhores plataformas para se iniciar, porém, algumas coisas ainda devem ser melhoradas.
Se você discorda, teve problemas parecidos ou ainda teve outros tipos de problemas, deixe nos comentários
e se puder conheça nossos jogos desenvolvidos com o corona, abraços a todos e até a próxima.

[SkateBoardAttack](https://play.google.com/store/apps/details?id=aftersixgames.com) - Jogo onde o personagem principal é um android que anda de skate e destroi maças e janelas.

[EnDroid - Enduro Race](https://play.google.com/store/apps/details?id=com.aftersixapps.endroid) - Jogo onde o objetivo é você ultrapassar todos os carros sem bater.

[Get the pigeon](https://play.google.com/store/apps/details?id=aftersixgames.gtp.com) - Jogo onde o personagem principal é o gato que aparece em nosso outro jogo, o [Pigeon Simulator](https://play.google.com/store/apps/details?id=com.aftersixgames.pigeonsimulator) que está sendo desenvolvido no Unity 3D.