


### Group completed configuration spaces

We discuss enriched configuration-space models of [[group completions]] of plain [[configuration spaces of points]].

Write $Conf(\mathbb{R}^n)$ for the "plain" configuration space of unlabeled and unordered points in $\mathbb{R}$, hence the space of finite subsets of $\mathbb{R}^n$.
This is a naturally a topological partial abelian monoid, where the addition of a pair of configurations is well-defined if they are disjoint, in which case it is given by their union &lbrack;[Segal 1973, p. 215](#Segal73)&rbrack;.
Let's write
$$
  \mathbb{G}Conf(\mathbb{R}^n)
  \;\coloneqq\;
  \Omega B_{\sqcup} Conf(\mathbb{R}^n)
$$
for the [[group completion]] of the configuration space with respect to this partial operation of disjoint union. 

[Segal 1973, Thm. 1](#Segal73) says, in particular, that this group completed configuration space is [[weak homotopy equivalence|weak homotopy equivalent]] to the $n$-fold [[iterated loop space]] of the [[n-sphere|$n$-sphere]] $S^n$:
$$
  \mathbb{G} Conf(\mathbb{R}^n)
  \;\simeq\;
  \Omega^n S^n
  \,.
$$

Here is should be useful to have a more explicit description of the group completed configuration space again as a configuration space, now of objects somewhat richer than plain points.

\begin{imagefromfile}
    "file_name": "OkuyamaRelations-240714.jpg",
    "float": "right",
    "width": 300,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 15
    }
\end{imagefromfile}


Since the group completion must introduce the existence of "anti-points" much in the sense of [[antiparticles]], it is tempting to think that $\mathbb{G}Conf(\mathbb{R}^n)$ should be equivalent to the configuration space $Conf^{\pm}(\mathbb{R}^n)$ of *charged* points, where each point in a configuration carries a label in $\{\pm 1\}$ and where equal-charged points must not coincide while oppositely charged points may coincide in which case they annihilate &lbrack;[McDuff 1975, p. 94](#McDuff75)&rbrack;.
However, this is *not* the case: $Conf^{\pm}(\mathbb{R}^n) \neq \mathbb{G}Conf(\mathbb{R}^n)$ &lbrack;[McDuff 1975, p. 96](#McDuff75)&rbrack;.

Still, the basic idea can be salvaged &lbrack;[Okuyama 2005](#Okuyama05)&rbrack; if only one allows charged points to be replaced by "strings" --- namely straight line segments of finite lenght in $\mathbb{R}^n$ each parallel to, say, the first coordinate axis --- with charged endpoints, where pair creation/annihilation of strings smoothens out the corresponding interaction of points, in the familiar way in which interactions in [[string theory]] smoothen out singular [[Feynman diagrams]] (only that here this is not postulated but demanded in order that the resulting moduli space models $\mathbb{G}Conf(\mathbb{R}^n)$):

On the right, if a filled circle is taken to indicate that the corresponding point is part of the interval, while an open circle indicates that it is not, then the curved arrows correspond to continuous paths in the configuration space of intervals, $Conf^I(\mathbb{R}^n)$, according to [Okuyama 2005, Def. 3.1-2](#Okuyama05) --- there denoted $I_n(S^0)$.

With this stringy resolution of the charged points, the expected equivalence does hold &lbrack;[Okuyama 2005, Thm. 1](#Okuyama05)&rbrack;:

$$
  Conf^I(\mathbb{R}^n)
  \;\;
  \simeq
  \;\;
  \mathbb{G}Conf(\mathbb{R}^n)
  \,.
$$

(...)


## References

* {#Segal73} [[Graeme Segal]], *Configuration-spaces and iterated loop-spaces*, Invent. Math. **21** (1973) 213-221  &lbrack;[doi:10.1007/BF01390197](https://doi.org/10.1007/BF01390197), [pdf](http://dodo.pdmi.ras.ru/~topology/books/segal.pdf), MR 0331377&rbrack;

* {#McDuff75} [[Dusa McDuff]], *Configuration spaces of positive and negative particles*, Topology **14** 1 (1975) 91-107 \[<a href="https://doi.org/10.1016/0040-9383(75)90038-5">doi:10.1016/0040-9383(75)90038-5</a>, [pdf](https://core.ac.uk/download/pdf/81183648.pdf)\]

* {#Okuyama05} [[Shingo Okuyama]]: *The space of intervals in a Euclidean space*, Algebr. Geom. Topol. **5** (2005) 1555-1572 &lbrack;[arXiv:math/0511645](https://arxiv.org/abs/math/0511645), [doi:10.2140/agt.2005.5.1555](https://doi.org/10.2140/agt.2005.5.1555)&rbrack;

