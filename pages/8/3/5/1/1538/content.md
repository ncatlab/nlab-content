

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Dijkgraaf-Witten theory_ in dimension $n$ is the [[TFT|topological]] [[sigma-model]] [[quantum field theory]] whose [[target space]] is the [[classifying space]] of a [[discrete group]] and whose 
[[background gauge field]] is a [[circle n-bundle with connection]] on $\mathbf{B}G$ (necessarily flat) which is equivalently a [[cocycle]] in the [[group cohomology]] of $G$ with coefficients in the [[circle group]].

Viewed in a broader context and generalizing: Dijkgraaf-Witten theory is the [[schreiber:∞-Chern-Simons theory]] induced from a [[characteristic class]] $\mathbf{c} : \mathbf{B}G \to \mathbf{B}^n U(1)$ on a [[discrete ∞-groupoid]] $\mathbf{B}G := Disc B G$. If $G$ here is an ordinary [[discrete group]] this is traditional Dijkgraaf-Witten theory, if $G$ is a discrete [[2-group]] and the background field is a circle 4-bundle, then this is called the [[Yetter model]].

This are the first two steps in filtering of target spaces by [[homotopy type]] [[truncated|truncation]] of [[schreiber:∞-Chern-Simons theory]] <a href="http://nlab.mathforge.org/schreiber/show/infinity-Chern-Simons+theory#DiscreteTargets">with discrete target spaces</a>.

### Concise survey of the ingredients

We may think of this as  describing the [[quantum mechanics]] of an $(n-1)$-[[brane]] with $n$-dimensional [[worldvolume]] $\Sigma$ propagating on $B G$ and being [[charge]]d under a [[gauge field|higher analog]] of the [[electromagnetic field]]: 

a field configuration over $\Sigma$ (a $\Sigma$-shaped _trajectory_) is a [[morphism]] $\phi : \Sigma \to \mathbf{B}G$, hence equivalently a $G$-[[principal bundle]] on $\Sigma$. The [[configuration space]] of fields over $\Sigma$ is the [[groupoid]] of $G$-[[principal bundle]]s over $\Sigma$.

The [[background gauge field]] is a [[morphism]] $\alpha : \mathbf{B}G \to \mathbf{B}^n U(1)$ -- hence a [[characteristic class]] for $G$: a [[cocycle]] of degree $n$ in the [[group cohomology]] of $G$. 

The value of the [[Lagrangian]] $L(\phi)$ on a field configuration $\phi$ is the [[characteristic class]] of this bundle with respect to the universal characteristic class of the given [[principal infinity-bundle|circle n-bundle]]:

$$
  L : (\Sigma \stackrel{\phi}{\to} \mathbf{B}G)
  \mapsto
  (\alpha(\phi) : \Sigma \stackrel{\phi}{\to} \mathbf{B}G \stackrel{\alpha}{\to} \mathbf{B}^n U(1)).
$$

This is the [[classical field theory]] input of the model. The [[extended quantum field theory]] defined by this is supposed to be a rule that assigns space of [[state]]s to lower dimensional pieces of $\Sigma$ and to $n$-dimensional $\Sigma$s a propagator.

The space of [[state]]s assigned to a $\Sigma$ of [[dimension]] $n-k$ for $k \in \mathbb{N}$ is the [[k-groupoid]] of [[section]]s of the higher line bundle [[associated infinity-bundle|associated]] to the [[circle n-bundle|circle (n-k)-bundle]] $\tau_\Sigma \alpha$ obtained by [[transgression]] of $\alpha$ to the [[mapping space]] $\mathbf{H}(\Sigma, \mathbf{B}G)$. 


The propagator on $\Sigma$ of dimension $n$ is given by the [[path integral]] computed with [[measure]] the [[groupoid cardinality]] of $\mathbf{B}G$ and  [[integral kernel]] given by the [[action functional]]

$$
  \exp(i S(-)) : G Bund(\Sigma) \to U(1)
$$

that sends a field $\phi$ to the evaluation of $\alpha(\phi)$ on the [[fundamental class]] of $\Sigma$

