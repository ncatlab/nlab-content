[[!redirects internal category in homotopy type theory]]

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

### In set theory

In general, the notion of [[equivalence of categories]] and [[isomorphism]] of [[categories]] are not the same. However, there is a subclass of categories for which [[equivalence of categories]] are the same as [[isomorphism]] of [[categories]]. These categories are the *univalent* categories. 

### In type theory

One may consider [[internal categories]] in [[homotopy type theory]]. Under the [[relation between type theory and category theory|interpretation]] of [[HoTT]] in an [[(infinity,1)-topos]], this corresponds to the concept of a [[category object in an (infinity,1)-category]]. The general idea is presented there at _[Homotopy Type Theory Formulation](category+object+in+an+%28infinity%2C1%29-category#HomotopyTypeTheoryFormulation)_.

For internal [[1-categories]] in HoTT (as opposed to more general internal [[(infinity,1)-categories]]) a comprehensive discussion was given in ([Ahrens-Kapulkin-Shulman-13](#AhrensKapulkinShulman13)).

In some literature, the "Rezk-completeness" condition on such categories is omitted from the definition, and categories that satisfy it are called *saturated* or *univalent*.

Similarly to the [[univalence axiom]] we make two notions of sameness the same. This leads to some nice concequences.

## Definition ##

### In set theory

\begin{definition}
A **univalent category** is a category $C$ such that the set of isomorphisms $A \cong B$ between every two objects $A \in Ob(C)$ and $B \in Ob(C)$ of $C$ is a [[subsingleton]], and there is an isomorphism $f:A \cong B$ if and only if $A = B$. 

\end{definition}

### In type theory

In a [[dependent type theory]] with some notion of [[identity type]] or [[path type]], there are two notions of "sameness" for objects of a precategory. On one hand we have an [[isomorphism]] between objects $a$ and $b$, on the other hand we have equality of objects $a$ and $b$. 

There is a special kind of category called a **univalent category** where these two notions of equality coincide and some very nice properties arise.

If $A$ is a category and $a,b:A$, then there is a map

$$idtoiso : (a=b) \to (a \cong b)$$

\begin{proof}
By induction on identity, we may assume $a$ and $b$ are the same. But then we have $1_a:hom_A(a,a)$, which is clearly an isomorphism. $\square$
\end{proof}

The inverse of $idtoiso$ is denoted $isotoid$.

A **univalent category** or **saturated category** is a category which satisfies a categorical version of [[antisymmetry]] for [[posets]] called *Rezk completeness*: the canonical function 
$$idtoiso : (a=b) \to (a \cong b)$$
from the identity type between two objects $a$ and $b$ to the type of isomorphisms between $a$ and $b$ is an equivalence of types. 

In [[extensional type theory]], the type theoretic definition and thd set theoretic definitions are equivalent to each other. Every [[identity type]] is a [[proposition]]/[[subsingleton]] in extensional type theory. Thus, by the Rezk completeness condition, the set of isomorphisms is a subsingleton, and two objects which are isomorphic to each other are also equal to each other. 

However, the two definitions are not the same in [[intensional type theory]] for general categories; instead, they only coincide for [[strict categories]], where the definitions define *[[strict category|strict]] univalent categories*. 

## Examples ##

### In set theory

* Every [[poset]] is a univalent category
* The [[walking parallel pair]] is a univalent category which is not a [[poset]]
* The [[free object|free]] [[category]] on a [[directed acyclic graph]] is a univalent category. 

### In type theory 
Note: All categories given can become univalent via the [[Rezk completion]].

* There is a category $\mathit{Set}$, whose type of objects is $Set$, and with $hom_{\mathit{Set}}(A,B)\equiv (A \to B)$. Under [[univalence]] this becomes a [[category]]. One can also show that any [[category]] of set-level structures such as groups, rings topologicial spaces, etc. is also univalent.

* For any 1-type $X$, there is a univalent category with $X$ as its type of objects and with $hom(x,y)\equiv(x=y)$. If $X$ is a set we call this the **discrete category** on $X$. In general, we call this a **groupoid**.

* For any type $X$, there is a category with $X$ as its type of objects and with $hom(x,y)\equiv \| x= y \|_0$. The composition operation
$$\|y=z\|_0 \to \|x=y\|_0 \to \|y=z\|_0$$
is defined by induction on [[truncation]] from concatenation of the [[identity type]]. We call this the **fundamental groupoid** of $X$.

* There is a category whose type of objects is $\mathcal{U}$ and with $hom(X,Y)\equiv \| X \to Y\|_0$, and composition defined by induction on truncation from ordinary composition of functions. We call this the **homotopy category of types**. 

## Properties ##

### In set theory

Given two categories $A$ and $B$, if $B$ is univalent, then the functor category $B^A$ is univalent. 

\begin{proof}
Let $F:A \to B$ and $G:A \to B$ be functors from $A$ to $B$. We must show that there is at most one natural isomorphism between $F$ and $G$, and if $F \cong G$, then $F = G$. 

Suppose that $\gamma:F \to G$ is a natural isomorphism. Then for any object $a \in A$, there is an isomorphism $\gamma_a: F_{ob}(a) \cong G_{ob}(a)$ in $B$. Since $B$ is univalent, this shows that $F_{ob}(a) = G_{ob}(a)$, and by function extensionality, that $F_{ob} = G_{ob}$. 

Now, for 
\end{proof}

A [[bijective-on-objects functor]] between two categories $A$ and $B$ is a functor $F:A \to B$ where the object function $F_{ob}:Ob(A) \to Ob(B)$ is a [[bijection]]. 

A [[split essentially surjective functor]] between $A$ and $B$ is a functor $F:A \to B$ where for every object $b \in Ob(B)$, there is an object $a \in Ob(A)$ and a n isomorphism $f:F_{ob}(a) \cong b$. 

A [[fully faithful functor]] is a functor where 

These definitions are important for defining the two notions of equality for categories: 

An **[[isomorphism]] of categories** is a fully faithful bijective-on-objects functor. 

An **[[equivalence of categories]]** is a fully faithful split essentially surjective functor. Equivalently, it is a functor $F:A \to B$ which has a left adjoint $G:B \to A$ such that the unit $\eta:1_A \to G F$ and counit $\epsilon:F G \to 1_B$ are isomorphisms. 

\begin{theorem}
For univalent categories, isomorphism of categories and equivalence of categories coincide.
\end{theorem}

...

### In type theory

\begin{lemma}
In a univalent category, the type of objects is a 1-type.
\end{lemma}

\begin{proof}
It suffices to show that for any $a,b:A$, the type $a=b$ is a set. But $a=b$ is equivalent to $a \cong b$ which is a set. 
\end{proof}

There is a canonical way to turn a [[category]] into a univalent category via the [[Rezk completion]].

## Related pages

* [[category]]

* [[type-theoretic definition of category]]

* [[Rezk completion]] (for [[displayed categories]])

* [[homotopy groups of spheres in homotopy type theory]]

* [[cohomology in homotopy type theory]]

* [[Hopf construction in homotopy type theory]]

* [[synthetic (infinity,1)-category theory|synthetic $(\infty,1)$-category theory]]

## References
 {#References}

### General
  {#ReferencesGeneral}



The relation between [[complete Segal space|Segal completeness]] (now often "[[Rezk completion|Rezk completeness]]") for internal categories in HoTT and the [[univalence axiom]] had been pointed out in

* [[Urs Schreiber]], _[Segal completenes and Univalence](https://golem.ph.utexas.edu/category/2012/05/segalcompleteness_and_univalen.html)_ (2012)

A comprehensive discussion for [[1-categories]] then appeared in:

* {#AhrensKapulkinShulman13} [[Benedikt Ahrens]], [[Chris Kapulkin]], [[Michael Shulman]], _Univalent categories and the Rezk completion_, Mathematical Structures in Computer Science **25** 5 (*From type theory and homotopy theory to Univalent Foundations of Mathematics*),  (2015) 1010-1039   $[$[arXiv:1303.0584](https://arxiv.org/abs/1303.0584), [doi:10.1007/978-3-319-21284-5_14](https://doi.org/10.1007/978-3-319-21284-5_14)$]$

Exposition:

* [[Mike Shulman]],  _[Category Theory in Homotopy Type Theory](https://golem.ph.utexas.edu/category/2013/03/category_theory_in_homotopy_ty.html)_, 2013

Implementation in [[Coq]]:

* [[Jason Gross]], [[Adam Chlipala]], [[David Spivak]], *Experience Implementing a Performant Category-Theory Library in Coq*,  In:  *Interactive Theorem Proving. ITP 2014* Lecture Notes in Computer Science, **8558** Springer (2014)  $[$[arXiv:1401.7694](http://arxiv.org/abs/1401.7694), [doi:10.1007/978-3-319-08970-6_18](https://doi.org/10.1007/978-3-319-08970-6_18)$]$

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

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)


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
