
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea
**Atomic sites** are [[sites]] $(\mathcal{C}, J_{at})$ equipped with the _atomic topology_ $J_{at}$. The corresponding [[sheaf toposes]] $Sh(\mathcal{C}, J_{at})$ are precisely the [[atomic topos|atomic Grothendieck toposes]].

## Definition

+-- {: .num_defn}
###### Definition

A [[site]] $(\mathcal{C}, J_{at})$ is called **atomic** if the [[covering sieve|covering]] [[sieves]] $S$ of $J_{at}$ are exactly the [[inhabited set|inhabited]] sieves $S\neq\emptyset$. A [[Grothendieck topology]] $J_{at}$ of this form is called _atomic_.
=--

## Example

Let $FinSet^{op}_{mono}$ be the opposite of the category $FinSet_{mono}$ with objects finite sets and monomorphisms. Then $(FinSet^{op}_{mono}, J_{at})$ is an atomic site and the corresponding sheaf topos $Sh(FinSet^{op}_{mono}, J_{at})$ is the [[Schanuel topos]].
That $J_{at}$ is indeed a [[Grothendieck topology]] is ensured by prop. \ref{atomic_ore}.

## Properties

+-- {: .num_prop #atomic_ore}
###### Proposition
Let $\mathcal{C}$ be a [[category]]. Then $\mathcal{C}$ can be made into an atomic site if and only if for any diagram
$$
\array{
  & & A \\
  & & \downarrow\\
  B & \to & C
}
$$
there is an object $D$ and arrows $D \to A, B$ such that the following diagram commutes:
$$
\array{
  D & \to & A \\
  \downarrow & & \downarrow\\
  B & \to & C
}
$$
=--

+-- {: .proof}
###### Proof
This is exactly what is needed for the pullback stability axiom to hold, and the other axioms are immediate.
=--

The condition occurring in the proposition is called the (right) [[Ore condition]]. It is a result by [[Peter Johnstone|P. T. Johnstone]] (1979) that $Set^{\mathcal{C}^{op}}$ is a [[De Morgan topos]] precisely if $\mathcal{C}$ satisfies the Ore condition. Whence we see that every [[atomic topos|atomic Grothendieck toposes]] is a ([[Boolean topos|Boolean]]) subtopos of a De Morgan [[presheaf topos]].

Recall that the [[dense topology]] $J_d$ on a category $\mathcal{C}$ consists of all sieves $S\in J_d(C)$ with the property that given $f:D\to C$ there exists $g:E\to D$ such that $f\cdot g\in J_d(C)$. The atomic topology is a special case of this:

+-- {: .num_prop #atomic_dense}
###### Proposition
Let $\mathcal{C}$ be a [[category]] satisfying the [[Ore condition]]. Then the atomic topology $J_{at}$ coincides with the dense topology $J_d$.
=--

+-- {: .proof}
###### Proof
For $\mathcal{C}=\emptyset$ the claim is trivial. So let $C\in\mathcal{C}$ be an object and $S$ a sieve on $C$.

Assume $S\in J_d(C)$, then for $id\colon C\to C$ there exists $g:E\to C$ with $id\cdot g\in S$ whence $S\in J_{at}(C)$.

Conversely, assume $S\in J_{at}(C)$ and let $f:D\to C$ be a morphism. Then there exists $g\in S$ by assumption and the diagram $D\overset{f}{\rightarrow} C \overset{g}{\leftarrow} E$ can be completed to a commutative square $f\cdot i = g\cdot h$ but $g\cdot h\in S$ since $g\in S$ and $S$ is a sieve. Whence $f \cdot i\in S$ and, accordingly, $S\in J_d(C)$.
=--

In other words, the atomic topology is just the [[dense topology]] on a categories satisfying the Ore condition. Since the corresponding sheaf toposes of the dense topology are just the double negation subtoposes of the corresponding presheaf topos we finally get: 

+-- {: .num_prop}
###### Proposition
Atomic Grothendieck toposes i.e. toposes (equivalent to) $Sh(\mathcal{C}, J_{at})$ for $(\mathcal{C}, J_{at})$ an atomic site are precisely (the toposes  equivalent to) the [[double negation|double negation subtoposes]] $Sh_{\neg\neg}(Set^{\mathcal{C}^{op}})$ for a De Morgan presheaf topos $Set^{\mathcal{C}^{op}}$. $\qed$
=--

The sheaves of atomic sheaf toposes $Sh(\mathcal{C}, J_{at})$ are easy to describe:

+-- {: .num_prop}
###### Proposition
Let $(\mathcal{C}, J_{at})$ be an atomic site. A presheaf $P\in Set^{\mathcal{C}^{op}}$ is a sheaf for $J_{at}$ iff for any morphism $f:D\to C$ and any $y\in P(D)$ , if $P(g)(y)=P(h)(y)$ for all diagrams
$$
E\overset{g}{\underset{h}{\rightrightarrows}} D\overset{f}{\to} C
$$
with $f\cdot g=f\cdot h$ , then $y=P(f)(x)$ for a unique $x\in P(C)$.
=--

For the proof see Mac Lane-Moerdijk ([1994](#MM94), pp.126f).

## The more general definition

Thus far we have presented the classical approach as presented in Mac Lane-Moerdijk ([1994](#MM94)) going back to Barr-Diaconescu ([1980](#BD80)) but it was observed by [[Olivia Caramello|O. Caramello]] ([2012](#Ca12)) that the atomic topology can in fact be defined on arbitrary categories not only on those satisfying the [[Ore condition]].

+-- {: .num_defn}
###### Definition'

Let $\mathcal{C}$ be a category. The _atomic topology_ $J_{at}$ on $\mathcal{C}$ is the smallest [[Grothendieck topology]] containing all the nonempty sieves. A site of the form $(\mathcal{C}, J_{at})$ is called _atomic_.
=--

Note that $J_{at}$ is well defined as the intersection of all Grothendieck topologies with the property that all nonempty sieves cover. The following proposition justifies the terminology:

+-- {: .num_prop}
###### Proposition
Let $(\mathcal{C}, J_{at})$ be an atomic site. Then $Sh(\mathcal{C}, J_{at})$ is an [[atomic topos|atomic Grothendieck topos]].
=--

+-- {: .proof}
###### Proof
The main idea is to consider the full subcategory $\mathcal{C}'$ on those objects $U$ with $\emptyset\notin J_{at}(U)$ together with the [[dense sub-site|induced topology]] $J'_{at}=J_{at}|_{\mathcal{C}'}$. Then one shows that $\mathcal{C}'$ satisfies the Ore condition and concludes by the [[comparison lemma]] that $Sh(\mathcal{C}', J'_{at})\simeq Sh(\mathcal{C}, J_{at})$. For the details see Caramello ([2012](#Ca12), prop.1.4).
=--

+-- {: .num_example}
###### Example

Consider the category $\mathcal{C}$ on the 'walking co-span' $\bullet\rightarrow \bullet \leftarrow \bullet$. $\mathcal{C}$ is connected but does not satisfy the [[Ore condition]]. Then according to a remark in Caramello ([2012](#Ca12),rem.1.5.) the subcategory $\mathcal{C}'$ is empty and $Sh(\mathcal{C},J_{at})\simeq 1$ is degenerate and, in particular,  $Sh(\mathcal{C},J_{at})$ is not equivalent to $Sh(\mathcal{C},J_d)\simeq Sh_{\neg\neg}(Set^{\bullet\leftarrow\bullet\rightarrow\bullet})$ since the latter is equivalent to the non-atomic topos $Set\times Set$. In particular, the atomic topology on a category will be distinct from the [[dense topology]] in general.

Further details on $Set^{\bullet\leftarrow\bullet\rightarrow\bullet}$, the topos of hypergraphs, may be found at [[hypergraph]].
=--

## Related entries

* [[dense topology]]

* [[atomic topos]]

* [[atomic geometric morphism]]

* [[Ore condition]]

* [[De Morgan topos]]

## Reference

* {#BD80}[[Michael Barr]], [[Radu Diaconescu]], _Atomic Toposes_ ,  JPAA **17** (1980) pp.1-24. ([pdf](http://www.math.mcgill.ca/barr/papers/atom.top.pdf))

* {#Ca12}[[Olivia Caramello]], _Atomic toposes and countable categoricity_ , Appl. Cat. Struc. **20** no. 4 (2012) pp.379-391. ([arXiv:0811.3547](http://arxiv.org/abs/0811.3547))

* {#MM94} [[Saunders Mac Lane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ , Springer Heidelberg 1994. (pp.115, 126)

[[!redirects atomic topology]]