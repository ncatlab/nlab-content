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

