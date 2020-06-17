# Este projeto foi feito por Brad Traversy e adicionado para estudo através do git clone.

> ## Consulte o repositório oficial [aqui][]

  [aqui]: https://github.com/bradtraversy/btre_project       "Brad Traversy"

--------------------------------------------
# Incluindo Markdown para aprendizagem.

### Lista ordenada:
1. Bird
5. McHale
8. Parish

### Lista desordenada:

*   Bird
*   Magic

---
### Fontes diferenciadas:
*single asterisks*

_single underscores_

**double asterisks**

__double underscores__

Portanto, se você deseja incluir um símbolo de direitos autorais em seu artigo, escreva:

&copy;
e Markdown o deixará em paz. Mas se você escrever:

AT&T
O Markdown o traduzirá para:

AT&amp;T

4 < 5

4 &lt; 5

This is an H1
=============

This is an H2
---------------

# This is an H1

## This is an H2

###### This is an H6

# This is an H1 #

## This is an H2 ##

### This is an H3 ######

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
id sem consectetuer libero luctus adipiscing.

> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.


As citações de bloco podem conter outros elementos de Markdown, incluindo cabeçalhos, listas e blocos de código:

> ## This is a header.
> 
> 1.   This is the first list item.
> 2.   This is the second list item.
> 
> Here's some example code:
> 
>     return shell_exec("echo $input | $markdown_script");
>

## LISTAS
O Markdown suporta listas ordenadas (numeradas) e não ordenadas (com marcadores).

As listas não ordenadas usam asteriscos, vantagens e hífens - de forma intercambiável - como marcadores de lista:

*   Red
*   Green
*   Blue

é equivalente a:

+   Red
+   Green
+   Blue

e:

-   Red
-   Green
-   Blue

As listas ordenadas usam números seguidos de pontos:

1.  Bird
2.  McHale
3.  Parish


Os itens da lista podem consistir em vários parágrafos. Cada parágrafo subsequente em um item da lista deve ser recuado por 4 espaços ou uma guia:

1.  This is a list item with two paragraphs. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit. Aliquam hendrerit
    mi posuere lectus.

    Vestibulum enim wisi, viverra nec, fringilla in, laoreet
    vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
    sit amet velit.

2.  Suspendisse id sem consectetuer libero luctus adipiscing.
Parece bom se você recuar todas as linhas dos parágrafos subsequentes, mas aqui novamente, o Markdown permitirá que você seja preguiçoso:

*   This is a list item with two paragraphs.

    This is the second paragraph in the list item. You're
only required to indent the first line. Lorem ipsum dolor
sit amet, consectetuer adipiscing elit.

*   Another item in the same list.

Para colocar um bloco de código em um item da lista, o bloco de código precisa ser recuado duas vezes  - 8 espaços ou duas guias:

*   A list item with a code block:

        <code goes here>
Vale a pena notar que é possível acionar uma lista ordenada por acidente, escrevendo algo como isto:

1986. What a great season.
Em outras palavras, uma sequência numérica-período-espaço no início de uma linha. Para evitar isso, você pode escapar com barra invertida do período:

1986\. What a great season.

Para produzir um bloco de código no Markdown, basta recuar todas as linhas do bloco em pelo menos 4 espaços ou 1 guia. Por exemplo, dada esta entrada:

This is a normal paragraph:

    This is a code block.

A remarcação gerará:

<p>This is a normal paragraph:</p>

<pre><code>This is a code block.
</code></pre>

Um nível de recuo - 4 espaços ou 1 guia - é removido de cada linha do bloco de código. Por exemplo, isto:

Here is an example of AppleScript:

    tell application "Foo"
        beep
    end tell
vai se transformar em:

<p>Here is an example of AppleScript:</p>

<pre><code>tell application "Foo"
    beep
end tell
</code></pre>

Dentro de um bloco de código, e comercial ( &) e colchetes angulares ( <e >) são convertidos automaticamente em entidades HTML. Isso facilita muito a inclusão de exemplos de código-fonte HTML usando o Markdown - basta colá-lo e recuá-lo, e o Markdown lidará com o incômodo de codificar os e comercial e colchetes angulares. Por exemplo, isto:

    <div class="footer">
        &copy; 2004 Foo Corporation
    </div>
vai se transformar em:

<pre><code>&lt;div class="footer"&gt;
    &amp;copy; 2004 Foo Corporation
&lt;/div&gt;
</code></pre>

REGRAS HORIZONTAIS

Você pode produzir uma tag de regra horizontal ( <hr />) colocando três ou mais hífens, asteriscos ou sublinhados em uma linha por si mesmos. Se desejar, você pode usar espaços entre os hífens ou asteriscos. Cada uma das seguintes linhas produzirá uma regra horizontal:

* * *

***

*****

- - -

---------------------------------------
ELEMENTOS DE EXTENSÃO
LIGAÇÕES
O Markdown suporta dois estilos de links: embutido e referência .

Nos dois estilos, o texto do link é delimitado por [colchetes].

