


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

For $\lambda$ a [[partition]]/[[Young diagram]], its Plancherel probability is (see at *[[hook length formula]]*):

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

With respect to the Plancherel measure $Part(n)$ in the [[limit of a sequence|limit]] of large $n \to \infty$, the [[logarithm]] of $dim\big( S^{(\lambda)}\big) = \left\vert sYTableaux_\lambda \right\vert$ (see at [[hook length formula]]) is [[almost surely]] approximately constant (i.e. independent of $\lambda$) on the value 

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


## References

* {#VershikKerov85} [[Anatoly Vershik]], [[Sergei Kerov]], *Asymptotic of the largest and the typical dimensions of irreducible representations of a symmetric group*, Functional Analysis and Its Applications volume 19, pages 21–31 (1985) ([doi:10.1007/BF01086021](https://doi.org/10.1007/BF01086021))

* Maciej Dołęga, *Central limit theorem for random Young diagrams with respect to Jack measure* 2014 ([pdf](https://www.impan.pl/~mdolega/papers/CLT.pdf))

See also:

* Wikipedia, [Plancherel measure](https://en.wikipedia.org/wiki/Plancherel_measure)

In relation to [[matrix models]]:

* Suvankar Dutta, Debangshu Mukherjee, Neetu, Sanhita Parihar, *A Unitary Matrix Model for q-deformed Plancherel Growth* ([arXiv:2105.09342](https://arxiv.org/abs/2105.09342))

[[!redirects Plancherel measures]]
