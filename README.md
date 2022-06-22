# Dio Projeto de Animações Front-End
## HTML e CSS

## Sumário 
* [KeyFrames](#keyframes)
* [Animations](#animations)
* [Positions](#positions)
* [Transform](#transform)
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
### Transform
### Before
