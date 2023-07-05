
### Canonical Forgetful Functor
 {#CanonicalForgetfulFunctor}

Every $\mathcal{V}$-[[enriched monoidal category]] $(\mathcal{C}, \otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ has a canonical [[forgetful functor]] 

$$
  U_{\mathcal{C}} \coloneqq \mathcal{C}(1_{\mathcal{C}},-) \colon \mathcal{C} \longrightarrow \mathcal{V}
$$

given by forming [[hom-objects]] out of the [[tensor unit]]. 

This functor is automatically [[lax monoidal functor|lax monoidal]] and if $\mathcal{C}$ is [[closed monoidal category|closed monoidal]] with [[internal hom]] $[-,-]_{\mathcal{C}}$ then we further have $U_{\mathcal{C}}[-,-]_{\mathcal{C}} \cong \mathcal{C}(-,-)$. This functor is particularly important to the theory of enriched categories.

+-- {: .num_prop #CanonicalForgetfulFunctor} 
###### Proposition

$U_{Ch} \colon Ch_\bullet(\mathcal{A}) \to R\text{Mod}$ takes a chain complex to its cycles/closed elements of degree 0.
=--

\begin{remark}
In particular $U_{Ch}$ does not simply take a chain complex to its term at degree 0. That would of course give a different forgetful functor.
\end{remark}




***


$$
  Br_N
  \longrightarrow
  Aut\big(
    \pi(\Sigma \setminus N)
  \big)
  \longrightarrow
  Aut\Big(
    A\big(
      \Sigma \setminus N
    \big)
  \Big)
$$


