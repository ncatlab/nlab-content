Let $V$ be a symmetric [[closed monoidal category]] and $C$, $D$, [[enriched category|enriched categories]] over $V$. Then a __distributor__ or __profunctor__ (also called a _[[bimodule|(bi)module]]_) from $C$ to $D$ is a $V$-functor from $C \otimes D^{op}$ to $V$, we write

$$
  F : C \stackrel{|}{\to} D : C\otimes D^{op} \to V
  \,.
$$

Such distributors are composed by using a [[end|coend]] to "trace out" the middle variable:

for $F : C \stackrel{|}{\to} D$ and $G : D \stackrel{|}{\to} E$ distributors, their composite  $G \circ F: C \stackrel{|}{\to} E$ is defined to be

$$
  G \circ F := \int^{d \in D} F(-,d)\otimes G(d,-)
  \,.
$$

This yields a [[bicategory]] $V\Mod$ with

* objects are $V$-enriched categories;

* morphisms are distributors with the above composition;

* 2-morphisms are natural transformations.

#Examples#

* Recall that a one-object [[Vect]]-[[enriched category]] is just an [[algebra]], while a general [[Vect]]-[[enriched category]] is an [[algebroid]]. The full sub-bicategory of $Vect\Mod$ on one-object $Vect$-enriched categories is the familiar category of [[algebra]]s, [[bimodule]]s and bimodule homomorphisms.

* For $V = (Set, \times)$ we have that the bicategory of $Set$-modules is equivalent to that of sets, [[span]]s of sets and morphisms of spans:
$$
  Set\Mod \simeq Span(Set) 
  \,.
$$

* Accordingly for $S = (Set^{op}, \times)$ we get the bicategory of [[cospan]]s
$$
  Set^{op}\Mod \simeq Span(Set^{op}) = Cospan(Set) 
  \,.
$$


#Remarks#

* Every ordinary $V$-functor $f : C \to D$ yields a distributor $\hat F : C \stackrel{|}{\to} D$ which is 
the [[adjunct]] of the postcomposition 
$$
  C \stackrel{f}{\to} D \stackrel{Y}{\to} [D^{op},V]
$$
with the [[Yoneda embedding]] under the Hom-adjunction. This extends to a bifunctor
$$
  V\Cat \to V\Mod
  \,.
$$

  * For $V = Vect$ this is the generalization of how every morphism $A \to B$ of [[algebra]]s induces the $A$-$B$ bimodule which as a vector space is $B$ with obvious right $B$ action and left $A$-action induced by first mapping $A$ to $B$ via $f$ and then using multiplication in $B$.

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

The common generalization of [[bimodule]]s and [[span]]s in terms of distributors has been discussed on the blog at

* John Baez, _Bimodules versus spans_ ([blog](http://golem.ph.utexas.edu/category/2008/08/bimodules_versus_spans.html))

There is a discussion of distributors in the recently republished:

* J.-M. Cordier and T. Porter, (1989), Shape Theory: Categorical Methods of Approximation, Mathematics and its Applications, Ellis Horwood. Reprinted Dover (2008).

***

#Discussion#

On a previous version of this entry with opposite convention on where to put the ${}^{op}$ [[Todd Trimble|Todd]] has remarked

+--{.query}
_Todd_: There is an inevitable debate here about whether one should use $C^{op} \otimes D \to V$ or $C \otimes D^{op} \to V$. My own convention is to use the latter. For example, every functor $C \to D$ yields a distributor by composition with the Yoneda embedding on $D$. 
=--
