
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--

# W-types
* table of contents
{: toc}

## Idea

A *W-type* is a [[set]] or [[type]] which is defined [[induction|inductively]] in a [[well-founded relation|well-founded]] way -- an [[inductive type]].  In most [[set theory|set theories]], W-types can be proven to exist, but in [[predicative mathematics]] or [[type theory]], where this is not the case, they are often assumed explicitly to exist. In particular W-types can be used to provide a [[constructive mathematics|constructive]] counterpart of the [[classical logic|classical]] notion of a [[well-ordering]] and to uniformly define a variety of [[inductive types]]. More complex inductive types, such as strictly positive inductive types, can be reduced to W-types; see [AAG](#AAG). This can even be extended to [[inductive families]].

The [[terms]]/[[elements]] of a W-type can be considered to be "rooted well-founded [[trees]]" with a certain branching type; different W-types are distinguished by their branching signatures.  A branching signature is represented essentially by a [[family of sets]] $\{A_b\}_{b\in B}$ which can be interpreted as requiring that each *node* of the tree is labeled with an element of the set $B$, and that if a node is labeled by $b$ then it has exactly ${|A_b|}$ outgoing edges, each labeled by an element of $A_b$.  From a more computational point of view, the W-type can be viewed as a data type, where $B$ indexes the set of *constructors* and $A_b$ is the *arity* of the constructor $b$.

If the trees are not required to be well-founded, we obtain instead a [[coinduction|coinductively]] defined type, called a "co-W-type" or an [[M-type]].

## Examples

(1) The most basic W-type is the [[natural numbers]].  Here there are two constructors:

* $0$ of arity zero, and
* $S$ of arity one.
Therefore, zero is a natural number, any natural number has a successor, and all natural numbers are generated in this way.

(2) Similarly, if $X$ is any set, then the W-type $L X$ of [[lists]] of elements of $X$ has $|X|+1$ constructors:

* $nil$ of arity zero, and
* $cons(x,-)$ of arity one, for each $x\in X$.
Therefore, $nil$ is a list, $cons(x,\ell)$ is a list for any list $\ell$ and $x\in X$, and all lists are generated in this way.

(3) [[identity type]]s arise as a more general kind of W-type; see [this blog post](http://homotopytypetheory.org/2011/04/18/whats-special-about-identity-types/).


## Definition
 {#Definition}

Actually, there are two slightly different formulations of W-types.

### W-types in categories

#### Plain version

This version of W-types is the most natural for mathematicians used to thinking in terms of [[set theory]] or [[category theory]], the [[categorical semantics]] of W-types, due to ([Moerdijk-Palmgren 00](#MoerdijkPalmgren00)).

Here we describe a W-type as the [[initial algebra|initial]] [[algebra for an endofunctor]].  The family $\{A_b\}_{b\in B}$ can be thought of as a [[morphism]] $f\colon A\to B$ in some [[category]] $\mathcal{C}$ (the [[fiber]] over $b\in B$ being $A_b$), and the [[endofunctor]] in question is the composite

$$ 
  \mathcal{C} \overset{A^*}{\longrightarrow} \mathcal{C}_{/A} \overset{\Pi_f}{\longrightarrow} \mathcal{C}_{/B} \overset{\Sigma_B}{\longrightarrow} \mathcal{C}
  \,,
$$

where $A^*$ is [[context extension]], hence is the [[pullback]] functor (a.k.a. $A\times -$), $\Pi_f$ is a [[dependent product]], and $\Sigma_B$ is a [[dependent sum]] (a.k.a. the [[forgetful functor]] from $\mathcal{C}_{/B}$ to $\mathcal{C}$).  

Such a composite is called a _[[polynomial endofunctor]]_.  

This definition makes sense in any [[locally cartesian closed category]], although the W-type (the initial algebra) may or may not exist in any given such category.  (A non-elementary construction of them is given by the [[transfinite construction of free algebras]].)

This definition is most useful when the category $\mathcal{C}$ is not just 
[[locally cartesian closed category|locally cartesian closed]] but is a [[Π-pretopos]], since often we want to use at least [[coproducts]] in constructing $A$ and $B$.  For example, a [[natural numbers object]] is a W-type specified by one of the coproduct inclusions $1\to 1+1$, and the [[list object]] $L X$ is a W-type specified by $X\to X+1$.  More generally, endofunctors that look like [[polynomial]]s in the traditional sense:
$$ F(Y) = A_n \times Y^{\times n}  + \dots + A_1 \times Y  + A_0 $$
can be constructed as polynomial endofunctors in the above sense in any $\Pi$-pretopos.  A $\Pi$-pretopos in which all W-types exist is called a **[[ΠW-pretopos]]**.

In a [[topos]] with a [[natural numbers object]] (NNO), W-types for any polynomial endofunctor can be constructed as certain sets of well-founded trees; thus every topos with a NNO is a [[ΠW-pretopos]].  This applies in particular in the topos [[Set]] (unless one is a [[predicative mathematics|predicativist]], in which case $Set$ is not a topos and W-types in it must be postulated explicitly).


#### Dependent W-types
 {#DependentWTypesCategoricalSemantics}

The above has a natural generalization to [[dependent type|dependent]] W-types ([Gambino-Hyland 04](#GambinoHyland04)): 

given a [[diagram]] of the form

$$
  \array{
    A &\stackrel{f}{\longrightarrow}& B
    \\
    \downarrow^{\mathrlap{h}} && \downarrow^{\mathrlap{g}}
    \\
    C && C
  }
$$

there is the _[[dependent polynomial functor]]_

$$ 
  \mathcal{C}_{/C} \overset{h^\ast}{\longrightarrow} 
  \mathcal{C}_{/A} 
    \overset{\Pi_f}{\longrightarrow} 
  \mathcal{C}_{/B} 
    \overset{\Sigma_g}{\longrightarrow} 
  \mathcal{C}_{/C}
  \,,
$$

This reduces to the above for $C = \ast$ the [[terminal object]].
Notice that we do not necessarily have $g f \simeq h$, so this is not just simply a polynomial endofunctor of $\mathcal{C}/_{C}$ considered as a lccc in its own right.


### W-types in type theory

In [[type theory]], W-types are introduced by giving explicit constructors and destructors, a.k.a. [[term introduction]] and [[term elimination]] rules.  If the type theory is *[[extensional type theory|extensional]]*, i.e. [[identity type|identities]] have unique proofs and (dependent) [[function types]] are [[function extensionality|extensional]] ($f=g$ if and only if $f(x)=g(x)$ for all $x$), then this is more or less equivalent to the categorical version given above.  The type theories that are the [[internal logic]] of familiar kinds of categories are all extensional in this sense.

The rules for $W$-types in extensional type theory are the following:

(1) $W$-formation rule
$$\frac{A:Type\; x:A\vdash B(x):Type}{(W x:A)B(x):Type}$$

+--{: .query}
[[Andreas Abel]]: A and B are used exactly the other way round in the introductory text to this page.  (Before, A was the arity, now B is the arity.)  Harmonize!?
=--

In the following we will sometimes abbreviate $(W x:A)B(x)$ by $W$.

(2) $W$-introduction rule
$$\frac{a:A\; t:B(a)\to W}{sup(a,t):W}$$

(3) $W$-elimination rule
$$\frac{\array{w:W\vdash C(w):Type\\
x:A, u:B(x)\to W, v:(\Pi y:B(x))C(u(y))\vdash\\
c(x,u,v):C(sup(x,u))}}{w:W\vdash wrec(w,c):C(w)}$$

(4) $W$-computation rule
$$\frac{\array{w:W\vdash C(w):Type\\
x:A, u:B(x)\to W, v:(\Pi y:B(x))C(u(y))\vdash\\
c(x,u,v):C(sup(x,u))}}{\array{
x:A, u:B(x)\to W\vdash wrec(sup(x,u),c)=\\
c(x,u,\lambda y.wrec(u(y),c)):C(sup(x,u))}}$$

([Awodey-Gambino-Sojakova](#AwodeyGambinoSojakova) &#167;2, originally from [Martin-L&#246;f](#Martin-LofITT))

The main distinction from the naive categorical theory above is that the map $f$ (from the lines above the rules) must be assumed to be a [[display map]], i.e. to exhibit $A$ as a [[dependent type]] over $B$, in order that the dependent product $\Pi_f$ be defined.  In the case of dependent polynomial functors, $q$ must also be a display map in order to define $\Sigma_q$.  (Actually, using [[adjunction|adjointness]], one can still define the W-type even if $q$ is not a display map, but its properties are not as good.  This extra generality is important, however.  For example, [[identity type]]s arise as this more general kind of W-type; see [this blog post](http://homotopytypetheory.org/2011/04/18/whats-special-about-identity-types/).)

+--{: .query}
[[Mike Shulman]]: Is the term "W-type" still used in this generality?  Or are they just called "inductive types"?
=--

Note also that in [[intensional type theory]], a W-type is only an initial algebra with respect to propositional equality, not definitional equality.  In particular, the constructors are injective only propositionally, not definitionally.  This applies already for the natural numbers.

## Properties
 {#Properties}

In [[homotopy type theory]], if $A$ as h-level $n\geq -1$, then $W A B$ has h-level $n$ (as it should be for [[(infinity,1)-colimits]]). A formal proof of this is discussed in ([Danielsson](#Danielsson)).

## Related concepts

* [[M-type]]

* [[predicative topos]]

[[!include notions of type]]

## References

The original definition in [[type theory]] is due to

* [[Per Martin-Löf]], _Intuitionistic Type Theory_, Notes by G. Sambin of a series of lectures given in Padua, 1980. Bibliopolis, 1984.
 {#Martin-LofITT}

The [[categorical semantics]] of W-types by initial algebras of polynomial endofunctors is due to

* [[Ieke Moerdijk]], [[Erik Palmgren]], _Wellfounded trees in categories_, Annals of Pure and Applied Logic 104 (2000) 189 &#8211; 218 ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.44.6700))
 {#MoerdijkPalmgren00}

*  [[Benno van den Berg]],  [[Ieke Moerdijk]] (2008-09-25); _$W$-types in sheaves_; [vdBM_Wtypes.ps/pdf](http://www.phil.cmu.edu/projects/ast/Papers/)

Dependent W-type were introduced in 

* [[Nicola Gambino]], [[Martin Hyland]], _Wellfounded trees and dependent polynomial functors_. In Types for proofs and programs, volume 3085 of Lecture Notes in Comput. Sci., pages 210&#8211;225. Springer-Verlag, Berlin, 2004 ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.98.4534))
 {#GambinoHyland04}

Related work is:

* [[Michael Abbott]], [[Thorsten Altenkirch]], and [[Neil Ghani]], _Representing Nested Inductive Types using W-types_ ([pdf](http://www.cs.nott.ac.uk/~psztxa/publ/icalp04.pdf))

Discussion in relation to [[identity types]] and [[homotopy type theory]] is in

* {#AwodeyGambinoSojakova} [[Steve Awodey]], [[Nicola Gambino]], [[Kristina Sojakova]], *Inductive types in homotopy type theory* ([arXiv:1201.3898](http://arxiv.org/abs/1201.3898))
 

* [[Steve Awodey]], [[Nicola Gambino]], [[Kristina Sojakova]], _Homotopy-initial algebras in type theory_ ([arXiv:1504.05531](http://arxiv.org/abs/1504.05531))


Work towards dependent W-types in HoTT is here; see also [[inductive families]].

* Christian Sattler, _On relating indexed W-types with ordinary ones_, 2015 [PDF](http://cs.ioc.ee/types15/abstracts-book/contrib31.pdf)

A formal proof about the [[h-level]] of W-types is discussed in

* Nils Anders Danielsson, _Positive h-levels are closed under W_ ([web](https://homotopytypetheory.org/2012/09/21/positive-h-levels-are-closed-under-w/))
 {#Danielsson}

and also in

* Jasper Hugunin, _IWTypes_, <https://github.com/jashug/IWTypes>

which also computes the [[identity types]] of W-types (and more generally [[indexed W-types]]).

Discussion of W-types in [[homotopy type theory]], or rather in [[model categories]] presenting [[homotopy theories]], is in 

* [[Benno van den Berg]], [[Ieke Moerdijk]], _W-types in Homotopy Type Theory_ ([arXiv:1307.2765](http://arxiv.org/abs/1307.2765))
 {#vdBergMoerdijk13}

W-types in [[Coq]] [wiki](https://coq.inria.fr/cocorico/WTypeInsteadOfInductiveTypes)

[[!redirects W-types]]