# HTML


• HTML significa Hyper Text Markup Language (Linguagem de Marcação de Hipertexto)

• Um arquivo HTML é um arquivo de texto contendo etiquetas de marcação (markup tags)

• As marcações dizem para o navegador Web como mostrar a página

```bash
# Tags

<html>

  <head>
    <title>Título da página</title>
  </head>

  <body>
    <p>Esta é minha primeira página.</p>
    <b>Este texto está em negrito</b>
  </body>
</html>

<br> //Quebra de linha

<h1>Este é um título</h1>

<p>Este é um parágrafo</p>

<p>
Este <br> é um parágrafo com <br> quebra de linha
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

<!-- O HTML usa a tag <a> (âncora) para criar um vínculo (link) -->

<!-- Link com um site -->
<a href="https://github.com/pedroliveirahm">Git Hub
</a>

<!-- target="_blank" abre em outra aba do browser -->
<a href="https://github.com/pedroliveirahm"
target="_blank">Visite meu perfil!</a>

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

# Listas não Ordenadas (Unorderd List)
<html>

  <body>
    <ul>  
      
      <li>Café</li>
      <li>Chá</li>
      <li>Leite</li>
  
  </ul>
  </body>

</html>

# Lista Ordenada (Orded List)

<ol>
  <li>Café</li>
  <li>Leite</li>
</ol>

# Formulários <form>
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

O valor do atributo alt é um texto definido pelo autor

O atributo "alt" diz ao leitor o que está perdendo numa página se o navegador não pode carregar imagens 

O navegador irá então exibir o texto alternativo em vez da imagem.

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

```