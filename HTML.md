# HTML

• HTML significa Hyper Text Markup Language (Linguagem de Marcação de Hipertexto)

• Um arquivo HTML é um arquivo de texto contendo etiquetas de marcação (markup tags)

• As marcações dizem para o navegador Web como mostrar a página

• Pode ser criado usando um simples editor de textos

# Tags

<html>
<head>
<title>Título da página</title>
</head>
<body>
Esta é minha primeira página. <b>Este texto está em negrito</b>
</body>
</html>

<!-- Para o <body> -->
<br> <h1>Este é um título</h1>

<p>Este é um parágrafo</p>

<p>
Este <br> é um parágrafo com<br> quebras de linha
</p>

<strong>
Este texto está forte
</strong>

<big>
Este texto está grande
</big>

<small>
Este texto está pequeno
</small>

<code>
Define texto de código de computador
</code>

<kbd>
Define texto de teclado
<kbd>

<var> Define variável <var>

<pre>
Define um cmd
</pre>

# Ancoras

<!-- A HTML usa a tag <a> (âncora) para criar um vínculo (link) -->

<!-- Link com um site -->
<a href="https://github.com/pedroliveirahm">Git Hub
</a>

<!-- target="_blank" abre em outra página web -->
<a href="http://www.w3schools.com/"
target="_blank">Visite as W3Schools!</a>

<!-- Link com um especificação da aba -->
<a href="#dicas">Dicas</a>


# Dicas

# Molduras
<!--  tag <frameset> define como dividir a janela em molduras -->
<!--  tag <frame> define qual documento HTML colocar em cada moldura -->
<frameset cols="25%,75%">
   <frame src="frame_a.htm">
   <frame src="frame_b.htm">
</frameset>

# Listas não Ordenadas
<!-- Unorded List <ul> -->
<html>
<body>

<h4>Uma Lista Não Ordenada:</h4>
<ul>
  <li>Café</li>
  <li>Chá</li>
  <li>Leite</li>
</ul>

</body>
</html>

<!-- Orded List <ol> -->
<ol>
<li>Café</li>
<li>Leite</li>
</ol>

# Formulários
<!--  Campo de texto type="text" -->

<form>
Primeiro nome: 
<input type="text" name="firstname">
<br>
Último nome: 
<input type="text" name="lastname">
</form>

<br> 

<!-- Botões Radiais type="radio" -->

<form>
<input type="radio" name="sex" value="male"> Masculino
<br>
<input type="radio" name="sex" value="female"> Feminino
</form>

<br>

<!--  Caixa de seleção  type="checkbox"-->

<form>
<input type="checkbox" name="bike">
Eu tenho uma bicicleta
<br>
<input type="checkbox" name="car">
Eu tenho um carro
</form>

<br>

# Tag img e  atributo scr (source)

<img src="">

<!-- O valor do atributo alt é um texto definido pelo autor  -->
<!-- O atributo "alt" diz ao leitor o que ele ou ela está perdendo numa página se o navegador não pode carregar imagens. O navagador irá então exibir o texto alternativo em vez da imagem. -->

<img src="https://www.hostinger.com.br/tutoriais/wp-content/uploads/sites/12/2019/08/O-que-e-url.png" alt="Hostinger img">

<br>

# Folha de estilo externa (CSS)

<head>
<link rel="stylesheet" type="text/css"
href="meuestilo.css">
</head>

# Tag meta

<!-- Este elemento meta define palavras-chave para a sua página -->

<meta name="keywords" content="HTML, DHTML, CSS, XML, XHTML, JavaScript, VBScript">

# Script

<html>
<head>
</head>

<body>
<script type="text/javascript">
document.write("Oi Mundo!")
</script>
</body>

</html>