$$
  \exp(i S(\phi)) = \int_\Sigma \alpha(\phi)
  \,.
$$


### Gentle exposition


(...)

## Details of DW-theory as an extended TQFT

The Dijkgraaf-Witten model is an example of (fully) [[extended topological quantum field theory]]. Namely, the above data not only assign an element in $U(1)$ to any closed $n$-dimensional manifold, but also a vector space to any closed $(n-1)$-dimensional manifold, a [[2-vector space]] to any closed $(n-2)$ manifold, and so on, ending with an [[n-vector space]] assigned to the point. Also, manifolds with boundary corresponds to (higher) linear operators between these (higher) vector spaces. According to the [[cobordism hypothesis]], the whole structure of the Dijkgraaf-Witten model as an fully extended  TQFT is contained in the datum of the $n$-Vector space it assigns to the point. This is the space of [[section|sections]] of the flat $n$-vector bundle $\mathbf{B}G\to n Vect$ induced by the background field $\mathbf{B}G\to \mathbf{B}^n U(1)$. 


### Finite Group Cohomology

Since the target space of Dijkgraaf-Witten theory is the [[delooping]] groupoid $\mathbf{B}G$ of a [[group]] $G$ ([[internalization|internal]] to [[Set]]), any background field given by a morphism $\alpha : \mathbf{B}G \to A$ in [[∞Grpd]] is a [[cocycle]] in the [[group cohomology]] of $G$, as described there.

Here we have a finite (or discrete) group $G$, and a discrete abelian group $A$, and we want to define $H^n(G;A)$. A way of doing this is to realize everything topologically: from $G$ we build the classifying space $\mathcal{B}G$, and from $A$ the [[Eilenberg-MacLane space]] $\mathcal{B}^n A=K(A,n)$. Then we consider the space of maps $hom(\mathcal{B}G,\mathcal{B}^n A)$ (these are our [[cocycle]]s) and take its $\pi_0$.

This way we have a familiar description, in a certain sense (topological spaces, continuous maps, homotopies,..), of the set $H^n(G;A)$. The drawback is that the topological spaces involved here are "gigantic" (infinite dimensional [[CW-complex]]es), where we had started with a very "little" datum: a finite group. So one can wonder if there is a finite model for the above construction, and the homotopy hypothesis serves it on a silver plate. Namely, since $G$ is discrete, $\mathcal{B}G$ is a [[homotopy n-type|1-type]], and nothing but the [[geometric realization]] of the [[delooping]] [[groupoid]] $\mathbf{B}G$ (boldface $B$ here); similarly $\mathcal{B}^n A$ is the topological geometric realization of the $n$-groupoid $\mathbf{B}^n A$, and the space of cocycles is $hom(B G,B^n A)$. since $G$ is a finite group, $B G$ is a finite groupoid, and so $hom(B G,B^n A)$ is a finite set. This set is the finite model for $hom(\mathcal{B}G,\mathcal{B}^n A)$ we were looking for.

To be continued...


