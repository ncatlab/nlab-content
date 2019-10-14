# Double gluing

* table of contents
{: toc}

## Idea

**Double gluing**, coupled with orthogonality, is a method for creating new models of [[linear logic]] such as [[star-polycategories]] and [[star-autonomous categories]]. It is a variation of gluing methods (such as [[Artin gluing]]) that works for classical rather than intuitionistic (linear) logic. It is a general method that encompases many existing spaces such as [[phase spaces]], [[coherence spaces]], [[finiteness spaces]], [[totality spaces]], [[probabilistic coherence spaces]].

Although the name presumably refers to gluing along "two functors at once", it turns out to also be closely connected to [[double categories]], and in particular to [[comma double categories]]. 


## Double gluing along hom-sets with orthogonality

### Coherence spaces via double gluing

We begin with the definition of [[coherence spaces]], presented in a way that is amenable to generalization.

If $u\subset X$ and $v\subseteq X$, write $u\perp v$ if $|u\cap v|\leq 1$. Given $U\subseteq P(X)$, let ${U}^\perp=\{v \subseteq X \mid \forall u \in U. u \perp v\}$. Now a [[coherence space]] can be given by a set $X$ together with a set $U\subseteq P(X)$ of cliques and a set $V\subseteq P(X)$ of co-cliques that are orthogonal in the sense that $U=V^\perp$ and $V=U^\perp$. 

In this presentation of coherence spaces, we can regard $u$ as a relation $1\to X$, and $v$ as a relation $X\to 1$. The relation $\perp$ is then a family of subsets $\perp_X\subseteq [1\to X]\times [X\to 1]$. 

### General definition of double gluing along hom-sets with tight orthogonality

Let $C$ be a [[symmetric monoidal category]] with an object $I^*$, and let a family $\perp_X\subseteq C(I,X)\times C(X,I^*)$ of relations be given. (For coherence spaces, let $C=Rel$ and $I=I^*$ and $\perp$ be as above. 

Let $X$ be an object of $C$. The relation $\perp$ defines a [[Galois connection]] between $C(I,X)$ and $C(X,I^*)$ in the usual way: for ${U}\subseteq C(I,X)$ we have ${U}^\perp = \{ v \in C(X,I^*) \mid \forall u\in {U}. u\perp v \}$, and likewise for ${V}\subseteq C(X,J)$ we have ${V}^\perp = \{ u \in C(I,X) \mid \forall v\in {V}. u\perp v \}$.

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

## References

* [[Martin Hyland]] and Andrea Schalk, _Glueing and orthogonality for models of linear logic_, Theoretical Computer Science 294 (2003) 183–231 ([pdf](https://core.ac.uk/download/pdf/21173316.pdf))
 {#HylandSchalk}

* [[Aleks Kissinger]] and Sander Uijlen, _A  categorical semantics for causal structure_. Arxiv [1701.04732](https://arxiv.org/abs/1701.04732).
