<h1 align="center">Pré-processador SASS </h1>

``` css
    $variableName: value;
```
**Para adicionar uma variável**


``` css
    @import "fileName";
    
```

**Para importar arquivos, nota: criar arquivos com _ antes do nome ``` _base ``` para o sass não compilar**


``` css
    
    
    .container {

        $text-color2: rgb(0, 17, 255);

        color: white;

        p {
            color: $text-color2;
        }
    }
```

**Acessa os elementos filhos por meio de encadeiamento**
