
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{: toc}


## Idea

**Extraordinary natural transformations**, or **extranatural transformations**, are what you get when you "bend the rules" for [[natural transformation]]s.  One intuitive approach to them is through [[string diagrams]]: every time you bend a string (that represents a component of a natural transformation) into a U-shape or upside-down U-shape, the U-shape represents a component of an extranatural transformation.  Thus, the rules for extranatural transformations mirror rules for ordinary [[natural transformations]], except they are bent into shapes with a covariant part and a contravariant part.  (Cf. interactions between particles and their corresponding [[antiparticle]]s.) 

A transformation can also be ordinary-natural in some variables and extraordinary-natural in other variables.  Sometimes this sort of transformation is called a *generalized natural transformation*.  The late [[Max Kelly]] was fond of saying that really it's all the same basic concept, however, so why proliferate terminology needlessly?  So he would simply say a transformation was "natural" in all its arguments, both the "ordinary" and the "extraordinary" ones.

The calculus of natural and extranatural transformations is a very simple string diagram calculus; perhaps the most basic one.  It was first introduced by Eilenberg, Kelly, and Mac Lane in the mid 60's.

There is also a yet more general notion of [[dinatural transformation]].  However, there are few examples of dinatural transformations which are not extranatural.  Also, unlike extranatural transformations, dinatural transformations cannot be generalized to all [[enriched categories]] and do not admit a natural string diagram calculus.



## Examples

Consider the [[function set]] functor $\hom: Set^{op} \times Set \to Set$ (or more generally, the [[internal hom]] functor $\hom: V^{op} \times V \to V$ where $V$ is [[symmetric monoidal category|symmetric monoidal]] [[closed category|closed]]). The [[identity transformation]] $1: \hom \to \hom$ has components of the form 

$$1_{x, y}: x^y \to x^y$$ 

and this of course is natural in each of the separate arguments $x, y$. String diagrammatically, this naturality would be represented by placing the domain over the codomain and linking the two instances of $x$ with a straight line and the two instances of $y$ with a straight line. Although it's trivial, let's at least record what naturality in say $y$ would mean: it means that for any morphism $g: y \to y'$ we have an equation of the form

\[ \label{naturality} 1_{x, y} x^g = x^g 1_{x, y'}: x^{y'} \to x^y \]

<center>
<img src="http://younesse.net/assets/nLab/extranatural+transformation/svg/naturality.svg" title="Xy-Pic code available by replacing /svg/img.svg by /img.md in the image URL" width="250"/>
</center>


Now, the [[adjunction]] between [[tensor product]] and internal hom allow us to "bend" the transformation into another: 

$$eval_{x, y}: x^y \otimes y \to x$$ 

in which the two instances of $y$ are linked by a U-shape. This gives a transformation which is natural in $x$ but not of course in $y$; rather, in $y$ we have an equation which is companion to (eq:naturality): 

