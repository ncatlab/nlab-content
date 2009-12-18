[[!redirects A Survey of Elliptic Cohomology - compactifying the derived moduli space]]


<div class="rightHandSide toc">

[[!include higher algebra - contents]]

</div>


>**Abstract** This entry discusses the descent spectral sequence and sheaves in homotopy theory.  Using said spectral sequence we compute $\pi_* tmf_{(3)}$.


+-- {: .standout}

This is a sub-entry of

* [[A Survey of Elliptic Cohomology]]

see there for background and context.

=--

Here are the entries on the previous sessions:


* [[A Survey of Elliptic Cohomology - cohomology theories]]

* [[A Survey of Elliptic Cohomology - formal groups and cohomology]]

* [[A Survey of Elliptic Cohomology - E-infinity rings and derived schemes]]

* [[A Survey of Elliptic Cohomology - elliptic curves]]

* [[A Survey of Elliptic Cohomology - equivariant cohomology]]

 
* [[A Survey of Elliptic Cohomology - derived group schemes and (pre-)orientations]]

* [[A Survey of Elliptic Cohomology - A-equivariant cohomology]]

* [[A Survey of Elliptic Cohomology - the derived moduli stack of derived elliptic curves]]

* [[A Survey of Elliptic Cohomology - towards a proof]]

* [[A Survey of Elliptic Cohomology - compactifying the derived moduli stack]]

***


#The Descent Spectral Sequence#
* automatic table of contents goes here
{:toc}

##The spectral sequence##

We would like to understand the following theorem.

**Theorem.** Let $( X, \mathbf{O})$ be a derived Deligne-Mumford stack.  Then there is a spectral sequence
$$H^s (X ; \pi_t \mathbf{O}) \Rightarrow \pi_{t-s} \Gamma (X , \mathbf{O}).$$

###Recalling what is what###
Let $X$ be an $\infty$-topos, heuristically $X$ is ''sheaves of spaces on an $\infty$-category $C$.''  Further $\mathbf{O}$ is a functor $\mathbf{O} : \{ E_\infty \}^{op} \to X$, which for a cover $U$ of $C$ formally assigns
$$A \mapsto (U \mapsto \mathrm{Hom} (A , \mathbf{O} (U))).$$
Via DAG V 2.2.1 we can make sense of global sections and $\Gamma (X , \mathbf{O})$ is an $E_\infty$-ring.

Given an $\infty$-category $C$ we can form the subcategory of $n$ _truncated objects_ $\tau_{\le n} C$ which consists of all objects such that all mapping spaces have trivial homotopy groups above level $n$. Further $\tau_{\le n} : C \to C$ defines a functor which serves the role of the Postnikov decomposition.

Let $X$ be an $\infty$-topos, define $\mathrm{Disc} \; X : = \tau_{\le 0} X$.  Further define functors $\pi_n : X_* \to N (\mathrm{Disc} \; X)$ by
$$Y \mapsto \tau_{\le 0} \mathrm{Map} (S^n , Y) = \pi_n (Y) .$$

**Facts.**

1. For $A \in \mathrm{Disc} \; X$ an abelian group object there exists $K(A,n) \in X$, such that
$$ H^n (X, A) := \pi_0 \mathrm{Map} (1_X , K(A,n)) $$
corresponds to sections of $K(A,n)$ along the identity of $C$.

1. If $C$ is an ordinary site, $H^n (X, A)$ corresponds to ordinary sheaf cohomology (HTT 7.2.2.17).


###The non-derived descent ss###
Let us define a mapping space $\mathrm{Tot} \; X = \mathrm{hom}^\Delta (\Delta , X)$, this is the hom-set as simplicial objects.  Now
$$\mathrm{Tot} \; X = \lim ( \dots \to \mathrm{Tot}^n \; X \to \mathrm{Tot}^{n-1} \; X \to \dots \to \mathrm{Tot}^0 \to * ) ,$$
where $\mathrm{Tot}^n \; X = \mathrm{Tot} (\mathrm{cosk}_n X )$.
We have a homotopy cofiber sequence
$$F_n \to \mathrm{Tot}^n \; X \to \mathrm{Tot}^{n-1} \; X$$
and it is a fact that
$$F_s \simeq \Omega^s ( \prod_{|I|=s+1} \mathbf{O} (U_I )),$$
for the fibered product $U_I$ corresponding to the cover $\{ U_i \to N\}$ of an object $N$ of the etale site of $M_{1,1}$.

