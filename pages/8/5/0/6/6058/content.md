
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

This entry is about the article

* [[Alexander Kahle]], [[Alessandro Valentino]], _T-duality and Differential K-Theory_ ([arXiv:0912.2516](http://arxiv.org/abs/0912.2516))
 {#KahleValentino}

on the identification of the correct description in [[differential cohomology]] ([[ordinary differential cohomology]] and [[differential K-theory]]) of [[T-duality]] or [[topological T-duality]].

A review is in section 7.4 of 

* [[Ulrich Bunke]], [[Thomas Schick]], _Differential K-theory. A survey_ ([arXiv:1011.6663](http://arxiv.org/abs/1011.6663)).
 {#BunkeSchick}

We try to indicate some of the content. There are two main ingredients:

* a [formalization of the setup](#FormalizationOfTheSetup)

which proposes a refinement of the ingredients of [[topological T-duality]] to [[differential cohomology]]; and then the

* [statement of differential T-duality](#StatementOfDifferentialTduality),

which is the assertion that this setup naturally induces the T-duality operation as an [[isomorphism]] on [[twisted differential K-theory]].


## Formalization of the setup
 {#FormalizationOfTheSetup}


Let $\Lambda \subset \mathbb{R}^n$ be a [[lattice]] (an [[discrete group|discrete]] subgroup of the [[abelian group]] of [[real number]]s to the $n$th [[cartesian product|cartesian power]]).

Write 

$$
  \hat \Lambda := Hom_{Grp}(\Lambda, \mathbb{Z})
$$

for the dual lattice and

$$
  (-,-) : \lambda \times \hat \Lambda \to \mathbb{Z}
$$

for the canonical pairing (the [[evaluation map]]).

The [[quotient]] $\mathbb{R}^n / \Lambda$ is a [[torus]].
A $\mathbb{R}^n/\Lambda$-[[principal bundle]] is a [[torus]]-bundle. Write $B \mathb{R}^n/\Lambda \in $ [[Top]] for the [[classifying space]] and $\mathbf{B} \mathbb{R}^n / \Lambda$ for its [[moduli space]]: the [[smooth infinity-groupoid|smooth groupoid]] [[delooping]] the [[Lie group]] $\mathbb{R}/\Lambda$.

Torus bundles on a [[smooth manifold]] $X$ are classified by $H^2(X, \Lambda)$. Following the discussion at [[smooth ∞-groupoid]] we write here $\mathbf{H}(X, \mathbf{B}\mathbb{R})$ for the [[groupoid]] of smooth torus bundles and _smooth_ bundle morphisms between. Write $\mathbf{H}_{conn}(X,\mathbf{B} \mathbb{R}^n /\Lambda)$ for the corresponding differential refinement to bundles with [[connection on a bundle|connection]].

The tensor product of [[chain complex]]es

$$
  (\Lambda \to \mathbb{R}^n \to 0) \otimes
  (\hat \Lambda \to \mathbb{R}^n \to 0)
  \simeq
  (\Lambda \otimes \hat \Lambda \to (\Lambda \oplus \hat \Lambda) \otimes \mathbb{R}^n \to \mathbb{R}^{2n} \to 0 \to 0)
$$

induces (via the [[Dold-Kan correspondence]]) the [[cup product]] 

$$
  H^k_{diff}(X, \Lambda) \times
  H^l_{diff}(X, \hat \Lambda)
  \to 
  H^{k+l}_{diff}(X, \Lambda \otimes \hat \Lambda)
   \stackrel{(-,-)}{\to}
  H^{k+l}_{diff}(X, \mathbb{Z})
  \,.
$$

Differential T-duality relates differential cohomological structures on $\mathbb{R}^n / \Lambda$-principal bundles with that on certain dual $\mathbb{R}^n /\hat \Lambda$-principal bundles:

+-- {: .num_defn #DifferentialTDualityPair}
###### Definition

A **differential T-duality pair** is

* a [[smooth manifold]] $X$;

* a $\mathbb{R}^n/\Lambda$-[[principal bundle]] $P \to X$ with connection $\theta$ and a $\mathbb{R}^n / \hat \Lambda$-principal bundle $\hat P \to X$ with connection $\hat \theta$;

  such that the underlying topological class of the [[cup product]]
  $(P, \theta) \cup (\hat P, \hat \theta )$ is trivial;

* a choice of trivialization 
  
  $$
    \sigma 
     : 
    (0,C) \stackrel{\simeq}{\to} (P, \theta) \cup (\hat P , \hat \theta)
    \,.
  $$

=--

This is ([KahleValentino, def. 21](#KahleValentino)). It is the evident differential generalization of the description in [[topological T-duality]] that appears for instance around (7.11) of ([BunkeSchick](#BunkeSchick)).

+-- {: .num_remark}
###### Remark

We may refine this naturally to a **[[2-groupoid]] of twisted T-duality pairs** $TDualityPairs(X)_{conn}$, the [[homotopy pullback]]

$$
  \array{
    TDualityPairs(X)_{conn} &\stackrel{tw}{\to}& H^4_{diff}(X)
    \\
    \downarrow &\swArrow_{\sigma}& \downarrow
    \\
    \mathbf{H}(X, \mathbf{B}\mathbb{R}^n/\Lambda \times \mathbf{B} \mathbb{R}^n/\hat \Lambda)
    &\stackrel{}{\to}&
    \mathbf{H}(X, \mathbf{B}^3 U(1))_{conn}
  }
  \,.
$$

This is itself an example of [[twisted cohomology]] (as discussed there). (We use here the notation at _[[schreiber:differential cohomology in a cohesive topos]]_ .)

The differential T-duality pairs of def. \ref{DifferentialTDualityPair} are those elements $(P,\hat P, \sigma) \in TDualityPairs(X)_{conn}$ for which the [[twisted cohomology|twist]] $tw(P,\hat P, \sigma) \in H^4_{diff}(X)$ in [[ordinary differential cohomology]] has an underlying tricial [[circle n-bundle|circle 3-bundle]]. We could restrict the homotopy pullback to these, but it seems natural to include the full collection of twists. (Notice that these "twist" here are not the twists in "twisted K-theory", rather we are observing that already the notion of T-duality pairs itself is an example of cocycles in twisted cohomology in the general sense.)

Notice that the above analogous to the notion of _[[differential string structure]]s in $StringBund(X)_{tw,conn}$ over $X$: as discussed in detail there, this is the [[homotopy pullback]]

$$
  \array{
    StringBund(X)_{tw,conn} &\to& H^4_{diff}(X)
    \\
    \downarrow &\swArrow_{\sigma}& \downarrow
    \\
    \mathbf{H}(X, \mathbf{B}Spin \times \mathbf{B} SU)
    &\stackrel{\frac{1}{2}\hat \mathbf{p}_1 - \frac{1}{46}\hat \mathbf{c}}{\to}&
    \mathbf{H}(X, \mathbf{B}^3 U(1))_{conn}
  }
  \,.
$$


=--

+-- {: .num_defn }
###### Definition (roughly)

Write $\mathbf{H}_{diff,2}(X, \mathbf{B}^3 U(1))$ for a [[3-groupoid]] whose objects are cocycles in [[ordinary differential cohomology]] in degree 4, but whose morphisms need not preserve connections and are instead such that the [[automorphism]] [[2-groupoid]] of the 0-object is that of circle 2-bundles with connection $\mathbf{H}_{diff}(X, \mathbf{B}^2 U(1))$.

=--

A 1-groupoid truncation of this idea is the object denoted $\mathcal{H}^p(X)$ in [KahleValentino, A.2](#KahleValentino).

+-- {: .num_defn }
###### Remark

In terms of the notion of [[differential function complex]] we should simply set

$$
  \mathbf{H}_{diff,2}(X, \mathbf{B}^3 U(1))
  :=
  filt_1 ( H \mathbb{Z}_4)^X
  \,.
$$


(Notice the $filt_1$ instead of $filt_0$. ) By [this proposition](http://ncatlab.org/nlab/show/differential%20function%20complex#homotopy_groups_24) this has the right properties.
=--

## Statement of differential T-duality
 {#StatementOfDifferentialTDuality} 

(...)

category: reference