Para criar um link embutido, use um conjunto de parênteses regulares imediatamente após o colchete de fechamento do texto do link. Dentro dos parênteses, coloque o URL para o qual deseja apontar o link, juntamente com um título opcional para o link, entre aspas. Por exemplo:

This is [an example](http://example.com/ "Title") inline link.

[This link](http://example.net/) has no title attribute.
Vai produzir:

<p>This is <a href="http://example.com/" title="Title">
an example</a> inline link.</p>

<p><a href="http://example.net/">This link</a> has no
title attribute.</p>
Se você estiver se referindo a um recurso local no mesmo servidor, poderá usar caminhos relativos:

See my [About](/about/) page for details.   
Os links no estilo de referência usam um segundo conjunto de colchetes, dentro do qual você coloca um rótulo de sua escolha para identificar o link:

This is [an example][id] reference-style link.
Opcionalmente, você pode usar um espaço para separar os conjuntos de colchetes:

This is [an example] [id] reference-style link.
Então, em qualquer lugar do documento, você define o rótulo do seu link assim, em uma linha por si só:

[id]: http://example.com/  "Optional Title Here"
Isso é:

Colchetes contendo o identificador do link (opcionalmente recuado da margem esquerda usando até três espaços);
seguido por dois pontos;
seguido por um ou mais espaços (ou tabulações);
seguido pelo URL do link;
opcionalmente seguido por um atributo title para o link, entre aspas duplas ou simples ou entre parênteses.
As três definições de link a seguir são equivalentes:

[foo]: http://example.com/  "Optional Title Here"
[foo]: http://example.com/  'Optional Title Here'
[foo]: http://example.com/  (Optional Title Here)

NOTA: Há um bug conhecido no Markdown.pl 1.0.1 que impede que aspas simples sejam usadas para delimitar títulos de links.

O URL do link pode, opcionalmente, estar entre colchetes angulares:

[id]: <http://example.com/>  "Optional Title Here"
Você pode colocar o atributo title na próxima linha e usar espaços ou guias extras para preenchimento, que tendem a parecer melhor com URLs mais longos:

[id]: http://example.com/longish/path/to/resource/here
    "Optional Title Here"
As definições de link são usadas apenas para criar links durante o processamento do Markdown e são retiradas do documento na saída HTML.

Os nomes de definição de link podem consistir em letras, números, espaços e pontuação - mas não diferenciam maiúsculas de minúsculas. Por exemplo, esses dois links:

[link text][a]
[link text][A]
são equivalentes.

O atalho implícito do nome do link permite omitir o nome do link; nesse caso, o próprio texto do link é usado como o nome. Basta usar um conjunto vazio de colchetes - por exemplo, para vincular a palavra "Google" ao site google.com, você pode simplesmente escrever:

[Google][]
E então defina o link:

[Google]: http://google.com/
Como os nomes dos links podem conter espaços, esse atalho funciona até para várias palavras no texto do link:

Visit [Daring Fireball][] for more information.
E então defina o link:

[Daring Fireball]: http://daringfireball.net/
As definições de link podem ser colocadas em qualquer lugar do seu documento Markdown. Costumo colocá-los imediatamente após cada parágrafo em que são usados, mas se você quiser, pode colocá-los todos no final do documento, como notas de rodapé.

Aqui está um exemplo de links de referência em ação:

I get 10 times more traffic from [Google] [1] than from
[Yahoo] [2] or [MSN] [3].

  [1]: http://google.com/        "Google"
  [2]: http://search.yahoo.com/  "Yahoo Search"
  [3]: http://search.msn.com/    "MSN Search"

Usando o atalho implícito do nome do link, você pode escrever:

I get 10 times more traffic from [Google][] than from
[Yahoo][] or [MSN][].

  [google]: http://google.com/        "Google"
  [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
  [msn]:    http://search.msn.com/    "MSN Search"

Ambos os exemplos acima produzirão a seguinte saída HTML:

<p>I get 10 times more traffic from <a href="http://google.com/"
title="Google">Google</a> than from
<a href="http://search.yahoo.com/" title="Yahoo Search">Yahoo</a>
or <a href="http://search.msn.com/" title="MSN Search">MSN</a>.</p>
Para comparação, aqui está o mesmo parágrafo escrito usando o estilo de link embutido do Markdown:

I get 10 times more traffic from [Google](http://google.com/ "Google")
than from [Yahoo](http://search.yahoo.com/ "Yahoo Search") or
[MSN](http://search.msn.com/ "MSN Search").
O ponto dos links no estilo de referência não é que eles sejam mais fáceis de escrever. O ponto é que, com links no estilo de referência, a fonte do documento é muito mais legível. Compare os exemplos acima: usando links de estilo de referência, o parágrafo em si tem apenas 81 caracteres; com links de estilo embutido, são 176 caracteres; e como HTML bruto, são 234 caracteres. No HTML bruto, há mais marcação do que texto.

Com os links no estilo de referência do Markdown, um documento de origem se assemelha muito mais à saída final, conforme renderizada em um navegador. Ao permitir que você mova os metadados relacionados à marcação para fora do parágrafo, você pode adicionar links sem interromper o fluxo narrativo da sua prosa.

ÊNFASE

O markdown trata os asteriscos ( *) e sublinhados ( _) como indicadores de ênfase. O texto está quebrado com um *ou _será quebrado com uma <em>tag HTML ; double *ou _'s serão agrupados com uma <strong>tag HTML . Por exemplo, esta entrada:</strong></em>


*single asterisks*

_single underscores_

**double asterisks**

__double underscores__
vai produzir:

<em>single asterisks</em>

<em>single underscores</em>

<strong>double asterisks</strong>

<strong>double underscores</strong>
Você pode usar o estilo que preferir; a única restrição é que o mesmo caractere deve ser usado para abrir e fechar um período de ênfase.

A ênfase pode ser usada no meio de uma palavra:

un*frigging*believable
Mas se você cercar um *ou _com espaços, ele será tratado como um asterisco ou sublinhado literal.

Para produzir um asterisco literal ou sublinhado em uma posição em que, de outra forma, seria usado como um delimitador de ênfase, você pode escapar da barra invertida:

\*this text is surrounded by literal asterisks\*

CÓDIGO
Para indicar um intervalo de código, envolva-o com aspas de backtick ( `). Diferentemente de um bloco de código pré-formatado, uma extensão de código indica o código dentro de um parágrafo normal. Por exemplo:

Use the `printf()` function.
vai produzir:

<p>Use the <code>printf()</code> function.</p>
Para incluir um caractere de backtick literal em um período de código, você pode usar vários backticks como delimitadores de abertura e fechamento:

``There is a literal backtick (`) here.``
que produzirá isso:

<p><code>There is a literal backtick (`) here.</code></p>
Os delimitadores de backtick em torno de uma extensão de código podem incluir espaços - um após a abertura, um antes do fechamento. Isso permite que você coloque caracteres literais de backtick no início ou no final de um período de código:

A single backtick in a code span: `` ` ``

A backtick-delimited string in a code span: `` `foo` ``
vai produzir:

<p>A single backtick in a code span: <code>`</code></p>

<p>A backtick-delimited string in a code span: <code>`foo`</code></p>
Com um intervalo de código, e comercial e colchetes angulares são codificados como entidades HTML automaticamente, o que facilita a inclusão de exemplo de tags HTML. Markdown irá transformar isso:

Please don't use any `<blink>` tags.
para dentro:

<p>Please don't use any <code>&lt;blink&gt;</code> tags.</p>
Você pode escrever isto:

`&#8212;` is the decimal-encoded equivalent of `&mdash;`.
para produzir:

<p><code>&amp;#8212;</code> is the decimal-encoded
equivalent of <code>&amp;mdash;</code>.</p>

IMAGENS

É certo que é bastante difícil criar uma sintaxe "natural" para colocar imagens em um formato de documento de texto sem formatação.

O Markdown usa uma sintaxe de imagem que se parece com a sintaxe dos links, permitindo dois estilos: inline e referência .

![Alt text](btre/static/img/lightbox/loading.gif "loading")

A sintaxe da imagem embutida é assim:

![Alt text](btre/static/img/lightbox/next.png "Next")

![Alt text](btre/static/img/showcase.jpg)

Isso é:

Um ponto de exclamação: !;
seguido por um conjunto de colchetes, contendo o alt texto do atributo para a imagem;
seguido por um conjunto de parênteses, contendo o URL ou caminho da imagem, e um title atributo opcional entre aspas duplas ou simples.
A sintaxe da imagem no estilo de referência tem a seguinte aparência:

![Alt text][id]

Onde "id" é o nome de uma referência de imagem definida. As referências de imagem são definidas usando uma sintaxe idêntica às referências de link:

[id]: url/to/image  "Optional title attribute"
No momento da redação deste artigo, o Markdown não possui sintaxe para especificar as dimensões de uma imagem; se isso for importante para você, você pode simplesmente usar <img>tags HTML regulares .

DIVERSOS
LINKS AUTOMÁTICOS
O Markdown suporta um estilo de atalho para criar links "automáticos" para URLs e endereços de email: basta colocar o URL ou o endereço de email entre colchetes angulares. O que isso significa é que, se você deseja mostrar o texto real de um URL ou endereço de e-mail e também tem um link clicável, é possível:

<http://example.com/>
O Markdown transformará isso em:

<a href="http://example.com/">http://example.com/</a>
Os links automáticos para endereços de email funcionam da mesma maneira, exceto que o Markdown também executará um pouco de codificação decimal e hexadecimal aleatória de entidades para ajudar a ocultar seu endereço de spambots de coleta de endereços. Por exemplo, o Markdown transformará isso:

<address@example.com>

\*literal asterisks\*

> # Fonte:
>> ## Click neste [site][] para ver o conteúdo original sobre makdown.

  [site]: https://daringfireball.net/projects/markdown/syntax       "Markdown"
