
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

Given a [[presymplectic form]] $(X, \omega)$ (hence any closed [[differential 2-form]]), a _[[prequantization]]_ of it in the traditional sense is a choice of [[circle bundle with connection]] on $X$ whose [[curvature]] 2-form is $\omega$. Since the [[circle group]] $U(1)$ is equivalent, as a [[smooth ∞-group]] to the [[2-group]] coming from the [[crossed module]] $(\mathbb{Z} \hookrightarrow \mathbb{R})$, such a lift exists whenever the [[periods]] of $\omega$ are integral, hence are in the inclusion of the [[integers]] into the [[real numbers]] $\mathbb{Z} \hookrightarrow \mathbb{R}$.

But conversely this means that for _any_ closed differential 2-form $\omega$ there is a [[connection on a 2-bundle]] on a $(\Gamma \hookrightarrow \mathbb{R})$-[[principal 2-bundle]], where $\Gamma \hookrightarrow \mathbb{R}$ is the inclusion of the [[discrete group]] of [[periods]] of $\omega$. 

If here $\Gamma \hookrightarrow \mathbb{R}$ is a global multiple of the canonical inclusion $\mathbb{Z} \hookrightarrow \mathbb{R}$ then there is of course an [[isomorphism]] $(\mathbb{R}/\Gamma) \simeq (\mathbb{R}/\mathbb{Z}) =  U(1)$. This identification coresponds to a choice of _[[Planck's constant]]_ (see there).
 
If however $\Gamma$ is not [[finitely generated object|finitely generated]], then the [[smooth 2-group]] $(\Gamma \to \mathbb{R})$ is not equivalent to a smooth 1-group, and hence this is a genuine case of _[[higher geometric prequantization]]_. The upshot being that while not every closed 2-form has an ordinary [[prequantization]], it always does have one in [[higher geometric prequantization]], at least if we admit to choose the structure 2-group accordingly.

These considerations are currently mostly motivated purely mathematically. But the claim is that there useful physical applications (... eventually to be added here...).

## References

The observation that non-integral closed 2-forms can be prequantized by [[diffeological space|diffeological]] [[principal bundles]] for the diffeological quotient of $\mathbb{R}$ by the subgroup of periods is due to 

* [[Alan Weinstein]], _Cohomology of symplectomorphism groups and critical
values of hamiltonians_, Math. Z. 201 (1989), 75&#8212;82

and reviewed in section II 2.5 of 

* [[Jean-Luc Brylinski]], _Loop spaces, characteristic classes and geometric quantization_

The remark that the non-manifold quotient is usefully thought of as regarded instead in
 [[higher geometric prequantization]] by prequantum [[principal 2-bundles]] was made in

* [[Christoph Wockel]], _Non-integral geometric prequantisation_, talk at [HSLR II](http://www.ru.nl/math/research/vmconferences/higher-geometric/) (2012)


Mentioning of prequantization of non-integral forms is also in section 3.2.1 of 

* Yoshiaki Maeda, [[Peter Michor]], Takushiro Ochiai, Akira Yoshioka (eds.), _From Geometry to Quantum Mechanics: In Honor of Hideki Omori_

[[!redirects prequantization of non-integral 2-forms]]
[[!redirects geometric quantization of non-integral 2-forms]]
