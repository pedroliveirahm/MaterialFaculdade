### Sumário
* [C++](#c)
* [C](#c-1)


# Paradigmas da Programação
* Imperativo - máquina de turing
     * Davam comandos de passo a passo do que a máquina teria que fazer
     * Geravam códigos muito grandes, logo, era um código de difícil manuntenção
* Procedural - aqui surge as funções/métodos, o que diminui o tamanho do código
* Estrutural - surgue condicionais, loops, diminuindo mais ainda o tamanho do código
* Orientado a objetos - trazer o mundo real para a programação, aqui surge as classes e os conceitos de objeto (polimorfismo, herança, encapsulamento)
# Paradigmas Declarativos
* Se preocupam em como fazer, e não como foi feito
* Programação Funcional - surgiu para ser mais rápida que a p.o.o
* Programação Lógica
* Linguagens de marcação
     * HTML, XML, SQL
# C++
* Linguagem multiparadigma
     * Paradigma da programação procedural
          * Tudo que está dentro da função main vai ser executada de forma sequêncial
     * Paradigma da programação orientada a objetos
## Variáveis
### Tipagem
* Estática - é preciso atribuir o tipo primitivo de dado à variável
### Tipos Primitivos
* Também conhecidos como tipos de dados
* Armazenam só 1 valor por variável, por isso são chamados de tipos de dados simples
* `string` nome = "Pedro";
     * è necessário incluir biblioteca
     ```bash
     #include <string>
     ```
* `int` numeroInteiro = 10;
* `float` numeroFlutuante1 = 1.6235; 
     * precisão de +- 6 casas decimais;
* `double` numeroFlutuante2 = 1.6235; 
     * precisão de +- 10 casas decimais;
* `char` sexo = 'M';
* `bool` escolha = true;
### Boas Práticas
* Recomenda-se que a declaração de variáveis sejam as primeiras intruções da função 
## Entrada e Saída de Dados
* Incluir biblioteca :
```bash
#include <iostream>
using namespace std;
```
### Saída
* Função : `cout` <<;
```bash
#include <iostream>
using namespace std;

int main() {
     cout << "Olá mundo !";
}
```
### Entrada
* Função : `cin` >>;
```bash
#include <iostream>
#include <string>
using namespace std;

int main() {
     string nome;

     cout << "Escreva seu nome : ";
     cin >> nome;

     cout << "Seu nome é : " << nome;
}
```
## Condicionais
* if...else if...else
* switch() {case : ;}
## Laços de Repetição
* for
* while
* do...while
# C
## Entrada e Saída de Dados
* Incluir biblioteca :
```bash
#include <stdio.h>
```
### Saída de Dados
* Função : `printf();`
* Sintaxe : `prinft("string de controle", arg1,arg2,...);`
* Na string de controle do prinft() pode conter :
     * texto
     * códigos especiais
          * \n - pular linha
          * \t - tab
     * formatos - relacionados aos argumentos
```bash
#include <stdio.h>

int main() {
     printf("Olá mundo !");
}
```
### Entrada de Dados
* Função : `scanf();`
* Sintaxe : scanf(`"string de controle"`, `&variável`);
* Na string de controle do scanf() pode conter : 
     * formatos
```bash
#include <stdio.h>

int main() {
     char nome[15];

     printf("Digite seu nome : ");
     scanf("%s", nome);

     printf("Seu nome é : %s", nome);
}
```
* Não se deve utilizar o `&` com `vetores` - os colchetes indicam vetores
     ```bash
     char nome[15];
     
     scanf("%s", nome);
     ```
## Variáveis
* Variável Global
* Variável de Parâmetro
* Variável Local
### Tipagem
* Estática
### Tipos Primitivos
* Também conhecidos como tipos de dados
* Armazenam só 1 valor por variável, por isso são chamados de tipos de dados simples
* `char` - formato `%c`
     ```bash
     char letra = 'P';
     ```
     * string - formato `%s`
          ```bash
          char nome[] = "Pedro";
          ```
          * È possível específicar o número de caracteres no [ ] da variável `nome`
* `int` - formato `%d`
     ```bash
     int numeroInteiro = 10;
     ```
* `float \ double` - formato `%f`
     ```bash
     float numeroFlutuante1 = 10.222;
     double numeroFlutuante2 = 10.2222222;
     ```
* void - não possui valor
     * utilizado para indicar que uma função não possui valor
### Onde Declarar
```bash
#include <stdio.h>

int resultado; // variável global

int multiplicacao (int n1, int n2) { # variáveis de parâmetro
     int produto; # variável local
     
     produto = n1 * n2;
     return produto; # funções de tipo primitivo requerem um retorno
} 

int main() {
     resultado = multiplicacao(10, 500);
     printf("%d", resultado);
}
```
### Qualificadores
* Na declaração, precedem o tipo primitivo
     * `short`
     * `long`
     * `unsigned`
     * `signed` - default
```bash
unsigned int valor;
```
* C permite que o programa defina se uma variável de tipo numérico deva ou não reservar o bit de sinal (números negativos)
```bash
unsigned int; # não reserva o bit de sinal
signed int; # reserva o bit de sinal
```
* Se nenhum modificador for indicado, por default, o compilador C reservará o bit de sinal
## Constantes
* È semelhante a uma variável, exceto que seu valor armazenado é imutável(constante)
```bash
#include <stdio.h>

int main() {
     const int i = 10;
     prinft("%d", i);
}
```
```bash
#include <stdio.h>

int main() {
     const int i = 10;
     i = 20;
     printf("%d", i);
}
$ERROR
```
## Diretiva de Pré-Processamento
* No pré-processamento ocorre a substituição
```bash
#include <stdio.h>
#define pi 3.1416   // diretiva

int main() {
     float raio; 
     printf("Para que possa ser calculado a área e o comprimento do círculo, informe o raio : ");
     scanf("%f", &raio);
    
     float area = pi * raio * raio, comp = 2 * pi * raio;
     printf("O círculo possui área e comprimento de, respectivamente, %.2f e %.2f", area, comp);
}
```
## Função `fgets`
* Específica para leitura de string ao invés do scanf()
* Sintaxe : fgets(variável,número-max-de-caracteres, stdin);
```bash
#include <stdio.h>

int main() {
char nome[15];

printf("Escreva seu nome : ");
fgets(nome, 15, stdin);

printf("Seu nome é : %s", nome);
}
```
## Arrays - Vetores
* È um `tipo de dado estruturado` que permite armazenar vários dados|elementos de um mesmo primitivo em uma variável, que, neste caso, será chamada de array
     * A quantidade de dados são conhecidas como `length`(tamanho) ou posições
     * E cada dado pode ser acessado por um índice
     * A contagem de índices começa do 0...(tamanho - 1)
### Sintaxe
```bash
<tipo-prmitivo> <nome-vetor>[tamanho] = {dado1, dado2,...};
```
* Caso não se especificar o tamanho máximo do array, ao atribuir, o compilador irá alocar o espaço suficiente para armazenar todos os valores
```bash
int numeros[5] {40, 60, 50, 30, 40}
```
```bash
int numeros {4, 7, 12, 52}
```
```bash
#include <iostream>
#define qtdAlunos 20

int main() {
     float nota[qtdAlunos], soma;

     for (int i = 0; i < qtdAlunos; i++) {
          printf("");
          scanf("f", &nota[i]);
          soma = soma + nota[i];
     }
     printf("Média da disciplina = %f", soma);
}
```
## Matrizes
* È uma estrutura de dados homogênea, a qual cada elemento pode ser acessada por dois índices
     * Dividida em `colunas`(eixo y) e `linhas`(eixo x)
     * A contagem dos índices vai de 0...(tamanhoColunas - 1)
### Sintaxe
```bash
<tipo-primitivo> <nome-matriz>[tamanhoColunas][tamanhoLinhas];
```
```bash
int numeros[3][5] {1,2,3,4,5} {1,2,3,4,5} {1,2,3,4,5};
```
* Foram alocadas 3 colunas, as quais acoplam 5 linhas
