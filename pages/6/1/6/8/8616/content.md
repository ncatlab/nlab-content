
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

For $f \colon X \to Y$ a [[smooth function]] between [[smooth manifold]], and for $\omega \in \Omega^n(Y)$ a [[differential n-form]], there is the _pullback_ $n$-form $f^* \omega \in \Omega^n(X)$.

### In terms of push-forward of vector fields

If differential forms are defined as linear duals to [[vectors]] then pullback is the dual operation to [[pushforward of a vector field]]

$$
  f^* \omega(v_1, \cdots, v_n) = \omega(f_* v_1, \cdots, f_* v_n)
  \,.
$$

### In terms of coordinate expression

Differential forms may be defined by [[Yoneda extension]] from differential forms on [[Cartesian spaces]] (see at _[[geometry of physics -- differential forms]]_). 

For $X = \mathbb{R}^{\tilde k}$ and $Y = \mathbb{R}^k$ [[Cartesian spaces]] and $f \;\colon\; X \longrightarrow Y$ a [[smooth function]] between them, and on [[differential 1-forms]]

$$
  \omega = \sum_{i = 1}^k \omega_i \mathbf{d}x^i
$$

the pullback operation $f^\ast$ is given by

$$
  f^* \mathbf{d}x^i
  \;\coloneqq\;
  \sum_{j = 1}^{\tilde k} \frac{\partial f^i}{\partial \tilde x^j} \mathbf{d}\tilde x^j
$$

and hence

$$
  f^* \omega = f^* \left( \sum_{i} \omega_i \mathbf{d}x^i \right)
  \coloneqq
  \sum_{i = 1}^k \left(f^* \omega\right)_i \sum_{j = 1}^{\tilde k} \frac{\partial f^i }{\partial \tilde x^j}  \mathbf{d} \tilde x^j 
  \,,
$$

where 

* $f^* \omega_i$ is the pullback of functions defined by 
   
  $$
    (f^* \omega_i)(x) = \omega_i(f(x)) \;\;\;\forall x \in X
  $$

* the function

  $$
    \frac{\partial f^i}{\partial \tilde x^j} \colon \mathbb{R}^{\tilde k} \to \mathbb{R}
  $$ 

  is the [[partial derivative]] of the $k$-th [[coordinate]] component of $f$ along the $j$the coordinate.

## Properties

### Compatibility with the de Rham differential


+-- {: .num_prop #CompatibilityWithDeRhamDifferential}
###### Proposition
**(compatiblity with the [[de Rham differential]])**

Pullback of differential forms commutes with the [[de Rham differential]]:

$$
  f^* \circ \mathbf{d}_Y = \mathbf{d}_X \circ f^*
  \,.
$$

Hence it constitutes a [[chain map]] between the [[de Rham complexes]]

$$
  f^* \colon \Omega^\bullet(Y) \to \Omega^\bullet(X)
  \,.
$$

=--

### Sheaf of differential forms

Under pullback differential forms form a [[presheaf]] on the catories [[CartSp]] and [[SmthMfd]], in fact a [[sheaf]] with respect to the standard [[open cover]]-[[coverage]].

## Related concepts


* [[change of integration variables]]


[[!include notions of pullback -- contents]]



## References

A standard reference is 

* Bott, Tu, _Differential forms in algebraic topology_.

See also for instance  

* [[Theodore Frankel]], Section 2.7 of _[[The Geometry of Physics - An Introduction]]_

[[!redirects pullbacks of a differential form]]

[[!redirects pullback of differential forms]]
[[!redirects pullbacks of differential forms]]

[[!redirects pullback form]]
[[!redirects pullback forms]]

[[!redirects pullback of functions]]
[[!redirects pullbacks of functions]]

[[!redirects pullback of a function]]
[[!redirects pullbacks of functions]]

