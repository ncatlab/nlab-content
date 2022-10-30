
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
  (-,-) : \Lambda \times \hat \Lambda \to \mathbb{Z}
$$

for the canonical pairing (the [[evaluation map]]). Notice that $\hat\Lambda$ is canonically identified with the lattice of $(\mathbb{R}^n)^*$ consisting of those linear functionals $\varphi:\mathbb{R}^n\to\mathbb{R}$ such that $\varphi(\Lambda)\subseteq \mathbb{Z}$. With this identification, the canonical pairing $\Lambda \times \hat \Lambda \to \mathbb{Z}$ can be seen as the restriction to $\Lambda \times \hat \Lambda$ of the canonical pairing $\mathbb{R}^n\otimes(\mathbb{R}^n)^*\to \mathbb{R}$.

The [[quotient]] $\mathbb{R}^n / \Lambda$ is a [[torus]].
A $\mathbb{R}^n/\Lambda$-[[principal bundle]] is a [[torus]]-bundle. Write $\mathcal{B}\mathbb{R}^n/\Lambda \in $ [[Top]] for the [[classifying space]] and $\mathbf{B} \mathbb{R}^n / \Lambda$ for its [[moduli space]]: the [[smooth infinity-groupoid|smooth groupoid]] [[delooping]] the [[Lie group]] $\mathbb{R}/\Lambda$.

Torus bundles on a [[smooth manifold]] $X$ are classified by $H^2(X, \Lambda)$. Following the discussion at [[smooth ∞-groupoid]] we write here $\mathbf{H}(X, \mathbf{B}\mathbb{R}^n/\Lambda)$ for the [[groupoid]] of smooth torus bundles and _smooth_ bundle morphisms between. Write $\mathbf{H}_{conn}(X,\mathbf{B} \mathbb{R}^n /\Lambda)$ for the corresponding differential refinement to bundles with [[connection on a bundle|connection]].

The tensor product of [[chain complex]]es

$$
  (\Lambda \to \mathbb{R}^n \to 0) \otimes
  (\hat \Lambda \to (\mathbb{R}^n)^* \to 0)
  \simeq
  (\Lambda \otimes \hat \Lambda \to \Lambda\otimes (\mathbb{R}^n)^* \oplus \mathbb{R}^n\otimes \hat \Lambda) \to \mathbb{R}^{n}\oplus(\mathbb{R}^n)^* \to 0 \to 0)
$$
together with the map of complexes
$$
(\Lambda \otimes \hat \Lambda \to \Lambda\otimes (\mathbb{R}^n)^* \oplus \mathbb{R}^n\otimes \hat \Lambda \to \mathbb{R}^{n}\oplus(\mathbb{R}^n)^* \to 0 \to 0)\to 
(\Lambda \otimes \hat \Lambda \to 0 \to 0 \to 0 \to 0)\stackrel{(-,-)}{\to}
(\mathbb{Z}\to 0\to 0\to 0\to 0)
$$
induces (via the [[Dold-Kan correspondence]]) the [[cup product]] 
$$
  H^k(X, \Lambda) \times
  H^l(X, \hat \Lambda)
  \to 
  H^{k+l}(X, \Lambda \otimes \hat \Lambda)
   \stackrel{(-,-)}{\to}
  H^{k+l}(X, \mathbb{Z})
  \,.
$$
This is conveniently seen as a manifestation of the morphism of smooth groupoids
$$
\mathbf{B}\mathbb{R}^n/\Lambda\times \mathbf{B}(\mathbb{R}^n)^*/\hat\Lambda\to \mathbf{B}^4\mathbb{Z}.
$$
This can in turn be naturally refined as follows: instead of truncating the amove morphism of chain complexes at the bottom level, consider the lenght two truncation:
$$
(\Lambda \otimes \hat \Lambda \to \Lambda\otimes (\mathbb{R}^n)^* \oplus \mathbb{R}^n\otimes \hat \Lambda \to \mathbb{R}^{n}\oplus(\mathbb{R}^n)^* \to 0 \to 0)\to 
(\Lambda \otimes \hat \Lambda \to \Lambda\otimes (\mathbb{R}^n)^* \oplus \mathbb{R}^n\otimes \hat \Lambda \to 0 \to 0 \to 0)\stackrel{(-,-)}{\to}
(\mathbb{Z}\to \mathbb{R}\to 0\to 0\to 0)
$$
_(here there is a normalization factor $1/2$ to be taken into account: in the evaluation map $\Lambda\otimes (\mathbb{R}^n)^* \oplus \mathbb{R}^n\otimes \hat \Lambda\to \mathbb{R}$)_
giving the
morphism of smooth groupoids
$$
\mathbf{B}\mathbb{R}^n/\Lambda\times \mathbf{B}(\mathbb{R}^n)^*/\hat\Lambda\to \mathbf{B}^3(\mathbb{Z}\to \mathbb{R})\simeq \mathbf{B}^3\mathbf{U}(1).
$$
Differential T-duality is (the homotopy fiber of) the lifting of this morphism to a morphism
$$
(\mathbf{B}\mathbb{R}^n/\Lambda)_{conn}\times (\mathbf{B}(\mathbb{R}^n)^*/\hat\Lambda)_{conn}\to \mathbb{R})\simeq \mathbf{B}^3\mathbf{U}(1)_{conn}
$$
It relates differential cohomological structures on $\mathbb{R}^n / \Lambda$-principal bundles with that on certain dual $(\mathbb{R}^n)^* /\hat \Lambda$-principal bundles:

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

