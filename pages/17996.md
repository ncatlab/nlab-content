[[!redirects basic line bundle on the 2-sphere]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _basic line bundle on the 2-sphere_ is the [[complex line bundle]] on the [[2-sphere]] whose [[first Chern class]] is a generator $\pm 1 \in \mathbb{Z} \,\simeq\, H^2(S^2, \mathbb{Z})$, equivalently the [[tautological line bundle]] on the [[Riemann sphere]] regarded as [[complex projective space|complex projective 1-space]].

This is the [[pullback bundle]] of the map $S^2 \to B U(1) \simeq B^2 \mathbb{Z}$ to the [[classifying space]]/[[Eilenberg-MacLane space]] which itself represents a generator of the [[homotopy group]] $\pi_2(S^2) \simeq \mathbb{Z}$.

Beware that this basic line bundle is sometimes called the "canonical line bundle on the 2-sphere", but it is  _not_ [[isomorphism|isomorphic]] to what in complex geometry is called the [[canonical bundle]] of the 2-sphere regarded as a [[Riemann surface]]. Instead it is "one half" of the latter, its [[theta characteristic]]. See also at _[[geometric quantization of the 2-sphere]]_.

The basic line bundle is the canonically [[associated bundle]] to basic [[circle principal bundle]]: the [[complex Hopf fibration]]. Another name for it is the [[tautological line bundle]] for the complex [[projective space|projective line]] $\mathbb{P}^1(\mathbb{C})$ (the [[Riemann sphere]]), namely the map $\mathbb{C}^2 \setminus \{(0, 0)\} \to \mathbb{P}^1(\mathbb{C})$ mapping $(x, y)$ to $[x; y]$. 

## Definition

The [[classifying space]] for [[circle principal bundles]], or equivalently (via forming [[associated bundles]]) that of [[complex line bundles]] is $B U(1)$, which as a [[Grassmannian]] is the infinite [[complex projective space]] $\mathbb{C}P^\infty$. The [[homotopy type]] of this space is that of the [[Eilenberg-MacLane space]] $K(\mathbb{Z},2)$. This means that $K(\mathbb{Z},2)$ is in particular [[path-connected topological space|path-connected]] and has second [[homotopy group]] the [[integers]]: $\pi_2(K(\mathbb{Z},2)) \simeq \mathbb{Z}$.

It being the [[classifying space]] for complex line bundles means that 

$$
  \left\{
     \array{ 
        \text{isomorphism classes of}
        \\
        \text{complex line bundles}
        \\
        \text{on}\,\, S^2 
     }
  \right\}
  \;\simeq\;
  \left\{
    \array{
      \text{continuous functions}
      \\
      S^2 \longrightarrow K(\mathbb{Z},2)
      \\
      \text{up to homotopy}
    }
  \right\}
  \;\simeq\;
  \pi_2(K(\mathbb{Z},2))
  \;\simeq\;
  \mathbb{Z}
  \,.
$$

The ([[isomorphism class]]) of the complex line bundle which corresponds to $+1 \in \mathbb{Z}$ under this sequence of [[isomorphisms]] is called the _basic complex line bundle on the 2-sphere_. 

Hence the basic complex line bundle on the 2-sphere is [[generalized the|the]] [[pullback bundle]] of the [[universal complex line bundle]] on $B U(1)$ along the map $S^2 \to B U(1)$ which represents the element $1 \in \mathbb{Z} \simeq \pi_2(B U(1))$. If the [[classifying space]] $B U(1)$ is represented by the infintie [[complex projective space]] $\mathbb{C}P^\infty$ with its canonical [[CW-complex]] structure ([this prop.](complex+projective+space#CellComplexStructureOnComplexProjectiveSpace)), then this map is represented by the canonical cell incusion $S^2 \hookrightarrow\mathbb{C}P^\infty$.

Notice that there is a non-trivial [[automorphism]] of $\mathbb{Z}$ as an [[abelian group]] given by $n \mapsto -n$. This means that there is an ambiguity in the definition of the basic line bundle on the 2-sphere. 

## Properties


+-- {: .num_lemma #ClutchingConstructionOfBasicLineBundle}
###### Lemma
**([[clutching construction]] of the basic line bundle)

Under the [[clutching construction]] of [[vector bundles]] on the [[2-sphere]], the basic complex line bundle on the 2-sphere is given by the [[transition function]]

$$
  \mathbb{C} \supset \, S^1 \longrightarrow GL(1,\mathbb{C}) \, \subset \mathbb{C}
$$

from the [[Euclidean space|Euclidean]] [[circle]] $S^1 \subset \mathbb{R}^2 \simeq \mathbb{C}$ to the complex [[general linear group]] in 1-dimension, which is $GL(1,\mathbb{C}) \simeq \mathbb{C} \setminus \{0\}$ given simply by

$$
  z \mapsto z
  \,,
$$

Alternatively, due to the sign ambiguity in the definition of the basic bundle, its clutching transition function is given by

$$
  z \mapsto - z
  \,.
$$

=--

+-- {: .proof}
###### Proof

Under the [[clutching construction]] the [[isomorphism class]] of a complex line bundle corresponds to the [[homotopy class]] of its clutching transition function

$$
  S^1 \to GL(1, \mathbb{C}) \simeq \mathbb{C} \setminus \{0\}
$$

hence to an element of the [[fundamental group]] $\pi_1(\mathbb{C} \setminus \{0\}) \simeq \mathbb{Z}$. Hence by definition, the basic bundle has clutching transition function corresponding to $\pm 1  \in \mathbb{Z} \simeq [S^1, GL(1,\mathbb{Z})]$ and this element is represented by the function $z \mapsto \pm z$.

=--



+-- {: .num_prop #TensorRelationForBasicLineBundleOn2Sphere}
###### Proposition
**(fundamental tensor/sum relation of the basic complex line bundle)**

Under [[direct sum of vector bundles]] $\oplus_{S^2}$ and [[tensor product of vector bundles]] $\otimes_{S^2}$, the basic line bundle on the 2-sphere $H \to S^2$ satisfies the following relation

$$
  H \oplus_{S^2} H
    \;\simeq\;
  \left(
    H \otimes_{S^2} H
  \right)
    \oplus_{S^2}
  1_{S^2}
$$

(where $1_{S^2}$ denotes the [[trivial vector bundle]] [[complex line bundle]] on the 2-sphere).

=--

(e.g ([Hatcher, Example 1.13](#Hatcher)))

+-- {: .proof}
###### Proof

Via the [[clutching construction]] there is a single [[transition function]] of the form

$$
  S^1 \longrightarrow GL(n,\mathbb{C})
$$

that characterizes all the bundles involved. With $S^1 \hookrightarrow \mathbb{C}$ identified with the [[topological subspace]] of [[complex numbers]] of unit [[absolute value]], the standard choice for these functions is

* for the [[trivial vector bundle|trivial]] [[line bundle]] $1_{S^2}$ we may choose

  $f_1 \colon z \mapsto \left( 1 \right)$;

* for the basic line bundle we may choose (by lemma \ref{ClutchingConstructionOfBasicLineBundle}) 

  $f_H \colon z \mapsto \left( z\right)$ 

This yields

* for $H \otimes H \oplus 1_{S^2}$ the clutching function 
   
  $z \mapsto \left( \array{ z^2 & 0 \\ 0 & 1 }\right)$

* for $H \oplus H$ the clutching function

  $z \mapsto \left( \array{ z & 0 \\ 0 & z }  \right)$.

Since the complex [[general linear group]] $Gl(n,\mathbb{C})$ is [[path-connected topological space|path-connected]] (by [this prop.](general+linear+group#ConnectednessOfGeneralLinearGroup)), there exists a [[continuous function]]

$$
  \gamma \colon [0,1] \longrightarrow GL(2,\mathbb{C})
$$

connecting the identity matrix on $\mathbb{C}^2$ with the one that swaps the two entries, i.e.

with $\gamma(0) = \left( \array{ 1 & 0 \\ 0 & 1 }  \right)$

and $\gamma(1) = \left(  \array{ 0 & 1 \\ 1 & 0 } \right)$

Therefore the function

$$
  \array{
    S^1 \times [0,1] &\overset{}{\longrightarrow}& GL(2,\mathbb{C})
    \\
    (z,t) 
      &\overset{\phantom{AA}}{\longrightarrow}& 
    f_{H \oplus 1}(z) \cdot \gamma(t) \cdot f_{1 \oplus H}(z) \cdot \gamma(t)
  }
$$

(with [[matrix multiplication]] on the right) is a [[left homotopy]] from $f_{H \oplus H}$ to $f_{H \otimes H \oplus 1}$.


=--

+-- {: .num_remark}
###### Remark
**([[fundamental product theorem in topological K-theory]])**

Under the map

$$
  Vect(S^2)_{/\sim} \longrightarrow K(X)
$$

that sends [[complex vector bundles]] to their class in the [[topological K-theory]] ring $K(X)$, the fundamental tensor/sum relation of prop. \ref{TensorRelationForBasicLineBundleOn2Sphere} says that the K-theory class $H$ of the basic line bundle in $K(X)$ satisfies the relation

$$
  \begin{aligned}
    (H - 1)^2 
    & = 
    H^2  + 1 - \underset{= H^2 + 1}{\underbrace{2 H}}
    \\
    = &   0
  \end{aligned}  
$$

in $K(X)$. 

(Notice that $H-1$ is the image of $[H]$ in the [[reduced K-theory]] $\tilde K(X)$ of $S^2$ under the splitting $K(X) \simeq \tilde K(X) \oplus \mathbb{Z}$ (by [this prop.](topological+K-theory#KGrupDirectSummandReducedKGroup)).)

It follows that there is a [[ring homomorphism]] of the form

$$
  \array{
    \mathbb{Z}[h]/\left( (h-1)^2 \right)
      &\overset{}{\longrightarrow}&
    K(S^2)
    \\
    h &\overset{\phantom{AAA}}{\mapsto}& H
  }
$$

from the [[polynomial ring]] in one abstract generator, [[quotient ring|quotiented]] by this relation, to the [[topological K-theory]] ring.

It turns out that this homomorphism is in fact an [[isomorphism]], hence that the relation $(H-1)^2 = 0$ from prop. \ref{TensorRelationForBasicLineBundleOn2Sphere} is the _only_ relation satisfied by the basic complex line bundle in topological K-theory.

More generally, for $X$ a [[topological space]], then there is a composite ring homomorphism

$$
  \array{
    K(X) \otimes \mathbb{Z}[h]/((h-1)^2)
      & \longrightarrow & 
    K(X) \times K(S^2)
      & \longrightarrow &
    K(X \times S^2)
    \\
    (E, h)
      &\overset{\phantom{AAA} }{\mapsto}&
    (E,H)
      &\overset{\phantom{AAA}}{\mapsto}&
    (\pi_{X}^\ast E) \cdot (\pi_{S^2}^\ast H) 
  }
$$

to the topological K-theory ring of the [[product topological space]] $X \times S^2$, where the second map is the [[external tensor product]] of vector bundles.

This composite is an [[isomorphism]] if $X$ is a [[compact Hausdorff space]] (for $X = \ast$ the [[point space]] this reduces to the previous statement).

This is called the _[[fundamental product theorem in topological K-theory]]_. It is the main ingredient in the [[proof]] of [[Bott periodicity]] in complex topological K-theory.

=--


## Related concepts

* [[universal complex line bundle]]

* [[tautological line bundle]], [[equivariant tautological line bundle]]

## References

* {#Hatcher} [[Allen Hatcher]], _Vector bundles and K-theory_ ([web](https://www.math.cornell.edu/~hatcher/VBKT/VBpage.html))

* {#Wirthmuller12} [[Klaus Wirthmüller]], _Vector bundles and K-theory_, 2012 ([pdf](ftp://www.mathematik.uni-kl.de/pub/scripts/wirthm/Top/vbkt_skript.pdf))


[[!redirects basic line bundles on the 2-sphere]]