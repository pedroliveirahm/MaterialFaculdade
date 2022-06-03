<h4>Sumário</h4>

* [Selectors](#selectors)
* [Fonter Internas](#fontes-internas)
* [Espaçamentos](#espaçamentos)
* [Box Model](#box-model)
* [Flexbox](#flexbox)
* [Grid](#grid)
* [Propriedade Position](#propriedade-position)
* [Responsividade](#responsividade)
* [Media Query](#media-query)
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
• O ponto (.) é usado para colocar uma classe enquanto no ID é (#)

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
    font-size: tamanhopx; #16px é o que já aparece sem alteração
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
* Margem interna - espaçamento dentro do conteúdo para borda
# Flexbox
• Flex-direction : eixo x ou y
* row / row-reverse; (padrão, em linha) <br>
* column / column-reverse; (em coluna)  
    * Quando em coluna, o flex-direction inverte o eixo do align-items com o  justify-content

• Flex-wrap : 
* nowrap; (padrão, sem quebra de linha)
* wrap / wrap-reverse; (quebra de linha)
 

• Flex-flow : flex-direction + flex-wrap
* row nowrap; (padrão)
* column wrap; (coluna + quebra de linha)
* etc

• Align-items : eixo y
* flex-start; (padrão, no começo)
* flex-end; (no fim)
* center; (no centro do eixo)

• Align-self : se comporta como align-items para itens individuais

• Align-content : espaçamento entre linhas
* flex-start; (padrão, no começo)
* flex-end; (no fim)
* center; (no centro do eixo x)
* space-between; ( alinham-se com distâncias iguais entre eles)
* space-around; (alinham-se com distâncias iguais em torno deles)


• Justify-content : eixo x
* flex-start; (padrão, no começo)
* flex-end; (no fim)
* center; (no centro do eixo x)
* space-between; ( alinham-se com distâncias iguais entre eles)
* space-around; (alinham-se com distâncias iguais em torno deles)

# Flexbox2 
## Flex Container
* display
* flex-direction
* flex-wrap
* flex-flow
* justify-content
* align-items
* align-content
# Grid 
* display: grid;

* O container é dividido em blocos
* grid-column-start : (posição x); // começa na coluna 1 
* grid-column-end : (x+1); //estende o item até a coluna x+1 // aplica-se a prop. span
* grid-column : ; //abreviação do grid-column-end + start // span também se aplica
* grid-row-start: (posição y); //semelhante a grid-column-start
* grid-row-end : (y+1); //estende o item até a coluna y+1
* grid-row : ; //abreviação do grid-row-start + end // 
* grid-area : grid-row-start / column start / row-end / column-end;
* order : (position x); 

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
# Media Query

# Sass

# CSS Grid
* display: grid;
* grid-template-columns : 1fr 1fr; fr é a unidade fracional, neste caso, 2 colunas, cada uma com 50% de espaço.
    * Apesar de ser 2 colunas, há 3 linhas
    * a criação de colunas pode ser em px, % ou na unidade fracionada (fr)
    * grid-template-columns : repeat(4, 1fr); abreviação para criar 4 colunas com 1fr
    * grid-template-columns : minimax(200px,1fr) 1fr 1fr; a primeira coluna tem min de 200px e max de 1fr
    * grid-template-columns : repeat(auto-fit, 100px); o auto-fit é responsivo por calcular automaticamente o total de colunas, neste caso, cada uma com 100px
    * grid-templatecolumns : repeat(auto-fit, minmax(100px, auto));
    <!-- * grid-template-columns : repeat(auto-fill, minmax(100px, auto)); o auto-fill ele preenche mesmo sem ter items para o container -->
* grid-template-rows : 10px 20px 30px 40px : as linhas ditam a altura da coluna
* grid-template-areas : "a b c" "d e f"; foi criado 2 linhas com 3 colunas
* grid-area : a; o seletor ficará posicionado na area "a" acima

---
Made with by 💙 Pedro PC 👋 <a href="https://github.com/pedroliveirahm">Seen my GitHub</a>
* <strong>Fale comigo : <a href="https://bio.link/pedroliveirahm" target="_blank">Contato</a></strong>