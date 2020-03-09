# Estruturas ligadas

Um estudo acerca das estruturas ligadas pilha, fila e lista. Para verificar o uso de estruturas que fazem uso de array, veja o outro estudo clicando [aqui](https://github.com/Gwolner/tad-pilha-fila-lista).

Definição

A principal diferença entre uma estrutura com uso de array e uma estrutura ligada, é que esta ultima faz uso de ponteiros para tornar a inserção e remoção de dados abstratos mais coerente com a necessidade do sistema. Um array (vetor) precisa ter a quantidade de dados que irá comportar definida previamente, o que ocasiona dois problemas: ou se ocupa mais memória do que se precisa ao declarar array muito grande ou se, se o tamanho for pequeno, faltará espaço no vetor para armazenar alguns desses dados.

Para solucionar estes impasse usa-se estrutura ligada, onde o uso de ponteiros, manipulados corretamente, torna favorável o uso das estrutura pilha, fila ou lista, permitindo adicionar ou remover dados dinâmicamente.

## Funções X Ponteiros

Neste estudo usamos Javascript e, por se tratar de uma estrutura de alto nível, os ponteiros foram substituidos pela função No.

```js
function No(){
	var item;
	var proximoNo;
}
```

Ela apresenta as instâncias <b>item</b> e <b>proximoNo</b>. Item comporta o dado abstrato que se deseja manipular e proximoNo contém a referência para o nó seguinte, onde este comportará o item seguinte e assim por diante, até que o proximo nó aponte para <b>null</b>.

## Pilha X Fila X Lista

Das três estruturas de dados, pilha e fila se comportam conforme esperado, com a diferença de que se pode aumentar seu tamanho de forma dinâmica. O mesmo não ocorre quando se trata da listas encadeadas, pois devido sua maior flexibilidade de funcionamento em relação as demais, pode-se criar variações como <b>listas duplamente encadeadas</b>, <b>listas encadeadas circulares</b> e <b>listas circulares duplamente encadeadas</b>.

### Lista encadeada (Lista ligada)

Nenhuma novidade em relação a lista além da já mencionada flexibilidade de tamanho.

<img src="img/lista_encadeada.png" aling="center"> 

* Inserção

Para adicionar um dado é preciso que o novo nó aponte para o nó seguinte da posição que se deseja ocupar e, em seguida, que o nó anterior a esta passe a apontar o novo nó, fazendo assim com que o novo nó seja inserido entre os dois nós já existentes.

<img src="img/insere.png" aling="center">

* Remoção

O nó que se deseja remover possui um nó anterior e um nó seguinte. O nó anterior deve apontar para o nó seguinte e desassociar o nó que será removido. Este, por sua vez, deve desassociar-se do no seguinte, passando a ficar fora da lista.

<img src="img/remove.png" aling="center">

### Lista duplamente encadeada (Lista duplamente ligada)

É uma lista em que um nó não só aponta para o nó seguinte, como tambem para o nó anterior.

<img src="img/duplamente_encadeada.png" aling="center">

### Lista circular

Quando o último nó da lista aponta para o primeiro de modo que este aponte para o próximo e assim por diante até chegar novamente ao último, trata-se uma lista circular. Na lista circular, qualquer nó pode apontar para o seguinte de modo a retornar pra ele mesmo.

<img src="img/circular.png" aling="center">

### Lista circular duplamente encadeada (Lista circular ligada duplamente)

Como o nome sugere, possui um comportamento híbrido da lista circular e duplamente encadeada. Cada nó aponta para o seguinte e para o anterior ao mesmo tempo, sendo que o primeiro nó aponta para o último e para o segundo, enqaunto o último aponta para o penúltimo e para o primeiro.

<img src="img/circular_dupla.png" aling="center">
