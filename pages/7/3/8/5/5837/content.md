
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

## Examples

### Of the 3-sphere

+-- {: .num_theorem #SmaleConjecture}
###### Theorem

The diffemorphism group of the 3-sphere is [[homotopy equivalence|homotopy equivalent]] to the [[orthogonal group]] $O(4)$, the equivalence being exhibited by the canonical inclusion

$$
  O(4) \hookrightarrow Diff(S^3)
  \,.
$$

=--

After being conjectured by Smale, this was proven in ([Hatcher 1983](#Hatcher)).

### Of general 3-manifolds

+-- {: .num_theorem}
###### Theorem

For every [[smooth manifold]] $X$ of [[dimension]] 3 the canonical map

$$
  Diff(X) \to Homeo(X)
$$

sending [[diffeomorphisms]] to their underlying [[homeomorphisms]] of [[topological spaces]] is a [[weak homotopy equivalence]]. 

=--

That this follows from the Smale cojecture, theorem \ref{SmaleConjecture}, was shown in [Cerf](#Cerf). For discussion see [Hatcher, 1978](#Hatcher78).


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

The [[homotopy type]] $\Pi(Diff(\sigma))$ of the diffeomorphism group $Diff(\Sigma)$ is of interest (e.g. [Hatcher](#HatcherHomotopyType)).

For instance this is the [[automorphism ∞-group]] of a manifold, regarded as a [[k-morphism]] in an [[(∞,n)-category of cobordisms]].

Specifically, the group of connected components is the [[mapping class group]]

$$
  \pi_0(\Pi(Diff(\Sigma))) = MCG(\Sigma)
  \,.
$$

#### For surfaces
 {#HomotopyTypeForSurfaces}

+-- {: .num_prop}
###### Proposition


For $\Sigma$ a [[closed manifold|closed]] [[orientation|orientable]] [[surface]], then the [[fundamental ∞-groupoid|bare homotopy type]] of its diffeomorphism group is

1. if $\Sigma$ is the [[sphere]] then
 
   $$
     \Pi(Diff(S^2)) \simeq \Pi(O(3))
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




## References

### For 2-manifolds (surfaces)

* {#ZieschangVogtColdeway} Zieschang, Vogt and Coldeway, _Surfaces and planar discontinuous groups_


### For 3-manifolds

* {#Cerf} J. Cerf, _Sur les diff&#233;omorphismes de la sph&#232;re de dimension trois ($\Gamma_4 = 0$)_, Lecture Notes in Math., vol. 53, Springer-Verlag, Berlin and New York, 1968_
 

* {#Hatcher78} [[Allen Hatcher]], _Linearization in 3-dimensional topology_, Proceedings of the international congress of Mathematicians, Helsinki (1978)
 
* {#Hatcher} [[Allen Hatcher]], _A proof of the Smale conjecture, $Diff(S^3) \simeq O(4)$, Annals of Mathematics 117 (1983) ([jstor](http://www.jstor.org/pss/2007035))
 

* {#Waldhausen68} [[Friedhelm Waldhausen]], _On Irreducible 3-Manifolds Which are Sufficiently Large_, Annals of Mathematics
Second Series, Vol. 87, No. 1 (Jan., 1968), pp. 56-88 ([JSTOR](http://www.jstor.org/stable/1970594))

### Homotopy type and mapping class group

{#EarleEells67} C.J. Earle,  J. Eells, _The diffeomorphism group of a compact Riemann surface,
Bulletin of the American Mathematical Society 73(4) 557--559, 1967


* {#HatcherHomotopyType} [[Alan Hatcher]], _A 50-Year View of DiffeomorphismGroups_ ([pdf](http://www.math.cornell.edu/~hatcher/Papers/Diff%28M%292012.pdf))


[[!redirects diffeomorphism groups]]
[[!redirects Smale conjecture]]