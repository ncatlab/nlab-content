
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

The _diffeomorphism group_ $Diff(X)$ of a [[smooth manifold]] $X$ is the [[group]] of its [[diffeomorphism]]s: the [[automorphism group]] of $X$ as an [[object]] of the [[category]] [[SmoothMfd]].

Beware that when $X$ is assumed [[orientable]] then sometimes, but not always, $Diff(X)$ is implicitly taken to be the group of orientation-preserving diffeomorphisms. 



## Properties

### Relation to homotopy equivalences

For the following kinds of manifolds $\Sigma$ it is true that every [[homotopy equivalence]] 

$$
  \alpha \colon \Pi(\Sigma) \stackrel{\simeq}{\longrightarrow} \Pi(\Sigma)
$$

(hence every [[equivalence of infinity-groupoids|equivalence]] of their [[fundamental infinity-groupoids]]) is [[homotopy|homotopic]] to a [[diffeomorphism]]

$$
  a \colon \Sigma \stackrel{\simeq}{\longrightarrow} \Sigma
$$

i.e. that given $\alpha$ there is $a$ with

$$
  \alpha \simeq \Pi(a)
  \,.
$$


* for $\Sigma$ any [[surface]] ([Zieschang-Vogt-Coldeway](#ZieschangVogtColdeway))

* for $\Sigma$ a [[Haken 3-manifold]] ([Waldhausen](#Waldhausen68)) 

* for $\Sigma$ any  [[hyperbolic manifold]] of finite [[volume]] and of [[dimension]] $\geq 3$ (by [[Mostow rigidity theorem]]) (check)

### Homotopy type and mapping class group
 {#HomotopyTypeAndMappingClassGroup}

The [[homotopy type]] $\Pi(Diff(\Sigma))$ of the diffeomorphism group $Diff(\Sigma)$ is of interest (e.g. [Hatcher 12](#Hatcher12)).

For instance this is the [[automorphism ∞-group]] of a manifold, regarded as a [[k-morphism]] in an [[(∞,n)-category of cobordisms]].

Specifically, the group of connected components is the [[mapping class group]]

$$
  \pi_0(\Pi(Diff(\Sigma))) = MCG(\Sigma)
  \,.
$$

#### For 1-manifolds

$$
  \Pi(Diff(S^1))\simeq \Pi(O(2))
$$

$$
  \Pi(Diff(D^1))\simeq \Pi(O(1))
$$

#### For 2-manifolds (surfaces)
 {#HomotopyTypeForSurfaces}

+-- {: .num_prop #HomotopyTypeOfDiffClosedOrientableSurface}
###### Proposition


For $\Sigma$ a [[closed manifold|closed]] [[orientation|orientable]] [[surface]], then the [[fundamental ∞-groupoid|bare homotopy type]] of its diffeomorphism group is

1. if $\Sigma$ is the [[sphere]] then
 
   $$
     \begin{aligned} 
        \Pi(Diff(S^2)) & \simeq \Pi(O(3))
        \\
        & \simeq MCG(S^2)\times \Pi(SO(3))
        \\
        & \simeq \mathbb{Z}_2 \times \Pi(SO(3))
     \end{aligned}
   $$

1. if $\Sigma$ is the [[torus]] then

   $$
     \begin{aligned}
       \Pi(Diff(S^1 \times S^1)) 
       & \simeq 
       MCG(S^1 \times S^1)\times \Pi(S^1 \times S^1 )
       \\
       & \simeq GL_2(\mathbb{Z}) \times B(\mathbb{Z} \times\mathbb{Z})
     \end{aligned}
   $$ 

1. in all other cases all higher [[homotopy groups]] vanish:

   $$
     \Pi(Diff(\Sigma)) \simeq MCG(\Sigma)
   $$

=--

The first statement is due to ([Smale 58](#Smale58)), see also at _[[sphere eversion]]_. The second and third are due to ([Earle-Eells 67](#EarleEells67), [Gramain 73](#Gramain73)).

#### For 3-manifolds

+-- {: .num_prop}
###### Proposition

$$
  \Pi(Diff(S^1 \times S^2))
  \simeq
  \Pi(O(2) \times O(3))
  \times
  \Omega \Pi(SO(3))
  \,.
$$

=--

([Hatcher 81](#Hatcher81))


\begin{theorem}
\label{SmaleConjecture}
**(Smale conjecture)**
\linebreak
The bare [[homotopy type]] of the [[diffeomorphism group]] of the [[3-sphere]] is that of the [[orthogonal group]] $O(4)$

$$
  \esh\big(
    Diff(S^3)
  \big) 
  \;\simeq\; 
  \esh 
  \,
   O(4))
  \,,
$$

the equivalence being exhibited by the canonical inclusion

$$
  O(4) \hookrightarrow Diff(S^3)
  \,.
$$

Also

$$
  \esh
   \,
   Diff(D^3)
   \;\simeq\; 
   \esh
   \, 
   O(3)
   \,.
$$
\end{theorem}

After being conjectured by Smale, this was proven in ([Hatcher 1983](#Hatcher)).



Generally:


+-- {: .num_theorem}
###### Theorem

For every [[smooth manifold|smooth]] [[3-manifold]] the canonical map

$$
  \Pi(Diff(X)) \to \Pi(Homeo(X))
$$

sending [[diffeomorphisms]] to their underlying [[homeomorphisms]] of [[topological spaces]] is a [[weak homotopy equivalence]]. 

=--

That this follows from the Smale cojecture, theorem \ref{SmaleConjecture}, was shown in ([Cerf](#Cerf)). For discussion see ([Hatcher, 1978](#Hatcher78)).

+-- {: .num_prop}
###### Proposition

If a 3-manifold $X$ is not a [[Seifert 3-manifold]] via an $S^1$-action then

$$
  \Pi(Diff(X)) \simeq MCG(X)
  \,.
$$

=--

If $X$ is Seifert via an $S^1$-action, then the component of $Diff(X)$ are typically $\Pi(S^1)$-s.



## References

### Smooth structure

The observation that infinite-dimensional  [[smooth groups]] such as diffeomorphism groups (and [[quantomorphism groups]] etc.) are naturally regarded as [[internal groups]] in [[diffeological spaces]] -- [[diffeological groups]] -- is due to

* {#Souriau79} [[Jean-Marie Souriau]], _Groupes diff&#233;rentiels_, in _Differential Geometrical Methods in Mathematical Physics_ (Proc. Conf., Aix-en-Provence/Salamanca, 1979), Lecture Notes in Math. 836, Springer, Berlin, (1980), pp. 91&#8211;128. ([MathScinet](http://www.ams.org/mathscinet-getitem?mr=607688))


### For 2-manifolds (surfaces)

{#EarleEells67} C.J. Earle,  J. Eells, _The diffeomorphism group of a compact Riemann surface,
Bulletin of the American Mathematical Society 73(4) 557--559, 1967


* {#ZieschangVogtColdeway} Zieschang, Vogt and Coldeway, _Surfaces and planar discontinuous groups_


### For 3-manifolds

* {#Cerf} J. Cerf, _Sur les diff&#233;omorphismes de la sph&#232;re de dimension trois ($\Gamma_4 = 0$)_, Lecture Notes in Math., vol. 53, Springer-Verlag, Berlin and New York, 1968_
 

* {#Hatcher78} [[Allen Hatcher]], _Linearization in 3-dimensional topology_, Proceedings of the international congress of Mathematicians, Helsinki (1978)
 

* {#Hatcher81} [[Allen Hatcher]], _On the diffeomorphism group of $S^1\times S^2$_, Proceedings of the AMS 83 (1981), 427-43 ([pdf](http://www.math.cornell.edu/~hatcher/Papers/newDiffS1xS2.pdf))

* {#Hatcher} [[Allen Hatcher]], _A proof of the Smale conjecture, $Diff(S^3) \simeq O(4)$, Annals of Mathematics 117 (1983) ([jstor](http://www.jstor.org/pss/2007035))
 

* {#Waldhausen68} [[Friedhelm Waldhausen]], _On Irreducible 3-Manifolds Which are Sufficiently Large_, Annals of Mathematics
Second Series, Vol. 87, No. 1 (Jan., 1968), pp. 56-88 ([JSTOR](http://www.jstor.org/stable/1970594))


### For 4-manifolds

For 4-manifolds the analogue of the Smale conjecture fails:

* {#Watanabe18} [[Tadayuki Watanabe]], *Some exotic nontrivial elements of the rational homotopy groups of $Diff(S^4)$* ([arXiv:1812.02448](https://arxiv.org/abs/1812.02448))

* {#Watanabe21} [[Tadayuki Watanabe]], *Addendum to: Some exotic nontrivial elements of the rational homotopy groups of $Diff(S^4)$ (homological interpretation)* ([arXiv:2109.01609](https://arxiv.org/abs/2109.01609))

  > (via  [[graph complexes]])


### General

* {#Hatcher12} [[Alan Hatcher]], _A 50-Year View of Diffeomorphism Groups_, talk at the 50th Cornell Topology Festival in May 2012 ([pdf](http://www.math.cornell.edu/~hatcher/Papers/Diff%28M%292012.pdf), [[HatcherDiffeomorphismReview.pdf:file]])




[[!redirects diffeomorphism groups]]
[[!redirects Smale conjecture]]