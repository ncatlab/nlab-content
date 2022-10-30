
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _homotopy coherent diagram_ is a [[diagram]] of [[object]]s in a [[homotopical category]], where [[commutative diagram|commutativity]] is replaced by explicit [[homotopies]], those homotopies are to then be [[coherent]]ly linked by higher homotopies ... and so on. 

It is a model for an [[(∞,1)-functor]].

The idea perhaps intuitively makes sense but the management of the interactions between the various levels of homotopy requires care. The ideas were handled in various ways , but we will concentrate on approaches linked to the initial work of [[Michael Boardman]] and [[Rainer Vogt]] and then developed further by [[Jean-Marc Cordier]] and [[Tim Porter]]. 

We will often use h.c. as an abbreviation for ''homotopy coherent''.


## Definition 

### In components

The original definition of [Vogt, 1973](#Vogt) is essentially the following.

Suppose now that we have the h.c. diagram $F : S(\mathbb{A}) \to \mathcal{B}$.  This is specified by assignments:

* to each [[object]] $a$ of $\mathbb{A}$, it assigns an object $F(a)$ of $\mathcal{B}$;

* for each string of composable [[morphism]]s in $\mathbb{A}$,

$$\sigma = (f_0, \ldots, f_n)$$

starting at $a$ and ending at $b$, a simplicial map

$$F(\sigma) : S(\mathbb{A})(0,n+1) \to \mathcal{B}(F(a), F(b)),$$

that is, a higher homotopy

$$F(\sigma) : \Delta[1]^n \to \mathcal{B}(F(a), F(b)),$$

such that

(i) if $f_0 = id$, $F(\sigma) = F(\partial_0\sigma)(proj \times \Delta[1]^{n-1})$

(ii) if $f_i = id$, $0\lt i \lt n$

$$F(\sigma) = F(\partial_i\sigma(.(I^i \times m \times I^{n-i}),$$ 

where $m : I^2 \to I$ is the multiplicative structure on $I = \Delta[1]$ by the 'max' function on $\{0,1\}$;

(iii) if $f_n = id$, $F(\sigma) = F(\partial_n \sigma)(I^{n-1} \times proj)$;

(iv)$_{i}$  $F(\sigma)|(I^{i-1}\times \{0\} \times I^{n-i}) = F(\partial_i\sigma), 1 \leq i \leq n-1$;

(v)$_{i}$  $F(\sigma)|( I^{i-1}\times \{1\} \times I^{n-i}) = F(\sigma^\prime_i) . F(\sigma_i)$, where $\sigma_i = (f_0, \ldots, f_{i-1})$ 
and $\sigma^\prime = (f_i, \ldots, f_n)$.  We have used $\partial_i$ for the face operators in the nerve of $\mathbb{A}$.


This original form can be very useful for checking (bare hands!) within an application that a diagram <i>is</i> h.c., although the $SSet$-functor approach is for many uses more compact and maniable and allows functorial constructions more easily. The link with the [[bar construction]] and [[comonadic resolution]] approaches give suggestive links to interpretation of cohomology classes.


### As algebras over an operad.

For $\mathcal{E}$ a [[symmetric monoidal category]], and $C$ a small $\mathcal{E}$-[[enriched category]],
there is an [[operad]] $Diag_C$ whose [[algebras over an operad]] are $\mathcal{E}$-[[enriched functor]]s

$$
  F : C \to \mathcal{E} 
$$

hence $C$-[[diagram]]s in $\mathcal{E}$.

If $\mathcal{E}$ is also a [[monoidal model category]] with an [[interval object]] $H$ in a sufficiently nice way, then there exists the [[Boardman-Vogt resolution]] 

$$
  HoCoDiag_C := W(H, Diag_C)
  \,.
$$

The algebras over this operad are then precisely homotopy coherent diagrams over $C$ in $\mathcal{E}$. For $\mathcal{E} = $ [[Top]] regarded with the standard [[model structure on topological spaces]] and $H = [0,1]$ the standard interval, this reproduces the ordinary notion of homotopy coherent diagrams ([BergerMoerdijk](#BergerMoerdijkAlgebras))





## Properties


### Equivalence 

(i) If $X : \mathbf{A}\to $ [[Top]] is a commutative diagram and we
replace some of the $X(a)$ by homotopy equivalent $Y(a)$ with specified
homotopy equivalence data:

$$f(a) : X(a) \to Y(a), \quad g(a) : Y(a) \to X(a)$$

$$H(a) : g(a)f(a) \simeq Id, \quad K(a) : f(a)g(a) \simeq Id,$$

then we can combine these data into the construction of a h. c. diagram $Y$
based on the objects $Y(a)$ and homotopy coherent maps 

$$f : X\to Y, \quad g : 
Y \to X,  etc.,$$

making $X$ and $Y$ homotopy equivalent as h.c. diagrams.

(This applied to a $G$-space, $X$, shows that if we replace $X$ by 
a homotopy equivalent $Y$, then $Y$ will be a h. c. version of a $G$-space, i.e. a
h. c. diagram of shape $BG$, the corresponding one object groupoid to $G$.)

### Homotopy coherent nerve



+-- {: .un_theorem}
###### Theorem
**Cordier (1980)**

For each a [[small category]] $\mathbb{A}$, the [[sSet]]-[[enriched category]]
${S(\mathbb{A})}$ defined in [[homotopy coherent nerve#the_cosimplicial_category]] is such that a
h.c. diagram of shape ${\mathbb{A}}$ in [[Top]] is given precisely by an 
[[sSet]]-[[enriched functor]]

$$
  F : {S(\mathbb{A})} \to Top
$$

=--

This suggested the extension of h.c. diagrams to other contexts such as a
general locally Kan $SSet$-category, $\mathcal{B}$ and suggests the definition of homotopy coherent diagram in a $\mathcal{S}$-category and thus a [[homotopy coherent nerve]] of an $SSet$-category.


To understand simplical h.c. diagrams and thus the h.c. simplicial [[nerve]] $N(\mathcal{B})$, we  unpack the definition of homotopy coherence, for conveneince, repeating some points made in [[homotopy coherent nerve]].


The first thing to note is that for any $n$ and $0\leq i\lt j\leq n$, $S[n](i,j) \cong \Delta[1]^{j-i-1}$, the $(j-i-1)$-cube given by the product of $j-i-1 $ copies of $\Delta[1]$.  Thus we can reduce the higher homotopy data to being just that, maps from higher dimensional cubes.

Next some notation:

Given simplicial maps

$$f_1: K_1 \to \mathcal{B}(x,y),$$

$$f_2: K_2 \to \mathcal{B}(y,z),$$

we will denote the composite

$$K_1 \times K_2 \to \mathcal{B}(x,y)\times \mathcal{B}(y,z) \stackrel{c}{\to} \mathcal{B}(x,z)$$

just by $f_2.f_1$ or $f_2f_1$.  (We already have seen this in the h.c. diagram above for 
$\mathbb{A} = [3]$.  $X(123)X(01)$ is actually $X(123)(I \times X(01) )$, whilst $X(23)X(012)$ is exactly what it states.)



### Rectification

Every homotopy coherent diagram is weakly equivalent to a strict diagram, a phenomenon known as _[[rectification]]_.

#### Vogt's theorem

+-- {: .un_theorem}
###### Theorem
**(Vogt)**

If $\mathbf{A}$ is a small category, there is a category $\mathbf{Coh(A,Top)}$
  of h.c. diagrams and homotopy classes of h. c. maps between them.  Moreover
  there is an equivalence of categories

$$\mathbf{Coh(A,Top)} \stackrel{\simeq}{\to} \mathbf{Ho(Top^A)}.$$

=--


#### Berger-Moerdijk theorem

If we think of hc diagrams as algebras over an operad, then this rectification is a special case of the general rectification theorem for such algebras. See [[model structure on algebras over an operad]] for details.


## Examples 

**h.c. diagrams in a category with [[cylinder functor]], denoted $-\times I$**

1.  A diagram indexed by the small category, $[2]$.

<div style="width: 167px; margin: auto">
<svg width="167" height="103" xmlns="http://www.w3.org/2000/svg" xmlns:svg="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" xmlns:math="http://www.w3.org/1998/Math/MathML" se:nonce="36876">
 <g>
  <title>Layer 1</title>
  <foreignObject height="24" width="32" font-size="16" id="svg_36876_1" y="67" x="0">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>X</mi>
      <mo stretchy="false">(</mo>
      <mn>0</mn>
      <mo stretchy="false">)</mo>
     </mrow>
     <annotation encoding="application/x-tex">X(0)</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_36876_2" height="24" width="32" font-size="16" y="0" x="67">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>X</mi>
      <mo stretchy="false">(</mo>
      <mn>1</mn>
      <mo stretchy="false">)</mo>
     </mrow>
     <annotation encoding="application/x-tex">X(1)</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_36876_11" height="24" width="32" font-size="16" y="67" x="134.5">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>X</mi>
      <mo stretchy="false">(</mo>
      <mn>2</mn>
      <mo stretchy="false">)</mo>
     </mrow>
     <annotation encoding="application/x-tex">X(2)</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="32" font-size="16" id="svg_36876_20" y="29" x="18">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mstyle scriptlevel="1">
       <mrow>
        <mi>X</mi>
        <mo stretchy="false">(</mo>
        <mn>01</mn>
        <mo stretchy="false">)</mo>
       </mrow>
      </mstyle>
     </mrow>
     <annotation encoding="application/x-tex">\scriptsize{X(01)}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_36876_21" height="20" width="32" font-size="16" y="82.5" x="67">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mstyle scriptlevel="1">
       <mrow>
        <mi>X</mi>
        <mo stretchy="false">(</mo>
        <mn>02</mn>
        <mo stretchy="false">)</mo>
       </mrow>
      </mstyle>
     </mrow>
     <annotation encoding="application/x-tex">\scriptsize{X(02)}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_36876_32" height="20" width="32" font-size="16" y="29.5" x="118.5">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mstyle scriptlevel="1">
       <mrow>
        <mi>X</mi>
        <mo stretchy="false">(</mo>
        <mn>12</mn>
        <mo stretchy="false">)</mo>
       </mrow>
      </mstyle>
     </mrow>
     <annotation encoding="application/x-tex">\scriptsize{X(12)}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_36876_43" height="20" width="36" font-size="16" y="49.5" x="61.5">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mstyle scriptlevel="1">
       <mrow>
        <mi>X</mi>
        <mo stretchy="false">(</mo>
        <mn>012</mn>
        <mo stretchy="false">)</mo>
       </mrow>
      </mstyle>
     </mrow>
     <annotation encoding="application/x-tex">\scriptsize{X(012)}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <line marker-end="url(#se_marker_end_svg_36876_54)" id="svg_36876_54" y2="24.5" x2="72.5" y1="72.5" x1="29.5" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_36876_55)" id="svg_36876_55" y2="69.5" x2="132.5" y1="22.5" x1="89.5" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="null" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_36876_56)" id="svg_36876_56" y2="80.5" x2="127.5" y1="80" x1="33" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="null" stroke-width="2" stroke="#000000" fill="none"/>
 </g>
 <defs>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_36876_54">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_36876_55">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_36876_56">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
 </defs>
</svg>
</div>

is h.c. if there is specified a homotopy 

$$X(012) : X(0)\times I \to X(2),$$

$$X(012) : X(02) \simeq X(12)X(01).$$

1. For a diagram indexed by $[3]$: Draw a 3-simplex, marking the vertices
$X(0), \ldots, X(3)$, the edges $X(ij)$, etc., the faces $X(ijk)$, etc.  The 
homotopies $X(ijk)$ fit together to make the sides of a square

$$
 \begin{matrix}
  X(1 3)X(0 1)&\xrightarrow{X(1 2 3)X(0 1)}&X(2 3)X(1 2)X(0 1)\\
  \mathllap{X(0 1 3)}\left\uparrow\space{30}{20}{0}\right.& &\left.\space{30}{20}{0}\right\uparrow\mathrlap{X(2 3) X(0 1 2)}\\
  X(0 3)&\xrightarrow[\qquad X(0 2 3)\qquad]{\quad}&X(2 3)X(0 2)
 \end{matrix}
$$
and the
diagram is made h.c. by specifying a second level homotopy 

$$X(0123) : X(0)\times I^2\to X(3)$$

filling this square, in the sense that restricting to each side of the square in the double homotopy gives the correspondingly labelled homotopy from the diagram.



These can be continued for larger $[n]$, and the results glued together to
make larger h.c. diagrams.  Of course, this is not how it is done, but it
provides some understanding of the basic idea.  





## References

For [[Rainer Vogt|Vogt]]'s theorem, the original reference is 

* {#Vogt} [[Rainer Vogt]], _Homotopy limits and colimits_, Math. Z., 134 (1973) 11-52. 


A generalisation of his theorem using simplicially enriched categories and the [[homotopy coherent nerve]] of such a thing, is to be found in

* [[J.-M. Cordier]] and [[T. Porter]], _Vogt's Theorem on Categories of Homotopy Coherent Diagrams_,  Math. Proc. Camb. Phil. Soc. 100 (1986) pp. 65-90.


A neat application to changing objects in diagrams within a homotopy type can be found in

* J.-M. Cordier and T. Porter, _Maps between homotopy coherent diagrams_, Top. and its Appls.,  28, (1988), 255 &#8211; 275.

See also 

* [[William Dwyer]], [[Dan Kan]], [[Jeff Smith]], _Homotopy commutative diagrams and their realizations_, Journal of Pure and Applied Algebra 57 (1989) 5-24 (<a href="https://doi.org/10.1016/0022-4049(89)90023-6">doi:10.1016/0022-4049(89)90023-6</a>)

A summary of homotopy coherence can be found in Chapter 5 of 

* [[K. H. Kamps]] and T. Porter, _Abstract Homotopy and Simple Homotopy Theory_ ([GoogleBooks](http://books.google.de/books?id=7JYKxInRMdAC&dq=Porter+Kamps&printsec=frontcover&source=bl&ots=uuyl_tIjs4&sig=Lt8I92xQBZ4DNKVXD0x76WkcxCE&hl=de&sa=X&oi=book_result&resnum=3&ct=result#PPP1,M1))

and in chapter 10 of 

* [[Tim Porter]], _[[Crossed Menagerie]]_

The operad-theoretic description of homotopy-coherent diagrams is in

* {#BergerMoerdijkAlgebras}[[Clemens Berger]], [[Ieke Moerdijk]], _Resolution of coloured operads and rectification of homotopy algebras_ ([arXiv:math/0512576](http://arxiv.org/abs/math/0512576))


See [[model structure on algebras over an operad]] for more on this.

[[!redirects homotopy coherent diagrams]]

[[!redirects Vogt's theorem]]

[[!redirects homotopy coherent functor]]
[[!redirects homotopy coherent functors]]

[[!redirects homotopy commutative diagram]]
[[!redirects homotopy commutative diagrams]]

