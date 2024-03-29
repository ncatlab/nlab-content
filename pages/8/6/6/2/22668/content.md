
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

 The *Schur-Weyl measure* is [[probability distribution]] on the [[set]] of  [[Young diagrams]] of given number of boxes, closely related to expressions appearing in [[Schur-Weyl duality]].

## Definition

For $n \in \mathbb{N}_+$, write:

* $YDiagrams_n$ for the [[set]] of [[partitions]] of $n$, hence of [[Young diagrams]] with $n$ boxes;

* for $\lambda \in YDiagrams_n$ write:

  * $sYTableaux_\lambda$ for the set of [[standard Young tableaux]] of shape $\lambda$;

  * for $N \in \mathbb{N}_+$ write

    * $ssYTableaux_\lambda(N)$ for the set of [[semistandard Young tableaux]] of shape $\lambda$ and with labels  $\leq N$.

Then the *Schur-Weyl measure* for $n,N \in \mathbb{N}$ is

$$
  \array{
    YDiagrams_N
    &
    \overset{ p^{SW} }{\longrightarrow}
    &
    [0,1]
    \\
    \lambda
    &\mapsto&
    \frac
      {   
        \left\vert
          sYTableaux_\lambda
        \right\vert
        \cdot
        \left\vert
          ssYTableaux_\lambda(N)
        \right\vert
      }
      {N^n}
  }
$$

(e.g. [Petrov 19, slide 76](#Petrov19))

In the special case that $N = n$, and writing

* $S^{(\lambda)} \in Rep(Sym(n))$ for the [[complex numbers|complex]] [[irreducible representation]] of the [[symmetric group]] which is labeled by $\lambda$ (the [[Specht module]], see the *[[representation theory of the symmetric group]]*);

* $V^{(\lambda)} \in Rep(Sym(n))$ for the [[complex numbers|complex]] [[irreducible representation]] of the ([[special linear group|special]]) [[general linear group]] which is labeled by $\lambda$ (see the *[[representation theory of the general linear group]]*),

this is equal to (see at *[[hook length formula]]*):

$$
  p^{SW}(\lambda)
  \;=\;
  \frac
    {
      dim\big( S^{(\lambda)} \big)
      \cdot
      dim\big( V^{(\lambda)} \big)
    }
    {N^n}
  \,.
$$




## Properties

### Entropy
 {#Entropy}

With respect to the Schur-Weyl measure on $Part(n)$ and in the [[limit of a sequence|limit]] of large $n = c N^2 \to \infty$, the [[logarithm]] of the Schur-Weyl probability is [[almost surely]] approximately constant (i.e. independent of $\lambda$) on the value 

$$
  -
  ln
  p^{SW}
  \;\sim\;
  \sqrt{n}\cdot H_c
$$

for some $H_c \in \mathbb{R}$, in that for all $\epsilon \in \mathbb{R}_+$ we have

$$
 \underset{n = c N^2 \to \infty}{\lim} 
 p^{SW}
 \left(
   \left\{
     \lambda \in Part(n)
     \;\left\vert\;
       \tfrac{-1}{\sqrt{n}}
       ln
       p^{SW}(\lambda)
       -
       H_c
       \;\lt\;
       \epsilon
     \right.
   \right\}
 \right)
 \;=\;
 1
  \,.
$$

([Mkrtchyan 14, Thm. 1.1](#Mkrtchyan14))


### Relation to Cayley distance kernel

The Schur-Weyl measure is the [[pushforward measure]] of the probability distribution on [[pure states]] encoded by the "Cayley state" ([here](Cayley+distance+kernel#TheCayleyState)): the [[quantum state]] that is given by the [[Cayley distance kernel]] -- see [there](Cayley+distance+kernel#TheCayleyStateProbabilityDistribution) for details.

## Related concepts

* [[Plancherel measure]]

* [[asymptotic representation theory]]

* [[Robinson-Schensted-Knuth algorithm]]


## References

Review:

* {#Petrov19} [[Leonid Petrov]], slides 73-76 in: *Random Matrices*, lecture notes 2019 ([pdf slides](https://rmt-fall2019.s3.amazonaws.com/rmt-fall2019.pdf), [[PetrovRandomMatrices.pdf:file]], [webpage](https://lpetrov.cc/2019/07/rmt-announce))

  > (in the context of [[random matrix theory]])

See also:

* {#Mkrtchyan14} [[Sevak Mkrtchyan]], *Entropy of Schur-Weyl Measures*, Annales de l'I.H.P. Probabilités et statistiques, Tome 50 (2014) no. 2, pp. 678-713.  ([arXiv:1107.1541](https://arxiv.org/abs/1107.1541), [numdam:AIHPB_2014__50_2_678_0](http://www.numdam.org/item/AIHPB_2014__50_2_678_0))

* [[Pierre-Loïc Méliot]], *Kerov’s central limit theorem for Schur-Weyl and Gelfand measures*, [DMTCS proc.](https://www.dmtcs.org/dmtcs-ojs/index.php/proceedings/) AO, 2011, 669–680 ([pdf](https://www.imo.universite-paris-saclay.fr/~meliot/files/kerovclt.pdf))

* {#Meliot10a} [[Pierre-Loïc Méliot]], _Kerov's central limit theorem for Schur-Weyl measures of parameter 1/2_ ([arXiv:1009.4034](https://arxiv.org/abs/1009.4034))


* M. S. Boyko and N. I. Nessonov, *Entropy of the Shift on $II_1$-representations of the Group $S(\infty)$* ([pdf](http://iamm.su/upload/iblock/9e9/t2-n1-15-37.pdf))


[[!redirects Schur-Weyl measures]]

