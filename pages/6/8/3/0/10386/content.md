
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[physics]], a [[local Lagrangian]] induces a [[covariant phase space]] equipped with a canonical [[presymplectic form]]. The [[quotient]] of this by [[symmetries]] that, in good cases, make the pre-symplectic form a genuine [[symplectic form]], is called the _reduced phase space_. 

Generally, given a [[symplectic manifold]] or [[presymplectic manifold]] or [[Poisson manifold]] regarded as a [[phase space]] equipped with a suitable ([[Hamiltonian action|Hamiltonian-]]) [[action]] by a [[Lie group]], the corresponding [[symplectic reduction]] or [[presymplectic reduction]] or [[Poisson reduction]] is, if it exists, the corresponding reduced phase space.

[[!include symplectic reduction - table]]

## Details

### For local Lagrangians

Given a [[local Lagrangian]] (we display it in [[codimension]] 1 [[mechanics]] for simplicity of notation)

$$
  L \;\colon\; \Omega^{0,1}\left(\mathbf{Fields}(I) \times I\right)
$$

the corresponding [[covariant phase space]] is the space of solutions of the [[Euler-Lagrange equations]]

$$
  \{EL = 0\} 
$$

equipped with the [[presymplectic form]]

$$
  \omega = \delta \frac{\delta L}{\delta \dot \phi} \wedge \delta \phi
$$

which is exact, with [[potential]]

$$
  \theta = \frac{\delta L}{\delta \dot \phi} \wedge \delta \phi
$$

as discussed in detail at _[[covariant phase space]]_.

Together, this is a [[prequantum bundle]], hence a [[circle bundle with connection]] whose [[curvature]] is $\omega$. It so happens that the underlying U(1)-[[principal bundle]] of this is trivial, and hence the [[connection on a bundle|connection]] is given by the globally defined [[differential 1-form]] $\theta$.

But this trivialility is only superficial: the [[symmetry]] [[group]] $G$ of the Lagrangian is supposed to act by [[Hamiltonian flows]] and the prequantum connection $\theta$ is to be equipped with $G$-[[equivariant connection]] structure for it to count as a connection on the [[reduced phase space]].

Another way to say this, using the [[higher differential geometry]] of [[smooth groupoids]]: the above [[prequantum bundle]] is modulated by a map $\theta \;\colon\; \{EL = 0\} \longrightarrow \mathbf{B}U(1)_{conn}$ to the [[smooth groupoid|smooth]] [[moduli stack]] of [[circle n-bundles with connection|circle bundles with connection]], and  the $G$-[[Hamiltonian action]] induced the [[action groupoid]] $\{EL = 0\} \longrightarrow \{EL = 0\}//G$; and the construction of the reduced [[prequantization]] is the construction of the diagonal [[morphism]] $\nabla_{red}$ in the following [[diagram]] (of [[smooth groupoids]])

$$
  \array{
    \{EL = 0\} &\stackrel{\theta}{\longrightarrow}& \mathbf{B}U(1)_{conn}
    \\
    \downarrow & \nearrow_{\nabla_{red}}
    \\
    \{EL = 0\}//G
  }
  \,.
$$

### For extended local Lagrangians

For $n$-dimensional [[field theory]], the [[local Lagrangian]] of the above dsicussion arises as the [[transgression]] of an $n$-form Lagrangian down in [[codimension]] $n$, a refinement discussed in more detail at _[[local prequantum field theory]]_. Such a Lagrangian may analogously be understood as being the [[principal infinity-connection|higher connection]] on a [[prequantum n-bundle]] which, in turn, maps to the ordinary [[prequantum bundle]] under [[transgression]]. Hence one may ask for a _universal_ or _extended_ [[equivariant structure]] already on this [[prequantum n-bundle]] which is such that under [[transgression]] (to any [[Cauchy surface]]) it induces an equivariant structure and hence a reduced phase space as above. 

Examples of such extended reduced phase space structures include:

* the [[universal Chern-Simons circle 3-connection]] 

* the [[universal Chern-Simons circle 7-connection]] 

and other examples discussed at _[[local prequantum field theory]]_.
## Related concepts

* [[symplectic reduction]]

* [[quantization commutes with reduction]]

* [[equivariant cohomology]]

* [[BV-BRST formalism]]

## References

Textbook account:


* [[Marc Henneaux]], [[Claudio Teitelboim]], §2.2.3 in: _[[Quantization of Gauge Systems]]_, Princeton University Press (1992) &lbrack;[ISBN:9780691037691](https://press.princeton.edu/books/paperback/9780691037691/quantization-of-gauge-systems), [jstor:j.ctv10crg0r](https://www.jstor.org/stable/j.ctv10crg0r)&rbrack;



See also the references at _[[quantization commutes with reduction]]_.

[[!redirects reduced phase spaces]]


