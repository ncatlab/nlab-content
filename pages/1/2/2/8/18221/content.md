
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

One may consider [[internal categories]] in [[homotopy type theory]]. Under the [[relation between type theory and category theory|interpretation]] of [[HoTT]] in an [[(infinity,1)-topos]], this corresponds to the concept of a [[category object in an (infinity,1)-category]]. The general idea is presented there at _[Homotopy Type Theory Formulation](category+object+in+an+%28infinity%2C1%29-category#HomotopyTypeTheoryFormulation)_.

For internal [[1-categories]] in HoTT (as opposed to more general internal [[(infinity,1)-categories]]) a comprehensive discussion was given in ([Ahrens-Kapulkin-Shulman-13](#AhrensKapulkinShulman13)).

In some literature, the "Rezk-completeness" condition on such categories is omitted from the definition, and categories that satisfy it are called *saturated* or *univalent*.

Similarly to the [[univalence axiom]] we make two notions of sameness the same. This leads to some nice concequences.

## Definition ##
In [[homotopy type theory]], there are two notions of "sameness" for objects of a precategory. On one hand we have an [[isomorphism]] between objects $a$ and $b$, on the other hand we have equality of objects $a$ and $b$. 

There is a special kind of category called a **univalent category** where these two notions of equality coincide and some very nice properties arise.

\begin{lemma}
If $A$ is a category and $a,b:A$, then there is a map

$$idtoiso : (a=b) \to (a \cong b)$$
\end{lemma}

\begin{proof}
By induction on identity, we may assume $a$ and $b$ are the same. But then we have $1_a:hom_A(a,a)$, which is clearly an isomorphism. $\square$
\end{proof}

The inverse of $idtoiso$ is denoted $isotoid$.

## Examples ##
Note: All categories given can become univalent via the [[Rezk completion]].

* There is a category $\mathit{Set}$, whose type of objects is $Set$, and with $hom_{\mathit{Set}}(A,B)\equiv (A \to B)$. Under [[univalence]] this becomes a [[category]]. One can also show that any [[category]] of set-level structures such as groups, rings topologicial spaces, etc. is also univalent.

* For any 1-type $X$, there is a univalent category with $X$ as its type of objects and with $hom(x,y)\equiv(x=y)$. If $X$ is a set we call this the **discrete category** on $X$. In general, we call this a **groupoid**.

* For any type $X$, there is a category with $X$ as its type of objects and with $hom(x,y)\equiv \| x= y \|_0$. The composition operation
$$\|y=z\|_0 \to \|x=y\|_0 \to \|y=z\|_0$$
is defined by induction on [[truncation]] from concatenation of the [[identity type]]. We call this the **fundamental groupoid** of $X$.

* There is a category whose type of objects is $\mathcal{U}$ and with $hom(X,Y)\equiv \| X \to Y\|_0$, and composition defined by induction on truncation from ordinary composition of functions. We call this the **homotopy category of types**. 

## Properties ##

\begin{lemma}
In a univalent category, the type of objects is a 1-type.
\end{lemma}

\begin{proof}
It suffices to show that for any $a,b:A$, the type $a=b$ is a set. But $a=b$ is equivalent to $a \cong b$ which is a set. 
\end{proof}

There is a canonical way to turn a [[category]] into a univalent category via the [[Rezk completion]].

## Related pages

* [[type-theoretic definition of category]]

* [[Rezk completion]]

* Particularly useful in the context of such categories are [[displayed categories]].

## References
 {#References}

### General
  {#RefetencesGeneral}



The relation between [[complete Segal space|Segal completeness]] (now often "[[Rezk completion|Rezk completeness]]") for internal categories in HoTT and the [[univalence axiom]] had been pointed out in

* [[Urs Schreiber]], _[Segal completenes and Univalence](https://golem.ph.utexas.edu/category/2012/05/segalcompleteness_and_univalen.html)_ (2012)

A comprehensive discussion for [[1-categories]] then appeared in:

* {#AhrensKapulkinShulman13} [[Benedikt Ahrens]], [[Chris Kapulkin]], [[Michael Shulman]], _Univalent categories and the Rezk completion_, Mathematical Structures in Computer Science **25** 5 (*From type theory and homotopy theory to Univalent Foundations of Mathematics*),  (2015) 1010-1039   $[$[arXiv:1303.0584](https://arxiv.org/abs/1303.0584), [doi:10.1007/978-3-319-21284-5_14](https://doi.org/10.1007/978-3-319-21284-5_14)$]$

Exposition:

* [[Mike Shulman]],  _[Category Theory in Homotopy Type Theory](https://golem.ph.utexas.edu/category/2013/03/category_theory_in_homotopy_ty.html)_, 2013

Discussion of implementation of this in [[Coq]] includes 

* [[Jason Gross]], [[Adam Chlipala]], [[David Spivak]], _Experience Implementing a Performant Category-Theory Library in Coq_ ([arXiv:1401.7694](http://arxiv.org/abs/1401.7694))

[[Coq]] code formalizing this includes the following:

* _[github.com/benediktahrens/rezk_completion](https://github.com/benediktahrens/rezk_completion)_

Generalization to [[(n,1)-categories]] is discussed in

* {#CapriottiKraus17} [[Paolo Capriotti]], [[Nicolai Kraus]], _Univalent Higher Categories via Complete Semi-Segal Types_ ([arXiv:1707.03693](https://arxiv.org/abs/1707.03693))

and, by different means, in

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* ([arXiv:1705.07442](https://arxiv.org/abs/1705.07442))

* {#Riehl18} [[Emily Riehl]], _The synthetic theory of ∞-categories vs the synthetic theory of ∞-categories_, talk at [Vladimir Voevodsky Memorial Conference 2018](http://www.math.ias.edu/vvmc2018) ([pdf](http://www.math.jhu.edu/~eriehl/Voevodsky.pdf))

Formalization of [[bicategories]]:

* [[Benedikt Ahrens]], Dan Frumin, Marco Maggesi, Niels van der Weide, _Bicategories in Univalent Foundations_ ([arXiv:1903.01152](https://arxiv.org/abs/1903.01152))

Lemmas and proofs are taken from 

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)


### By coinduction
  {#ReferencesCoinduction}

A formalization in [[HoTT]]-[[Agda]] of general [[(n,r)-categories]] for $n,r \in \mathbb{N} \sqcup \{\infty\}$, defined as [[coinductive types]] of infinity-graphs, with operations defined by induction-coinduction, is implemented in

* {#Morrison19} Darin Morrison, _[agda-nr-cats](https://github.com/5HT/agda-nr-cats)_, 
_[agda-infinity-categories](https://github.com/freebroccolo/agda-infinity-categories/)

\linebreak





[[!redirects internal categories in homotopy type theory]]

[[!redirects internal category in HoTT]]
[[!redirects internal categories in HoTT]]

[[!redirects internal category theory in homotopy type theory]]
[[!redirects internal category theory in HoTT]]

[[!redirects saturated category]]
[[!redirects univalent category]]
[[!redirects saturated categories]]
[[!redirects univalent categories]]
