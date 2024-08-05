There are several notions under a name of compatible localization; where localization pertains to the localization of rings or of localization of categories. 

## (Pairwise) compatibility of a family of localizations 

Consider a family of localizations sharing the same source ring (or source category). Two Gabriel localizations $i_{R k}: R\to R_k$, $k = 1,2$ of a ring $R$, with 
corresponding localization endofunctors for modules $Q_{k}:M\to M_k$ are mutually compatible if the consecutive localization of $Q_2 Q_1 R$ is naturally a ring and $Q_1 Q_2 R$ is a ring (semi-compatible if just one of the two), such that the corresponding localization arrow is a morphism of rings. This is equivalent to the following more general criterium.  

Two [[affine localization]]s with the inverse image functors
$Q_k^*$ and direct image functors $Q_{k*}: A\to A_k$, $k = 1,2$ are mutually compatible if the endofunctors $Q_k:=Q_{k*}Q_k^*$ mutually commute as endofunctors of $A$.

According to Thomason-Trobaugh, an [[algebraic scheme]] is **semiseparated** if it has an affine cover such that the intersection of any two affines in the cover is affine (semiseparated cover). For example, every [[separated scheme]] is semiseparated. [[Alexander Rosenberg]] extends this terminology to [[noncommutative scheme]]s by observing that an affine cover is semiseparated iff the corresponding localization functors restricting the category of quasicoherent sheaves on the whole scheme to an element of a cover, form a compatible family of affine localizations.  


## Compatible Ore localizations

