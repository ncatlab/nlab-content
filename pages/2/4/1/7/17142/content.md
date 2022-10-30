
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

What is called _Thom's theorem_ or the _Pontrjagin-Thom isomorphism_ (due to [Thom 54](#Thom54), [Pontrjagin 55](#Pontrjagin55))) states that for a given universal [[G-structure]] the [[homotopy group of a spectrum|homotopy groups]] of the universal [[Thom spectrum]] $M G$ form the [[cobordism ring]]

$$
  \Omega^G_\bullet \simeq \pi_\bullet(M G)
$$

of manifolds with [[G-structure]], and that this [[isomorphism]] is exhibited by the [[Pontryagin-Thom construction]] (see [there](Pontrjagin-Thom+collapse+map#ForEmbeddingsIntoAnNSphere)).

More generally, for $X$ a [[topological space]], then the group of $G$-bordism classes of $G$-manifolds in $X$ is isomorphic to the [[generalized homology]] of $X$ with [[coefficients]] in $M G$:

$$
  \Omega^G_\bullet(X)
   \simeq
  \pi_\bullet( M G \wedge X_+)
   \simeq
  M G_\bullet(X)
$$

## Bordism

Throughout, let $\mathcal{B}$ be a multiplicative [[(B,f)-structure]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#BfStructure)).

+-- {: .num_defn #NegativeOfManifoldWithBfStructure}
###### Definition

Write $I \coloneqq [0,1]$ for the standard interval, regarded as a [[smooth manifold]] [[manifold with boundary|with boundary]]. For $c \in \mathbb{R}_+$ Consider its embedding

$$
  e \;\colon\; I \hookrightarrow \mathbb{R}\oplus \mathbb{R}_{\geq 0}
$$

as the arc

$$
  e \;\colon\; t \mapsto \cos(\pi t) \cdot e_1 + \sin(\pi t) \cdot e_2
  \,,
$$

where $(e_1, e_2)$ denotes the canonical [[linear basis]] of $\mathbb{R}^2$, and equipped with the structure of a manifold with normal [[framing]] structure ([def.](Introduction+to+Stable+homotopy+theory+--+S#ExamplesOfBfStructures)) by equipping it with the canonical framing

$$
  fr \;\colon\; t \mapsto \cos(\pi t) \cdot e_1 + \sin(\pi t) \cdot e_2
$$

of its [[normal bundle]]. 

Let now $\mathcal{B}$ be a [[(B,f)-structure]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#BfStructure)).  Then for $X \overset{i}{\hookrightarrow}\mathbb{R}^k$ any embedded manifold with $\mathcal{B}$-structure $\hat g \colon X \to B_{k-n}$ on its [[normal bundle]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#ManifoldWithBfStructure)), define its **negative** or **oientation reversal**  $-(X,i,\hat g)$ of $(X,i, \hat g)$ to be the restriction of the structured manifold

$$
  (X \times I \overset{(i,e)}{\hookrightarrow} \mathbb{R}^{k+2}, \hat g \times fr)
$$

to $t = 1$. 

=--


+-- {: .num_defn #BordismRelation}
###### Definition

Two closed manifolds of [[dimension]] $n$ equipped with normal $\mathcal{B}$-structure $(X_1, i_1, \hat g_1)$ and $(X_2,i_2,\hat g_2)$ ([def.](Introduction+to+Stable+homotopy+theory+--+S#ManifoldWithBfStructure)) are called **bordant** if there exists a [[manifold with boundary]] $W$ of dimension $n+1$ equipped with $\mathcal{B}$-strcuture $(W,i_W, \hat g_W)$ if its [[boundary]] with $\mathcal{B}$-structure restricted to that boundary is the [[disjoint union]] of $X_1$ with the negative of $X_2$, according to def. \ref{NegativeOfManifoldWithBfStructure}

$$
  \partial(W,i_W,\hat g_W)
    \simeq
  (X_1, i_1, \hat g_1)
    \sqcup
  -(X_2, i_2, \hat g_2)
  \,.
$$

=--

+-- {: .num_prop #BordismIsAnEquivalenceRelation}
###### Proposition

The [[relation]] of $\mathcal{B}$-[[bordism]] (def. \ref{BordismRelation}) is an [[equivalence relation]].

Write $\Omega^\mathcal{B}_{\bullet}$ for the $\mathbb{N}$-graded set of $\mathcal{B}$-bordism classes of $\mathcal{B}$-manifolds.

=--

+-- {: .num_prop #BordismGroupAndBordismRing}
###### Proposition

Under [[disjoint union]] of manifolds, then the set of $\mathcal{B}$-bordism equivalence classes of def. \ref{BordismIsAnEquivalenceRelation} becomes an $\mathbb{Z}$-graded [[abelian group]]

$$
  \Omega^{\mathcal{B}}_\bullet \in Ab^{\mathbb{Z}}
$$

(that happens to be concentrated in non-negative degrees). This is called the **$\mathcal{B}$-bordism group**.

Moreover, if the [[(B,f)-structure]] $\mathcal{B}$ is multiplicative ([def.](Introduction+to+Stable+homotopy+theory+--+S#BfStructure)), then [[Cartesian product]] of manifolds followed by the multiplicative composition operation of $\mathcal{B}$-structures makes the $\mathcal{B}$-bordism ring into a [[commutative ring]], called the **$\mathcal{B}$-bordism ring**.

$$
  \Omega^{\mathcal{B}}_\bullet \in CRing^{\mathbb{Z}}
  \,.
$$

=--

e.g. ([Kochmann 96, prop. 1.5.3](#Kochmann96))

## Thom's theorem

Recall that the [[Pontrjagin-Thom construction]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#PontrjaginThomConstruction)) associates to an embbeded manifold $(X,i,\hat g)$ with normal $\mathcal{B}$-structure ([def.](Introduction+to+Stable+homotopy+theory+--+S#ManifoldWithBfStructure)) an element in the [[stable homotopy group]] $\pi_{dim(X)}(M \mathcal{B})$ of the universal $\mathcal{B}$-[[Thom spectrum]] in degree the dimension of that manifold.

+-- {: .num_lemma #PontrjaginThomIsRingHomomorphims}
###### Lemma

For $\mathcal{B}$ be a multiplicative [[(B,f)-structure]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#BfStructure)),
the $\mathcal{B}$-[[Pontrjagin-Thom construction]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#PontrjaginThomConstruction)) is compatible with all the relations involved to yield a graded [[ring]] [[homomorphism]]

$$
  \xi
  \;\colon\;
  \Omega^{\mathcal{B}}_\bullet
    \longrightarrow
  \pi_\bullet(M \mathcal{B})
$$

from the $\mathcal{B}$-[[bordism ring]] (def. \ref{BordismGroupAndBordismRing}) to the [[stable homotopy groups]] of the universal $\mathcal{B}$-[[Thom spectrum]] equipped with the ring structure induced from the canonical [[ring spectrum]] structure ([def.](Introduction+to+Stable+homotopy+theory+--+S#UniversalThomSpectrumForBfStructure)).

=--

+-- {: .num_theorem}
###### Theorem

The ring homomorphsim in def. lemma \ref{PontrjaginThomIsRingHomomorphims} is an [[isomorphism]].

=--

Due to ([Thom 54](#Thom54), [Pontrjagin 55](#Pontrjagin55)). See for instance ([Kochmann 96, theorem 1.5.10](#Kochmann96)).




## Related entries

* [[Pontryagin-Thom collapse map]]

* [[Thom's transversality theorem]]

## References

Due to 

* {#Thom54} [[René Thom]], _Quelques propri&#233;t&#233;s globales des vari&#233;t&#233;s 
diff&#233;rentiables_ Comment. Math. Helv. 28, (1954). 17-86

* {#Pontrjagin55} [[Lev Pontrjagin]], _Smooth manifolds and their applications in Homotopy theory_, Trudy Mat. Inst. im Steklov, No 45, Izdat. Akad. Nauk. USSR, Moscow, 1955 (AMS Translation Series 2, Vol. 11, 1959)

Reviews include

* {#Stong68} [[Robert Stong]], _Notes on Cobordism theory_, 1968 ([toc pdf](http://pi.math.virginia.edu/StongConf/Stongbookcontents.pdf), [publisher page](http://press.princeton.edu/titles/6465.html))

* {#Kochmann96} [[Stanley Kochmann]], section 1.5 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

Further lecture notes include

* [[John Francis]], _Topology of manifolds_ course notes (2010) ([web](http://math.northwestern.edu/~jnkf/classes/mflds/)), Lecture 3: _Thom's theorem_ ([pdf](http://math.northwestern.edu/~jnkf/classes/mflds/3thom.pdf)),  Lecture 4 _Transversality_ (notes by I. Bobkova) ([pdf](http://math.northwestern.edu/~jnkf/classes/mflds/4transversality.pdf))


* {#Malkiewich11} [[Cary Malkiewich]], section 3 of _Unoriented cobordism and $M O$_, 2011 ([pdf](http://math.uiuc.edu/~cmalkiew/cobordism.pdf))

* Tom Weston, Part I of _An introduction to cobordism theory_ ([pdf](http://people.math.umass.edu/~weston/oldpapers/cobord.pdf)) 

* [[Manifold Atlas]], _[The Pontrjagin-Thom isomorphism](http://www.map.mpim-bonn.mpg.de/B-Bordism#The_Pontrjagin-Thom_isomorphism)_


[[!redirects Thom theorem]]

[[!redirects Pontrjagin-Thom theorem]]