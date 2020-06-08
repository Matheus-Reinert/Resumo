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


