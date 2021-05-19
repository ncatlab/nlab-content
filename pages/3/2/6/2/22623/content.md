
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
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

Given a [[partition]]/[[Young diagram]] $\lambda$ with $n$ boxes/of $n$:  

the *hook length formula* expresses both 

* the [[number]] of [[standard Young tableaux]] of shape $\lambda$,

* the [[dimension]] of the [[irreducible representation]] of [[symmetric group|Sym(n)]] labelled by $\lambda$ (i.e. of the [[Specht module]] $S^{(\lambda)}$)

in terms of the lengths of all "hooks" inside the Young diagram;

similarly, the *[[hook-content formula]]* expresses both

* the [[number]] of [[semistandard Young tableau]] of shape $\lambda$;

* the [[dimension]] of the [[irreducible representation]] of [[SU(n)]]

in terms of the length of all hooks and the "content" of all of the boxes.

[[!include hook length and content formulas -- table]]


## Preliminaries

Given a [[Young diagram]], the *hook* at any one of its boxes is the collection of boxes to the right and below that box, and including the box itself. We write "$\ell hook_\lambda$" for the *length* of such a hook, i.e. for the number of boxes it contains. Formally:

\begin{defn}\label{HookLength}
**(hook length)** \linebreak
Let $\lambda = (\lambda_1 \geq \cdots \geq \lambda_{rows(\lambda)})$ be a [[partition]]/[[Young diagram]]. Then for 

* $i \in \{1, \cdots, rows(\lambda)\}$,

* $j \in \{1, \cdots, \lambda_i\}$

the *hook length* at $(i,j)$ is

