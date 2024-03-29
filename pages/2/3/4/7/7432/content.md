
> This article is on the mathematical concept of atom as used in the theory of [[preorder|preorders]], and related mathematical notions. For small projective objects in categories see at [[atomic object]]. For still other uses, see [[atom (disambiguation)]].


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Compact objects
+-- {: .hide}
[[!include compact object - contents]]
=--
=--
=--

# Atoms
* table of contents
{: toc}


## Idea

An atom in a [[poset]] is a [[minimal element]] among those which are not actually the [[bottom element|minimum]].  Thus an atom is as small as possible without being nothing.  In an atomic poset, every element may be broken down (typically not uniquely) into atoms. 

A related but slightly weaker concept is that of "tiny element", which has important generalizations in the context of enriched category theory. 

## Definitions

Let $S$ be a [[poset]] (or [[proset]]) with a [[bottom element]] $\bot$.  Recall that an element of $S$ is __[[positive element|positive]]__ if it is not a bottom element.  An element $a$ of $S$ is __atomic__ if, given any element $p \leq a$, $p$ is positive iff $a \leq p$.  An __atom__ of $S$ is simply an atomic element of $S$.  Note that every atom must be positive (since $a \leq a$).

The atoms are precisely the [[minimal elements]] of the set of positive elements.  For a poset, $a$ is atomic iff every $p \leq a$ is positive iff $p = a$.  Using [[classical logic]] too, $a$ is atomic iff every $p \leq a$ satisfies $p = \bot$ [[xor]] $p = a$.

The p(r)oset $S$ is __atomic__ (or more commonly in the literature, **atomistic**; see remarks below) if every element is a [[supremum]] of atoms.  In this case, every element $x$ is a supremum of those atoms $a \leq x$.  Note that $\bot$ is a supremum of no atoms, and every atom is a supremum of itself, so the condition is really about the nontrivial nonatomic elements.

In [[constructive mathematics]], we require a more complicated definition of a [[positive element]], but the other definitions above remain correct (under the stated conditions), once we have that.  In [[predicative mathematics|predicative]] constructive mathematics, positivity cannot be defined at all, and $S$ must come equipped with a [[positivity predicate]] before we may consider its atoms.



### Remarks on terminology 

