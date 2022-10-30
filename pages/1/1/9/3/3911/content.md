
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Fiber integration_ or _push-forward_ is a process that sends [[generalized cohomology]] classes on a [[bundle]] $E \to B$ of [[manifolds]] to cohomology classes on the base $B$ of the bundle, by _evaluating them on each fiber_ in some sense. 

This sense is such that if the cohomology in question is [[de Rham cohomology]] then fiber integration is ordinary [[integration]] of [[differential form]]s over the fibers. Generally, the fiber integration over a bundle of $k$-dimensional fibers reduces the degree of the cohomology class by $k$.

Composing pullback of cohomology classes with fiber integration yields the notion of [[transgression]].

## Definition

### In generalized cohomology by Umkehr maps

#### Along maps of manifolds

Here is the rough outline of the construction via [[Umkehr maps]].

The basic strategy is this:

1. start with a map $E \to B$

1. make $E$ bigger by passing to its [[Thom space]] $Th(E)$ such that we have a map the other way round $B \to Th(E)$;

1. choose an [[orientation in generalized cohomology|orientation]] structure that makes the cohomology of $E$ equivalent to that of $Th(E)$ (the [[Thom isomorphism]]);

1. compose the Thom isomorphism with the pullback along $B \to Th(E)$ to get an "Umkehr" map from cohomology of $E$ to cohomology of $B$.

Now in detail.


Let $p : E \to B$ be a [[bundle]] of smooth compact [[manifolds]] with typical [[fiber]] $F$. 


By the [[Whitney embedding theorem]] one can choose an embedding $e:E \hookrightarrow \mathbb{R}^n$ for some $n \in \mathbb{N}$. From this one obtains an embedding

$$
  (p,e) : E \hookrightarrow B \times \mathbb{R}^n
  \,.
$$

Let $N_{(p,e)} (E)$ be the [[normal bundle]] of $E$ relative to this embedding. It is a rank $n- dim F$ bundle over the image of $E$ in $B \times \mathbb{R}^n$.

Fix a [[tubular neighbourhood]] of $E$ in $B \times \mathbb{R}^n$ and identify it with the total space of $N_{(p,e)}$. Then collapsing the whole $B \times \mathbb{R}^n - N_{(p,e)}(E)$ to a point gives the [[Thom space]] of $N_{(p,e)}(E)$, and the quotient map

$$
  B \times \mathbb{R}^n 
  \to 
  B \times \mathbb{R}^n / (B \times \mathbb{R}^n - N_{(p,e)}(E))
  \simeq
  Th(N_{(p,e)}(E))
$$

factors through the [[one-point compactification]] $(B \times \mathbb{R}^n)^*$
of $B \times \mathbb{R}^n$. Since $(B \times \mathbb{R}^n)^*\cong \Sigma^n B_+$,
the $n$-fold [[suspension]] of $B_+$ (or, equivalently, the [[smash product]] of $B$ with the $n$-sphere: $\Sigma^n B_+= S^n \wedge B_+$), we obtain a factorization
$$
  B \times \mathbb{R}^n \to \Sigma^n B_+ \stackrel{\tau}{\to} Th(N_{(p,e)}(E))
  \,,
$$
where $\tau$ is called the [[Pontrjagin-Thom collapse map]].

Explicitly, as sets we have $\Sigma^n B_+ \simeq B \times \mathbb{R}^n \cup \{\infty\}$ and $Th(N_{(e,p)}(E)) = N_{(e,p)} \cup \{\infty\}$, and for $U \subset \Sigma^n B_+$ a tubular neighbourhood of $E$ and $\phi : U \to N_{(e,p)}(E)$ an isomorphism, the map 

$$
  \tau : \Sigma^n B_+ \stackrel{}{\to} Th(N_{(p,e)}(E))
$$

is defined by

