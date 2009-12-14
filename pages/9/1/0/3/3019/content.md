[[!redirects A Survey of Elliptic Cohomology - compactifying the derived moduli space]]


<div class="rightHandSide toc">

[[!include higher algebra - contents]]

</div>


>**Abstract** We sketch how to compactify $M^{Der}$ such that the underlying scheme is the Deligne-Mumford compactification of $M_{1,1}$.


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

***


# Compactifying $M^{Der}$#
* automatic table of contents goes here
{:toc}

##Introduction##
Let $\mathbf{M}^{Der}$ be the derived Deligne-Mumford moduli stack of oriented elliptic curves.  Recall that the underlying Deligne-Mumford stack $\pi_0 \mathbf{M}^{Der}$ is $\mathbf{M}_{1,1}$ the classical Deligne-Mumford stack which is the fine moduli stack of elliptic curves.  We would like to construct a derived Deligne-Mumford stack $\overline{\mathbf{M}^{Der}}$ such that $\pi_0 \mathbf{M}^{Der}$ is the classical compactification $\overline{\mathbf{M}_{1,1}}$.

Recall that one can define the $E_\infty$-ring $tmf[\Delta^{-1}]$ as the global sections of $\OM_{\mathbf{M}^{Der}}$.  If we take global sections of $\mathbf{O}_{\overline{\mathbf{M}^{Der}}}$ then we get the $E_\infty$-ring $tmf$.

##The Tate Curve##

Let us focus on elliptic curves over $\mathbb{C}$.  The coarse moduli space of such elliptic curves is again $\mathbb{C}$ with the classifying map given by the $j$-invariant.  $\mathbb{C}$ is not compact, but we can compactify the moduli space by allowing curves with nodal singularities (generalized elliptic curves). 

For each $q \in \mathbb{C}, \; \lvert q \rvert \lt 1$, there is an elliptic curve over $\mathbb{C}$ defined by a Weierstrass equation
$$y^2 + xy = x^3 +a_4(q) x + a_6 (q) .$$
If $0 \lt \lvert q \rvert \lt 1$ the elliptic curve is isomorphic to $\mathbb{C}^*  /q^\mathbb{Z}$ as a Riemann surface with group structure induced from $\mathbb{C}^*$ (equivalently, this curve corresponds to $\mathbb{C}/ \Lambda_\tau$ where $e^{2\pi i \tau} = q$). As a function of $q$, $a_4$ and $a_6$ are analytic over the open disk and their power series at $q=0$ have integral coefficients hence the Weierstrass equation defines an elliptic curve $T$ over $\mathbb{Z}[ [q] ]$.  We really would like to think of $T$ as an elliptic curve over $\mathbb{Z} ( (q) ):= \mathbb{Z} [ [q] ][q^{-1}]$.

It should be noted that this construction (which goes back to Tate) can be extended to more general fields.

The Tate curve defines a cohomology theory $K_{Tate}$ (an elliptic spectrum).  As a cohomology theory $K_{Tate}$ is just $K$-theory tensored with $\mathbb{Z}( (q) )$.

##Annular Field Theories##
As shown in Pokman Cheung's thesis, the Tate curve has a connection to  supersymmetric field theories as defined by Stolz and Teichner.  The main result of is that a subspace of $2|1$ field theories (annular theories) is the $0th$-space of the spectrum $K_{Tate}$.

Let $SAB$ be the subcategory of $2|1$-EB whose morphisms are annuli. Note that $SAB$ does not contain tori.  $SAB$ in essence is completely determined by the supergroup $\mathbb{R}^{2|1}$.  Let $AFT_n$ be the space of natural transformations analogous to the definition of Stolz and Teichner.

**Theorem (Theorem 2.2.2 of Cheung).** For each $n \in \mathbb{Z}$, we have
$AFT_n \simeq (K_{Tate})_n .$

