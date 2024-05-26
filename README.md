# Angular v18: Native Fallback Content for ng-content
*April 26, 2024 | 9 Minute Read*

Quando construímos componentes Angular, muitas vezes precisamos de uma maneira de fornecer conteúdo alternativo para slots de conteúdo projetado usando o elemento `ng-content`. Anteriormente, havia algumas soluções alternativas para isso, mas nada ideal. Com a última versão do Angular, isso se tornou uma funcionalidade nativa. Neste post, vou mostrar exatamente como isso funciona. Vamos lá!

## Versão do Angular

**Importante**: O que será mostrado aqui requer Angular versão 18 ou superior. Se você estiver usando uma versão anterior, precisará atualizar antes de poder utilizar essas técnicas.


## Convertendo Atributos de String para Projeção de Conteúdo com ng-content

O primeiro passo é converter rótulos de atributos de string para projeção de conteúdo usando `ng-content`. Isso envolve atualizar o template do componente de botão para usar elementos `ng-content` com atributos `select`. Em vez de usar atributos para os rótulos, utilizamos agora projeção de conteúdo, onde os elementos são projetados dentro dos slots definidos pelo `ng-content`.

## Adicionando Conteúdo de Fallback em Regiões de ng-content

A parte mais interessante desta nova funcionalidade é a capacidade de adicionar conteúdo de fallback diretamente nos slots do `ng-content`. Isso significa que, se nenhum conteúdo for projetado para um slot específico, o conteúdo de fallback será exibido. Esse recurso é útil quando queremos ter valores padrão que serão utilizados na ausência de conteúdo projetado.

Por exemplo, podemos definir textos padrão para botões que serão exibidos caso nenhum conteúdo seja fornecido explicitamente.

## Conteúdo de Fallback Não Funciona com Slots Condicionais

Uma limitação importante a ser observada é que o conteúdo de fallback não será exibido se o slot for condicionado dinamicamente. Isso significa que, se o conteúdo projetado depender de uma condição que pode mudar durante a execução, o conteúdo de fallback não será aplicado quando a condição não for atendida.

## Conclusão

Com o Angular 18, temos uma maneira nativa de fornecer conteúdo de fallback para conteúdo projetado usando o elemento `ng-content`. Isso elimina a necessidade de lógica condicional complicada e facilita a criação de componentes reutilizáveis e robustos.

**Quer ver em ação?** Confira o código de demonstração e exemplos dessas técnicas no Stackblitz. Se você tiver alguma dúvida ou comentário, não hesite em deixar um comentário.
