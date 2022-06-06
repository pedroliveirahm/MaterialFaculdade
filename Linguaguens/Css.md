<h4>Sumário</h4>

* [Selectors](#selectors)
* [Fonter Internas](#fontes-internas)
* [Espaçamentos](#espaçamentos)
* [Box Model](#box-model)
* [Flexbox](#flexbox)
* [Grid](#grid)
* [Propriedade Position](#propriedade-position)
* [Responsividade](#responsividade)
* [Sass](#sass)

# Selectors
selector {<br>
    property: value;<br>
    property: value1 value2 value3;<br>
}
```bash
$Exemplo

body {
    color: white;
    border: 1px solid blue;
}
```
## Classes e ID's
• A Classe permiti selecionar mais de um elemento, enquanto o ID permiti selecionar apenas 1
* Usar apenas classes é uma boa prática

• O ponto (.) é usado para colocar uma classe. Enquanto no ID é (#)
# Cores
• Nome da cor | Hexadecimal | RGB (Red,Green,Blue) & RGBA (Red,Green,Blue,Transparência)
```bash
body {
    background: white;
    color: red;
}

h1 {
    color: #000000;
}

p { 
    color: rgb(0,0,255);
    # 255 é o número máximo, então trata-se da cor mais forte do azul  
}

a {
    color: rgba(0,0,255,0.6) 
    # A solidez máxima é 1, quanto menor mais transparente
}
```
# Fontes Internas
```bash
body {
    font-family: fonte;
    font-size: tamanhopx; # 16px é o tamanho predefinido (default)
    font-weight: bold; # negrito 
}
```
* Diferença entre Sans-Serif e Serif -> a Serif tem um acabamento nas extremidades das letras
# Espaçamentos
```bash
.class {
    background-color: #333;
    color: #eee;
    width: 960px; # Largura
    margin: auto; # (auto) colocar o elemento de uma forma que a margin fique igual dos dois lados
    padding: 20px;
    border: 3px solid red; 
}
```
## Unidades Css 
* Layout fixo
    * `px` 

* Layout fluido
    * `%` - 0 a 100%
    * `auto` - automático
    * `viewport height` - 0 a 100vh
    * `viewport width` - 0 a 100vw

* Texto fixo
    * `1px` == 0.75pts
    * `16px` (padrão) == 12pts no Word

* Texto fluido
    * `em` - multiplicado pelo pai 
    * `rem` - multiplicado pelo root (padrão, 16px)

```bash
body {
    background-color: #333;
    color: #eee;
    width: 80%;
    box-sizing: border-box; # Usado normalmente no * { }
}
```
# Box Model
• Top | Bottom | Left | Right
 
• Margin -> Border -> Padding -> Conteúdo

• Margin
* Margem externa - espaçamento fora do conteúdo

• Border
* Borda do conteúdo

• Padding
* Margem interna - distância do conteúdo até a borda
# Flexbox
## Flex-direction
• `Eixo x ou y`
* row / row-reverse; (padrão, em linha) <br>
* column / column-reverse; (em coluna)  
    * Quando em coluna, o flex-direction inverte o eixo do align-items com o  justify-content
## Flex-wrap 
• `Quebra de linha`
* nowrap; (padrão, sem quebra de linha)
* wrap / wrap-reverse; (quebra de linha)
## Flex-flow 
• `flex-direction + flex-wrap`
* row nowrap; (padrão)
* column wrap; (coluna + quebra de linha)
* etc
## Align-items 
• `Eixo y`
* flex-start; (padrão, no começo)
* flex-end; (no fim)
* center; (no centro do eixo)

• Align-self : se comporta como align-items para itens individuais
## Align-content 
• `Espaçamento entre linhas`
* flex-start; (padrão, no começo)
* flex-end; (no fim)
* center; (no centro do eixo x)
* space-between; ( alinham-se com distâncias iguais entre eles)
* space-around; (alinham-se com distâncias iguais em torno deles)
## Justify-content 
• `Eixo x`
* flex-start; (padrão, no começo)
* flex-end; (no fim)
* center; (no centro do eixo x)
* space-between; ( alinham-se com distâncias iguais entre eles)
* space-around; (alinham-se com distâncias iguais em torno deles)
# Grid
```bash 
display: grid; # o container é dividido em blocos
```
```bash
grid-template-column: 1fr 1fr; # 2 colunas foram criadas, cada uma com 50%
```
* a criação de colunas pode ser em px, % ou na unidade fracionada (fr)
* apesar de ser 2 colunas, há 3 linhas
    * grid-template-columns : repeat(4, 1fr); abreviação para criar 4 colunas com 1fr
    * grid-template-columns : minimax(200px,1fr) 1fr 1fr; a primeira coluna tem min de 200px e max de 1fr
    * grid-template-columns : repeat(auto-fit, 100px); o auto-fit é responsivo por calcular automaticamente o total de colunas, neste caso, cada uma com 100px
    * grid-templatecolumns : repeat(auto-fit, minmax(100px, auto));
    * grid-template-columns : repeat(auto-fill, minmax(100px, auto)); o auto-fill ele preenche mesmo sem ter items para o container
```bash
grid-template-rows: 50vh 50vh; # duas linhas foram criadas, cada uma com 50vh
```
```bash
grid-column-start : (posição x); # começa na coluna 1
``` 
```bash
grid-column-end : (x+1); # estende o item até a coluna x+1
```
* grid-column : ; // abreviação do grid-column-end/grid-column-start
```bash
grid-row-start: (posição y); # começa na linha 1
```
```bash
grid-row-end: (y+1); # estende o item até a coluna y+1
```
* grid-row: ; // abreviação do grid-row-start/grid-row-end
```bash
grid-template-areas: 
"header header"
"main aside"
"footer footer"; # foram criadas 3 linhas com 2 colunas, cada
```
```bash
• grid-gap : 10px 20px; # é a distância entre as linhas e colunas, respectivamente
```
* justify-content (eixo x), align-content (eixo y) são aplicáveis
* justify-items (eixo x), align-items (eixo y) são aplicáveis
* justify-self (eixo x), align-self (eixo y) são aplicáveis 
# Propriedade Position
• Responsavel pelo modo que o elemento é posicionado
* Static | Relative | Fixed | Absolute | Sticky

* Static é o padrão;
* Segue o fluxo da página
* Propriedades top, bottom, right, left não são aplicáveis
# Responsividade
• Responsividade é a a adptação do tamanho das páginas ao tamanho das telas

• Pode ser aplicada através : 
* box-sizing: border-box;
* width: % ou vw;
* height: % ou vh;
* max-width: px;
* max-height: px;
* através de `media querys`
## Media Query
* 
# Sass
*
---
Made with by 💙 Pedro PC 👋 <a href="https://github.com/pedroliveirahm">Seen my GitHub</a>
* <strong>Fale comigo : <a href="https://bio.link/pedroliveirahm" target="_blank">Contato</a></strong>