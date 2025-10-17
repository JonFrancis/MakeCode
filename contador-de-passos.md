# Contador de Passos

## Conte seus passos com o micro:bit! @unplugged

Transforme seu @boardname@ em um contador de passos. Vamos usar o sensor de movimento (acelerômetro) para identificar quando damos um passo com o micro:bit.

## {Variável}

Primeiro, precisamos criar uma variável para acompanhar o número de passos 🦶.

Em ``||variables:Variáveis||`` na Caixa de Ferramentas. Faça um nova variável e chame ela de **passos**

Arraste um bloco ``||variables:definir passos para 0||`` para dentro do bloco ``||basic:no iniciar||``.

```blocks
let passos = 0
```

## {Contando Passos}

Vamos registrar um passo sempre que o micro:bit for chacoalhado. 

Em ``||input:Entrada||``. Pegue um bloco ``||input:ao sacudir||``.

```blocks
input.onGesture(Gesture.Shake, function () {})
```

## {Contando Passos}

Em ``||variables:Variáveis||``. Pegue um bloco ``||variables:alterar passos||`` para dentro do bloco ``||input:em agitar||``. 

Agora, toda vez que sacudirmos o micro:bit (ou dermos um passo), vamos somar 1 ao valor da variável ``||variables:passos||``.

```blocks
let passos = 0
input.onGesture(Gesture.Shake, function () {
    passos += 1
})
```

## {Mostrando os passos}

Em ``||basic:Básico||``. Arraste um bloco ``||basic:mostrar número||`` abaixo do bloco ``||variables:mudar passos||``.

```blocks
let passos = 0
input.onGesture(Gesture.Shake, function () {
    passos += 1
    basic.showNumber(0)
})
```

## {Mostrando os passos}

Em ``||variables:Variáveis||``. Arraste um bloco ``||variables:passos||`` para dentro do bloco ``||basic:mostrar número||``, substituindo o número **0**.

```blocks
let passos = 0
input.onGesture(Gesture.Shake, function () {
    passos += 1
    basic.showNumber(passos)
})
```

## {Testando}

Conecte o @boardname@ ao computador e clique no botão ``|Baixar|``. Siga as instruções para transferir seu código para o @boardname@. Depois que o código for baixado, conecte o @boardname@ na bateria e ande por aí.