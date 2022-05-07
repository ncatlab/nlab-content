+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### 2-Category theory
+-- {: .hide}
[[!include 2-category theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{: toc}

## Idea

Just as one could define an [[internal logic]], such as [[first order logic]], [[higher order logic]], or [[geometric logic]] in a [[(1,1)-category]] with sufficient structure, in a [[(2,1)-category]], one should be able to define an _internal set theory_. 

Defining a [[set theory]] internal to a (1,1)-category is not possible, unless one is talking about [[material set theories]] such as [[ZFC]], because any groupoid or category internal to an ambient (1,1)-category is necessarily a [[strict category|strict]] groupoid or category, which violates the [[principle of equivalence]] and is thus [[evil]]. Instead, in order to construct an internal set theory, an internal notion of [[weak category]] is needed. 

The basic ideas of the internal set theory induced by a given category C are:

* the objects $A$ of $C$ are regarded as collections of things of a given type $A$

* the morphisms $A\rightarrow B$ of $C$ are regarded as terms of type $B$ containing a free variable of type $A$ (i.e. in a context $x:A$)

* A [[faithful morphism]] $F:A \rightarrow B$ is regarded as a set [[family of sets]] by thinking of it as the discrete collection of all those things of type $B$ for which the type $A$ is inhabited. $B$ is regarded as an [[index set]]. If $B$ is a [[terminal object]] $*$ in $C$, then $A$ and $F$ are equivalent as discrete objects and are regarded as sets. 

  * The [[hom-set]] of morphisms in the weak category of discrete objects of $A$ and faithful morphisms are regarded as the collection of functions between two sets $X:A \rightarrow *$ and $Y:A \rightarrow *$. In particular, functions have set-theoretic equality. 

* Set theoretic operations are implemented by universal constructions on discrete objects.

  * The [[empty set]] is an [[initial object|initial]] discrete object. 

  * The [[singleton]] is a [[terminal object|terminal]] discrete object and a (2,1)-[[generator]]. 

  * The [[Cartesian product]] is a [[2-limit|(2,1)-product]] of discrete objects

  * The [[solution set]] of a set-theoretic [[equation]] is a [[2-pullback|(2,1)-pullback]] of discrete objects

  * The [[disjoint union]] is a [[disjoint coproduct|disjoint]] and [[pullback stability|(2,1)-pullback stable]] [[2-colimit|(2,1)-coproduct]] of discrete objects.

and so on.

* A dependent type over an object $A$ of $C$ may be interpreted as a morphism $B \rightarrow A$ whose “fibres” represent the types $B(x)$ for $x:A$. This morphism might be restricted to be a [[display map]] or a [[fibration]].

## See also

* [[internal logic]]

* [[syntactic category]]

* [[category of sets]]