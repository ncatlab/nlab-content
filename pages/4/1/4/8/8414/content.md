
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


# Contents 
* table of contents 
{: toc}

## Idea 

In [[order theory]], the _lexicographic order_ is a generalization of the order in which words are listed in a dictionary, according to the order of the first letters for which the spelling of two words differs. 

## Definition 

+-- {: .num_defn} 
###### Definition 

Let $\{L_i\}_{i \in I}$ be a [[well-ordered set|well-ordered]] [[indexed set|family]] of [[strict total order|strictly totally ordered sets]]. The **lexicographic order** on the [[Cartesian product]] of sets $L = \prod_{i \in I} L_i$ is the [[strict total order]] defined as follows: if $x, y \in L$ and $x \neq y$, then $x \lt y$ iff $x_i \lt y_i$ where $i$ is the [[least element]] in the set $\{j \in I \colon x_j \neq y_j\}$. 

=-- 

While this notion is most often seen for strict total orders, it can be applied also toward more general [[relations]]. For example, one might apply the construction to sets equipped with a [[transitive relation]] $\lt$, dropping the [[strict total order|trichotomy assumption]]. 

Often this notion is extended to [[subsets]] of $\prod_{i \in I} L_i$ as well. For instance, the [[free monoid]] $S^\ast$ on a [[linear order|linearly ordered]] set $S$ can be embedded in a countable power 

$$
  i \;\colon\; 
  S^\ast 
  \xhookrightarrow{\phantom{--}} 
  (1 + S)^\mathbb{N} 
  \;=\; 
  \prod_{n \in \mathbb{N}} (1 + S)
  \,,
$$ 

where $1 + S$ is the result of freely adjoining a bottom element $e$ to $S$, and for each finite list $(s_1, \ldots, s_k)$ we have 

$$i(s_1, \ldots, s_k) = (s_1, s_2, \ldots, s_k, e, e, e, \ldots).$$ 

Then the lexicographic order on $S^\ast$ is the one inherited from its embedding into the lexicographically ordered set $(1 + S)^\mathbb{N}$. 

+-- {: .num_remark #antidictionary} 
###### Remark 
The decision to freely adjoin a _[[bottom]]_ element $e$ is of course purely a convention, based on the ordinary dictionary convention that the Scrabble word AAH should come after AA. Alternatively, we could equally well deem that $e$ is a freely adjoined top element, so that AA comes after AAH; this might be called the "anti-dictionary" convention. 
=-- 

### Corecursive definition 

if $L$ is linearly ordered and the underlying set $C = L^\mathbb{N}$ is regarded as the [[terminal coalgebra]] for the functor $L \times - \colon Set \to Set$, with coalgebra structure $\langle h, t \rangle \colon C \to L \times C$, then the lexicographic order on $C$ may be defined [[corecursion|corecursively]]: 

* $c \lt c'$ if $h(c) \lt h(c')$ or ($h(c) = h(c')$ and $t(c) \lt t(c')$). 

For the special case $L = \mathbb{N}$, the terminal coalgebra $\mathbb{N}^\mathbb{N}$ with this lexicographic order is order-isomorphic to the real interval $[0, \infty)$. This isomorphism is described more precisely [here](/nlab/show/continued+fraction#PavPratt).

## References

A [[category theory|category theoretic]] analysis of lexicographic order:

* [[Reinhard Börger]], [[Walter Tholen]], Anna Tozzi: _Lexicographic sums and fibre-faithful maps_, Applied Categorical Structures **1** (1993) 59-83 &lbrack;[doi:10.1007/BF00872986](https://doi.org/10.1007/BF00872986)&rbrack;

[[!redirects lexicographic ordering]] 
[[!redirects dictionary order]] 
[[!redirects dictionary ordering]] 
