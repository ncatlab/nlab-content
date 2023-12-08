
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

This page describes aspects of the [[combinatorics]] of [[Cartesian products]] of [[simplicial sets]], mostly by describing (Prop. \ref{NonDegenerateSimplicesInProductOfSimplices}) the non-degenerate simplicices inside a [[Cartesian product]] $\Delta[p] \times \Delta[q]$ of basic [[n-simplices]] for $n = p,q$. These are enumerated by $(p,q)$-(un-)[[shuffles]] in a manner that for [[simplicial abelian groups]] is originally known from the [[Eilenberg-Zilber map]].


## Products of simplicial sets
 {#ProductsOfSimplicialSets}

\begin{proposition}\label{CartesianProductOfSimplicialSetsIsComponentwise}
**([[cartesian product]] of [[simplicial sets]])**\linebreak
For $K, L \,\in\,$ [[SimplicialSets]], their [[Cartesian product]], 

$$
  K \times L
  \;\in\;
  SimplicialSets
$$

is the [[simplicial set]] whose $k$th component [[set]] is the [[Cartesian product]] of [[Sets]] of the components of the two factors

\[
  \label{ComponentSetsOfProductSimplicialSet}
  (K\times L)_k
  \;=\;
  K_k \times L_k
  \,,
\]

and whose face- and degeneracy maps are, similarly, the image under the Cartesian product-[[functor]] of the face- and degeneracy maps of the factors:

\[
  \label{StructureMapsOfProductSimpliciaSet}
  d^{K \times L}_i(x,y) 
  \;=\; 
  \big(
    d^K_i(x), \, d^L_i(y)
  \big)
  \,,
  \;\;\;\;\;
  s^{K \times L}_i(x,y) 
  \;=\; 
  \big(
    s^K_i(x), \, s^L_i(y)
  \big)
\]

\end{proposition}
\begin{proof}  
Since [[SimplicialSets]] is a [[category of presheaves]], namely over the [[simplex category]], this is a special case of the general fact that [[limits of presheaves are computed objectwise]].

But it is also immediate to check that
(eq:StructureMapsOfProductSimpliciaSet) with (eq:ComponentSetsOfProductSimplicialSet)
satisfies the defining [[universal property]] of the [[Cartesian product]].
\end{proof}

\begin{remark}\label{DegenerateSimplicesInProductOfSimplicialSets}
**(degenerate simplices in product of simplicial sets)**
Prop. \ref{CartesianProductOfSimplicialSetsIsComponentwise} 
means in particular that a [[simplex]] 
of the form $\big(s_\alpha(x),\, s_\beta(y)\big) \,\in\, K \times L$  may be non-degenerate even though its two components are each degenerate (see the archetypical Example \ref{NonDegenerateSimplicesInSimplicialSquare} below).

Indeed, the proposition says that the degenerate simplices in $K \times L$ are precisely those such that their two simplex-components in $K$ and $L$, respectively, are in the image of the *same* degeneracy map $\alpha = \beta$.
\end{remark}



## Non-degenerate cells in a product of simplices
 {#NonDegenerateCellsInAProductOfSimplices}

Using the [above](#ProductsOfSimplicialSets) basic facts about products of simplicial sets, we have the following explicit characterization of the non-degenerated cells in products $\Delta[p] \times \Delta[q]$ of the basic [[simplices]] (the simplicial sets [[representable functor|represented]] by the objects in the [[simplex category]]).

### Characterization
 {#Characterization}

\begin{proposition}\label{NonDegenerateSimplicesInProductOfSimplices}
**(non-degenerate $(p+q)$-simplices in $\Delta[p] \times \Delta[q]$)**
\linebreak
For $p,q \,\in\, \mathbb{N}$,
the non-degenerate simplices in the [[Cartesian product]] (Prop. \ref{CartesianProductOfSimplicialSetsIsComponentwise})

$$
  \Delta[p] \times \Delta[q]
$$ 

of standard [[simplices]] in [[sSet]] correspond, under the [[Yoneda lemma]], to precisely those [[morphisms]] of [[simplicial sets]]

\[
  \label{GenericSimplexInProductOfSimplices}
  \Delta[p+q]
  \xrightarrow{\;\; \sigma \;\;}
  \Delta[p] \times \Delta[q]
\]

which satisfy the following equivalent conditions:

* as morphisms of [[posets]] they are [[strictly monotone]];

* as [[permutations]] of $(p+q)$ elements they are $(p,q)$-[[shuffles]];

* as morphisms of [[finitely generated object|finitely generated]] [[categories]] they take generating morphisms to generating morphisms;

\end{proposition}

(e.g. [Kerodon 2.5.7.2](#Kerodon): [00RH](https://kerodon.net/tag/00RH))

Here the first statement says that such morphisms may hence be represented by [[paths]]

* on a $(p+1)\times(q+1)$-lattice,

* from one corner to its opposite corner,

* consisting of $p+q$ unit steps, 

* each either horizontally or vertically

and the second statement says that such paths are characterized by the $(p,q)$-[[shuffle]] $(\mu_1 \lt \cdots \lt \mu_p, \, \nu_1 \lt \cdots \lt \nu_q)$ of lists of step numbers $\mu_i$ where the path proceeds horizontally and step numbers $\nu_i$ where it proceeds vertically:

\begin{tikzcd}[
    sep=30pt
  ]
    &[-12pt]
    &
    \mathclap{
      \color{gray}
      \mu_1 = 1
    }
    &
    \mathclap{
      \color{gray}
      \mu_2 = 4
    }
    &
    \color{gray}
    \cdots
    \\[-20pt]
    &
    {(0,0)}
    \ar[r]
    \ar[d]
    \ar[
      r,-,
      color=blue,
      opacity=.25,
      line width=6pt
    ]
    &
    %
    {(1,0)}
    \ar[r]
    \ar[d]
    \ar[
      d,-,
      color=blue,
      opacity=.25,
      line width=6pt
    ]
    &
    {(2,0)}
    \ar[rr,dotted]
    \ar[d]
    &
    &
    {(p,0)}
    \ar[d]
    \\
    \color{gray}
    \nu_1 = 2
    &
    {(0,1)}
    \ar[r]
    \ar[d]
    &
    {(1,1)}
    \ar[r]
    \ar[d]
    \ar[
      d,-,
      color=blue,
      opacity=.25,
      line width=6pt
    ]
    &
    {(2,1)}
    \ar[rr, dotted]
    \ar[d]
    &
    &
    {(p,1)}
    \ar[d]
    \\
    \color{gray}
    \nu_2 = 3
    &
    {(0,2)}
    \ar[r]
    \ar[dd, dotted]
    &
    {(1,2)}
    \ar[r]
    \ar[dd, dotted]
    \ar[
      r,-,
      color=blue,
      opacity=.25,
      line width=6pt
    ]
    &
    {(2,2)}
    \ar[rr, dotted]
    \ar[dd, dotted]
    \ar[ddrr, dotted]
    \ar[
      ddrr,-,
      color=blue,
      opacity=.25,
      line width=6pt,
      dotted
    ]
    &
    &
    {(p,2)}
    \ar[dd, dotted]
    \\
    \color{gray}
    \vdots
    &
    &
    &
    &&
    \\
    &
    {(0,q)}
    \ar[r]
    &
    {(1,q)}
    \ar[r]
    &
    {(2,q)}
    \ar[rr, dotted]
    &
    &
    {(p,q)}
\end{tikzcd}


\begin{proof}
From Prop. \ref{CartesianProductOfSimplicialSetsIsComponentwise} 
it is clear (Rem. \ref{DegenerateSimplicesInProductOfSimplicialSets}) that a 
simplex $\sigma$ (eq:GenericSimplexInProductOfSimplices) is degenerate 
precisely if, when regarded as a path as above, it contains a [[constant function|constant]] step, i.e. one which moves neither horizontally nor vertically. But then -- by degree reasons, since we are looking at paths of $p + q$ steps in a lattice of side length $p$ and $q$ -- it must be that the path proceeds by $p + q$ unit steps. 
\end{proof}

\begin{remark}\label{NotationForSimplicesInAProductOfSimplices}
**(sequence- and shuffle-notation for simplices in a product of simplices)** \linebreak
Written as a [[pair]] of $(p+q)$-simplices, one in $\Delta[p]$ and one in $\Delta[q]$, the non-degenerate simplex (eq:GenericSimplexInProductOfSimplices) is hence a [[pair]] of [[monotone]] lists of [[natural numbers]]

\[
  \label{ListNotationForProductsOfSimplices}
  \left(
    \begin{array}{ccccccccc}
      0& \ldots & 0 & 1 & \ldots & 1 & 2 & \ldots & p
      \\
      0& \ldots & i & i & \ldots & j & j & \ldots & q
    \end{array}
  \right)
  \,,
\]

such that one row has a constant step precisely where the other has not.

Recording the step numbers where either of these lists is non-constant yields a *$(p,q)$-[[shuffle]]*:

\[
  \label{ShuffleNotationForProductsOfSimplices}
  \begin{array}{cc}
    \text{positions of horizontal steps}
    &
    \text{positions of vertical steps}
    \\
    \mu_1 \lt \mu_2 \lt \cdots \lt \mu_p
    &
    \nu_1 \lt \nu_2 \lt \cdots \lt \nu_p
  \end{array}  
\]

namely a [[permutation]] of $(p+q)$ elements where each element is larger than its left neighbour, except possibly when going from the $p$th to the $p+1$st element.

\end{remark}

The shuffle-data yields a conveniently explicit re-construction of the product of simplices, as follows:


\begin{definition}
For $\mu = (\mu_1 \lt  \mu_2 \lt \cdots \lt \mu_p)$ a sequence of [[natural numbers]] in $\{1, \cdots,  p+q\}$, write

$$
  \sigma_\mu 
  \;\colon\; 
  X_q \to X_{p+q}
$$

for the [[composition|composite]]

$$
  [p+q] 
    \overset{\;\; 
      \sigma_{\mu_q - 1 }  
    \;\;}{\longrightarrow}
  [p+q-1]
    \longrightarrow
    \cdots
    \longrightarrow
  [q + 2]
    \overset{\;\; 
      \sigma_{ \mu_{2} - 1 } 
    \;\;}{\longrightarrow}
   [q + 1]
   \overset{\;\; 
     \sigma_{ \mu_1 - 1 } 
   \;\;}{\longrightarrow}
   [q]
  \,,
$$

where $\sigma_i \,\colon\, [n+1] \to [n]$ denotes  the [[surjective map|surjective]] [[monotone map]] (the [[codegeneracy map]]) that repeats the index $i$.

\end{definition}

\begin{proposition}
The non-degenerate simplices in the [[Cartesian product]] (Prop. \ref{CartesianProductOfSimplicialSetsIsComponentwise})

$$
  \Delta[p] \times \Delta[q]
$$ 

of [[simplices]] in [[sSet]] are precisely those of the form 

$$
  (\sigma_\nu, \sigma_\mu) 
    \;\in\; 
  Hom\big(
    \Delta[p + q]
    ,\,
    \Delta[p] \times \Delta[q]
  \big)
  \;=\;
  \big(
    \Delta[p] \times \Delta[q]
  \big)_{p+q}
$$ 

for $(\mu,\nu)$ a $(p,q)$-[[shuffle]].


\end{proposition}

\linebreak


### Examples
 {#Examples}

\begin{example}\label{CylindersOfSimplices}
**([[cylinders]] of [[simplices]])**

The non-degenerate (n+1)-simplices in the [[cylinder]] over the [[n-simplex]]
$$
  \begin{aligned} 
           & \Delta[1] 
    \\ 
    \times & \Delta[n] 
  \end{aligned}
  \;\in\;
  sSet
$$ 

are, according to Prop. \ref{CartesianProductOfSimplicialSetsIsComponentwise}
 and in the notation of Remark \ref{NotationForSimplicesInAProductOfSimplices}, as follows:

$$
  \begin{array}{cc}
  \text{path} &\phantom{A}& (1,n)\text{-shuffle}
  \\
  \phantom{A}
  \\
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 1 & 1 & 1 & 1 & \cdots & 1 & 1
    \mathrlap]
    \\
    \mathllap[
    0 & 0 & 1 & 2 & 3 & \cdots & n-1 & n
    \mathrlap]
  }
  \;\,
  \right)
  &&
  \Big(
    1
    ,
    \;
    2, 3, 4, 5, 6, \cdots, n
  \Big)
  \,,
  \\
  \phantom{A}
  \\
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 0 & 1 & 1 & 1 & \cdots & 1 & 1
    \mathrlap]
    \\
    \mathllap[
    0 & 1 & 1 & 2 & 3 & \cdots & n-1 & n
    \mathrlap]
  }
  \;\,
  \right)
  &&
  \Big(
    2
    ,\;
    1, 3, 4, 5, 6, \cdots, n
  \Big)
  \\
  \phantom{A}
  \\
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 0 & 0 & 1 & 1 & \cdots & 1 & 1
    \mathrlap]
    \\
    \mathllap[
    0 & 1 & 2 & 2 & 3 & \cdots & n-1 & n
    \mathrlap]
  }
  \;\,
  \right)
  &&
  \Big(
    3
    ,\;
    1, 2, 4, 5, 6,  \cdots, n
  \Big)
  \\
  \phantom{A}
  \\
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 0 & 0 & 0 & 1 & \cdots & 1 & 1
    \mathrlap]
    \\
    \mathllap[
    0 & 1 & 2 & 3 & 3 & \cdots & n-1 & n
    \mathrlap]
  }
  \;\,
  \right)
  &&
  \Big(
    4
    ,\;
    1, 2, 3, 5, 6 \cdots, n
  \Big)
  \end{array}
