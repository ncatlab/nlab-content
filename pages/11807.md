
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}
## Idea

For $R \,\colon\, \mathcal{D} \to \mathcal{C}$ a [[functor]] which [[preserved limit|preserves]] [[finite limits]], the [[left adjoint]] [[profunctor]] 

\[
  \label{FormulaForLeftAdjointProfunctor}
  \array{
    \mathcal{C} 
    &\longrightarrow&
    Func(\mathcal{D}, Set)^{op} 
    \\
    c
    &\mapsto&
    \Big(
    d 
      \mapsto
      \mathcal{C}
      \big(
        c
        ,\,
        R(d)
      \big)
    \Big)
  }
\]

factors through the [[pro-objects]] $Pro(\mathcal{D})$. This $\mathcal{C}\to Pro(\mathcal{D})$ is called the _pro-left adjoint_ to $R$. Its extension $L\colon Pro(\mathcal{C})\to Pro(\mathcal{D})$ is a genuine [[left adjoint]] to $Pro(R)$, the _[[proadjoint]]_.

The analogous definition applies in the generality of [[(infinity,1)-category theory|$(\infty,1)$-category theory]] -- if [[Set]] is replaced by [[∞Grpd]] in (eq:FormulaForLeftAdjointProfunctor) -- to yield the notion of pro left-adjoint [[(∞,1)-functors]], generalizing [[left adjoint|left]] [[adjoint (∞,1)-functors]]. 

## Example

### Pro-&#233;tale homotopy type

Consider any [[(∞,1)-sheaf ∞-topos]] with its [[global sections]] [[geometric morphism]]

$$
  \mathbf{H}
   \stackrel{\overset{\Delta}{\longleftarrow}}{\underset{\Gamma}{\longrightarrow}}
  \infty Grpd
 \,.
$$

If here the [[constant ∞-stack]] [[inverse image]] $\Delta$ does have a further [[left adjoint|left]] [[adjoint (∞,1)-functor]] $\Pi$ (so that $\mathbf{H}$ is a [[locally ∞-connected (∞,1)-topos]]) then $\Pi$ may be understood as taking any object to its [[fundamental ∞-groupoid]] or [[geometric realization]] [[homotopy type]].

In general $\Pi$ does not exist, but the pro-left adjoint $\Pi_{pro}$ of $\Delta$ may always be formed. This sends any object to what in the case of the $\infty$-topos over an [[étale site]] is called its _[[étale homotopy type]]_. 

In general $\Pi_{pro}$ sends the [[terminal object]] to the [[shape of an (∞,1)-topos|shape of the $(\infty,1)$-topos]] of $\mathbf{H}$.

##Related topics

* [[proadjoint]]

* [[prorepresentable functor]]

## References

Discussion in the context of [[shape of an (infinity,1)-topos|shape of an $(\infty,1)$-topos]]:

* {#Hoyois13} [[Marc Hoyois]], p. 3 of _Higher Galois theory_, Algebraic & Geometric Topology __17__ 1 (2017) 567-643 ([arxiv/1506.07155](https://arxiv.org/abs/1506.07155), [doi:10.2140/agt.2017.17.567](https://doi.org/10.2140/agt.2017.17.567))

See also:

* E. Giuli, Pro-reflective subcategories, J. Pure Appl. Algebra 33 (1984) 19&#8211;29.

[[!redirects pro-left adjoints]]

