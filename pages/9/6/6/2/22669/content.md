


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A [[probability distribution]] on [[Young diagrams]].

## Definition

From an [answer](https://math.stackexchange.com/questions/846556/why-is-the-plancherel-measure-interesting/3487507#3487507) by [[Vadim Alekseev]]:

Suppose $G$ is a [[locally compact group]].
What one ultimately wants to study is (upon fixing _a_ Haar measure in the noncompact case) the left regular representation $\lambda\colon G\to U(L^2(G,\mathrm{Haar}))$. Now, general theory tells us that while it's not always possible to decompose $L^2(G)$ as a direct _sum_ of irreducible reprenentations (this already fails for $G=\mathbb{Z}$), it is always possible to decompose it as a [[direct integral]] of irreducible representations (which are parametrised by the [[unitary dual]] $\widehat G$ of $G$). Now, if $G$ is unimodular and type I,  the direct integral decomposition (with respect to _both_ left and right actions of $G$) is as follows:
$$
L^2(G) \cong \int_{\widehat G} H_\pi\,d\mu(\pi),
$$
where $H_\pi = \pi\otimes \pi^*$, and its understanding requires, in particular, to determine the measure $\mu$ on $\widehat G$ such that the above becomes an isometric isomorphism. The unique measure with this property is called the *Plancherel measure* of $G$ (associated to a given Haar measure). Equivalently, it's the unique measure such that
$$
\|f\|_2^2 = \int_{\widehat{G}} \|\pi(f)\|_{\mathrm{HS}}^2 \mathrm{d}\mu(\pi),\quad f\in L^1(G,\mathrm{Haar})\cap L^2(G,\mathrm{Haar}).
$$

From a [[MathOverflow]] [answer](https://mathoverflow.net/questions/284756/characterizing-the-plancherel-measure/284762#284762) by [[Cameron Zwarich]]:

If $G$ is a unimodular second countable Type I group, then the Plancherel measure is the unique measure $\mu$ such that
$$\|f\|_2^2 = \int_{\widehat{G}} \|\pi(f)\|_{\mathrm{HS}}^2 \mathrm{d}\mu(\pi).$$
for every $f \in \mathrm{L}^1(G) \cap \mathrm{L}^2(G)$. This appears as Theorem 18.8.2 in Dixmier's book on $C^*$-algebras.

When $G$ is not unimodular, the question becomes more complicated, because the Plancherel measure needs to be twisted by a section of a line bundle; see the paper of Duflo-Moore on the subject for the gory details. When $G$ is not second countable, I do not know of a published result; the technical details of direct integral theory are more difficult in this case and not standard. When $G$ is not Type I, the decomposition of the left regular representation into irreducibles is no longer unique, and some of the operators on the right-hand side of the formula will fail to have finite Hilbert-Schmidt norm.

The closest analogue to the definition of a [[Haar measure]] on abelian [[locally compact groups]] as a left-invariant [[Radon measure]] is the characterization of the Plancherel measure as a unique co-invariant trace (or weight) on the von Neumann algebra $\mathcal{M}$ generated by the left-regular representation of $G$. Suppose $G$ satisfies the same hypotheses as above and $\Delta : \mathcal{M} \to \mathcal{M} \overline{\otimes} \mathcal{M}$ is the comultiplication on $\mathcal{M}$ given by $\lambda(s) \mapsto \lambda(s) \otimes \lambda(s)$. Then the Plancherel trace is the unique normal semifinite trace $\tau$ on $\mathcal{M}$ such that
$$\tau((\varphi \otimes \mathrm{id}) (\Delta(a))) = \tau(a)$$
for all $a \in \mathcal{M}_\tau^+$ and $\varphi \in \mathcal{M}_*$. A similar characterization holds for the Plancherel weight of an arbitrary locally compact group, or for the Haar weight of a locally compact quantum group. For proofs, see volume 2 of Takesaki or any of the literature on von Neumann algebraic quantum groups.

## Definition for symmetric groups

For $\lambda$ a [[partition]]/[[Young diagram]], its *Plancherel probability* is (see at *[[hook length formula]]*):

$$
  p^{Pl}_\lambda
  \;\coloneqq\;
  \frac
    {
      \big(
        dim(S^{(\lambda)}) 
      \big)^2
    }
    {n!}
  \;=\;
  n!
  \underset{
    { 1 \leq i \leq rows(\lambda) }
    \atop
    { 1 \leq j \leq \lambda_i }
  }{\prod}
  \frac{1}{ \big(\ell hook_\lambda(i,j)\big)^2 }
  \,,
$$

where 

* $S^{(\lambda)}$ denotes the [[complex numbers|complex]] [[irrep]] of the [[symmetric group]] that is labelled by $\lambda$ via the [[representation theory of the symmetric group]] (the $\lambda$th [[Specht module]])
 
* $\ell hook_\lambda(i,j)$ denotes the *hook length* at the $(i,j)$-box in the Young diagram $\lambda$.

## Properties
 {#Properties}

With respect to the Plancherel measure on $Part(n)$ and in the [[limit of a sequence|limit]] of large $n \to \infty$, the [[logarithm]] of $dim\big( S^{(\lambda)}\big) = \left\vert sYTableaux_\lambda \right\vert$ (see at [[hook length formula]]) is [[almost surely]] approximately constant (i.e. independent of $\lambda$) on the value 

$$
  ln
  \big(
    \left\vert sYTableaux_\lambda \right\vert
  \big)
  \;\sim\;
  \tfrac{c}{2}
  \sqrt{n}
  -
  \tfrac{1}{2}\ln(n!)
$$

for some $c \in \mathbb{R}$ (numerically: $c \gt 1.8$), in that for all $\epsilon \in \mathbb{R}_+$ we have

$$
 \underset{n \to \infty}{\lim} 
 p^{Pl}
 \left(
   \left\{
     \lambda \in Part(n)
     \;\left\vert\;
       \tfrac{2}{\sqrt{n}}
       ln
       \frac
         {\left\vert sYTableaux_\lambda \right\vert}
         {\sqrt{n!}}
       -
       c
       \;\lt\;
       \epsilon
     \right.
   \right\}
 \right)
 \;=\;
 1
  \,.
$$

([Vershik & Kerov 85, p. 22 (2 of 11)](#VershikKerov85))

## Related concepts

* [[Schur-Weyl measure]]

* [[hook length formula]]

* [[asymptotic representation theory]]

## References

* {#VershikKerov85} [[Anatoly Vershik]], [[Sergei Kerov]], *Asymptotic of the largest and the typical dimensions of irreducible representations of a symmetric group*, Functional Analysis and Its Applications volume 19, pages 21–31 (1985) ([doi:10.1007/BF01086021](https://doi.org/10.1007/BF01086021))

* Maciej Dołęga, *Central limit theorem for random Young diagrams with respect to Jack measure* 2014 ([pdf](https://www.impan.pl/~mdolega/papers/CLT.pdf))

See also:

* Wikipedia, [Plancherel measure](https://en.wikipedia.org/wiki/Plancherel_measure)

* [[Anatoly Vershik]], *Two lectures on the asymptotic representation theory and statistics of Young diagrams*,  In: Vershik A.M., Yakubovich Y. (eds) *Asymptotic Combinatorics with Applications to Mathematical Physics* Lecture Notes in Mathematics, vol 1815. Springer 2003 ([doi:10.1007/3-540-44890-X_7](https://doi.org/10.1007/3-540-44890-X_7))

* [[G. Olshanski]], *Asymptotic representation theory*, Lecture notes 2009-2010 ([webpage](https://lpetrov.cc/art), [pdf 1](https://storage.lpetrov.cc/Olshanski_ART_course_1.pdf), [pdf 2](https://storage.lpetrov.cc/Olshanski_ART_course_2.pdf))

In relation to [[matrix models]]:

* Suvankar Dutta, Debangshu Mukherjee, Neetu, Sanhita Parihar, *A Unitary Matrix Model for q-deformed Plancherel Growth* ([arXiv:2105.09342](https://arxiv.org/abs/2105.09342))

[[!redirects Plancherel measures]]
