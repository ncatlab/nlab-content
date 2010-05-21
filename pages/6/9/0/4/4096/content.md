{:myproof: .proof style="margin-left:2em;margin-right:1em;background:#fef;-moz-border-radius:10px;padding:1ex;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;-moz-border-radius:10px;background:#ffe;"}
{:mynumprop: .num_prop style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;-moz-border-radius:10px;background:#eff;"}

<div class="rightHandSide toc">
[[!include functional analysis - contents]]
</div>

#Contents#
* autoamtic table of contents goes here
{:toc}

## Idea

A **DF space** is a type of [[locally convex topological vector space]].  The basic idea is that a DF space is _morally_ the [[strong dual]] of a [[Fréchet space]].  That is, it has all the nice structure that such a dual would have but without the bother of actually having to be a dual space.

## Definition

+-- {: mynumdef #DFspace}
###### Definition
A [[locally convex topological vector space]] is a **DF space** if it possesses a [[fundamental system|fundamental sequence]] of [[subsets of lctvs|bounded sets]] and if every [[subsets of lctvs|strongly bounded]] countable union of [[subsets of lctvs|equicontinuous]] subsets of the dual is again equicontinuous.
=--

## Properties

1. The [[strong dual]] of a [[Fréchet space|metrisable]] locally convex topological vector space is a DF space.
2. Every [[normable space]] is a DF space.
3. Every [[infrabarrelled space]] that has a [[fundamental system|fundamental sequence]] of [[subsets of lctvs|bounded sets]] is a DF space.
4. In particular, every [[LB space]] is a DF space, since any bounded set in an LB space is contained in one of the factors.

+-- {: mynumprop #MetDF}
###### Proposition
A locally convex topological vector space that is [[Fréchet space|metrisable]] and is a DF space is [[normable space|normable]].
=--

+-- {: myproof}
###### Proof
Let $E$ be a metrisable DF space.

To prove the result, we shall use a proposition recorded in [[functional analysis bibliography|Schaefer (IV.6.7)]].  That says that a [[subsets of lctvs|convex]], [[subsets of lctvs|circled]] subset $V$ of $E$ is a [[neighbourhood]] of $0$ if (and only if) for every [[subsets of lctvs|convex]], [[subsets of lctvs|circled]] [[subsets of lctvs|bounded]] subset $B \subseteq E$, $B \cap V$ is a $0$-neighbourhood in $B$.

As $E$ is metrisable, it has a countable $0$-neighbourhood base, say $(V_n)$.  As $E$ is a DF space, it has a countable fundamental family of bounded sets, say $(B_n)$.  Let us assume, without loss of generality, that this family is increasing.

For each $k \in \mathbb{N}$, as $B_k$ is bounded, there is some $\lambda_k \gt 0$ such that $B_k \subseteq \lambda_k V_k$.  Since, by assumption, the $B_k$ are an increasing family, we have $B_k \subseteq \lambda_l V_l$ for all $l \ge k$.  Let $B \coloneqq \bigcap \lambda_k V_k$.  This is a bounded set since it is contained in $\lambda_k V_k$ for each $k$.  Let $l \in \mathbb{N}$ and consider $B_l \cap B$.  We can write this as

$$
B_l \cap \big(\bigcap_{k=1}^{l-1} \lambda_k V_k\big) \cap B_l \cap \big( \bigcap_{k \ge l} \lambda_k V_k \big).
$$

Since $B_l \subseteq \lambda_k V_k$ for $k \ge l$, the last part is unnecessary and so we see that

$$
B_l \cap B = B_l \cap \big(\bigcap_{k=1}^{l-1} \lambda_k V_k \big).
$$

This is then a finite intersection of open sets in $B_l$ and so is open in $B_l$.

As this holds for any of the $B_l$s, it holds for any bounded set, whence the proposition from Schaefer applies to show that $B$ is a $0$-neighbourhood.  Thus $E$ possesses a bounded $0$-neighbourhood, whence is normable.
=--

## References

See [[functional analysis bibliography]].