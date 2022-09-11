<h1 align="center">Pré-processador SASS</h1>

<h1 align="center">Variáveis</h1>

``` css
    $variableName: value;
```
* Para adicionar uma variável

<h1 align="center">Imports</h1>

``` css

    @import "fileName";
    
```

* Para importar arquivos, nota: criar arquivos com _ antes do nome ``` _base ``` para o sass não compilar

<h1 align="center">Encadeiamento</h1>

``` css
    
    
    .container {

        $text-color2: rgb(0, 17, 255);

        color: white;

        p {
            color: $text-color2;
        }
    }
```

* Acessa os elementos filhos por meio de encadeiamento

<h1 align="center">Parece função, mas não é</h1>

``` css
    
    @mixin nomeDaFunção(){
        propriedade: value;
    }
        
```
* Declarar um bloco de código para uso futuro

``` css
    
    @include propriedade();
        
```

* Utilizar o bloco de código criado acima em um determinado elemento


<h1 align="center">Condicionais</h1>


``` css
    
    @mixin nomeDaFunção($val){
    @if $val == danger {
        color: red;
    }
    @else if $val == alert {
        color: yellow;
    }
    @else{
        color: black;
    }
}
        
```

* Se determinada condição bater, faz algo

<h1 align="center">Repetições</h1>

``` css
    
    @for $i from 1 through 5 {
    .text-#{$i} {
        font-size: 15px * $i;
    }
}
        
```
* Passa por cada elemento do html criando uma classe com número do index



``` css
    
    $colors: (color01: blue, color02: red, color03: green);

    @each $key, $color in $colors {
        .#{$color}-text { color: $color;}
    }
       
```


``` css
    
    $colors: (blue, red, green);

    @each $color in $colors {
        .#{$color}-text { color: $color;}
    }
       
```

``` css
    

    @each $color in (blue, red, green) {
        .#{$color}-text { color: $color;}
    }
       
```

* Os 3 modos estão corretos. Adiciona uma cor específica para cada posição no index 


<h1 align="center">Herança</h1>

``` css
    
    
    .flex {
        display: flex;
        justify-content:center;
        align-items: center;
    }
    
    
    body{
        @extends .flex;
    }
       
```

* ``` @extends ``` herda todos os atributos do elemento criado

