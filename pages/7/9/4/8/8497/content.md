
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $G$ a [[group]] and $V_1$ and $V_2$ two objects equipped with $G$-[[action]], the **conjugation action** on morphisms $f : V_1 \to V_2$ (not necessarily respecting the $G$-action) is for $g \in G$

$$
  f \mapsto g \circ f \circ g^{-1}
  \,.
$$

The [[invariants]] of the conjugation action are the $G$-action [[homomorphism]].

In the case that the $G$-action on $V_2$ is trivial, this is the _precomposition action_ and in the case that the action on $V_1$ is trivial this is the _postcomposition action_.

In [[matrix calculus]] conjugation actions are also known as _[[similarity transformations]]_.


## Definition
 {#Definition}

+-- {: .num_defn #ConjugationActionForDiscrete1Groups}
###### Definition

Given a [[discrete group]] $G$ and two $G$-actions $\rho_1$ and $\rho_2$ on [[sets]] $S_1$ and $S_2$, respectively, then the [[function set]] $[S_1, S_2]$ is naturally equipped with the [[conjugation action]]

$$
  Ad \;\colon \;  [S_1, S_2] \times G \longrightarrow [S_1,S_2]
$$

which takes $((S_1 \stackrel{f}{\to} S_2), g)$ to 

$$
  \rho_2(-)(g)\circ f \circ  \rho_1(-)(g^{-1})
  \;\colon\;
  S_1 \stackrel{\rho_1(-)(g^{-1})}{\longrightarrow} S_1 \stackrel{f}{\longrightarrow} S_2\stackrel{\rho_2(-)(g)}{\longrightarrow} S_2
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

The [[conjugation action]] construction of def. \ref{ConjugationActionForDiscrete1Groups} is the [[internal hom]] in the [[category]] of actions.

=--

+-- {: .proof}
###### Proof

We need to show that for any three [[permutation representations]],  [[functions]]

$$
  \phi \;\colon\; S_3 \longrightarrow [S_1,S_2]
$$

which [[intertwiner|intertwine]] the $G$-action on $S_3$ with the conjugation action on $[S_1,S_2]$ are in [[natural bijection]] with functions

$$
  \tilde \phi \;\colon\; S_3 \times S_1 \longrightarrow S_2
$$

which intertwine the diagonal action on the [[Cartesian product]] $S_3 \times S_1$ with the action on $S_2$.

The condition on $\phi$ means that for all $g\in G$ and $s_3 \in S_3$ it sends

$$
  \phi
   \;\colon\;
  \rho_3(s_3)(g)
  \mapsto
  \left(
    s_1 \mapsto
    \rho_2\left(
     \phi\left(s_3\right)\left( \rho_1\left(s_1\right)\left(g^{-1}\right) \right)\right)\left(g\right) 
  \right)
 \,.
$$

This is equivalently a function $\tilde \phi$ of two variables which sends

$$
  \tilde \phi
  \;\colon\;
  (\rho_3(s_3)(g), s_1)
  \mapsto
  \rho_2
  (
     \phi(s_3)( 
       \rho_1(s_1)(g^{-1})
     )
  )(g)
 \,.
$$

Since this has to hold for all values of the variables, it has to hold when substituing $s_1$ with $\rho_1(s_1)(g)$. After this substitution the above becomes

$$
  \tilde \phi
  \;\colon\;
  (\rho_3(s_3)(g),
  \rho_1(s_1)(g))
  \mapsto
   \rho_2(\phi(s_3)(s_1 ))(g) 
  \,.
$$

This is the intertwining condition on $\tilde \phi$. Conversely, given $\tilde \phi$ satisfying this for all values of the variables, then running the argument backwards shows that its hom-[[adjunct]] $\phi$ satisfies its required intertwining condition.

=--

The following is immediate but conceptually important:

+-- {: .num_prop }
###### Proposition

The [[invariants]] of the conjugation action on $[S_1,S_2]$ is the set of action [[homomorphisms]]/[[intertwiners]]. 

=--

Hence the inclusion of invariants into the conjugation action gives the inclusion of the external [[hom set]] of the category of $G$-action into the set underlying the [[internal hom]]

$$ 
  G Act(\rho_1,\rho_2)\hookrightarrow [\rho_1,\rho_2]
  \,.
$$



+-- {: .num_remark }
###### Remark

Regarding the conjugation action as the [[internal hom]] of actions immediately gives the generalization of this concept to more general kinds of actions, notably to [[infinity-actions]] in general [[(infinity,1)-toposes]]. See at _[infinity-action -- Conjugation action](infinity-action#CartesianClosedMonoidalStructure)_ for more on this.

=--

## Related concepts

* [[inner automorphism]]

* [[adjoint action]], [[free loop space of classifying space]]

* [[conjugate subgroup]]


[[!redirects conjugation actions]]

[[!redirects precomposition action]]
[[!redirects precomposition actions]]

[[!redirects postcomposition action]]
[[!redirects postcomposition actions]]

[[!redirects pre-composition action]]
[[!redirects pre-composition actions]]

[[!redirects post-composition action]]
[[!redirects post-composition actions]]


