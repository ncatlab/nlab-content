
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Yoneda lemma
+--{: .hide}
[[!include Yoneda lemma - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _subobject classifier_ in a [[topos]] is a morphism 
$true : * \to \Omega$ such that every [[monomorphism]] $A \hookrightarrow B$ in the topos (hence every [[subobject]]) is the [[pullback]] of this morphism along a unique morphism (the [[characteristic morphism]] of $A$) $B \to \Omega$.

In this sense $\Omega$ is the [[classifying space|classifying object]] for subobjects.


## Definition

+-- {: .num_defn}
###### Definition

In a [[category]] $C$ with [[finite limit]]s, a **subobject classifier** is a [[monomorphism]] $true : * \to \Omega$ out of the [[terminal object]], such that for every [[monomorphism]] $U \to X$ in $C$ there is a unique morphism $\chi_U : X \to \Omega$ such that there is a [[pullback]] [[diagram]]

$$
  \array{
    U &\to& *   
    \\
    \downarrow && \downarrow^{\mathrlap{true}}
    \\
    X &\stackrel{\chi_U}{\to}& \Omega
  }
  \,.
$$

=--

See for instance ([MacLane-Moerdijk, p. 22](#MacLaneMoerdijk)).

+-- {: .num_remark}
###### Remark

Some terminology:

If it exists, the object $\Omega$ is also called the **object of [[truth value]]s**, a [[global element]] $K \to \Omega$ is called a **[[truth value]]** and the element $true : * \hookrightarrow \Omega$ is the truth value **[[true]]**, where all these terms allude to the [[internal logic]] of the category $C$.

Note that the subobjects classified by the truth values are [[subterminal object]]s.

The morphism $\chi_U$ is also called the **[[characteristic map]]** or **[[classifying map]]** of the subobject $U \hookrightarrow X$.

=--

+-- {: .num_prop}
###### Proposition

If $C$ has [[finite limit]]s and is in addition a [[locally small category]], then it has a subobject classifier precisely if the [[subobject]]-assigning [[presheaf]]

$$
  Sub : C^{op} \to Set
$$
$$
  X \mapsto \{U \hookrightarrow X\}/\sim
$$

is [[representable functor|representable]]. In this case the representing object is [[generalized the|the]] subobject classifier: there is a [[natural isomorphism]]

$$
  Sub(X) \simeq C(X, \Omega)
$$

in $X \in C$.

Moreover, in this case $C$ is [[well-powered category|well powered]].

=--

This appears for instance as ([MacLane-Moerdijk, prop. I.3.1](#MacLaneMoerdijk)).

In more detail: given a [[morphism]] $f: c \to d$ in $C$, the function

$$
  Sub(f): Sub(d) \to Sub(c)
$$

takes a [[subobject]] $i: t \hookrightarrow d$ to the subobject of $d$ obtained by [[pullback|pulling back]] $i$ along $f$. (Notice that [[monomorphism]]s, as discussed there, are stable under pullback.) 

The representability of this functor means there is an object $\Omega$ together with a subobject $t: T \hookrightarrow \Omega$ which is *[[universal construction|universal]]*, meaning that given any subobject $i: s \hookrightarrow c$, there is a unique morphism $f: c \to \Omega$ such that $i$ is obtained as the pullback of $t$ along $f$.

+-- {: .proof}
###### Proof

To see that a subobject classifier induces such a natural isomorphism,
we need that the morphisms $Sub(f)$ for $f \in Mor(C)$ corresponds to the morphisms $C(f,\Omega)$. This is the [[pasting law]] for [[pullback]]s.

Conversely, to see that a subobjects-representing object $\Omega$ is a subobject classifier, use that by [[natural transformation|naturality]] we have for each morphism $ \phi : X \to \Omega$ a [[commuting diagram]]

$$
  \array{
    Sub(\Omega) &\stackrel{\simeq}{\to}& C(\Omega, \Omega)
    \\
    {}^{\mathllap{Sub(\phi)}}\downarrow && \downarrow^{\mathrlap{C(\phi,\Omega)}}
    \\
    Sub(X) &\stackrel{\simeq}{\to}& C(X, \Omega)
  }
$$

whose commuativity says that every element of $Sub(X)$ is the pullback along some $\phi : X \to \Omega$ of the subobject of $\Omega$ corresponding under the natural isomorphism to $Id : \Omega \to \Omega$.

By further playing around with this one finds that this latter subobject of $\Omega$ has to be a [[terminal object]]. 

=--


## Examples

### In $Set$

In the category of [[set]]s, the 2-element set $\mathbf{2} = \{f, t\}$ plays the role of $\Omega$; the morphism $t: 1 \to \mathbf{2}$ just names the element $t$. Given a [[subset]] $S \subseteq X$, the characteristic function $\chi_S: X \to \mathbf{2}$ is the function defined by $\chi_S(x) = t$ if $x \in S$, and $\chi_S(x) = f$ if $x \notin S$.

+-- {: .num_remark}
###### Remark

It is not usually true in [[toposes]] that $\Omega$ is the [[coproduct]] $\mathbf{2} = 1 + 1$; toposes where that occurs are called _[[Boolean topos|Boolean]]. Thus the category $Set$ of sets is a Boolean topos, as is the [[presheaf]] topos $Set^G$ when $G$ is a [[groupoid]].

=--

### In a presheaf topos

The subobject classifier in a [[presheaf]] topos $PSh(S)$ is the presheaf that sends each object $U \in S$ to the set $sieves(U)$ of [[sieve]]s on it, equivalently the set of subobjects of the [[representable functor|representable]] [[presheaf]] $Y(U)$: $\Omega : U \mapsto sieves(U)$.

The corresponding morphism $true : * \to \Omega$ of presheaves is the [[natural transformation]] that picks over each object the _maximal sieve_ $true_U = maximal_{sieves(U)} : * \to sieves(U)$

#### In $G Set$

As a special case of presheaf toposes, for $G$ a [[discrete group]] and $G Set = [\mathbf{B} G, Set]$ the topos of [[permutation representation]]s, there are precisely two [[sieve]]s on the single object of the [[delooping]] [[groupoid]] $\mathbf{B}G$: the trivial one and the empty one. Hence the subobject classifier here is the 2-element set as in [[Set]], but now regarded as a $G$-set with trivial $G$-[[action]].


### In a non-boolean topos

An example of a non-[[Boolean topos]] is the [[category of sheaves]] over a "typical" [[topological space]] $X$ such as the [[real line]] $\mathbb{R}$ in its usual [[topology]]. In this case, $\Omega$ is the sheaf where the set of sections over an [[open subset]] $U$ is the set of open subsets of $U$, with the obvious restriction maps; the [[sheaf and topos theory|sheaf topos]] in this case is guaranteed to be non-Boolean provided there are some non-regular open sets in $X$ (a open set is _regular_ if it is the interior of its closure). The "[[internal logic]]" of such a topos is [[intuitionistic logic|intuitionistic]]. 


### In a slice topos

+-- {: .num_prop}
###### Proposition

Let $\mathcal{E}$ be a [[topos]] and $X \in \mathcal{E}$ any object. Write $\mathcal{E}/X$ for the corresponding [[over-topos]].

The subobject classifier of $\mathcal{E}/X$ is $p_2 : \Omega_{\mathcal{E}} \times X \to X$. 

=--

+-- {: .proof}
###### Proof

This follows for instance from the statement that the [[inverse image]] of any [[base change geometric morphism]] is a [[logical functor]] and hence preserves subobject classifiers: Here we are looking at the base change along $p : X \to *$ and hence $p^* \Omega_{\mathcal{E}}\simeq \Omega_{\mathcal{E}} \times X$.

But the statement is also easily directly checked.

=--


## Properties

The subobject classifier always comes with the structure of an internal [[partial order|poset]]; that is, a relation $\subseteq\, \hookrightarrow \Omega\times\Omega$ which is internally reflexive, antisymmetric, and transitive.  This can be constructed directly, or obtained via the [[Yoneda lemma]] since the collection of subobjects of any object is an external poset.

In fact, this internal poset is an internal [[Heyting algebra]]; it\'s an internal [[Boolean algebra]] if and only if the topos is Boolean.

## Generalizations: object classifier

In higher topoi the the subobject classifiers are the [[generalized universal bundle|universal fibrations]]:

in the [[n-topos|(n+1)-topos]] $n Cat$ of [[n-category|n-categories]] the subobject classifier is the [[stuff, structure, property|forgetful functor]]

$$
  n true : (n-1)Cat_* \to (n-1)Cat
$$

from the $n$-category of [[pointed object|pointed]] $(n-1)$-categories to that of $(n-1)$-categories, which forgets the point.

This is described in more detail at [[generalized universal bundle]]. See also the discussion at [[stuff, structure, property]].

In fact, using the notion of [[(-1)-category]] the subobject classifier in [[Set]] does fit precisely into this pattern: 

the 2-element set $\mathbf{2}$ may be regarded as the [[0-category]] of [[(-1)-category|(-1)-categories]] (of which there are two) and the one-element set $*$ is the [[0-category]] of [[pointed object|pointed]] [[(-1)-category|(-1)-categories]], of which there is one.

In the context of [[(∞,1)-topos]] [[Higher Topos Theory|theory]] subobject classifiers are discussed in section 6.1.6 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

As pointed out there, from some perspective it is not so much a _subobject_ classifier that matters in [[higher topos theory]], but an 

* [[object classifier]].


## Related concepts

* [[classifying space]], [[classifying stack]], [[moduli space]], [[moduli stack]], [[derived moduli space]]

* [[classifying topos]]

* [[universal principal bundle]], [[universal principal ∞-bundle]]

* [[classifying topos]}

* [[classifying morphism]]


## References#

section I.3 and I.4 in

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_
 {#MacLaneMoerdijk}

[[!redirects subobject classifiers]]