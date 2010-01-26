<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}


## Idea ##

Motivic cohomology was for a long time a hypothetical [[cohomology]] theory of [[scheme]]s whose hypothetical existence [[Alexander Grothendieck]] proposed in the 1960s should be the underlying reason for what are called the [[standard conjectures on algebraic cycles]].

Several different realizations of this hypothetical cohomology theory have been proposed:

1. The proposal due to Morel (?) based on Morel-Voevodsky's [[A1-homotopy theory]] effectively identifies motivic cohomology with the cohomology as given in the [[(∞,1)-topos]] $\mathbf{H}_{Nis}$ of [[∞-stack]]s on the [[Nisnevich site]], following the general notion of [[cohomology]] (as described there): for $X$ a [[scheme]] and $A \in \mathbf{H}_{Nis}$ some coefficient object, the motivic cohomology of $X$ with coefficients in $A$ is the connected components of the [[derived hom space|(∞,1)-categorical hom-space]] of morphisms from $X$ to $A$:

   $$
     H_{motivic}(X,A)  = \pi_0 \mathbf{H}_{Nis}(X,A)
     \,.
   $$

    More precisely, the full $\mathbf{H}_{Nis}$ knows about what would be called the [[nonabelian cohomology]] generalization of motivic cohomology: motivic cohomology proper is the special case of this where coefficient objects $A$ are taken to be [[spectrum object]]s with respect to the [[Tate sphere]] built from $\mathbb{A}^1$ and taken to be [[A1-homotopy theory|A1-homotopy invariant]]. 

   This is described in the section [Homtopy stabilization of the (∞,1)-topos on Nis](#InfStackDef) below.

1. Another proposal has been put forward by Voevodsky. More on this in the section [Voevodsky's definition](#VoevodskysDef) below.


## Homotopy stabilization of the $(\infty,1)$-topos on $Nis$ {#InfStackDef}

Write 

* $Nis$ for the [[Nisnevich site]]

* $\mathbf{H}_{Nis}$ for the [[(∞,1)-topos]] of [[∞-stack]]s on $Nis$;

* $\mathbf{H}_{Nis}^{I}$ for its [[homotopy localization]], its 
  [[A1-homotopy theory]];

* $Stab_T(\mathbf{H}_{Nis}^I)$ for the geometric [[stabilization]] of 
  $\mathbf{H}_{Nis}^I$ at the [[Tate sphere]]s. This 
  produces the $T$-[[spectrum object]]s in $\mathbf{H}_{Nis}$.

Then motivic [[cohomology]], and motivic [[homotopy]] are given by connected components of [[derived hom space|(∞,1)-categorical hom-space]]s in $Stab_T(\mathbf{H}_{Nis}^I)$.

There is a standard way to _[[presentable (∞,1)-category|present]]_ all this structure:

* as described at [[models for ∞-stack (∞,1)-toposes]], the standard way to [[presentable (∞,1)-category|present]] $\mathbf{H}_{Nis}$ is in terms of the [[model structure on simplicial presheaves]] on $Nis$

* then the [[homotopy localization]] is modeled by 
  the corresponding [[Bousfield localization of model categories|left Bousfield localization]] of this model structure;

* and finally the [[stabilization]] may be modeled by further Bousfield
  localization at all suspension morphism  $T \wedge X \to X$ for  
  $T = \mathbb{A}^1/(\mathbb{A}^1-{0})$ 
  a suitable model of the circle and $\wedge$ the internal 
  [[smash product]].

### References

A concise overview of the constructions and definitions just outlined above is in

* J. F. Jardine, _Motivic spaces and the motivic stable category_ 
  ([pdf](http://www.aimath.org/WWN/motivesdessins/motivic.pdf))

More details on the [[Nisnevich site]], the [[model structure on simplicial presheaves]] on it and its [[homotopy localization]] to [[A1-homotopy theory]] is in [section 3](http://www.math.uiuc.edu/K-theory/0305/nowmovo.pdf#page=60) of

* [[Fabien Morel]], [[Vladimir Voevodsky]], _$\mathbb{A}^1$-homotopy theory of schemes_ ,  K-theory, 0305 ([web](http://www.math.uiuc.edu/K-theory/0305/) [pdf](http://www.math.uiuc.edu/K-theory/0305/nowmovo.pdf))

### Chow groups as cohomology with coefficients in Eilenberg-MacLane objects {#ChowGroupsAsInfStackCohomology}

In any [[(∞,1)-topos]] $\mathbf{H}$, the most important notion of [[cohomology]] is that with coefficients in the corresponding 
[[Eilenberg-MacLane object]]s $K(A,n)$

$$
  H^n(X,A) := \pi_0 \mathbf{H}(X, K(A,n))
  \,.
$$

For instance in [[Top]] this gives the
"ordinary" cohomology, for instance [[integral cohomology]] for $A = \mathbb{Z}$.

In the [[∞-stack]] [[(∞,1)-topos]] $\mathbf{H}_{Nis}$ cohomology with  coefficients in the corresponding [[Eilenberg-MacLane object]]s identifies with the notion of [[Chow group]]s.

> the following paragraphs are due to [[Denis-Charles Cisinski]],
  taken from [this MathOverflow thead](http://mathoverflow.net/questions/2520/homotopy-theory-of-schemes-examples).

To keep things simple, let us assume we work over a [[perfect field]]. The easiest part of motivic cohomology which we can get is the [[Picard group]] (i.e. the [[Chow group]] in degree 2). This works essentially like in [[Top]]: in the [[model structure on simplicial presheaves|(model) category of simplicial Nisnevich sheaves]] (over smooth $k$-schemes), the classifying space of the multiplicative group $\mathbb{G}_m := \mathbb{A}^1 - \{0\}$  has the $\mathbb{A}^1$-[[homotopy n-type|homotopy type]] of the infinite dimensional projective space. 

Moreover, as the Picard group is homotopy invariant for regular schemes (semi-normal is even enough), the fact that $H^1(X,\mathbb{G}_m) = Pic(X)$ reads as

$$
  \pi_0 \mathbb{H}_{Nis}(X,\mathbf{B} \mathbb{G}_m)
  = 
  Ho(SSh(Nis))(X, \mathbb{B} \mathbf{B} \mathbb{G}_m)
  =
  Pic(X)
  = 
  CH^2(X)
  \,
$$

where $\pi_0 \mathbf{H}_{Nis}(-,-) = Ho(SSh(Nis))(-,-)$ stands for the [[hom-set]] in the [[homotopy category]] of $k$-schemes.

In general, we denote by $K(\mathbb{Z}(n),2n)$ the $n$-th motivic 
[[Eilenberg-MacLane object]], i.e. the object of $Ho(SSh(Nis))$ which represents the $n$-th [[Chow group]] in $Ho(SSh(Nis))$: for any smooth $k$-scheme $X$, one has

$$
  \pi_0 \mathbf{H}(\Sigma^i X , K(\mathbb{Z}(n)), 2n))
  =
  Ho(SSh(Nis))(\Sigma^i X , K(\mathbb{Z}(n)), 2n))
  = 
  H^{2n -i}(X, \mathbb{Z}(n))
  \,.
$$

There are several models for $K(\mathbb{Z}(n),2n)$, one of the smallest being constructed as follows. What is explained above is that $K(\mathbb{Z}(1),2)$ is the infinite projective space. $K(\mathbb{Z}(0),0)$ is simply the constant sheaf . For higher $n$, here is the following construction (this is Voevodsky's).

Given a $k$-scheme $X$, denote by $L(X)$ the [[presheaf with transfers]] associated to $X$, that is the presheaf of abellian groups whose sections over a smooth $k$-scheme $V$ are the finite [[correspondence]]s from $V$ to $X$ (i.e. the finite linear combinations of cycles $\Sum n_i Z_i$  in $V \times X$ such that $Z_i$ is finite and surjective over $V$). This is a presheaf, where the pullbacks are defined using the pullbacks of cycles (the condition that the $Z_i$; are finite and surjective over a smooth (hence normal) scheme $V$ makes that this is well defined without working up to rational equivalences, and as we consider only pullbacks along maps $U \to V$ with $U$ and $V$ smooth (hence regular) ensures that the multiplicities which will appear from these pullbacks will always be integers). The [[presheaf]] $L(X)$ is a [[sheaf]] for the [[Nisnevich topology]]. This construction is functorial in $X$ (we will need this functoriality only for closed immersions).

Let $X$ (resp. $Y$) be the cartesian product of $n$ (resp. $n-1$) copies of the projective line. The point at infinity gives a family of $n$ maps $u_i : Y \to X$. Then a model of the [[Eilenberg-MacLane object]] $K(\mathbb{Z}(n), 2n)$ in $\mathbf{H}_{Nis}$ is the sheaf of sets obtained as the quotient (in the category of Nisnech sheaves of abelian groups) of $L(X)$ by the subsheaf generated by the images of the maps $L(u_i) : L(Y) \to L(X)$.




## Voevodsky's definition {#VoevodskysDef}

In the mid 1990s [[Vladimir Voevodsky]] proposed a concrete definition of motivic cohomology of a smooth [[scheme]] $X$ over a field as the [[hypercohomology]] of certain [[complex of sheaves]] on the [[Zariski site|Zariski]] or [[etale cohomology|etale]] [[site]] of $X$ (an analog of the [[category of open subsets]] of a [[topological space]]). This complex is called the **motivic complex**; the existence of such a complex was predicted as part of the so-called Beilinson dream. 

Voevodsky gave a concrete definition of the [[derived category]] of the hypothetical category of [[mixed motive|mixed motives]]. The [[category of motives]] has not only more objects but also locally more morphisms than the category of schemes, and it comes with a [[functor]] from an appropriate category of schemes.  The morphisms are certain [[correspondence]]s, and Voevodsky has shown that the motivic complexes are realized as derived hom-complexes in his derived category of mixed motives.

Voevodsky's proposal has been shown to have most properties that Grothendieck and Beilinson had demanded of the hypothetical cohomology theory, except that to date it hasn't been shown yet that the cohomology groups vanish in negative degree, as they should.




The **motivic complex** -- a [[chain complex]] of [[sheaf|sheaves]] with values in abelian groups -- is defined in [definition 3.1, page 33](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf#page=33) of 

* Carlo Mazza, Vladimir Voevodsky and Charles Weibel, _Lectures in motivic cohomology_ ([web](http://math.rutgers.edu/~weibel/motiviclectures.html) [pdf](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf))

+-- {: .un_defn}
###### Definition
The motivic cohomology of a [[smooth scheme]] $X$ is the [[abelian sheaf cohomology]], more specifically hypercohomology, of the motivic complex of sheaves with transfers on the Zariski site. See [definition 3,4, page 22](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf#page=34).
=--

The analogous definition with the Zariski [[site]] structure of $X$ replaced by the [[etale cohomology|etale site]] $Et(X)$ is in [lecture 10](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf#page=87).


### As hom-sets of motives

Motivic cohomology computes certain derived hom-sets in the [[motive|category of motives]].

This is discussed in [lecture 14](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf#page=121) of [MaVoWe](http://math.rutgers.edu/~weibel/motiviclectures.html). See [prop 14.16](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf#page=126).


### References ##

* [[Carlo Mazza]], [[Vladimir Voevodsky]] and [[Charles Weibel]], _Lectures in motivic cohomology_ ([web](http://math.rutgers.edu/~weibel/motiviclectures.html) [pdf](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf))

## Further references

* [[Eric Friedlander]], _[Algebraic Cycles and algebraic K-theory, II](http://www.math.northwestern.edu/~eric/lectures/)_ ([lecture 6 (pdf)](http://www.math.northwestern.edu/~eric/lectures/ihp/ihplec6.pdf))

* J. F. Jardine, _Motivic symmetric spectra_, Doc. Math. 5 (2000), 445--553

* [[Alexander Beilinson|A. Be?linson]], R. MacPherson, V. Schechtman, _Notes on motivic cohomology_,  Duke Math. J.  54  (1987),  no. 2, 679--710; [doi](http://dx.doi.org/10.1215/S0012-7094-87-05430-5).

[[!redirects motivic complex]]
[[!redirects motivic complexes]]