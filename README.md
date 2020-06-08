Alocação de memória

malloc();  /  #stdlib.h

Função malloc(memory allocation) aloca espaço para um bloco de memória RAM (= random access memory) do computador e devolve o endereço desse bloco.  O número de bytes é especificado no argumento da função. A seguir temos a alocção de 1 byte:

char *ptr;
ptr = malloc (1);
scanf ("%c", ptr);

malloc devolve um endereço genérico void*. No exemplo utilizando ptr, possui um endereço que é armazenado no mesmo, possui o tipo de ponteiro-para-char.  A transformação do ponteiro genérico em ponteiro-para-char é automática; não é necessário escrever ptr = (char *) malloc (1);.

Se for necessário alocar espaço para um objeto que precisa de mais que 1 byte, convém usar o operador sizeof, que diz quantos bytes o objeto em questão tem:

typedef struct {
   int dia, mes, ano; 
} data;
data *d;
d = malloc (sizeof (data));
d->dia = 31; d->mes = 12; d->ano = 2016;

Note que sizeof não é uma função mas um operador, tal como return, por exemplo. Os parênteses na expressão sizeof (data) são necessários porque data é um tipo-de-dados.  O operador sizeof também pode ser aplicado diretamente a uma variável:  se var é uma variável então  sizeof var  é o número de bytes ocupado por var.

-----------------------------------------------------------------------------------------------------

Listas

Listas são conjuntos de elementos, objetos, variáveis, tarefas, ou qualquer coisa que se possa enumerar e formar um conjunto. POdem ser implementadas de várias formas, mas de maneira geral podemos separar em duas principais: Arrays ou Encadeadas.

Array: é uma estrutura com posições fixas, cada elemento da lista deve ser colocado em uma posição no array;

Encadeadas: Listas encadeadas são estruturas de dados lineares e dinâmicas, a grande vantagem que elas possuem em relação ao uso de vetor é o fato de terem tamanho máximo relativamente infinito (o tamanho máximo é o da memória do computador), ao mesmo tempo que podem ter o tamanho mínimo de 1 elemento evitando o desperdício de memória.

-----------------------------------------------------------------------------------------------------

Pilhas 

Uma pilha é uma estrutura de dados que admite remoção de elementos e inserção de novos objetos.  Mais especificamente, uma  pilha (= stack)  é uma estrutura sujeita à seguinte regra de operação:  sempre que houver uma remoção, o elemento removido é o que está na estrutura há menos tempo.

Em outras palavras, o primeiro objeto a ser inserido na pilha é o último a ser removido. Essa política é conhecida pela sigla LIFO (= Last-In-First-Out).