$$

and so on.

\end{example}




\begin{example}
\label{NonDegenerateSimplicesInSimplicialSquare}
**(non-degenerate simplices in [[simplicial set|simplicial]] [[square]])**
\linebreak
The complete set of non-degenerate simplices in 
$\Delta[1] \times \Delta[1]$
is, in specialization of Example \ref{CylindersOfSimplices}, 
according to Prop. \ref{CartesianProductOfSimplicialSetsIsComponentwise}
and in the notation of Remark \ref{NotationForSimplicesInAProductOfSimplices}, 
the following:

  \begin{tikzcd}
    \scalebox{.8}{$
      \left( {[0]} \atop {[0]} \right)
    $}
    \ar[
      rr,
      "{
        \left(
        {[0,0]}
        \atop
        {[0,1]}
        \right)
      }"{above, scale=.8}
    ]
    \ar[
      dd,
      "{
        \left(
        {[0,1]}
        \atop
        {[0,0]}
        \right)
      }"{left, scale=.8}
    ]
    \ar[
      ddrr,
      "{
        \left(
        { [0,1] }
        \atop
        { [0,1] }
        \right)
      }"{description, scale=.8}
    ]
    &&
    \scalebox{.8}{$
      \left( {[0]} \atop {[1]} \right)
    $}
    \ar[
      dd,
      "{
        \left(
        {[0,1]}
        \atop
        {[1,1]}
        \right)
      }"{right, scale=.8}
    ]
    \ar[
      ddll,
      phantom,
      "{
        \left(
        { [0,0,1] }
        \atop
        { [0,1,1] }
        \right)
      }"{pos=.15, scale=.8}
    ]
    \ar[
      ddll,
      phantom,
      "{
        \left(
        { [0,1,1] }
        \atop
        { [0,0,1] }
        \right)
      }"{pos=.85, scale=.8}
    ]
    \\
    \\
    \scalebox{.8}{$
      \left( {[1]} \atop {[0]} \right)
    $}
    \ar[
      rr,
      "{
        \left(
        {[1,1]}
        \atop
        {[0,1]}
        \right)
      }"{below, scale=.8}
    ]
    &&
    \scalebox{.8}{$
      \left( {[1]} \atop {[1]} \right)    
    $}
  \end{tikzcd}

