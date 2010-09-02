# LatteX

The aim of this project is to provide some JavaScript libraries together with some usage guidelines to ease the web publishing in the same way that LaTeX has done.

Currently this repository acts as dumping area for various experiments.


## Automatic paragraphs from line breaks

Mode for the lazy people, who dont want to write new `<p></p>` all the time.

`<pre>Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.`

`Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat facer possim assum.`

`Typi non habent claritatem insitam; est usus legentis in iis qui facit eorum claritatem. Investigationes demonstraverunt lectores legere me lius quod ii legunt saepius. Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium lectorum. Mirum est notare quam littera gothica, quam nunc putamus parum claram, anteposuerit litterarum formas humanitatis per seacula quarta decima et quinta decima. Eodem modo typi, qui nunc nobis videntur parum clari, fiant sollemnes in futurum.</pre>`

becomes

`<p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.</p>`

`<p>Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat facer possim assum.</p>`

`<p>Typi non habent claritatem insitam; est usus legentis in iis qui facit eorum claritatem. Investigationes demonstraverunt lectores legere me lius quod ii legunt saepius. Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium lectorum. Mirum est notare quam littera gothica, quam nunc putamus parum claram, anteposuerit litterarum formas humanitatis per seacula quarta decima et quinta decima. Eodem modo typi, qui nunc nobis videntur parum clari, fiant sollemnes in futurum.</p>`


## LaTeX math rendering

Uses: AsciiMathML

`<pre>`
`Example: Let $x \in N$ be odd.  Claim: $x^2$ is odd.`

`Proof: If $x \in N$ is odd (assumption), then $x=2k+1$ with some $k \in N$ (definition of oddness). Then $x^2= 4k^2+4k+1 = 2(2k^2+2k)+1$, meaning that $x^2$ is odd. $~\Box$`
`</pre>`



## Automatic chapter, section and paragraph numbering

Done without CSS3, so that numbers are also selectable (Browsers implement CSS3 numbering so that numbers are not part of DOM and therefore not selectable)


`<h1>Title</h1>`

`<h2>Chapter</h2>`

`<h3>Section</h3>`
`<h3>Section</h3>`

`<h4>Subsection</h4>`
`<h4>Subsection</h4>`

`<h2>Chapter</h2>`
`<h3>Section</h3>`

becomes

`1 Chapter			
1.1 Section
1.2 Section
1.2.1 Subsection
1.2.2 Subsection
2 Chapter
2.1 Section`

And every heading gets id attribute with the numbering, meaning that you can anchor the page by #1.1 or #1.2.1



## Automatic syntax highlighting

Uses: shjs

`<pre class="sh_ruby">`
`numbers = [1,2,3,4]`
`puts numbers.first`
`</pre>`


## Forced page breaks in print

CSS3 page breaking

`<div class="page-break"></div>`


## Page numbering

CSS3 page numbering

