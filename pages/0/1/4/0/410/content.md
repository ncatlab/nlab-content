
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Informally, a **free functor** is a [[left adjoint]] to a [[forgetful functor]] -- part of a [[free-forgetful adjunction]]. (This is informal because the concept of [[forgetful functor]] is informal; *any* functor might be viewed as forgetful, so *any* left adjoint might be viewed as free, while in practice only some are.)

Formally, with respect to a [[monad]] or [[algebraic theory]] or [[operad]] $T$, and $T Alg(C)$ the corresponding category of [[algebras over a monad]] or [[algebras over an algebraic theory]] or [[algebras over an operad]], respectively, in some category $C$, the **free $T$-algebra functor** is the [[left adjoint]] to the [[forgetful functor]] $T Alg(C) \to C$.

Such a functor may be thought of as sending any [[object]] of $C$ to the $T$-algebra _freely generated_ by it.


### Free objects

In general, if $U: C \to D$ is thought of as a forgetful functor and $F: D \to C$ is its left adjoint, then $F(x)$ is the __[[free object|free C-object]]__ on an object $x$ of $D$.

More generally, even if the entire left adjoint $F$ doesn't exist, a [[free object]] on $x$ can be defined using a universal property, as "what the value of $F(x)$ would be if $F$ existed."  Conversely, if a free object on $x$ exists for *all* $x\in D$, then the left adjoint $F$ can be assembled from them.


### Cofree functors

[[duality|Dually]], a __cofree functor__ is a [[right adjoint]] to a forgetful functor. 

For the classical functors which forget algebraic structure, cofree functors are less common than free functors.


## Examples

Classically, examples of free constructions were characterized by a [[universal property]]. For example, in the case of the free group on a set $X$ the universal property states that any map $X \to G$ as sets uniquely extends to a group homomorphism $F(X) \to G$. When such a free construction can be realized as a left adjoint functor, this universal property is just a transliteration of the fact that the [[unit of an adjunction|unit]] of the [[free-forgetful adjunction]] is an [[initial object]] in the [[comma category]] $(X \downarrow U)$ (where $U$ is the forgetful functor out of the category of algebras, see e.g. the proof of Freyd's general [[adjoint functor theorem]].)

### For free functors

* the [[free monoid]] functor [[Set]] $\to$ [[Mon]];

* the [[free module]] functor [[Set]] $\to$ $K$ [[Mod]] for a [[rig]] $K$;

* the [[free group]] functor [[Set]] $\to$ [[Grp]];

* the [[group completion]] functor [[Mon]] $\to$ [[Grp]]

  in the abelian case in particular:

  the [[Grothendieck group of a commutative monoid|Grothendieck group completion]] functor [[CMon]] $\to$ [[Ab]]

* the [[free abelian group]] functor [[Set]] $\to$ [[Ab]];

* the [[abelianization]] functor [[Grp]] $\to$ [[Ab]];

* the [[free category]] functor $Grph_{d,r} \to$ [[Cat]];

* the [[free operad]] functor;

* the [[unitisation]] functor [[Rng]] $\to$ [[Ring]].

Free constructions *on* [[categories]]:

* [[free cocompletion]], [[free coproduct completion]], [[idempotent completion]], [[Cauchy completion]]

One formal sort of free functor is the [[left adjoint]] $C\to C^T$, where $T$ is a [[monad]] on the [[category]] $C$ and $C^T$ is its [[Eilenberg-Moore category]] (the category of $T$-algebras).  This includes all of the examples above and many others.

A general way to construct free functors is with a [[transfinite construction of free algebras]] (in [[set theory|set-theoretic]] foundations), or with an [[inductive type]] or [[higher inductive type]] (in [[type theory|type-theoretic]] foundations).


### For cofree functors

* The [[cofree coalgebra]] on a vector space. More generally, if $M$ is an [[operad]] in a symmetric monoidal category $V$, $Prop(M)$ its associated [[PROP]], and if $C$ is a monoidal $V$-category, then an $M$-coalgebra in $C$ may be identified with a monoidal $V$-functor $Prop(M)^{op} \to C$. Under suitable completeness assumptions on $C$, the forgetful functor $M$-$Coalg_C \to C$ has a right adjoint, and this forgetful functor is [[comonadic functor|comonadic]]. 

* If $M$ is a monoid, the forgetful functor $Set^M \to Set$ on (left) $M$-sets has a right adjoint $X \mapsto \hom(M, X)$, where $M$ acts on functions $f: M \to X$ according to the rule $(m f)(m') = f(m' m)$. This forgetful functor is comonadic. Much more generally, the right adjoint to the underlying functor $Set^C \to Set/C_0$ ($C_0$ the set of objects of a category $C$) is comonadic. More generally still, if $V$ is complete and $f: C \to D$ is a functor between small categories, the functor $V^f: V^D \to V^C$ has a right adjoint (although $V^f$ will not normally be comonadic in this generality). 

* The forgetful functor $Cat \to Set$, taking a small category to its set of objects, has a right adjoint $K$ for which $K X$ is a category whose objects are elements of $X$ and where there is exactly one morphism $x \to y$ for any $x, y \in X$. The category $K X$, which is a groupoid, is known as the chaotic category on $X$, or the indiscrete category on $X$. 

* When $U: C \to Set$ is [[topological concrete category]] over $Set$, as for example the forgetful functor $U: Top \to Set$, it frequently happens that $U$ possesses a right adjoint, assigning to a set an "indiscrete topology". 

* The ring of [[Witt vectors]] is the co-free [[Lambda-ring]].

* A rich source of examples is [[coreflective subcategories]], which are comonadic over the ambient category. For example, the category of compactly generated spaces is coreflective in the category of all spaces, $Top$.  



## Related concepts

* [[free object]], [[universal property]]


[[!redirects free functor]]
[[!redirects free functors]]
[[!redirects free construction]]
[[!redirects free constructions]]
[[!redirects freely generated]]
[[!redirects free]]

[[!redirects cofree functor]]
[[!redirects cofree functors]]
[[!redirects cofree]]
[[!redirects co-free functor]]
[[!redirects co-free functors]]
[[!redirects co-free]]
[[!redirects fascist functor]]
[[!redirects fascist functors]]
[[!redirects fascist]]

[[!redirects free-forgetful adjunction]]
