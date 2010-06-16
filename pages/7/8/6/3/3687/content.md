
#Contents#
* automatic table of contents goes here
{:toc} 

## Idea

To every complex 3-dimensional [[Calabi-Yau variety]] $X$ is associated a 2-dimensional [[sigma-model]] $N=2$-[[CFT|superconfomal field theory]] $SCFT(X)$. There is at least for some CY $X$ a map $X \mapsto \hat X$ which exchanges the [[Hodge number]]s $h^{1,1}$ and $h^{1,2}$ such that $SCFT(X)$ is expected to be equivalent to $SCFT(\hat X)$. 

$$
  SCFT(X) \simeq SCFT(\hat X)
  \,.
$$

This is called _mirror symmetry_ .

In this form mirror symmetry remains a conjecture, not the least because for the moment there is no complete construction of these SCFTs. But to every such $SCFT(X)$ one can associate two [[TCFT]]s, $A(X)$ and $B(X)$, the [[A-model]] and the [[B-model]]. These $N=1$ supersymmetric field theories were obtained by [[Edward Witten]] using a "topological twist". The topological A-model can be expressed in terms of [[symplectic geometry]] of a variety and the topological B-model can be expressed in terms of the [[algebraic geometry]] of a variety. 

These topological theories are easier to understand and do retain a little bit of the information encoded in the full SCFTs. In terms of these the statement of mirror symmetry says that passing to mirror CYs _exchanges_ the A-model with the $B$-model:

$$
  A(X) \simeq B(\hat X)
  \,.
$$

By a version of the [[cobordism hypothesis]]-theorem, these [[TCFT]]s (see there) are encoded by [[A-∞ categories]] that are [[Calabi-Yau categories]]: the [[A-model]] by the [[Fukaya category]] $Fuk(X)$ of $X$ which can be understood as a [[stable (∞,1)-category]] representing the Lagrangean intersection theory on the underlying [[symplectic manifold]]; and the [[B-model]] by an [[enhanced triangulated category|enhancement]] of the [[derived category]] of [[coherent sheaves]] $D^b_\infty(\hat X)$ on $\hat X$.

In terms of this data, mirror symmetry is the assertion that these [[A-∞ categories]] are equivalent

$$
  Fuk(X) \simeq D^b_\infty(\hat X)
  \,.
$$

This was conjectured by [[Maxim Kontsevich]] in 1994 and is now pretty much established. Kontsevich introduced the categorical variant in 1994 under the name **homological mirror symmetry**  and used the [[A-infinity-category|A∞-categories]] as a model for [[stable (∞,1)-categories]] in his work. 

The expression of mirror symmetry via $(\infty,1)$-categories is equivalent to the SCFT formulation according to the theorems of [[Maxim Kontsevich]] and independently by [[Kevin Costello]] (see [[TCFT]]) which reconstruct the quantum field theory from a [[Calabi-Yau category|Calabi-Yau A-infinity-category]]. 

The mirror symmetry conjecture roughly claims that every Calabi-Yau 3-fold has a mirror. In fact one considers (mirror symmetry for) degenerating families for Calabi-Yau 3-folds in large volume limit (what can be expressed precisely via the Gromov-Hausdorff metric). The appropriate definition of (an appropriate version of) the [[Fukaya category]] of a symplectic manifold is difficult to achieve in desired generality. 
Invariants/tools of Fukaya category include symplectic [[Floer homology]] and Gromov-Witten invariants (building up the [[quantum cohomology]]). Mirror symmetry is related to the [[T-duality]] on each fiber of an associated Lagrangian fibration (Strominger-Yau-Zaslow conjecture).  


## References

The original statement of the homological mirror symmetry conjecture is in

* [[Maxim Kontsevich]], _Homological algebra of mirror symmetry_, Proc. ICM Z&#252;rich 1994, [alg-geom/9411018](http://arxiv.org/abs/alg-geom/9411018)

A review and status report is in

* M. Ballard, _Meet homological mirror symmetry_ ([arxiv:0801.2014](http://arxiv.org/abs/0801.2014))


Other reviews include

* Paul Aspinwall, Tom Bridgeland, Alastair Craw, Michael R. Douglas, Mark Gross, _Dirichlet branes and mirror symmetry_, Amer. Math. Soc. Clay Math. Institute 2009. (very readable!)


The relation to [[T-duality]] was established in

* Andrew Strominger, Shing-Tung Yau, Eric Zaslow, _Mirror Symmetry is T-Duality_, Nucl.Phys.B479:243-259,1996 (DOI 10.1016/0550-3213(96)00434-8) [hep-th/9606040](http://arxiv.org/abs/hep-th/9606040)


* C. Vafa, S-T. Yau editors, _Winter school on mirror symmetry, vector bundles, and Lagrangian submanifolds_, Harvard 1999, AMS, Intern. Press (includes A. Strominger, S-T. Yau, E. Zaslow, _Mirror symmetry is $T$-duality_  as pages  333--347; ). 


* K. Hori, S. Katz, A. Klemm et al. _Mirror symmetry I_, AMS, Clay Math. Institute 2003.

* Paul Seidel, _Fukaya categories and Picard-Lefschetz theory_, Zurich Lectures in Advanced Mathematics. European Mathematical Society, Z&#252;rich, 2008. viii+326 pp

* Mark Gross, Bernd Siebert, _Mirror symmetry via logarithmic degeneration data I_, [math.AG/0309070](http://arxiv.org/abs/math/0309070), _From real affine geometry to complex geometry_, [math.AG/0703822](http://arxiv.org/abs/math/0703822), _Mirror symmetry via logarithmic degeneration data II_, [arxiv/0709.2290](http://arxiv.org/abs/0709.2290) 

* Maxim Kontsevich, Yan Soibelman, _Homological mirror symmetry and torus fibrations_, [math.SG/0011041](http://arxiv.org/abs/math/0011041)

* Yong-Geun Oh, Kenji Fukaya, _Floer homology in symplectic geometry and
mirror symmetry_, Proc. ICM 2006, [pdf](http://www.math.wisc.edu/~oh/Oh-icm2006.pdf)




* wikipedia: [mirror symmetry (string theory)](http://en.wikipedia.org/wiki/Mirror_symmetry_%28string_theory%29), [homological mirror symmetry](http://en.wikipedia.org/wiki/Homological_mirror_symmetry)

### Complete proofs {#CompleteProofs}

Here is a list with references that give complete proofs of homological mirror symmetry on certain (types of) spaces.

* M. Abouzaid, I. Smith, _Homological mirror symmetry for the four-torus_ ([arXiv:0903.3065](http://arxiv.org/abs/0903.3065))

* A. Polishchuk and E. Zaslow, _Categorical mirror symmetry: the elliptic curve_ , Adv. Theor. Math. Phys., 2:443470, 1998.

* P. Seidel, _Homological mirror symmetry for the quartic surface_ ([arXiv:0310414](http://arxiv.org/abs/math/0310414))

* Alexander I. Efimov, _Homological mirror symmetry for curves of higher genus_ ([arXiv:0907.3903](http://arxiv.org/abs/0907.3903))

[[!redirects homological mirror symmetry]]