Applying $\pi_*$ to the cofiber sequence we obtain an exact couple and hence a spectral sequence with 
$$ E^1_{t,s} = \pi_{t-s} F_s \Rightarrow \lim_n \pi_{t-s} \mathrm{Tot}^n X  = \pi_{t-s} \mathrm{Tot} X = \pi_{t-s} \mathbf{O} (N). $$ 
Note that $\pi_{t-s} F_s$ is the Cech complex of the cover, so the $E^2$-page calculates Cech cohomology.  If we choose an affine cover, hence acyclic and $\lim^1 =0$, then 
$$E^2_{t,s} \Rightarrow H^s (N, \pi_t \mathbf{O}) .$$


##Stacks and Hopf Algebroids##

Let $X$ be a (non-derived) Deligne-Mumford stack on $\mathrm{Aff}$ and let $\mathrm{Spec} \; A \to X$ be a faithfully flat cover, then
$$ \mathrm{Spec} \; A \times_X \mathrm{Spec} \; A = \mathrm{Spec} \; \Gamma,$$
for some commutative ring $\Gamma$. Via the projection maps (which are both flat) we have a groupoid in $\mathrm{Aff}$, by definition it is a [[Hopf algebroid]] $(A, \Gamma)$.

Now let $(A,\Gamma)$ be a Hopf algebroid, then the collection of principal bundles form a stack $M_{A,\Gamma}$.  Here a principal bundle is a map of schemes $P \to X$, a $\mathrm{Spec} \; \Gamma$ equivariant map $P \to \mathrm{Spec} \; A$, where the action is given by a map $P \times_{\mathrm{Spec} A} \mathrm{Spec} \; \Gamma \to P$. In this we have an equivalence of 2-categories
$$ \{DM \; Stacks\} \simeq \{Hopf \; Algebroids, \; bibundles\} .$$
and
$$ \{DM \; stacks \; equipped \; with \; cover\} \simeq \{Hopf \; algebroids, \; functors \; of \; groupoids\}. $$

Let $X$ be a scheme then a sheaf of abelian groups is a functor
$$\mathfrak{I} : \mathrm{Aff}/X^{op} \to \mathrm{Ab} .$$
The structure sheaf $\mathbf{O}_X$ is defined by
$$ \mathbf{O}_X ( \mathrm{Spec} \; A \to X) = A .$$
Let $\mathfrak{I}$ be a sheaf of $\mathbf{O}_X$ modules.  $\mathfrak{I}$ is quasi-coherent if for any map $\mathrm{Spec} \; B \to \mathrm{Spec} \; A$ and maps $f: \mathrm{Spec} \; A \to X$, $g: \mathrm{Spec} \; B \to X$ we have
$$ B \otimes_{A} \mathfrak{I} (f) \simeq \mathfrak{I} (g) .$$
We have an equivalence of categories $\mathrm{QCSh}/\mathrm{Spec} \; A \simeq A$-mod via the assignment $\mathfrak{I} \mapsto \mathfrak{I} (1_A)$.

Now consider the stack $M_{A,\Gamma}$ from above.  One can show that quasi-coherent sheaves over $M_{A, \Gamma}$ is nothing but a $(A,\Gamma)$ [[comodule]], that is an $A$-module, $M$, and a coaction map of $A$-modules
$$M \to \Gamma \otimes^{d_1}_{A} M$$
where the right hand side is an $A$-module via the map $d_0$.

