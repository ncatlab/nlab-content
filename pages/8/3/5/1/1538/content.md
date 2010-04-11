<div class="rightHandSide toc">
[[!include physicscontents]]
</div>


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

#Remarks#

Dijkgraaf-Witten theiry is to be thought of as the finite group version of [[Chern-Simons theory]]. Chern-Simons theory looks formally just as the above, only that all finite $n$-groupoids appearing here are replaced by smooth $n$-groupoids ([[infinity-stack]]s on $Diff$).

#References#

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

For more on this see

...

[[!redirects Dijkgraaf--Witten theory]]
[[!redirects Dijkgraaf–Witten theory]]