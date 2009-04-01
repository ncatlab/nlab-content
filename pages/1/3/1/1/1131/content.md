{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
{:goal: style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
+-- {: goal}
###### Lexicon entry on
##Differential graded Lie algebras (DGLA)


(The previous entry in this lexicon can be found at [[differential graded coalgebra]].) 
=--
##Differential graded Lie algebras

A _pre-graded Lie algebra_ (pre-gla) is a [[graded vector space|pre-gvs]], $L$, together with a bilinear map of degree zero

$$[\quad,\quad ] : L\otimes L \to L,$$

such that

$$[x,y] = (-1)^{|x||y|+1}[y,x]$$

and 

$$(-1)^{|x||z|}[x,[y,z]] +(-1)^{|y||x|}[y,[z,x]] +(-1)^{|z||y|}[z,[x,y]] = 0$$

for every triple $(x,y,z)$ of homogeneous elements in $L$.

(The first property is call _antisymmetry_, the second _the Jacobi identity_.)

A _morphism_ $f: L \to L^\prime$ of pre-glas is a linear map of degree zero, that is compatible with the brackets,

$$f[x,y] = [f(x),f(y)].$$

####Examples

a) To any augmented pre-ga $A$, one can associate a pre-gla, denoted $\bar{A}_L$, with underlying gvs $\bar{A}$ and with bracket, the commutator, $[x,y] = xy -(-1)^{|x||y|}yx$ for each pair $(x,y)$ of homogeneous elements.  $\bar{A}_L$ is abelian (i.e. with trivial bracket) if and only if $A$ is graded commutative.

b) If $A$ is a pre-cga and $L$ is a pre-gla, the tensor product $A\otimes L$ has a pre-gla structure with bracket

$$[a\otimes l,a^\prime\otimes l^\prime] = (-1)^{|a||l|}aa^\prime \otimes [l,l^\prime]$$

for $a,a^\prime, l, l^\prime$ homogeneous.


####Derivations of graded Lie algebras

Let $L$ be a pre-gla.  A _derivation_ of glas, of degree $p\in \mathbb{Z}$, is a linear mapping $\theta \in Hom_p(L,L)$ such that

$$\theta[x,y] = [\theta{x},y] + (-1)^{p|x|}[x,\theta(y)]$$

for any pair $x,y$ of homogeneous elements of $L$.  We denote by $Der_p(L)$, the vector space of degree $p$ derivations of the gla, $L$.

###Differential graded Lie algebras

A differential $\partial$ of a pre-gla is a Lie algebra derivation of degree -1 such that $\partial\circ \partial = 0$.  The pair $(L,\partial)$ is then called a _differential pre-graded Lie algebra_ (pre-dgla); its homology $H(L,\partial)$, is a pre-gla.  

A morphism of pre-dglas is a morphism for both the underlying pre-gla and the pre-dgvs. We denote the corresponding category  by $pre-DGLA$.

####Examples

a) If $(A,\partial)$ is an augmented pre-dga, $(\bar{A}_L,\partial)$ is a pre-dgla.

b) If $(A,\partial)$ is a pre-cdga and $(L,\partial^\prime)$, a pre-dgla, $A \otimes L$, together with the tensor product differential, is a pre-dgla.

c)  Let $(V,\partial)$ be a pre-dgvs, then the pre-dgvs, $(Hom(V,V),D)$, constructed earlier is a pre-dga  for the multiplication law given by composition of mappings.  Its associated pre-dgla has

$$[f,g] = f\circ g - (-1)^{|f||g|}g\circ f$$

and 

$$Df = [\partial,f].$$

In particular, if $(V,\partial) = (A,d)$ is a cdga (resp. $(V,\partial) = (L,\partial)$ is dgla), then $Der(A,d) = (\bigoplus_p Der_p(A),D)$, (resp. $Der(L,\partial) = (Der_p(L),D)$) is a sub-pre-dgl of $(Hom(V,V),D)$.


####DGLA

A dgla is a pre-dgla with a lower grading; explicitly:


###Definition

A **differential graded Lie algebra**, $(L,\partial)$, is a graded vector space $L = \bigoplus_{p\geq 0}L_p$, together with a bilinear map of degree 0
$$[\quad ,\quad] : L\otimes L \to L,$$
and a differential $\partial$ satisfying 
$$\partial L_p \subseteq L_{p-1},  \quad [x,y] = (-1)^{|x||y|+1}[y,x],$$
$$(-1)^{|x||z|}[x,[y,z]] +(-1)^{|y||x|}[y,[z,x]] +(-1)^{|z||y|}[z,[x,y]] = 0$$
and
$$\partial[x,y] = [\partial x,y] + (-1){|x|}[x,\partial y]$$
for every triple $(x,y,z)$ of homogeneous elements in $L$.

Let $DGLA$ be the corresponding category.



