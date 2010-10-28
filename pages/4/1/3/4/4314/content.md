
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Foundations
+--{: .hide}
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

### Vop&#283;nka cardinals

Unlike some large cardinal axioms, Vop&#283;nka's principle is not merely an assertion that "there exist very large cardinals" but rather an assertion about the precise size of the "universe" (the "boundary" between sets and proper classes).  In other words, the universe could be "too big" for Vop&#283;nka's principle to hold, in addition to being "too small."

More precisely, if $\kappa$ is a cardinal such that $V_\kappa$ satisfies ZFC + Vop&#283;nka's principle (we may call such a $\kappa$ a **Vop&#283;nka cardinal**), then knowing that $\lambda\gt\kappa$ does not necessarily imply that $V_\lambda$ also satifies Vop&#283;nka's principle.  By contrast, if $V_\kappa$ satisfies ZFC + "there exists a [[measurable cardinal]]" (say), then there must be a measurable cardinal less than $\kappa$, and that measurable cardinal will still exist in $V_\lambda$ for any $\lambda\gt\kappa$.  On the other hand, large cardinal axioms such as "there exist arbitrarily large measurable cardinals" have the same property that Vop&#283;nka's principle does: even if measurable cardinals are unbounded below $\kappa$, they will not be unbounded below $\lambda$ if $\lambda$ is the next greatest [[inaccessible cardinal]] after $\kappa$.


### Category-theoretic motivation

From a category-theoretic perspective, Vop&#283;nka's principle can be motivated by applications and consequences, but it can also be argued for somewhat *a priori*, on the basis that *large discrete categories* are rather pathological objects.  We can't avoid them entirely (at least, not without restricting the rest of mathematics fairly severely), but maybe at least we can prevent them from occurring in some nice situations, such as full subcategories of locally presentable categories.  See [this MO answer](http://mathoverflow.net/questions/29302/reasons-to-believe-vopenkas-principle-huge-cardinals-are-consistent/29473#29473).




## Statements

### The Vop&#283;nka principle

Vop&#283;nka's principle has many equivalent statements.  Here are a few:

+-- {: .un_theorem}
###### Theorem

The VP is equivalent to the statement:

Every [[discrete category|discrete]] [[full subcategory]] of a [[locally presentable category]] is [[small category|small]].

=--

+-- {: .un_theorem}
###### Theorem

The VP is equivalent to the statement:

For every [[proper class]] sequence $\langle M_\alpha | \alpha \in Ord\rangle$ of [[logic|first-order structures]], there is a pair of [[ordinals]] $\alpha\lt\beta$  for which $M_\alpha$ [[elementary embedding|embeds elementarily]] into $M_\beta$.

=--

+-- {: .un_theorem}
###### Theorem

The VP is equivalent to the statement:

For $C$ a [[locally presentable category]],  every [[full subcategory]] $D \hookrightarrow C$ which is closed under [[colimit]]s is a [[coreflective subcategory]].

=--

This is ([AdamekRosicky, theorem 6.28](#AdamekRosicky)).



### The weak Vop&#283;nka principle

The Vop&#283;nka principle implies the weak Vop&#283;nka principle

+-- {: .un_theorem}
###### Theorem

The weak VP is equivalent to the statement:

For $C$ a [[locally presentable category]],  every [[full subcategory]] $D \hookrightarrow C$ which is closed under [[limit]]s is a [[reflective subcategory]].

=--

This is [AdamekRosicky, theorem 6.28](#AdamekRosicky)



## Consequences

+-- {: .un_theorem}
###### Theorem

The VP implies the statement:

Every [[cofibrantly generated model category]] is [[Quillen equivalence|Quillen equivalent]] to a [[combinatorial model category]].

=--

This is proven in ([Rosicky](#Rosicky)).


## References

The relation to the theory of [[locally presentable categories]] is the contents of chapter 6 of

* [[Jiri Adamek]], [[Jiří Rosický]], _Locally presentable and accessible categories_ London Mathematical Society Lecture Note Series 189
{#AdamekRosicky}

The relation to [[combinatorial model categories]] is discussed in

* [[Jiří Rosický]], _Are all cofibrantly generated model categories combinatorial?_ ([ps](http://www.math.muni.cz/~rosicky/papers/cof1.ps))
{#Rosicky}

category: foundational axiom

[[!redirects Vopěnka's principle]]
[[!redirects Vopenka's principle]]
[[!redirects Vopěnka's principle]]
[[!redirects Vopenka's principle]]
[[!redirects Vopěnka cardinal]]
[[!redirects Vopěnka cardinals]]
[[!redirects Vopenka cardinal]]
[[!redirects Vopenka cardinals]]
