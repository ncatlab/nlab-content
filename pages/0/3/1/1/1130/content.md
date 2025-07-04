
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential-graded objects
+--{: .hide}
[[!include differential graded objects - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}



## Definition

### Abstract definition

A _dg-coalgebra_ is a [[comonoid]] in the [[category]] of [[chain complex]]es.

Equivalently, this is a graded [[coalgebra]] $C$ equipped with a [[coderivation]]

$$
  D : C \to C
$$

that is of degree -1 and squares to 0, 

$$
  D^2 = 0 
  \,.
$$


### Detailed component definition


#### Pre-coalgebra

 A _pre-graded coalgebra_ (pre-gc), $(C,\Delta, \varepsilon)$, is a [[graded vector space|pre-gvs]] $C$ together with linear maps of degree 0

$$\Delta: C\to C\otimes C,    \varepsilon : C\to k,$$

such that the obvious (usual) diagrams commute.  (When there is no ambiguity, we may write $C$ instead of $(C,\Delta, \varepsilon)$.)


The field $k$ is a coalgebra for the canonical isomorphism $k\to k\otimes k$ with $\varepsilon = id_k$.

A morphism $\psi : C \to C'$ of pre-gcs is a linear mapping of degree zero such that

$$(\psi \otimes \psi)\circ \Delta = \Delta' \circ \psi   and    \varepsilon = \varepsilon' \circ \psi.$$

The linear counit mapping $\varepsilon :C \to k$ is always a morphism of pre-gcs.


#### Coaugmentations

A _coaugmentation_ of a pre-gc is a morphism $\eta : k \to C$.  We will write $1$ for $\eta(1)$.  

The cokernel $\bar{C}$ of $\eta$ can be identified with $Ker \varepsilon$ and so can be considered as a subspace of $C$.

The reduced diagonal $\bar{\Delta} : \bar{C} \to \bar{C}\otimes \bar{C}$, induced by $\Delta$ is defined by $\Delta x = 1\otimes x + x\otimes 1 + \bar{\Delta }x$.  The _vector space of primitives_ of $C$, denoted $P(C)$, is the kernel of the reduced diagonal.

A morphism of coaugmented pre-gcs, $\psi : (C,\eta)\to (C',\eta')$, is a morphism of the pre-gcs which satisfies $\eta' = \psi \circ \eta$. It preserves primitives.



#### The commutation morphism

Let $V$ and $V'$ be two pre-gvs.  The commutation morphism 
$$\tau : V\otimes V' \to V'\otimes V$$
is defined by $\tau( v\otimes v') = (-1)^{|v||v'|} v'\otimes v$, on homogeneous elements.


#### Tensor product of pre-gcs.

Let $(C,\Delta, \varepsilon)$ and $(C',\Delta', \varepsilon')$ be two pre-graded coalgebras.  The mappings
$$C\otimes C'\stackrel{\Delta\otimes \Delta'}{\to}C\otimes C\otimes C'  \otimes C'\stackrel{C\otimes \tau \otimes C}{\to}(C\otimes C')\otimes (C\otimes C')$$

and 

$$C\otimes C'\stackrel{\varepsilon\otimes \varepsilon'}{\to}k \otimes k\stackrel{\cong}{\to}k$$

give $C\otimes C'$ a pre-gc structure.

If $\eta$ and $\eta'$ are coaugmentations of $C$ and $C'$ respectively, then $\eta\otimes\eta'$ defines a coaugmentation of $C\otimes C'$.



#### Coderivations of pre-graded coalgebras

If $C$ is a pre-gc, a _coderivation_ of degree $p\in \mathbb{Z}$, is a linear map $\theta \in Hom_p(C,C)$ such that 

$$\Delta \circ \theta = (\theta \otimes id_C + \tau \circ(\theta \otimes id_C)\circ \tau)\circ \Delta,  and  \varepsilon\circ \theta = 0.$$

A coderivation $\theta$ of a coaugmented pre-gc $(C,\eta)$ is a coderivation of $C$ such that $\theta\circ \eta = 0$.



#### Differential graded coalgebras

A _differential_ $\partial$ on a (coaugmented) pre-gc, $C$, is a coderivation of degree -1 such that $\partial\circ\partial = 0$.

The pair, $(C, \partial)$ is called a _differential (coaugmented) pre-graded coalgebra_ (pre-dgc).  Its homology $H(C,\partial)$ will be a pre-gc.

