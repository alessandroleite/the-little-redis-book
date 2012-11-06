## Sobre ##
O livro Little Redis Book é uma introdução ao Redis.
<!-- The Little Redis Book is a free book introducing Redis. -->

Este livro foi escrito por [Karl Seguin](http://openmymind.net), com ajuda do [Perry Neal](http://twitter.com/perryneal).
<!-- The book was written by Karl Seguin, with Perry Neal's assistance. -->

Se você gostou deste livro, talvez você também irá gostar do livro [The Little MongoDB Book](http://openmymind.net/2011/3/28/The-Little-MongoDB-Book/).
<!-- If you liked this book, maybe you'll also like The Little MongoDB Book. -->

## Licença ##
O livro é distribuído gratuitamente sobre a licença [Attribution-NonCommercial 3.0 Unported license](<http://creativecommons.org/licenses/by-nc/3.0/legalcode>).

## Traduções ##

* [Russo](https://github.com/kondratovich/the-little-redis-book)
* [Italiano](https://github.com/sandroconforto/the-little-redis-book) - [pdf](https://github.com/sandroconforto/the-little-redis-book/raw/master/book/redisIt.pdf)
* [Chinês](https://github.com/JasonLai256/the-little-redis-book)
* [Japoês](https://github.com/craftgear/the-little-redis-book/)

## Formatos ##

O livro é escrito no formato [Markdown](http://daringfireball.net/projects/markdown/) e convertido para PDF utilizando o [pandoc](http://johnmacfarlane.net/pandoc/). Alguns comandos específicos em LaTex foram incluídos no arquivo Markdown para ajudar na geração do PDF (comandos para o título das páginas e para a quebra de página entre os capítulos).

<!-- The book is written in [Markdown](http://daringfireball.net/projects/markdown/) and converted to PDF using [pandoc](http://johnmacfarlane.net/pandoc/). A few LaTex specific commands have been placed in the Markdown file to help with PDF-generation (namely for the title page and to create page breaks between chapters). -->

Para gerar o PDF, ou para os formatos Kindle ou EPUB, baixe e instale o [pandoc](http://johnmacfarlane.net/pandoc/), que é um conversor universal de documentos.

<!-- To generate PDF, Kindle and EPUB formats, download and install [pandoc](http://johnmacfarlane.net/pandoc/), a universal document converter. -->

## Gerando o arquivo PDF ##

O pandoc possui o aplicativo **markdown2pdf** para gerar o PDF que utiliza uma variação do *template* <https://github.com/claes/pandoc-templates>:

<!-- pandoc includes markdown2pdf to generate the PDF using a variation of https://github.com/claes/pandoc-templates: -->

	#!/bin/sh
	paper=a4paper
	hmargin=3cm
	vmargin=3cm
	fontsize=11pt

	mainfont=Verdana
	sansfont=Tahoma
	monofont="Courier New"
	columns=onecolumn
	geometry=portrait
	nohyphenation=true


	markdown2pdf --xetex --template=template/xetex.template \
	-V paper=$paper -V hmargin=$hmargin -V vmargin=$vmargin \
	-V mainfont="$mainfont" -V sansfont="$sansfont" -V monofont="$monofont" \
	-V geometry=$geometry -V columns=$columns -V fontsize=$fontsize \
	-V nohyphenation=$nohyphenation en/redis.md -o redis.pdf

## Gerando o EPUB ##
Utilize o seguinte comando (modificado do comando encontrado em <http://news.ycombinator.com/item?id=3502033>) para gerar o arquivo EPUB.

<!-- Use the following command (modified from the one found at <http://news.ycombinator.com/item?id=3502033>) to generate the EPUB: -->

	pandoc -f markdown -t epub --epub-metadata=en/metadata.xml \
	--template=template/xetex.template -V paper=$paper \
	-V hmargin=$hmargin -V vmargin=$vmargin -V mainfont="$mainfont" \
	-V sansfont="$sansfont" -V monofont="$monofont" -V geometry=$geometry \
	-V columns=$columns -V fontsize=$fontsize -V nohyphenation=$nohyphenation \
	en/redis.md -o redis.epub

## Imagem do Livro ##
O arquivo PSD da imagem do livro está disponível. A fonte utilizada é a [Comfortaa](http://www.dafont.com/comfortaa.font).

<!-- A PSD of the title image is included. The font used is [Comfortaa](http://www.dafont.com/comfortaa.font). -->
