# Pivot-Table

# Sobre
Pivot Table é uma biblioteca javascript drag'n drop   a demo esta disponível em  https://jhersonharyson.github.io/pivot-table/

# Créditos
Gerador de Tabelas Dinâmicas desenvolvido por [nicolaskruchten](https://github.com/nicolaskruchten/pivottable)
projeto original disponível em https://pivottable.js.org/

O projeto original está disponível sobre under an MIT license from CDNJS and NPM and Bower under the name pivottable. And on Packagist.org, it is nicolaskruchten/pivottable.


# Modo de Usar

* Importando arquivo: 

```javascript
function(){
            var derivers = $.pivotUtilities.derivers;

            var renderers = $.extend(
                $.pivotUtilities.renderers,
                $.pivotUtilities.c3_renderers,
                $.pivotUtilities.d3_renderers,
                $.pivotUtilities.export_renderers
                );

               $.getJSON("func.json", function(data) { // func.json é um arqivo.json
                      $("#output").pivotUI(data, {
                          renderers: renderers });
               })
           }
```

* Array de objeto javascript : 

```javascript
function(){
            data = [
                      {
                        nome: "Marcus", 
                        valor: 1.6
                      },
                      {
                        nome: "Pedro", 
                        valor: 53.0
                      }
                    ];
                    
            var derivers = $.pivotUtilities.derivers;

            var renderers = $.extend(
                $.pivotUtilities.renderers,
                $.pivotUtilities.c3_renderers,
                $.pivotUtilities.d3_renderers,
                $.pivotUtilities.export_renderers
                );

              
                $("#output").pivotUI(data, {
                    renderers: renderers });
            }
```
* Requisição ajax

```javascript
function(){
            var derivers = $.pivotUtilities.derivers;

            var renderers = $.extend(
                $.pivotUtilities.renderers,
                $.pivotUtilities.c3_renderers,
                $.pivotUtilities.d3_renderers,
                $.pivotUtilities.export_renderers
                );

               $.get( "api/servico/pega-json", function( data ) { // func.json é um arqivo.json
                      if(data)
                          $("#output").pivotUI(JSON.parse(data), { renderers: renderers });
               })
           }
```

# Usando atraves de um iframe
```javascript
 <iframe src="https://jhersonharyson.github.io/pivot-table/?resource=https://jsonplaceholder.typicode.com/todos&color=blue" style="border:0px; width: 100%; min-height: 800px"></iframe>
```
* o `src` recebe como query 2 parametros `resource` (url de obtenção de dados [.json]) e `color` onde os parametros `blue` e `green` referen-se respectivamente as cores `rgb(30,71,123)` e `rgb(77,157,76)` qualquer outra cor pode ser passada como parâmetro utilizando o padão `rgb()` ou `rgba()`
