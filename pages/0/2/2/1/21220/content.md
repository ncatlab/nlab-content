
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a [[symmetry group]] $G$ equipped with a [[homomorphism]] $G \overset{\phi}{\longrightarrow} O(s,t)$ to an [[orthogonal group]] (for instance a [[Pin group]]), a  _pseudoscalar_ is an element of the 1-dimensional [[linear representation]] (over a given [[ground field]] $k$) 

$$
  \mathbf{1}_{{}_{sgn}}
  \;\in\;
  Rep_k(G)
$$

that is given by forming the [[determinant]] ([[sign representation]]):

\[
  \label{DeterminantRepresentation}
  \mathbf{1}_{{}_{sgn}}
  \;\;\coloneqq\;\;
  \left(
  \array{
    G \times k
    &\longrightarrow&
    k
    \\
    (g, c ) &\mapsto& det\big( \phi(g) \big)
  }
  \right)
  \,.
\]

More generally, given a [[function]] with values in $\mathbf{1}_{{}_{sgn}}$, or yet more generally a [[section]] of a [[fiber bundle]] with [[typical fiber]] $\mathbf{1}_{{}_{sgn}}$, this whole function/section is often called a _pseudoscalar_; more precisely: a _pseudoscalar [[field (physics)|field]]_. 
This as opposed to [[scalar fields]], which take values in the 1-dimensional [[trivial representation]] $\mathbf{1}$.

If the [[fiber bundle]] in question is a "[[canonical bundle]]"/[[determinant line bundle]] of a [[Riemannian manifold]] of [[dimension]] $n$, hence the top [[exterior power]] of a [[tangent bundle]] (i.e. top degree ([[Kähler differential form|Kähler]]) [[differential form]]-bundle) then such "pseudoscalar fields" of [[physics]] are what are called _[[densities]]_ in [[mathematics]].

## Related concepts

* The [[tensor product of representations]] of any type $X$ of representations with a [[determinant]]/[[sign representation]] (eq:DeterminantRepresentation) is often called a "pseudo-X representation". For instance of $X$ is "[[vector representation]]" then we get [[pseudovector representation]], etc.

* [[scalar]], [[scalar field]]

* [[density]], [[determinant line bundle]]


## References

See also

* Wikipedia, _[Pseudoscalar](https://en.wikipedia.org/wiki/Pseudoscalar)_

[[!redirects pseudoscalars]]

[[!redirects pseudo-scalar]]
[[!redirects pseudo-scalars]]

[[!redirects pseudoscalar representation]]
[[!redirects pseudoscalar representations]]
[[!redirects pseudo-scalar representation]]
[[!redirects pseudo-scalar representations]]

[[!redirects pseudoscalar field]]
[[!redirects pseudoscalar field]]
[[!redirects pseudo-scalar field]]
[[!redirects pseudo-scalar field]]


