
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--

# Extensional relations
* table of contents
{: toc}

## Idea

Given an extensional relation $\prec$ on a set, two elements are equal if they cannot be distinguished by the structure of the set of elements that they are related to, that those elements are related to, and so on forever in one direction.  We generally think of $x \prec y$ as saying that $x$ is a 'member' of $y$, so that $\prec$ is extensional when "$x$ is determined by its members" as in the [[axiom of extensionality]] for material [[set theory]].


## Definitions

We begin with the historically first definition, which is correct for [[well-founded relations]].  We then consider ways to extend this to more general relations, where the last version seems to be most correct.


### Weak extensionality

A relation $\prec$ on a set $S$ is __weakly extensional__ if, given any elements $x$ and $y$ of $S$, $x = y$ whenever (for all $t$) $t \prec x$ if and only if $t \prec y$.

Interpreting $\prec$ as membership $\in$, this corresponds to the [[axiom of extensionality]] as usually stated for [[pure sets]]. However, it is really only appropriate when $\prec$ is [[well-founded relation|well-founded]], just as the usual axiom of extensionality must be strengthened in the absence of the [[axiom of foundation]].

However, when $\prec$ is well-founded, weak extensionality is equivalent to all the stronger notions below; thus in that case it is usually called just **extensionality**.


### Finsler extensionality

Let $\prec^*$ be the reflexive-[[transitive closure]] of the relation $\prec$ on $S$ (so $\prec^*$ is a [[preorder]]).  Given an element $y$ of $S$, let $S \downarrow^* y$ be the [[downset]] of $y$ under $\prec^*$:
$$ S \downarrow^* y = \{ x: S \;|\; x = t_0 \prec \cdots \prec t_n = y \} $$
with $n \geq 0$.  Note that $y$ itself belongs to $S \downarrow^* y$ (through $n = 0$, if in no other way), so we may take it to be a [[pointed set]].  Then $\prec$ is __Finsler-extensional__ if it is weakly extensional and, given any elements $x$ and $y$ of $S$, $x = y$ whenever $S \downarrow^* x$ and $S \downarrow^* y$ are isomorphic as pointed sets equipped with a relation $\prec$.

Note that this definition includes weak extensionality, which won\'t follow from the other half unless $\prec$ is well-founded (see the examples below).  It is possible to get weak extensionality free by using the [[transitive closure]] $\prec^+$ instead; that is, define $S \downarrow^+ y$ with $n \gt 0$ only.  But then you need another step; define $(S \downarrow^+ y)^\top$ to be a pointed set with a new point $\top$ adjoined to $S \downarrow^+ y$; let $x \prec \top$ if and only if $x \prec y$ in $S$ itself.  (For a well-founded relation, $(S \downarrow^+ y)^\top \cong S \downarrow^* y$; in general, however, $y$ may already belong to $S \downarrow^+ y$, yet $y \ne \top$ in $(S \downarrow^+ y)^\top$.)  Then $\prec$ is Finsler-extensional on $S$ if and only if $x = y$ whenever $(S \downarrow^+ x)^\top \cong (S \downarrow^+ y)^\top$ as pointed sets equipped with $\prec$.

It is immediate that Finsler extensionality implies weak extensionality; the converse may be proved (using [[induction]]) for well-founded relations.


### Scott extensionality

Given an element $y$ of $S$, let a __path__ to $y$ consist of a sequence
$$ x = t_0 \prec \cdots \prec t_n = y $$
for $n \geq 0$.  Then let $T_y$ be the set of paths to $y$; given paths $\vec{t}$ and $\vec{u}$ in $N_y$, say that $\vec{t} \to \vec{u}$ if $\vec{u} = (t_1, \ldots, t_m)$ for some $m \leq n$.  Then $T_y$ with the relation $\to$ is the __tree__ to $y$.

$S$ is __Scott-extensional__ if the only [[automorphism]] of any such tree $T_y$ (as a set equipped with a relation $\to$) is the [[identity function]] on $T_y$.

