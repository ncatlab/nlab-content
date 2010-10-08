
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

## Idea

Informally, a **free functor** is a [[left adjoint]] to a [[forgetful functor]]. (This is informal because the concept of forgetful functor is informal; *any* functor might be viewed as forgetful, so *any* left adjoint might be viewed as free, while in practice only some are.)


## Examples

* the [[free monoid]] functor $Set \to Mon$

* the [[free module]] functor $Set \to K Mod$ for a [[rig]] $K$

* the [[free group]] functor $Set \to Grp$

* the [[free abelian group]] functor $Set \to Ab$

* the [[free category]] functor $Quiv \to Cat$

One formal sort of free functor is the left adjoint $C\to C^T$, where $T$ is a [[monad]] on the category $C$ and $C^T$ is its [[Eilenberg-Moore category]] (the category of $T$-algebras).  This includes all of thee examples above and many others.


## Free objects

In general, if $U: C \to D$ is thought of as a forgetful functor and $F: D \to C$ is its left adjoint, then $F(x)$ is the __free $C$-object__ on an object $x$ of $D$.

More generally, even if the entire left adjoint $F$ doesn't exist, a [[free object]] on $x$ can be defined using a universal property, as "what the value of $F(x)$ would be if $F$ existed."  Conversely, if a free object on $x$ exists for *all* $x\in D$, then the left adjoint $F$ can be assembled from them.


## Cofree functors

Dually, a __cofree functor__ is a [[right adjoint]] to a forgetful functor; for the classical functors which forget algebraic structure, cofree functors are less common than free functors.  As a political joke (which works best for someone who associates political freedom with the left wing), cofree functors have sometimes been called __fascist functors__. Some discussion of this joke may be found at the [nForum](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=1768). 

### Examples

* The cofree coalgebra on a vector space. More generally, if $M$ is an [[operad]] in a symmetric monoidal category $V$, $Prop(M)$ its associated [[PROP]], and if $C$ is a monoidal $V$-category, then an $M$-coalgebra in $C$ may be identified with a monoidal $V$-functor $Prop(M)^{op} \to C$. Under suitable completeness assumptions on $C$, the forgetful functor $M$-$Coalg_C \to C$ has a right adjoint, and this forgetful functor is [[comonadic functor|comonadic]]. 

* If $M$ is a monoid, the forgetful functor $Set^M \to Set$ on (left) $M$-sets has a right adjoint $X \mapsto \hom(M, X)$, where $M$ acts on functions $f: M \to X$ according to the rule $(m f)(m') = f(m' m)$. This forgetful functor is comonadic. Much more generally, the right adjoint to the underlying functor $Set^C \to Set/C_0$ ($C_0$ the set of objects of a category $C$) is comonadic. More generally still, if $V$ is complete and $f: C \to D$ is a functor between small categories, the functor $V^f: V^D \to V^C$ has a right adjoint (although $V^f$ will not normally be comonadic in this generality). 

* The forgetful functor $Cat \to Set$, taking a small category to its set of objects, has a right adjoint $K$ for which $K X$ is a category whose objects are elements of $X$ and where there is exactly one morphism $x \to y$ for any $x, y \in X$. The category $K X$, which is a groupoid, is known as the chaotic category on $X$, or the indiscrete category on $X$. 

* When $U: C \to Set$ is [[topological concrete category]] over $Set$, as for example the forgetful functor $U: Top \to Set$, it frequently happens that $U$ possesses a right adjoint, assigning to a set an "indiscrete topology". 

* A rich source of examples is [[coreflective subcategories]], which are comonadic over the ambient category. For example, the category of compactly generated spaces is coreflective in the category of all spaces, $Top$.  

[[!redirects free functor]]
[[!redirects free functors]]
[[!redirects free construction]]
[[!redirects free constructions]]

[[!redirects cofree functor]]
[[!redirects cofree functors]]
[[!redirects co-free functor]]
[[!redirects co-free functors]]
[[!redirects fascist functor]]
[[!redirects fascist functors]]