##Cohomology of Sheaves##
Recall that sheaf cohomology is obtained by deriving the global sections functor.  If $X$ is a [[noetherian scheme|noetherian]] scheme/stack then we restrict to deriving
$$ \Gamma (-) : \mathrm{QCSh}/X \to \mathrm{Ab} .$$
Suppose further that $X = \mathrm{Spec} \; A$, so $\Gamma$ lands in $A$-modules, however from above we know $\mathrm{QCSh}/\mathrm{Spec} \; A \simeq A$-mod, hence $\Gamma$ is exact and all higher cohomology groups vanish.

Let $\mathfrak{I}_N$ be a quasi-coherent sheaf on a DM stack $M_{A,\Gamma}$.  Then global sections of $\mathfrak{I}_N$ induce global sections $n \in N$ such that the two pullbacks to $\Gamma$ correspond to each other
$$ \Gamma \otimes_A^{d_0} N \to \Gamma \otimes_A^{d_1} N; \; 1 \otimes n \mapsto 1 \otimes n .$$
That is the coaction map $n \mapsto 1 \otimes n$ is well defined and $n: A \to N; \; 1 \mapsto n$ is a map of comodules.  This allows us to interpret global sections as
$$ \mathrm{Hom}_{A,\Gamma} (A, -) : \mathrm{Comod}_{A,\Gamma} \to A-\mathrm{mod} ,$$
so a section is a map from the trivial sheaf to the given sheaf.  It follows that
$$ H^n ( M_{A,\Gamma} , \mathfrak{I}_N ) = \mathrm{Ext}^n_{A,\Gamma} (A,N) .$$
To simplify notation we write the above as $H^n (A, \Gamma ; N)$ and if the $N$ is suppressed it is assumed that $N=A$.  In general we compute these Ext groups via the [[cobar complex]].

###Change of Rings###
Let $(A,\Gamma)$ be a Hopf algebroid and $f: A \to B$  a ring homomorphism.  Define
$$ \Gamma_B = B \otimes_A^{d_0} \Gamma \otimes_A^{d_1} B ,$$
so we have a map of Hopf algebroids $f_* : (A, \Gamma) \to (B, \Gamma_B)$ and of stacks
$$ f^* : M_{B,\Gamma_B} \to M_{A,\Gamma} .$$

**Theorem.** If there exists a ring $R$ and a homomorphism $\Gamma \otimes_A B \to R$ such that
$$A \to \Gamma \otimes_A B \to R $$
is faithfully flat, then $f^*$ is an equivalence of stacks.

###The Weierstrass Stack###
Given $C/S$ an [[elliptic curve]], [[Riemann-Roch theorem|Riemann–Roch]] gives us (locally on $S$) sections $x \in \Gamma (C, \mathbf{O} (2e)) , \; y \in \Gamma (C, \mathbf{O} (3e))$ such that $x^3-y^2 \in \Gamma (C, \mathbf{O}(5e))$ and $C \simeq C_{\underline{a}} \subset \mathbb{P}^2$ is given by
$$ y^2 + a_1 xy + a_3 y = x^3 +a_2 x^2 +a_4 X + a_6 $$
for $a_i \in \mathbf{O}_S$ and $e = [0: 1:0]$.  Such a curve is said to be in Weierstrass form or simply a Weierstrass curve.