There is some terminological variance in the literature to the notion of atomic poset as defined here. In particular, [Wikipedia](http://en.wikipedia.org/wiki/Atom_%28order_theory%29) defines an _atomic poset_ to be a poset in which every positive element has an atom below it, and refers to our stronger notion of atomic poset by the term "atomistic poset". Note well that the Wikipedia conventions seem to be the ones observed in most lattice-theoretic texts. 

"Atomic" and "Atomistic" differ for the simple example of the [[divisor lattice]] for some number $n$. The atoms in this lattice are prime numbers while it may also contain [[semi-atom|semi-atoms]] which are powers of primes. This lattice is atomic because any object not the [[bottom]],  $1$, is divisible by a prime in the lattice. However it is not generally atomistic, but is instead uniquely semi-atomistic (every  object is the product of a unique set of semi-atoms with bottom corresponding to the empty set), which is one way of stating the [[fundamental theorem of arithmetic]], also known as the *unique factorization theorem*.

The two notions coincide in the case of complete Boolean algebras $B$. Indeed, suppose $B$ is atomic in the Wikipedia sense, and for any element $b \in B$, consider the relative complement 

$$c = b \wedge \neg (\bigvee \{atoms\, a: a \leq b\})$$ 

To show $B$ is atomistic, it suffices to show $c = 0$. If not, then there is an atom $a'$ such that $a' \leq c$, which means both $a' \leq b$ and 

$$a' = a' \wedge a' \leq a' \wedge \bigvee \{atoms\, a: a \leq b\} = 0$$ 

since $a' \leq \neg(\bigvee \{atoms\, a: a \leq b\})$. This is a contradiction. 

Our (*pro tem*) decision to define the word "atomic" in the idiosyncratic nLab sense above is consistent with its use elsewhere in category theory; see the sections below on atomic objects and on categorification. 


## Examples

+-- {: .num_example}
###### Example

In a [[power set]] the atoms are the [[singleton subsets]].  Every power set is atomic, and in fact every atomic [[complete boolean algebra]] is (up to [[isomorphism]]) a power set.

=--

+-- {: .num_example}
###### Example

In a [[lattice of subtoposes]] the atoms are the 2-valued [[Boolean toposes]]. See [this proposition](subtopos#BooleantoposesAreAtoms).

=--

## Properties

If $a$ is an atom in a [[lattice]] or more generally a [[meet]] [[semilattice]] and $b$ any other element then (using classical logic)
$$ a \wedge b \in \{a, \bot\} .$$
This is simply because $a \wedge b \leq a$, so equals either $a$ or $\bot$.


## Atoms and tiny elements 

If $E$ is a poset or preorder, in other words a $\mathbf{2}$-[[enriched category]], an element $e \in E$ is _[[tiny object|tiny]]_ if the hom $E(e, -)\colon E \to \mathbf{2}$ preserves all [[supremum|sups]] that exist in $E$. It is arguable (from an [[nPOV]]) that the weaker concept of tiny element is more fundamental than the notion of atom; for example, as we will see below, replacing atoms by tiny elements permits one to generalize the characterization of power sets as complete atomic Boolean algebras. 

+-- {: .num_prop}
###### Proposition 
A tiny element in a Boolean algebra is precisely an atom. 
=-- 

+-- {: .proof}
###### Proof 
Let $a$ be an atom. Let $\{x_i\}$ be a collection of elements that admits a supremum such that $a \leq \bigvee_i x_i$. Then 

$$a = a \wedge \bigvee_i x_i = \bigvee_i a \wedge x_i$$ 

(where the second equation holds since $a \wedge -$ is a left [[adjoint functor|adjoint]], because $B$ is a [[Heyting algebra]]). Since $a$ is positive, for some $i$ the element $a \wedge x_i$ is positive as well. Trivially it holds that $a \wedge x_i \leq a$; since $a$ is an atom, the inequality is an equality. Thus $a \leq x_i$ for some $i$, which is what we want. 

If $a$ is not an atom, i.e., if $0 \lt b \lt a$ for some $b$, then 

$$a = b \vee (a \wedge \neg b)$$ 

If $B(a, -)$ preserved the join on the right, then either $a \leq b$ which is evidently false, or $a \leq a \wedge \neg b$, i.e., $a \leq \neg b$, i.e., $b = a \wedge b \leq 0$, also evidently false. Thus $B(a, -)$ does not preserve suprema. 
=-- 

Only one half of this proposition holds (an atom is a tiny element) if we replace the Boolean algebra $B$ by a general [[frame]]. (In fact, this direction even holds in impredicative constructive mathematics, if the frame is equipped with a [[positive element|positivity predicate]].) On the other hand, tiny elements need not be atoms (an easy example is the frame of down-sets of a [[poset]], where principal down-sets are atomic objects, but generally not atoms in the underlying poset of the frame). 

Be this as it may, [Lawvere](http://www.acsu.buffalo.edu/~wlawvere/ToposMotion.pdf#page=6) has written, "In order to settle once and for all the various terminological differences, perhaps we can use a.t.o.m. as an abbreviation for 'amazing tiny object model'." This is Lawvere's 'objective' way of abbreviating "atomic object"; the word 'amazing' here is presumably chosen to evoke what Lawvere has called the "amazing right adjoint" to an exponential functor $(-)^D$, particularly in the case of [[synthetic differential geometry]] where such adjoints exist for [[infinitesimal object|infinitesimal objects]] $D$. 


## Generalization and categorification 

The result that an atomic complete Boolean algebra is isomorphic to a power set -- hence to a [[presheaf]] with values in the [[0-category]] $\mathbf{2} = (-1)Grpd$ of [[(-1)-groupoid|(-1)-groupoids]] -- may be generalized and categorified as follows.  

Let $E$ be a $V$-category, where $V$ is a [[cosmos]] (a complete, cocomplete, symmetric monoidal closed category). We define an object $e$ of $E$ to be **tiny** or **atomic** if $E(e, -) \colon E \to V$ preserves any $V$-colimit that exists in $E$. (As usual, the appropriate notion of colimit in the enriched setting is [[weighted colimit]].) 

In what follows, we suppose the full $V$-subcategory $Tiny(E)$ of atomic objects in $E$ is essentially small. The inclusion $i \colon Tiny(E) \hookrightarrow E$ induces a restricted Yoneda embedding 

$$E \to V^{Tiny(E)^{op}}$$ 

sending an object $e$ to $E(i-, e)$. We say that $E$ is **[[atomic category|atomic]]** if $i \colon Tiny(E) \hookrightarrow E$ is $V$-[[dense functor|dense]], in other words if every object $e$ of $E$ is a canonical colimit of atomic objects below it, in the precise sense that the following enriched [[coend]] exists, and its canonical map to $e$, 

$$\int^{a \in Tiny(E)} E(i a, e) \cdot i a \to e,$$ 

is an isomorphism. 

If $E$ is a preorder, i.e., is $\mathbf{2}$-enriched where $\mathbf{2}$ is the category of $(-1)$-categories, the coend amounts to the supremum 

$$\sup \{i a: i a \leq p\}$$ 

so that $E$ is atomic precisely if every element is the sup of the tiny elements below it. 

+-- {: .num_thm} 
###### Theorem 
A small-cocomplete atomic preorder $E$ is equivalent to the free sup-lattice $2^{T^{op}}$ generated by the preorder $T = Tiny(E)$ of tiny elements. Conversely, every free sup-lattice $2^{T^{op}}$ is small-cocomplete and atomic, where $T$ is the poset of tiny elements. 
=-- 

N.B. "Free sup-lattice" refers to a left adjoint of the forgetful functor $U \colon SupLat \to Preord$ from sup-lattices to preorders. 

+-- {: .proof} 
###### Proof 
Since $E$ is cocomplete, and since $\mathbf{2}^{Tiny(E)^{op}}$ is the free sup-lattice or cocomplete preorder generated from $Tiny(E)$, the inclusion $i \colon Tiny(E) \to E$ extends uniquely to a sup-preserving map 

$$L \colon \mathbf{2}^{Tiny(E)^{op}} \to E$$ 

which sends $X \colon Tiny(E)^{op} \to \mathbf{2}$ to 

$$\int^{a \in Tiny(E)} X(a) \cdot i a = \sup \{i a: X(a) = 1\}.$$

This $L$ is left adjoint to the restricted Yoneda embedding $R \colon E \to \mathbf{2}^{Tiny(E)^{op}}$. The condition that $E$ is atomic says that for each $e \in E$, the value of the counit of $L \dashv R$ at $e$ is an isomorphism 

$$\int^a E(i a, e) \cdot i a \cong e.$$ 

On the other hand, the value of the unit of $L \dashv R$ at an object $X$ is given by a string of isomorphisms 

$$\array{
X & \stackrel{Yoneda}{\cong} & \int^a X(a) \cdot Tiny(E)(-, a) \\
 & \cong & \int^a X(a) \cdot E(i-, i a) \\
 & \cong & E(i-, \int^a X(a) \cdot i a)
}$$ 

where the last isomorphism obtains from the fact that $E(i a, -)$ preserves colimits if $a$ is tiny. Thus the unit is also an isomorphism. 

For the converse: each representable object $T(-, t)$ of $\mathbf{2}^{T^{op}}$ is tiny, because the covariant functor $2^{T^{op}}(T(-, t), -)$, being the same as evaluation at $t$ by the Yoneda lemma, preserves colimits. Furthermore, every functor $X: T^{op} \to \mathbf{2}$ is a canonical colimit of representables, so that $2^{T^{op}}$ is atomic in addition to being cocomplete. 
=-- 

+-- {: .num_cor}
###### Corollary 
A complete atomic Boolean algebra $B$ is isomorphic to $2^T$, where $T$ is the discrete preorder of atoms of $B$. 
=-- 

The argument given for the theorem above carries over without obstruction to the general enriched setting. In particular, replacing $\mathbf{2} = (-1)$-$Cat$ by its categorification $Set = 0$-$Cat$, we get the following result, first enunciated in Bunge's thesis. 

+-- {: .num_thm}
###### Theorem (Bunge)
A category $E$ is equivalent to a [[presheaf topos]] (functors with values in the 1-category [[Set]] of [[0-groupoids]]) if and only if it is cocomplete and atomic as a $Set$-category. Representables $C(-, c)$ are (among the) atomic objects of $Set^{C^{op}}$, and generate the presheaf topos by closing under all small colimits. 
=-- 

(The literal statement in Bunge's thesis is that a category is equivalent to a presheaf category $Set^{C^{op}}$ if and only if it is cocomplete, regular, and has a generating set of atomic objects, but this is trivially the same since presheaf toposes are of course [[regular category|regular]].)  

## Related concepts 

* [[compact object]] 

* [[connected object]] 

* [[Cauchy completion]] 


[[!redirects atom]]
[[!redirects atoms]]
[[!redirects atomic element]]
[[!redirects atomic elements]]