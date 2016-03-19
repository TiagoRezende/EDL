###Introdução

_Swift_ é uma recente linguagem de programação desenvolvida com o principal objetivo de servir programadores que pretendem
desenvolver aplicativos e programas para _iOS_, _OS X_, _watchOS_, _tvOS_ (todos esses pertencentes _Apple_) e _Linux_.

###Origens e influências

O projeto de criação da linguagem _Swift_ foi desenvolvido por programadores da _Apple_, liderados por _Chris Lattner_.
Teve início em _2010_, sendo lançado em _2014_ sua primeira versão oficial. E mais tarde recebendo versões em _2015_ e em _2016_. 
Desenvolvido principalmente como uma alternativa ao _Objetive-C_, com uma escrita mais simples e um poder maior de expressão 
entre outras otimizações, apesar de possuir similaridades a _C_ e _Objective-C_. _Swift_ foi projetada para trabalhar com os 
frameworks da _Apple_,  _Cocoa_ e _Cocoa Touch_, e com códigos em _Objective-C_.
Foi influenciada por várias linguagens, principalmente:  _C_, _C#_,  _Objective-C_, _D_ , _Haskell_, _Python_,  _Ruby_ e _Rust_. 
A seguir uma breve linha do tempo para ilustrar suas influências.

>1972 - C

>1983 - Objective-C

>1990 - Haskell 

>1991 - Python

>1995 - Ruby

>2000 - C# 

>2001 - D

>2010 - Rust

>2014 - Swift

###Classificação

Swift é uma linguagem compilada e multi-paradigma, sendo:

>Imperativa

>Funcional

>Orientada a Objetos

Quanto a tipagem:

>Forte

>Estática

>Inferida

###Avaliacão Comparativa

#####>Leitura (readability)

Por possuir muitas classes, bibliotecas e paradigmas diferentes, a leitura de programas se torna mais difícil, embora isso dependa
do programa. Semelhante ao que acontece em Java. Por outro lado C e Python possuem uma leitura mais compreensível. 

#####>Escrita (writability)

A escrita é mais dinâmica e fácil de ser desenvolvida como em Java e Python ( possuem similaridades na parte orientada a objetos). 
A tipagem inferida e forte contribui para um código mais enxuto e fácil de escrever. Devido a restrições da linguagem, C tem uma 
escrita mais difícil em comparação com Swift.

#####>Expressividade

É uma linguagem com alto poder de expressão. É possível transcrever o código de outras linguagens para Swift sem alterar muito o código
ou até simplificando, permitindo em uma leitura mais legível. (Exemplos de comparação da expresividade nos slides.)

###Exemplo de Código 

Trecho do código do jogo FlappySwift, uma implementação de FlappyBird para iOS 8:

override func touchesBegan(touches: Set<UITouch>, withEvent event: UIEvent?) {

     /* Called when a touch begins*/
     if moving.speed > 0 {
        for touch: AnyObject in touches {
           let location = touch.locationInNode(self)
           bird.physicsBody?.velocity = CGVector(dx: 0, dy: 0)
           bird.physicsBody?.applyImpulse(CGVector(dx: 0, dy: 30))
        }
     } else if canRestart {
        self.resetScene()
     }
}  

Escolhi esse código pois pertence a um jogo conhecido no mundo todo. Certamente alguns colegas devem ter o jogo em seus celulares.
Assim, posso mostrar uma aplicação direta da linguagem Swift, mostrando sua utilidade no contexto da criação de softwares para iOS. 

O trecho trata de eventos de toque na tela do jogo. Quando alguem tocar na tela, o pássaro controlado pelo jogador deve ter sua
velocidade e seu impulso alterados para assim poder continuar desviando dos obstaculos. Para isso, alguns atributos do objeto
passaro devem ser alterados e alguns métodos chamados para tanto.
###Bibliografia

Wikipedia:

https://en.wikipedia.org/wiki/Swift_(programming_language)

Swift, site oficial:

https://swift.org/

Github, código do jogo completo:

https://github.com/fullstackio/FlappySwift