If $(C,\partial)$ and $(C',\partial')$ are two pre-dgcs, then their tensor product $(C,\partial)\otimes(C',\partial')$ is a pre-gdgc with the structures defined earlier.

A _morphism_ of (coaugmented) pre-dgcs is a morphism both of (coaugmented) pre-gcs and of pre-dgvs.  We denote the resulting categories by $pre DGC$ (resp. $pre \eta DGC$).


#### Cocommutative pre-dgcs

A pre-gc $C$ is _cocommutative_ if $\tau\circ\Delta = \Delta$, similarly for a pre-dgc.  The subcategories of cocommutative d.g. coalgebras will be denoted $pre CDGC$ (resp. $pre \eta CDGC$).


#### CDGC

A _cocommutative differential graded coalgebra_ is a pre-cdgc on a graded vector space of lower grading (so $C_p = 0$ for $p \lt 0$).  This gives categories $CDGC$ (resp. $\eta CDGC$).



#### $n$-connected $\eta$ cdgcs

A coaugmented cdgc $(C, \partial)$ is _$n$-connected_ if $\bar{C}_p = 0$ for $p\leq n$.  

This gives a category $CDGC_n$.  Any connected (i.e. $0$-connected) cdgc is canonically coaugmented with $\bar{C}$ coinciding with $C_+$.



#### Hom-algebras and duals

Let $(C,\partial)$ be a pre-cdgc and $(A,d)$ a pre-cdga.  The pre-dgvs $(Hom(C,A),D)$ is a pre-cdga for the usual differential and the multiplication $f.g = \mu\circ (f\otimes g)\circ \Delta$,
$$ C\stackrel{\Delta}{\to}C\otimes C\stackrel{(f\otimes g)}{\to}A\otimes A\stackrel{\mu}{\to} A,$$

for $f,g \in Hom(C,A)$.

In particular $\#(C,\partial)= (Hom(C,k),D)$  defines a functor from $pre CDGC$ to $pre CDGA$, which commutes with homology and is such that $\# CDGC_n \subseteq CDGA^n$.  Conversely, if $(A,d)$ is a pre-cdga of finite type, $\#(A,d)$ is a pre-cdgc. 


#### Coalgebra filtrations

Let $(C,\partial)$ be a pre-dgc. A _coalgebra filtration_ (resp. _differential coalgebra filtration_) of $(C,\partial)$ is a family of subspaces $F_p C$, $p\in \mathbb{Z}$ such that 

$$F_p C\subseteq F_{p+1} C, \quad \Delta F_p C \subseteq \sum_k F_k C\otimes F_{p-k} C, \quad (resp.\quad and \quad \partial F_p C\subseteq F_p C).$$


#### Filtrations of the primitives

Let $(C,\eta)$ be a coaugmented pre-gc, $\bar{C}$ the cokernel of $\eta$, $\bar{\Delta}$, the reduced diagonal.

The iteration of $\bar{\Delta}$ is defined by
 
$$\bar{\Delta}^1 = \bar{\Delta}; \quad \bar{\Delta}^p = (\bar{\Delta}\otimes \bar{C} \otimes \ldots \bar{C}) \otimes \bar{\Delta}^{(p-1)}.$$

The (increasing) filtration of the primitives is $F_p C = Ker\bar{\Delta}^p$, $p\geq 1$. It is a graded coalgebra filtration.

If $(C,\partial, \eta)$ is a coaugmented pre-dgc, each $F_p C$ is stable under the differential and, in particular, $F_1 = P(C)$.  $P$ thus defines a functor from $pre \eta CDGC$ to $pre DGVS$.  

Let $\mu$ be the comultiplication of the pre-ga $\# C$, the dual of $C$.  Elementary results on duality show, for finite type:  $Im\bar{\mu}^p$ is the orthogonal complement of $Ker\bar{\Delta}^p$, so, in particular, $Q(\# C) =\# P(C)$.

Let $(C,\eta)$ be a coaugmented pre-gc and $F_p C$ the filtration of its primitives.  $C$ is _conilpotent_ if $C = \bigcup_k F_k C$.
A connected coalgebra is conilpotent and conilpotency is preserved by tensor product.

#### The pre-gc structure on $T(V)$

We will denote by $T'(V)$, the gvs $T(V)$, together with the coalgebra structure in which the reduced diagonal is given by 

$$\bar{\Delta}(v_1\otimes \ldots \otimes v_n) = \sum_{p=1}^{n-1} (v_1\otimes \ldots \otimes v_p)\otimes(v_{p+1}\otimes \ldots \otimes v_n).$$

