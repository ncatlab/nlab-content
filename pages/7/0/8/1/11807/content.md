
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

For $R \colon \mathcal{D} \to \mathcal{C}$ a [[functor]] which preserves [[finite limits]] then the [[left adjoint]] [[profunctor]] $\mathcal{C}\to Func(\mathcal{D}, \infty Grpd)^{op}$ factors through the [[pro-objects]] $Pro(\mathcal{D})$. This $\mathcal{C}\to Pro(\mathcal{D})$ is the _pro-left adjoint_ to $R$. Its extension $L\colon Pro(\mathcal{C})\to Pro(\mathcal{D})$ is a genuine [[left adjoint]] to $Pro(R)$, the _[[proadjoint]]_.

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

In general $\Pi_{pro}$ sends the [[terminal object]] to the [[shape of an (∞,1)-topos|shape]] of $\mathbf{H}$.


## References

* {#Hoyois13} [[Marc Hoyois]], _A note on &#201;tale homotopy_, 2013 ([pdf](http://math.northwestern.edu/~hoyois/papers/etalehomotopy.pdf))

[[!redirects pro-left adjoints]]