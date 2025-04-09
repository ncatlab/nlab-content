
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

In [[set-level foundations]], there are two ways to compare two [[objects]] of a [[category]] for sameness: by [[equality]] or by [[isomorphism]].  The [[principle of equivalence]] argues that isomorphism is the "correct" notion of "sameness" for objects of a category, but the notion of equality is still present to be ignored.

Note that even in a [[skeletal category]], where the mere *property* of "being isomorphic" coincides with the property of "being equal", one cannot collapse the notions of isomorphism and equality because an object can still be isomorphic to itself in more than one way.  This distinction only disappears in a [[gaunt category]], but not every category is equivalent to a gaunt one.

By contrast, in [[higher foundations]], it is possible to expand the notion of "equality" so that it coincides with isomorphism: just as two objects can be isomorphic in more than one way, they can also be equal in more than one way.  The notion of "category" in which equality and isomorphism coincide in this way is called *univalent* or *saturated*.  This is an analogue for 1-categories of imposing antisymmetry on a [[preordered set]] (a.k.a. a [[(0,1)-category]]) to obtain a [[partially ordered set]] (a.k.a. a skeletal or gaunt (0,1)-category).

Since we are talking about [[1-categories]] whose hom-types are [[h-sets]], in a univalent category the type of objects is a [[1-type]].  By contrast, a "[[precategory]]" in higher foundations maintains equality of objects (which can have arbitrary [[h-level]]) as separate from isomorphism, while a "[[strict category]]" requires that the type of objects form a set.

## Definition ##

We work in a [[dependent type theory]] with some notion of [[identity type]] or [[path type]], denoted $a=b$.  If $A$ is a [[precategory]] and $a,b:ob(A)$, we write $a\cong b$ for the type of isomorphisms from $a$ to $b$.

\begin{lemma}
There is a map
$$idtoiso : (a=b) \to (a \cong b)$$
\end{lemma}
\begin{proof}
By induction on identity, we may assume $a$ and $b$ are the same. But then we have $1_a:hom_A(a,a)$, which is clearly an isomorphism.
\end{proof}

\begin{definition}
A **univalent category** or **saturated category** is a precategory which is *Rezk complete*, meaning that the above canonical function 
$$idtoiso : (a=b) \to (a \cong b)$$
an equivalence of types. 
\end{definition}

### In simplicial type theory

In [[simplicial type theory]], a **univalent category** or **saturated category** is a [[complete Segal type]] in which all [[hom-types]] are [[sets]].

$$\mathrm{isUniCat}(A) \coloneqq \mathrm{isCompleteSegal}(A) \times \prod_{x:A} \prod_{y:A} \mathrm{isSet}(\mathrm{hom}_A(x, y))$$

## Comparing notions of category

In [[homotopy type theory]], univalent categories are arguably the best notion of "category".  Specifically, in HoTT/UF:

1. Most naturally occurring precategories are in fact univalent categories, such as the category [[Set]] and most categories of structured objects built from it such as [[Grp]], [[Ring]], [[Vect]], [[Mod]], [[Top]], [[Met]], [[StrCat]], etc.
2. Furthermore, *every* precategory is [[equivalence of categories|weakly equivalent]] to a univalent category (its [[Rezk completion]]).
3. The theory of univalent categories is abstractly nicer than that of either precategories or strict categories.  For instance, the statement "a fully faithful and essentially surjective functor is an equivalence" for strict categories is equivalent to the [[axiom of choice]], for precategories it is just false, and for univalent categories it is just true. (On the other hand it can be argued that one should be using [[split essentially surjective functors]] instead of [[essentially surjective functors]], since every equivalence of precategories is fully faithful and split essentially surjective.)
4. Under the semantics of HoTT/UF in [[(infinity,1)-toposes]], univalent categories are interpreted by the correct notion of [[stacks]] of 1-categories.  (See [[relation between type theory and category theory]] and [[category object in an (infinity,1)-category]].)  This is not true for either precategories or strict categories.  (Although in the "classical" model in [[∞Gpd]], univalent categories are interpreted by 1-truncated [[complete Segal spaces]], while strict categories are interpreted by 1-truncated [[Segal categories]] and precategories are interpreted by 1-truncated [[Segal spaces]].  Thus, in this model only, strict categories also give a correct notion of "category", although precategories still do not.)

For these reasons, some of the HoTT/UF literature (including the [[HoTT Book]]) refers to univalent categories as simply "categories".

The situation in plain [[intensional type theory]] is less clear, since without the [[univalence axiom]], naturally-occurring precategories cannot be shown to be univalent (or strict) and the Rezk completion need not exist.  Thus, in this case precategories seem unavoidable.  Fortunately, a surprising amount of category theory can be developed with precategories.

(To be completely precise, the notion of "univalent category" can also be defined in [[set-level foundations]].  In that case it turns out to be equivalent to the notion of [[gaunt category]], which again is not satisfactory as a general notion of "category".  More generally, a [[strict category]] is univalent if and only if it is gaunt.)

