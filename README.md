# Algoritmo_de_ordenacao

#HEAP_SORT
  Este algoritmo de ordenação é baseado na estrutura de dados HEAP, que nada mais é do que um vetor (X) que pode ser visto como uma árvore binária completa, onde cada nó possui no máximo 2 filhos. Cada vértice da árvore corresponde a um elemento do vetor. A árvore é completamente preenchida exeto no último nível. Cada nível é sempre preenchido da direita para a esquerda. Além disso, num HEAP, para todo vértice i diferente da raiz, a seguinte propriedade deve ser válida: X[PAI(I)] > X[I]].
  Dado um índece (i) do valor, para se descobrir as posições em que se encontram o seu pai, o filho esquerdo e o direito, para se descobrir as posições em que se encontram o seu pai, o filho esquerdo e o direito, realizam-se os cálculos: PAI(I) = I / 2, FILHO ESQUERDO(I) = 2 * I E FILHO DIREITO(I) = 2*I + I. 
  
  Para ordenar o vetor de entrada X, inicialmente transforma-se o vetor num HEAP, utiliando o procedimento heap_fica. O procedimento heap_fica analisa se um determinado elemento da posição J atende a propriedade. Caso não atenda, o maior de seus filhos é trocando com o pai J que não atende a propriedade HEAP, e o processo continua até levar o elelemto j a uma folha out até que a propriedade seja satsfeito.
  
  Após ter transformado o vetor em um HEAP, passa-se para a etapa em que a ordenaçáo é realizada de fato. Com HEAP sendo um vetor, o maior elemento ficará na raiz(OU PRIMEIRA POSIÇÃO DO VETOR), então o primeiro elemento pode ser trocado com o último de maneira que ocupará a posição correta dentro do vetor que está sendo ordenado, visto que quem estã na raiz é o maior elemento e deve ficar na última posição após a ordenação. Após feita a troca, descnsidera-se esse último elemento e aplica-se o método heap_fica novamente sobre a raiz, que agora deixou de atender á propriedade HEAP. Dessa forma, após aplicação do método, ẽ novamente obtido o maior elemento na raiz da árvore, e pode ser feito o mesmo processo de troca com o penúltimo elemento. O processo continua até a árvore permanecer de forma crescente.