Then Scott extensionality implies Finsler extensionality, and the converse holds for well-founded relations.


### Strong extensionality

The strongest version of extensionality is motivated by the study of [[terminal coalgebra]]s and [[coinduction]].

Let $S$ be equipped with a binary relation $\prec$.  A __[[bisimulation]]__ on $(S,\prec)$ is a binary relation $\sim$ such that whenever $x \sim y$, for any $a \prec x$ there is a $b \prec y$ with $a \sim b$, and conversely for every $b \prec y$ there is an $a \prec x$ with again $a \sim b$.  We then say that $\prec$ is __strongly extensional__ if every bisimulation is contained in the identity relation; i.e., $x = y$ whenever $x \sim y$ for any bisimulation $\sim$.  In general, this is probably the best situation in which to say that $\prec$ is simply __extensional__.

Finsler and Scott extensionality may be understood as special cases of this for particular bisimulations $\sim$.  (So can strong extensionality, since any set equipped with a relation has a weakest bisimulation $\approx$.)  This is the approach taken by Aczel to study all the above notions of extensionality together.

In particular, strong extensionality implies Scott extensionality, and the converse holds for well-founded relations.  Thus, all forms of extensionality are equivalent for well-founded relations.

### In homotopy type theory

In [[homotopy type theory]], a relation is an [[h-proposition]]-valued [[type family]]. A binary relation $\prec$ on a carrier type $S$ is **weakly extensional** if for all terms $a:S$ and $b:S$ the canonical function

$$\mathrm{idtoextcond}(a, b):(a =_S b) \to \prod_{c:S} (c \prec a) \simeq (c \prec b)$$

is an [[equivalence of types]]. This implies that the type $S$ is an [[h-set]]. 

## Examples

