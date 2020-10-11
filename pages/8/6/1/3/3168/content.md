
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents 
{:toc}


## Idea

In [[category theory]] and specifically in [[topos theory]], the notion of _inhabited object_ in a general [[topos]] is a generalization of the notion of [[inhabited set]] from the archetypal topos [[Set]]. It is the [[semantics]] of an [[inhabited type]] in [[type theory]].


## Definition

An object $X$ in a [[topos]] $\mathcal{T}$ is said to be **internally inhabited** if in the [[internal logic]] of the topos it is true that

$$
  \exists x \in X.
$$

This is equivalent to saying that the unique map $X \to 1$ is an [[epimorphism]].  More generally, we can make the same definition in any [[regular category]], in which case it is equivalent to $X\to 1$ being a [[regular epimorphism]].

The term **well-supported** is also used for this notion (in general, the [[support]] of $X$ is the [[image]] of $X\to 1$).

In terms of [[(∞,1)-category theory]], internally inhabited means _[[(-1)-connected]]_.

On the other hand, $X$ is said to be **externally** or **globally inhabited** if there exists a morphism $1\to X$, i.e. a [[global element]].  The adjective "externally" is perhaps misleading, since this notion can also be expressed in the internal [[type theory]] of the topos (as having an [[element]]/[[term]] $x:X$), though not in its more usual internal [[higher-order logic]].  The internal assertion "every internally inhabited object is globally inhabited" is a version of the [[propositional axiom of choice]] (PAC).

Every globally inhabited object is internally inhabited, since every [[split epimorphism]] is a regular epimorphism.  The converse is true if $1$ is [[projective object|projective]], as is the case in a [[well-pointed topos]] (such as [[Set]]).  (This may seem to contradict the above, since PAC can fail even in (constructively) well-pointed toposes, but the point is that PAC also says something about *families* of inhabited objects rather than single "globally defined" objects.)

Some sources use "$X$ is inhabited" in the global sense, while others use the term "inhabited" only internally.  Regardless, a [[pointed object]] always means one _equipped with_ a global element $1\to X$ (which is the same whether interpreted internally or externally), and the terms "global element" and "well-supported" are always unambiguous.


## Examples

For [[Grothendieck topos|sheaf toposes]] with [[point of a topos|enough points]], in which epimorphisms are [[stalk]]wise epimorphisms, an object is (internally) inhabited if the [[germ]] of $X$ over every [[stalk]] is an [[inhabited set]].

One situation where this plays a role is in the study of certain [[smooth topos]]es with objects $\mathbb{I}$ of _invertible infinitesimals_ . There is an immediate definition of such a topos, the topos called $\mathcal{Z}$ at [[Models for Smooth Infinitesimal Analysis]], for which this object exists, but is not inhabited. Only the weaker internal statement $\not \not \exists x \in \mathbb{I}$ is true.

But for some useful constructions in these toposes, such as for giving an internal definition of [[distribution]]s as genuine functions (internally), it is desirable to have $\mathbb{I}$ be inhabited. In the above situation this is achieved by [[forcing]] the existence of invertible infinitesimal elements. The result is the refined topos denoted $\mathcal{B}$ at [[Models for Smooth Infinitesimal Analysis]].


## In a well-pointed topos

The category [[Set]] is a very special sort of topos.  A generally useful principle in formulating categorical properties of [[Set]] is that "external" and "internal" notions should coincide.  A general default understanding across the nLab is that $Set$ is a [[well-pointed topos]] whose terminal object $1$ is projective and [[indecomposable object|indecomposable]].  These latter properties of the terminal object hold for any well-pointed topos if the metalogic is [[classical logic|classical]]; for purposes of [[constructive mathematics]], we usually agree to add them in.

As remarked above, projectivity of $1$ easily makes internal and external inhabitedness agree.  We also present a constructive/intuitionistic proof of the following result about *emptiness*.

+-- {: .num_prop} 
###### Proposition 
In a well-pointed topos, an object $X$ which is _not_ internally inhabited is empty (is an initial object). 
=-- 

Note that the negation "not" in this statement is an *external* one, which is what makes it nontrivial.  If an object is *internally* "not inhabited", then it is empty essentially by definition.

+-- {: .proof} 
###### Proof 
Let $X \to U \hookrightarrow 1$ be the epi-mono factorization of the unique map $X \to 1$. Here $m: U \hookrightarrow 1$ is monic but not epic if $X \to 1$ is not epic, and we use this to prove $U \cong 0$. In that case, we have a map $X \to 0$, whence $X \cong 0$ since in a topos initial objects are strict. (For given $X \to 0$, the projection $\pi_1: X \times 0 \to X$ has a section, and it follows that $X \cong 0$ since $X \times 0 \cong 0$ and retracts of initial objects are initial. This also implies that for any $V$ the map $i: 0 \to V$ is monic: for it is obviously true that for any pair of maps $h, k: A \to 0$ we have that $i h = i k$ implies $h = k$, as $A$ is initial by strictness and this makes $h = k$ automatic.) 

Let $f: U \to \Omega$ be the classifying map of the mono $1_U: U \to U$, and let $g: U \to \Omega$ be the classifying map of the mono $0 \to U$. There is no map $1 \to U$, else $m: U \to 1$ would retract it and hence be epic. Hence it is vacuously true that $f x = g x$ for all $x: 1 \to U$, and so $f = g$ by well-pointedness. Hence the subobjects $1_U$ and $0$ coincide, forcing $U \cong 0$.   (In other words, the presence of a [[subobject classifier]] causes any [[generator]] to be a [[strong generator]].)
=-- 


## Related concepts

* [[inhabited set]]


[[!redirects well-supported object]]
[[!redirects well-supported objects]]

[[!redirects inhabited]]