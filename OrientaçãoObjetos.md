# Classe
* Uma classe é um elemento do código Java que é utilizada para `representar` objetos do mundo real.
* Dentro dela é declarado atributos e métodos, que representram,respectivamente, as características e comportamentos do objeto.

## Sintaxe
* Palavra reservada `class` seguida pelo nome da classe.
```bash
class NomeDaClasse {
    // local onde os atributos, construtores e métodos são criados
}
```
* Também é possível especificar o `modificador de acesso`. Por meio dele informamos a visibilidade da classe :
    * Public
    * Private
    * Default

```bash
public class Produto {

  private String nome; //atributo1
  private int quantidade; //atributo2

  public Produto() {
    // Construtores
  }

  public void apresentarProduto() {
    // Métodos
  }

}
```

## Como utilizar
* Da mesma maneira que se utiliza uma variável de tipo primitivo
* È declarado o tipo (neste caso o nome da classe) seguido pelo nome da variável.

```bash
Produto produtoUm;
produtoUm = new Produto();
produtoUm.apresentarProduto();
```
* A segunda linha deste código representa o processo de instanciação de uma classe. 

* Na linha anterior, a variável produtoUm foi definida como sendo do tipo Produto. Em seguida, com a palavra reservada `new`, um espaço é criado na memória para armazenar um novo objeto do tipo Produto. 
* O construtor Produto() especifica como o objeto deve ser criado. Por fim, uma referência a esse objeto é atribuída à variável produtoUm.
* Assim, através de produtoUm podemos acessar o objeto criado (e seus atributos e métodos). 
* Na terceira linha, por exemplo, utilizando a variável, acessamos o objeto e chamamos o método apresentarProduto().
* definir a variável que conterá sua referência normalmente é declarado em apenas uma linha.

```bash
Produto produtoUm = new Produto();
```

## Extends
* Quando uma classe precisa herdar características de outra, fazemos o uso de herança

```bash
public class MinhaClasse extends ClasseQualquer {

}
```