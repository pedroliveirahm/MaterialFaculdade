<h4>Sumário</h4>

* [O que é](#o-que-é)

* [Abstração](#abstração)

* [Classes](#classes)

* [Objetos](#objetos)

# O que é
* È um método de programação `(paradigma)` que usa tipos de dados personalizados.
    * Em vez de operar apenas com tipos de dados primitivos, é possível construir novos tipos de dados
* Baseia-se fundamentalmente no conceito de objetos

## Vantagens
* Fornece uma estrutura modular para a construção de programas.
    * O programa fica dividido em partes menores, facilitando a organização e a manuntenção do código
* Reuso de código, acelerando o desenvolvimento.

* No conceito de encapsulamento, não é necessário conhecer a implementação interna de um objeto para poder usá-lo.

# Abstração
* Abstrair é pegar um problema e selecionar aspectos específicos, deixando de lado outros aspectos. Representando uma entidade do mundo real na forma de ideas.
    * Entidades abstraídas (objetos) podem se comunicar entre si, por meio de mensagens

## Mensagens 
* Mensagem é um sinal enviado de um objeto a outro, requisitando um serviço, usando uma operação programada no objeto chamado.
    * As mensagens somente ocorrem entre objetos que possuam uma associação

* As mensagens também são programadas.
    * Quando uma mensagem é recebida, uma operação é invocada no objeto chamado
* Há vários formatos de mensagens: procedures (subs e functions), passagem de sinais entre threads, acionamento de eventos, etc

# Classes
* Classe representa uma ideia e classifica objetos que tenham propriedades similares.
* Blocos de construção mais importantes dos sistemas O.O, com responsabilidades bem definidas dentro da aplicação.
* Coleção de objetos descritos com os mesmos atributos e operações.
* Tipo personalizado de dados "molde" para a criação de objetos.
* Um conjunto de classes é chamado de `namespace`

# Objetos
* Ocorrência específica de uma classes `(instância de classe)`.

* Representa entidades do mundo real, como carros, pessoas, contas, etc, e outros conceitos, como, gráficos (círculos, quadrados, cones).
* Tem características próprias (atributos) e executa ações (métodos), provenientes da classe que originou o objeto.

## Atributo
* Propriedade particular de uma ocorrência de uma classe, por exemplo o nome e a altura de uma pessoa.

* Há dois tipos de atributos : 
    * Estáticos : Mantém o mesmo valor durante sua existência, como a data de nascimento
    * Dinâmico : Valores que variam com o passar do tempo, como a idade

## Método 
* Similar a uma função procedural.
    * Tudo que está dentro do método será executado de forma sequêncial

* È a lógica contida em uma classe para atribuir comportamentos (sequência de comandos), identificada por um nome.
* O ato de invocar (chamar) um método é a passagem de mensagens para o objeto.
* Exemplos de métodos, a classe pessoa pode ter métodos como :
    * nascer (), comer(), morrer()

# Relação Class e Object
* A classe é um molde por onde se defini os atributos e o métodos.

* Já o objeto é uma instância dessa classe na memória da máquina em tempo de execução.
* Uma classe pode gerar vários objetos.

## Representação da Classe
* UML - È uma linguaguem de modelagem unificada

* Diagrama de classes em UML:
    * Nome da classe :
        * Lista de atributos
        * Lista de métodos

* Por exemplo
    * Class pessoa
        * dataDeNascimento
        * altura
        * peso
        * nome

    * 
---
Made with by 💙 Pedro PC 👋 <a href="https://github.com/pedroliveirahm">Seen my GitHub</a>
* <strong>Fale comigo : <a href="https://bio.link/pedroliveirahm" target="_blank">Contato</a></strong>