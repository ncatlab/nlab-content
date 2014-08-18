
> This entry is about &#233;tale morphisms between [[schemes]]. The term _[[étale map]]_ is preferred in the context of [[topology]] and [[differential geometry]], see [[étalé space]] for the topological version. 


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### &#201;tale morphisms
+--{: .hide}
[[!include etale morphisms - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The notion of _&#233;tale morphism of schemes_ is the realization of the general notion of [[étale morphism]] for maps between [[schemes]], hence it captures roughly the idea of a map of schemes which is a [[local homeomorphism]]/[[local diffeomorphism]].

A central use of &#233;tale morphisms of schemes is that they appear as [[coverings]] in the [[Grothendieck topology]] of the [[étale site]]. The [[abelian sheaf cohomology]] with respect to these &#233;tale covers of schemes is accordingly called _[[étale cohomology]]_.



## Definition

+-- {: .num_defn #EquivalentConditionsForEtale}
###### Definition

A [[morphism]] of [[schemes]] is an **&#233;tale morphism** if the following equivalent conditions hold:

1. it is

   1. [[smooth morphism of schemes|smooth]] 

   1. [[unramified morphism|unramified]] 

1. it is

   1. [[smooth morphism of schemes|smooth]] 

   1. of [[relative dimension]] $0$. 

1. it is 

   1. [[flat morphism|flat]] 

   1. [[unramified]];

1. it is

   1. [[formally étale morphism of schemes|formally étale]];

   1. [[locally of finite presentation]]

=--

(A number of other equivalent definitions are listed at [wikipedia](http://en.wikipedia.org/wiki/Etale_morphism).)  

+-- {: .num_remark}
###### Remark

For morphisms $f \colon X \longrightarrow Y$ between [[algebraic varieties]] over an [[algebraically closed field]] this means that for all points $p \in X$ the induced morphism on [[tangent cones]]

$$
  T_p X \longrightarrow T_{f(p)} Y
$$

is an [[isomorphism]]. This is analogous to the corresponding characterization of [[local diffeomorphisms]] of [[smooth manifolds]].

=--

+-- {: .num_remark}
###### Remark

Relaxing the finiteness condition in item 4 of \ref{EquivalentConditionsForEtale} yields the notion of _[[weakly étale morphism]]_.

[[étale morphism of schemes|étale morphism]] $\Rightarrow$ [[pro-étale morphism of schemes|pro-étale morphism]] $\Rightarrow$ [[weakly étale morphism of schemes|weakly étale morphism]] $\Rightarrow$ [[formally étale morphism of schemes|formally étale morphism]]


=--

+-- {: .num_defn}
###### Definition

A jointly surjective collection of &#233;tale morphisms $\{U_i \to X\}$ is called an [[étale cover]].

=--


+-- {: .num_remark}
###### Remark

Most of the pairs of conditions in def. \ref{EquivalentConditionsForEtale} can be read as constraining the fiber of the morphism to be first suitably surjective/[[bundle]]-like ([[smooth morphism of schemes|smooth]], [[flat morphism|flat]]) and second suitably locally injective ([[unramified]]).

Specifically the first condition has an [[infinitesimal object|infinitesimal anlog]]: a [[formally étale morphism]] is a [[formally smooth morphism|formally smooth]] and [[formally unramified morphism]]. These notions also have an interpretation in [[synthetic differential geometry]] and there they correspond to the statement that a [[local diffeomorphism]] is a [[submersion]] which is also an [[immersion of smooth manifolds]].

=--


+-- {: .num_defn}
###### Definition

A morphism is **[[formally étale morphism]]** if it is 

* [[formally smooth]] (satisfying an infinitesimal lifting property) 

* and [[formally unramified]]. 

=--

+-- {: .num_remark}
###### Remark

These are sheaf-like properties, which can be formalized in the language of [[Q-categories]] ([[monopresheaf]] and [[epipresheaf]] properties on the $Q$-category of nilpotent thickenings). 

See at _[[differential cohesion]]_ and at _[[infinitesimal shape modality]]_.
=--

## Properties


### Closure properties

+-- {: .num_prop}
###### Proposition

* A [[composite]] of two &#233;tale morphism is itself &#233;tale.

* The [[pullback]] of an &#233;tale morphism is &#233;tale.

* If $f_1 \circ f_2$ is &#233;tale and $f_1$ is, then so is $f_2$.

=--

(e.g. [Milne, prop. 2.11](#Milne))

+-- {: .proof}
###### Proof

Use that an &#233;tale morphism is a [[formally étale morphism]] with finite fibers, and that $f \colon X \to Y$ is formally &#233;tale precisely if the [[infinitesimal shape modality]] [[unit of a monad|unit]] [[natural transformation|naturality square]]

$$
  \array{
    X &\longrightarrow& \Pi_{inf}(X)
    \\
    \downarrow && \downarrow
    \\
    Y &\longrightarrow& \Pi_{inf}(Y)
  }
$$

is a [[pullback]] square. Then the three properties to be shown are equivalently the [[pasting law]] for pullback diagrams.

=--


+-- {: .num_prop}
###### Proposition


A [[smooth morphism of schemes]] is &#233;tale iff there is an [[étale cover]] of the base  scheme by [[open subschemes]] such that the pullback of the projection to each of them is an open local isomorphism of [[locally ringed spaces]] (and in particular, the pullback of the projection morphism is an [[étalé space|étale map]] of the corresponding underlying topological spaces). 

=--

+-- {: .num_remark}
###### Remark

This disjointness picture of &#233;tale covers make them suitable for having nontrivial [[cohomology]] in situations where Zariski covers give vanishing cohomology.

=--

### Classes of examples

+-- {: .num_prop}
###### Proposition

Let $k$ be a [[field]]. A morphism of [[scheme]]s $Y \to Spec k$ is &#233;tale precisely if $Y$ is a [[coproduct]] $Y \simeq \coprod_i Spec k_i$ for each $k_i$ a finite and separable [[field extension]] of $k$.

=--

This appears for instance as [de Jong, prop. 3.1 i)](#deJong). 

+-- {: .num_remark}
###### Remark

Such &#233;tale morphisms are classified by the classical [[Galois theory]] of field extensions.

=--


+-- {: .num_prop}
###### Proposition

A [[ring]] homomorphism of [[affine varieties]] $Spec(A) \to Spec(B)$ for $Spec(B)$ non-singular and for $A \simeq B[x_1, \cdots, x_n]/(f_1, \cdots, f_n)$  with [[polynomials]] $f_i$ is &#233;tale precisel if the [[Jacobian]] $det(\frac{\partial f_i}{\partial x_j})$ is invertible.

=--

This appears for instance as ([Milne, prop. 2.1](#Milne)).




### As locally constant sheaves {#AsLocallyConstantSheaves}

+-- {: .num_prop}
###### Proposition

A [[sheaf]] $F$ on a scheme $X$ corresponds to an &#233;tale morphism $Y \to X$ precisely if there is an [[étale cover]] $\{U_i \to X\}$ such that each restriction

$$
  F|_{U_i} \simeq LConst K_i
$$

is [[isomorphic]] to a [[constant sheaf]] on a [[set]] $K_i$.

=--

A proof is in ([Deligne](#Deligne)).



## Examples
 {#Examples}


+-- {: .num_example}
###### Example

A finite separable [[field extension]] $K \hookrightarrow L$ corresponds dually to an &#233;tale morphism $Spec L \to Spec K$. These are the morphisms classified by classical [[Galois theory]].

=--

+-- {: .num_example #OpenImmersionIsEtale}
###### Example

Every [[open immersion of schemes]] is an &#233;tale morphism of schemes.
In particular a standard open inclusion (a [[cover]] in the [[Zariski topology]]) induced by the [[localization of a commutative ring]]

$$
  Spec(R[S^{-1}]) \longrightarrow Spec(R)
$$

is &#233;tale.

=--

(e.g. [[The Stacks Project|Stacks Project, lemma 28.37.9]])

+-- {: .proof}
###### Proof

By one of the equivalent characterizations of [[étale morphism]] it is sufficient to check that the map $Spec(R[S^{-1}]) \longrightarrow Spec(R)$ is a [[formally étale morphism]] and [[locally of finite presentation]].

The latter is clear, since the very definition of 

$$
  R[S^{-1}] = R[s_1^{-1}, \cdots, s_n^{-1}](s_1 s_1^{-1} - 1, \cdots , s_n s_n^{-1} - 1)
$$ 

exhibits a [[finitely presented algebra]] over $R$.

To see that it is formally &#233;tale we need to check that for every [[commutative ring]] $T$ with [[nilpotent ideal]] $J$ we have a [[pullback]] diagram

$$
  \array{
    Hom(R[S^{-1}], T) &\longrightarrow& Hom(R[S^{-1}],T/J)
    \\
    \downarrow && \downarrow
    \\
    Hom(R, T) &\longrightarrow& Hom(R, T/J)
  }
  \,.
$$

Now by the [[universal property]] of the [[localization of a commutative ring|localization]], a homomorphism $R[S^{-1}] \longrightarrow T$ is a homomorphism $R \longrightarrow T$ which sends all elements in $S \hookrightarrow R$ to invertible elements in $T$. But no element in a [[nilpotent ideal]] can be invertible, Therefore the fiber product of the bottom and right map is the set of maps from $R$ to $T$ such that $S$ is taken to invertibles, which is indeed the top left set.


=--




## Related concepts

* [[étale morphism]]

* **&#233;tale morphism of schemes**

  * [[étale site]], [[étale cohomology]]

  * [[étale (∞,1)-site]]

  * [[étale morphism of E-∞ rings]]

## References

The classical references are


* [[Pierre Deligne]] et al., _Cohomologie &#233;tale_ , Lecture Notes in Mathematics, no. 569, Springer-Verlag, 1977.
{#Deligne}

* [[James Milne]], _[[Étale Cohomology]]_, Princeton Mathematical Series __33__, 1980. xiii+323 pp.

Lecture notes include

* [[James Milne]], section 2 of _[[Lectures on Étale Cohomology]]_
 {#Milne}

* [[Aise Johan de Jong]], _&#201;tale cohomology_ ([pdf](http://math.columbia.edu/~pugin/Teaching/Etale_files/EtaleCohomology.pdf))
{#deJong} --- link broken, couldn't find another copy online

The local structure theorems are discussed in 

* Leovigildo Alonso, Ana Jeremias, Marta Perez, _Local structure theorems for smooth maps of formal schemes_ ([arXiv:math/0605115](http://arxiv.org/abs/math/0605115))

Discussion of etale morphisms between [[E-infinity rings]]/[[spectral schemes]] is in 

* [[Jacob Lurie]], section 8.5 of _[[Higher Algebra]]_

and generally in [[E-∞ geometry]] in 

* [[Jacob Lurie]], section 1.2 of _[[Quasi-Coherent Sheaves and
Tannaka Duality Theorems]]_



[[!redirects étale morphism of schemes]]

[[!redirects etale morphisms of schemes]]
[[!redirects étale morphisms of schemes]]