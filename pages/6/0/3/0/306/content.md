
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Subsets $A$ of a set $X$ correspond precisely to maps from $X$ to the set of truth values of classical logic via their [[characteristic function]] $\chi_A:X\to \{0,1\}$. The concept of a **subobject classifier** generalizes this situation to [[toposes]] other than [[Set]]:

A _subobject classifier_ in a [[topos]] is a morphism 
$true : * \to \Omega$ such that every [[monomorphism]] $A \hookrightarrow B$ in the topos (hence every [[subobject]]) is the [[pullback]] of this morphism along a unique morphism (the [[characteristic morphism]] of $A$) $B \to \Omega$.

In this sense $\Omega$ is the [[classifying space|classifying object]] for subobjects and $true : * \to \Omega$ the _generic_ subobject.

The existence of a subobject classifier in a category is a powerful property which induces much other structure that lies at the heart of [[topos theory]].

By restricting the class of monomorphism appropriately, the concept can be relativized to the concept of an _**M**-subobject classifier_[^weak]: e.g. demanding only classification of strong monomorphisms leads to [[quasitopos|quasitoposes]].

In [[type theory]], a [[type]] closely related to the subobject classifier is the [[type of propositions]], often denoted $Prop$ or (sometimes in [[homotopy type theory]]) $hProp$.

[^weak]: For **M** the class of strong monomorphisms, this is called a _weak subobject classifier_ in Johnstone (2002, p.120).

## Definition

+-- {: .num_defn}

###### Definition

In a [[category]] $C$ with [[finite limit]]s, a **subobject classifier** is a [[monomorphism]] $true : * \to \Omega$ out of the [[terminal object]], such that for every [[monomorphism]] $U \to X$ in $C$ there is a unique morphism $\chi_U : X \to \Omega$ such that there is a [[pullback]] [[diagram]] of the following form:

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

