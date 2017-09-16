_Dijkgraaf-Witten theory_ in dimension $n$ is the topological [[sigma-model]] [[quantum field theory]] whose 

* target space is the groupoid $\mathbf{B} G = \{\bullet \stackrel{g}{\to} \bullet | g \in G\}$ for $G$ a finite [[group]];

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

Dijkgraaf-Witten theiry is to be thought of as the finite group version of [[Chern-Simons theory]]. Chern-Simons theory looks formally just as the above, only that not all finite $n$-groupoids appearing are smooth $n$-groupoids ([[infinity-stack]]s on $Diff$).

#References#

The idea originates, of course, in 

* Dijkgraaf, Witten, ...

A first comprehensive structural account od DW theory as a [[FQFT|functorial QFT]] was given in 

* Freed, Quinn

More conceptual clarifications were given in

* Simon Willerton, _Drinfeld double via gerbes and finite groupoids_

Recently there have been attempts to understand the structure here more systematically:

Section 3 of

* Freed-Hopkins-Lurie-Teleman,...

For $n=1$ it is shown in

* [[Johan Alm]], [[Quantization as a Kan Extension]]

that the quantization procedure for DW theory is nothing but the Kan extension of the background field from target space down to parameter space. 