On this page we will not use the plain term "category" at all, but speak only of "precategories", "univalent categories", and "strict categories".

\begin{remark}
Most nLab pages about category theory are, and should remain, written in a fairly foundation-agnostic way.  If the reader is interpreting them in HoTT/UF, it is usually best to read "category" as meaning "univalent category" for the reasons above.  However, in many cases it is also possible to read it as meaning "precategory" or "strict category", as would be necessary if interpreting them in plain intensional type theory.

It is not usually necessary for pages about ordinary category theory to remark on this issue at all.  However, if there are subtleties regarding the choice of interpretation (e.g. if some construction, such as a [[Kleisli category]], may lead out of the world of univalent categories; or if some structure, such as a [[dagger category]], requires changing the notion of "univalence"), it is appropriate to include a remark.  Such a remark should generally be lower down on the page, not at the top, so that it doesn't confuse first-time readers.
\end{remark}



## Examples 

Note: All categories given can become univalent via the [[Rezk completion]].

* As noted above, every [[gaunt category]] is a [[strict category|strict]] univalent category, or equivalently a [[skeletal category|skeletal]] univalent category.

* There is a precategory [[Set]], whose type of objects is $Set$, and with $hom_{Set}(A,B)\equiv (A \to B)$.  The [[univalence axiom]] implies that this is a univalent category.  One can also show from this that any precategory of set-level structures such as groups, rings topological spaces, etc. is also univalent.

* For any [[1-type]] $X$, there is a univalent category with $X$ as its type of objects and with $hom(x,y)\equiv(x=y)$. If $X$ is a set we call this the **discrete category** on $X$. In general, we call it a **(univalent) groupoid**.

* More generally, or any type $X$, there is a precategory with $X$ as its type of objects and with $hom(x,y)\equiv \| x= y \|_0$. The composition operation
$$\|y=z\|_0 \to \|x=y\|_0 \to \|y=z\|_0$$
is defined by induction on [[truncation]] from concatenation of the [[identity type]]. We call this the **fundamental pregroupoid** of $X$.  It is univalent if and only if $X$ is a 1-type; its Rezk completion is the **fundamental (univalent) groupoid** of $X$.

* There is a precategory whose type of objects is the [[type universe]] $\mathcal{U}$ and with $hom(X,Y)\equiv \| X \to Y\|_0$, and composition defined by induction on truncation from ordinary composition of functions.  We call this the **homotopy precategory of types**; it is not univalent (although it contains the univalent category [[Set]] as a sub-precategory).

## Properties ##

\begin{theorem}
Given two categories $A$ and $B$, if $B$ is univalent, then the functor category $B^A$ is univalent. 
\end{theorem}

\begin{proof}
Let $F:A \to B$ and $G:A \to B$ be functors from $A$ to $B$. 

Suppose that $\gamma:F \to G$ is a natural isomorphism. Then for any object $a : Ob(A)$, there is an isomorphism $\gamma_a: F_{ob}(a) \cong G_{ob}(a)$ in $B$. Since $B$ is univalent, this shows that $F_{ob}(a) = G_{ob}(a)$ for all objects $a$, and by function extensionality, that $F_{ob} = G_{ob}$. 

Now, for any $a : Ob(A)$ and $b : Ob(B)$, the functions $F_{mor}(a,b):Mor_A(a,b) \to Mor_B(F_{ob}(a),F_{ob}(b))$ and $G_{mor}(a,b):Mor_A(a,b) \to Mor_B(G_{ob}(a),G_{ob}(b))$ are equal, because we established above that $F(a) = G(a)$ for all $a : Ob(a)$. Because the object functions and morphism functions of $F$ and $G$ are equal to each other, $F = G$. 

Thus, if there is an isomorphism $\gamma:F \cong G$, then $F = G$. 

this proof needs to be revised since it is missing the explicit identifications
\end{proof}

An [[equivalent-on-objects functor]] between two precategories $A$ and $B$ is a functor $F:A \to B$ where the object function $F_{ob}:Ob(A) \to Ob(B)$ is a equivalence of types.

A [[split essentially surjective functor]] between $A$ and $B$ is a functor $F:A \to B$ where for every object $b : Ob(B)$, there is a specified object $a : Ob(A)$ and an isomorphism $f:F_{ob}(a) \cong b$. 

A [[fully faithful functor]] is a functor $F:A\to B$ such that each map on [[hom-sets]] $F_{a,b} : A(a_0,a_1) \to B(F(a_0),F(a_1))$ is an [[equivalence of types]].

These definitions are important for defining the two notions of equality for categories: 

An **[[isomorphism]] of categories** is a fully faithful equivalent-on-objects functor. 

