### Java
* [Variáveis](#variáveis)
* [Entrada e Saída de Dados](#entrada-e-saída-de-dados)
* [Condicionais](#condicionais)
* [Laços de Repetição](#laços-de-repetição)
* [Classe](#classe)
* [Funções](#funções)
* [Modificadores de Acesso](#modificadores-de-acesso)
* [Arrays](#arrays)
### Programação Orienta a Objetos
[Principais Conceitos](#principais-conceitos)

# Java
* Dispõe do paradigma da programação orientado a objetos
## Variáveis
### Tipagem
* Estática - é preciso atribuir o tipo primitivo a variável
### Tipos Primitivos
* `int`
* `float`
* `double`
* `char`
* `boolean`
## Entrada e Saída de Dados
### Saída
* Classe : `PrintStream` <nome-variável> = new PrintStream(System.in);
```bash
PrintStream sysout = new PrintStream(System.out);
sysout.println("Hello World");
```
* O nome da variável é a desejar
### Entrada
* Classe : `Scanner` <nome-variável> = new Scanner(System.in);
```bash
String nome;
int idade;

Scanner sysin = new Scanner(System.in);
nome = sysin.nextLine(); # método que transforma o input em String
idade = sysin.netxInt(); # método que transforma o input em int
```
## Condicionais
* `If{}...Else if{}...Else{]`
* `Switch{Case : }`
## Laços de Repetição
* `For`
* `While`
* `Do...While`
## Classe
* Uma classe é um elemento do código que é utilizada para `representar` objetos do mundo real
* Dentro dela é declarado `atributos` e `métodos`, que representram, respectivamente, as características e comportamentos do objeto.
### Sintaxe
* Palavra reservada `class`
  * public class `NomeClasse` {}
```bash
class NomeClasse {
    // local onde os atributos, construtores e métodos são criados
}
```
## Funções
* Conhecido, também, como métodos
* Principal objetivo das funções é encapsular ações e reutilizar o código
### Sintaxe
* `void` verboSubstantivo(<parâmetros>) {}
  * função void é uma função que não tem retorno
```bash
void ligar(String remetente){
  System.out.format("Ligando para %s...", remetente);
}
```
```bash
String marca = "Iphone", cor = "Ciano";
int armazenamento = 256;

void descreverCelular() {
  System.out.format("O %s possui as seguintes características : \ncor %s\narmazenamento de %dgb", this.marca, this.cor, this.armazenamento);
}
```
## Modificadores de Acesso 
* Por meio dele informamos a visibilidade da classe, atributos e métodos :
    * Public
    * Private
    * Default - não colocar nenhum modificador
```bash
public class Produto {

  private String nome; # atributo1
  private int quantidade;  # atributo2

  public Produto() { # Método construtor
    // Construtores
  }

  public void apresentarProduto() {
    // Métodos
  }

}
```
* Os atributos de uma classe, por boa prática, deve ser colocado como private, evitando a confusão do uso de variáveis globais
  * Caso precise altera-los, usam-se os métodos getters e setters

## Objeto
### Instanciar uma Classe
* Instanciar uma classe é criar um novo objeto
* Um objeto nada mais é do que uma variável do tipo classe
### Sintaxe
* Classe <nome-variável> = new Classe();
* O objeto terá todos os atributos e métodos da classe 
```bash
Produto caneta = new Produto(); # instanciação de uma classe

caneta.apresentarProduto(); # chamada de um método presente na classe Produto
```
* A variável caneta foi definida como sendo do tipo Produto. Em seguida, com a palavra reservada `new`, um espaço é criado na memória para armazenar um novo objeto do tipo Produto. 
* O construtor `Produto()` especifica como o objeto deve ser criado.
* Na segunda linha de código, através do objeto, é realizado a chamada do método `apresentarProduto()`.
## Arrays (Vetores)
* È um `tipo de dado estruturado` que permite armazenar vários dados|elementos de um mesmo primitivo em uma variável, que, neste caso, será chamada de array
     * A quantidade de dados são conhecidas como `length`(tamanho) ou posições
     * E cada dado pode ser acessado por um índice
     * A contagem de índices começa do 0...(tamanho - 1)
### Wrapper Class
* Uma classe que representa um tipo primitivo
* int -> Integer
* float -> Float
* double -> Double
* char -> Character
* -> String
### Array Estático
* Array = Array Estático
#### Como Declarar :
* <tipo-primitivo/wrapper-class>[] <nome-array> = new <tipo-primitivo/wrapper-class>[x];
    * x é quantidade máxima de índices armazenáveis naquele array
```bash
String[] nomes = new String[3];
nome[0] = "Zé";
nome[1] = "Lé";
nome[2] = "Cleitinho";
```
```bash
for(int i = 0; i < nomes.length; i++) {
    System.out.println(nomes[i]);
}
```
### Array Dinâmico
* ArrayList = Array Dinâmico
    * È uma classe do JDK
    * Só aceita Wrapper Class
#### Como Declarar : 
* ArrayList<wrapper-class> <nome-arrayList> = new ArrayList<wrapper-class>();
```bash
ArrayList<String> nomes = new ArrayList<String>();
nomes.add("Marquinhos"); # automaticamente índice 0 
nomes.add("Luquinhas"); # automaticamente índice 1
nomes.add("Aninha"); # automaticamente índice 2
```
* `.add` é um método públic, sendo a string, neste caso, um argumento
* e a contagem de índices é predefinida(default)
#### Métodos
* `.add(value)` -> adicionar
```bash
    $Exemplo
ArrayList<Integer> numeros = new ArrayList<Integer>();
numeros.add(2);
numeros.add(1);
numeros.add(-2);
numeros.add(0);
numeros.add(-1);
```
* `size()` -> tamanho, função semelhante ao `.length`
```
System.out.println("O array possui tamanho de : " + numeros.size());
```
* `.get(index)` -> pegar
```bash
for (int i = 0; i < numeros.size(); i++) {
    System.out.println(numeros.get(i));
}
```
* `.remove(index)` -> remover
```bash
System.out.println("Imprimindo a sequência exceto o número 0" + numeros.remove(3));
for (int i = 0; i < numeros.size(); i ++) {
    System.out.println(numeros.get(i));
}
```
`.sort(nome-arrayList)` -> ordenar
```bash
Collections.sort(numeros);

for (int i = 0; i < numeros.size(); i ++) {
    System.out.println(numeros.get(i));
}
# -2, -1, 0, 1, 2 
```
## Foreach
* For() específico para arrays
* For (<wrapper-class> <nome-variável> : <array>) {}
    * <nome-variável> vai representar cada índice dentro do array
### Array Estático
```bash
int soma = 0;

Integer[] numeros = new Integer[4];
numeros[0] = 925;
numeros[1] = -291;
numeros[2] = -1050;
numeros[3] = 845;

for (Integer numero : numeros) {
     soma += numero;
}
System.out.println(soma);
```
### Array Dinâmico
```bash
ArrayList<String> nomes = new ArrayList<String>();
nomes.add("Sere");
nomes.add("Lepe");

for (String nome : nomes) {
    System.out.println(nome);
}
```
# Orientação a Objetos em Java
## Principais conceitos
  * [Abstração](#abstração)
  * [Encapsulamento](#encapsulamento)  
  * [Herança](#herança)
  * [Polimorfismo](#polimorfismo)
## Abstração
* ...
## Encapsulamento
* Envolve as funções|métodos presentes na classe
```bash
public void acelerar() {

}
```
* Para acelerar um carro, não é necessário saber o todo que envolve a aceleração do carro, apenas que é necessário pisar no pedal
## Herança
* Quando uma classe herda atributos e/ou métodos de outra classe
### Extends
* Quando uma classe precisa herdar características de outra classe, fazemos o uso de herança
```bash
public class MinhaClasse extends ClasseQualquer {

}
```
### Interface
* ...
### Polimorfismo
*
---
Made with by 💙 Pedro PC 👋 <a href="https://github.com/pedroliveirahm">Seen my GitHub</a>
* <strong>Fale comigo : <a href="https://bio.link/pedroliveirahm" target="_blank">Contato</a></strong>