A dgla is $n$-_reduced_ (resp. _homologically $n$-reduced_) if $L_p = 0$ (resp. $H_p(L,\partial) = 0$) for all $p\lt n$.  Denote by $DGLA_n$ (resp.  $DGLA}_{hn}$), the corresponding categories.

####Filtrations

If $(L,\partial)$ is a pre-dgla, a _gla-filtration_ of $L$ (resp. a _dgla-filtration_ of $( L,\partial)$ ) is a family of subgraded vector spaces $F_p L$, $p\in \mathbb{Z}$, such that $F_p L\subseteq F_{p+1}L$, $[F_p L,F_n L]\subseteq F_{p+n} L$, (resp. and $\partial F_p L\subseteq F_p L$).

####Bracket length filtration

Let $L$ be a pre-gla.  Its _bracket length filtration_ is obtained from the descending central series:

$$F^1 L = L; \quad F^p L = [L,F^{p-1} L] \quad  if \quad p\geq 2.$$

It is a gla-filtration.

$Q(L) = L/F^2L$ is called the _space of indecomposables_ of $L$.

If $(L,\partial)$ is a pre-dgla, $F^p L$ is stable by $\partial$.  Letting $Q(\partial)$ be the induced differential on $Q(L)$, $Q$ then defines a functor
$$Q : pre\!-\!DGLA \to pre\!-\!DGVS.$$

####Free Lie algebra, $\mathbb{L}(V)$.

Let $V$ be a pre-gvs, $T(V)$, the tensor algebra on $V$ with augmentation ideal $\overline{T(V)}$ (recall $T(V) = \bigoplus_{n\geq 0} V^{\otimes n}$ and the augmentation sends $V (= V^{\otimes 1}$ to 0). 

 Let $\overline{T(V)}_L$ be $\overline{T(V)}$ with the pre-gla structure given by the commutators.  We denote by $\mathbb{L}(V)$, the Lie subalgebra of $\overline{T(V)}_L$ generated by $V$. 
+--{:query}
[[Tim Porter|Tim]]: A more explicit description may help here, cf. Quillen, Rational Homotopy theory (p.281) or MacLane, Homology.
=--
If $L$ is a pre-gla, any morphism of pre-gvs $f: V\to L$ has a unique extension to a pre-gla morphism $\hat{f} :\mathbb{L}(V)\to L$.  If $(e_\alpha)_{\alpha\in I}$ is a homogeneous basis for $V$, $\mathbb{L}(V)$ may be denoted $\mathbb{L}((e_\alpha)_{\alpha\in I})$.

On the free Lie algebra $\mathbb{L}(V)$, the bracket length filtration comes from a gradation $\mathbb{L}(V) = \bigoplus_j\mathbb{L}^j(V) $, where $\mathbb{L}^j(V) $ is the subspace generated by the brackets of elements of $V$ of length $j$.  The inclusion $\mathbb{L}(V)\hookrightarrow T(V)$ identifies $\mathbb{L}^j(V)$ with $\mathbb{L}(V)\cap T^j(V)$.

If $\mathbb{L}(V), \partial)$ is a dgla, free as a gla, with $V$ fixed, $\partial$ is the sum of derivations $\partial_k$ defined by : $\partial_k \subset \mathbb{L}^k(V)$.  The isomorphism between $V$ and $Q\mathbb{L}(V)$ identifies $\partial_1V$ with $Q(\partial)$.  $\partial_1$ (resp. $\partial_2$) is called the _linear part_ (resp, the _quadratic part_) of $\partial$.




####Products and Coproducts (sums)

Let $(L,\partial)$ and $(L^\prime,\partial^\prime)$ be two dglas.  Their _product_ $(L,\partial)\times(L^\prime,\partial^\prime)$ in $DGLA$ is defined by:

*  the underlying vector space is the direct sum $L\oplus L^\prime$;

*  $(L,\partial)$ and $(L^\prime,\partial^\prime)$ are two sub differential graded Lie algebras of $(L,\partial)\times(L^\prime,\partial^\prime)$;

*  if $x\in L$ and $x^\prime \in L^\prime$, then $[x,x^\prime] = 0$.

Their _coproduct_ or _sum_ $(L,\partial)\star(L^\prime,\partial^\prime)$ is often called their _free product_. 

 For example.

$$\mathbb{L}(V)\star \mathbb{L}(V^\prime) \cong   \mathbb{L}(V\oplus V^\prime).$$

More generally if $L$ and $L^\prime$ are given by generators and relations

$$L = \mathbb{L}(V)/I , \quad L^\prime = \mathbb{L}(V^\prime)/I^\prime ,$$

$$L\star L^\prime = \mathbb{L}(V\oplus V^\prime)/{I,I^\prime}.$$

The differential on $L\star L^\prime$ is the unique Lie algebra derivation extending $\partial$ and $\partial^\prime$.






{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
{:goal: style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
+-- {: goal}

###### Lexicon links onwards:

[[Tim Porter|Tim]]:  The lexicon will continue on a new entry on [[differential graded Hopf algebra|differential graded Hopf algebras]].  
=--