+-- {: .num_lemma }
###### Lemma

The choice $\sigma$ of the trivialization of the cup product of the two torus bundles induces canonically elments in degree 3 ordinary differential cohomology (two [[circle n-bundle with connection|circle 2-bundles with connection]]) on $P$ and on $\hat P$, respectively, whose pullbacks to the [[fiber product]] $P \times_X \hat P$ are equivalent there.

=--

This is ([KahleValentino, 2.2, 2.3](#KahleValentino)), where an explicit construction of the classes and their equivalence is given.

+-- {: .num_remark }
###### Remark

This is a special case of the general statement about extensions of higher bundles discussed <a href="http://www.ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos+--+structures#ExtendedBundlesByBundlesOfExtensions">here</a>:

Let $A \to \mathbf{B} \mathbb{R}^n / \Lambda \times \mathbf{B} \mathbb{R}^n / \hat \Lambda$ be the [[homotopy fiber]] of the pairing class $\mathbf{B} \mathbb{R}^n / \Lambda \times \mathbf{B} \mathbb{R}^n / \hat \Lambda \to \mathbf{B}^3 U(1)$. This leads to the long [[fiber sequence]] (as discussed there)

$$
  \cdots \to \mathbf{B}^2 U(1) \to A \to \mathbf{B} \mathbb{R}^n / \Lambda \times \mathbf{B} \mathbb{R}^n / \hat \Lambda \to \mathbf{B}^3 U(1) 
$$

The characteristic map $X \to \mathbf{B} \mathbb{R}^n / \Lambda \times \mathbf{B} \mathbb{R}^n / \hat \Lambda$ of a pair of torus bundles $P , \hat P \to X$ factors through $A$ precisely if these form a T-duality pair. Such a factorization induces a $\mathbf{B} U(1)$-[[principal 2-bundle]] on the [[fiber product]] $P \times_X \hat P$. This follows from the following [[pasting diagram]] of [[homotopy pullback]]s

$$
  \array{
    P \times_X \hat P &\stackrel{\tilde \tau}{\to}& \mathbf{B}^2 U(1) &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    X &\to& A & \to & \mathbf{B} \mathbb{R}^n / \Lambda \times \mathbf{B} \mathbb{R}^n / \hat \Lambda 
  }
  \,.
$$

The $\tilde \tau$ here is the class on the fiber product in question.

Notice that in the top left we indeed have $P \times_X \hat P$: the bottom left homotopy pullback of the product coefficients is equivalently given by the following pasting composite of homotopy pullbacks

$$
  \array{
     && && P \times_X \hat P
     \\
     && & \swarrow && \searrow
     \\
     && P &&&& \hat P
     \\
     & \swarrow && \searrow && \swarrow && \searrow
     \\
     * && && X && && *
     \\
     & \searrow && \swarrow && \searrow && \swarrow
     \\
     && \mathbf{B}\mathbb{R}^n / \Lambda 
     && && \mathbf{B}\mathbb{R}^n / \hat \Lambda
  }
  \,.
$$

Notice also that this is again directly analogous to the situation for [[string structure]]s: as discussed there, a string structure on $X$ induces a $\mathbf{B}U(1)$-2-bundle on the total space of a $Spin$-principal bundle over $X$. 

=--

## Statement of differential T-duality
 {#StatementOfDifferentialTDuality} 

(...)

category: reference