See for instance ([MacLane-Moerdijk, p. 32](#MacLaneMoerdijk)).

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

takes a [[subobject]] $i: t \hookrightarrow d$ to the subobject of $c$ obtained by [[pullback|pulling back]] $i$ along $f$. (Notice that [[monomorphism]]s, as discussed there, are stable under pullback.) 

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

whose commutativity says that every element of $Sub(X)$ is the pullback along some $\phi : X \to \Omega$ of the subobject of $\Omega$ corresponding under the natural isomorphism to $Id : \Omega \to \Omega$.

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

+-- {: .num_prop}
###### Proposition

The subobject classifier in a [[presheaf topos]] $PSh(S)$ is the [[presheaf]] that sends each [[object]] $U \in S$ to the [[set]] $sieves(U)$ of [[sieves]] on it

$$
  \Omega 
    \;\colon\; 
  U \mapsto sieves(U)
$$

Here $sieves(U)$ is equivalently the set of [[subobjects]] of the [[representable functor|representable]] [[presheaf]] $Y(U)$.


The corresponding morphism $true : * \to \Omega$ of presheaves is the [[natural transformation]] that picks over each object the _maximal sieve_ $true_U = maximal_{sieves(U)} : * \to sieves(U)$.

=--

+-- {: .num_remark}
###### Remark

If one views a [[presheaf]] over a [[small category]] $S$ as a set varying (or evolving) over $S$, then the subobject classifier in $PSh(S)$ may be viewed as encapsulating the ways of an element to be in the set ranging from 'never' to 'always' being in the set. 

In $Set = PSh(\ast)$ these two extremes are the only possibilities, but in the general case there are ways to become an element 'over time'. 

It might be helpful to have a look at the simple example of a subobject classifier in the presheaf topos of directed graphs worked out at [[Quiv]] to get some intuition.

=--

#### In $G Set$

As a special case of presheaf toposes, for $G$ a [[discrete group]] and $G Set = [\mathbf{B} G, Set]$ the topos of [[G-sets]], there are precisely two [[sieves]] on the single object of the [[delooping]] [[groupoid]] $\mathbf{B}G$: the trivial one and the empty one. Hence the subobject classifier here is the 2-element set as in [[Set]], but now regarded as a $G$-set with trivial $G$-[[action]].

For toposes of (left) actions of general [[monoid|monoids]] $M$ the picture changes dramatically, since then there will usually exist non-trivial left ideals and, accordingly, the structure of $\Omega$ will become richer: Its underlying set has elements all left ideals, with $m\in M$ acting on a left ideal $L$ by mapping it to the left ideal $\{n\in M| n\cdot m\in L\}$. (Of course, the same description of $\Omega$ applies to the case of groups as well, it is just, that groups lack non-trivial left ideals!)

### In a sheaf topos
The following is adapted from p. 34 of [Caramello](#Caramello).

Let $(C, J)$ be a [[site|Grothendieck site]]. A [[sieve]] $S$ on an object $c \in C$ is $J$-closed when, for any arrow $f :d \to c$, if $f^*(S) \in J(d)$ then $f \in S$. It's called *closed* since this is a closure property: $S$ contains all arrows it covers. If $(C, J)$ is a [[locale]] with the open covers topology, then this condition means that $S$ is a collection of subopens of $c$ which is closed under unions. Clearly, every sieve on $c$ can be saturated to a closed one.

The subobject classifier of $\mathrm{Sh}(C,J)$ is defined on objects as
$$
  \Omega_J(c) = \{ S | \text{S is a J-closed sieve on c} \}
$$
and on morphisms as
$$
  \Omega_J(f : c \to d) = f^*
$$
where $f^*$ denotes, as above, pullback of [[sieve|sieves]].

The arrow $\mathsf{true} : 1 \to \Omega_J$ picks the maximal sieve on each object (the one generated by the identity).

Given a mono $m : B \to A$, the classifying arrow $\chi_m : A \to \Omega_J$ is given by
$$
  \chi_m(c)(x) = \{f : d \to c | A(f)(x) \in A'(d)\},
$$
for any $c \in C$ and $x \in A(c)$.

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

### In a non-topos 

The category $Set_\ast$ of [[pointed sets]] has a subobject classifier (specified up to unique isomorphism as the pointed set with two elements). 

If one is willing to admit non-locally small categories, then the category of [[proper class|classes]] in [[ZFC]] is not a topos (it is not cartesian closed) but has a subobject classifier: any two-element set.

The opposite of the category of commutative von Neumann algebras has a subobject classifier given by $\mathbb{C}^2$ [according to Simon Henry on MathOverflow](https://mathoverflow.net/questions/384346/is-the-opposite-category-of-commutative-von-neumann-algebras-a-topos), but is not a topos because it is not cartesian closed (see Dmitri Pavlov's answer to the same MathOverflow question).


## Properties

Suppose a category $\mathbf{C}$ has a subobject classifier; this entails some striking structural consequences for $\mathbf{C}$. We list a few here: 

+-- {: .num_prop #regular} 
###### Proposition
Every [[monomorphism]] in $\mathbf{C}$ is a [[regular monomorphism]], i.e. is an [[equalizer]] of some pair of maps. 
=-- 

+-- {: .proof} 
###### Proof 
For $\chi_i: X \to \Omega$ the characteristic map of a mono $i: A \to X$, we find that $i$ is the equalizer of a pair of maps $X \rightrightarrows \Omega$: 

$$\array{
 & & 1 \\
 & \mathllap{!} \nearrow & \downarrow \mathrlap{t} \\
X & \underset{\chi_i}{\to} & \Omega.
}$$ 
=-- 

+-- {: .num_cor} 
###### Corollary 
$\mathbf{C}$ is [[balanced category|balanced]], i.e., a morphism in $\mathbf{C}$ is an isomorphism iff it is both [[monomorphism|monic]] and [[epimorphism|epic]]. 
=-- 

+-- {: .proof} 
###### Proof 
"Only if" is trivial. The "if" comes from the fact that an epic (epimorphic) equalizer must be an isomorphism, for if $i: A \to X$ is the equalizer of $f, g: X \rightrightarrows Y$ and $i$ is epic, then $f = g$, whence $1_X$ is their equalizer, so $i: A \to X$ must have been an isomorphism. 
=-- 

+-- {: .num_prop} 
###### Proposition 
Any two epi-mono factorizations of a map in $\mathbf{C}$ are canonically isomorphic. 
=-- 

+-- {: .proof} 
###### Proof 
Suppose $i p = j q$ where $p, q$ are epic and $i, j$ are monic. Since $j$ is regular, it is the equalizer of some parallel pair $f, g$ as in the diagram 

$$\array{
A & \stackrel{p}{\to} & B & & \\ 
\mathllap{q} \downarrow & & \downarrow \mathrlap{i} & & \\ 
C & \underset{j}{\to} & D & \stackrel{\overset{f}{\to}}{\underset{g}{\to}} & E,
}$$ 

so that $f i p = f j q = g j q = g i p$, whence $f i = g i$ since $p$ is epic, whence $i$ factors through $j$ as $j$ is the equalizer: $i = j k$ for some $k: B \to C$. Then also $k p = q$ since $j k p = i p = j q$ and $j$ is monic. We have that $k$ is monic since $i$ is, and $k$ is epic since $q$ is. Thus $k$ is an isomorphism. 
=-- 

Already these results impose some tight restrictions on $\mathbf{C}$. We get some more by exploiting the internal structure of $\Omega$. 

The subobject classifier always comes with the structure of an internal [[partial order|poset]]; that is, a relation $\subseteq\, \hookrightarrow \Omega\times\Omega$ which is internally reflexive, antisymmetric, and transitive.  This can be constructed directly (see Proposition \ref{implication} below), or obtained via the [[Yoneda lemma]] since the collection of subobjects of any object is an external poset.

Similarly, since we assume that $\mathbf{C}$ is finitely complete, each subobject poset $Sub(X)$ has intersections (gotten as pullbacks or [[fiber products]] of pairs of monics $i: A \to X,j: B \to X$), and the intersection operation 

$$\cap: Sub(X) \times Sub(X) \to Sub(X)$$ 

is natural in $X$. Hence we have a family of maps 

$$\cap: \hom(X, \Omega \times \Omega) \to \hom(X, \Omega)$$ 

natural in $X$; by the [[Yoneda lemma]], we infer the presence of an internal intersection map 

$$\wedge: \Omega \times \Omega \to \Omega$$ 

making $\Omega$ an internal [[meet-semilattice]]. 

More significantly, $\Omega$ is an internal [[Heyting algebra]]. More accurately, it's a Heyting algebra provided it has joins; without joins it is a [[cartesian closed category|cartesian closed]] poset: 

+-- {: .num_prop #implication} 
###### Proposition 
There is an internal implication operator 

$$\Rightarrow: \Omega \times \Omega \to \Omega$$ 

uniquely specified by the internal condition 

$$w \wedge u \leq v \qquad iff \qquad w \leq u \Rightarrow v.$$ 
=-- 

+-- {: .proof} 
###### Proof (sketch) 
Construct $\subseteq \hookrightarrow \Omega \times \Omega$ as the equalizer of the pair of maps 

$$\Omega \times \Omega \stackrel{\overset{\pi_1}{\longrightarrow}}{\underset{\wedge}{\longrightarrow}} \Omega$$ 

and then define $\Rightarrow: \Omega \times \Omega \to \Omega$ to be the characteristic map of $\subseteq \hookrightarrow \Omega \times \Omega$. Now if $\chi_u, \chi_v$ are two maps $X \to \Omega$, one calculates that $w \hookrightarrow X$ is contained in the subobject classified by $\chi_u \Rightarrow \chi_v$ iff $w \cap u = w \cap u \cap v$, which is just a way of saying $w \cap u \leq v$. 
=-- 

+-- {: .num_cor} 
###### Corollary 
In every subobject poset $Sub(X)$, meets distribute over any joins that exist. 
=-- 

+-- {: .proof} 
###### Proof 
Because $U \cap -$ is left adjoint to the external operator $U \Rightarrow -$ on $Sub(X)$, it preserves any joins that happen to exist in $Sub(X)$. 
=-- 

Normally these results are proved in the context of [[toposes]], where we may say for example that $\Omega$ is an internal [[Boolean algebra]] if and only if the topos is [[Boolean topos|Boolean]]. But as the proofs above indicate, we need only exploit the definition of subobject classifier making reference only to finite limit structure. 

In a topos, the subobject classifier $\Omega$ is always [[injective object|injective]], and, so is the _power object_ $\Omega^X$ for every object $X$ (See at [[injective object#Exponential_injectives|injective object]] for some of the details). In particular, every object $X$ embeds into an injective object by the singleton monomorphism $X\to\Omega^X$: 'A topos has enough injective objects!'. More generally, injective objects in a topos are precisely the ones that are retracts of some $\Omega^X$ (Cf. [Borceux 1994](#Borceux3), p.315; [Moerdijk-MacLane 1994](#MoerdijkMacLane), p.210).

### Johnstone's exercise 

A curiosity from Johnstone's [Topos Theory](#J77), posed as an exercise, is that any monomorphism $\Omega \to \Omega$ is an isomorphism and even an [[involution]]. Thus $\Omega$ is a [[Hopfian object]]. 

An online proof may be found [here](https://ncatlab.org/toddtrimble/published/Monic+endomorphisms+on+the+subobject+classifier). 

## Categories with a contractible subobject classifier

Suppose a [[topos]] $\mathcal{E}$ has a [[connected component|connected components functor]] $\Pi$ [[left adjoint]] to $\Delta\dashv \Gamma$ assigning to an object $X$ the set of it connected components. We call $X$ [[connected object|connected]] if $\Pi(X)$ is a [[singleton]] and [[contractible space|contractible]] if $\Pi(X^Y)$ is connected for all $Y\in\mathcal{E}$. It can be shown that provided $\Pi$ preserves [[finite products]], $\Omega$ is contractible iff $\Omega$ is connected which in turn implies the same for all other [[injective object|injective objects]] (see at [[sufficiently cohesive topos]]).

Now the subobject classifier $\Omega$ has always two disjoint points $\mathsf{true}$, $\mathsf{false}$ whence provided it is connected we can view it (together with its Heyting algebra structure) has a (highly nonlinear) generalized [[interval object]] and define a notion of [[homotopy]] relative to $\Omega$. The intuition here is that [[true|truth]] and [[false|falsity]] are continuously connected in such toposes and blend into each other, endowing (the logic in) $\mathcal{E}$ with a certain [[Hegel|Hegelian]] flavor. The contractability of $\Omega$ was taken as a key property of a [[gros topos]] of spaces by [[William Lawvere]]. Further information on this particular class of [[cohesive topos|cohesive toposes]] and discussion of properties of $\Omega$ relevant in this context is at [[sufficiently cohesive topos]].

## Categories without subobject classifiers

As the previous section indicates, having a subobject classifier is a very strong property of a category and "most" categories with finite limits don't have one.

For example, there is an easy condition ensuring a category[^1] with a terminal object can't have a subobject classifier: if there are no nonidentity morphisms out of the terminal object. This includes the following examples. 

[^1]: We mean a nontrivial category, obviously, where "trivial" here means every object is terminal. 

* Any top bounded partial order.

* In $Ring$, the [[category of rings]], there are no nonidentity morphisms out of the terminal object the [[zero ring]].

Here's another obstacle: 

* If an [[abelian category]] had a subobject classifier, every subobject of every object would have to be the kernel of its classifying map. In particular, the subobject $0$ of every object $A$ would have to be the kernel of its classifying map, so that every object in this abelian category would embed into the subobject classifier $\Omega$ (including, say, all small products of $\Omega$ with itself) which in nontrivial cases would cause size issues.

But a real killer is the fact that all monos are regular, or its consequences of the category being balanced and uniqueness of epi-mono factorizations: 

* The categories [[Pos]], [[Cat]], [[Top]] are not balanced (consider the map from a discrete structure on a set to an indiscrete structure on the same set, induced by the identity function). The category [[CMon]] is not balanced (consider the inclusion $\mathbb{N} \hookrightarrow \mathbb{Z}$ which is epic). 

Even though all monos in [[Grp]] are regular, we can kill off $Grp$ by observing that if $t: 1 \to \Omega$ were a subobject classifier, the proof of Proposition \ref{regular} indicates that every mono $i: A \to X$ would have to be the [[kernel]] of $\chi_i$. But not all monos in $Grp$ are kernels. 

Perhaps an even more decisive killer is the observation that meets distribute over (arbitrary) joins in subobject orders. This eliminates many categories from consideration: 

* Lattices of subobjects in $Grp$ or $Ab$ are rarely distributive. 

* For any nontrivial category with [[biproducts]], there are non-distributive subobject lattices. Take any object $A$, so that we have three subobjects $i_1: A \to A \oplus A$, $i_2: A \to A \oplus A$, and $\Delta: A \to A \oplus A$. Then $i_1 \vee i_2 = \top$, whereas $i_1 \wedge \Delta = \bot = i_2 \wedge \Delta$. Under distributivity we have 
$$\Delta = \Delta \wedge \top = \Delta \wedge (i_1 \vee i_2) = (\Delta \wedge i_1) \vee (\Delta \wedge i_2) = \bot \vee \bot = \bot$$ 
but $\Delta = \bot$ forces $A = 0$. So the only such category that can have a subobject classifier is trivial. 


## Generalizations

### Weak subobject classifier

There are many subclasses of [[monomorphisms]], such as [[regular monomorphisms]], [[strong monomorphisms]], and [[extremal monomorphisms]]. As a result, there are weaker forms of subobject classifiers that only classify a subclass of monomorphisms instead of all monomorphisms. 

Suppose there is a [[category]] $C$ with [[finite limit]]s. Let $S$ be a subclass of [[monomorphisms]] in $C$, whose elements we shall refer to as $S$-monomorphisms. An $S$-**subobject classifier** is an $S$-[[monomorphism]] $true : * \to \Omega$ out of the [[terminal object]], such that for every $S$-[[monomorphism]] $U \to X$ in $C$ there is a unique morphism $\chi_U : X \to \Omega$ such that there is a [[pullback]] [[diagram]] of the following form:

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

* If $S$ is the class of all [[monomorphisms]] in $C$, then $\Omega$ is just a **subobject classifier**. 
* If $S$ is the class of all [[extremal monomorphisms]] in $C$, then $\Omega$ is an **extremal subobject classifier**. 
* If $S$ is the class of all [[strong monomorphisms]] in $C$, then $\Omega$ is a **strong subobject classifier**. 
* If $S$ is the class of all [[regular monomorphisms]] in $C$, then $\Omega$ is a **regular subobject classifier**. 
* If $S$ is the class of all [[effective monomorphisms]] in $C$, then $\Omega$ is an **effective subobject classifier**. 
* If $S$ is the class of all [[strict monomorphisms]] in $C$, then $\Omega$ is a **strict subobject classifier**. 

Strong subobject classifiers in particular are important in the definition of a [[quasitopos]]. 

### Object classifier

In higher topoi the subobject classifiers are the [[generalized universal bundle|universal fibrations]]:

In the [[(n,1)-topos|(n+1,1)-topos]] $n Grpd$ or $(n,0) Cat$ of [[n-groupoid|(n,0)-categories]] the subobject classifier is the [[stuff, structure, property|forgetful functor]]

$$
  (n,1) true : (n-1,0)Cat_* \to (n-1,0)Cat
$$

from the $(n,1)$-category of [[pointed object|pointed]] $(n-1,0)$-categories to that of $(n-1,0)$-categories, which forgets the point.

This is described in more detail at [[generalized universal bundle]]. See also the discussion at [[stuff, structure, property]].

In fact, using the notion of [[(-1)-category|(-1,0)-category]] the subobject classifier in [[Set]] does fit precisely into this pattern: 

the set of truth values $\Omega$ may be regarded as the [[(0,1)-category]] of [[(-1)-category|(-1,0)-categories]] (of which there are two) and the one-element set $*$ is the [[(0,1)-category]] of [[pointed object|pointed]] [[(-1)-category|(-1,0)-categories]], of which there is one.

In the context of [[(∞,1)-topos]] [[Higher Topos Theory|theory]] subobject classifiers are discussed in section 6.1.6 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ , Princeton UP 2009.

Whereas for 1-toposes the _subobject classifier_ is the key structural ingredient (besides the exactness properties), in [[higher topos theory]] this role is taken over by the [[object classifier]], as pointed out in Lurie (2009).


## Related concepts

* [[quasitopos]] where a weaker notion of subobject classifier only classifies [[strong monomorphism]]s. 

* [[discrete object classifier]]

* [[(sub)object classifier in an (infinity,1)-topos]]

* [[type of propositions]], [[type of types]]

* [[classifying space]], [[classifying stack]], [[moduli space]], [[moduli stack]], [[derived moduli space]]

* [[classifying topos]]

* [[universal principal bundle]], [[universal principal ∞-bundle]]

* [[classifying morphism]]

* [[sufficiently cohesive topos]]

* [[localic topos]]


## References#

The concept was introduced in

* [[William Lawvere]], _Quantifiers and sheaves_ , Actes Congrès intern. math. **1** (1970), pp.329-334. ([pdf](http://www.mathunion.org/ICM/ICM1970.1/Main/icm1970.1.0329.0334.ocr.pdf)) 

Discussion of the concept can be found in the usual suspects

* [[Francis Borceux]], _Handbook of Categorical Algebra 3_ , Cambridge UP 1994. {#Borceux3}

* {#Goldblatt84} R. Goldblatt, *Topoi - The Categorical Analysis of Logic*, 2nd ed. North-Holland Amsterdam 1984. (Dover reprint New York 2006; [project euclid](http://projecteuclid.org/euclid.bia/1403013939))

* {#J77}[[Peter Johnstone]], _Topos Theory_ , Academic Press New York 1977.

* [[Peter Johnstone]], _Sketches of an Elephant I_ , Oxford UP 2002.

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ , Springer Heidelberg 1994. (section I.3-4)
 {#MacLaneMoerdijk}  

See also

* [[Francis Borceux]], _When is $\Omega$ a cogenerator in a topos ?_ , Cah. Top. Géom. Diff. Cat. **XVI** no.1 (1975) pp.3-15. ([numdam](http://www.numdam.org/item?id=CTGDC_1975__16_1_3_0))

For sheaves

* {#Caramello}[[Olivia Caramello]], _Topos Theory: Lectures 7-14: Sheaves on a site_, [slides](https://www.oliviacaramello.com/Teaching/Lectures7_to_14.pdf)

[[!redirects subobject classifiers]]