An **[[equivalence of categories]]** is a fully faithful split essentially surjective functor. Equivalently, it is a functor $F:A \to B$ which has a left adjoint $G:B \to A$ such that the unit $\eta:1_A \to G F$ and counit $\epsilon:F G \to 1_B$ are isomorphisms. 

\begin{theorem}
For univalent categories, isomorphism of categories and equivalence of categories coincide.
\end{theorem}

...

\begin{lemma}
In a univalent category, the type of objects is a 1-type.
\end{lemma}

\begin{proof}
It suffices to show that for any $a,b:A$, the type $a=b$ is a set. But $a=b$ is equivalent to $a \cong b$ which is a set. 
\end{proof}

There is a canonical way to turn a [[category]] into a univalent category via the [[Rezk completion]].

## Related pages

* [[category]]

* [[gaunt category]]

* [[locally univalent bicategory]]

* [[type-theoretic definition of category]]

* [[Rezk completion]] (for [[displayed categories]])

* [[homotopy groups of spheres in homotopy type theory]]

* [[cohomology in homotopy type theory]]

* [[Hopf construction in homotopy type theory]]

* [[synthetic (infinity,1)-category theory|synthetic $(\infty,1)$-category theory]]

* [[complete Segal type]]

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

* {#Ahrens13} [[Benedikt Ahrens]], *Univalent categories and Rezk completion*, talk at IRIT (2013) &lbrack;[[Ahrend-UnivalentCategories.pdf:file]]&rbrack;

* [[Amélia Liao]], *Univalent Category Theory*, [[Homotopy Type Theory Electronic Seminar Talks]], (October 2022) &lbrack;[video](https://www.youtube.com/watch?v=asY6dXkR2yg)&rbrack;




Implementation in [[Coq]]:

* [[Jason Gross]], [[Adam Chlipala]], [[David Spivak]], *Experience Implementing a Performant Category-Theory Library in Coq*,  In:  *Interactive Theorem Proving. ITP 2014* Lecture Notes in Computer Science, **8558** Springer (2014)  $[$[arXiv:1401.7694](http://arxiv.org/abs/1401.7694), [doi:10.1007/978-3-319-08970-6_18](https://doi.org/10.1007/978-3-319-08970-6_18)$]$

[[Coq]] code formalizing this includes the following:

* _[github.com/benediktahrens/rezk_completion](https://github.com/benediktahrens/rezk_completion)_

and in [[cubical Agda]]:

* [[1lab]]: *[Cat.Base](https://1lab.dev/Cat.Base.html)*


Generalization to [[(n,1)-categories]] is discussed in

* {#CapriottiKraus17} [[Paolo Capriotti]], [[Nicolai Kraus]], _Univalent Higher Categories via Complete Semi-Segal Types_ ([arXiv:1707.03693](https://arxiv.org/abs/1707.03693))

and, by different means, in

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* ([arXiv:1705.07442](https://arxiv.org/abs/1705.07442))

* {#Riehl18} [[Emily Riehl]], _The synthetic theory of ∞-categories vs the synthetic theory of ∞-categories_, talk at [Vladimir Voevodsky Memorial Conference 2018](http://www.math.ias.edu/vvmc2018) ([pdf](http://www.math.jhu.edu/~eriehl/Voevodsky.pdf))

Formalization of [[bicategories]]:

* [[Benedikt Ahrens]], Dan Frumin, Marco Maggesi, Niels van der Weide, _Bicategories in Univalent Foundations_ ([arXiv:1903.01152](https://arxiv.org/abs/1903.01152))

Lemmas and proofs above are taken from:

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

On [[monoidal category|monoidal]] [[univalent categories]]:

* [[Kobe Wullaert]], [[Ralph Matthes]], [[Benedikt Ahrens]], *Univalent Monoidal Categories* &lbrack;[arXiv:2212.03146](https://arxiv.org/abs/2212.03146)&rbrack;


### By coinduction
  {#ReferencesCoinduction}

A formalization in [[HoTT]]-[[Agda]] of general [[(n,r)-categories]] for $n,r \in \mathbb{N} \sqcup \{\infty\}$, defined as [[coinductive types]] of infinity-graphs, with operations defined by induction-coinduction, is implemented in

* {#Morrison19} Darin Morrison, _[agda-nr-cats](https://github.com/5HT/agda-nr-cats)_, 
_[agda-infinity-categories](https://github.com/freebroccolo/agda-infinity-categories/)

\linebreak




[[!redirects internal category in homotopy type theory]]
[[!redirects internal categories in homotopy type theory]]

[[!redirects internal category in HoTT]]
[[!redirects internal categories in HoTT]]

[[!redirects internal category theory in homotopy type theory]]
[[!redirects internal category theory in HoTT]]

[[!redirects saturated category]]
[[!redirects univalent category]]
[[!redirects saturated categories]]
[[!redirects univalent categories]]

[[!redirects weak saturated category]]
[[!redirects weak univalent category]]
[[!redirects weak saturated categories]]
[[!redirects weak univalent categories]]
