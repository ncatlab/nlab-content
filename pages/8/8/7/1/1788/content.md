> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak


***

## Idea

For a [[pair]] of [[coprime]] [[natural numbers]] $n_+, n_- \in \mathbb{N}_{\geq 1}$, $qcd(n_+, n_-) = 1$, the *$(n_+, n_-)$-spindle* --- also denoted $S^2(n_+, n_-)$ or $\Sigma(n_+, n_-)$ and equivalently being the *weighted projective space* $\mathbb{C}P(n_+, n_-)$ --- is the 2-[[dimension of a manifold|dimensional]] [[orbifold]] whose [[underlying]] coarse [[topological space]] is the [[2-sphere]]/[[Riemann sphere]] $\mathbb{C}P^1$, but where the [[poles]] $0, \infty \in \mathbb{C}P^1$ are [[cone]] tips of order $n_+, n_-$, respectively.

If either $n_\pm = 1$ but $n_{\pm} \gt 1$ then this is also called a *teardrop* orbifold. If both $n_+ = n_- = 1$ then the definition reduces to that of the ordinary ([[Riemann sphere|Riemann]]) [[2-sphere]] $S^2$.

## Definition

We describe the spindle orbifold [as a proper étale Lie groupoid](orbifold#DefinitionViaProperEtaleGroupoids) (the following  description is far from unique, as far as [[Morita equivalence|Morita equivalent]] [[proper topological groupoid|proper]] [[étale Lie groupoids]] go, but it is about the simplest evident realization):

1. the [[smooth manifold]] of [[objects]] is the [[disjoint union]] of two copies of the [[plane]] $\mathbb{R}^2$ --- which for notational purposes, at least, will be useful to think of as the *[[complex line]]* $\mathbb{C}$:
  \[
    \label{ObjectSpaceForSpindleGroupoid}
    Obj\big(\mathbb{C}P(n_+, n_-)\big) 
      \;\coloneqq\; 
    \mathbb{C}_+
      \;\sqcup\;
    \mathbb{C}_-
    \mathrlap{\,,}
  \]

2. the [[smooth manifold]] of [[morphisms]] is the [[disjoint union]] of 

   1. (these) two copies of $\mathbb{C}$ [[product manifold|times]] the [[underlying set]] of the [[cyclic group]] $C_{n_{\pm}}$ of [[order of a group|order]] $n_\pm$, respectively,

   1. two copies of its [[puncture|punctured]] version $\mathbb{C}^\times \coloneqq \mathbb{C} \setminus \{0\}$ (its [[complement]] of the origin), [[product manifold|times]] the [[underlying set]] of the [[direct product group|product]] [[cyclic group]] $C_{n_{+}} \times C_{n_-}$:

  \[
    \label{MorphismSpaceForSpindleGroupoid}
    Mor\big(\mathbb{C}P(n_+, n_-)\big) 
      \;\coloneqq\; 
    \Big(
      (\mathbb{C}_+ \times C_{n_+})
        \;\sqcup\; 
      (\mathbb{C}_- \times C_{n_-})
   \Big)
      \;\sqcup\; 
    \Big(
      (\mathbb{C}_{+-}^\times \times C_{n_+} \times C_{n_-})
        \;\sqcup\; 
      (\mathbb{C}_{-+}^\times \times C_{n_-} \times C_{n_+})
    \Big)
    \mathrlap{\,,}
  \]

where the subscripts only serve to [[indexed set|index]] the [[direct sum|direct summands]]. Here the first pair of direct summands may be referred to as the "internal" morphisms (as they will operate within either chart, implementing here the actual orbi-singularities), and the second pair of summands as the "external" or "gluing" morphisms (as they operate between charts, implementing nothing but their gluing).

Concretely, with the abbreviation

$$
  q_{\pm}
  \coloneqq
  e^{2 \pi \mathrm{i}/n_{\pm}}
  \,,
$$

the [[source]] and [[target]] [[smooth function|maps]] are

$$
  \begin{array}{ccc}
    Mor\big(\mathbb{C}P(n_+, n_-)\big)
    &\overset{(s,t)}{\longrightarrow}&
    Obj\big(\mathbb{C}P(n_+, n_-)\big)^2
    \\
    \big(
      (z,\pm), [k_\pm]
    \big)
      &\mapsto&
    \big(
      (z, \pm)
      ,
      (z q_{\pm}^{k_{\pm}}, \pm)
    \big)
    \\
    \\
    \big(
      (v,\pm \mp), [0], [0]
    \big)
      &\mapsto&
    \Big(
      \big( 
        v^{n_\pm}, \pm
      \big)
      ,
      \big(
        v^{-n_\mp}, \mp
      \big)
    \Big)
  \end{array}
$$

and the [[composition]] map for the "internal" morphisms is that of the [[action groupoid]] $\mathbb{C}_{\pm} \sslash C_{\pm}$:

$$
  \begin{array}{ccc}
    Mor\big(\mathbb{C}P(n_+, n_-)\big)
    {}_s \times_t
    Mor\big(\mathbb{C}P(n_+, n_-)\big)
    &\overset{(-)\circ (-)}{\longrightarrow}&
    Mor\big(\mathbb{C}P(n_+, n_-)\big)
    \\
    \Big(
     \big(
       (z q_{\pm}^{k_{\pm}} ,\pm),[k'_\pm]
     \big)
     , 
     \big(
       (z,\pm),[k_\pm]
     \big)
    \Big)
     &\mapsto&
    \big(
      (z,\pm), [k'_\pm + k_\pm]
    \big) 
    \,.
  \end{array}
$$

Finally, the general "gluing" morphism is the unique composite

$$
  \big(
    (v,\pm,\mp), [k_\pm], [k_\mp]
  \big)
  \;\equiv\;
  \big(
    (v^{-n_\mp},\mp), [k_\mp])
  \big)
  \circ
  \big(
    (v,\pm,\mp), [0], [0]
  \big)
  \circ 
  \big(
    (v^{n_\pm} \cdot q^{-k_{\pm}}, \pm), [k_\pm]
  \big)
  \,,
$$

which defines either side by the other (meaning that the gluing morphisms are a [[groupoid torsor]] from either side over these [[action groupoids]]). Its [[source]] and [[target]] maps are

$$
  (s,t)
  \;\colon\;
  \big(
    (v,\pm,\mp), [k_\pm], [k_\mp]
  \big)
  \mapsto
  \big(
    (v^{-n_{\mp}} \cdot q^{+ k_{\mp}}, \pm)
    ,
    (v^{n_{\pm}} \cdot q^{- k_{\pm}}, \pm)
  \big)
  \mathrlap{\,.}
$$



(...)