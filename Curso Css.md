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