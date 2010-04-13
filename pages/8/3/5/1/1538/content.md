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

* parameter spaces $\Sigma = \Pi_1(X)$ are [[skeleton|skeleta]] of the [[fundamental groupoid]]s of $n$-dimensional manifolds $X$.

Therefore 

* a field configuration $\Sigma  = \Pi_1(X) \stackrel{\phi}{\to} \mathbf{B} G$ is a $G$-bundle on $X$ (recall that $G$ is assumed to be a finite group);

* the action $\Pi_1(X) \stackrel{\phi}{\to} \mathbf{B} G \stackrel{exp(i S)}{\to} \mathbf{B}^n U(1)$ of this field configuration is the cohomology class $c(\phi)$ of this bundle under the given group cocycle;

* the weight in the path integral over all $\phi$ for $n$-dimensional $X$ (i.e. in codimension 0) is the [[groupoid cardinality|groupoid measure]] of the [[functor category]] $[\Pi_1(X), \mathbf{B}G]$.

##Finite Group Cohomology

To understand Dijkgraaf-Witten theory, it may be helpful to take a step backwards and consider finite [[group cohomology]] (see there for more details).

Here we have a finite (or discrete) group $G$, and a discrete abelian group $A$, and we want to define $H^n(G;A)$. A way of doing this is to realize everything topologically: from $G$ we build the classifying space $\mathcal{B}G$, and from $A$ the [[Eilenberg-MacLane space]] $\mathcal{B}^n A=K(A,n)$. Then we consider the space of maps $hom(\mathcal{B}G,\mathcal{B}^nA)$ (these are our [[cocycle]]s) and take its $\pi_0$.

This way we have a, in a certain sense familiar (topological spaces, continuous maps, homotopies,..), description of the set $H^n(G;A)$. The drawback is that the topological spaces involved here are "gigantic" (infinite dimensional [[CW-complex]]es), where we had started with a very "little" datum: a finite group. So one can wonder if there is a finite model for the above construction, and the homotopy hypotesis serves it on a silver plate. Namely, since $G$ is discrete, $\mathcal{B}G$ is a [[homotopy n-type|1-type]], and nothing but the [[geometric realization]] of the [[delooping]] [[groupoid]] $\mathbf{B}G$ (boldface $B$ here); similarly $\mathcal{B}^n A$ is the topological geometric realization of the $n$-groupoid $\mathbf{B}^n A$, and the space of cocycles is $hom(B G,B^n A)$. since $G$ is a finite group, $B G$ is a finite groupoid, and so $hom(B G,B^n A)$ is a finite set. This set is the finite model for $hom(\mathcal{B}G,\mathcal{B}^n A)$ we were looking for.

To be continued...

## Remarks

Dijkgraaf-Witten theiry is to be thought of as the finite group version of [[Chern-Simons theory]]. Chern-Simons theory looks formally just as the above, only that all finite $n$-groupoids appearing here are replaced by smooth $n$-groupoids ([[infinity-stack]]s on $Diff$).

## References

The idea originates, of course, in 

* Robbert Dijkgraaf and Edward Witten, [[DW.pdf:file]], Commun. Math. Phys.  129 (1990), 393.

A first comprehensive structural account od DW theory as a [[FQFT|functorial QFT]] was given in 

* Dan Freed, Frank Quinn, _Chern-Simons theory with finite gauge group_ ([arXiv](http://de.arxiv.org/abs/hep-th/9111004))

A review is given on p. 68 of

* [[Bruce Bartlett]], _Categorical aspects of topological quantum field theory_ ([arXiv](http://de.arxiv.org/abs/math.QA/0512103))

Further conceptual clarifications were established in

* Simon Willerton, _The twisted Drinfeld double of a finite group via gerbes and finite groupoids_ ([arXiv](http://arxiv.org/abs/math.QA/0503266))

Recently there have been attempts to understand the structure here more systematically:

Section 3 of

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_ 

proposes a general abstract nonsense way to construct [[path integral]] quantizations for finite group theories such as DW.

For more on this see the discussion on the [n-Forum](http://www.math.ntnu.no/~stacey/Vanilla/nForum/comments.php?DiscussionID=1046&Focus=8337#Comment_8337).

...

[[!redirects Dijkgraaf--Witten theory]]
[[!redirects Dijkgraaf–Witten theory]]