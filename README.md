# Dio Projeto de Animações Front-End
## HTML e CSS

## Sumário 
* [KeyFrames](#keyframes)
* [Animations](#animations)
* [Positions](#positions)
* [Transitions](#transitions)
* [Before](#before) 


### KeyFrames
Define uma sequencia de passos (do início ao fim) a serem seguidos em um intervalo, para criar uma animação. 
```
@keyframes backgroudTransition {
  0% {
    background-position: 0% 80%;
  }

  50% {
    background-position: 80% 100%;
  }

  100% {
    background-position: 0% 90%;
  }
}
```

### Animations
Define o timing de uma animação (keyframe) como tempo de início, entrada e saída, delay, etc
Propriedades:
animation-name: Nome da animação (@keyframes)
animation-duration: O tempo de duração do ciclo de animação
animation-timing-function: Define como as transições se comportam.
animation-delay: Define o delay entre o elemento ser carregado e a animação iniciar.
animation-iteration-count: O número de vezes que a animação se repete, podendo ser infinito.
animation-direction: Define se a animação deve alternar a direção a cada execução ou voltar ao início e repetir a si mesma.
animation-fill-mode: Define quais valores são aplicados por animação antes e depois da execução.
animation-play-state: Permite a pausa de uma sequencia

```
  /* nome da animação | duração | timing-funcion*/
  animation: backgroudTransition 8s ease-in-out infinite;

```


### Positions
Define a posição de um elemento na tela. 
Static: Posicionado no canto superior esquerdo e segue o fluxo dos outros elementos. Não aceita as propriedades auxiliares (top | botton | left | right).
Fixed: Faz com que o elemento não se mova na tela mesmo que uma página tenha rolamento (botão send to top, whatsapp). Aceita as propriedades auxiliares.
Sticky: Literalmente colado, faz com que o elemento fique fixo em relação ao **rolamento da página**. É utilizado com as propriedades auxiliares pois precisa de um posicionamento de referência.
Relative: Altera a posição de um elemento tendo como referência **sua posição inicial**. Assim, sua posição só se altera quando aplicadas as propriedades auxiliares.
Absolute: Possui 2 comportamentos:

1- O elemento possui um elemento pai com um position *diferente* de static: O elemento filho recebe as propriedades auxiliares e se posiçiona em relação ao **elemento pai** 
Ex:
```
.pai{
  width:100px;
  height:100px;
  background-color:red;
  position: relative;
  top:50px;
  left:50px;
}

.filho{
  width:50px;
  height:50px;
  background-color:blue;
  position:absolute;
  top:50px;
  left:50px
}

```
O elemento filho acumulará 100px do topo e 100px da esquerda da tela, pois está posicionado em relação ao pai.

2- O elemento filho *não possui* um elemento pai com position diferente de static (confuso, mas vc pega ;) ): O elemento filho com position absolute se posiciona em relação á tela.
Ex:
```
.pai{
  width:100px;
  height:100px;
  background-color:red;
  top:50px;
  left:50px;
}

.filho{
  width:50px;
  height:50px;
  background-color:blue;
  position:absolute;
  top:50px;
  left:50px
}

```

O filho seria posicionado a 50px do topo e da esquerda da tela e não em relação ao elemento pai.

[Artigo incrível do Dev Luan Alves explicando o assunto](https://www.alura.com.br/artigos/entenda-a-propriedade-position-css)


### Transitions
Permite alterar os valores das propriedades do elemento, controlando o tempo e a forma das alterações

Propriedades [w3schools](https://www.w3schools.com/css/css3_transitions.asp):
transition	A shorthand property for setting the four transition properties into a single property
transition-delay	Specifies a delay (in seconds) for the transition effect
transition-duration	Specifies how many seconds or milliseconds a transition effect takes to complete
transition-property	Specifies the name of the CSS property the transition effect is for
transition-timing-function	Specifies the speed curve of the transition effect


### Before
Before e After criam um pseudo-elemento antes e depois do elemento principal, respectivamente. É muito utilizado na estilização e melhora da UI. Na aula a professora utilizou o before para criar um efeito de abertura com margens, definindo o before com position:absolute, margin:#ffffff e opacity:0, para que quando fosse disparado o evento :hover, a margem expandisse e se formasse um efeito de abertura.
