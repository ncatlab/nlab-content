
\tableofcontents


## Idea

**Double gluing**, coupled with orthogonality, is a method for creating new models of [[linear logic]] such as [[star-polycategories]] and [[star-autonomous categories]]. It is a variation of gluing methods (such as [[Artin gluing]]) that works for classical rather than intuitionistic (linear) logic. It is a general method that encompases many existing spaces such as [[phase spaces]], [[coherence spaces]], [[finiteness spaces]], [[totality spaces]], [[probabilistic coherence spaces]].

Although the name presumably refers to gluing along "two functors at once", it turns out to also be closely connected to [[double categories]], and in particular to [[comma double categories]]. 


## Double gluing along hom-sets with orthogonality

### Coherence spaces via double gluing

We begin with the definition of [[coherence spaces]], presented in a way that is amenable to generalization.

If $u\subset X$ and $v\subseteq X$, write $u\perp v$ if $|u\cap v|\leq 1$. Given $U\subseteq P(X)$, let ${U}^\perp=\{v \subseteq X \mid \forall u \in U. u \perp v\}$. Now a [[coherence space]] can be given by a set $X$ together with a set $U\subseteq P(X)$ of cliques and a set $V\subseteq P(X)$ of co-cliques that are orthogonal in the sense that $U=V^\perp$ and $V=U^\perp$. 

In this presentation of coherence spaces, we can regard $u$ as a relation $1\to X$, and $v$ as a relation $X\to \bot$. The relation $\perp$ is then a family of subsets $\perp_X\subseteq [1\to X]\times [X\to \bot]$. 

### General definition of double gluing along hom-sets with tight orthogonality

