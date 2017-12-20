
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--

#Moduli space of curves and#
* table of contents
{:toc}

## Idea

The [[moduli space]]/[[moduli stack]] of [[algebraic curves]]/[[Riemann surfaces]] is a sort of space of parameters parametrizing [[algebraic curves]] of given [[genus]].

[Deligne-Mumford 69](#DeligneMumford69) a nontrivial [[compactification]] of a moduli space of Riemann surfaces of fixed genus which is a [[Deligne-Mumford stack]], since called the _[[Deligne-Mumford compactification]]_.

There is also a decorated version of curves with marked points, and
of the corresponding compactified moduli space of stable curves of genus $g$ with $n$ marked points $\mathcal{M}_{g,n}$ which plays an important role in the mathematical study of [[Gromov-Witten invariants]] and of [[conformal blocks]].

The special case of $g = 1$, $n =1$ is the [[moduli stack of elliptic curves]] $\mathcal{M}_{1,1}= \mathcal{M}_{ell}$.

## Properties

### Over the complex numbers
  {#OverTheComplexNumbers}


+-- {: .num_remark #EquivalentlyModuliOfAlmostComplexStructures}
###### Remark

On 2-[[dimension|dimensional]] [[manifold]] every [[almost complex structure]] is integrable and hence is already a [[complex structure]] (see [this proposition](complex+structure#In2dAnyAlmostComplexStructureIsIntegrable)).

Hence the moduli space of complex surfaces is also equivalent to just the [[quotient orbifold]] of the space of [[almost complex structures]] by the orientation-preserving part of the [[diffeomorphism group]].

=--


This is reviewed for instance in ([Madsen 07, section 1.1](#Madsen07)).

+-- {: .num_remark #InTermsOfTheHigherToposOfSmoothStacks}
###### Remark

We indicate how via remark \ref{EquivalentlyModuliOfAlmostComplexStructures} the moduli space of complex curves has a formulation in the [[homotopy type theory|homotopy-type theory]] $\mathbf{H}$ of [[smooth homotopy types]].

By the discussion at _[[almost complex structure]]_ (see [this remark](complex+structure#InTermsOfSmoothStacks)), if the [[tangent bundle]] of a $2n$-dimensional [[smooth manifold]] is modulated by a map

$$
  \tau_X \;\colon\;  X \longrightarrow \mathbf{B}GL(2n,\mathbb{R})
$$ 

to the [[delooping]] in [[smooth stacks]] of the [[general linear group]], then an [[almost complex structure]] on $X$ is equivalently a lift $J$ in 

$$
  \array{
     X && \stackrel{J}{\longrightarrow} && \mathbf{B} GL(n,\mathbb{C})
     \\
     & {}_{\mathllap{\tau}}\searrow && \swarrow_{\mathrlap{almComp}}
     \\
     && \mathbf{B} GL(2n,\mathbb{R})
  }
  \,.
$$

This in turn is equivalently a map 

$$
  J \;\colon\; \tau_X \longrightarrow almComp
$$

in the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}GL(2n,\mathbb{R})}$, hence with the canonical empedding

$$
  \tau_{(-)} \;\colon\; SmthMfd_{2n}^{et} \hookrightarrow \mathbf{H}_{/\mathbf{B}GL(2n,\mathbb{R})}
$$

of the category of [[smooth manifolds]] with [[local diffeomorphisms]] between them
understood, then $almComp \in \mathbf{H}_{/\mathbf{B}GL(2n,\mathbb{R})}$ is the universal [[moduli stack]] of [[almost complex structures]].

Now $\tau_X$ carries a canonical [[∞-action]] by the [[diffeomorphism group]]. Using this one may canonically form the [[homotopy quotient]]

$$
  [\tau_X, almComp]//Diff(X)
$$

by a general abstract construction that is discussed in some detail at _[general covariant -- Formalization in homotopy type theory](general+covariance#InHomotopyTypeTheory)_. For $n =1$ this is hence the Riemann moduli space.

=--


### Homotopy type and cohomology
 {#HomotopyTypeAndCohomology}

The [[homotopy type]] of the Riemann moduli spaces $\mathcal{M}_g$ (i.e. of the [[geometric realization]] of the [[orbifold]], hence essentially of the delooping of the [[mapping class group]]) is essentially unknown.  Even its [[orbifold cohomology]] over the [[rational numbers]] is fully known only for $g \leq 4$.

However, in a stable range it has been fully computed in ([Madsen-Weiss 02](#MadsenWeiss02)), proving what was previously [[conjecture|conjectured]] by [[Mumford's conjecture]]. A review is in ([Madsen 07](#Madsen07)).



### Orbifold Euler characteristic
 {#OrbifoldEulerCharacteristic}

The [[orbifold Euler characteristic]] $\chi$ of $\mathcal{M}_{g,1}$ is given by the [[Riemann zeta function]] at negative integral values  as follows ([Zagier-Harer 86](#ZagierHarer86)):

$$
  \chi(\mathcal{M}_{g,1}) = \zeta(1-2g)
  \,.
$$

By the expression of the [[Riemann zeta function]] at negative integral values by the [[Bernoulli numbers]] $B_n$, this says equivalently that

$$
  \chi(\mathcal{M}_{g,1}) = -\frac{B_{2g}}{2g}
  \,.
$$

For instance for $g = 1$ (once punctured complex [[tori]], hence complex [[elliptic curves]]) this yields

$$
  \chi(\mathcal{M}_{1,1}) = -\frac{1}{12}
$$

for the [[orbifold Euler characteristic]] of the [[moduli space of elliptic curves]].

### Relation to Teichm&#252;ller space

Over the complex number then the moduli space of curves is a quotient of _[[Teichmüller space]]_. ([Hubbard-Koch 13](#HubbardKoch13))


## Examples

### $g = 0$, $n = 0$

By the [[Riemann mapping theorem]], $\mathcal{M}_{0,0}\simeq \ast$ is the point.

### $g = 1$, $n = 0$

$\mathcal{M}_{1,0} \simeq \mathbb{R}^2$

### $g = 1$, $n = 1$

$\mathcal{M}_{1,1} = \mathcal{M}_{ell}$, the [[moduli stack of elliptic curves]].

### $g \geq 2$, $n = 0$

For [[genus]] $g\geq 2$ the moduli stack of [[complex structures]] is equivalently that of [[hyperbolic metrics]]. This way a lot of [[hyperbolic geometry]] is used in the study of $\mathcal{M}_{g \geq 2, n}$.


## Related entries

* [[moduli space]], [[moduli stack]], [[mapping class group]], [[enumerative geometry]], [[Mumford class]], [[Deligne-Mumford stack]]

* [[moduli space of (higher) line bundles]]

* [[Witten conjecture]]


## References

Original articles include

* {#DeligneMumford69} [[Pierre Deligne]], [[David Mumford]], _The irreducibility of the space of curves of given genus_, Publications Math&#233;matiques de l'IH&#201;S (Paris) 36: 75&#8211;109 (1969) [numdam](http://www.numdam.org/numdam-bin/fitem?id=PMIHES_1969__36__75_0)

* [[David Mumford]], _Towards an enumerative geometry of the moduli space of curves_, Arithmetic and geometry, Vol. II, Birkh&#228;user Boston, Boston, MA, 1983, pp. 271&#8211;328, [MR85j:14046](http://www.ams.org/mathscinet-getitem?mr=85j:14046)

Discussion of the [[orbifold cohomology]] of the moduli stack is in

* John Harer, _The cohomology of the moduli space of curves_, Lec. Notes in Math. 1337, p. 138&#8211;221. Springer, Berlin, 1988.

The stable rational [[orbifold cohomology]] of the moduli stack was computed in

* {#MadsenWeiss02} [[Ib Madsen]], [[Michael Weiss]], _The stable moduli space of Riemann surfaces: [[Mumford's conjecture]]_,  Ann. of Math. (2) __165__ (2007), no. 3, 843--941, [MR2009b:14051](http://www.ams.org/mathscinet-getitem?mr=2009b:14051), [doi](http://dx.doi.org/10.4007/annals.2007.165.843), [math.AT/0212321](http://arxiv.org/abs/math.AT/0212321)

exposition of this is in

* {#Madsen07} [[Ib Madsen]], _Moduli spaces from a topological viewpoint_, Proceedings of the International Congress of Mathematics, Madrid 2006 (2007) ([pdf](http://www.icm2006.org/proceedings/Vol_I/20.pdf))

See also

* Gabriele Mondello, _Combinatorial classes on $\mathcal{M}_{g,n}$ are tautological_, Int. Math. Res. Not. __44__ (2004), 2329-&#8211;2390, [MR2005g:14056](http://www.ams.org/mathscinet-getitem?mr=2005g:14056), [doi](http://dx.doi.org/10.1155/S1073792804131462), [math.AG/0303207](http://arxiv.org/abs/math/0303207)

* Gabriele Mondello, _Riemann surfaces, ribbon graphs and combinatorial classes_, in: Handbook of Teichm&#252;ller theory. Vol. II,  151--215, IRMA Lect. Math. Theor. Phys., 13, Eur. Math. Soc., Z&#252;rich, 2009; draft with index: [pdf](http://www.mat.uniroma1.it/~mondello/me/papers/ober-definitive.pdf), arxiv version [math.AG/0705.1792](http://arxiv.org/abs/0705.1792), [MR2010f:32012](http://www.ams.org/mathscinet-getitem?mr=2010f:32012)

* [[Alastair Hamilton]], _Classes on compactifications of the moduli space of curves through solutions to the quantum master equation_, Lett. Math. Phys. __89__  (2009), no. 2, 115--130.

* _The moduli of curves_ [pdf](http://www2.imperial.ac.uk/~acorti/download/moduli.pdf)

The [[orbifold Euler characteristic]] of the moduli space of curves was originally computed in

* {#ZagierHarer86} [[Don Zagier]], John Harer, _The Euler characteristic of the moduli space of curves_, Inventiones mathematicae (1986) Volume: 85, page 457-486 ([EUDML](https://eudml.org/doc/143377))

The complex analytic structure and the relation to [[Teichmüller space]] is further discussed in

* {#HubbardKoch13} [[John Hubbard]], [[Sarah Koch]], _An analytic construction of the Deligne-Mumford compactification of the moduli space of curves_ ([arXiv:1301.0062](http://arxiv.org/abs/1301.0062)) 

Reviews include

* _Mathematical ideas and notions in quantum field theory -- 5. The Euler characteristic of the moduli space of curves_ ([[EulerCharacteristicOfSpaceOfCurves.pdf:file]])

[[etale homotopy type|Étale homotopy type]] of moduli stacks of curves is discussed in

* Paola Frediani, Frank Neumann, _&#201;tale homotopy types of moduli stacks of algebraic curves with symmetries_, K-Theory 30: 315-340, 2003 ([arXiv:math/0404387](http://arxiv.org/abs/math/0404387))


[[!redirects moduli spaces of curves]]

[[!redirects moduli space of Riemann surfaces]]
[[!redirects moduli spaces of Riemann surfaces]]

[[!redirects moduli space of complex curves]]
[[!redirects moduli spaces of complex curves]]
[[!redirects moduli stack of complex curves]]
[[!redirects moduli stacks of complex curves]]


[[!redirects moduli stack of curves]]
[[!redirects moduli stacks of curves]]

[[!redirects moduli stack of Riemann surfaces]]
[[!redirects moduli stacks of Riemann surfaces]]

[[!redirects moduli stack of algebraic curves]]
[[!redirects moduli stacks of algebraic curves]]

[[!redirects Riemann moduli space]]
[[!redirects Riemann moduli spaces]]

[[!redirects moduli space of punctured curves]]
[[!redirects moduli spaces of punctured curves]]