$$
  \tau : x \mapsto 
  \left\{
    \array{
      \phi(x) & | x \in U
      \\
      \infty & | otherwise
    }
  \right.
  \,.
$$

Now let $H$ be some [[multiplicative cohomology theory]], and assume that the Thom space $Th(N_{(p,e)}(E))$ has an $H$-[[orientation in generalized cohomology|orientation]], so that we have a  [[Thom isomorphism]]. Then combined with the [[suspension isomorphism]] the pullback along $\tau$ produces a morphism

$$
  \int_F : H^\bullet(E) \to H^{\bullet - dim F}(B)
$$

of cohomologies

$$
  \array{
   H^\bullet(E)
   \\
   \downarrow^{\mathrlap{\simeq_{Thom}}{\to}}
   \\
   H^{\bullet + n - dim F}(D(N_{(p,e)}(E)),S(N_{(p,e)}(E)))
   \\
   \downarrow^{\mathrlap{\simeq}}
   \\
   \tilde H^{\bullet + n - dim F}(Th(N_{(p,e)}(E)))
   &
   \stackrel{\tau^*}{\to}
   &
   \tilde H^{\bullet + n - dim F}(\Sigma^n B_+)
   \\
   && \downarrow{\mathrlap{\simeq_{suspension}}}   
   \\
   &&
   H^{\bullet - dim F}(B)
   }
   \,.
$$


This operation is independent of the choices involved. It is the **fiber integration** of $H$-cohomology along $p : E \to B$.

#### Along representable morphisms of stacks

The above definition generalizes to one of push-forward
in generalized cohomology on [[stacks]] over [[SmthMfd]]
along [[representable morphisms of stacks]].

(...)

### In generalized differential cohomology

See

* [[fiber integration in differential cohomology]]

  * [[fiber integration in ordinary differential cohomology]]

  * [[fiber integration in differential K-theory]]


### In KK-theory
 {#InKKTheory}

We discuss fiber integration/push-forward/[[Gysin maps]] in 
[[operator K-theory]], hence in [[KK-theory]] ([Connes-Skandalis 85](#ConnesSkandalis84), [BMRS 07, section 3](#BMRS07)).

The following discusses KK-pushforward

1. _[Along an embedding](#KKPushForwardAlongEmbedding)_

1. _[Along a submersion](#KKPushforwardAlongSubmersion)_

1. _[Along a fibration of closed spin^c manifolds](#AlongAFibrationOfClosedSpinCManifolds)_

1. _[Along a general K-oriented map](#KKPushforwardAlongGeneralMap)_

1. _[In twisted K-theory](#KKPushforwardAlongGeneralMap)_


The construction goes back to ([Connes 82](#Connes82)), where it is given over smooth manifolds. Then ([Connes-Skandalis 84](#ConnesSkandalis84), [Hilsum-Skandalis 87](#HilsumSkandalis87)) generalize this to maps between [[foliations]] by KK-elements betwen the [[groupoid convolution algebras]] of the coresponding [[holonomy groupoids]] and  ([Rouse-Wang 10](#RouseWang10)) further generalize to the case where a [[circle 2-bundle]] twist is present over these foliations. A purely algebraic generalization to (K-oriented) maps between otherwise arbitrary [[noncommutative topology|noncommutative spaces]]/[[C*-algebras]] is in ([BMRS 07](#BMRS07)).

#### Along an embedding
 {#KKPushForwardAlongEmbedding}

([Connes-Skandalis 84, above prop. 2.8](ConnesSkandalis84))

Let $h \colon X \hookrightarrow Y$ be an [[embedding]] of [[compact topological space|compact]] [[smooth manifolds]]. 

The push-forward constructed from this is supposed to be an element in [[KK-theory]]

$$
  h! \colon KK_d(C(X), C(Y))
$$

in terms of which the push-forward on [[operator K-theory]] is induced by postcomposition: 

$$
  h_! 
    \;\colon\;
  K^\bullet(X) 
   \simeq 
  KK_\bullet(\mathbb{C}, X)
  \stackrel{h!\circ (-)}{\to}
  KK_{\bullet+d}(\mathbb{C},Y)
  \simeq
 KK^{\bullet+d}(Y)
 \,,
$$

where $d = dim(X) - dim(Y)$. 


Now, if we could "thicken" $X$ a bit, namely to a [[tubular neighbourhood]] 

$$
  h  \;\colon\; X \hookrightarrow U \stackrel{j}{\hookrightarrow} Y
$$ 

of $h(X)$ in $Y$ without changing the K-theory of $X$, then the element in question will just be the KK-element

$$
  j! \in KK(C_0(U), C(Y))
$$

induced directly from the [[C*-algebra]] homomorphism $C_0(U) \to C(Y)$ from the [[algebra of functions]] [[vanishing at infinity]] of $U$ to functions on $Y$, given by extending these functions by 0 to functions on $Y$.
Or rather, it will be that element composed with the assumed KK-equivalence

$$
  \psi \colon C(X) \stackrel{\simeq_{KK}}{\to} C_0(U)
  \,.
$$

The bulk of the technical work in constructing the push-forward is in constructing this equivalence. ([BMRS 07, example 3.3](#BMRS07))

In order for it to exist at all, assume that the [[normal bundle]]

$$
  N_Y X \coloneqq h^\ast(T Y)/ T X
$$

has a [[spin^c structure]]. Write $S(N_Y X)$ for the associated [[spinor bundle]]. 

Then there is an invertible element in [[KK-theory]]

$$
  \iota^X! \in KK_n(C(X), C_0(N_Y X))
$$

hence a KK-equivalence $\iota^X! \colon C(X) \stackrel{\simeq}{\to} C_0(N_Y X)$, where $C_0(-)$ denotes the [[algebra of functions]] [[vanishing at infinity]].

This is defined as follows. Consider the pullback $\pi_n^\ast S(N_Y X) \to N_Y X$ of this spinor to the normal bundle itself along the projection $\pi_N \colon N_Y X \to X$.  Then...

Moreover, a choice of a [[Riemannian metric]] on $X$ allows to find a [[diffeomorphism]] between the [[tubular neighbourhood]] $U_{h(X)}$ of $h(X)$ and a neighbourhood of the zero-section of of the normal bundle

$$
  \Phi \colon U_{h(X)} \hookrightarrow N_Y X
  \,.
$$

This induces a KK-equivalence

$$
  [\Phi] \colon C_0(N_Y X) \stackrel{\simeq_{KK}}{\to} C_0(U)
  \,.
$$

Therefore the push-forward in operator K-theory along $f \colon X \hookrightarrow Y$ is given by postcomposing in [[KK-theory]] with

$$
  h! \colon
  C(X)
    \underoverset{\simeq_{KK}}{i^X!}{\to}
  C_0(N_Y X)
    \underoverset{\simeq_{KK}}{\Phi}{\to}
  C_0(U)
    \stackrel{j!}{\to}
  C(Y)
  \,.
$$



#### Along a proper submersion
 {#KKPushforwardAlongSubmersion}

([Connes-Skandalis 84, above prop. 2.9](ConnesSkandalis84))


For $\pi \colon X \to Z$ a [[K-orientation|K-oriented]] [[proper map|proper]] [[submersion]] of compact smooth manifolds, the push-forward map along it is reduced to the [above](#KKPushForwardAlongEmbedding) case of an embedding by 

1. using that by the [[Whitney embedding theorem]] every compact $X$ may be embedded into some $\mathbb{R}^{2q}$ such as to yield an embedding

   $$
     h \colon X \to Z \times \mathbb{R}^{2 q} 
   $$ 

1. using that there is a KK-equivalence 

   $$
     \iota^Z! \colon C(Z) \stackrel{\simeq_{KK}}{\to} C_0(Z \times \mathbb{R}^{2q})
     \,.
   $$

The resulting push-forward is then given by postcomposition in [[KK-theory]] with

$$
  \pi! \colon C(X) \stackrel{h!}{\to} C_0(Z \times \mathbb{R}^{2}q)
   \underoverset{\simeq_{KK}}{(\iota^Z!)^{-1}}{\to} 
  C(Z)
  \,.
$$

([BMRS 07, example 3.4](#BMRS07))

#### Along a smooth fibration of closed $Spin^c$-manifolds
 {#AlongAFibrationOfClosedSpinCManifolds}

Specifically, for $\pi \colon X \to Z$ a smooth fibration over a closed smooth manifold whose [[fibers]] $X/Z$ are

* [[closed manifold|closed]] [[smooth manifolds|smooth]] [[spin^c structure|spin^c]] [[manifolds]] of even [[dimension]]

the push-forward element $\pi! \in KK(C_0(X), C_0(Z))$ is given by the [[Fredholm module|Fredholm]]-[[Hilbert module]] obatined from the fiberwise [[spin^c Dirac operator]] acting on the fiberwise [[spinors]]. ([Connes-Skandalis 84, proof of lemma 4.7](ConnesSkandalis84), [BMRS 07, example 3.9](BMRS07)).

In detail, write

$$
  T(X/Z) \hookrightarrow T X
$$

for the sub-bundle of the total [[tangent bundle]] on the [[vertical vectors]] and choose a [[Riemannian metric]] $g^{X/Z}$ on this bundle (hence a collection of Riemannian metric on the fibers $X/Z$ smoothly varying along $Z$). Write $S_{X/Z}$ for the corresponding [[spinor bundle]]. 

A choice of horizontal complenet $T X \simeq T^H X \oplus T(X/Z)$ induces an [[affine connection]] $\nabla^{X/Z}$. This combined with the [[symbol map]]/Clifford multiplication of $T^\ast (X/Z)$ on $S_{X/Z}$ induces a fiberwise [[spin^c Dirac operator]], acting in each fiber on the [[Hilbert space]] $L^2(X/Z, S_{X/Z})$. 

This yields a [[Fredholm module|Fredholm]]-[[Hilbert bimodule]]

$$
  (D_{X/Z}, L^2(X/Z, S_{X/Z}))
$$

which defines an element in [[KK-theory]]

$$
  \pi ! \in KK(C_0(X), C_0(Z))
  \,. 
$$

Postcompositon with this is the push-forward map in K/KK-theory, equivalently the [[index]] map of the collection of Dirac operators.






#### Along a general K-oriented map
 {##KKPushforwardAlongGeneralMap}

([Connes-Skandalis 84, def. 2.1](ConnesSkandalis84))


Now for $f \colon X \to Y$ an arbitray [[K-orientation|K-oriented]] smooth proper map, we may reduce push-forward along it to the above two cases by factoring it through its [[graph map]], followed by projection to $Y$:

$$
  f \;\colon\;
  X \stackrel{graph(f)}{\to}
  X \times Y
  \stackrel{p_Y}{\to}
  Y
  \,.
$$

Hence push-forward along such a general map is postcomposition in [[KK-theory]] with

$$
  f! \coloneqq p_Y !\circ graph(f)!
  \,.
$$

([BMRS 07, example 3.5](#BMRS07))


#### In twisted K-theory
 {#KKPushforwardAlongGeneralMap}

We discuss push forward in K-theory more generally by [[Poincaré duality C*-algebras]] hence [[dual objects]] in [[KK-theory]].

Let $i \colon Q \to X$ be a map of [[compact topological space|compact]] [[manifolds]] and let $\chi \colon X \to B^2 U(1)$ modulate a [[circle 2-bundle]] regarded as a [[twisted K-theory|twist for K-theory]]. Then forming [[twisted groupoid convolution algebras]] yields a [[KK-theory]] morphism of the form

$$
  C_{i^\ast \chi}(Q)
  \stackrel{i^\ast}{\longleftarrow}
  C_{\chi}(X)
  \,,
$$

with notation as in [this definition](Poincar&#233;+duality+algebra#CStarAlgebraOf2BundleOnManifold). By [this proposition](Poincar&#233;+duality+algebra#DualOfCompactManifoldWithTwist) the [[dual morphism]] is of the form

$$
  C_{\frac{W_3(\tau_Q)}{i^\ast \chi}}(Q)
  \stackrel{i_!}{\longrightarrow}
  C_{\frac{W_3(\tau_X)}{\chi}}(X)
  \,.
$$

If we assume that $X$ has a [[spin^c structure]] then this is

$$
  C_{\frac{W_3(\tau_Q)}{i^\ast \chi}}(Q)
  \stackrel{i_!}{\longrightarrow}
  C_{\frac{1}{\chi}}(X)
  \,.
$$

Postcomposition with this map in [[KK-theory]] now yields a map from the $\frac{W_3(\tau_Q)}{i^\ast \chi}$-[[twisted K-theory]] of $Q$ to the $\chi^{-1}$-[[twisted K-theory]] of $X$:

$$
  i_! \colon K_{\bullet + W_3(\tau_Q) - i^\ast \chi}(Q) \to K_{\bullet -\chi}
  \,.
$$

If we here think of $i \colon Q \hookrightarrow X$ as being the inclusion of a [[D-brane]] [[worldvolume]], then $\chi$ would be the class of the [[background gauge field|background]] [[B-field]] and an element 

$$
  [\xi] \in K_{\bullet + W_3(\tau_Q) - i^\ast \chi}(Q)
$$ 

is called (the K-class of) a _[[Chan-Paton gauge field]]_ on the D-brane satisfying the _[[Freed-Witten-Kapustin anomaly cancellation]]_ mechanism. (The orginal _[[Freed-Witten anomaly cancellation]]_ assumes $\xi$ given by a [[twisted unitary bundle|twisted line bundle]] in which case it exhibits a [[twisted spin^c structure]] on $Q$.) Finally its [[fiber integration|push-forward]]

$$
  [i_! \xi] \in K_{\bullet- \chi}(X)
$$

is called the corresponding _[[D-brane charge]]_.

## Examples

### To the point

When $B$ is a point, one obtains integration aginst the [[fundamental class]] of $E$, 
$$
\int_E:H^\bullet(E)\to H^{\bullet-dim E}(*)
$$
taking values in the coefficients of the given cohomology theory. Note that in this case $\Sigma^n B_+=S^n$, and this hints to a relationship between the Thom-Pontryagin construction and [[Spanier-Whitehead duality]]. And indeed [[Atiyah duality]] gives a homotopy equivalence between the [[Thom spectrum]] of the stable normal bundle of $E$ and the Spanier-Whitehead dual of $E$.
...

## Related concepts

* [[Grothendieck-Riemann-Roch theorem]]

* [[geometric quantization by push-forward]]

* [[twisted Umkehr map]]

[[!include generalized fiber integration synonyms - table]]

## References

### General

Fiber integration of differential forms is discussed in section VII of volume I of

* [[Werner Greub]], [[Stephen Halperin]], [[Ray Vanstone]], _[[Connections, Curvature, and Cohomology]]_ Academic Press (1973)

A quick summary can be found from [slide 14](http://www.math.wisc.edu/~gstgc/slides/Koytcheff.pdf#page=14) on in

* [[Robin Koytcheff]], _A homotopy-theoretic view of Bott-Taubes integrals_ ([pdf slides](http://www.math.wisc.edu/~gstgc/slides/Koytcheff.pdf))

More details are in 

* [[Ralph Cohen]], [[John Klein]], _Umkehr Maps_ ([arXiv:0711.0540](http://arxiv.org/abs/0711.0540))

### In noncommutative topology and KK-theory
 {#ReferencesInKKTheory}

Push-forward in [[twisted K-theory]] is discussed in 

* [[Alan Carey]], [[Bai-Ling Wang]], _Thom isomorphism and Push-forward map in twisted K-theory_ ([arXiv:math/0507414](http://arxiv.org/abs/math/0507414))
 {#CareyWang05}

and section 10 of

* [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_, in Robert S. Doran, Greg Friedman, [[Jonathan Rosenberg]], _Superstrings, Geometry, Topology, and $C^*$-algebras_, Proceedings of Symposia in Pure Mathematics [vol 81](http://www.ams.org/bookstore-getitem/item=PSPUM-81), American Mathematical Society ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))
 {#AndoBlumbergGepner10}


Discussion of fiber integration [[Gysin maps]]/[[Umkehr maps]] in [[noncommutative topology]]/[[KK-theory]] as [above](#InKKTheory) is in the following references.

The definition of the element $f! \in KK(C(X), C(Y))$ for a $K$-oriented map $f \colon X \to Y$ between smooth manifolds goes back to section 11 in

* [[Alain Connes]], _A survey of foliations and operator algebras_, Proceedings of the A.M.S., 38, 521-628 (1982) ([pdf](http://www.alainconnes.org/docs/foliationsfine.pdf))
 {#Connes82}

The functoriality of this construction is demonstrated in section 2 of the following article, which moreover generalizes the construction to maps between [[foliations]] hence to KK-elements between [[groupoid convolution algebras]] of [[holonomy groupoids]]:

* [[Alain Connes]], [[Georges Skandalis]], _The longitudinal index theorem for foliations_. Publ. Res. Inst. Math. Sci. 20,
no. 6, 1139&#8211;1183 (1984) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.165.4218))
 {#ConnesSkandalis84}

More on this is in

* [[Michel Hilsum]], [[Georges Skandalis]], _Morphismes K-orient&#233; d'espace de feuille et fonctoralit&#233; en th&#233;orie de Kasparov_, Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 4, 20 no. 3 (1987), p. 325-390 ([numdam](http://www.numdam.org/item?id=ASENS_1987_4_20_3_325_0))
 {#HilsumSkandalis87}

(the article that introuced [[Hilsum-Skandalis morphisms]]).

This is further generalized to [[circle 2-bundle]]-twisted convolution algebras of foliations in 

* Paulo Carrillo Rouse, [[Bai-Ling Wang]], _Twisted longitudinal index theorem for foliations and wrong way functoriality_ ([arXiv:1005.3842](http://arxiv.org/abs/1005.3842))
 {#RouseWang10}

Dicussion for general [[C*-algebras]] is in section 3 of 

* Jacek Brodzki, [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]], _Noncommutative correspondences, duality and D-branes in bivariant K-theory_, Adv. Theor. Math. Phys.13:497-552,2009 ([arXiv:0708.2648](http://arxiv.org/abs/0708.2648))
 {#BMRS07}

and specifically including also [[twisted K-theory]] again (and the relation to [[D-brane charge]]) in section 7 of

* Jacek Brodzki, [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]], _D-Branes, RR-Fields and Duality on Noncommutative Manifolds_, Commun. Math. Phys. 277:643-706,2008 ([arXiv:hep-th/0607020](http://arxiv.org/abs/hep-th/0607020))
 {#BrodzkiMathaiRosenbergSzabo06}




[[!redirects Pontrjagin-Thom construction]]
[[!redirects Pontryagin-Thom construction]]

[[!redirects umkehr map]]
[[!redirects umkehr maps]]
[[!redirects Umkehr map]]
[[!redirects Umkehr maps]]

[[!redirects fiber integration in generalized cohomology]]
[[!redirects integration in generalized cohomology]]

[[!redirects push-forward in generalized cohomology]]