Let $C$ be a [[symmetric monoidal category]] with an object $I^*$, and let a family $\perp_X\subseteq C(I,X)\times C(X,I^*)$ of relations be given. (For coherence spaces, let $C=Rel$ and $I=I^*$ and $\perp$ be as above. 

Let $X$ be an object of $C$. The relation $\perp$ defines a [[Galois connection]] between $C(I,X)$ and $C(X,I^*)$ in the usual way: for ${U}\subseteq C(I,X)$ we have ${U}^\perp = \{ v \in C(X,I^*) \mid \forall u\in {U}. u\perp v \}$, and likewise for ${V}\subseteq C(X,I^*)$ we have ${V}^\perp = \{ u \in C(I,X) \mid \forall v\in {V}. u\perp v \}$.

We define a **tight orthogonality space** $(X,U,V)$ to be an object $X\in C$ together with ${U}\subseteq C(I,X)$ and ${V}\subseteq C(X,I^*)$ that is a fixed point of this Galois connection, ${U}^\perp = {V}$ and ${V}^\perp= U$.  
A **morphism** between tight orthogonality spaces $(X_1,{U_1},{V_1})\to (X_2,{U_2},{V_2})$ is a morphism $f\in C(X_1,X_2)$ such that

1. if $u\in {U_1}$, then $f\circ u \in {U_2}$;
2. if $v\in{V_2}$ then $v\circ f\in {V_1}$.

**Theorem:** (Hyland-Schalk): If an orthogonality $\bot_X\subseteq C(I,X)\times C(X,I^*)$ on a star-autonomous category satisfies four conditions for orthogonalities, a symmetry condition, and a precision condition, then the tight orthogonality spaces form a [[star-polycategory]].

One source of good orthogonality relations $\bot_X\subseteq C(I,X)\times C(X,I^*)$ are the focuses $F\subseteq C(I,I^*)$, from which we can let 
$u\bot_X v$ if $(v\circ u)\in F$. However, not all the useful orthogonalities arise from focuses.

### Examples

* [[coherence spaces]]: Let $C=Rel$, and let $u\bot_X v$ if $|u\cap v|\leq 1$.
* [[totality spaces]]: Let $C=Rel$, and let $u\bot_X v$ if $|u\cap v|=1$.
* [[finiteness spaces]]: Let $C=Rel$, and let $u\bot_X v$ if $|u\cap v|\lt\omega$.
* [[phase semantics]]: Let $M$ be a commutative monoid, and let $F\subseteq M$ be given. Regarding $M$ as a one-object category, with object $I$, we put $u\bot_I v$ if $vu\in F$. Then an object of the orthogonality category $(I,U,V)$ is determined by a "fact" $U\subseteq M$. However, to get the poset version of phase semantics we restrict the morphisms of the orthogonality category to the ones that come from the identity $I\to I$. 
* probabilistic coherence spaces: Let $C$ be the category of weighted relations, i.e. countable sets and $[0,\infty]$-valued matrices between them. Let $u\bot_X v$ if $(v\circ u)\in [0,1]$. In other words, the focus $F\subseteq C(I,I^*)$ comprises the scalars in $[0,1]$. One then cuts down further to impose a bounded completeness condition.
* quantum causal structure: Let $C=CP$, the category of finite dimensional Hilbert spaces and completely positive maps between them (see [[quantum operation]], although here we do not begin by insisting that they are trace preserving). Let $u\bot_X v$ if $v\circ u=1$. In other words, the focus $F\subseteq CP(\mathbb{C},\mathbb{C})$ is the singleton map $\{1\}$. Now, for any finite dimensional Hilbert space $X$, $\{trace_X\}^\perp$ comprises "states" of $X$, and a morphism
$(X,\{trace_X\}^\perp,\{trace_X\}^{\perp\perp})\to (Y,\{trace_Y\}^\perp,\{trace_Y\}^{\perp\perp})$ is the same thing as a [[quantum operation]], i.e. a completely positive trace preserving map.
* [[Frölicher spaces]]: Let $C=Set$, let $I=I^*=\mathbb{R}$, and let $u\bot_X v$ if $(v\circ u):\mathbb{R}\to\mathbb{R}$ is smooth. In other words, the focus $F\subseteq C(\mathbb{R},\mathbb{R})$ comprises the smooth maps.

## General double gluing

Let $C$ be any (symmetric) [[polycategory]] and $E$ a co-subunary polycategory (i.e. all morphisms have codomain arity 0 or 1), and let $L:C\to Chu(E)$ be a polycategory functor.  We consider $C$ as a vertically discrete [[double polycategory]] and $L$ as a functor $C\to \mathbb{C}hu(E)$ into the [[double Chu construction]].  Similarly, consider $Chu(E)$ as a vertically discrete double polycategory, including into $\mathbb{C}hu(E)$ as the horizontal polycategory.

The **double gluing** polycategory is then the [[comma double category|comma double]] polycategory (i.e. the [[comma object]] in the 2-category of polycategories)
\begin{tikzcd}
  Gl(L) \ar[d] \ar[r] \ar[dr,phantom,"\Downarrow"] & Chu(E) \ar[d] \\
  C \ar[r,"L"'] & \mathbb{C}hu(E)
\end{tikzcd}

Note that:

1. If $C$ is a multicategory (i.e. a co-unary polycategory), then so is $Gl(L)$.

2. If $E$ has a counit that is terminal so that $Chu(E) = Chu(E,1)$, $C$ is a representable multicategory (i.e. a symmetric monoidal category), and $E$ is representable and closed with products so that $Chu(E,1)$ is a $\ast$-autonomous category, then polycategory functors $C\to Chu(E)$ are equivalent to pairs of a lax symmetric monoidal functor $L:C\to E$ and a functor $K:C\to E^{op}$ together with a "contraction" $L(R) \otimes K(R\otimes S) \to K(S)$ satisfying a few axioms.  This is how the definition is phrased in [Hyland and Schalk](#HylandSchalk).

3. If $C$ is a $\ast$-polycategory, then $\ast$-polycategory functors $L:C\to Chu(E)$ are equivalent to functors $U_{\le 1} C\to E$ where $U_{\le 1} C$ is the underlying co-subunary polycategory of $C$.  If $E$ has a counit that is terminal so that $Chu(E) = Chu(E,1)$, then these are equivalent to multicategory functors $U_{=1} C \to E$.  In particular, we can double-glue along any lax symmetric monoidal functor with $\ast$-autonomous domain.

If $C$ and $E$ are closed and representable with sufficient limits and colimits, then one can show (similarly to the conditions for a Chu construction to be representable) that $Gl(L)$ is also representable (as a multicategory or a polycategory, respectively) and closed.  Thus, double gluing can produce closed symmetric monoidal and $\ast$-autonomous categories.

The case of double gluing along hom-functors, discussed above, is the case when $E=Set$ so that $Chu(E,1)$ is $\ast$-autonomous, as above, and $L(X) =C(I,X)$ with $K(X) = C(X,I^*)$, together with a restriction that the gluing morphisms be monic (and the additional "orthogonality" restriction.

## References

* Audrey M. Tan, Full Completeness for models of Linear Logic, PhD thesis, Cambridge (1997) &lbrack;[pdf](/nlab/files/FullCompletenessForModelsOfLinearLogicTan.pdf)&rbrack;

* {#HylandSchalk} [[Martin Hyland]] and Andrea Schalk, _Glueing and orthogonality for models of linear logic_, Theoretical Computer Science 294 (2003) 183–231 ([pdf](https://core.ac.uk/download/pdf/21173316.pdf))
 
* [[Aleks Kissinger]] and Sander Uijlen, _A  categorical semantics for causal structure_. Arxiv [1701.04732](https://arxiv.org/abs/1701.04732).

An abstract understanding of the double glueing construction:

* [[Richard Garner]]: *Three investigations into linear logic*, MSc thesis, Macquarie (2005) &lbrack;[pdf](https://web.science.mq.edu.au/~rgarner/Thesis/Smith-Knight-Essay.pdf), [[Garner-LinearLogic.pdf:file]]&rbrack;


[[!redirects double gluing construction]]
[[!redirects double gluing constructions]]