$$
  \ell hook_\lambda(i,j)
  \;\coloneqq\;
  1 +
  (\lambda_i - j) + (\lambda'_j - 1)
  \,,
$$

where $\lambda'$ denotes the *conjugate partition* (see [there](Young+diagram#Conjugation)).

\end{defn}

\begin{definition}
**(numbers of (semi-)standard Young tableaux)** \linebreak
Given a [[partition]] $\lambda \in Part(n)$, and a [[positive number|positive]] [[natural number]] $N \in \mathbb{N}_+$, consider

* the number of [[standard Young tableaux]]:

  \[
    \label{NumberOfStandardYoungTableauxOfFixedShape}
    \left\vert sYTableaux_\lambda\right\vert
    \;\in\;
    \mathbb{N}_+
  \]

* the number of [[standard Young tableaux]] with bounded entries $T_{i j} \leq N$:

  \[
    \label{NumberOfSemiStandardYoungTableauxOfFixedShape}
    \left\vert ssYTableaux_\lambda(N)\right\vert
    \;\in\;
    \mathbb{N}_+
  \]

of shape $\lambda$.
\end{definition}


## Details


### Counting standard Young tableaux

\begin{prop}
**(hook length formula for standard Young tableaux)** \linebreak
Given a [[partition]] ([[Young diagram]]) $\lambda$ of $n$ (boxes), the number (eq:NumberOfStandardYoungTableauxOfFixedShape) of [[standard Young tableaux]] of shape $\lambda$ equals the [[factorial]] of $n$ over the [[multiplication|product]] of the hook lengths (Def. \ref{HookLength}) at all the boxes of $\lambda$:

\[
  \label{HookLengthFormulaCountingNumberOfStandardYoungTableau}
  \left\vert 
    sYTableaux_\lambda
  \right\vert
    \;=\; 
  \frac{
    n!  
  }{
    \prod_{(i,j)} \ell hook_\lambda(i,j)
  }.
\]

\end{prop}

This is due to [Frame, Robinson & Thrall 54](#FrameRobinsonThrall54). Textbook accounts include [Stanley 99, Cor. 7.21.6](#Stanley99), [Sagan 01 Thm. 3.10.2](#Sagan01).

### Measuring dimension of irreps of $Sym(n)$

The [[dimension]] of the [[irrep]] of the [[symmetric group]] $Sym(n)$ that is labelled by a given [[Young diagram]] $\lambda$ (the [[Specht module]] $S^{(\lambda)}$, see at [[representation theory of the symmetric group]]) equals the number of [[standard Young tableaux]] of shape $\lambda$

\[
  dim(S^{(\lambda)})  
  \;=\;
  \left\vert
    sYTableaux_\lambda
  \right\vert
\]

(e.g. [Sagan, Thm. 2.6.5](#Sagan01)) 

and hence is also given by the hook length formula (eq:HookLengthFormulaCountingNumberOfStandardYoungTableau):

\[
  \label{HookLengthFormulaMeasuresDimensionOfIrrepOfSymmetricGroup}
  dim(S^{(\lambda)})
  \;=\;
  \frac{
    n!  
  }{
    \prod_{(i,j)} \ell hook_\lambda(i,j)
  }
  \,.
\]

This is actually the statement of [Frame, Robinson, & Thrall 54, Thm. 1](#FrameRobinsonThrall54). Textbook accounts include [James 78, Thm. 20.1](#James78).



### Counting semi-standard Young tableaux
 {#ForSemiStandardYoungTableaux}

\begin{prop}
**(hook length formula for semi-standard Young tableaux)** \linebreak
Given 

  * a [[partition]] ([[Young diagram]]) $\lambda$ of $n$ (boxes), 

  * a [[positive number|positive]] [[natural number]] $N \in \mathbb{N}_+$, 

the number (eq:NumberOfSemiStandardYoungTableauxOfFixedShape) of semi-standard Young tableaux of shape $\lambda$ and entries $\leq N$ ([hence](semistandard+Young+tableau#eq:RelationToSchurPolynomialsOfFinitelyManyVariables) the value of the [[Schur polynomial]] $s_\lambda(x_1, \cdots, x_N)$ at $x_i = 1$) is:

\[
  \label{TheHookLengthFormulaForSemistandardYoungTableaux}
  \left\vert
    ssYTableaux_\lambda(N)
  \right\vert
  \;=\;
  s_\lambda
  \big(
    \underset{
      \mathclap{
        N\; arguments
      }
    }{
    \underbrace{
      1, \cdots, 1
    }
    }
  \big)
    \;=\; 
  \underset{(i,j)}{\prod}
  \frac{
    N - i + j
  }{
    \ell hook_\lambda(i,j)
  }
  \,.
\]

\end{prop}

Here 

$$
  content(i,j) \;\coloneqq\; j - i
$$

is also called the *content* of the box $(i,j)$, whence (eq:TheHookLengthFormulaForSemistandardYoungTableaux) is also called a *[[hook-content formula]]* ("hook length and box content"):

$$
  \left\vert
    ssYTableaux_\lambda(N)
  \right\vert
  \;=\;
  s_\lambda
  \big(
    \underset{
      \mathclap{
        N\; arguments
      }
    }{
    \underbrace{
      1, \cdots, 1
    }
    }
  \big)
    \;=\; 
  \underset{(i,j)}{\prod}
  \frac{
    N + content(i,j)
  }{
    \ell hook_\lambda(i,j)
  }
  \,.
$$


### Measuring of dimension of irreps of $GL(n, \mathbb{C})$

The [[dimension]] of the [[irrep]] $V^{(\lambda)}$ of the [[general linear group]] $GL(n, \mathbb{C})$ that is labelled by a given [[Young diagram]] $\lambda$ (see at [[representation theory of the general linear group]]), is also given by the hook-content formula (eq:TheHookLengthFormulaForSemistandardYoungTableaux):

$$
  dim\big(V^{(\lambda)}\big)
  \;=\;
  \underset{(i,j)}{\prod}
  \frac{
    N + content(i,j)
  }{
    \ell hook_\lambda(i,j)
  }
$$

This appears as [Sternberg 94 (C.27)](#Sternberg94)


## Related concepts

* [[hook-content formula]]

* [[Plancherel measure]]

## References

### For standard Young tableaux

The original proof is due to:

* {#FrameRobinsonThrall54} [[James Sutherland Frame]], [[Gilbert de Beauregard Robinson]], [[Robert McDowell Thrall]], *The Hook Graphs of the Symmetric Group*, Canadian Journal of Mathematics, Volume 6, 1954, pp. 316 - 324 ([doi:10.4153/CJM-1954-030-1](https://doi.org/10.4153/CJM-1954-030-1))

Textbook accounts:

* {#James78} [[G. D. James]], Thm. 20.1 in: *The Representation Theory of the Symmetric Groups*,  Lecture Notes in Mathematics, volume 682, Springer 1978 ([doi:10.1007/BFb0067708](https://link.springer.com/book/10.1007/BFb0067708), [pdf](http://www-users.math.umn.edu/~webb/oldteaching/Year2010-11/the-representation-theory-of-the-symmetric-groups-SLN.pdf))

* {#Stanley99} [[Richard Stanley]], Cor. 7.21.6 in: *Enumerative combinatorics 2*, Cambridge University Press (1999, 2010) ([doi:10.1017/CBO9780511609589](https://doi.org/10.1017/CBO9780511609589), [webpage](http://www-math.mit.edu/~rstan/ec/))

* {#Sagan01} [[Bruce Sagan]], Thm. 3.10.2 & Thm. 2.6.5 in: _The symmetric group_, Springer 2001 ([doi:10.1007/978-1-4757-6804-6](https://link.springer.com/book/10.1007/978-1-4757-6804-6), [pdf](http://math.sfsu.edu/federico/Clase/RepTh/sagan.pdf))

Further review:

* Alex Ghorbani, Section 4.4 of: *Applications of representation theory to combinatorics* ([pdf](http://math.uchicago.edu/~may/REU2020/REUPapers/Ghorbani.pdf))


* [[Yufei Zhao]], Section 4.4. of _Young Tableaux and the Representations of the Symmetric Group_ ([pdf](https://yufeizhao.com/research/youngtab-hcmr.pdf), [[ZhaoYoungTableaux.pdf:file]])

* Shiyue and Andrew, *Young Tableaux and Probability*, 2019 ([pdf](http://www.mit.edu/~lindrew/hooklength.pdf))

See also:

* Wikipedia, *[Hook length formula](https://en.wikipedia.org/wiki/Hook_length_formula)*

Alternative proofs:

* Jean-Christophe Novelli, Igor Pak, Alexander V. Stoyanovskii, *A direct bijective proof of the hook-lengthformula*, Discrete Mathematics and Theoretical Computer Science1, 1997, 53–67 ([pdf](https://www.math.ucla.edu/~pak/papers/bij.pdf))

* Kenneth Glass, Chi-Keung Ng, *A Simple Proof of the Hook Length Formula*, The American Mathematical Monthly Vol. 111, No. 8 (Oct., 2004), pp. 700-704 ([jstor:4145043](https://www.jstor.org/stable/4145043)) 

* Jason Bandlow, *An elementary proof of the hook formula*, The Electronic Journal of Combinatorics **15** (2008) ([pdf](http://www.kurims.kyoto-u.ac.jp/EMIS/journals/EJC/Volume_15/PDF/v15i1r45.pdf))

* [[Bruce Sagan]], *Probabilistic proofs of the hook length formulas involving trees*, S&eacute;minaire Lotharingien de Combinatoire 61A (2009) ([pdf](https://users.math.msu.edu/users/bsagan/Papers/Old/pph.pdf))


Generalizations:

* Ionuţ Ciocan, Fontanine Matjaž, Konvalinka, Igor Pak, *The weighted hook length formula*, Journal of Combinatorial Theory, Series A Volume 118, Issue 6, August 2011, Pages 1703-1717 ([doi:10.1016/j.jcta.2011.02.004](https://doi.org/10.1016/j.jcta.2011.02.004))

* Alejandro Morales, Igor Pak, Greta Panova, *Hook formulas for skew shapes I. q-analogues and bijections*, Journal of Combinatorial Theory Series A 154 (2018), pp 350--405 ([arXiv:1512.08348](https://arxiv.org/abs/1512.08348))

### For semistandard Young tableaux

The original proof:

* [[Richard Stanley]], Theorem 15.3 in: *Theory and application of plane partitions 2*, Studies in Applied Math. **50** 3 (1971), 259-279 ([pdf](http://www-math.mit.edu/~rstan/pubs/pubfiles/12-2.pdf), [[StanleyPlanePartitions2.pdf:file]])

Review:

* {#Stanley99} [[Richard Stanley]], Thm. 7.21.2 in: *Enumerative combinatorics 2*, Cambridge University Press (1999, 2010) ([doi:10.1017/CBO9780511609589](https://doi.org/10.1017/CBO9780511609589), [webpage](http://www-math.mit.edu/~rstan/ec/))

* *A proof of the HCF* ([pdf](https://someproofsandstuff.files.wordpress.com/2015/03/hookcon.pdf), [[AProofOfTheHCF.pdf:file]])

### For dimensions of irreps

Textbook accounts:

* {#Sternberg94} [[Shlomo Sternberg]], Section 5.4 and Appendix C.7 of: *Group Theory and Physics*, Cambridge University Press 1994

Review for [[Sym(n)]]:

* James Stevens, Section 2.2 of: *Schur-Weyl duality* ([pdf](http://math.uchicago.edu/~may/REU2016/REUPapers/Stevens.pdf))

Review for [[SU(n)]]:

* {#Peluse14} [[Sarah Peluse]], Section 1 of: *Irreducible representations of $SU(n)$ with prime power degree*, S&eacute;minaire Lotharingien de Combinatoire 71 (2014), Article B71d ([pdf](https://www.emis.de/journals/SLC/wpapers/s71peluse.pdf))

* *Some Notes on Young Tableaux as useful for irreps of $\mathrm{su}(n)$* ([pdf](http://www.physics.mcgill.ca/~keshav/673IV/youngtableaux.pdf))

* Section 2 of: *Group Theory primer $SU(n)$* ([pdf](http://web.physics.ucsb.edu/~phys229B/s2013/Lectures_files/Chap13grouptheory.pdf))


[[!redirects hook length formulas]]

[[!redirects hook-length formula]]
[[!redirects hook-length formulas]]


