[[!redirects empty 158]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
#### Foundations
+--{: .hide}
[[!include higher algebra - contents]]
[[!include foundations - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

[[!redirects diagonizable algebra]]
[[!redirects Magari Algebra]]
[[!redirects Magari algebras]]

## Idea

A  _diagonizable_ or **Magari algebra** is a [[Boolean algebra]] together with a modal operator internalizing the diagonalization properties involved in [[incompleteness theorem|Gödel's second incompleteness theorem]].

## Definition
A _Magari algebra_ is a pair $(M,\diamond)$ where $M$ is a [[Boolean algebra]] and $\diamond:M\to M$ is an operator satisfying:

1. $\diamond\bot=\bot$ and $\diamond (x\vee y) =\diamond x\vee \diamond x$ .

2. $\diamond x=\diamond (x\wedge \neg\diamond x)$.

### Remark

Suppose that $T$ is a 'G&#246;delian' theory containing enough arithmetics in order to admit a formula $\mathsf{Cons}$ internalizing consistency. $\mathsf{Cons}$ induces an operator $\diamond_T$ on the [[Lindenbaum-Tarski algebra]] of provable equivalence classes of formulas of $T$ by $[\varphi]\to [\mathsf{Cons}(T+\varphi)]$.

Then the condition M2 for $\diamond_T$ can be viewed as expressing the non-provability of the consistency of the theory $T'=T+\varphi$ since $\mathsf{Cons}(T')$ says that $T'$ is consistent whereas $\mathsf{Cons}(T'+\neg\mathsf{Cons}(T'))$ says that $T'+\neg\mathsf{Cons}(T')$ is consistent i.e. not $T'\vdash\mathsf{Cons}(T')$ (For more details see [Beklemishev-Gabelaia 2012](#BG12)).

## Properties

From M1 it follows that $\diamond$ is monotone: $x\leq y$ implies $\diamond x\leq \diamond y$.

Moreover, $\diamond$ satisfies the following **transitivity property**:
$$\diamond\diamond x\leq\diamond x\quad ,\forall x\in M.$$

To see this, consider $\diamond\diamond x\leq\diamond\diamond x\vee\diamond x=\diamond (x\vee \diamond x)$ where the last equation follows from the commutativity of $\vee$ together with M1.

Set $y=x\vee\diamond x$ whence sofar we have got : $\diamond\diamond x\leq\diamond y$. Now we want to show that $\diamond y\leq\diamond x$:

From M2 plus the definition of $y$: $\diamond y=\diamond(y\wedge\neg\diamond y)=\diamond((x\vee\diamond x)\wedge \neg\diamond y)=\diamond((x\wedge\neg\diamond y)\vee(\diamond x\wedge\neg\diamond y))$. But $\diamond x\wedge\neg\diamond y=\bot$ since the expanded left side is a $\wedge$ containing a factor $\diamond x\wedge\neg\diamond x$. Whence $\diamond((x\wedge\neg\diamond y)\vee(\diamond x\wedge\neg\diamond y))=\diamond((x\wedge\neg\diamond y)\vee\bot)=\diamond(x\wedge\neg\diamond y)$ but $\diamond(x\wedge\neg\diamond y)\leq\diamond x$ since $x\wedge\neg\diamond y\leq x$ and $\diamond$ is monotone. Whence all in all we get $\diamond y\leq\diamond x$ and we are done.

## Examples

* Let $X$ be a [[topological space]] and $d:2^X\to 2^X$ the **Cantor-Bendixson derivative** that maps a subset $A\subseteq X$ to the set $d A$ of all its [[accumulation point|accumulation points]]. Then $(2^X,d)$ is a Magari algebra iff $X$ is a [[scattered space]]. This result is due to L. Esakia and, independently, H. Simmons (cf. [Beklemishev-Gabelaia 2012](#BG12)).

## Related entries

* [[provability logic]]

* [[scattered space]]

* [[scattered topos]]

* [[diagonal argument]]

* [[Gödel's incompleteness theorem]]

* [[arithmetic pretopos]]

## References

* {#BG12}L. Beklemishev, D. Gabelaia, _Topological interpretations of provability logic_ , arXiv:1210.7317 (2012).  ([abstract](http://arxiv.org/abs/1210.7317))

* A. Macintyre, H. Simmons, _G&#246;del's diagonalization technique and related properties of theories_ , Coll. Math. **28** no.2 (1973) pp.165-180. ([pdf](http://yadda.icm.edu.pl/yadda/element/bwmeta1.element.desklight-8bd6a8c7-d547-43f0-b220-eda51556c1ad/c/cm28_2_01.pdf))