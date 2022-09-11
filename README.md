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
