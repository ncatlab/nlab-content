
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

A [[category]] is called **gaunt** if all its [[isomorphisms]] are in fact [[identities]]. This is a property of [[strict categories]]; that is, it is not [[principle of invariance|invariant]] under [[equivalence of categories]]. See below for some related concepts that are invariant.

Every gaunt category is [[skeletal category|skeletal]], but not conversely.  Every gaunt category is also [[univalent category|univalent]]; the converse holds in [[set-level foundations]] but not in the [[higher foundations]] where univalent categories are usually considered.  More generally, gaunt categories are precisely the categories that are both [[strict category|strict]] and univalent.

## Definitions

### In set-level foundations

\begin{definition}
A **gaunt category** or **stiff category** is a [[skeletal category]] $C$ whose [[core]] is [[thin category|thin]]. 

\end{definition}

Expanding out, this becomes

\begin{definition}
A **gaunt category** or **stiff category** is a category $C$ such that the set of isomorphisms $A \cong B$ between every two objects $A \in Ob(C)$ and $B \in Ob(C)$ of $C$ is a [[subsingleton]], and there is an isomorphism $f:A \cong B$ if and only if $A = B$. 

\end{definition}

### In type theory

In a [[dependent type theory]] with some notion of [[identity type]] or [[path type]], there is another definition of gaunt category available. 

\begin{definition}
A **gaunt category** or **stiff category** is a strict univalent category. 
\end{definition}

Expanded out, this becomes

\begin{definition}
A **gaunt category** or **stiff category** is a category whose type of objects is 0-truncated and which additionally satisfies a condition called *Rezk completeness*: the canonical function 
$$idtoiso : (a=b) \to (a \cong b)$$
from the identity type between two objects $a$ and $b$ to the type of isomorphisms between $a$ and $b$ is an equivalence of types. 
\end{definition}

In [[set-level type theory]], the type theoretic definition and the set-level definitions are equivalent to each other.  For in this case, every [[identity type]] is a [[proposition]]/[[subsingleton]].  Thus, by the Rezk completeness condition, the set of isomorphisms is a subsingleton, and two objects which are isomorphic to each other are also equal to each other. 


## Examples

* Every [[poset]] is a gaunt category.
* The [[walking parallel pair]] is a gaunt category which is not a [[poset]].
* The [[free category]] on a [[directed graph]] is a gaunt category. 
* The [[category]] of [[Archimedean ordered fields]] and [[monotonic]] [[field homomorphisms]] is a gaunt category. 
* The [[delooping]] of a group is (in set-level foundations) a [[skeletal category]] that is not gaunt (unless the group is [[trivial group|trivial]]).
* The [[walking isomorphism]], as usually defined, is not gaunt.  (In [[homotopy type theory]], one can Rezk-complete the walking isomorphism, obtaining a univalent category that is gaunt and indeed equivalent to the [[terminal category]].)
* The [[simplex category]] and more generally any [[Reedy category]] is gaunt.

## Properties


### Relation to other properties of categories

Gaunt categories are necessarily [[skeletal]]; a skeletal category is gaunt iff every [[automorphism]] is an [[identity morphism]]. Consequently a [[thin]] gaunt category is skeletal, and since a thin skeletal category is a [[poset category]] a thin gaunt category is also a poset category.

Note that a gaunt category need not be thin, since we may have parallel non-isomorphisms which are not equal. Similarly, a thin category need not be gaunt since we may have isomorphisms that aren't the identity.

The [[core]] of a gaunt category is a [[set]]. 


### Relation to complete Segal spaces

The [[nerve]] [[simplicial set]] of a [[category]], regarded as a [[simplicial object]] in [[homotopy types]] under the inclusion $Set \hookrightarrow \infty Grpd$, is a _[[complete Segal space]]_ precisely if the category is gaunt. More discussion of this is at _[Segal space -- Examples -- In Set](Segal%20space#InSetByNervesOfCategories)_.

### In higher foundations

As noted above, in [[higher foundations]] the gaunt categories are precisely the [[strict category|strict]] and [[univalent categories]]. Thus, every property which is satisfied of strict categories and univalent categories apply to gaunt categories. 

In addition, we have

\begin{theorem}
The [[Rezk completion]] of a core-thin category is a gaunt category. 
\end{theorem}


## Related invariant concepts

To make sense of the definition of a gaunt category, we need to use equality of objects: For every isomorphism $f : a \simeq b$, there is an equality $p : a = b$, relative to which $f$ equals the identity at $a$. Replacing the equality $p$ by an isomorphism $g : a \simeq b$, the resulting condition holds for all categories.
This echoes how one might understand the definition in [[univalent foundations]]: the univalence condition for a [[univalent category]] is another way of saying that every isomorphism is an identity (and uniquely so).

Alternatively, we could avoid the equality on objects by requiring only that every [[automorphism]] $f : a \cong a$ be equal to the identity at $a$. This amounts to requiring that the [[core]] be a [[thin category]], i.e., that parallel isomorphisms are equal.  A category has this property if and only if it is *equivalent* to a gaunt one.

{#Incidentally} Incidentally, we may view both [[strict categories]] and categories up to [[equivalence of categories|equivalence]] as embedded in the type of [[flagged categories]]. Recall that a [[flagged category]] consists of a category $C$, a [[groupoid]] $X$, and an [[essentially surjective functor]] $p \colon X \to C$. In this way, we can view categories as those [[flagged categories]] where $p$ is an [[equivalence of groupoids|equivalence]] onto the [[core]] of $C$, and [[strict categories]] as those flagged categories where $X$ is a [[set]] (up to homotopy: an "[[h-set]]"): see at *[[category with an atlas]]*. The [[intersection]] of categories-up-to-equivalence and [[strict categories]] within the type of flagged categories is then exactly this type of core-thin categories.  (This is the semantics in [[Gpd]] of the fact that in [[homotopy type theory]], the gaunt categories are precisely the [[strict category|strict]] and [[univalent categories]].)

## See also

* [[strict category]]

* [[univalent category]]

* [[skeletal category]]

* [[thin category]]

* [[symmetric proset]]

* [[core]]

* [[gaunt Segal type]]

## References

The term "gaunt category" was apparently introduced in 

* {#BarwickSchommerPries} [[Clark Barwick]], [[Chris Schommer-Pries]], _On the Unicity of the Homotopy Theory of Higher Categories_ ([arXiv:1112.0040](http://arxiv.org/abs/1112.0040), [slides](http://prezi.com/w0ykkhh5mxak/the-uniqueness-of-the-homotopy-theory-of-higher-categories/))


in the context of a discussion of [[(infinity,n)-categories]].

In the [[Elephant]], gaunt categories are briefly mentioned under the name "stiff categories", in the paragraph preceding B1.3.11 (about [[split fibration|splitting]] of [[Grothendieck fibrations]]).


[[!redirects gaunt category]]
[[!redirects gaunt categories]]
[[!redirects stiff category]]
[[!redirects stiff categories]]

[[!redirects strict saturated category]]
[[!redirects strict univalent category]]
[[!redirects strict saturated categories]]
[[!redirects strict univalent categories]]

[[!redirects gauntness]]