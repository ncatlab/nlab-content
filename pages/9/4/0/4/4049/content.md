
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

The notion of _$V$-enriched natural transformation_ is the appropriate notion of [[homomorphism]] between [[enriched functors]], the analog in [[enriched category theory]] of the ordinary notion of [[natural transformation]] in ordinary [[category theory]].

$V$-Enriched natural transformations constitute the [[2-morphisms]] in the [[2-category]] [[VCat]].

## Definition 
 {#Definition}

For $V$ a [[cosmos for enrichment]], let 

* $\mathbf{C}$, $\mathbf{D}$ be a [[pair]] of $V$-[[enriched categories]]

  (we denote their [[hom-objects]] by $C(-, -)$ etc., instead of $\hom_C(-, -)$ or similar),

* $F, G \,\colon\, \mathbf{C} \longrightarrow \mathbf{D}$ a [[pair]] of $V$-[[enriched functors]] between them. 

Then:

\begin{definition}
\label{EnrichedNaturalTransformation}
An **enriched natural transformation** between these enriched functors

$$
  \eta \colon F \longrightarrow G
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

\[\label{ExtranaturalitySquare}\]
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

\end{definition}
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



## Properties


### As 2-morphisms

In generalization of how for plain [[natural transformations]] there is a notion of [[horizontal composition]] ("[[whiskering]]") and [[vertical composition]], so for enriched natural transformations:

\begin{proposition}\label{RightWhiskering}
**(horizontal composition)**
\linebreak
Given

\begin{tikzcd}
  \mathbf{C}
  \ar[
    rr,
    bend left=30,
    "{ F }",
    "{\ }"{name=s, swap}
  ]
  \ar[
    rr,
    bend right=30,
    "{ G }"{swap},
    "{\ }"{name=t}
  ]
  \ar[
     from=s,
     to=t,
     Rightarrow,
     shorten=10pt,
     "{ \eta }"
  ]
  &&
  \mathbf{D}
  \ar[
    rr,
    "{ H }"
  ]
  &&
  \mathbf{E}
\end{tikzcd}

where

1. $\eta$ is an enriched natural transformation (Def. \ref{EnrichedNaturalTransformation}) 

1. $H$ is an [[enriched functor]]

then we obtain an enriched natural transformation of the form

\begin{tikzcd}   
  \mathbf{C}
  \ar[
    rr,
    bend left=30,
    "{ H \circ F }",
    "{\ }"{name=s, swap}
  ]
  \ar[
    rr,
    bend right=30,
    "{ H \circ G }"{swap},
    "{\ }"{name=t}
  ]
  \ar[
     from=s,
     to=t,
     Rightarrow,
     shorten=10pt,
     "{ H(\eta) }"
  ]
  &&
  \mathbf{E}
\end{tikzcd}

with component maps given as the [[composition]]

$$
  I 
  \overset{\eta_c}{\longrightarrow}
  \mathbf{D}\big(F(c),\,G(c)\big)
  \overset{H_{F(c), G(c)}}{\longrightarrow}
  \mathbf{E}\big(H \circ F(c),\,H \circ G(c)\big)
  \,.
$$
\end{proposition}


### Relation to strong natural transformations

For [[closed monoidal categories]] $V$ there is a close relation between $V$-enriched natural transformations and $V$-[[strong natural transformations]].

For the moment see at *[enriched monad -- relation to strong monads](enriched+monad#RelationToStrongMonads)* for more.



## Examples

\begin{example}
  With [[Set]] denoting the category of [[sets]] and [[functions]] equipped with its [[cartesian monoidal category|cartesian monoidal]]-[[structure]] (via [[Cartesian product]] of sets), [[Set]]-enriched natural transformations are just plain [[natural transformations]] between [[functors]] between [[locally small categories]].
\end{example}

\begin{example}
\label{StrictTwoNaturalTransformations}
 With *[[Cat]]* denoting the [[1-category]] of [[small category|small]] [[strict categories]] equipped with its [[cartesian monoidal category|cartesian monoidal]] [[structure]] (via forming [[product categories]]), $Cat$-enriched natural transformations are also known as *[[strict 2-natural transformations]]*.
\end{example}


## Related concepts

* [[strong natural transformation]]

* [[enriched functor]]

* [[enriched functor category]]

* [[enriched adjoint functor]]


## References

* {#EilenbergKelly65} [[Samuel Eilenberg]], [[G. Max Kelly]],  §I.10 of: *Closed Categories*, in: *[[Proceedings of the Conference on Categorical Algebra - La Jolla 1965]]*, Springer (1966) 421-562 &lbrack;[doi:10.1007/978-3-642-99902-4](https://doi.org/10.1007/978-3-642-99902-4)&rbrack;

* [[Max Kelly]], p. 9 of: _Basic Concepts of Enriched Category Theory_, Cambridge University Press, Lecture Notes in Mathematics **64** (1982), Reprints in Theory and Applications of Categories, **10** (2005) 1-136 &lbrack;[tac:tr10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf)&rbrack;

* {#Borceux94} [[Francis Borceux]], def. 6.2.4 of: _[[Handbook of Categorical Algebra]] Vol 2_, Cambridge University Press (1994)

* [[Emily Riehl]], §3.5 in *[[Categorical Homotopy Theory]]*, Cambridge University Press (2014) &lbrack;[doi:10.1017/CBO9781107261457](https://doi.org/10.1017/CBO9781107261457), [pdf](http://www.math.jhu.edu/~eriehl/cathtpy.pdf)&rbrack;


For more references see at _[[enriched category]]_.


[[!redirects enriched natural transformation]]
[[!redirects enriched natural transformations]]

[[!redirects enriched natural isomorphism]]
[[!redirects enriched natural isomorphisms]]
