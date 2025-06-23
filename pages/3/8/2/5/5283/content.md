


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


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

There is a canonical bilinear pairing on multivector fields called the [[Schouten bracket]]. This makes mutlivector fields into a [[Gerstenhaber algebra]]. (Cf. [Roger 2009 §2.3.1](#Roger09), [VYL11 appd. A](#VYL11).)



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

A more general discussion of this phenomenon in ([Cattaneo–Fiorenza–Longoni](#CattaneoFiorenzaLongoni)). Even more generally, see [[Poincaré duality]] for [[Hochschild cohomology]].

### Integral sections

Just as for vector fields one has the notion of an [[flow of a vector field|integral curve]], so for $k$-vector fields one has a generalization known as **integral sections**. Given a $k$-vector field $X$ on a manifold $M$, and a point $p\in M$, an integral section is a map $\phi: U\subset \mathbb{R}^k \to M$ such that $\phi(0)=p$ and
$$
\phi_* (x) (\partial_{x^{\alpha}} \vert_x ) = X_{\alpha} (\phi(x))
$$ 

See e.g. Section 3.1 in [de León et al. 2015](#deLeon15) and the references cited therein for more.

## Related concepts

* [[bivector]]


## References

The isomorphisms between the de Rham complex and the complex of polyvector field is reviewed for instance on p. 3 of

* [[Thomas Willwacher]], [[Damien Calaque]], _Formality of cyclic cochains_ ([arXiv:0806.4095](http://arxiv.org/abs/0806.4095))
{#WillwacherCalaque}

and in section 2 of 

* [[Alberto Cattaneo]], [[Domenico Fiorenza]], Riccardo Longoni, _On the Hochschild-Kostant-Rosenberg map for graded manifolds_, [arXiv:math/0503380](https://arxiv.org/abs/math/0503380)
{#CattaneoFiorenzaLongoni}

and on p. 6 of 

* {#Roger09} [[Claude Roger]]: _Gerstenhaber and Batalin-Vilkovisky algebras_, Archivum mathematicum, [**45** (2009) 4](https://www.emis.de/journals/AM/09-4/) &lbrack;[abstract](https://www.emis.de/journals/AM/09-4/roger.html), [pdf](http://www.emis.de/journals/AM/09-4/roger.pdf)&rbrack;

See also:

* {#VYL11} Joris Vankerschaver, Hiroaki Yoshimura, Melvin Leok, appendix A of: *On the Geometry of Multi-Dirac Structures and Gerstenhaber Algebras*, J. Geom. Phys. **61** 8 (2011) 1415-1425 &lbrack;[arXiv:1102.2835](https://arxiv.org/abs/1102.2835), [doi:10.1016/j.geomphys.2011.03.005](https://doi.org/10.1016/j.geomphys.2011.03.005)&rbrack;


An exposition of multivector fields and their use in Lagrangian and Hamiltonian theories:

* {#deLeon15} Manuel De León, Modesto Salgado, Silvia Vilarino-Fernández. *Methods of differential geometry in classical field theories: k-symplectic and k-cosymplectic approaches*. World Scientific, 2015. ([arXiv:1409.5604](https://arxiv.org/abs/1409.5604)).

[[!redirects multivector field]]
[[!redirects multivector fields]]
[[!redirects multi-vector field]]
[[!redirects multi-vector fields]]
[[!redirects multi vector field]]
[[!redirects multi vector fields]]

[[!redirects multivector]]
[[!redirects multivectors]]

[[!redirects multi-vector]]
[[!redirects multi-vectors]]

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