
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Idempotents
+-- {: .hide}
[[!include idempotents - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--



# Idempotent adjunctions
* table of contents
{: toc}


## Definition
 {#Definition}


\begin{prop}\label{EquivalentConditionsForIdempotency}
**(equivalent conditions for idempotency)**
\linebreak
Let $F \,\colon\, C \rightleftarrows D \,\colon\, G$ be an [[adjunction]] with [[unit of an adjunction|unit]] $\eta$ and [[counit of an adjunction|counit]] $\varepsilon$.  Then the following conditions on their [[whiskering]] are equivalent:

1. $F \eta$ is a [[natural isomorphism]].

1. $\varepsilon F$ is a natural isomorphism.

1. $G \varepsilon F$ is a natural isomorphism &#8212; i.e. the [[monad]] induced by the adjunction is an [[idempotent monad]].

1. $G F \eta = \eta G F$.

1. $G F \eta G = \eta G F G$.

1. $G\varepsilon$ is a natural isomorphism.

1. $\eta G$ is a natural isomorphism.

1. $F \eta G$ is a natural isomorphism &#8212; i.e. the [[comonad]] induced by the adjunction is an [[idempotent comonad]].

1. $F G \varepsilon = \varepsilon F G$.

1. $F G \varepsilon F = \varepsilon F G F$.

1. {#IdempotentAdjunctionFactoredThroughFixedPoints} The adjunction factors through its [[fixed point of an adjunction|fixed points]] as

   $$
     C
     \underoverset 
       {\underset{G_1}{\hookleftarrow}}  
       {\overset{F_1}{\longrightarrow}}
       {\;\;\; \bot \;\;\;}
     E 
     \underoverset
       {\underset{G_2}{\longleftarrow}}
       {\overset{F_2}{\hookrightarrow}}
       {\;\;\; \bot \;\;\;}
     D
     \,,
   $$ 

   where $F_2$ and $G_1$ are [[fully faithful functor|fully faithful]], i.e. $F_1\dashv G_1$ is a [[reflective subcategory|reflection]] and $F_2 \dashv G_2$ is a [[coreflective subcategory|coreflection]].

\end{prop}
\begin{definition}\label{IdempotentAdjunction}
**(idempotent adjunction)**
\linebreak
When the equivalent conditions from Prop. \ref{EquivalentConditionsForIdempotency} hold, the adjunction is said to be *idempotent*.  
\end{definition}

An original reference for the equivalence of all but the last of these conditions is [MacDonald & Stone 1982, Prop. 2.8](#MacDonaldStone82); a textbook account is in [Grandis 2021, Thm. 3.8.2](#Grandis21). The full statement including the (co)reflective factorization through the fixed points is made explicit in the proof of [Grandis 2021, Thm. 3.8.7](#Grandis21), which also makes explicit that:

+-- {: .num_remark}
###### Remark

For an idempotent adjunction as in def. \ref{IdempotentAdjunction}, the functors $F$ and $G$ restrict to an [[equivalence of categories]] between the [[full images]] of $F$ and of $G$ (which are, respectively, a [[coreflective subcategory]] of $D$ and a [[reflective subcategory]] of $C$, both equivalent to the $E$ in the last item above).  In other words, for an idempotent adjunction, the category of [[fixed point of an adjunction|fixed points]] has a particularly simple form.

=--

+-- {: .num_remark}
###### Remark

If an idempotent adjunction is [[monadic adjunction|monadic]], then (up to equivalence) it consists of the inclusion and reflection of a [[reflective subcategory]] (i.e. the algebras for an [[idempotent monad]]).  Dually, if it is [[comonadic adjunction|comonadic]], it consists of the inclusion and coreflection of a [[coreflective subcategory]].  Thus, the primary interest in isolating the notion of *idempotent adjunction* is when considering adjunctions which are neither monadic nor comonadic.

=--

## Examples

### General

\begin{example}
Any adjunction between [[posets]] is idempotent.  This is a central fact in the theory of [[Galois connections]].  Thus, in a sense, *non-idempotent* adjunctions are an important new idea arising by the "groupoidal" form of [[vertical categorification]].
\end{example}

\begin{example}
More generally, an adjunction in which the [[full image]] of either functor is a [[poset]] must be idempotent.  This follows from conditions 4, 5, 9, and 10 in Prop. \ref{EquivalentConditionsForIdempotency}.  This fact arises when constructing [[generalized kernels]].
\end{example}


\begin{example}
The [[material-structural adjunction]] between [[material set theory|material set theories]] and [[structural set theory|structural set theories]] is idempotent.  The [[fixed point of an adjunction|fixed categories]] consist of the models satisfying appropriate versions of the [[axiom of foundation]] or anti-foundation.
\end{example}

\begin{example}\label{CoCommaAdjunction}
**((co)comma construction)**
\linebreak
The [[comma category]] construction forms part of an adjunction
$$ 
  cocomma 
  \;\colon\; 
  Span(X,Y) 
  \; \rightleftarrows \; 
  Cospan(X,Y)
  \;\colon\; 
  comma 
$$
between [[spans]] and [[cospans]] of categories whose feet are given by categories $X$ and $Y$ ([Shulman 2016](#Shulman16)).
This adjunction is idempotent and factors into the [[reflection]] into [[discrete]] [[two-sided fibrations]] in the category $Span(X,Y)$ and the [[coreflection]] from [[codiscrete cofibrations]] in $Cospan(X,Y)$.
\end{example}


### Involving topological spaces

\begin{example}
The "[[frame of opens]]" and "space of points" functors between [[topological spaces]] and [[locales]] form an idempotent adjunction.  The resulting [[equivalence of categories]] is between [[sober spaces]] (which are reflective in [[Top]]) and [[spatial locales]] (which are coreflective in [[Loc]]).
\end{example}

\begin{example}
For any [[topological space]] $X$, there is an idempotent adjunction between the category $[O(X)^{\op}, Set]$ of [[presheaves]] on $X$ and the [[slice category]] $Top_{/X}$ of [[TopologicalSpaces]] over $X$ (the right adjoint gives the presheaf of [[sections]] of a space over $X$).  The resulting equivalence of categories is between [[sheaves]] in the modern sense of presheaves satisfying [[descent]], and sheaves in the original sense as [[étalé spaces]].  See [this blog post](http://golem.ph.utexas.edu/category/2010/02/sheaves_do_not_belong_to_algeb.html).
\end{example}


### Between topological and diffeological spaces
 {#BetweenTopologicalAndDiffeologicalSpaces}


[[!include adjunction between topological spaces and diffeological spaces]]



## Related concepts

* A [[categorification]] of the notion of idempotent adjunction is that of [[lax-idempotent 2-adjunction]].

* In an [[adjoint triple]], one of the two [[adjoint pairs]] is idempotent if and only if the other one is; see [there](adjoint+triple#Idempotent) for more.

## References

The characterization of idempotent adjunctions is proven/due to:

* {#MacDonaldStone82} [[John L. MacDonald]], [[Arthur L. Stone]], Prop. 2.8 in: *The tower and regular decomposition*, Cahiers de Topologie et Géométrie Différentielle Catégoriques, Tome 23 (1982) no. 2, pp. 197-213 ([numdam:CTGDC_1982__23_2_197_0](http://www.numdam.org/item/?id=CTGDC_1982__23_2_197_0))

Textbook accounts:

* {#Grandis21} [[Marco Grandis]], Section 3.8 in: _Category Theory and Applications: A Textbook for Beginners_, World Scientific 2021 ([doi:10.1142/12253](https://doi.org/10.1142/12253))

See also:

* Alessandro Ardizzoni, José Gómez-Torrecillas, Claudia Menini, Prop. 1.3 in:  *Monadic Decompositions and Classical Lie Theory*,  Appl Categor Struct 23, 93–105 (2015)  ([arXiv:1203.2881](https://arxiv.org/abs/1203.2881), [doi:10.1007/s10485-013-9326-7](https://doi.org/10.1007/s10485-013-9326-7))


The [example of D-topological spaces](#BetweenTopologicalAndDiffeologicalSpaces) inside [[topological spaces|topological]]/[[diffeological spaces]] is due to:

* {#SYH10} [[Kazuhisa Shimakawa]], K. Yoshida, [[Tadayuki Haraguchi]], Section 3 of: _Homology and cohomology via enriched bifunctors_, Kyushu Journal of Mathematics, 2018 Volume 72 Issue 2 Pages 239-252 ([arXiv:1010.3336](https://arxiv.org/abs/1010.3336), [doi:10.2206/kyushujm.72.239]( https://doi.org/10.2206/kyushujm.72.239))


The example \ref{CoCommaAdjunction} of the (co)comma adjunction is also mentioned in:

* {#Shulman16} [[Mike Shulman]], reply [MO:a/247311/381](https://mathoverflow.net/a/247311/381) (2016) to: "An 'explicit' description of cocomma categories?"  






[[!redirects idempotent adjunctions]]