The counit and the coaugmentation are the natural mappings $T(V)\to k$ and $k\to T(V)$, respectively.

The coalgebra $T' (V)$ is non-commutative if $dim V\gt 1$ and has $V$ as its vector space of primitives.

If $C$ is a conilpotent pre-gc, then any morphism $f : C\to V$ of pre-gvs for which $f(1) = 0$, admits a unique lifting to a pre-gc morphism $\hat{f}:C \to T'(V)$.

#### Shuffles

A _$(p,q)$-[[shuffle]]_ $\sigma$ is a permutation of $\{1, \ldots, p+q\}$ such that 

$$\sigma(i) \lt \sigma(j) \quad if \quad 1\leq i\lt j\leq p \quad or \quad p+1 \leq i \lt j\leq p+q.$$



#### The pre-cgc structure on $\bigwedge V$

We will denote $\bigwedge' V$, the gvs $\bigwedge V$ together with the coalgebra structure in which the reduced diagonal is given by 

$$\bar{\Delta}(v_1\wedge \ldots \wedge v_n) = \sum_{p=1}^{n-1} \sum_\sigma\varepsilon(\sigma)(v_{\sigma(1)}\wedge \ldots \wedge v_{\sigma(p)})\otimes(v_{\sigma(p+1)}\wedge \ldots \wedge v_{\sigma(n)}),$$

in which the second sum is over all $(p,n-p)$-shuffles and $\varepsilon(\sigma)$ is the Koszul sign of $\sigma$.


The counit and coaugmentation are the natural mappings $\bigwedge V \to k$, and $k\to \bigwedge V$ respectively.

If $C$ is a conilpotent pre-cgc, any pre-gvs morphism $f:C \to V$ for which $f(1) = 0$ admits a unique lifting to a pre-cgc morphism $\hat{f} : C \to \bigwedge' V$.

There is an injective homomorphism of pre-gcs
$$\chi : \bigwedge{\!}' V \to T'(V)$$
given by
$$\chi(x_1\wedge \ldots x_n) = \sum_\nu \varepsilon(\nu)x_{\nu(1)}\otimes \ldots \otimes x_{\nu(n)},$$
where the sum is over all permutations and $\varepsilon(\sigma)$ is the corresponding Koszul sign.  It has, as image, all the symmetric tensors (in the graded sense).

On $\bigwedge' V$ and $T'(V)$, the filtration of the primitives comes from a gradation

$$F_p\bigwedge{\!}' V = \bigwedge^{\leq p}V = \bigoplus_{k\leq p}\bigwedge^k V;$$
$$F_p T'(V) = T^{\leq p}(V) = \bigoplus_{k\leq p} T^k(V).$$




## Related concepts

### Differential graded algebras

Dually, a [[dg-algebra]] is a [[monoid]] in [[chain complex]]es.

### Semifree dg-coalgebras and $L_\infty$-algebras 

The notion of dg-coalgebra whose underlying [[coalgebra]] is cofree is related by duality to that of [[semifree dga]].

Semicofree dg-coalgebras concentrated in negative degree and with differential of degree -1 are  the same as [[L-∞-algebras]]

### Model category structure

There is a [[model structure on dg-coalgebras]].


## Properties

### As filtered colimits of finite-dimensional pieces
 {#AsFilteredColimits}

+-- {: .num_prop }
###### Proposition

Every dg-coalgebra is the [[filtered colimit]] of its finite-dimensional sub-dg-coalgebras.

=--

This is due to ([Getzler-Goerss 99](#GetzlerGoerss99)), in generalization to the analogous fact for plain [[coalgebras]], see at _[coalgebra -- As filtered colimits](coalgebra#AsFilteredColimits)_. 


See also at _[[L-infinity algebra]]_ the section _[Ind-Conilpotency](L-infinity-algebra#IndConilpotency)_. This plays a role for instance for constructing [[model structures for L-infinity algebras]], see [there](model+structure+for+L-infinity+algebras#OnProAlg).


## References

The [[model structure on dg-coalgebras]] is due to 

* {#GetzlerGoerss99} [[Ezra Getzler]], [[Paul Goerss]], _A model category structure for differential graded coalgebras_, 1999 ([ps](http://www.math.northwestern.edu/~pgoerss/papers/model.ps), [[GetzlerGoerss99.pdf:file]])





[[!redirects differential graded coalgebras]]

[[!redirects dg-coalgebra]]
[[!redirects dg-coalgebras]]

