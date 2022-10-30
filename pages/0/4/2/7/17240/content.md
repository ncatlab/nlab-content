
#Contents#
* table of contents
{:toc}

## Idea

A cohomology [[spectral sequence]] is called _multiplicative_ if there is a [[graded algebra]] structure on each page such that the differentials acts as [[derivations]].

For example the [[Serre spectral sequence|Serre]]-[[Atiyah-Hirzebruch spectral sequence]] with [[coefficients]] in a [[ring spectrum]].
 
## Constructions

### From spectral products for Cartan-Eilenberg systems

The following give sufficient conditions for a [[Cartan-Eilenberg spectral sequence]] to be multiplicative. This is due to ([Douady 58](#Douady58)). The following is taken from ([Goette 15](#Goette15)).


Recall that a [[Cartan-Eilenberg system]] $(H,\eta,\partial)$ consists of modules $H(p,q)$ for each $p\le q$, morphisms $\eta\colon H(p',q')\to H(p,q)$ for all $p\le p'$, $q\le q'$, and boundary morphisms $\partial\colon H(p,q) \to H(q,r)$ for all $p\le q\le r$, such that

1. $\eta=\mathrm{id}\colon H(p,q)\to H(p,q)$,

2. $\eta=\eta\circ\eta\colon H(p'',q'')\to H(p',q')\to H(p,q)$,

3. $\eta$ and $\partial$ commute,

4. there are long exact sequences $\cdots\to H(q,r)\stackrel\eta\to H(p,r)\stackrel\eta\to H(p,q)\stackrel\partial\to H(q,r)\to\cdots$.

The conditions needed for convergence have been omitted. A typical example is $H(p,q)=\tilde h_\bullet(X_p/X_q)$, where $\cdots\supset X_{-1}\supset X_0\supset X_1\supset\cdots$ is a decreasing sequence of cofibrations and $\tilde h_\bullet$ is some generalised homology theory. The grading is suppressed in the following, but you can easily fill it in.


To set up a spectral sequence from $(H,\eta,\partial)$, one defines
$$Z^r_p=\mathrm{im}\bigl(H(p,p+r)\stackrel\eta\to H(p,p+1)\bigr)\;,$$
$$B^r_p=\mathrm{im}\bigl(H(p-r+1,p)\stackrel\partial\to H(p,p+1)\bigr)\;,$$
$$E^r_p=Z^r_p/B^r_p\;,$$
$$d^r_p\colon Z^r_p/B^r_p\twoheadrightarrow Z^r_p/Z^{r+1}_p\cong
B^{r+1}_{p+r}/B^r_{p+r}\hookrightarrow Z^r_{p+r}/B^r_{p+r}\;.$$
Details are in [Switzer 75, section 15](#Switzer75) In particular
$$\ker(d^r_p)=Z^{r+1}_p/B^r_p\qquad\text{and}\qquad
\mathrm{im}(d^r_p)=B^{r+1}_p/B^r_p\;.$$
For $a=\eta(a_0)\in H(p,p+1)$, $a_0\in H(p,p+r)$, one has
$$d^r_p([a])=[\partial a_0]\in E^r_p\qquad\text{with}\qquad\partial a_0\in H(p+r,p+r+1)\;.$$


+-- {: .num_defn #SpectralProduct}
###### Definition

Let $(H,\eta,\partial)$, $(H',\eta',\partial')$ und $(H'',\eta'',\partial'')$ be [[Cartan-Eilenberg systems]]. A _spectral product_ $\mu\colon(H',\partial')\times(H'',\partial'')\to(H,\partial)$ is a sequence of maps
$$\mu_r\colon H'(m,m+r)\otimes H''(n,n+r)\to H(m+n,m+n+r)$$
such that for all $m$, $n$, $r\ge 1$, the following two diagrams commute.

$$
  \array{
    H'(m, m+r) \otimes H''(n, n+r)
      &\stackrel{\mu_r}{\longrightarrow}&
    H(m+n, m+n+r)
    \\
    \downarrow^{\mathrlap{\eta' \oplus \eta''}} && \downarrow^{\mathrlap{\eta}}
    \\
    H'(m, m+1) \otimes H''(n, n+1)
     &\stackrel{\mu_1}{\longrightarrow}&
    H(m+n, m+n+1)
  }
$$

$$
  \array{
    H'(m, m+r) \otimes H''(n, n+r) &\stackrel{\mu_r}{\longrightarrow}& H(m+n,m+n+r)
    \\
    \downarrow^{\mathrlap{\partial' \oplus \eta'' \oplus \eta' \otimes \partial''}}
    && 
    \downarrow^{\mathrlap{\partial}}
    \\
    H'(m+r, m+r+1) \otimes H''(n,n+1) 
    \\
    \oplus     &\stackrel{\mu_1 + \mu_1}{\longrightarrow}& 
    H_{p+q-1}(m+n+r, m+n+r+1)
    \\
    H'(m,m+1) \otimes H''(n+r, n+r+1)
  }
  \,.
$$


=--

+-- {: .num_remark}
###### Remark

The first diagram in def. \ref{SpectralProduct} is weaker than in ([Douady 58](#Douady58)). The second can be read as a Leibniz rule.

=--

+-- {: .num_theorem}
###### Theorem

A spectral product $\mu\colon(H',\partial')\times(H'',\partial'')\to(H,\partial)$ induces products
$$\mu^r\colon E^{\prime r}_m\otimes E^{\prime\prime r}_n\to E^r_{m+n}\;,$$
such that

1. $\mu^1=\mu_1$

2. $d^r_{m+n}\circ\mu^r=\mu^r\circ(d^{\prime r}_m\otimes\mathrm{id})\pm\mu^r\circ(\mathrm{id}\circ d^{\prime\prime r}_n)$,

3. $\mu^{r+1}$ is induced by $\mu^r$.

=--

([Goette 15](#Goette15), following [Douady 58, theorem II](#Douady58)

+-- {: .proof}
###### Proof

Assume by induction that $\mu^r$ is induced by $\mu_1$. In particular,
$$Z^{\prime r}_m\otimes Z^{\prime\prime r}_n\stackrel{\mu_1}\to Z^r_{m+n}\;,$$
$$B^{\prime r}_m\otimes Z^{\prime\prime r}_n\stackrel{\mu_1}\to B^r_{m+n}\;,$$
$$Z^{\prime r}_m\otimes B^{\prime\prime r}_n\stackrel{\mu_1}\to B^r_{m+n}\;.$$
This is clear for $r=1$ if we put $\mu^1=\mu_1$ because $E^1_p=Z^1_p=H(p,p+1)$
and $B^1_p=0$.

Let $[a]\in Z^{\prime r}_m$, $[b]\in Z^{\prime\prime r}_n$ be represented by $a=\eta'(a_0)\in H'(m,m+1)$, $b=\eta''(b_0)\in H''(n,n+1)$ with $a_0\in H'(m,m+r)$, $b_0\in H''(n,n+r)$.
Using the first diagram and the construction of $d^r_{m+n}$, we conclude that
$$(d^r_{m+n}\circ\mu^r)([a]\otimes[b])=d^r_{m+n}[\mu_1(a\otimes b)]=d^r_{m+n}[\eta(\mu_r(a_0\otimes b_0))]=(\partial\circ\mu_r)(a_0\otimes b_0)\;.$$
From the second diagram, we get
$$(\partial\circ\mu_r)(a_0\otimes b_0)=\mu_1(\partial'a_0\otimes\eta''b_0)\pm\mu_1(\eta'a_0\otimes\partial''b_0)=\mu^r(d^{\prime r}_m[a]\otimes[b])\pm\mu^r([a]\otimes d^{\prime\prime r}_n[b])\;.$$
This proves the Leibniz rule (2).

From the Leibniz rule and the facts that $\ker(d^r_p)=Z^{r+1}_p/B^r_p$ and $\mathrm{im}(d^r_p)=B^{r+1}_p/B^r_p$, we conclude that $\mu^r$ induces a product on $E^{r+1}_p\cong\ker(d^r_p)/\mathrm{im}(d^r_p)$, which proves (3). Because $\mu^r$ is induced by $\mu_1$, so is $\mu^{r+1}$, and we can continue the induction. 

=--

## References


* {#Douady58} [[Adrien Douady]], _La suite spectrale d'Adams : structure multiplicative_ S&#233;minaire Henri Cartan, 11 no. 2 (1958-1959), Exp. No. 19, 13 p ([Numdam](http://www.numdam.org/item?id=SHC_1958-1959__11_2_A10_0))

* {#Switzer75} [[Robert Switzer]], _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975. 

* {#Goette15} [[Sebastian Goette]], [MO comment](http://mathoverflow.net/a/231235/381) 2015
