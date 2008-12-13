[[!include contents]] 

[[Dr. Joe]]

Every wiki needs a sandbox! Just test here and don't worry about messing things up.

***

Trying to upload a file: [[n.png:pic]].... nope didn't work, I get "Internal Server Error".

Okay worked this time. [[Bruce Bartlett]]

$$\array{\arrayopts{\rowalign{center}}\begin{svg}
<svg xmlns="http://www.w3.org/2000/svg" width="10em" height="10em" viewBox="0 0 120 120">
  <desc>A_n Quiver</desc>
  <g fill="none" stroke="black" stroke-width="1">
   <path d="M 60 25 l 25 20 l 0 30 l -25 20 l -25 -20 l 0 -30 z" />
   <g stroke-dasharray="2">
     <path d="M 60 0 l 0 25" />
     <path d="M 85 45 l 25 -20" />
     <path d="M 85 75 l 25 20" />
     <path d="M 60 95 l 0 25" />
     <path d="M 35 75 l -25 20" />
     <path d="M 35 45 l -25 -20" />
   </g> 
  </g>
  <g fill="red" stroke="none">
   <circle cx="60" cy="25" r="4" />
   <circle cx="85" cy="45" r="4" />
   <circle cx="85" cy="75" r="4" />
   <circle cx="60" cy="95" r="4" />
   <circle cx="35" cy="75" r="4" />
   <circle cx="35" cy="45" r="4" />
  </g>
  <foreignObject x="45" y="0" width="16" height="20"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><msub><mi>v</mi><mn>1</mn></msub></math></foreignObject>
  <foreignObject x="83" y="15" width="16" height="20"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><msub><mi>v</mi><mn>2</mn></msub></math></foreignObject>
  <foreignObject x="5" y="25" width="20" height="25"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><msub><mi>v</mi><mrow><msub><mi>n</mi><mn>1</mn></msub></mrow></msub></math></foreignObject>
</svg>
\end{svg}& \equiv \left({U(k)}^{n_1},\{v_i\}\right)}$$


| Function name | Description                    |
| ------------- | ------------------------------ |
| `help()`      | Display the help window.       |
| `destroy()`   | **Destroy your computer!**     |  

Apple
:   Pomaceous fruit of plants of the genus Malus in 
the family Rosaceae.

Orange
:   The fruit of an evergreen tree of the genus Citrus.

Term 1

:   This is a definition with two paragraphs. Lorem ipsum 
    dolor sit amet, consectetuer adipiscing elit. Aliquam 
    hendrerit mi posuere lectus.

    Vestibulum enim wisi, viverra nec, fringilla in, laoreet
    vitae, risus.

:   Second definition for term 1, also wrapped in a paragraph
    because of the blank line preceding it.

Term 2

:   This definition has a code block, a blockquote and a list.

        code block.

    > block quote
    > on two lines.

    1.  first list item
    2.  second list item

You can make abbreviations. Here I'm going to make an abbreviation for the n-category cafe: 

*[nCat]: n-category cafe
Is this a new line?

Now apparently I just type nCat and it should output "n-category cafe". Did it work?  No!

Trying theorem numbering:

+-- {: .num_theorem #Lagrange}
###### Theorem
**(Lagrange's Theorem)**. Let $G$ be a finite group, and let $H$
be a subgroup of $G$. Then the order of $H$ divides the order of
$G$.
=--

By Theorem \ref{Lagrange}, we know that the order of $H$ divides the order of $G$.


+-- {: .un_defn}
###### Definition
**(Definitive definition)**
By definition, this definition is a definition. Definitely.
=--

[[John Baez]]: Here's how include a link to a picture:

![A pic](http://math.ucr.edu/home/baez//cassini_over_enceladus.jpg)


Here goes the neighborhood( [[Eric Forgy]] )

~~~~
This is a code block, fenced-style
~~~~

Huh? That is [PHP Markdown extra code](http://michelf.com/projects/php-markdown/extra/#fenced-code-blocks). That should work here, right...? [[Bruce Bartlett]]

Uploading little pdf icon for linking to pdf's: [[pdficon_small.gif:file]]

Uploading little n-category cafe icon: [[n-cafe_5.gif:file]]

Attempting to link to an n-category cafe post: [My link](http://golem.ph.utexas.edu/category/2008/11/nlab.html#c020636)

Attempting to link to a pdf file: [My link](http://www.math.uni-hamburg.de/home/schreiber/sin.pdf)

Attempting to link to a _page_ inside a pdf file: [My link](http://www.math.uni-hamburg.de/home/schreiber/sin.pdf#page=12)

Attempting to link to an arXiv file: [Higher dimensional algebra and topological quantum field theory](http://arxiv.org/abs/q-alg/9503002)

+-- {: .my_gismo}
Hi is this a gismo?
=--

category: meta