
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The [[special orthogonal group]] in [[dimension]] 3.

## Properties

### Cohomology

+-- {: .num_prop }
###### Proposition

The [[integral cohomology|integral]] [[cohomology ring]] of the [[classifying space]] [[BSO(n)|$B SO(3)$]] is

$$
  H^\bullet\big( 
    B SO(3), \mathbb{Z}
  \big) 
  \;\simeq\;
  \mathbb{Z}\big[ p_1, W_3\big] / (2 W_3)
  \,,
$$ 

where 

* $p_1 \in H^4\big(B SO(3), \mathbb{Z}\big)$ is the [[universal characteristic class|universal]] [[first Pontryagin class]];

* $W_3 = \beta(w_2) \in H^3\big( B SO(3), \mathbb{Z}\big)$ is the [[universal characteristic class|universal]] degree-3 [[integral Stiefel-Whitney class]].

=--

This is a special case of [Brown 82, theorem 1.5](#Brown82), which is also reviewed as [Rudolph-Schmidt 17, Thm. 4.2.23 with Remark 4.2.25](#RudolphSchmidt17).


\linebreak

### Finite subgroups

+-- {: .num_theorem #ClassificationOfFiniteSubgroupsOfSO3}
###### Theorem
**([[ADE classification]] of [[finite group|finite]] [[subgroups]] of [[SO(3)]] and [[spin group|Spin(3)]]$\simeq$ [[SU(2)]])**

The [[finite group|finite]] [[subgroups]] of the [[special orthogonal group]] $SO(3)$ as well as the [[finite group|finite]] [[subgroups]] of the [[special unitary group]] [[SU(2)]] are, up to [[conjugation]], given by the following classification:

[[!include ADE -- table]]


Here under the [[double cover]] projection (using the [exceptional isomorphism](spin+group#ExceptionalIsomorphisms) $SU(2) \simeq Spin(3)$)

$$
  SU(2) \simeq Spin(3) \overset{\pi}{\longrightarrow} SO(3)
$$

all the finite subgroups of $SU(2)$ except the [[odd number|odd]]-[[order of a group|order]] [[cyclic groups]] are the [[preimages]] of the corresponding finite subgroups of $SO(3)$, in that we have [[pullback]] [[diagrams]]

$$
  \array{
    \left\langle
     \exp
     \left(
       \pi \mathrm{i} \tfrac{1}{n} 
     \right)
    \right\rangle
    &
    =
    &
    \mathbb{Z}/(2n)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    Spin(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    Spin(3)
    \\
    &&
    \big\downarrow
    &{}^{(pb)}&
    \big\downarrow
    &{}^{(pb)}&
    \big\downarrow^{ \mathrlap{\pi} }
    \\
    \left\langle
     Ad_{
     \exp
     \left(
       \pi \mathrm{i} \tfrac{1}{n} 
     \right)
     }
    \right\rangle
    &
    =
    &
    \mathbb{Z}/n
    &\overset{\phantom{AA}}{\hookrightarrow}&
    SO(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    SO(3)    
  }
$$

exhibiting the [[even number|even]] [[order of a group|order]] [[cyclic groups]] as subgroups of [[Spin(2)]], including the the minimal case of the [[group of order 2]]

$$
  \array{
    \left\langle
     \exp
     \left(
       \pi \mathrm{i}
     \right)
     =
     -1
    \right\rangle
    &
    =
    &
    \mathbb{Z}/2
    &\overset{\phantom{AA}}{\hookrightarrow}&
    Spin(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    Spin(3)
    \\
    &&
    \big\downarrow
    &{}^{(pb)}&
    \big\downarrow
    &{}^{(pb)}&
    \big\downarrow^{ \mathrlap{\pi} }
    \\
    \left\langle
     Ad_{
     \exp
     \left(
       \pi \mathrm{i} 
     \right)
     }
     =
     e
    \right\rangle
    &
    =
    &
    1
    &\overset{\phantom{AA}}{\hookrightarrow}&
    SO(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    SO(3)    
  }
$$


as well as

$$
  \array{
    \left\langle
      \exp\left( \pi \mathrm{i} \tfrac{1}{n} \right), \, \mathrm{j} 
    \right\rangle
    &=&
    2 D_{2n}
    &\overset{\phantom{AA}}{\hookrightarrow}&
    Pin_-(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    Spin(3)
    \\
    &&
    \big\downarrow
    &{}^{(pb)}&
    \big\downarrow
    &{}^{(pb)}&
    \big\downarrow^{ \mathrlap{\pi} }
    \\
    \left\langle
      Ad_{\exp\left( \pi \mathrm{i} \tfrac{1}{n}  \right) }, 
      \, 
      Ad_{\mathrm{j}} 
    \right\rangle
    &&
    D_{2n}
    &\overset{\phantom{AA}}{\hookrightarrow}&
    O(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    SO(3)    
  }
$$

exhibiting the [[binary dihedral groups]] as sitting inside the [[Pin(2)]]-[[subgroup]] of [[Spin(3)]],

but only [[commuting diagrams]]

$$
  \array{
    \left\langle
     \exp
     \left(
       2 \pi \mathrm{i} \tfrac{1}{{2n+1}} 
     \right)
    \right\rangle
    &
    =
    &
    \mathbb{Z}/(2n+1)
    &&\overset{\phantom{AA}}{\hookrightarrow}&&
    Spin(3)
    \\
    &&
    \big\downarrow
      &&
      &&
    \big\downarrow^{ \mathrlap{\pi} }
    \\
    \left\langle
     Ad_{
     \exp
     \left(
       2 \pi \mathrm{i} \tfrac{1}{2n+1} 
     \right)
     }
    \right\rangle
    &
    =
    &
    \mathbb{Z}/(2n+1)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    SO(2)
    &\overset{\phantom{AA}}{\hookrightarrow}&
    SO(3)    
  }
$$

for the [[odd number|odd]] [[order of a group|order]] [[cyclic group|cyclic]] [[subgroups]].

=--

This goes back to ([Klein 1884, chapter I](finite+rotation+group#Klein1884)). 
Full proof for $SO(3)$ is spelled out for instance in ([Rees 05, theorem 11](finite+rotation+group#Rees05), [De Visscher 11](finite+rotation+group#DeVisscher11)). The proof for the case of $SL(2,\mathbb{C})$ is spelled out in ([Miller-Blichfeldt-Dickson 16](finite+rotation+group#MillerBlichfeldtDickson16)) reviewed in ([Serrano 14, section 2](finite+rotation+group#Serrano14)). The proof of the case for $SU(2)$ given the result for $SO(3)$ is spelled out in [Keenan 03, theorem 4](finite+rotation+group#Keenan03).

\linebreak

### Irreducible representations

$SO(3)$ has an [[irreducible representation]] as the group of rotations in [[Euclidean space|$\mathbb{R}^3$]], whose [[group action|action]] preserves both the [[dot product]] and [[cross product]].  This is the "defining representation".

But something analogous happens to be true in  $\mathbb{R}^7$: There is an  $SO(3)$ [[subgroup]] of the [[exceptional Lie group]] [[G2|$G_2$]] (see [there](G2#Subgroups)) for which the irreducible representation of $G_2$ on $\mathbb{R}^7$ remains irreducible when restricted to this subgroup. $SO(3)$ preserves the dot and cross products defined there in terms of the imaginary [[octonions]].

This $7$-dimensional representation may also be realized as the space of harmonic cubic [[homogeneous polynomials]] on $\mathbb{R}^3$, otherwise known as the space of $f$-orbital wavefunctions.


## Related concepts

* [[principal SO(3)-bundle]]

* [[finite rotation group]]

* [[Euclidean group]]

* [[rigid body dynamics]]


[[!include low dimensional rotation groups -- table]]



\linebreak


## References


* Jason Hanson, _Rotations in three, four, and five dimensions_ ([arXiv:1103.5263](https://arxiv.org/abs/1103.5263))


See also 

* Wikipedia, _[3D rotation group](https://en.wikipedia.org/wiki/3D_rotation_group)_

On the [[integral cohomology]] of the [[classifying space]]:

* {#Brown82} [[Edgar H. Brown]], _The Cohomology of $B SO_n$ and $BO_n$ with Integer Coefficients_, Proceedings of the American Mathematical Society, Vol. 85, No. 2 (Jun., 1982), pp. 283-288 ([jstor:2044298](https://www.jstor.org/stable/2044298))

reviewed in 

* {#RudolphSchmidt17} Gerd Rudolph, Matthias Schmidt, around Theorem 4.2.23 of _Differential Geometry and Mathematical Physics: Part II. Fibre Bundles, Topology and Gauge Fields_, Theoretical and Mathematical Physics series, Springer 2017 ([doi:10.1007/978-94-024-0959-8](https://link.springer.com/book/10.1007/978-94-024-0959-8))

Visualisation and explanation:

* {#Egan11a} [[Greg Egan]], _[The Double Covers of SO(3) and SO(4)](https://www.gregegan.net/ORTHOGONAL/03/WavesExtra.html#DC)_ (2011)
* {#Egan11b} [[Greg Egan]], _[Representations of SO(3) and SO(4)](https://www.gregegan.net/ORTHOGONAL/03/WavesExtra.html#R34)_ (2011)

[[!redirects third special orthogonal group]]
[[!redirects SO3]]
