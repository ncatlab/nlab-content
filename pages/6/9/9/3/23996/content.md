
#Contents#
* table of contents
{:toc}

## Idea

*Persistent cohomotopy* (not yet an established term) would be the study of [[cohomotopy]] in situations where the [[domain]] [[topological space|space]] and/or its [[continuous function|map]] to an [[n-sphere]] may depend on a parameter to yield not just a single [[cohomotopy set]], but a [[filtered object|filtered]] set (a filtered [[group]] when the [[dimension of a cell complex|dimension]] of the domain space is large enough). One concrete implementation of this general notion is considered in [Franek & Krčál 2017](#FranekKrcal17), see [below](#Definition). 

In this context it has been shown ([Franek & Krčál 2016](#FranekKrcal16), [2017](#FranekKrcal17)) that persistent cohomotopy groups improve on the [[well groups]] used in [[persistent homology]] in ways that are practically relevant notably in [[topological data analysis]]:

1. persistent cohomotopy can distinguish functions that are indistinguishable by their [[well groups]] ([FK16, Sec. 1.2](#FranekKrcal16)),

1. even though coarser than cohomotopy groups, well groups in general are not (or not known to be) algorithmically [[computability|computable]], while the cohomotopy groups are proven computable in a fair range of dimensions ([CKMSVW14](computational+topology#CKMSVW14)).

Generally, one may understand persistent cohomotopy both as the [[duality|dual]] of *[[persistent homotopy]]* as well as a [[non-abelian cohomology]]-version of the more widely considered notion of [[persistent homology]]:


| | coarse |  intermediate | fine  |
|--|--|--|--|
| **[[homology]]** | [[ordinary homology]] | [[generalized homology]] | [[homotopy groups|homotopy]] |
| **[[cohomology]]** | [[ordinary cohomology]] | [[Whitehead-generalized cohomology|generalized cohomology]] | [[cohomotopy]] |
|  |  |  |  | 
| **persistent homology** | [[persistent homology|persistent ordinary homology]] | persistent generalized homology | [[persistent homotopy]] |
| **persistent cohomology** | persistent ordinary cohomology | persistent generalized cohomology | [[persistent cohomotopy]] |


## Definition
 {#Definition}

[Franek & Krčál 2017](#FranekKrcal17)

For 

* $X$ a [[topological space]],

* $n \in \mathbb{N}$ a [[natural number]],

* $r \in \mathbb{R}_{\gt 0}$ a [[positive number|positive]] [[real number]],

* $f \,\colon\, X \xrightarrow{\;\;\;\;\;\;} \mathbb{R}^n$ a [[continuous map]],

such that with

* $A_r \,\coloneqq\, f^{-1}\big( \mathbb{R}^n \setminus B_r \big) \;\xhookrightarrow{i_r}\; X\;$

we have that 

* $(X,A_r)$ is a [[CW-pair]] of [[dimension of a cell complex|dimension]] $dim(X) \leq 2n - 3$

consider the following induced [[exact sequence]] of [[cohomotopy]]-groups (where square brackets $[X,Y]$ denote the [[hom-set]] $Ho(X,Y)$ in the [[classical homotopy category]], hence [[homotopy classes]] of [[continuous functions]] $X \to Y$):

\begin{tikzcd}[row sep=small]
  \pi_{n-1}
  \big(
    X
  \big)
  \ar[r, "{ \iota_r^\ast}"]
  \ar[d, phantom, "{\coloneqq}"{rotate=-90}]
  &
  \pi_{n-1}
  \big(
    A 
  \big)
  \ar[d, phantom, "{\coloneqq}"{rotate=-90}]
  \ar[r, "{ \delta_r }"]
  &
  \pi_{n}
  \big(
    X
  \big)
  \ar[d, phantom, "{\coloneqq}"{rotate=-90}]
  \\
  \big[
    X
    ,\,
    S^{n-1}
  \big]
  \ar[r, "{ [\iota_r. S^{n-1}] }"]
  &
  \big[
    A
    ,\,
    S^{n-1}
  \big]
  \ar[r]
  &
  \big[
    X
    ,\,
    S^n
  \big]
\end{tikzcd}

and, finally, define the $n$-cohomotopy of $X$ *at resolution $1/r$ relative to $f$* to be ([FK17 (2)](#FranekKrcal17)):

$$
  \pi_n^{(f,r)}
  \;\coloneqq\;
  image(\delta_r)
  \;\simeq\;
  \Big\{
    [g/A_r]
    \,\in\,
    \pi_r(X/A_r)
    \,\big\vert\,
    (X, A_r) \xrightarrow{ \exists \, g } (\mathbb{R}^n,\, \mathbb{R}^n \setminus B_r)
  \Big\}
  \,,
$$

hence that subgroup of the cohomotopy group of the [[quotient topological space]] $X/A_r$ whose elements may be represented by [[continuous]] maps defined on all of $X$.

Notice that the function $f$ itself canonically represents an element

$$
  [f] \;\in\;
  \pi_n^{(f,r)}(X)
$$

which provides a base point, making this a [[pointed object|pointed]] group.

Moreover, for $r_1 \leq r_2$ we have a canonical inclusion

$$
  A_{r_2} \xhookrightarrow{ i_{r_1, r_2} }  A_{r_1}
$$

a canonical comparison [[homomorphisms]] of pointed groups


\begin{tikzcd}[row sep=small]
  \pi_n^{(f,r_1)}(X)
  \ar[d, hook]
  \ar[rr]
  &&
  \pi_n^{(f,r_2)}(X)
  \ar[d, hook]
  \\
  \big[
    X/A_{r_1}
    ,\,
    S^n
  \big]
  \ar[rr, "{ \big[ X/{i_{r_1,r_2}}, S^n\big] }"]
  &&
  \big[
    X/A_{r_2}
    ,\,
    S^n
  \big]
\end{tikzcd}

Regarding the [[positive number|positive]] [[real numbers]] ordered by $\leq$ as a [[poset]] and thus as a [[category]], the resulting [[diagram]]

$$
  \pi_n^{(f,\bullet)}
  (X)
  \;\colon\;
  (\mathbb{R}, \leq)
  \xrightarrow{\;\;\;}
  Grp
$$

is the *cohomotopy persistence module* ([FK17, p. 5](#FranekKrcal17), rhyming on *[[peristence module]]* in [[persistent homology theory]]) of $X$ relative to $f$.




## References

[[!include cohomotopy in topological data analysis -- references]]

[[!redirects persistent cohomotopy theory]]