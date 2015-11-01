
# Contents
* table of contents
{:toc}

## Definition

For $X$ a [[smooth manifold]] and $T X$ its [[tangent bundle]] a **multivector field** on $X$ is an element of the [[exterior algebra]] bundle $\wedge^\bullet_{C^\infty(X)}(\Gamma(T X))$ of skew-symmetric [[tensor power]]s of [[section]]s of $T X$.

* In degree $0$ these are simply the [[smooth function]]s on $X$.

* In degree $1$ these are simply the [[tangent vector field]]s on $X$.

* In degree $p$ these are sometimes called the __$p$-vector fields__ on $X$.


## Properties

### Hochschild cohomology

In suitable contexts, multivector fields on $X$ can be identified with the [[Hochschild cohomology]] $HH^\bullet(C(X), C(X))$ of the algebra of functions on $X$.


### Schouten bracket

There is a canonical bilinear pairing on multivector fields called the [[Schouten bracket]].

### Isomorphisms with de Rham complex

Let $X$ be a [[smooth manifold]] of [[dimension]] $d$, which is equipped with an [[orientation]] exhibited by a [[differential form]]
$\omega \in \Omega^d(X)$.

Then contraction with $\omega$ induces for all $0 \leq n \leq d$ an [[isomorphism]] of [[vector space]]s

$$
  \omega(-) : 
  T^n_{poly}(X)
    \stackrel{\simeq}{\to}
  \Omega^{(d-n)}(X)
  \,.
$$

The transport of the [[de Rham complex|de Rham differential]] along these isomorphism equips $T^\bullet_{poly}$ with the structure of a [[chain complex]]

$$
  \array{
    \Omega^{n}(X) &\stackrel{d_{dR}}{\to}& \Omega^{n+1}(X)
    \\
    \downarrow^{\mathrlap{\simeq}}
      &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    T^{d-n}_{poly} &\stackrel{div_\omega}{\to}&
    T^{d-n-1}_{poly} 
  }
  \,,
$$

The operation $div_\omega$ is a [[derivation]] of the [[Schouten bracket]] and makes multivectorfields into a [[BV-algebra]].

A more general discussion of this phenomenon in ([CattaneoFiorenzaLongoni](CattaneoFiorenzaLongoni)). Even more generally, see [[Poincaré duality]] for [[Hochschild cohomology]].


## References

The isomorphisms between the de Rham complex and the complex of polyvector field is reviewed for instance on p. 3 of

* Thomas Willwacher, Damien Calaque _Formality of cyclic cochains_ ([arXiv:0806.4095](http://arxiv.org/abs/0806.4095))
{#WillwacherCalaque}

and in section 2 of 

* [[Alberto Cattaneo]], [[Domenico Fiorenza]], Riccardo Longoni, _On the Hochschild-Kostant-Rosenberg map for graded manifolds_ ([pdf](http://www.math.uzh.ch/fileadmin/math/preprints/05-06.pdf))
{#CattaneoFiorenzaLongoni}

and on p. 6 of 

* [[Claude Roger]], _Gerstenhaber and Batalin-Vilkovisky algebras_, Archivum mathematicum, Volume 45 (2009), No. 4 ([pdf](http://www.emis.de/journals/AM/09-4/roger.pdf))


[[!redirects multivector field]]
[[!redirects multivector fields]]
[[!redirects multi-vector field]]
[[!redirects multi-vector fields]]
[[!redirects multi vector field]]
[[!redirects multi vector fields]]

[[!redirects tangent p-vector field]]
[[!redirects tangent p-vector fields]]

[[!redirects p-vector field]]
[[!redirects p-vector fields]]

[[!redirects polyvector field]]
[[!redirects polyvector fields]]
[[!redirects poly-vector field]]
[[!redirects poly-vector fields]]
[[!redirects poly vector field]]
[[!redirects poly vector fields]]