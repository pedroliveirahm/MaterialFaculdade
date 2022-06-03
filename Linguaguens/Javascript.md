<h4>Sumário</h4>

• [Variáveis](#variável)<br>
• [Objetos](#objetos)<br>
• [Arrays](#arrays)<br>
• [Funções](#função) <br>

- Operadores:<br>
  - [Operadores Aritiméticos](#operadores-aritiméticos)<br>
  - [Operadores de Igualdade](#operadores-de-igualdade)<br>
  - [Operador Ternário](#operador-ternário)<br>
  - [Operadores Lógicos](#operadores-lógicos)

• [Comparador Não Boleano](#comparador-não-boleano)<br>
• [Trocando Valor de Variáveis](#trocar-valores-de-variáveis)<br>
• [Condicionais](#condicionais)<br>
• [Laços de Repetição](#laços-de-repetição)<br>
• [Mini Projetos](#mini-projetos)<br>
• [Factory Function](#factory-functions)<br>
• [Constructor Function](#constructor-functions)<br>
• [Natureza Dinâmica dos Objetos](#natureza-dinâmica-dos-objetos)<br>
• [Clonagem de Objetos](#clonando-objetos)<br>
• [Math](#math)<br>
• [Strings](#strings)<br>
• [Template Literal](#template-literal)<br>
• [Date](#date)

# Avisos
* No JS não é necessário a atribuição de `;` no final de um comando
* E a declaração de uma string pode estar dentro de aspas simples ou duplas
# Variáveis
• `var`, `let` e `const`
```bash
$Exemplo
let idade = 18;
let nome = 'Pedro';
```
```bash
console.log(idade);
#18
```
```bash
console.log(nome);
#Pedro
```
```bash
console.log('Hello World');
#Hello World
```
## Const & Let
• Só usar a função (let) se for preciso alterar os valores posteriormente<br><br>
• A variável constante não tem seu valor alterado posteriormente

```bash
$Exemplo
const valoringresso = 190;
let valoringresso = 200;

console.log('valoringresso');
#Error
```
• Nesse caso ocorrerá um erro, pois não se pode alterar o valor de uma variável do tipo constante

## Var
• O Var é uma variável global, funciona em qualquer lugar do programa<br>
• O uso do var não é uma boa prática<br>
• O let e o const tem escopo de bloco, enquanto o var tem escopo de função
```bash
if(true) {
    var a = 1;
    let b = 2;
}

console.log(a);
#1

console.log(b);
#is not defined
```
* O var funciona normalmente, enquanto o let da *error* 

```bash
let b = 2;

if(true) {
    console.log(b)
}

#2
```
* Neste caso, funciona normalmente, pois a variável let está dentro de um bloco de código maior
## Tipos Primitivos
```bash
let nome = 'rafael'; //string
let idade = 18; //number - float, double e int
let aprovado = true; //boolean
let sobrenome; //undefined
let cor = null; //none - em casos para redefinir valor
```
## Tipagem Dinâmica
• No Js não é necessário atribuir o tipo primitivo a variável
```bash
let nome = 'Pedro';
typeof nome
#"string"
```
```bash
let idade = 18;
typeof idade
#"number"
```
```bash
let cor = null;
typeof cor
#"object"
```
# Objetos
```bash
$Exemplo
let nome = 'Pedro';
let idade = 18;
let estaAprovado = true;

let pessoa = {
    nome,
    idade,
    estaAprovado
};

let celular = {
    marca : 'Iphone',
    armazenamento : 256,
    tamanhoTela : {
        vertical : 5.92
        horizontal : 3.2
    },
    processador : 'M1'
};
```

```bash
console.log(pessoa);
#estaAprovado: true
#idade: 18
#nome: "Pedro"
#sobrenome: "Oliveira"

console.log(pessoa.nome);
#Pedro

console.log(typeof pessoa);
#Object
```
# Arrays
• Nada mais é do que um conjunto de dados que podem ser acessados por um índice
* O índice é onde se encontra uma informação de um conjunto de dados
* A contagem dos índices começa do 0
```bash
let idadefamilia = [18,36,40];
console.log(idadefamilia);
#(3) [18, 36, 40]
#0: 18
#1: 36
#2: 40
```
• Essa sequência numérica(0,1,2) são os índices

```bash
console.log(idadefamilia[2]);
#40
```
```bash
console.log(idadefamilia.length);
#3
```
# Função
• Controla todo o fluxo de execução
- Entrada de dados
- Saida de dados

• Padrão a seguir (Boas práticas)
- function verbo+Substantivo
- `camelCase` - umDoisTresQuatro

```bash
let corSite = "azul";

function escolherCor() {
    corSite = "";
}
console.log(corSite);
#azul

resetaCor();
console.log(corSite);
#vazio
```

```bash
let corSite = "verde";

function escolherCor(novaCor) {
    corSite = novaCor;
}
console.log(corSite);
#verde

escolherCor("vermelho");
console.log(corSite);
#vermelho
```

```bash
let corSite = "azul";

function resetaCor(cor,tonalidade) {
    corSite = cor + ' ' + tonalidade;
}
console.log(corSite);
#azul

resetaCor("verde", "claro");
console.log(corSite);
#verde claro
```
# Operadores Aritiméticos
• + Adição <br>
• - Subtração<br>
• \* Multiplicação<br>
• / Divisão<br>
• \*\* Exponenciação

• Operadores:
- Incremento ++
- Decremento --
```bash
let idade = 18;

console.log(idade++);
#18

console.log(idade);
#19
```
```bash
let idade = 20

console.log(++idade);
#21
```
# Operadores de Igualdade
```bash
console.log(1===1);
#true
```
* Está sendo tanto o valor quanto o tipo primitivo, também é o mais recomendado
```bash
console.log('1'===1);
#false
```
```bash
console.log('1'==1);
#true
```
* Está sendo comparado apenas o valor
# Operador Ternário
```bash
let pontos = 100;
let tipoCliente = pontos > 100 ? 'premium' : 'comum';

console.log(tipoCliente);
#comum
```
* ? -> se sim
* : -> se não
```bash
let pontos = 120;
let tipoCliente = pontos > 100 ? 'premium' : 'comum';

console.log(tipoCliente);
#premium
```
# Operadores Lógicos
• Tomam decisões baseadas em condições multiplas
- And `&&`
- Or `||`
- Not `!`
```bash
console.log(true&&true);
#true
```
```bash
console.log(true&&false);
#false
```

```bash
// Pessoa x, só pode aplicar para carteira de habilitação caso houver: carteira de trabalho && maior que 18 anos

let maiorDeIdade = true;
let possuiCarteiraDeTrabalho = true;
let podeAplicar = maiorDeIdade&&possuiCarteiraDeTrabalho;

console.log(podeAplicar);
#true
```
# Comparador não Booleano
• Falsy :
- Undefined
- Null
- 0
- False
- "" (string vazio)
- NaN (not a number) - calculos matemáticos que resultam em resultados não compatíveis

• Truthy:
- True
- String
- Number

```bash
const corPadrao = 'Azul';
let corPersonalizada = 'Vermelho';
let corPerfil = corPadrao || corPersonalizada;

console.log(corPerfil);
#Azul
```
- O `||` (Or) para de fazer a comparação ao aparecer o primeiro valor Truthy

# Trocar valores de Variáveis
```bash
let a = "Vermelho";
let b = "Azul";

let c = a;
a = b;
b = c;

console.log(a);
console.log(b);
```
### Com functions
```bash
var a = 10;

function trocarValor(a) {
    this.a = a;
    return a;
}

function mostrarValor(numero) {
    console.log(numero);
}

mostrarValor(a);
#10

trocarValor(20);
mostrarValor(this.a);
#20
```
```bash
let a = 10;

function trocarValor(valor) {
    a = valor;
    return a;
}

function mostrarValor() {
    console.log(a);
}

mostrarValor();
#10

trocarValor(20);
mostrarValor();
#20
```
# Condicionais
### If...else

```bash
let hora;

function inputHora(hora) {
    this.hora = hora;
    return hora;
}

function outputSaudacao() {

    if (this.hora >= 5.00 && this.hora < 12.00 ) {
        console.log("Bom dia !");
    } else if (this.hora >= 12.00 && this.hora < 18.00 ) {
        console.log("Boa tarde !");
    } else {
        console.log("Boa noite !");
    }
}

inputHora(11);
outputSaudacao();
#Bom dia !
```
### Switch case

```bash
let acesso; // comum, gerente, ceo

acesso = "ceo";

switch (acesso) {
    case "comum" : console.log("Você tem a permissao comum");
    break; //para de ler as outras condições

    case "gerente" :
    console.log("Você tem a permissao gerente");
    break;

    case "ceo" :
    console.log("Você tem a permissao ceo");
    break;

    default : # semelhante ao else
    console.log("Usuário não reconhecido");
}
```

# Laços de repetição

### For

```bash
for(let i = 0; i < 5; i++) {
    console.log("ABC", i);
}
```

```bash
for(;;) {
    console.log("Looping");
}
```

### While

```bash
let i = 0;

while (i < 5) {
    console.log(i);
    i++;
}
```
### Do...while

```bash
let i = 0

do {
    console.log(i);
    i++;
} while (i < 5)
```

### For...in
• Iteração sobre propriedade de objetos ou elementos de um array
```bash
$Exemplo
    # Objeto
const pessoa = {
    nome : "Pedro",
    idade : 18
};
    
    # Array
const cores = ["Verde", "Azul", "Amarelo"];
```
* O atributo "nome" é uma `key` e a atribuição "Pedro" é um `value`

* key-value
```bash
for(let key in pessoa) {
    console.log(key); # acesso as keys(atributos)

    console.log(key, pessoa.nome);
    # ou
    console.log(key, pessoa["nome"]);

    console.log(key,pessoa[key])
}
```
* Acessar uma propriedade(atributo) -> . ou [" "]
```bash
for(let key in cores) {
    console.log(key); # acesso aos índices

    console.log(key,cores[key]); # acesso as propriedades dos índices
}
```
*  Quando se acessa um array, todas as propriedades são acessadas pelo índice
### For...off
• Iteração sobre arrays
* Mais simples do que o For...in
```bash
const cores = ["Verde", "Azul", "Amarelo"];

for(let value of cores) {
    console.log(value); # acesso as propriedades dos índices do array
}
```
# Mini Projetos
## Máximo Entre Dois Valores
```bash
$Premissa
// Escrever uma função que usa 2 números e retorna o maior deles
```
```bash
$Exemplo
let maiorValor = max(38,46);
```

```bash
function max(numero1, numero2) {
    
    if (numero1 > numero2) {
        return numero1;
    } else {
        return numero2;
    }
}
```
#### Código mais limpo
* Uso do operador ternário
```bash
function max(numero1, numero2) {
    return numero1 > numero2 ? numero1 : numero2 ;
}
```
## Fizzbuzz
• Compara valores retorna baseado no valor de entrada
```bash
$Premissa
// Valor que não é um número, retornar -> Não é um número
// Valor divisível tanto por 3 quanto por 5, retornar -> FizzBuzz
// Valor divisível por 3, retornar -> Fizz
// Valor divisível por 5, retornar ->  Buzz
// Valor que não é divisível tanto por 3 quanto por 5, retornar -> Resto diferente de 0
```

```bash
const resultado = fizzBuzz(15);

function fizzBuzz(entrada) {
    if (typeof entrada !== "number")
        return "Não é um número";

    if (entrada % 5 === 0 && entrada % 3 === 0)
    return "FizzBuzz";

    if (entrada % 3 === 0)
        return "Fizz";

    if (entrada % 5 === 0)
        return "Buzz";

    if (entrada % 3 !== 0 && entrada % 5 !== 0)
    return "Resto da divisão é diferente de 0";
    
    return entrada;
}

console.log(resultado);
#FizzBuzz
```
## Medidor de Velocidade
```bash
$Premissa
// Velocidade max de 70km, retornar -> Limite permitido 
// A cade 5km a cima do limite, retornar -> + 1 ponto na carteira
// Função Math.Floor() <- Arredonda números
// Caso pontos forem maior ou igual a 12, return -> Carteira apreendida
```

```bash
function verificarVelocidade(velocidade) {
    const velocidadeMax = 70;
    
    if (velocidade <= velocidadeMax) {
        console.log("Ok, velocidade permitida");
    } else {
        const calculo = velocidade - velocidadeMax;
        const pontos = calculo / 5;
        
        if (pontos >= 12) {
            console.log("Sua carteira foi apreendida");
        } else {
            console.log("Você recebeu " + Math.floor(pontos) + " ponto(s) na carteira")
        }
    }
}

verificarVelocidade(109);
#Você recebeu 7 ponto(s) na carteira
```
## Par ou Ìmpar
```bash
$Premissa
// Receber uma quantidade de valores para avaliar
// Dizer cada número dessa sequência de valores é par ou ímpar
```

```bash
function exibirTipo(numero) {
    if (typeof numero !== "number") {
        console.log("Não é um número. Por gentileza, digite um número !")
    } else {
        for (let i = 0; i <= numero; i++) {
            if (i % 2 === 0) {
                console.log(i, "Par");
            } else {
                console.log(i, "Ímpar");
            }
        }
    }
}

exibirTipo(5);
```
### Encontro o String
```bash
$Premissa
// Criar um método que leia as propriedades de um objeto
// Exibir somente as propriedades do tipo String desse objeto
```
```bash
const filme = {
    nome : "Vingadores",
    ano : 2018,
    diretor : "Russo's",
    personagem : "Homem de Ferro"
}

function exibirPropriedades(object) {
    for (let key in object) {
        if (typeof object[key] === "string") {
            console.log(key, object[key]);
        }
    }
}

exibirPropriedades(filme);
```
### Multiplos de 3 e 5
```bash
$Premissa
// Criar uma função que retorna a soma de todos os multiplos de 3 e 5
```
```bash
function somar(numero) {
    let multiplo5 = 0;
    let multiplo3 = 0;

    for(let i = 0; i <= numero; i++) {
        if(i % 3 === 0)
            multiplo3 += i;
        if(i % 5 === 0)
            multiplo5 += i;
    }

    console.log(multiplo3 + multiplo5);
}

somar(10);
#33
```
### Calcular Média
```bash
$Premissa
// Calcular a média das notas escolares
```

```bash
const array = [70, 70, 80];

function mediaAluno(notas) {
    
    const media = calcularMedia(notas);

    if(media <= 59) return 'F';
    if(media <= 69) return 'D';
    if(media <= 79) return 'C';
    if(media <= 89) return 'B';
    return 'A';
}

function calcularMedia(array) {
    
    let soma = 0;

    for (let valor of array) {
        soma += valor;
    }

    return soma / (array.length);
}

console.log(mediaAluno(array));
#C
```
### Contador de Asteríscos
```bash
$Premissa
// Criar uma função que exibe a quantidade de * que aquela linha possui
```
```bash
function exibirAsterisos(linhas) {
    let padrao = '';
    for(let linha =  1; linha <= linhas; linha++) {
        padrao += '*';
        console.log(padrao);
    }
}

exibirAsterisos(10);
```
### Exibir Números Primos
```bash
$Premissa
// Criar função para mostrar os números primos
```
```bash
function exibirNumerosPrimos(limite) {
    for (let numero = 2; numero <= limite; numero++) {
        if (numeroPrimo(numero)) 
            console.log(numero);
    }
}

function numeroPrimo(numero) {
    for (let divisor = 2; divisor < numero; divisor++) {
            
        if(numero % divisor === 0) {
            return false;
        }
    }
    
    return true;
}

exibirNumerosPrimos(15);
```
# Factory Function
• Encapsula uma informação dentro de um método que cria um objeto

```bash
    # Object
const celular = {
    marca : 'ASUS',
    tamanhoTela : {
        vertical : 155,
        horizontal : 75
    },
    capacidadeBateria : 5000,
    ligar: function() {
        console.log("Fazendo ligação...");
    }
}
```
* Factory Function :
```bash
function criarCelular(marca,tamanhoTela,capacidadeBateria) {
    return celular = {
        marca,
        tamanhoTela,
        capacidadeBateria,
        ligar() {
            console.log("Fazendo ligação...");
        }
    }
}

const novoCelular = criarCelular('Zenfone', 5.5,5000);

console.log(novoCelular);
#{marca: 'Zenfone', tamanhoTela: 5.5, capacidadeBateria: 5000, ligar: ƒ}
```
# Constructor Function
* Semelhante com a factory function
```bash
# Pascal Case - UmDoisTresQuatro
function Celular(marca,tamanhoTela,capacidadeBateria) {
    this.marca = marca,
    this.tamanhoTela = tamanhoTela,
    this.capacidadeBateria = capacidadeBateria,
    this.ligar = function() {
        console.log("Fazendo Ligação...");
    }
}
# Não precisa do return

const novoCelular = new Celular("ASUS",5.2,5500);

console.log(novoCelular);
#Celular {marcaCelular: 'ASUS', tamanhoTela: 5.2, capacidadeBateria: 5500, ligar: ƒ}
```
# Natureza Dinâmica dos Objetos
```bash
const mouse = {
    cor : 'Azul',
    marca : 'RedDragon',
    tipo : 'Gamer'
};

mouse.dpi = 5000;
mouse.tipo = "Escritório";

mouse.mudarCor = function(cor) {
    this.cor = cor;
    return cor;
}

mouse.mudarCor('Red');
console.log(mouse);
```
# Clonagem de Objetos
* Object.assign({alvo}, object);
```bash
const celular = {
    marca : 'ASUS',
    tamanhoTela : {
        vertical : 155,
        horizontal : 75
    },
    capacidadeBateria : 5000,
    ligar : function() {
        console.log("Fazendo ligação...");
    }
};

const novoCelular = Object.assign({
    camera : 100
},celular);
console.log(novoCelular);
```
* Ou
```bash
const novoObjeto = {...celular};
console.log(novoObjeto);
```
# Math
• Família de funções mais usadas no JS
* Math.random() - Cria números aleatórios
* Math.max(3,6,8,10) - Diz o maior valor (10)
* Math.min(3,6,8,10) - Diz o menor valor (3)
# Strings
• Métodos de um String
* Tipo primitivo
```bash
const mensagem = ('Dona aranha subiu pela parede');
console.log(typeof mensagem);
#string
```
* Tipo objeto
```bash
const outraMensagem = new String('O rato roeu a roupa do rei de roma');
console.log(typeof outraMensagem);
#object
```
* Quando o `.` é usado, o JS encapsula o tipo primitivo permitindo usar como objeto e ter novas funcionalidades
```bash
console.log(outraMensagem.length);
```
* .length (comprimento) - neste caso, mostra a quantidade de caracteres
```bash 
console.log(outraMensagem[2]);
```
```bash
console.log(outraMensagem.includes('rato'));
#true
```
* .includes diz se existe ou não o que foi escrito;
```bash
console.log(mensagem.startsWith('Dona'));
#true
console.log(mensagem.endsWith('parede'));
#true
```
```bash
console.log(outraMensagem.indexOf('rato'));
#7
```
• Outros
* .trim();
* .split()
# Template Literal
```bash
let usuario = 'Pedro';

const email = `Olá, ${usuario}.

Esta é uma cartilha de email.

Me corresponda o mais rápido possível 

Obrigado`;

console.log(email);
```
# Date
```bash
const data = new Date();

console.log(data);
```
* Informa a data atual

