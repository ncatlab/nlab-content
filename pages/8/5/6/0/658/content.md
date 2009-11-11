Let $V$ be a symmetric [[closed monoidal category]] and $C$, $D$, [[enriched category|enriched categories]] over $V$. Then a **distributor** or **profunctor** or **[[bimodule|(bi)module]]** from $C$ to $D$ is a $V$-functor from $C \otimes D^{op}$ to $V$, we write

$$
  F : C &#8696; D : C\otimes D^{op} \to V
  \,.
$$

Such distributors are composed by using a [[end|coend]] to "trace out" the middle variable:

for $F : C &#8696; D$ and $G : D &#8696; E$ distributors, their composite  $G \circ F: C &#8696; E$ is defined to be

$$
  G \circ F := \int^{d \in D} F(-,d)\otimes G(d,-)
  \,.
$$

This yields a [[bicategory]] $V\Mod$ with

* objects are $V$-enriched categories;

* morphisms are distributors with the above composition;

* 2-morphisms are natural transformations.

At least for $V = Set$ a morphism in $Set Mod$ is often called a **profunctor** and the bicategory $Set Mod$ is then often denoted $Prof$.

#Alternative definitions#


## In terms of colimit-preserving functors on presheaf categories ##

A basic fact (e.g. Kashiwara, Schapira, [[Categories and Sheaves]], corollary 2.7.4, page 63) is that for $A$ a [[cocomplete category]], [[cocontinuous functor|colimit-preserving functors]] from [[presheaf|presheaves]] on some category $C$ to $A$ are canonically equivalent to functors from $C$ to $A$: we have an equivalence of [[functor category|functor categories]]

$$
 Cocont(PSh(C),A)
 \simeq
  Func(C,A)
  \,.
$$

This may be thought of as a consequence of the [[co-Yoneda lemma]] (and hence, of course, of the [[Yoneda lemma]]) which says that every presheaf is colimit over [[representable functor|representables]], i.e. over objects in the image of the [[Yoneda embedding]] $Y : C \to PSh(C)$. This immediate implies that a colimit-preserving functor on $PSh(C)$ is already determined by its restriction along $Y$ to $C$.

Now, distributors $C \otimes D^{op} \to V$ are [[adjunct]] to functors $C \to [D^{op}, V] \simeq PSh(D)$. Hence by the above, distributors are equivalent to colimit-preserving functors

$$
  PSh(C) \to PSh(D)
  \,.
$$

Indeed, there is an equivalence of bicategories
$V Mod$ and that of categories and colimit-preserving functors and natural transformation between their presheaf categories.

An explicit statement of this can be found for instance as prop. 4.2.4

* Gian Luca Cattani, PhD thesis from BRICS, University of Aarhus ([pdf](http://www.daimi.au.dk/~luca/thesis.html))

This formulation plays a big role also in the context of [[(∞,1)-categories]]. A [[presentable (∞,1)-category]] is one equivalent to a [[localization]] of some [[(∞,1)-category of (∞,1)-presheaves]] (i.e. some [[reflective (∞,1)-subcategory]] of the latter). The collection of all [[presentable (∞,1)-categories]] and colimit-preserving [[(∞,1)-functors]] betweem them forms the [[symmetric monoidal (∞,1)-category of presentable (∞,1)-categories]], whose [[tensor product]] is the "bilinear" tensor product coming from interpreting colimit-preserving functors as "linear" (reading: colimit $\sim$ sum).

This $(\infty,1)$-category $Pr^L$ therefore is an $(\infty,1)$-analog of $Set\text{-}Mod$. In [[geometric ∞-function theory]] one finds (see section 4 there) that morphisms in $Pr^L$ encode the "correspondence operations" such as Fourier-Mukai and its generalizations. See in that context also the examples below.


#Examples#

* Recall that a one-object [[Vect]]-[[enriched category]] is just an [[algebra]], while a general [[Vect]]-[[enriched category]] is an [[algebroid]]. The full sub-bicategory of $Vect\Mod$ on one-object $Vect$-enriched categories is the familiar category of [[algebras]], [[bimodules]] and bimodule homomorphisms.

* For $V = (Set, \times)$, $SetMod$ is the bicategory of [[locally small category|locally small categories]], [[profunctors]] and transformations. 

  The full sub-bicategory on [[discrete category|discrete categories]] is that of sets, [[spans]] of sets and morphisms of spans:
  $$
    Set\Mod_{disc} \simeq Span(Set) 
    \,.
  $$

* Accordingly for $S = (Set^{op}, \times)$ we get the bicategory of [[cospans]]
$$
  Set^{op}\Mod_{disc} \simeq Span(Set^{op}) = Cospan(Set) 
  \,.
$$


#Remarks#

* Every ordinary $V$-functor $f : C \to D$ yields a distributor $\hat F : C &#8696; D$ which is 
the [[adjunct]] of the postcomposition 
$$
  C \stackrel{f}{\to} D \stackrel{Y}{\to} [D^{op},V]
$$
with the [[Yoneda embedding]] under the Hom-adjunction. This extends to a bifunctor
$$
  V\Cat \to V\Mod
  \,.
$$

  * For $V = Vect$ this is the generalization of how every morphism $A \to B$ of [[algebras]] induces the $A$-$B$ bimodule which as a vector space is $B$ with obvious right $B$ action and left $A$-action induced by first mapping $A$ to $B$ via $f$ and then using multiplication in $B$.

  * For $V = Set$ this is the fact that every map $f : C \to D$ of sets induces the span 
$$
  \array{
    && C
    \\
    & {}^{Id}\swarrow && \searrow^{f}
    \\
    C &&&& D
  }
$$

* The bifunctor $V\Cat \to V\Mod$ exhibits $V\Mod$ as a [[framed bicategory]].


#Related entries#

* [[module]]

* [[2-vector space]]

#References#

_(what is a good  comprehensive reference?)_

Some exposition at

* John Baez, _Re: Klein 2-Geometry VII_ ([blog](http://golem.ph.utexas.edu/category/2006/11/klein_2geometry_vii.html#c005985))

The common generalization of [[bimodules]] and [[spans]] in terms of distributors has been discussed on the blog at

* John Baez, _Bimodules versus spans_ ([blog](http://golem.ph.utexas.edu/category/2008/08/bimodules_versus_spans.html))

There is a discussion of distributors in the recently republished:

* J.-M. Cordier and T. Porter, (1989), Shape Theory: Categorical Methods of Approximation, Mathematics and its Applications, Ellis Horwood. Reprinted Dover (2008).

Excellent  notes from a course on _distributors_ given by 
Jean B&#233;nabou in June 2000 at TU Darmstadt, and prepared by Thomas Streicher, are available from his website  &lt;http://www.mathematik.tu-darmstadt.de/~streicher>.


***

#Discussion#

On a previous version of this entry with opposite convention on where to put the ${}^{op}$ [[Todd Trimble|Todd]] has remarked

+--{.query}
_Todd_: There is an inevitable debate here about whether one should use $C^{op} \otimes D \to V$ or $C \otimes D^{op} \to V$. My own convention is to use the latter. For example, every functor $C \to D$ yields a distributor by composition with the Yoneda embedding on $D$. 

[[Mike Shulman|Mike]]: My convention is $D^{op}\otimes C$.  I agree with your reasoning for why $D$ should be contravariant; I like to put it first because in the hom-functor $C(-,-)$ the contravariant variable appears first.
=--

[[!redirects profunctor]]
[[!redirects profunctors]]
[[!redirects distributors]]
