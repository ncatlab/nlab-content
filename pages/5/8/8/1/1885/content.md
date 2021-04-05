
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The **Moore space** $M(G, n)$, where $G$ is an [[abelian group]] and $n \geq 1$, is a [[topological space]] which has non-trivial (reduced) [[homology group]]  $G$ precisely only in dimension $n$ and is simply connected if $n \geq 2$. 

(This is somewhat dual to the notion of [[Eilenberg-MacLane space]], which instead has nontrivial [[homotopy group]] in one single dimension.)

## Definition

(the following is based on [Hatcher](#Hatcher))

Let $G$ be an abelian group. Take a [[presentation]] of $G$ i.e. a [[short exact sequence]]
$$
  0\rightarrow H \rightarrow F\rightarrow G\rightarrow 0
$$ 

where $F$ a [[free abelian group]]. Since $H=ker(F\rightarrow G)$, it is a free abelian group as well and we choose [[bases]] $\{f_\alpha\}_\alpha$ for $F$ and $\{h_\beta\}_\beta$ for $H$. We then construct a [[CW complex]] 

$$
  X=M(G,n)
$$ 

by taking the $n$-th [[skeleton]] to be $X^n:=\vee_\alpha S^n_\alpha$ and for each $\beta$ we attach an $n+1$-cell as follows:

Write $h_\beta=\Sigma_\alpha d_{\alpha\beta}f_\alpha$ and let $\delta_{d_{\alpha\beta}}$ be $0$ if $d_{\alpha\beta}= 0$ and be $1$ otherwise. Define an attaching map $S^n_\beta\rightarrow X^n$ by contracting $\ell_\beta:=(\Sigma_\alpha \delta_{d_{\alpha\beta}})-1$ $(n-1)-$spheres in $S^n$ thus defining a map $S^n_\beta\rightarrow \vee_{\ell_\beta} S^n_{\alpha\beta}$ and then map each $S^n_{\alpha\beta}$ to $S^n_{\alpha}$ by a degree $d_{\alpha\beta}$. 

+-- {: .num_defn}
###### Definition

The ([[homotopy type]] of) the [[topological space]] $M(G,n)$ constructed this way we call the _Moore space_ of $G$ in degree $n$.

=--


The resulting CW-complex can be seen to have the desired properties via [[cellular homology]].

## Properties

### Homotopy type

The homotopy type of $M(G,n)$ is determined by specifying $G$ and $n$. 

### (Non-)Functoriality of the construction

The construction above is not functorial in $G$ because of the choice of bases (see more below). However, it does give a [[functor]] to the [[homotopy category]] $M(-,n):Ab\rightarrow Ho(Top)$.  

The functoriality problem of the construction above cannot be corrected. That is, there is no functor $Ab\rightarrow Top$ that lifts $M(-,n)$. 
This can be seen as a corollary of a counterexample of Carlsson which gives a negative answer to a conjecture of Steenrod:

+-- {: .num_remark}
###### Conjecture 
**(Steenrod)**

Given a group $G$ a $G$-module $M$ and a natural number $n$, there is a $G$-space $X$ which has only one non-zero reduced homology G-module in dimension $n$ that satisfy $\tilde{H}_n(X;\mathbb{Z}) \cong M$ as $G$-modules.

=--

Carlsson provides counter examples for such "equivariant Moore spaces" for all non-cyclic groups.

+-- {: .num_cor}
###### Corollary

There is thus no [[functor]] [[Ab]]$\rightarrow$ [[Top]] that lifts $M(-,n)\colon Ab\rightarrow Ho(Top)$ since if there was such, it would induce, for any group $G$ a functor $Ab^G\rightarrow Top^G$ and in particular a positive answer to the Steenrod conjecture.

Moreover, there can also not be an [[(∞,1)-functor]] $Ab\rightarrow L_{whe} Top$ that lifts $M(-,n)$ since this will similarly yield an $\infty$-functor $Ab^G\rightarrow Top^{hG}$ where $Top^{hG}$ is the [[(∞,1)-category]] of [[∞-actions]] of $G$ on spaces. Since there is a "rigidification" functor $Top^{hG}\rightarrow Top^G$ this would yield an (ordinary) functor $Ab^G\rightarrow Top^G$ which does not exist by our previous observation. 

=--


## Related concepts
 
### Co-Moore spaces

There is also a cohomology analogue known as a **co-Moore space** or a **Peterson space**, but this is not defined for all abelian $G$. [[sphere|Spheres]] are both Moore and co-Moore spaces for $G = \mathbb{Z}$.

Co-Moore spaces are the [[Eckmann-Hilton duality|Eckmann–Hilton duals]] of [[Eilenberg–Mac Lane spaces]]. 

According to Baues, Moore spaces are $H \pi$-duals to Eilenberg--Mac Lane spaces. This leads to an extensive duality for connected [[CW complexes]].

### Moore decomposition


Just as there is a [[Postnikov decomposition]] of a space as a tower of fibrations, so there is a [[Moore decomposition]] as a tower of cofibrations.


## Related concepts

* [[Peterson space]]

* [[Eilenberg–MacLane space]]

##References##

* Example 2.40 of Hatcher [Algebraic Topology](http://www.math.cornell.edu/~hatcher/AT/ATch2.pdf).
 {#Hatcher}

* [[Marek Golasinski]] and  [[Daciberg Lima Gon&#231;alves]], [On Co-Moore Spaces](https://www.mscand.dk/article/view/13841/11841)
* [[Hans J. Baues]], Homotopy types, in Handbook of Algebraic Topology, (edited by I.M. James), North Holland, 1995.

* Gunnar Carlsson "A counterexample to a conjecture of Steenrod"
Invent. Math. 64 (1981), no. 1, 171&#8211;174. 

[[!redirects Moore spaces]]
