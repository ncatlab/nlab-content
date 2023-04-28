
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea 

An _enriched natural transformation_ is the appropriate notion of [[homomorphism]] between [[enriched functors]], the analog in [[enriched category theory]] of the ordinary notion of [[natural transformation]] in ordinary [[category theory]].


## Definition 

For $V$ a [[cosmos for enrichment]], let 

* $\mathbf{C}$, $\mathbf{D}$ be a [[pair]] of [[enriched categories]]

  (we denote their [[hom-objects]] by $C(-, -)$ etc., instead of $\hom_C(-, -)$ or similar),

* $F, G \,\colon\, \mathbf{C} \longrightarrow \mathbf{D}$ a [[pair]] of $V$-[[enriched functors]] between them. 

Then:

An **enriched natural transformation** between these enriched functors

$$
  \eta \colon F \longrightarrow G'
$$ 

is a [[family]] of [[morphisms]] of $V$ 

$$
  \eta_c
  \;\colon\; 
  I 
    \longrightarrow 
  D(F c, G c)
$$ 

(out of the [[tensor unit]] $I$ of $V$) [[indexed set|indexed]] by  $c\in Ob(C)$)

such that for any [[pair]] of objects $c, c' \,\in\, Obj(\mathbf{C})$ the following [[commuting diagram|diagram commutes]]: 

\begin{tikzcd}
  &
  \mathbf{C}(c,c')
   \otimes 
  I 
  \ar[
    r,
    "{ 
       G_{c,c'} 
        \otimes 
       \eta_c 
    }"
  ]
  &
  \mathbf{D}\big(G(c),\, G(c')\big)
  \otimes
  \mathbf{D}\big(F(c),\, G(c)\big)
  \ar[
    dr,
    "{ \circ^{\mathbf{D}} }"
  ]
  &[-40pt]
  \\
  \mathbf{C}(c, c')
  \ar[
    ur,
    "{ r^{-1} }"
  ]
  \ar[
    dr,
    "{ l^{-1} }"{swap}
  ]
  & & &
  \mathbf{D}\big( F(c) ,\,G(c') \big)
  \\
  & 
  I
    \otimes
  \mathbf{C}(c, c')
  \ar[
    r,
    "{ 
       \eta_{c'} 
         \otimes 
       F_{c,c'}  
    }"{swap}
  ]
  &
  \mathbf{D}\big(F(c'),\, G(c') \big)
  \otimes
  \mathbf{D}\big(F(c),\, F(c')\big)
  \ar[
    ur,
    "{
      \circ^{\mathbf{D}}
    }"{swap}
  ]
\end{tikzcd}

Here

* $\otimes$ denotes the [[tensor product]] in $V$,

* $I$ denotes the [[tensor unit]] in $V$,

* $l$,$r$ denote the left and right [[unitors]] of $V$,

* $F_{c,c'}$, $G_{c,c'}$ denote the component [[maps]] of the [[enriched functors]] between [[hom-objects]],

* $\circ^{\mathbf{D}}$ denotes the [[composition]]-operation of $\mathbf{D}$.

The above diagram expresses the $V$-enriched version of [[commuting diagram|commutativity]] of the plain [[naturality square]]:

$$
  \array{   
    c
    &&
    F(c) &\overset{ \eta_c }{\longrightarrow}& G(c)
    \\
    \mathllap{{}^{f}}
    \Big\downarrow
    &\mapsto\;\;\;&
    \mathllap{{}^{F(f)}}
    \Big\downarrow
    &&
    \Big\downarrow\mathrlap{{}^{G(f)}}
    \\
    c'
    &&
    F(c') &\underset{\eta_{c'}}{\longrightarrow}& G(c')
  }
$$



## Related concepts

* [[enriched functor category]]

* [[enriched adjunction]]

## References

* [[Max Kelly]], p. 9 of: _Basic Concepts of Enriched Category Theory_, Cambridge University Press, Lecture Notes in Mathematics **64** (1982), Reprints in Theory and Applications of Categories, **10** (2005) 1-136 &lbrack;[tac:tr10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf)&rbrack;

* {#Borceux94} [[Francis Borceux]], def. 6.2.4 of: _[[Handbook of Categorical Algebra]] Vol 2_, Cambridge University Press (1994)

* [[Emily Riehl]], chapter 3, _Basics of enriched category theory_ in: _[[Categorical Homotopy Theory]]_, Cambridge University Press (2014) &lbrack;[pdf](http://www.math.jhu.edu/~eriehl/cathtpy.pdf), [doi:10.1017/CBO9781107261457](https://doi.org/10.1017/CBO9781107261457)&rbrack;

For more references see at _[[enriched category]]_.


[[!redirects enriched natural transformation]]
[[!redirects enriched natural transformations]]

[[!redirects enriched natural isomorphism]]
[[!redirects enriched natural isomorphisms]]