_Proof._
Let $A_{l,\tau}$ be the cylinder obtained by identifying non-horizontal sides of the parallelogram in the upper-half plane spanned by $l$ and $l\tau$ for $l \in \mathbb{R}_+$ and $\tau \in h$.

Let $E$ be a degree 0 field theory. The family of cylinders $\{A_{l,\tau} \}$ has the properties that $A_{l, \tau+1} = A_{l , \tau}$ and $A_{l, \tau} \circ A_{l, \tau'} = A_{l, \tau + \tau'}$.  For a fixed $l \in \mathbb{R}_+$, $\{E(A_{l,\tau}), \tau \in h \}$ is a commuting family of trace class (and hence compact) operators depending only on $\tau$ modulo $\mathbb{Z}$.  Therefore, by writing $q= e^{2 \pi i \tau}$ we can write $E (A_{l, \tau}) = q^{L} q^{\overline{L}}$, where $L, \overline{L}$ are unbounded operators with discrete spectrum. 

**Lemma.** The spectrum of $L-\overline{L} \subseteq \mathbb{Z}$.  Also, $\overline{L} = G^2$, where $G$ is an odd operator.


_Proof of Lemma._  The spectral argument follows from having an $S^1$ action.  To see the second claim note that for fixed $l$, $\mathbb{R}^{2|1}_+ /l \mathbb{Z}$ is a super Lie semi-group and the functor $E$ gives a representation $\mathbb{R}^{2|1}_+ \to \mathrm{End} (E(S^1_l))$ which is compatible with the super-semigroup law on $\mathbb{R}^{2|1}$ given by
$$(z_1 , \overline{z}_1 , \theta_1) , (z_2 , \overline{z}_2 , \theta_2) \mapsto (z_1 + z_2 , \overline{z}_1 +\overline{z}_2 + \theta_1 \theta_2 , \theta_1 + \theta_2) .$$
Now $\mathrm{Lie} (\mathbb{R}^{2|1}_+ ) = \langle \partial_z , \partial_{\overline{z}} , Q \rangle$, where $Q = \partial_\theta + \theta \partial_{\overline{z}}$.  Under $E$ the vector fields map to $L, \overline{L},$ and $G$ respectively.  Further, $[Q,Q] = 2Q^2 = 2 \partial_{\overline{z}},$ hence $G^2 = \overline{L}$.

We see that a degree 0 theory is determined by a pair of operators $(L, G)$.  By analyzing the spectral decomposition of the pair $(G, L-G^2)$ one can construct a weak equivalence of categories $AFT \to V$ (a homotopy equivalence of geometric realizations), where $V$ is a certain category of Clifford-modules.  Following work of Segal it is proved that $|V| \simeq (K_{Tate})_0$. The nonzero degrees follow a similar line of reasoning.


##$\overline{\mathbf{M}^{Der}}$##

We can extend the standard toric variety construction to derived schemes by replacing $\mathbb{C}$ by a fixed $E_\infty$-ring $R$.  That is given a fan $F= \{U_\alpha \}$ we can build a derived scheme $X_F$ where $X_F = \varinjlim \{U_\alpha\}$ and $U_\alpha = \mathrm{Spec} \; R [S_{\sigma_\alpha}]$ is an affine derived scheme.  We will define the (derived) Tate curve as the formal completion of the quotient of a toric variety.

Let $F_0 = \{ \{0\} , \mathbb{Z}_{\ge 0} \}$, so $X_{F_0} = \mathrm{Spec} R [\mathbb{Z}_{\ge 0}] = \mathrm{Spec} R[q]$.  Also, let $F= \langle \sigma_n \rangle_{n \in \mathbb{Z}}$, where
$$\sigma_n = \{ (a,b) \in \mathbb{Z} \times \mathbb{Z} \; | \; na \le b \le (n+1) a\}.$$
Note that by projection onto the first factor we have a map of fans $F \to F_0$ and consequently an induced map on varieties $f: X_F \to \mathrm{Spec} \; R[q]$.

