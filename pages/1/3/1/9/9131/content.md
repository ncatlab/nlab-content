
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

In [[Lagrangian field theory]] a _[[field history]]_ is a [[section]] of some [[fiber bundle]] $E \overset{fb}{\to} \Sigma$ over [[spacetime]]/[[worldvolume]] $\Sigma$. This is then called the _field bundle_.

The [[de Rham complex]] of the [[jet bundle]] of the field bundle, equipped with its canonical horizontal/vertical bigrading, is the _[[variational bicomplex]]_ of the [[Lagrangian field theory]].

For more see at _[[A first idea of quantum field theory]]_ the chapter _[Fields](A+first+idea+of+quantum+field+theory#Fields)_.

+-- {: .num_remark}
###### Remark

The notion of field bundle captures only some aspects of the general notion of spaces of physical fields. For instance the configurations of the _[[B-field]]_ do not form sections of a fiber bundle (but of a [[fiber infinity-bundle|fiber 2-bundle]]) and hence for instance the [magnetic charge anomaly](magnetic+charge#MagneticChargeAnomaly) has no real description by field bundles. See at _[[field (physics)]]_ in the section _[The idea of field bundles and its problems](field+%28physics%29#IdeaOfFieldBundlesAndItsProblems)_ for more.

=--

## Examples

+-- {: .num_example}
###### Example

For $E \to X$ the trivial bundle $X \times \mathbb{R} \to X $ or $X \times \mathbb{C} \to X$ a smooth section is simply a [[smooth function]] on $X$ with values in the [[real numbers]] or [[complex numbers]], respectively. In [[physics]] this is called a _[[scalar field]]_.

=--

+-- {: .num_example}
###### Example

More generally, for $V$ a [[vector space]], the trivial field bundle $X \times V \to X$ has as secton $V$-valued functions. These are also called _linear [[sigma-model]]_ fields.

Still more generally, if $Y$ is any manifold, then the sections of the trivial field bundle $X \times Y \to X$ are called _non-linear [[sigma-model]]_ fields.

=--


+-- {: .num_example}
###### Example

For $X$ a [[smooth manifold]] and $E \to X$ some [[tensor product]] of copies of the [[tangent bundle]] $T X \to X$ and the [[cotangent bundle]] $T^* X \to X$ a section is a [[tensor field]] of the corresponding rank.

Many physical fields are related to tensor fields, but few are genuinely tensor fields. See at _[[field (physics)]]_ for more on this. 

=--

## Related concepts

* [[fiber bundles in physics]]

* [[field (physics)]]

* [[extended phase space]]

## References

The traditional idea of field bundle is discussed for instance around section 7.3.3 of 

* Laurent Claessens, _Field theory from a bundle point of view_ (2011) ([pdf](http://student.ulb.ac.be/~lclaesse/lectures.pdf)).

Detailed discussion of field bundles in [[gauge theory]] with a fixed [[instanton sector]]/[[principal bundle]]-class is around section 2.5 of 

* {#BDS} [[Marco Benini]], [[Claudio Dappiaggi]], [[Alexander Schenkel]]: *Quantized Abelian principal connections on Lorentzian manifolds*,  Commun. Math. Phys. **330** (2014) 123–152 &lbrack;[arXiv:1303.2515](http://arxiv.org/abs/1303.2515), [doi:10.1007/s00220-014-1917-0](https://doi.org/10.1007/s00220-014-1917-0)&rbrack;

and the issue is highlighted more explicitly in 

* {#Schenkel14} [[Alexander Schenkel]], _On the problem of gauge theories in locally covariant QFT_, talk at _[Operator and Geometric Analysis on Quantum Theory](http://www.science.unitn.it/~moretti/convegno/convegno.html)_ Trento, 2014 ([[SchenkelTrento2014.pdf:file]]) 

* {#Schreiber14} [[Urs Schreiber]], _Higher field bundles for gauge fields_, talk at _[Operator and Geometric Analysis on Quantum Theory](http://www.science.unitn.it/~moretti/convegno/convegno.html)_ Trento, 2014 ([[schreiber:Higher field bundles for gauge fields|web]])

The issue was then fixed in 

* {#BeniniSchenkelSzabo15} [[Marco Benini]], [[Alexander Schenkel]], [[Richard Szabo]], _Homotopy colimits and global observables in Abelian gauge theory_ ([arXiv:1503.08839](http://arxiv.org/abs/1503.08839))

precisely by retaining to groupoids/stacks of fields, hence using a higher stacky field bundle.

A discussion of the problems of the traditional notion and its rectification in [[higher geometry]] is at

* section _[Fields](geometry%20of%20physics#Fields)_ of _[[geometry of physics]]_

[[!redirects field bundles]]

[[!redirects field fiber]]
[[!redirects field fibers]]
