#Contents#

* automatic table of contents goes here
{:toc}

#Idea#

A _subobject classifier_ in a [[topos]] is a morphism 
$true : * \to \Omega$ such that every [[monomorphism]] $A \hookrightarrow B$ in the topos (hence every [[subobject]]) is the [[pullback]] of this morphism along a unique morphism (the [[characteristic morphism]] of $A$) $B \to \Omega$.

In this sense $\Omega$ is the [[classifying space|classifying object]] for subobjects.


#Definition#


If $C$ is a [[finitely complete category]], a _subobject classifier_ is a [[representable functor|representing object]] for the functor
$$Sub: C^{op} \to Set$$
which assigns to each object $c$ of $C$ its set of [[subobject]]s. In [[topos theory]], the subobject classifier is traditionally denoted $\Omega$; it is also called the "[[truth value]] object".

(For this description to parse, we should ask that $C$ be [[locally small category|locally small]] and [[well-powered category|well-powered]], but actually it won't matter because presently we will redefine the notion in elementary terms, without reference to [[Set]].

In more detail: given a morphism $f: c \to d$ in $C$, the function
$$Sub(f): Sub(d) \to Sub(c)$$
takes a subobject $i: t \hookrightarrow d$ to the subobject of $d$ obtained by pulling back $i$ along $f$. [An easy basic lemma of category theory states that the [[pullback]] of a mono $i$ along any morphism $f$ is still a [[monomorphism|mono]].] The representability of this functor means there is an object $\Omega$ together with a subobject $t: T \hookrightarrow \Omega$ which is *[[universal construction|universal]]*, meaning that given any subobject $i: s \hookrightarrow c$, there is a unique morphism $f: c \to \Omega$ such that $i$ is obtained as the pullback of $t$ along $f$.

It is not hard to show that the domain $T$ of the universal subobject is a [[terminal object]], typically denoted $1$. Therefore the elementary definition of subobject classifier becomes

+--{.un_defn}
A __subobject classifier__ in a finitely complete category $C$ is an object $\Omega$ together with a morphism $t: 1 \to \Omega$ such that for any mono $i: s \to c$ in $C$, there exists a unique morphism $\chi_i: c \to \Omega$ such that $i$ arises as the pullback of $t$ along $\chi_i$. The morphism $\chi_i$ is called the _classifying map_ or _characteristic map_ (of the subobject or isomorphism-equivalence class of $i$).
=--

[[global element|Elements]] $\phi: 1 \to \Omega$ are often referred to as "truth values"; the distinguished element $t: 1 \to \Omega$ is referred to as "true".  Note that these truth values correspond to the [[subterminal object]]s.

# Examples

* In the category of [[set]]s, the 2-element set $\mathbf{2} = \{f, t\}$ plays the role of $\Omega$; the morphism $t: 1 \to \mathbf{2}$ just names the element $t$. Given a [[subset]] $S \subseteq X$, the characteristic function $\chi_S: X \to \mathbf{2}$ is the function defined by $\chi_S(x) = t$ if $x \in S$, and $\chi_S(x) = f$ if $x \notin S$.

  * **Remark** It is not usually true in toposes that $\Omega$ is the coproduct $\mathbf{2} = 1 + 1$; toposes where that occurs are called _[[Boolean topos|Boolean]]. Thus the category $Set$ of sets is a Boolean topos, as is the [[presheaf]] topos $Set^G$ when $G$ is a [[groupoid]].

* The subobject classifier in a [[presheaf]] topos $PSh(S)$ is the presheaf that sends each object $U \in S$ to the set $sieves(U)$ of [[sieve]]s on it, equivalently the set of subobjects of the [[representable functor|representable]] [[presheaf]] $Y(U)$: $\Omega : U \mapsto sieves(U)$.

  * the corresponding morphism $true : * \to \Omega$ of presheaves in the [[natural transformation]] that picks over each object the _maximal sieve_ $true_U = maximal_{sieves(U)} : * \to sieves(U)$

* An example of a non-Boolean topos is the category of [[sheaf|sheaves]] over a "typical" [[topological space]] $X$ such as $\mathbb{R}$ in its usual topology. In this case, $\Omega$ is the sheaf where the set of sections over an open set $U$ is the set of open subsets of $U$, with the obvious restriction maps; the [[sheaf and topos theory|sheaf topos]] in this case is guaranteed to be non-Boolean provided there are some non-regular open sets in $X$ (a open set is _regular_ if it is the interior of its closure). The "[[internal logic]]" of such a topos is [[intuitionistic logic|intuitionistic]]. 

# Properties

The subobject classifier always comes with the structure of an internal [[partial order|poset]]; that is, a relation $\subseteq\, \hookrightarrow \Omega\times\Omega$ which is internally reflexive, antisymmetric, and transitive.  This can be constructed directly, or obtained via the [[Yoneda lemma]] since the collection of subobjects of any object is an external poset.

In fact, this internal poset is an internal [[Heyting algebra]]; it\'s an internal [[Boolean algebra]] if and only if the topos is Boolean.

#Generalizations: object classifier#

In higher topoi the the subobject classifiers are the [[generalized universal bundle|universal fibrations]]:

in the [[n-topos]] $n Cat$ of [[n-category|n-categories]] the subobject classifier is the [[stuff, structure, property|forgetful functor]]

$$
  n true : (n-1)Cat_* \to (n-1)Cat
$$

from the $n$-category of [[pointed object|pointed]] $(n-1)$-categories to that of $(n-1)$-categories, which forgets the point.

This is described in more detail at [[generalized universal bundle]]. See also the discussion at [[stuff, structure, property]].

In fact, using the notion of [[(-1)-category]] the subobject classifier in [[Set]] does fit precisely into this pattern: 

the 2-element set $\mathbf{2}$ may be regarded as the [[0-category]] of [[(-1)-category|(-1)-categories]] (of which there are two) and the one-element set $*$ is the [[0-category]] of [[pointed object|pointed]] [[(-1)-category|(-1)-categories]], of which there is one.

In the context of [[(∞,1)-topos]] [[Higher Topos Theory|theory]] subobject classifiers are discussed in section 6.1.6 of

* [[Jacob Lurie]], [[Higher Topos Theory]].

As pointed out there, it is not so much a _subobject_ classifier that matters in [[higher topos theory]], but an 

* [[object classifier]].


#References#

section I.3 and I.4 in

* MacLane-Moerdijk, [[Sheaves in Geometry and Logic]]