*  The [[axiom of extensionality]] in material [[set theory]] states membership is an extensional relation on the class of [[pure sets]].  (Note that the [[axiom of foundation]] states that membership is a well-founded relation, so one usually doesn\'t worry about the different notions of extensionality for ill-founded relations.)  More generally, the membership relation on the [[transitive closure]] or reflexive-transitive closure of a pure set is an extensional relation on a set.

*  Conversely, one can *define* [[pure set]]s in *structural* [[set theory]] in part as sets equipped with an extensional (and optionally well-founded) relation.

* In any [[single-sorted definition of a category|single-sorted definition]] of a [[topos]], there is a [[terminal object]] $1$ (represented by the [[identity morphism]] of the terminal object), one could define the relation $\prec$ on the set of morphisms $C$ as 

$$a \prec b \coloneqq s(a) = 1 \wedge t(b) = 1 \wedge t(a) = s(b)$$

Due to the [[universal property]] of the [[terminal object]], $\prec$ is weakly extensional. However, $\prec$ is not strongly extensional. The relation $\sim$ defined by equality on every pair of functions $a \sim b \coloneqq a = b$, and in addition, $\mathrm{id}_2 \sim \mathrm{swap}$ and $\mathrm{swap} \sim \mathrm{id}_2$ for the identity function and the swap function on the set with two elements $2$, is a bisimulation on $\prec$, but it is not true that $\mathrm{id}_2 = \mathrm{swap}$.

*  A [[well-order]] is precisely a well-founded, [[transitive relation|transitive]], extensional relation.  Removing well-foundedness here gives a theory of ill-founded [[ordinal number]]s.

*  On the set $\mathbf{2} = \{0,1\}$, now let $0 \prec 0$ and $0 \prec 1$ (but no other relationships).  This relation is not weakly extensional, although it does satisfy the other half of Finsler extensionality, since $\mathbf{2} \downarrow^* 0 \ncong \mathbf{2} \downarrow^* 1$.  However, $(\mathbf{2} \downarrow^+ 0)^\top \cong (\mathbf{2} \downarrow^+ 1)^\top$; this shows the necessity of defining Finsler extensionality as we do.

*  On the set $\mathbf{2}$ again, let $0 \prec 1$ and $1 \prec 0$ (but $0 \nprec 0$ and $1 \nprec 1$).  This relation is weakly extensional but not Finsler-extensional, since $\mathbf{2} \downarrow^* 0 \cong \mathbf{2} \downarrow^* 1$.  Yet $0$ and $1$ can hardly be distinguished by $\prec$ when there is an [[automorphism]] of $(\mathbf{2},\prec)$ that swaps them; this and the other examples below motivate the stronger notions of extensionality.

*  On the set $\mathbf{3} = \{0,1,2\}$, let $2 \nprec 0$ and $i \nprec i$ but all other relationships hold.  Then this relation is Finsler-extensional but not Scott-extensional, since $T_2 \cong T_1$.

*  Finally, on the set $\mathbf{2}$ again, let $1 \nprec 0$ but all other relationships hold.  Then this relation is Scott-extensional but not strongly extensional, since $0 \approx 1$.


## Extensional quotients

Weak extensionality is a kind of [[antisymmetric relation|antisymmetry]] condition: Let $x \leq y$ mean that $t \prec y$ whenever $t \prec x$.  Then $\leq$ is clearly a [[preorder]], which is antisymmetric (so a [[partial order]]) if and only if $\prec$ is weakly extensional.

Now suppose that if $t \prec x$ if and only if $t \prec y$ for all $t$, then $x \prec z$ if and only if $y \prec z$ for all $z$.  Then if we define $x \equiv y$ to mean that $x \leq y$ and $y \leq x$, then $\equiv$ is an equivalence relation such that $\prec$ descends to a weakly extensional relation on the [[quotient set]] $S/{\equiv}$.

Strongly extensional quotients are even easier to construct, although they do create additional relationships.  It is easy to see that the union of any family of bisimulations is a bisimulation, and therefore there is a largest bisimulation $\approx$ for any binary relation $\prec$ on $S$.  Moreover, $\approx$ is an equivalence relation (though not every bisimulation need be so), and $\prec$ descends to a strongly extensional relation on the quotient $S/\approx$.


## Simulations

Given two sets $S$ and $T$, each equipped with a strongly extensional relation $\prec$, a [[function]] $f\colon S \to T$ is a __[[simulation]]__ of $S$ in $T$ if

*  $f(x) \prec f(y)$ whenever $x \prec y$ and
*  given $t \prec f(x)$, there exists $y \prec x$ with $t = f(y)$.

Then sets so equipped form a [[category]] with simulations as [[morphism]]s.

Note that there is at most one simulation from $S$ to $T$; in fact, strong extensionality for $T$ is equivalent to saying that any two simulations $S \rightrightarrows T$ are equal.  Also, any simulation from $S$ to $T$ must be an [[injection]]; in fact, strong extensionality for $S$ is equivalent to saying that any simulation $S \to T$ is injective.

Thus, we have a (large) [[poset]] of sets equipped with extensional relations, and we can consistently interpret the simulations as [[subset]] inclusion.  This leads to the model of sets equipped with extensional relations as [[transitive set]]s.


## References

*  Peter Aczel; [Non-Well-Founded Sets](https://web.archive.org/web/20161020002632/https://standish.stanford.edu/pdf/00000056.pdf), especially Chapter 4.

For extensional relations in [[homotopy type theory]], see

* [[Håkon Robbestad Gylterud]], [[Elisabeth Bonnevier]], *Non-wellfounded sets in HoTT* ([arXiv:2001.06696](https://arxiv.org/abs/2001.06696))

[[!redirects extensional relation]]
[[!redirects extensional relations]]

[[!redirects extensional quotient]]
[[!redirects extensional quotients]]

[[!redirects weak extensionality]]
[[!redirects Finsler extensionality]]
[[!redirects Scott extensionality]]
[[!redirects strong extensionality]]
