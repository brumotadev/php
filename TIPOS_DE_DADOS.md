# Tipos de Dados PHP

### Tipos de Dados Primitivos
- Integer: armazena números interios
- Float: armazena números com casas decimais
- String: armazena caracteres
- Boolean: armazena um valor verdadeiro ou falso (true or false)
- Null: valores nulos (ausência de valor)

### Mixed e Never

- Mixed(PHP 8.0): Representa qualquer tipo de dado
- Never(PHP 8.1): Representa um tipo de retorno que nunca ocorre 

### Callback(callable)

- É uma função que é passada como argumento para outra função, permitindo que a função chamada execute a função callback em algum momento durante sua execução.
- Sendo usadas em situações onde você deseja permitir que uma função aceite uma função personalizada para manipular ou processar dados de uma maneira específica.
- Tipos de Callbacks em PHP: Funções Simples, Funções Anônimas(closures), Métodos de Objetos, Métodos Estáticos.

### Resource

- É um tipo especial de dado que representa uma referência para recursos externos, como conexões com bancos de dados, streams de arquivos, conexões de rede, entre outros.
- Esses recursos não são tipos de dados comuns como inteiros ou strings; em vez disso, são identificadores que apontam para recursos gerenciados pelo sistema, que PHP gerencia internamente.
- Não pode ser criado diretamente pelo usuário. Ele é gerado por funções internas do PHP que interagem com recursos externos.


### Iterable(PHP 7.1)

- Pode ser qualquer estrutura de dados que pode ser percorrida por um loop(como "foreach")
- É um pseudo-tipo que engloba tanto arrays quanto objetos que implementam a interface "Traversable"
- Arrays em PHP são iteráveis(iterable) nativamente
- Objetos que implementam "traversable": qualquer objeto que implementa a interface ```Traversable``` (ou umas das suas subinterfaces como ```Iterator``` ou ```Generator```) também é considerado um ```Iterable```.
- O tipo Iterable é útil quando você deseja criar funções que podem aceitar qualquer tipo de coleção de dados iterável, proporcionando mais flexibilidade.

### Arrays

- Arrays em PHP são um dos tipos de dados mais utilizados e versáteis.
- Permiti armazenar múltiplos valores em uma única variável. 
- Eles são essencialmente coleções ordenadas de pares chave-valor, onde cada valor pode ser acessado por uma chave única.
- <i>Existem os seguintes tipos de Arrays em PHP:</i>
    - <b>Arrays Indexados:</b> 
        - As chaves são números interiso começando do indice 0
        - Usado para listar valores
        ```php
        <?php

        $fruits = ["Apple", "Banana", "Orange"];
        echo $fruits[0]; // Saída: Apple

        ?>
        ``` 
    - <b>Arrays Associativos:</b>
        - As chaves são strings ou inteiros, e não precisam ser sequenciais.
        - Usado para associar pares de valores, como em um dicionário.
        ```php
        <?php

        $person = [
        "name" => "Bruno",
        "age" => 30,
        "city" => "São Paulo"
        ];
        echo $person["name"]; // Saída: Bruno

        ?>
        ``` 
    - <b>Arrays Multidimensionais:</b>
        - Arrays que contém outros arrays como elementos
        - Podem ser usados para armazenar tabelas de dados ou estruturas complexas
        ```php
        <?php

        $matriz = [
            [1, 2, 3],
            [4, 5, 6],
            [7, 8, 9]
        ];
        
        echo $matriz[1][2]; // Saída: 6

        ?>
        ``` 