Two Weierstrass curves $(C_\underline{a} , e)$ and $(C_{\underline{a}'},e)$ are isomorphic if and only if they are related by a coordinate change of the form
$$ (X,Y) \mapsto (\lambda^{-2} X + r, \lambda^{-3} y + s \lambda^{-2} x +t ) .$$
For instance, this means that $a_1'= \lambda (a_1 +2s)$.  We then build a Hopf algebroid $(A, \Gamma)$ by defining
$$ A = \mathbb{Z} [a_1 , \dots , a_4 , a_6 ] , \; \Gamma = A [r,s,t, \lambda^\pm ] .$$
Further, define the stacks $M_{Weir} = M_{A, \Gamma}$ and $M_{ell} = M_{A[\Delta^{-1}] , \Gamma[\Delta^{-1}]}$.  Note that
$$ M_{ell} \subset \overline{M_{ell}} \subset M_{Weir} .$$

Let $\omega_{C/S} = \pi_* \Omega^1_{C/S}$ (which is locally free) and $\pi_{2n} \mathbf{O} = \omega^n$.  If $C$ is a Weierstrass curve, then $\omega$ is free with generator of degree 2
$$\eta = \frac{dx}{2y + a_1 x +a_3} .$$
Let $\omega^*$ correspond to the graded comodule
$$ A_* = A [ \eta^\pm ] \to \Gamma [\eta^\pm ] = \Gamma_* ; \; \eta \mapsto \lambda^{-1} \eta .$$

It is classical that 
$$ H^{0,*} (A, \Gamma ; A_*) = \mathbb{Z} [c_4 , c_6 , \Delta]/ (12^3 \Delta -c_4^3 +c_6^2 ) $$
that is the ring of modular forms.  So we get a map
$$ \pi_* tmf \to \{modular \; forms \} $$
as the edge homomorphism of our spectral sequence 
$$ H^{s,t} (A,\Gamma ; A_*) \simeq H^{s,t} (A_* , \Gamma_*) \Rightarrow \pi_{t-s} tmf .$$

It should be noted that we have a comparison map with the Adams-Novikov spectral sequence for $MU$.

##$p$-local Coefficients##
###With 6 inverted###
Note that if 2 is invertible than we can complete the square in the Weierstrass equation to obtain
$$ \overline{y}^2 = x^3 + 1/4 b_2 x^2 + 1/2 b_4 x + 1/4 b_6 $$
and the only automorphisms of the curve are $x \mapsto x+r$.  Now if 3 is invertible we complete the cube and have
$$ \overline{y}^2 = \overline{x}^3 -1/48 c_4 \overline{x} -1/864 c_6 $$
and this curve is rigid.  Define $C= \mathbb{Z} [c_4 , c_6 ]$ and $\Gamma_C = C$, then
$$ H^{s,*} (A_* , \Gamma_* ) [1/6] \simeq H^{s,*} (C,C) [1/6] = \mathbb{Z} [1/6 , c_4 , c_6 ] $$
if $s=0$ and 0 otherwise.

###Localized at 3###
It is true that $H^{s,t} (A_* , \Gamma_* ) = H^{s,t} (B, \Gamma_B)$ where
$$ B = \mathbb{Z}_{(3)} [ b_2 , b_4, b_6 ] \to \Gamma_B = B[r] ; \; b_2 \mapsto b_2 + 12r $$
and the degree of $r$ is 4.
We have the class $\alpha = [r] \in H^{1,4}$ and $\beta = [ -1/2 (r^2 \otimes r + r \otimes r^2)] \in H^{2,12}$.

**Theorem.** $H^{*,*} (B, \Gamma_B) = \mathbb{Z} [c_4 , c_6 , \Delta , \alpha, \beta ]$ subject to the following relations

1. $12^3 \Delta -c_4^3 +c_6^2 = \alpha^2 = 3\alpha = 3 \beta =0;$

1. $c_4 \alpha = c_6 \alpha = c_4 \beta = c_6 \beta = 0.$


Now let $I = (3 , b_2 , b_4 )$ and consider the Hopf algebroid $(B/I , \Gamma_B /I)$ which by change of rings theorem is equivalent to $(\mathbf{F}_3 , \mathbf{F}_3 [r]/(r^3))$. By using this Hopf algebroid and the comparison map with the Adams-Novikov spectral sequence one can prove the following theorem.

**Theorem.** The edge homomorphism $\pi_* tmf_{(3)} \to \{Modular Forms\}_{(3)}$ has 

1. Cokernel given by $\mathbb{Z}/3\mathbb{Z} [\Delta^n]$ for $n \ge 0$ and not divisble by 3;

1. Kernel consisting a copy of $\mathbb{Z}/3\mathbb{Z}$ in degrees 3,10,13,20,27,30,37,40 modulo 72.  This is the 3-torsion in $\pi_* tmf$.


For more see

[[Tilman Bauer]], **Computation of the homotopy of the spectrum tmf**. In _Geom. Topol. Monogr_., 13, 2008.