
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--

# Contents
* table of contents 
{: toc}

## Idea

A (binary) [[relation]] $\prec$ on a [[set]] $S$ is called _well-founded_ if it is valid to do [[induction]] on $\prec$ over $S$.


## Definition

Given a [[subset]] $A$ of $S$, suppose that $A$ has the property that, given any element $x$ of $S$, if
$$ \forall (t\colon S),\; t \prec x \Rightarrow t \in A ,$$
then $x \in A$.  Such an $A$ may be called a _$\prec$-inductive subset_ of $S$.  The relation $\prec$ is __well-founded__ if the only $\prec$-inductive subset of $S$ is $S$ itself.

Note that this is precisely what is necessary to validate induction over $\prec$: if we can show that a statement is true of $x\in S$ whenever it is true of everything $\prec$-below $x$, then it must be true of everything in $S$.  In the presence of [[excluded middle]] it is equivalent to other commonly stated definitions; see _Formulations in classical logic_ below.


### Formulations in classical logic

While the definition above follows how a well-founded relation is generally *used* (namely, to prove properties of elements of $S$ by induction), it is complicated.  Two alternative formulations are given by the following:

1. The relation $\prec$ has __no infinite descent__ (usually attributed to [[Pierre de Fermat]]) if there exists no [[sequence]] $\cdots \prec x_2 \prec x_1 \prec x_0$ in $S$.  (Such a sequence is called an _infinite descending sequence_.)

2. The relation $\prec$ is __classically well-founded__ if every [[inhabited set|inhabited]] subset $A$ of $S$ has a member $x \in A$ such that no $t \in A$ satisfies $t \prec x$.  (Such an $x$ is called a _minimal_ element of $A$.)

In [[classical mathematics]], both of these conditions are equivalent to being well-founded.  In constructive mathematics, we may prove that a well-founded relation has no infinite descent (see Proposition \ref{empty}), but not the converse, and that a classically well-founded relation is well-founded (see Proposition \ref{classical}), but not the converse.  

