
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Vop&#283;nka\'s principle
* table of contents
{: toc}

## Idea

**Vop&#283;nka's principle** is a [[large cardinal]] axiom which implies a good deal of simplification in the theory of [[locally presentable categories]].  

It is fairly strong as large cardinal axioms go: its consistency follows from the existence of [[huge cardinal]]s, and it implies the existence of arbitrarily large [[measurable cardinal]]s.

## Statements

### The Vop&#283;nka principle

Vop&#283;nka's principle has many equivalent statements.  Here are a few:

+-- {: .num_theorem}
###### Theorem

The VP is equivalent to the statement:

Every [[discrete category|discrete]] [[full subcategory]] of a [[locally presentable category]] is [[small category|small]].

=--

+-- {: .num_theorem}
###### Theorem

The VP is equivalent to the statement:

For every [[proper class]] sequence $\langle M_\alpha | \alpha \in Ord\rangle$ of [[logic|first-order structures]], there is a pair of [[ordinals]] $\alpha\lt\beta$  for which $M_\alpha$ [[elementary embedding|embeds elementarily]] into $M_\beta$.

=--

+-- {: .num_theorem #ColimitsCoreflective}
###### Theorem

The VP is equivalent to the statement:

For $C$ a [[locally presentable category]],  every [[full subcategory]] $D \hookrightarrow C$ which is closed under [[colimit]]s is a [[coreflective subcategory]].

=--

This is ([AdamekRosicky, theorem 6.28](#AdamekRosicky)).


+-- {: .num_theorem}
###### Theorem

The VP is equivalent to the statement:

Every [[cofibrantly generated model category]] (in a slightly more general sense than usual) is a [[combinatorial model category]].

=--

This is in ([Rosicky](#Rosicky))

+-- {: .num_remark}
###### Remark

If one insists on the traditional stricter definition of cofibrant generated model category, then the VP still implies that these are all combinatorial. But the VP is slightly stronger than this statement.

=--

+-- {: .num_theorem}
###### Theorem
The VP is equivalent to both of the statements:

1. For every $n$, there exists a [[C(n)-extendible cardinal]].
1. For every $n$, there exist arbitrarily large [[C(n)-extendible cardinals]].
=--

This is in ([BCMR](#BagariaCasacubertaMathiasRosicky)).


### The weak Vop&#283;nka principle

The Vop&#283;nka principle implies the weak Vop&#283;nka principle.

+-- {: .num_theorem}
###### Theorem

The weak VP is equivalent to the statement:

For $C$ a [[locally presentable category]],  every [[full subcategory]] $D \hookrightarrow C$ which is closed under [[limit]]s is a [[reflective subcategory]].

=--

This is [AdamekRosicky, theorem 6.22 and example 6.23](#AdamekRosicky)


### Relativized versions of Vop&#283;nka's principle

Vop&#283;nka's principle can be relativized to levels of the [[Lévy hierarchy]] by restricting the complexity of the (definable) classes to which it is applied.  The following theorems are from ([BCMR](#BagariaCasacubertaMathiasRosicky)).

+-- {: .num_theorem}
###### Theorem
For any $n\ge 1$, the following statements are equivalent.

1. There exists a [[C(n)-extendible cardinal]].
1. Every proper class of first-order structures that is defined by a conjunction of a $\Sigma_{n+1}$ formula and a $\Pi_{n+1}$ formula contains distinct structures $M$ and $N$ and an [[elementary embedding]] $M\hookrightarrow N$.
=--

The "$n=0$ case" of this is:

+-- {: .num_theorem}
###### Theorem
For any $n\ge 1$, the following statements are equivalent.

1. There exists a [[supercompact cardinal]].
1. Every proper class of first-order structures that is defined by a $\Sigma_2$ formula contains distinct structures $M$ and $N$ and an [[elementary embedding]] $M\hookrightarrow N$.
=--

Many more refined results can be found in ([BCMR](#BagariaCasacubertaMathiasRosicky)).


## Motivation

From a category-theoretic perspective, Vop&#283;nka's principle can be motivated by applications and consequences, but it can also be argued for somewhat *a priori*, on the basis that *large discrete categories* are rather pathological objects.  We can't avoid them entirely (at least, not without restricting the rest of mathematics fairly severely), but maybe at least we can prevent them from occurring in some nice situations, such as full subcategories of locally presentable categories.  See [this MO answer](http://mathoverflow.net/questions/29302/reasons-to-believe-vopenkas-principle-huge-cardinals-are-consistent/29473#29473).


## Consequences {#Consequences}


+-- {: .num_theorem #ConsequenceForBousfieldLoc}
###### Theorem

The VP implies the statement:

Let $C$ be a [[left proper model category|left proper]] [[combinatorial model category]] and $Z \in Mor(C)$ a [[class]] of [[morphism]]s. Then the [[Bousfield localization of model categories|left Bousfield localization]] $L_Z W$ exists.

=--

This is theorem 2.3 in ([RosickyTholen](#RosickyTholen))


+-- {: .num_corollary #ConsequenceForReflectiveInfCatLoc}
###### Corollary

The VP implies the statement:

Let $C$ be a [[locally presentable (∞,1)-category]] and $Z$ a class of morphisms in $C$. Then the reflective [[localization of an (∞,1)-category|localization]] of $C$ at $W$ extsts. 

=--

+-- {: .proof}
###### Proof

By the facts discussed at [[locally presentable (∞,1)-category]] and [[combinatorial model category]] and [[Bousfield localization of model categories]] we have that every locally presentable $(\infty,1)$-category is presented by a combinatorial model category and that under this correspondence reflective localizations correspond to left Bousfield localizations. The claim then follows with the ([above theorem](#ConsequenceForBousfieldLoc)).

=--

## Set-theoretic notes

### First- versus second-order

As usually stated, Vop&#283;nka's principle is not formalizable in first-order [[ZF]] set theory, because it involves a "second-order" [[quantifier|quantification]] over [[proper classes]] ("...there does not exist a large discrete subcategory...").  It can, however, be formalized in this way in a class-set theory such as [[NBG]].

On the other hand, it can be formalized in ZF as a first-order axiom schema consisting of one axiom for each class-defining formula $\phi$, stating that "$\phi$ does not define a class which is a large discrete subcategory..."  We might call this axiom schema the **Vop&#283;nka axiom scheme**.  As in most situations of this sort, the first-order Vop&#283;nka scheme is appreciably weaker than the second-order Vop&#283;nka principle.  See, for instance, [this MO question](http://mathoverflow.net/questions/45602/can-vopenkas-principle-be-violated-definably) and answer.


### Vop&#283;nka cardinals

Unlike some large cardinal axioms, Vop&#283;nka's principle does not appear to be merely an assertion that "there exist very large cardinals" but rather an assertion about the precise size of the "universe" (the "boundary" between sets and proper classes).  In other words, the universe could be "too big" for Vop&#283;nka's principle to hold, in addition to being "too small."

(The equivalence of Vop&#283;nka's principle with the existence of [[C(n)-extendible cardinals]] may appear to contradict this.  However, the property of being $C(n)$-extendible itself "depends on the size of the whole universe" in a sense.)

More precisely, if $\kappa$ is a cardinal such that $V_\kappa$ satisfies ZFC + Vop&#283;nka's principle, then knowing that $\lambda\gt\kappa$ does not necessarily imply that $V_\lambda$ also satifies Vop&#283;nka's principle.  By contrast, if $V_\kappa$ satisfies ZFC + "there exists a [[measurable cardinal]]" (say), then there must be a measurable cardinal less than $\kappa$, and that measurable cardinal will still exist in $V_\lambda$ for any $\lambda\gt\kappa$.  On the other hand, large cardinal axioms such as "there exist arbitrarily large measurable cardinals" have the same property that Vop&#283;nka's principle does: even if measurable cardinals are unbounded below $\kappa$, they will not be unbounded below $\lambda$ if $\lambda$ is the next greatest [[inaccessible cardinal]] after $\kappa$.

Relativizing Vop&#283;nka's principle to cardinals also raises the same first- versus second-order issues as above.  We say that a **Vop&#283;nka cardinal** is one where Vop&#283;nka's principle holds "in $V_\kappa$" where the quantification over classes is interpreted as quantification over all subsets of $V_\kappa$.  By contrast, we could define an **almost-Vop&#283;nka cardinal** to be one where $V_\kappa$ satisfies the first-order Vop&#283;nka scheme.  Then one can show, using the Mahlo reflection principle (see [here](http://mathoverflow.net/questions/45602/can-vopenkas-principle-be-violated-definably/46538#46538) again), that every Vop&#283;nka cardinal $\kappa$  is a limit of $\kappa$-many almost-Vop&#283;nka cardinals, and in particular the smallest almost-Vop&#283;nka cardinal cannot be Vop&#283;nka.  Thus, being Vop&#283;nka is much stronger than being almost-Vop&#283;nka.

### Definable counterexamples

If Vop&#283;nka's principle fails, then there exist counterexamples to all of its equivalent statements, such as a large discrete full subcategory of a locally presentable category.  If Vop&#283;nka's principle fails but the first-order Vop&#283;nka scheme holds, then no such counterexamples can be explicitly definable.

On the other hand, if the Vop&#283;nka scheme also fails, then there will be explicit finite formulas one can write down which define counterexamples.  However, there is no "universal" counterexample, in the following sense: if Vop&#283;nka's principle is consistent, then for any class-defining formula $\phi$, there is a model of set theory in which Vop&#283;nka's principle fails (and even in which the first-order Vop&#283;nka scheme fails), but in which $\phi$ does not define a counterexample to it.  See [here](http://mathoverflow.net/questions/45602/can-vopenkas-principle-be-violated-definably/46538#46538) yet again.


## References

The relation to the theory of [[locally presentable categories]] is the contents of chapter 6 of

* [[Jiří Adámek]], [[Jiří Rosický]], _[[Locally presentable and accessible categories]]_,  London Mathematical Society Lecture Note Series 189
{#AdamekRosicky}

The relation to [[combinatorial model categories]] is discussed in

* [[Jiří Rosický]], _Are all cofibrantly generated model categories combinatorial?_ ([ps](http://www.math.muni.cz/~rosicky/papers/cof1.ps))
{#Rosicky}

The implication of VP on [[homotopy theory]], [[model categories]] and [[cohomology localization]] are discussed in the following articles

* [[Jiří Rosický]], [[Walter Tholen]], _Left-determined model categories and universal homotopy theories_  Transactions of the American Mathematical Society
Vol. 355, No. 9 (Sep., 2003), pp. 3611-3623 ([JSTOR](http://www.jstor.org/stable/1194855)).
{#RosickyTholen}

* [[Carles Casacuberta]], Dirk Scevenels, [[Jeff Smith]], _Implications of large-cardinal principles in homotopical localization_  Advances in Mathematics
Volume 197, Issue 1, 20 October 2005, Pages 120-139 

* Joan Bagaria, [[Carles Casacuberta]], Adrian Mathias, [[Jiří Rosicky]] _Definable orthogonality classes in accessible categories are small_, [arXiv](http://arxiv.org/abs/1101.2792)
{#BagariaCasacubertaMathiasRosicky}

* Giulio Lo Monaco, _Vopěnka's principle in ∞-categories_, [arxiv:2105.04251](https://arxiv.org/abs/2105.04251)

category: foundational axiom

[[!redirects Vopěnka's principle]]
[[!redirects Vopenka's principle]]
[[!redirects Vopěnka's principle]]
[[!redirects Vopenka's principle]]
[[!redirects Vopěnka s principle]]
[[!redirects Vopenka s principle]]
[[!redirects Vopěnka principle]]

[[!redirects Vopěnka's axiom]]
[[!redirects Vopenka's axiom]]
[[!redirects Vopěnka's axiom]]
[[!redirects Vopenka's axiom]]
[[!redirects Vopěnka s axiom]]
[[!redirects Vopenka s axiom]]
[[!redirects Vopěnka's axiom scheme]]
[[!redirects Vopenka's axiom scheme]]
[[!redirects Vopěnka's axiom scheme]]
[[!redirects Vopenka's axiom scheme]]
[[!redirects Vopěnka s axiom scheme]]
[[!redirects Vopenka s axiom scheme]]
[[!redirects Vopěnka's axiom schema]]
[[!redirects Vopenka's axiom schema]]
[[!redirects Vopěnka's axiom schema]]
[[!redirects Vopenka's axiom schema]]
[[!redirects Vopěnka s axiom schema]]
[[!redirects Vopenka s axiom schema]]

[[!redirects Vopěnka cardinal]]
[[!redirects Vopěnka cardinals]]
[[!redirects Vopenka cardinal]]
[[!redirects Vopenka cardinals]]