See also [Friedman 2008, Fig. 20](#Friedman08).
\end{example}





\begin{example}
  The non-degenerate simplices in 
  $$
    \begin{aligned}
      & \Delta[2]
      \\
      \times & \Delta[1]
    \end{aligned}
  $$
  are, in specialization of Example \ref{CylindersOfSimplices}, 
  according to Prop. \ref{CartesianProductOfSimplicialSetsIsComponentwise}
  and in the notation of Remark \ref{NotationForSimplicesInAProductOfSimplices}, 
  the following three:

$$
  \begin{array}{cc}
  \text{ path }
  &&
  (2,1)\text{-shuffle}
  \\
  \phantom{A}
  \\
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 1 & 2 & 2
    \mathrlap]
    \\
    \mathllap[
    0 & 0 & 0 & 1 
    \mathrlap]
  }
  \;\,
  \right)
  &\phantom{AA}&
  \Big(
     1, 2 , \; 3
  \Big)
  \\
  \phantom{A}
  \\
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 1 & 1 & 2
    \mathrlap]
    \\
    \mathllap[
    0 & 0 & 1 & 1 
    \mathrlap]
  }
  \;\,
  \right)
  &&
  \Big(
     1, 3 , \; 2
  \Big)
  \\
  \phantom{A}
  \\
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 0 & 1 & 2
    \mathrlap]
    \\
    \mathllap[
    0 & 1 & 1 & 1 
    \mathrlap]
  }
  \;\,
  \right)
  &&
  \Big(
     2, 3 , \; 1
  \Big)
  \end{array}
