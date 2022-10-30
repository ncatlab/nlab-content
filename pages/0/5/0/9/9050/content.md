
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[Hodge theorem]] asserts, in particular, that for a [[compact topological space|compact]] [[Kähler manifold]], the canonical $(p,q)$-[[graded object|grading]] of its [[differential forms]] descends to its [[de Rham cohomology]]/[[ordinary cohomology]]. The resulting structure is called a _[[Hodge structure]]_, and is indeed the archetypical example of such.

## Definitions

+-- {: .num_defn}
###### Definition

Let $(X,g)$ be a [[compact topological space|compact]] [[oriented]] [[Riemannian manifold]] of [[dimension]] $d$. Write $\Omega^\bullet(X)$ for the [[de Rham complex]] of smooth [[differential form]]s on $X$ and $\star : \Omega^\bullet(X) \to \Omega^{d-\bullet}(X)$ for the [[Hodge star operator]].

The Hodge [[inner product]] 

$$
 \langle -,-\rangle : \Omega^\bullet(X) \otimes \Omega^{d-\bullet}(X)
  \to 
  \mathbb{R}
$$

is given by

$$
  \langle \alpha , \beta\rangle = \int_X \alpha \wedge \star \beta
  \,.
$$

Write $d^*$ for the formal [[adjoint]] of the de Rham differential under this iner product. Then

$$
  \Delta := [d,d^*] := d d^* + d^* d = (d + d^*)^2
$$

is the Hodge [[Laplace operator]] ($d + d^*$ is the corresponding [[Dirac operator]]). A [[differential form]] $\omega$ in the [[kernel]] of $\Delta$

$$
  \Delta \omega = 0
$$

is called a [[harmonic form]] on $(X,g)$.

Write $\mathcal{H}^k(X)$ for the [[abelian group]] of harmonic $k$-forms on $X$.

=--

## For Riemannian manifolds 
 {#ResultsOverRiemannianManifold}

+-- {: .num_prop}
###### Observation

Harmonic forms are precisely those in the kernel of $d + d^*$, which are precisely those in the joint kernel of $d$ and $d^*$.

=--

By the fact that the [[bilinear form]] $\langle -,-\rangle$ is non-degenerate. 

Therefore we have a canonical map $\mathcal{H}^k(X) \to H_{dR}^k(X)$ of harmonic forms into the [[de Rham cohomology]] of $X$.

+-- {: .num_theorem}
###### Theorem

The canonical map

$$
  \mathcal{H}^k(X) \to H_{dR}^k(X)
$$

is an [[isomorphism]].

=--

This means that every [[de Rham cohomology]] class on $(X,g)$ has precisely one harmonic cocycle reprentative.

But more is true

+-- {: .num_theorem}
###### Theorem

For $(X,g)$ as above, there exists a unique degree-preserving operator (the [[Green operator]] of the [[Laplace operator]] $\Delta$)

$$
  G : \Omega^\bullet(X) \to \Omega^\bullet(X)
$$

such that

* $G$ commutes with $d$ and with $d^*$;

* $G(\mathcal{H}^\bullet(X)) = 0$;

* and 
  
  $$
    Id - \pi_{\mathcal{H}} = [d, d^* G]
    \,,
  $$

  where $\pi_{\mathcal{H}}$ is the orthogonal projection on [[harmonic form]]s and the angular brackets denote the graded commutator $[d, d^* G] = [d,d^*]G = \Delta G$.

=--

See for instance page 6 of ([GreenVoisinMurre](#GreenVoisinMurre)).

## For K&#228;hler manifolds

(...)

## Related concepts

* [[Hodge-Maxwell theorem]]

* [[Hodge theory]], [[Hodge structure]]

* [[nonabelian Hodge theorem]]

* [[Poincaré lemma]]

* [[Stokes theorem]]

* [[de Rham theorem]]

* [[Dolbeault theorem]]

* [[Hodge conjecture]]



## References

The theorem is due to 

* [[William Hodge]], (1947)

A textbook account is for instance in seciton 1.1 of

* [[Chris Peters]], [[Jozef Steenbrink]], _[[Mixed Hodge Structures]]_, Ergebisse der Mathematik (2008) ([pdf](http://www.arithgeo.ethz.ch/alpbach2012/Peters_Steenbrinck))


Lecture notes include

* Xi Yin, _Notes on the Hodge Theorem_ ([pdf](http://www.people.fas.harvard.edu/~xiyin/hodge.pdf))

* [[Jonathan Evans]], _Hodge theorem_ ([pdf](http://www.homepages.ucl.ac.uk/~ucahjde/YM-lectures/lecture5.pdf))

See also

* Mark Green, [[Claire Voisin]], Jacob Murre, _Algebraic cycles and Hodge theory_ Lecture Notes in Mathematics, 1594 (1993)
{#GreenVoisinMurre}


[[!redirects Hodge's theorem]]
[[!redirects theorem of Hodge]]