Consider $f: X_F \to \mathrm{Spec} \; R[q]$, one can show that
1. $f^{-1} (q) \cong \mathbf{G}_m$ for $q \neq 0$;
1. $f^{-1} (0)$ is an infinite chain of rational curves, each intersecting the next in a node.

Consider the automorphism $\tau : \mathbb{Z} \times \mathbb{Z} \to \mathbb{Z} \times \mathbb{Z}$ defined by $\tau (a,b) = (a, b+a)$.  Note that $\tau (\sigma_n ) = \tau (\sigma_{n+1})$, so $\tau$ preserves the fan $F$ and consequently is an automorphism of the resulting toric variety $X_F$ which we also denote by $\tau$. Then
1. $\tau$ acts on $f^{-1} (q)$ by multiplication by $q$, for $q \neq 0$;
1. $\tau$ acts freely on $f^{-1}$.

Now define $\widehat{X}_F$ to be the formal completion of $X_F$ along $f^{-1} (0)$.  Similarly, define $R[ [q] ]$ as the formal completion of $R[q]$ along $q=0$. One can show that $\tau^{\mathbb{Z}}$ which is the multiplicative group generated by $\tau$ acts freely on $\widehat{X}_F$.


Define $\widehat{T}$ to be the formal (derived) scheme $\widehat{X}_F / \tau^\mathbb{Z}$.

**Theorem (Lurie/Grothendieck).**
The formal derived scheme $\widehat{T}$ is the completion of a unique derived scheme over $\mathrm{Spec} \; R[ [q] ]$.  That is, there exists a unique derived scheme $T \to \mathrm{Spec} \; R[ [q] ]$ such that $\widehat{T} = \mathrm{Spf} \; T$.

We call the derived scheme $T$ in the theorem above the _Tate curve_.
It is a fact that the restriction of $T$ to the punctured formal disk $\mathrm{Spec} \; R ( (q) )$ is an elliptic curve isomorphic to $\mathbf{G}_m / q^\mathbb{Z}$. 

We then see that an orientation of $T$ is equivalent to an orientation of $\mathbf{G}_m$ which is equivalent to working over the complex $K$-theory spectrum $K$. Therefore, the oriented Tate curve is equivalent to a map
$$T: \mathrm{Spec} \; K( (q) ) \to \mathbf{M}^{Der}.$$

Now note that the involution $\alpha : \mathbb{Z} \times \mathbb{Z} \to \mathbb{Z} \times \mathbb{Z}$ defined by $\alpha (a,b) = (a, -b)$ preserves the fan $F$ and $(\tau \circ \alpha)^2 = 1$.  We allow $\alpha$ to be complex conjugation on $K((q))$ thought of as a group action of $\{\pm 1\}$, so we have a map $\mathrm{Spec} \; K( (q) ) / \{\pm 1\} \to \mathbf{M}^{Der}$.

We can define a new derived Deligne-Mumford stack by forming an appropriate pushout square.

Finally, one can show that the underlying scheme $\pi_0 \overline{\mathbf{M}^{Der}}$ is $\overline{\mathbf{M}_{1,1}}$.

There are many subtleties associated with $\overline{\mathbf{M}^{Der}}$.  For instance, we would like to glue the universal curve $\E$ over $\mathbf{M}^{Der}$ with $T$ to obtain a universal elliptic curve $\overline{\E}$ over $\overline{\mathbf{M}^{Der}}$, however the result is only a _generalized_ elliptic curve; it is not a derived group scheme over $\overline{\mathbf{M}^{Der}}$ as it only has a group structure over the smooth locus of the map $\overline{\E} \to \overline{\mathbf{M}^{Der}}$.
Lurie asserts it is possible to construct the necessary geometric objects over $\overline{\mathbf{M}^{Der}}$ (I guess this will show up in DAG VII or VIII).  The global sections of the structure sheaf thus constructed is the spectrum $tmf$.