$$  

\end{example}

\begin{example}
  Some non-degenerate simplices in $\Delta[2] \times \Delta[2]$:

$$
  \begin{array}{cc}
    \text{path} &\phantom{AA}& (2,2)\text{-shuffle} 
    \\
    \phantom{A}
    \\
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 1 & 2 & 2 & 2
    \mathrlap]
    \\
    \mathllap[
    0 & 0 & 0 & 1 & 2 
    \mathrlap]
  }
  \;\,
  \right)
  &&
  \Big(
    1, 2, \; 3, 4
  \Big)
  \\
  \phantom{AA}
  \\
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 1 & 1 & 2 & 2
    \mathrlap]
    \\
    \mathllap[
    0 & 0 & 1 & 1 & 2 
    \mathrlap]
  }
  \;\,
  \right)
  &&
  \Big(
    1, 3, \; 2, 4
  \Big)
  \\
  \phantom{AA}
  \\
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 1 & 1 & 1 & 2
    \mathrlap]
    \\
    \mathllap[
    0 & 0 & 1 & 2 & 2 
    \mathrlap]
  }
  \;\,
  \right)
  &&
  \Big(
    1, 4, \; 2, 3
  \Big)
  \\
  \phantom{AA}
  \\
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 0 & 0 & 1 & 2
    \mathrlap]
    \\
    \mathllap[
    0 & 1 & 2 & 2 & 2 
    \mathrlap]
  }
  \;\,
  \right)
  &&
  \Big(
    3, 4, \; 1, 2
  \Big)
  \end{array}
