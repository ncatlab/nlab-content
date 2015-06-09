
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Given a [[symplectic vector space]] $(V,\omega)$ one may consider the restriction of its [[quantomorphism group]] to the [[affine symplectic group]] $ASp(V,\omega)$ ([Robbin-Salamon 93, corollary 9.3](#RobbinSalamon93))

$$
  \array{
     ESp(V,\omega) &\hookrightarrow& QuantMorph(V,\omega)
     \\
     \downarrow && \downarrow
     \\
     ASp(V,\omega)
     &\hookrightarrow&
     HamSympl(V,\omega)
  }
$$

Sometimes (e.g. [Robbin-Salamon 93, p. 30](#RobbinSalamon93)) this $ESp(V,\omega)$ is called the _extended symplectic group_, but maybe to be more specific one should at the very least say "[[extended affine symplectic group]]" or "extended inhomogeneous symplectic group" ([ARZ 06, prop. V.1](#ARZ06)). 

Notice that the further restriction to $V$ regarded as the [[translation group]] over itself is the [[Heisenberg group]] $Heis(V,\omega)$

$$
  \array{
     Heis(V,\omega)
     &\hookrightarrow&
     ESp(V,\omega) &\hookrightarrow& QuantMorph(V,\omega)
     \\
     \downarrow && \downarrow && \downarrow
     \\
     V
     &\hookrightarrow&
     ASp(V,\omega)
     &\hookrightarrow&
     HamSympl(V,\omega)
  }
$$

The group $ESp(V,\omega)$ is that of those [[quantomorphisms]] which come from [[Hamiltonians]] that are [[quadratic Hamiltonians]]. Those elements covering elements in the [[symplectic group]] instead of the [[affine symplectic group]] come from [[homogeneously quadratic Hamiltonians]] (e.g. [Robbin-Salamon 93, prop. 10.1](#RobbinSalamon93)). In fact $ESp$ is the [[semidirect product]] of the [[metaplectic group]] $Mp(V,\omega)$ with the [[Heisenberg group]] ([ARZ 06, prop. V.1](#ARZ06), see also [Low 12](#Low12))

$$
  ESp(V,\omega) \simeq Heis(V,\omega) \rtimes Mp(V,\omega)
  \,.
$$

## Example


Let $(V,\omega) = (\mathbb{R}^2, \mathbf{d}p\wedge \mathbf{d}q)$
be the 2-dimensional [[symplectic vector space]].

Write

$$
  q,p \colon \mathbb{R}^2 \longrightarrow \mathbb{R}
$$

for its two canonical coordinates functions (the "[[canonical coordinates]] and [[canonical momenta]]").

Write 

$$
  i \colon \mathbb{R}^2 \longrightarrow \mathbb{R}
$$

for the [[constant function]] with value 1. 

The [[Poisson bracket]] is

$$
  \{p.q\} = i 
  \,.
$$

Any [[smooth function]] $H \colon \mathbb{R}^2 \to \mathbb{R}$ we may call a [[Hamiltonian]]. Given a Hamiltonian $H$, its [[Hamiltonian flow]] is the [[flow]] given by the [[vector field]] (the [[Hamiltonian vector field]]) corresponding to the [[derivation]] $\{H,-\}$ on $C^\infty(\mathbb{R}^2)$.

Those Hamiltonians whose Hamiltonian flows are [[linear functions]] on $\mathbb{R}^2$ are precisely the [[homogeneously quadratic Hamiltonians]]:


$$
  \exp(t\{\tfrac{1}{2}p^2,-\}) 
  \colon 
  \left[
    \array{  
       q 
       \\
       p
    }
  \right]
  \mapsto
  \left[
    \array{
       q +t p 
       \\
       p
    }
  \right]
$$

$$
  \exp(\{\tfrac{1}{2}q^2,-\}) 
  \colon 
  \left[
    \array{  
       q
       \\
       p
    }
  \right]
  \mapsto
  \left[
    \array{
       q 
       \\
       p + t q
    }
  \right]
$$

$$
  \exp(t \{q p,-\}) 
  \colon 
  \left[
    \array{  
       q
       \\
       p
    }
  \right]
  \mapsto
  \left[
    \array{
       e^t q 
       \\
       e^{-t} p
    }
  \right]
$$

The general element of the [[metaplectic group]] $Mp(\mathbb{R}^2,\mathbf{d}q \wedge \mathbf{d}p)$ is hence


$$
  \exp(t_1 \tfrac{1}{2}p^2 + t_2 \tfrac{1}{2}q^2 + t_3 q p)
$$

By [[differentiation|differentiating]] this by $t$ at $t = 0$ we obtain a [[basis]] for the [[Lie algebra]]  $\mathfrak{sp}(V,\omega)$ of, both, the [[symplectic group]] $Sp(V,\omega)$ as well as its [[metaplectic group]] $Mp(V,\omega)$

$$
  \left[
    \array{
      0 & 0
      \\
      1 & 0
    }
  \right]
  \,,
  \;\;\;
  \left[
    \array{
       0 & 1
       \\
       0 & 0
     }
  \right]
  \,,
  \;\;\;
  \left[
     \array{
       1 & 0
       \\
       0 & -1
     }
  \right]
$$

The Hamiltonians that generate translations are precisely the homogeneously linear Hamiltonians:

$$
  \exp(t\{p,-\}) 
  \colon 
  \left[
    \array{  
       q
       \\
       p
    }
  \right]
  \mapsto
  \left[
    \array{
       q + t
       \\
       p
    }
  \right]
$$

$$
  \exp(t\{q,-\}) 
  \colon 
  \left[
    \array{  
       q
       \\
       p
    }
  \right]
  \mapsto
  \left[
    \array{
       q 
       \\
       p - t
    }
  \right]
$$

This is the key point where the extension appears: While these two linear translation operations themselves (i.e. the underlying [[symplectomorphisms]]) of course commute with each other, their generating Hamiltonians do not Poisson commute but instead form the [[Heisenberg algebra]] extension of the [[translation group]].

The general element of the extended affine symplectic group $ESp(\mathbb{R}^2, \mathbf{d}q \wedge \mathbf{d}p)$ is 

$$
  \exp(t_1 \tfrac{1}{2}p^2 + t_2 \tfrac{1}{2}q^2 + t_3 q p + t_4 p + t_5 q + t_6 i)
  \,.
$$


## References

* {#RobbinSalamon93} [[Joel Robbin]],  [[Dietmar Salamon]], _Feynman path integrals on phase space and the metaplectic representation_, Math. Z. __221__ (1996), no. 2, 307&#8211;-335, ([MR98f:58051](http://www.ams.org/mathscinet-getitem?mr=98f:58051), [doi](http://dx.doi.org/10.1007/BF02622118), [[RobbinSalamonMetaplectic.pdf:file]]), also  in [[Dietmar Salamon]] (ed.), _Symplectic Geometry_, LMS Lecture Note series 192 (1993) 

* {#ARZ06} [[Sergio Albeverio]], J. Rezende and J.-C. Zambrini, _Probability and Quantum Symmetries. II. The Theorem of Noether in quantum mechanics_, Journal of Mathematical Physics 47, 062107 (2006) ([pdf](http://gfm.cii.fc.ul.pt/people/jczambrini/JMathPhys-47-062107.pdf))

* {#Low12} Stephen G. Low, _Maximal quantum mechanical symmetry: Projective representations of the inhomogenous symplectic group_, J. Math. Phys. 55, 022105 (2014) ([arXiv:1207.6787](http://arxiv.org/abs/1207.6787))

[[!redirects extended inhomogeneous symplectic group]]