+-- {: .num_remark #LEM} 
###### Remark 
We note that classical well-foundedness is really too strong for constructive (i.e., intuitionistic) mathematics: if there exists an [[inhabited subset|inhabited]] relation that is classically well-founded, then [[excluded middle]] follows. (This holds true in any [[topos]]; for a proof, see [here](http://ncatlab.org/toddtrimble/published/classical+well-foundedness).) On the other hand, the infinite descent condition is too weak to be of much use in constructive mathematics. It is the inductive notion of well-foundedness that is just right. 
=-- 

Note however that in [[predicative mathematics]], the definition of well-founded may be impossible to even state, and so either of these alternative definitions would be preferable, provided classical logic is used.

Even in constructive predicative mathematics, (1) is strong enough to establish the [[Burali-Forti paradox]] (when applied to [[linear orders]]).  In [[material set theory]], (2) is traditionally used to state the [[axiom of foundation]], although the impredicative definition could also be used as an axiom scheme (and must be in constructive versions).  In any case, either (1) or (2) is usually preferred by classical mathematicians as simpler. 

To round out the discussion we prove the following two results, both valid in intuitionistic mathematics: 

+-- {: .num_prop #empty} 
###### Proposition 
If $(X, \prec)$ is a well-founded relation and $A \subseteq X$ has no minimal element, then $A$ is empty. 
=-- 

This result makes it trivial to infer (under classical logic) that classical well-foundedness is a consequence of well-foundedness. It also shows that well-foundedness rules out infinite descent (intuitionistically), since an infinite descent sequence has no minimal element. 

+-- {: .proof} 
###### Proof 
Let $U = \{u \in X: u \notin A\; \wedge \; (\forall x: X),\; x \prec u \Rightarrow x \notin A\}$. Clearly $U \cap A = \emptyset$. We show $U$ is inductive, so that under well-foundedness $U = X$ and $A = X \cap A = U \cap A = \emptyset$, as desired. 

So, suppose $z$ is an element such that $y \in U$ whenever $y \prec z$. We must show $z \in U$. Claim: $z \notin A$. For if $z \in A$, then $z$ would be a minimal element of $A$ (as $y \prec z \Rightarrow y \in U \Rightarrow y \notin A$). But this negates the assumption that $A$ has no minimal element. 

Thus $z \notin A$, and $y \prec z \Rightarrow y \in U \Rightarrow y \notin A$, so that $z \in U$. This completes the proof. 
=-- 

+-- {: .num_prop #classical} 
###### Proposition 
In intuitionistic set theory, classical well-foundedness implies (inductive) well-foundedness. 
=-- 

+-- {: .proof} 
###### Proof 
Let $\prec$ be a classically well-founded relation on $X$, and let $U$ be an inductive subset. We must show that every element $x \in X$ belongs to $U$. Since $U$ is inductive, it suffices to show that every $u \prec x$ belongs to $U$, i.e. we may assume given a $u$ such that $u\prec x$ and show $u\in U$. But under this assumption we have that $\prec$ is inhabited, so according to Remark \ref{LEM}, the law of [[excluded middle]] follows and we might as well then argue classically. The argument is well-known but we include it for completeness: under classical well-foundedness, if an inductive subset $U$ is not the entirety of $X$, then the complement $\neg U$ has a minimal element $y$. In that case, $v \prec y$ implies $v \in \neg\neg U = U$, but then $y \in U$ since $U$ is inductive, contradiction. Hence $U = X$ and in particular $u \in U$, which is what we wanted. 
=-- 

### Coalgebraic formulation 

Many inductive or recursive notions may also be packaged in [[coalgebra|coalgebraic]] terms. For the concept of well-founded relation, first observe that a binary relation $\prec$ on a set $X$ is the same as a coalgebra structure $\theta\colon X \to P(X)$ for the covariant [[power-set]] endofunctor on $Set$, where $y \prec x$ if and only if $y \in \theta(x)$. 

In this language, a [[subset]] $i\colon U \hookrightarrow X$ is $\prec$-inductive, or $\theta$-inductive, if in the [[pullback]]

$$\array{
H & \stackrel{j}{\to} & X \\ 
\downarrow & & \downarrow^\mathrlap{\theta} \\
P U & \underset{P i}{\to} & P X
}$$ 

the map $j$ factors through $i$. (Note that $j$ is necessarily [[monomorphism|monic]], since $P$ preserves monos.) Unpacking this a bit: for any $x \in X$, if $\theta(x) = V$ belongs to $P U$, that is if $\theta(x) \subseteq U$, then $x \in U$. This says the same thing as $\forall_{x\colon X} (\forall_{y\colon X} y \prec x \Rightarrow y \in U) \Rightarrow x \in U$. 

Then, as usual, the $P$-coalgebra $(X, \theta)$ is well-founded if every $\theta$-inductive subset $U \hookrightarrow X$ is all of $X$. 

Other relevant notions may also be packaged; for example, the $P$-coalgebra $X$ is [[extensional relation|extensional]] if $\theta\colon X \to P X$ is monic. See also [[well-founded coalgebra]]. 


### Simulations

Given two sets $S$ and $T$, each equipped with a well-founded relation $\prec$, a [[function]] $f\colon S \to T$ is a __[[simulation]]__ of $S$ in $T$ if
1.  $f(x) \prec f(y)$ whenever $x \prec y$ and
2.  given $t \prec f(x)$, there exists $y \prec x$ with $t = f(y)$.

Then sets so equipped form a [[category]] with simulations as [[morphisms]].  See [[extensional relation]] for more uses of simulations.

In coalgebraic language, a simulation $S \to T$ is simply a $P$-coalgebra homomorphism $f\colon S \to T$. Condition (1), that $f$ is merely $\prec$-preserving, translates to the condition that $f$ is a [[colax morphism]] of coalgebras, in the sense that there is an inclusion 

$$\array{
X & \stackrel{\theta_X}{\to} & P X \\
 ^\mathllap{f} \downarrow & \swArrow & \downarrow^\mathrlap{P f} \\
Y & \underset{\theta_Y}{\to} & P Y.
}$$ 


## Properties

Every well-founded relation is [[irreflexive relation|irreflexive]]; that is, $x \nprec x$.  Sometimes one wants a reflexive version $\preceq$ of a well-founded relation; let $x \preceq y$ if and only $x \prec y$ or $x = y$.  Then the requirement that $x$ be a minimal element of a subset $A$ states that $t \preceq x$ only if $t = x$.  But infinite descent or direct proof by induction still require $\prec$ rather than $\preceq$.

A [[well-order|well order]] may be defined as a well-founded [[linear order]], or alternatively as a [[transitive relation|transitive]], [[extensional relation|extensional]], well-founded relation. 

A [[well-quasi-order]] is a well-founded [[preorder]] (referring to the reflexive version of well-foundedness above) that in addition has no infinite [[antichain|antichains]]. 

The [[axiom of foundation]] in material [[set theory]] states precisely that the membership relation $\in$ on the proper class of all [[pure sets]] is well-founded.  In structural set theory, accordingly, one uses well-founded relations in building structural models of well-founded pure sets.


## Examples

Let $S$ be a [[finite set]].  Then any relation on $S$ whose [[transitive closure]] is irreflexive is well-founded.

Let $S$ be the set of [[natural numbers]], and let $x \prec y$ if $y$ is the [[successor]] of $x$: $y = x + 1$.  That this relation is well-founded is the usual principle of _mathematical induction_.

Again let $S$ be the set of natural numbers, but now let $x \prec y$ if $x \lt y$ in the usual order.  That this relation is well-founded is the principle of _strong induction_.

More generally, let $S$ be a set of [[ordinal numbers]] (or even the proper class of all ordinal numbers), and let $x \prec y$ if $x \lt y$ in the usual order.  That this relation is well-founded is the principle of _transfinite induction_.

Similarly, let $S$ be a set of [[pure sets]] (or even the proper class of all pure sets), and let $x \prec y$ if $x \in y$.  That this relation is well-founded is the _[[axiom of foundation]]_.

Let $S$ be the set of [[integers]], and let $x \prec y$ mean that $x$ properly divides $y$: $y/x$ is an integer other than $\pm{1}$.  This relation is also well-founded, so one can prove properties of integers by induction on their proper divisors.


[[!redirects well-founded relation]]
[[!redirects well-founded relations]]
[[!redirects well founded relation]]
[[!redirects well founded relations]]

[[!redirects classically well-founded relation]]
[[!redirects classically well-founded relations]]
[[!redirects classically well founded relation]]
[[!redirects classically well founded relations]]

[[!redirects relation without infinite descent]]
[[!redirects relations without infinite descent]]
[[!redirects relation with no infinite descent]]
[[!redirects relations with no infinite descent]]
[[!redirects Fermat's method of infinite descent]]
[[!redirects Fermat\'s method of infinite descent]]
[[!redirects Fermat's method of infinite descent]]
[[!redirects Fermat method of infinite descent]]
[[!redirects method of infinite descent]]
[[!redirects infinite descent]]