$$

\end{example}


\linebreak


## Related concepts

* [[Eilenberg-Zilber map]]

## References

The shuffle-formula is due (in terms of [[simplicial abelian groups]] of [[cochain on a simplicial set|chains on a simplicial set]], see at *[[Eilenberg-Zilber map]]*) to:

* [[Samuel Eilenberg]], [[Saunders MacLane]], (5.3) in: *On the groups $H(\Pi,n)$*, I, Ann. of Math. (2) 58, (1953), 55&#8211;106. ([jstor:1969820](https://www.jstor.org/stable/1969820))

following:

* [[Samuel Eilenberg]], [[Joseph A. Zilber]], American Journal of Mathematics Vol. 75, No. 1 (Jan., 1953), pp. 200-204 ([jstor:2372629](https://www.jstor.org/stable/2372629), [doi:10.2307/2372629](https://doi.org/10.2307/2372629))

The streamlined perspective of strictly monotonic morphisms $\Delta[p+q] \to \Delta[p] \times \Delta[q]$ is highlighted in 

* {#Kerodon} [[Kerodon]], 2.5.7.2 *$(p,q)$-Shuffles* ([00RH](https://kerodon.net/tag/00RH))



Exposition:

* {#Friedman08} [[Greg Friedman]], §5 of: _An elementary illustrated introduction to simplicial sets_, Rocky Mountain J. Math. 42(2): 353-423 (2012) ([arXiv:0809.4221](http://arxiv.org/abs/0809.4221), [doi:10.1216/RMJ-2012-42-2-353](https://projecteuclid.org/journals/rocky-mountain-journal-of-mathematics/volume-42/issue-2/Survey-Article-An-elementary-illustrated-introduction-to-simplicial-sets/10.1216/RMJ-2012-42-2-353.full))

Textbook accounts:

* {#Friedman20} [[Greg Friedman]], §2.5.1 & §B.6 in: *Singular Intersection Homology*,  Cambridge University Press 2020 ([doi:10.1017/9781316584446](https://doi.org/10.1017/9781316584446), [pdf](http://faculty.tcu.edu/gfriedman/IHbook.pdf))


[[!redirects products of simplices]]

[[!redirects product of simplicial sets]]
[[!redirects products of simplicial sets]]

[[!redirects Cartesian product of simplices]]
[[!redirects Cartesian products of simplices]]