\[ \label{extranaturality} eval_{x, y} (x^g \otimes y) = eval_{x, y'} (x^{y'} \otimes g): x^{y'} \otimes y \to x \]

<center>
<img src="http://younesse.net/assets/nLab/extranatural+transformation/svg/extranaturality_counit.svg" title="Xy-Pic code available by replacing /svg/img.svg by /img.md in the image URL" width="350"/>
</center>

and we say in this case that $eval_{x, y}$ is **extranatural** in $y$. Notice how the extranatural variable $y$ in $eval_{x, y}$ appears once covariantly [in the tensor factor] and once contravariantly [in the exponent], but together on the same side of the arrow [here the domain]. (There is a nice string diagram picture for (eq:extranaturality) which the reader might like to draw at this point.) 

Thus we already see that $eval_{x, y}$ is a "generalized natural" transformation, involving a mixture of naturality (in $x$) and extranaturality (in $y$).

The basic idea should now be clear, but let's give a few more examples. Starting with the identity transformation 

$$1_{x, y}: x \otimes y \to x \otimes y$$ 

we can again bend it using the tensor-hom adjunction to form an arrow 

$$coeval_{x, y}: x \to (x \otimes y)^y$$ 

where again $y$ appears once covariantly and once contravariantly, this time on the codomain side. The extranaturality in $y$ is the condition

$$(x \otimes g)^{y} coeval_{x, y} = (x \otimes y')^g coeval_{x, y'}$$

<center>
<img src="http://younesse.net/assets/nLab/extranatural+transformation/svg/extranaturality_unit.svg" title="Xy-Pic code available by replacing /svg/img.svg by /img.md in the image URL" width="350"/>
</center>

for every arrow $g: y \to y'$. 

As these examples indicate, instances of ordinary naturality are typically transferred into instances of extranaturality by means of adjunctions. Indeed, basic instances of U-shapes or upside-down U-shapes in string diagrams come about through counits and units of adjunctions, 

$$\varepsilon: F U \to 1 \qquad \eta: 1 \to U F$$


## Formalization {#Defn}

Let $F\colon A\times B\times B^{op} \to D$ and $G\colon A\times C\times C^{op}\to D$ be functors.  A family of morphisms
$$ \alpha_{a,b,c}\colon F(a,b,b) \to G(a,c,c) $$
for $a\in A$, $b\in B$, and $c\in C$ is said to be **natural**, or more precisely *ordinary-natural in $a$ and extranatural in $b$ and $c$*, if the following hold.

* For all $f\colon a\to a'$ in $A$ and all $b\in B$ and $c\in C$, the following square commutes (ordinary naturality in $a$):
  $$\array{&F(a,b,b) & \overset{F(f,1,1)}{\to} & F(a',b,b) &\\
  ^{\alpha_{a,b,c}} &\downarrow && \downarrow & ^{\alpha_{a',b,c}}\\
  &G(a,c,c)& \underset{G(f,1,1)}{\to} & G(a',c,c) &}$$
* For all $g\colon b\to b'$ in $B$ and all $a\in A$ and $c\in C$, the following square commutes (extranaturality in $b$):
  $$\array{&F(a,b,b') & \overset{F(1,1,g)}{\to} & F(a,b,b) &\\
  ^{F(1,g,1)} &\downarrow && \downarrow & ^{\alpha_{a,b,c}}\\
  &F(a,b',b')& \underset{\alpha_{a,b',c}}{\to} & G(a,c,c) &}$$
* For all $h\colon c\to c'$ in $C$ and all $a\in A$ and $b\in B$, the following square commutes (extranaturality in $c$):
  $$\array{&F(a,b,b) & \overset{\alpha_{a,b,c}}{\to} & G(a,c,c) &\\
  ^{\alpha_{a,b,c'}} &\downarrow && \downarrow & ^{G(1,h,1)}\\
  & G(a,c',c') & \underset{G(1,1,h)}{\to} & G(a,c',c) &}$$

It is convenient to draw "string diagrams" specifying in what variables a transformation is natural and extranatural.  For instance, the above transformation can be notated in this way:

<svg width="170" height="200" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:se="http://svg-edit.googlecode.com">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <g>
  <title>Layer 1</title>
  <polyline se:connector="svg_19989_1 svg_19989_4" fill="none" stroke-width="2" stroke="#000" points="29.273,38 29.7109,101.5 30.1489,165" id="svg_19989_7"/>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_19989_1" y="38" x="29">A</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_19989_2" y="38" x="85">B</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_19989_3" y="36" x="141">B</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_19989_4" y="183" x="30">A</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_19989_5" y="184" x="87">C</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_19989_6" y="184" x="142">C</text>
  <path stroke-width="2" stroke="#000" fill="none" id="svg_19989_8" d="m85,42c3.5,17.5 6.5,44.5 28,45c21.5,0.5 28,-27 28,-44"/>
  <path transform="rotate(-180, 114, 130.5)" id="svg_19989_9" stroke-width="2" stroke="#000" fill="none" d="m86,108c3.5,17.5 6.5,44.5 28,45c21.5,0.5 28,-27 28,-44"/>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="10" stroke-width="0" stroke="#000" fill="#000000" id="svg_19989_10" y="21" x="100">op</text>
  <text id="svg_19989_11" xml:space="preserve" text-anchor="middle" font-family="serif" font-size="10" stroke-width="0" stroke="#000" fill="#000000" y="166" x="103">op</text>
 </g>
</svg>

Similarly, a transformation from $f\colon (A,B,A^{op},C^{op}) \to X$ to $g\colon (C^{op},B,D^{op},D) \to X$ which is natural in $B$ and $C^{op}$ and extranatural in $A$ and $D$ would be notated in this way:

<svg width="250" height="200" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:se="http://svg-edit.googlecode.com">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <g>
  <title>Layer 1</title>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_43543_1" y="36" x="27">A</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_43543_2" y="35" x="85">B</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_43543_3" y="35" x="143">A</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_43543_4" y="35" x="198">C</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_43543_5" y="190" x="29">C</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_43543_6" y="189" x="83">B</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_43543_7" y="188" x="146">D</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_43543_8" y="186" x="201">D</text>
  <path stroke-width="2" stroke="#000000" fill="#FF0000" id="svg_43543_9" d="m84,42l0,121"/>
  <path stroke-width="2" stroke="#000000" fill="#ffffff" id="svg_43543_10" d="m29,45c0.5,21 21.5,38 43,37"/>
  <path stroke-width="2" stroke="#000000" fill="#ffffff" id="svg_43543_12" d="m93,82c30,0 51,-14 50,-38"/>
  <path stroke-width="2" stroke="#000000" fill="#ffffff" id="svg_43543_13" d="m146,160c0.5,-23 10.5,-41.5 28,-42c17.5,-0.5 27.5,21.5 28,42"/>
  <path stroke-width="2" stroke="#000000" fill="#ffffff" id="svg_43543_14" d="m198,41c1.5,18 -22.5,36.5 -34,46c-11.5,9.5 -46.5,25.5 -71,36"/>
  <path stroke-width="2" stroke="#000000" fill="#ffffff" id="svg_43543_15" d="m76,130c-22,9.5 -46,22.5 -47,34"/>
  <text transform="matrix(1, 0, 0, 0.9, 0, 3.9)" xml:space="preserve" text-anchor="middle" font-family="serif" font-size="12" stroke-width="0" stroke="#000000" fill="#000000" id="svg_43543_16" y="16" x="156">op</text>
  <text id="svg_43543_17" transform="matrix(1, 0, 0, 0.9, 0, 3.9)" xml:space="preserve" text-anchor="middle" font-family="serif" font-size="12" stroke-width="0" stroke="#000000" fill="#000000" y="14.8889" x="213">op</text>
  <text id="svg_43543_18" transform="matrix(1, 0, 0, 0.9, 0, 3.9)" xml:space="preserve" text-anchor="middle" font-family="serif" font-size="12" stroke-width="0" stroke="#000000" fill="#000000" y="189.333" x="46">op</text>
  <text id="svg_43543_19" transform="matrix(1, 0, 0, 0.9, 0, 3.9)" xml:space="preserve" text-anchor="middle" font-family="serif" font-size="12" stroke-width="0" stroke="#000000" fill="#000000" y="184.888" x="162">op</text>
 </g>
</svg>

## Extranatural calculus

We set down a few basic lemmas which describe how extranatural transformations compose. These lemmas become very intuitive once one draws string diagrams to accompany them. (Cf. "yanking moves" in the string diagram calculus of adjunctions.)

+-- {: .un_lemma}
###### Lemma 1 ("stalactites")

Let $F \colon C^{op} \times C \to D$ and $G \colon \underbrace{C^{op} \times C \times \cdots \times C^{op} \times C}_{2n} \to D$ be functors. If $\alpha_{x, y_1, \ldots, y_{n-1}, z} \colon F(x, z) \to G(x, y_1, y_1, \ldots, y_{n-1}, y_{n-1}, z)$ is natural in $x,z$ and extranatural in $y_1, \ldots, y_{n-1}$, and $\beta_{y_1, \ldots, y_n} \colon G(y_1, y_1, \ldots, y_n, y_n) \to H$ (for some object $H$ of $D$) is extranatural in $y_1, \ldots, y_n$, then 
$$\beta_{\underbrace{x, \ldots, x}_{n}} \alpha_{\underbrace{x, \ldots, x}_{n+1}}: F(x, x) \to H$$ 
is extranatural in $x$.
=--

<center>
<img src="http://younesse.net/assets/nLab/extranatural+transformation/svg/extranatural+transformation_stalactites.svg" width="450"/>
</center>

+-- {: .un_lemma}
###### Lemma 2 ("stalagmites")
Let $G \colon \underbrace{C^{op} \times C \times \cdots \times C^{op} \times C}_{2n} \to D$ and $H \colon C^{op} \times C \to D$ be functors.  If $\alpha_{y_1, \ldots, y_n} \colon F \to G(y_1, y_1, \ldots, y_n, y_n)$ (for some object $F$ of $D$) is extranatural in $y_1, \ldots, y_n$, and $\beta_{x, y_1, \ldots, y_{n-1}, z} \colon G(x, y_1, y_1, \ldots, y_{n-1}, y_{n-1} ,z) \to H(x,z)$ is natural in $x, z$ and extranatural in $y_1, \ldots, y_{n-1}$, then 
$$\beta_{\underbrace{x, \ldots, x}_{n+1}} \alpha_{\underbrace{x, \ldots, x}_{n}} \colon F \to H(x, x)$$ 
is extranatural in $x$. 
=--

<center>
<img src="http://younesse.net/assets/nLab/extranatural+transformation/svg/extranatural+transformation_stalagmites.svg" width="450"/>
</center>

+-- {: .un_lemma}
###### Lemma 3 ("yanking")

Let $F, H$ be functors of the form $C \to D$, and let $G: \underbrace{C \times C^{op} \times C \times  \ldots \times C^{op} \times C}_{2n+1} \to D$ be a functor. If $\alpha_{x, y_1, \ldots, y_n} \colon F(x) \to G(x, y_1, y_1, \ldots, y_n, y_n)$ is natural in $x$ and extranatural in $y_1, \ldots, y_n$, and if $\beta_{y_1, \ldots, y_n, z} \colon G(y_1, y_1, \ldots, y_n, y_n ,z) \to H(z)$, is natural in $z$ and extranatural in $y_1, \ldots, y_n$, then 
$$\beta_{\underbrace{x, \ldots, x}_{n+1}} \alpha_{\underbrace{x, \ldots x}_{n+1}}: F(x) \to H(x)$$ 
is natural in $x$. 
=--

<center>
<img src="http://younesse.net/assets/nLab/extranatural+transformation/svg/extranatural+transformation_yanking.svg" width="450"/>
</center>


In fact, these lemmas essentially capture "all possible" ways in which extranatural transformations can be composed.  The general statement, which is obtained by combining these, is that if the graphs representing the two transformations can be composed without creating any cycles, then the transformations can be composed. In some detail, if there are no cycles in the composed graph, then it can be shown that each connected components has one of the forms of the compositions in Lemma 1-3.  It then follows from the lemmas (and from the fact that extranaturality can be determined by separation of variables) that each connected component can be replaced by a single edge, and the resulting graph defines the type of the composed transformation.

This can be found in the original paper about extranatural transformations:

* Eilenberg and Kelly, *A generalization of the functorial calculus*, J. Algebra 3 366--375 (1966)

With the operation of "loop-free composition," extranatural transformations with a given target form a [[paracategory]].  And as we vary the source and target categories, they assemble into an [[extraordinary 2-multicategory]].


## Profunctors

One abstract way to describe the structure of extranatural transformations is as an [[extraordinary 2-multicategory]].  Another abstract structure, which arguably arises more naturally in practice (but also includes more data than necessary), is a [[compact closed category|compact closed]] monoidal [[bicategory]], [[double category]], or [[proarrow equipment]].

More should go here, but for now see [[compact closed double category]].

## Related concepts

* [[bifunctor]]

* [[Kelly-Mac Lane graph]]

* [[proof net]]

* [[homotopy]]

* [[transfor]]

  * [[natural transformation]]

    * **extranatural transformation**, [[dinatural transformation]]

  * [[pseudonatural transformation]]

    * [[pseudo-extranatural transformation]]

  * [[lax natural transformation]]

* [[end]]


## References

* {#EilenbergKelly65} [[Samuel Eilenberg]], [[G. Max Kelly]],  §III.5 of: *Closed Categories*, in: *[[Proceedings of the Conference on Categorical Algebra - La Jolla 1965]]*, Springer (1966) 421-562 &lbrack;[doi:10.1007/978-3-642-99902-4](https://doi.org/10.1007/978-3-642-99902-4)&rbrack;

* [[Samuel Eilenberg]], [[G. M. Kelly]], *A generalization of the functorial calculus*, J. Algebra **3&& 3 (1966) 366-375 &lbrack;[doi](http://dx.doi.org/10.1016/0021-8693%2866%2990006-8)&rbrack;

* [[Max Kelly]], [[Saunders MacLane]], _Coherence in closed categories_, JPAA **1** (1971) 97-140 &lbrack;[doi](http://dx.doi.org/10.1016/0022-4049%2871%2990013-2)&rbrack;

A generalization to [[pseudonatural transformations]] can be found in

* J.C. Vidal, J.S. Tur, _A 2-categorial generalization of the concept of institution_, Studia Logica, 2010 [doi](https://10.1007/s11225-010-9268-0)
* Alexander S. Corner, _A universal characterisation of codescent objects_, [TAC](http://tac.mta.ca/tac/volumes/34/24/34-24abs.html) 34:24, 2019.


[[!redirects extranatural transformations]]
[[!redirects extraordinary natural transformation]]
[[!redirects extraordinary natural transformations]]
[[!redirects extranaturality]]
[[!redirects extraordinary naturality]]
[[!redirects extranatural]]