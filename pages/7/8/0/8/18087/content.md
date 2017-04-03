
# F-norms
* table of contents
{: toc}

## Idea

An F-norm is a non-homogeneous variant of a [[norm]]: a translation-invariant [[metric]] on a [[vector space]] that satisfies properties in between being a [[G-norm]] (on the underlying [[abelian group]] of the vector space) and being a norm.  As with norms, there is a pseudo- variant.


## Definitions

Let $K$ be a [[topological field]] (typically the [[real numbers]] or the [[complex numbers]], but conceivably only a [[topological ring]], or at least a [[commutative ring|commutative]] one); we will call the elements of $K$ ''scalars''.  Let $V$ be a [[vector space]] (or [[module over a ring|module]]) over $K$; we will call the elements of $V$ ''vectors''.  Let $\|{-}\|$ be a [[function]] from (the underlying set of) $V$ to the set of [[real numbers]].

+-- {: .num_defn #Gseminorm}
###### Definition

If

1. ${\|0_V\|} = 0$ (or even just ${\|0\|} \leq 0$),
2. ${\|{-x}\|} = {\|x\|}$ (or even just ${\|{-x}\|} \leq {\|x\|}$) for each vector $x$, and
3. ${\|x + y\|} \leq {\|x\|} + {\|y\|}$ for each vector $x$ and vector $y$,

then ${\|{-}\|}$ is a __[[G-seminorm]]__.
=--

This is enough to prove that ${\|x\|} \geq 0$ for each $x$ in $V$, making $(x,y) \mapsto {\|y - x\|}$ (precisely) a translation-invariant [[metric]] on $V$.

Note that (under this metric), a [[net]] $x$ of vectors converges to zero iff, for each [[positive number]] $\delta$, eventually ${\|x\|} \lt \delta$.

+-- {: .num_defn #Fseminorm}
###### Definition

If

1. $\|{-}\|$ is a G-seminorm and
2. $a x + y$ converges to zero for each [[directed set]] $I$ (or even just for ${|I|} \leq 2^{2^{{|K|}+2{|V|}}}$ to avoid [[size issues]][^filters]), each [[Cauchy net|Cauchy]] $I$-net $a$ of scalars, each $I$-net $x$ of vectors that converges to zero, and each $I$-net $y$ of vectors that converges to zero,

[^filters]: Or use [[filters]].

then $\|{-}\|$ is an __F-seminorm__.
=--

If $K$ is [[complete space|complete]], then it is sufficient in clause \ref{Fseminorm}.2 to hypothesize that $a$ is [[convergent net|convergent]]; in that case, an F-seminorm is simply a G-seminorm such that both addition and scalar multiplication are continuous (relative to the topology on $K$ and the metric on $V$).