### The $k$-vector spaces of states in codimension $k$
 {#StatesInCodimensionk}

The [[n-vector space|k-vector space]] associated with a closed oriented $(n-k)$-dimensional manifold $X_{n-k}$ admits a simple description in terms of [[section]]s:

The background field $\alpha : \mathbf{B}G \to A$ is [[transgression|transgressed]] to the mapping space $[\Pi(X_{n-k}), \mathbf{B}G]$ by forming the [[internal hom]]

$$ 
  [\Pi(X_{n-k}), \mathbf{B}G]
  \stackrel{[\Pi(X_{n-k}), \alpha]}{\to}
  [\Pi(X_{n-k}), A]
  \stackrel{\tau_{\leq k}}{\to}
  \tau_{\leq k} [\Pi(X_{n-k}), A]
  \,,
$$

where the last morphism is the projection on the [[truncated|k-truncation]]. This defines a [[cocycle]] on the _space of fields_ $[\Pi(X_{n-k}), \mathbf{B}G]$ over $X_{n-k}$, which classifies some [[principal ∞-bundle]] on this space. Given a canonical [[representation]] of the _spaces of phases_ $\tau_k [\Pi(X_{n-k}), A]$ on a [[n-vector space|k-vector space]] we obtain the corresponding [[associated bundle]] over the space of fields. The $(k-1)$-category assigned by the [[extended topological quantum field theory]] to the closed $X_{n-k}$ is the category of sections of this $k$-vector bundle.


+-- {: .num_prop}
###### Proposition

We have

$$
  \tau_k [\Pi(X_{n-k}), \mathbf{B}^n U(1)]
  \simeq
  \mathbf{B}^k U(1)
$$

=--

+-- {: .proof}
###### Proof

By general abstract reasoning (recalled at [[cohomology]] and [[fiber sequence]], for instance) we have for the [[homotopy group]]s that

\[
  \pi_i[\Pi(X_{n-k}),\mathbf{B}^n U(1)]
  \simeq 
  H^{n-i}(X_{n-k}, U(1))
  \,.
\]

Now use the [[universal coefficient theorem]], which asserts that we have an [[exact sequence]]

\[
  0
  \to 
  Ext^1(H_{n-i-1}(X_{n-k},\mathbb{Z}),U(1))
  \to 
  H^{n-i}(X_{n-k},U(1))
  \to 
  Hom(H_{n-i}(X_{n-k},\mathbb{Z}),U(1))
  \to 0
  \,.
\]

Since $U(1)$ is an [[injective object|injective]] $\mathbb{Z}$-[[module]] we have 

$$
  Ext^1(-,U(1))=0
  \,.
$$  

Together this means that we have an [[isomorphism]]

\[
  H^{n-i}(X_{n-k},U(1))
  \simeq 
  Hom_{Ab}(H_{n-i}(X_{n-k},\mathbb{Z}),U(1))
\]

that identifies the [[cohomology group]] in question with the [[internal hom]] in [[Ab]] from the integral [[homology]] group of $X_{n-k}$ to $U(1)$.

For $i\lt k$, the right hand side is zero, and so 

$$
  \pi_i[\Pi(X_{n-k}),\mathbf{B}^n U(1)]=0 \;\;\;\;
  for i\lt k
  \,. 
$$ 

For $i=k$, instead, $H_{n-i}(X_{n-k},\mathbb{Z})\simeq \mathbb{Z}$, since $X_{n-k}$ is a closed $(n-k)$-manifold and so 

$$
  \pi_k[\Pi(X_{n-k}),\mathbf{B}^n U(1)]\simeq U(1)
  \,.
$$


=--

+-- {: .num_prop}
###### Remark
Another proof of the isomorphism $H^{n-k}(X_{n-k},U(1))\cong U(1)$ and of the identities $H^{n-i}(X_{n-k},U(1))=0$ for $i\lt k$ can be obtained as follows. Consider the short exact sequence of locally constant sheaves of abelian groups
$$
0\to \mathbb{Z}\to \mathbb{R}\to U(1)\to 1.
$$
This induces a long exact sequence in cohomology
$$
\cdots \to H^{n-i-1}(X_{n-k},U(1))\to H^{n-i}(X_{n-k},\mathbb{Z})\to H^{n-i}(X_{n-k},\mathbb{R}) \to H^{n-i}(X_{n-k},U(1))\to H^{n-i+1}(X_{n-k},\mathbb{Z})\to \cdots
$$
For $i\lt k$ we have $H^{n-i}(X_{n-k},U(1))=0$ by dimensional reasons, while for $i=k$ we find the exact sequence
$$
\cdots \to H^{n-k}(X_{n-k},\mathbb{Z})\to H^{n-k}(X_{n-k},\mathbb{R}) \to H^{n-k}(X_{n-k},U(1))\to 0.
$$
Since $X_{n-k}$ is a closed oriented manifold, we have $H^{n-k}(X_{n-k},\mathbb{Z})=\mathbb{Z}$, $H^{n-k}(X_{n-k},\mathbb{R})=\mathbb{R}$, and the map $H^{n-k}(X_{n-k},\mathbb{Z})\to H^{n-k}(X_{n-k},\mathbb{R})$ is the inclusion of $\mathbb{Z}$ into $\mathbb{R}$. Hence $H^{n-k}(X_{n-k},U(1))\cong \mathbb{R}/\mathbb{Z}\cong U(1)$.
=--
 
This means that the [[transgression]] of the Dijkgraaf-Witten background field

$$
  \alpha : \mathbf{B}G \to \mathbf{B}^n U(1)
$$

to the _space of field configurations_ $[\Pi(X_{n-k}), \mathbf{B}G]$ over $X_{n-k}$ is a [[cocycle]] of the form

$$
  [\Pi(X_{n-k}), \alpha] : [\Pi(X_{n-k}), \mathbf{B}G] \to \mathbf{B}^k U(1)
  \,.
$$

This classifies a $\mathbf{B}^{k-1} U(1)$-[[principal ∞-bundle]] $P$ over the space of field configurations, given by the [[pullback]]

$$
  \array{
    P &\to & \mathbf{E} \mathbf{B}^{k-1} U(1)
    \\
    \downarrow && \downarrow
     \\
     [\Pi(X_{n-k}), \mathbf{B}G] &\stackrel{[\Pi(X_{n-k}), \rho]}{\to}& \mathbf{B}^k U(1)
  }
  \,.
$$

(Here $\mathbf{E} \mathbf{B}^{k-1} U(1)$ is as described at [[universal principal ∞-bundle]].)


By the canonical $k$-[[representation]] $\rho : \mathbf{B}^k U(1) \to k Vect_{\mathbb{C}}$ of $\mathbf{B}^{k-1}U(1)$ on complex [[n-vector space|k-vector space]]s, we have [[associated bundle|associated]] to this canonically a $k$-vector bundle $E$, which may be realized as the pullback

$$
  \array{
    E &\to & k Vect_*
    \\
    \downarrow && \downarrow
     \\
     [\Pi(X_{n-k}), \mathbf{B}G] &\stackrel{\rho \circ [\Pi(X_{n-k}), \rho]}{\to}& k Vect
  }
  \,.
$$

Here $k Vect_*$ is the [[n-category|k-category]] of pointed $k$-vector bundles, see again [[generalized universal bundle]] for more.

If $X_{n-k}$ is closed then the $k$-vector spaces associated by the TFT to $X_{n-k}$ is the [[n-category|(k-1)-category]] of [[section]]s of this bundle $E$.

...

## Relation to Chern-Simons theory

Dijkgraaf-Witten theory is to be thought of as the finite group version of [[Chern-Simons theory]]. Chern-Simons theory looks formally just as the above, only that all finite $n$-groupoids appearing here are replaced by [[Lie ∞-groupoid]]s ([[∞-stack]]s on [[CartSp]]).

## Related concepts

* [[schreiber:∞-Chern-Simons theory]]

* [[higher dimensional Chern-Simons theory]]

  * [[1d Chern-Simons theory]]

    * [[1d Dijkgraaf-Witten theory]]

  * [[2d Chern-Simons theory]]

  * [[3d Chern-Simons theory]]

    * **Dijkgraaf-Witten theory**

    * [[2d Wess-Zumino-Witten theory]]

  * [[4d Chern-Simons theory]]

  * [[5d Chern-Simons theory]]

  * [[6d Chern-Simons theory]]

  * [[7d Chern-Simons theory]]

  * [[infinite-dimensional Chern-Simons theory]]

  * [[AKSZ sigma-model]]




## References

The idea originates, of course, in 

* [[Robbert Dijkgraaf]], [[Edward Witten]], _[[DW.pdf:file]]_, Commun. Math. Phys. __129__ (1990), 393,
 {#DijkgraafWitten90}

The discussion of the [[quasi-Hopf algebra]] associated with a [[group cohomology]] 3-[[cocycle]] $c \colon \mathbf{B}G \to \mathbf{B}^3 U(1)$ originates in

* [[Robbert Dijkgraaf]], V. Pasquier, P. Roche, _QuasiHopf algebras, group cohomology and orbifold models_, Nucl. Phys. B Proc. Suppl. __18B__ (1990), 60-72; _Quasi-quantum groups related to orbifold models_, Modern quantum field theory (Bombay, 1990), 375&#8211;383, World Sci. 1991

A review is in 

*  A. Coste, J-M. Maillard, _Representation Theory of Twisted Group Double_, Annales Fond.Broglie 29 (2004) 681-694, ([arXiv:hep-th/0309257](http://arxiv.org/abs/hep-th/0309257))

and conceptual clarifications were established in

* [[Simon Willerton]], _The twisted Drinfeld double of a finite group via gerbes and finite groupoids_, [arXiv/math.QA/0503266](http://arxiv.org/abs/math.QA/0503266)

and, earlier, in an unpublished manuscript of [[Paul Bressler]] (2002-2004). See at _[[Drinfeld double]]_ for more on this.


A first comprehensive structural account of DW theory as a [[FQFT|functorial QFT]] was given in 

* [[Daniel Freed]], [[Frank Quinn]], _Chern-Simons theory with finite gauge group_ Commun.Math.Phys. __156__:435-472, 1993, ([arXiv:hep-th/9111004](http://de.arxiv.org/abs/hep-th/9111004))
 {#FreedQuinn93}

A review is given on p. 68 of

* [[Bruce Bartlett]], _Categorical aspects of topological quantum field theory_, [arXiv/math.QA/0512103](http://de.arxiv.org/abs/math.QA/0512103)

First steps towards understand DW theory as an [[extended TQFT]] appear in 

* [[Daniel Freed]], _Higher Algebraic Structures and Quantization_ Commun.Math.Phys. 159 (1994) 343-398 ([arXiv:arXiv:hep-th/9212115](http://arxiv.org/abs/arXiv:hep-th/9212115))
 {#Freed94}

Discussion aiming towards a refinement of DW theory to an [[extended TQFT]] is in 

* Kevin Wray, _Extended topological gauge theories in codimension 0 and higher_ ([pdf](http://math.berkeley.edu/~kwray/papers/thesis.pdf))

Further conceptual refinement of this is indicated in section 3 and section 8 of

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_ (2010)

This proposes a general abstract way to construct [[path integral]] quantizations for finite group theories such as DW, see also at _[[prequantum field theory]]_. More along these lines is in 

* [[Jacob Lurie]], _Finiteness and ambidexterity in $K(n)$-local stable homotopy theory_, talk at _Notre Dame Graduate Summer School on Topology and Field Theories_ and _Harvard lecture_ 2012 ([video part 1](http://www.youtube.com/watch?v=eQayYLDw1VA), [part 2](http://www.youtube.com/watch?v=OEShrQyvmS4), [part 3](http://www.youtube.com/watch?v=nOIcdn1iUR4) [part 4](http://www.youtube.com/watch?v=ZwnClYedaYM), [pdf lecture notes](http://www.math.northwestern.edu/~celliott/notre_dame_notes/Lurie_notes.pdf) by Chris Elliott)

See also

* [[Thomas Nikolaus]], _Equivariant Dijkgraaf-Witten theory_, a talk at Muenster ([pdf](http://www.math.uni-hamburg.de/home/nikolaus/Muenster.pdf))

For more on this see the discussion on the [n-Forum](http://nforum.mathforge.org/discussion/1046/path-category-vs-cobordisms-for-bundles/?Focus=8337#Comment_8337).

## Dijkgraaf–Witten theory via Kan extensions

* [[Jeffrey C. Morton]], _Cohomological Twisting of 2-Linearization and Extended TQFT_, [arXiv:1003.5603](https://arxiv.org/abs/1003.5603).

* Section 2 and 3 of [[Gijs Heuts]] and [[Jacob Lurie]]'s Ambidexterity, in: Topology and Field Theories, [doi](https://doi.org/10.1090/conm/613).

* Section 3 of [[Daniel Freed]], [[Michael Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], Topological quantum field theories from compact Lie groups, [arXiv:0905.0731](https://arxiv.org/abs/0905.0731).


[[!redirects Dijkgraaf--Witten theory]]
[[!redirects Dijkgraaf–Witten theory]]
[[!redirects Dijkgraaf-Witten model]]
[[!redirects Dijkgraaf-Witten models]]