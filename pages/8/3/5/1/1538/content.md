<div class="rightHandSide toc">
[[!include physicscontents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

_Dijkgraaf-Witten theory_ in dimension $n$ is the topological [[sigma-model]] [[quantum field theory]] whose 

* target space is the groupoid $\mathbf{B}G = \{ \bullet \righttoleftarrow g \;|\; g \in G \}$ obtained by [[delooping]]  from a _finite_ [[group]] $G$ ;

* background field is an $n$-functor $exp(i S) : \mathbf{B} G \to \mathbf{B}^n U(1)$ 

  * this is the same thing as a $U(1)$-valued group $n$-cocycle $c$ on $G$;

* or rather the background field is the associated functor $\mathbf{B} G \to \mathbf{B}^n U(1) \to n Vect$ for the canonical representation of $\mathbf{B}^n U(1)$ 

  * (for this purpose often what is considered is the simple model of $n Vect$ given by $\mathbf{B}^{n-1} 1dVect_{iso}$).

* parameter spaces $\Sigma = \Pi(X)$ are [[skeleton|skeleta]] of the [[fundamental groupoid]]s of $n$-dimensional manifolds $X$.

Therefore 

* a field configuration $\Sigma  = \Pi(X) \stackrel{\phi}{\to} \mathbf{B} G$ is a $G$-bundle on $X$ (recall that $G$ is assumed to be a finite group);

* the action $\Pi(X) \stackrel{\phi}{\to} \mathbf{B} G \stackrel{exp(i S)}{\to} \mathbf{B}^n U(1)$ of this field configuration is the cohomology class $c(\phi)$ of this bundle under the given group cocycle;

* the weight in the path integral over all $\phi$ for $n$-dimensional $X$ (i.e. in codimension 0) is the [[groupoid cardinality|groupoid measure]] of the [[functor category]] $[\Pi(X), \mathbf{B}G]$.

## Details of DW-theory as an extended TQFT

The Dijkgraaf-Witten model is an example of (fully) [[extended topological quantum field theory]]. Namely, the above data not only assign an element in $U(1)$ to any closed $n$-dimensional manifold, but also a vector space to any closed $(n-1)$-dimensional manifold, a [[2-vector space]] to any closed $(n-2)$ manifold, and so on, ending with an [[n-vector space]] assigned to the point. Also, manifolds with boundary corresponds to (higher) linear operators between these (higher) vector spaces. According to the [[cobordism hypothesis]], the whole structure of the Dijkgraaf-Witten model as an fully extended  TQFT is contained in the datum of the $n$-Vector space it assigns to the point. This is the space of [[section|sections]] of the flat $n$-vector bundle $\mathbf{B}G\to n Vect$ induced by the background field $\mathbf{B}G\to \mathbf{B}^n U(1)$. 


### Finite Group Cohomology

Since the target space of Dijkgraaf-Witten theory is the [[delooping]] groupoid $\mathbf{B}G$ of a [[group]] $G$ ([[internalization|internal]] to [[Set]]), any background field given by a morphism $\alpha : \mathbf{B}G \to A$ in [[∞Grpd]] is a [[cocycle]] in the [[group cohomology]] of $G$, as described there.

Here we have a finite (or discrete) group $G$, and a discrete abelian group $A$, and we want to define $H^n(G;A)$. A way of doing this is to realize everything topologically: from $G$ we build the classifying space $\mathcal{B}G$, and from $A$ the [[Eilenberg-MacLane space]] $\mathcal{B}^n A=K(A,n)$. Then we consider the space of maps $hom(\mathcal{B}G,\mathcal{B}^nA)$ (these are our [[cocycle]]s) and take its $\pi_0$.

This way we have a, in a certain sense familiar (topological spaces, continuous maps, homotopies,..), description of the set $H^n(G;A)$. The drawback is that the topological spaces involved here are "gigantic" (infinite dimensional [[CW-complex]]es), where we had started with a very "little" datum: a finite group. So one can wonder if there is a finite model for the above construction, and the homotopy hypotesis serves it on a silver plate. Namely, since $G$ is discrete, $\mathcal{B}G$ is a [[homotopy n-type|1-type]], and nothing but the [[geometric realization]] of the [[delooping]] [[groupoid]] $\mathbf{B}G$ (boldface $B$ here); similarly $\mathcal{B}^n A$ is the topological geometric realization of the $n$-groupoid $\mathbf{B}^n A$, and the space of cocycles is $hom(B G,B^n A)$. since $G$ is a finite group, $B G$ is a finite groupoid, and so $hom(B G,B^n A)$ is a finite set. This set is the finite model for $hom(\mathcal{B}G,\mathcal{B}^n A)$ we were looking for.

To be continued...


### The $k$-vector spaces of states in codimension $k$

The [[n-vector space|k-vecto space]] associated with a closed $(n-k)$-dimensional manifold $X_{n-k}$ admits a simple description in terms of [[section]]s. By the [[universal coefficient theorem]] we find that the _space of phases_ on $X_{n-k}$ is

$$
  [\Pi(X_{n-k}), \mathbf{B}^n U(1)] \simeq \mathbf{B}^k U(1)
  \,.
$$

This means that the [[transgression]] of the background field

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

(Here $\mathbf{E} \mathbf{B}^{k-1} U(1)$ is as described at [[generalized universal bundle]].)


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

Dijkgraaf-Witten theiry is to be thought of as the finite group version of [[Chern-Simons theory]]. Chern-Simons theory looks formally just as the above, only that all finite $n$-groupoids appearing here are replaced by [[Lie ∞-groupoid]]s ([[∞-stack]]s on [[CartSp]]).

## References

The idea originates, of course, in 

* [[Robbert Dijkgraaf]] and [[Edward Witten]], [[DW.pdf:file]], Commun. Math. Phys.  129 (1990), 393.

A first comprehensive structural account od DW theory as a [[FQFT|functorial QFT]] was given in 

* [[Dan Freed]], [[Frank Quinn]], _Chern-Simons theory with finite gauge group_ ([arXiv](http://de.arxiv.org/abs/hep-th/9111004))

A review is given on p. 68 of

* [[Bruce Bartlett]], _Categorical aspects of topological quantum field theory_ ([arXiv](http://de.arxiv.org/abs/math.QA/0512103))

Further conceptual clarifications were established in

* [[Simon Willerton]], _The twisted Drinfeld double of a finite group via gerbes and finite groupoids_ ([arXiv](http://arxiv.org/abs/math.QA/0503266))

Recently there have been attempts to understand the structure here more systematically:

Section 3 of

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_ 

proposes a general abstract nonsense way to construct [[path integral]] quantizations for finite group theories such as DW.

For more on this see the discussion on the [n-Forum](http://www.math.ntnu.no/~stacey/Vanilla/nForum/comments.php?DiscussionID=1046&Focus=8337#Comment_8337).

...

[[!redirects Dijkgraaf--Witten theory]]
[[!redirects Dijkgraaf?Witten theory]]