Let $S$ and $T$ be two Ore sets in a domain $R$ and $i_T:R\to T^{-1}R$ the canonical map. Then $i_T(S)$ is left Ore in $T^{-1}R$ if for every $r\in R$, $t\in T$ and $s\in S$, there are $s'\in S$, $r'\in R$ and $t'\in T$ such that $s' t^{-1} r = t'^{-1}r' s$ in $T^{-1} R$.  
(This can be written as $t^{-1}r s^{-1} = s'^{-1}t'^{-1}r'$ in the module $T^{-1}S^{-1}T^{-1}R$.) 
We claim that it is sufficient to have this condition satisfied for $r = 1$. Indeed, find $\tilde{s}\in S$ and $\tilde{r}\in R$ so that $\tilde{s}r = \tilde{r} r$. We then find $t_1\in T$, $s_1\in S$ and $r_1\in R$ so that 
$s_1 t^{-1} = t^{-1}_1 r_1 \tilde{s}$. It follows that 
$s_1 t^{-1} r = t_1^{-1} r_1\tilde{s} r = t_1^{-1}(r_1\tilde{r})s$.

This could be found more readily by computing in the ring $(T\vee S)^{-1} R$ or module $T^{-1}S^{-1}T^{-1}R$ where the above condition is $t^{-1}r s^{-1} = s'^{-1}t'^{-1}r'$ . This can be interpreted also as $S^{-1} T^{-1} R\subset T^{-1}S^{-1}R$ within $(T\vee S)^{-1} R$. Then it is easy to use $r = 1$ case by $t^{-1} r s^{-1} = t^{-1}\tilde{s}^{-1}\tilde{r} = s_1^{-1}t_1^{-1}r_1\tilde{r}$. 


## Coaction compatible localizations

Given a right $B$-comodule algebra $(E, \rho)$ for a bialgebra $H$, with coaction $\rho : E\to E\otimes H$, an Ore localization 
of rings (or more general affine localization) $j : E\to E'$ is $\rho$-compatible if there exists a morphism $\rho': E'\to E\otimes H$ 
such that the following diagram commutes:

$$\array{
E & \stackrel{j}\to & E'\\
\downarrow\rho && \downarrow \rho'\\
E\otimes H &\stackrel{j\otimes H}\to & E'\otimes H
}$$

## Compatibility of localizations and endofunctors

A localization functor $Q^*=Q^*_\Sigma : A\to B$ 
(not necessarily having a right adjoint) 
universally inverting a family $\Sigma$ of morphisms in $A$
is compatible with an endofunctor $G:A\to A$ if $G(\Sigma)\subset \Sigma$. By the universality property of the localization functor, this is equivalent to the existence of a functor $G_\Sigma\in B$ 
such that $Q^* G = G_\Sigma Q^*$. 

If $Q^*$ is a localization having a fully faithful right adjoint $Q_*$, with counit $\epsilon$ (which is hence iso) and unit $\eta$; then the compatibility of $Q^*$ with an endofunctor $G$ is equivalent to any of the following:

(i) there exists a distributive law $l : Q_* Q^* G\to G Q_* Q^*$ where $Q_* Q^*$ is understood as (the underlying functor of) the idempotent monad induced by the adjunction $Q^*\dashv Q_*$

(ii) the natural transformation $Q^* G\eta : Q^* G\to Q^* G Q_* Q^*$ is invertible

(iii) there is a functor $G'$ and a natural isomorphism $Q^* G\cong G' Q^*$.

If (i) holds then $l$ is invertible and uniquely determined
by $G$ and the monad $Q^* Q_*$. Notice that $Q_* G_\Sigma \neq G Q_*$ in general. See [[zoranskoda:distributive law for idempotent monad]] for more.

One can also consider the distributive laws $\tilde{l} : G Q_* Q^*\to Q_* Q^* G$. The inverse $l^{-1}$ of the distributive law $l: G Q_* Q^*\to Q_* Q^* G$ as above is the unique invertible example of such. It is not clear (to me at least -- [[Zoran Škoda|Zoran]]) if there are also noninvertible examples for $\tilde{l}$.  

## Literature

For the pairwise compatibility of localizations see

* [[Fred Van Oystaeyen]], _Compatibility of kernel functors and localization functors_, Bull. Soc. Math. Belg. __28__ (1976), no. 2, 131--137. 

* [[Alain Verschoren]], _Compatibility and stability_, 
Notas de Matem&#225;tica [Mathematical Notes], 3. Universidad de Murcia, Secretariado de Publicaciones e Intercambio Cient&#237;fico, Murcia, 1990. xii+81 pp. ISBN: 84-7684-934-6 

* J. Mulet, A. Verschoren, _On compatibility. II._, Comm. Algebra 20 (1992), no. 7, 1897--1905. [doi](http://dx.doi.org/10.1080/00927879208824438)

* M. I. Segura, D. Tarazona, A. Verschoren, _On compatibility_,  Comm. Algebra __17__ (1989),  no. 3, 677--690. [doi](https://doi.org/10.1080/00927878908823751)

The compatibility of coactions with Ore localizations is introduced in 

* [[Zoran Škoda]], _Localizations for construction of quantum coset spaces_, in "Noncommutative geometry and Quantum groups", W.Pusz,  P.M. Hajac, eds. Banach Center Publications __61__, pp. 265--298, Warszawa 2003, [math.QA/0301090](https://arxiv.org/abs/math.QA/0301090).

The compatibilities between localization functors 
with endofunctors is formulated in 

* [[V. A. Lunts]], [[A. L. Rosenberg]], _Differential calculus in noncommutative algebraic geometry I. D-calculus on noncommutative rings_, MPI 1996-53 [pdf](http://www.mpim-bonn.mpg.de/preprints/send?bid=3894)

A version with distributive laws is introduced in 

* [[Zoran Škoda]], Some equivariant constructions in noncommutative algebraic geometry, Georgian Mathematical Journal 16 (2009), No. 1, 183--202, [arXiv:0811.4770](http://arxiv.org/abs/0811.4770).

See also 

* [[Zoran Škoda]], _Compatibility of (co)actions and localization_, [arXiv:0902.1398](http://arxiv.org/abs/0902.1398) (preliminary version).

[[!redirects compatible localizations]]