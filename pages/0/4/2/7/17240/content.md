
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[spectral sequence]] is called _multiplicative_ or a _spectral ring_ if there is a bi-[[graded algebra]] structure on each page such that the differentials act as graded [[derivations]] of total degree 1. 

For example the [[Serre spectral sequence|Serre]]-[[Atiyah-Hirzebruch spectral sequence]] with [[coefficients]] in a [[ring spectrum]].
 
## Constructions

### From spectral products on Cartan-Eilenberg systems

The following gives sufficient conditions for a [[Cartan-Eilenberg spectral sequence]] to be multiplicative. This is due to ([Douady 58](#Douady58)). The following is taken from ([Goette 15a](#Goette15)).



+-- {: .num_defn #SpectralProduct}
###### Definition

Let $(H,\eta,\partial)$, $(H',\eta',\partial')$ und $(H'',\eta'',\partial'')$ be [[Cartan-Eilenberg systems]]. A **spectral product** $\mu\colon(H',\partial')\times(H'',\partial'')\to(H,\partial)$ is a sequence of [[homomorphisms]]

$$
  \mu_r\colon H'(m,m+r)\otimes H''(n,n+r)\to H(m+n,m+n+r)
$$

such that for all $m$, $n$, $r\ge 1$, the following two [[commuting diagram|diagrams commute]]:

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

and

$$
  \array{
    H'(m, m+r) \otimes H''(n, n+r) &\stackrel{\mu_r}{\longrightarrow}& H(m+n,m+n+r)
    \\
    \downarrow^{\mathrlap{\partial' \otimes \eta'' \oplus \eta' \otimes \partial''}}
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

The first diagram in def. \ref{SpectralProduct} is weaker than in ([Douady 58](#Douady58)). The second may be read as a [[Leibniz rule]].

=--

Write $E$ for the [[Cartan-Eilenberg spectral sequence]] induced from the Cartan-Eilenberg system $H$.

+-- {: .num_prop #MultiplicativeStructureFromSpectralProduct}
###### Proposition

A spectral product $\mu\colon(H',\partial')\times(H'',\partial'')\to(H,\partial)$ as in def. \ref{SpectralProduct} induces products

$$
  \mu^r\colon E^{\prime r}_m\otimes E^{\prime\prime r}_n\to E^r_{m+n}\;,
$$

such that

1. $\mu^1=\mu_1$

2. $d^r_{m+n}\circ\mu^r=\mu^r\circ(d^{\prime r}_m\otimes\mathrm{id})\pm\mu^r\circ(\mathrm{id}\circ d^{\prime\prime r}_n)$,

3. $\mu^{r+1}$ is induced by $\mu^r$.

=--

([Goette 15a](#Goette15), following [Douady 58, theorem II](#Douady58)).

+-- {: .proof}
###### Proof

Assume by [[induction]] that $\mu^r$ is induced by $\mu_1$. In particular,
$$Z^{\prime r}_m\otimes Z^{\prime\prime r}_n\stackrel{\mu_1}\to Z^r_{m+n}\;,$$
$$B^{\prime r}_m\otimes Z^{\prime\prime r}_n\stackrel{\mu_1}\to B^r_{m+n}\;,$$
$$Z^{\prime r}_m\otimes B^{\prime\prime r}_n\stackrel{\mu_1}\to B^r_{m+n}\;.$$
This is clear for $r=1$ if we put $\mu^1=\mu_1$ because $E^1_p=Z^1_p=H(p,p+1)$
and $B^1_p=0$.

Let $[a]\in Z^{\prime r}_m$, $[b]\in Z^{\prime\prime r}_n$ be represented by $a=\eta'(a_0)\in H'(m,m+1)$, $b=\eta''(b_0)\in H''(n,n+1)$ with $a_0\in H'(m,m+r)$, $b_0\in H''(n,n+r)$.
Using the first diagram and the construction of $d^r_{m+n}$, we conclude that

$$
  (d^r_{m+n}\circ\mu^r)([a]\otimes[b])=d^r_{m+n}[\mu_1(a\otimes b)]=d^r_{m+n}[\eta(\mu_r(a_0\otimes b_0))]=(\partial\circ\mu_r)(a_0\otimes b_0)
 \;.
$$

From the second diagram, we get

$$
  (\partial\circ\mu_r)(a_0\otimes b_0)=\mu_1(\partial'a_0\otimes\eta''b_0)\pm\mu_1(\eta'a_0\otimes\partial''b_0)=\mu^r(d^{\prime r}_m[a]\otimes[b])\pm\mu^r([a]\otimes d^{\prime\prime r}_n[b])
\;.
$$

This proves the Leibniz rule (2).

From the Leibniz rule and the facts that $\ker(d^r_p)=Z^{r+1}_p/B^r_p$ and $\mathrm{im}(d^r_p)=B^{r+1}_p/B^r_p$, we conclude that $\mu^r$ induces a product on $E^{r+1}_p\cong\ker(d^r_p)/\mathrm{im}(d^r_p)$, which proves (3). Because $\mu^r$ is induced by $\mu_1$, so is $\mu^{r+1}$, and we can continue the induction. 

=--

## Examples

### AHSS for multiplicative cohomology
 {#AHSSForMultiplicativeCohomology}

We discuss that the multiplicative structure on the cohomology [[Serre spectral sequence|Serre]]-[[Atiyah-Hirzebruch spectral sequence]] for [[multiplicative cohomology theory|multiplicative]] [[generalized cohomology]]. This is taken from ([Goette 15b](#Goette15)).


+-- {: .num_defn #CESystemForMultiplicativeGeneralizedCohomology}
###### Definition

For $\pi\colon X\to B$ a [[Serre fibration]] over a [[CW-complex]] $B$.  And for $(\tilde h^\bullet,\delta,\wedge)$ a [[multiplicative cohomology theory|multiplicative]] [[reduced cohomology|reduced]]  [[generalized (Eilenberg-Steenrod) cohomology]] theory, define a [[Cartan-Eilenberg system]] $(H,\eta,\partial)$ by

$$
  H(p,q)=\tilde h^\bullet(X^{q-1}/X^{p-1})
$$

(where $X^k=\pi^{-1}(B^k)$) for $p\le q$ with the obvious maps $\eta\colon H(p',q')\to H(p,q)$ for $p\le p'$, $q\le q'$. 

The [[Cartan-Eilenberg spectral sequence]] of this Cartan-Eilenberg system is the [[Serre spectral sequence|Serre]]-[[Atiyah-Hirzebruch spectral sequence]].

=--

+-- {: .num_defn #SpectralProductForAHSS}
###### Definition


The spectral product $\mu\colon(H,\eta,\partial)\times(H,\eta,\partial)\to(H,\eta,\partial)$, 
def. \ref{SpectralProduct}, on the Cartan-Eilenberg system of def. \ref{CESystemForMultiplicativeGeneralizedCohomology}
is that given by the following morphism

$$
  \begin{aligned}
  F_{m,n,r}
    & \colon
    (X\wedge X)^{m+n+r-1}/(X\wedge X)^{m+n-1}
    \cong
    \bigcup_{a+b=m+n+r-1}(X^a\wedge X^b) / \bigcup_{c+d=m+n-1}(X^c\wedge X^d)
    \\
    & 
    \twoheadrightarrow
    \bigcup_{a+b=m+n+r-1}
     (X^a\wedge X^b)/(\bigcup_{a=0}^m(X^{a-1}\wedge X^{m+n+r-a})
    \cup\bigcup_{b=0}^n(X^{m+n+r-b}\wedge X^{b-1})
    \\
    & 
    \cong \bigcup_{a=m+1}^{m+r}(X^{a-1}\wedge X^{m+n+r-a})
    /
    \bigl(X^{m+r-1}\wedge X^{n-1}\cup X^{m-1}\wedge X^{n+r-1}\bigr)
    \\
    & \hookrightarrow  
    X^{m+r-1}\wedge X^{n+r-1}/(X^{m+r-1}\wedge X^{n-1}\cup X^{m-1}\wedge X^{n+r-1})
    \\
    & \cong (X^{m+r-1}/X^{m-1})\wedge(X^{n+r-1}/X^{n-1})
  \;.
  \end{aligned}
$$

Together with the [[diagonal]] map $\Delta$, for $r\ge 1$, we define

$$
  \begin{aligned}
    \mu_r 
     & \colon 
    H(m,m+r)\otimes H(n,n+r)
    \\
    & \cong\tilde h(X^{m+r-1}/X^{m-1})\otimes\tilde h(X^{n+r-1}/X^{n-1})
    \\
    &\stackrel\wedge\longrightarrow\tilde h\bigl((X^{m+r-1}/X^{m-1})\wedge(X^{n+r-1}/X^{n-1})\bigr)
    \\
    &\stackrel{F_{m,n,r}^*}\longrightarrow\tilde h\bigl((X\wedge X)^{m+n+r-1}/(X\wedge X)^{m+n-1}\bigr)
    \\
    &\stackrel{\Delta_X^*}\longrightarrow\tilde h(X^{m+n+r-1}/X^{m+n-1})=H(m+n,m+n+r)\;.
\end{aligned}

=--

+-- {: .num_prop}
###### Proposition

With def. \ref{SpectralProductForAHSS}, then 
for all $m$, $n$, $r\ge 1$, the following [[commuting diagram|diagram commutes]]

$$
  \array{
    H(m,m+1) \otimes H(n,n+1) &\stackrel{\mu_1}{\longrightarrow}& H(m+n, m+n+1)
    \\
    \uparrow^{\mathrlap{\eta \oplus \eta}}
    &&
    \uparrow^{\mathrlap{\eta}}
    \\
    H(m,m+r) \otimes H(n,n+r) &\stackrel{\mu_r}{\longrightarrow}& H(m+n,m+n+r)
    \\
    \downarrow^{\mathrlap{\partial \otimes \eta \oplus \eta \otimes \partial}}
    && 
    \downarrow^{\mathrlap{\partial}}
    \\
    H(m+r, m+r+1) \otimes H(n,n+1)
    \\
    \oplus &\stackrel{\mu_1 \pm \mu_1}{\longrightarrow}& 
       H(m+n+r, m+n+r+1)
    \\
    H(m,m+1) \otimes H(n+r, n+r+1)
  }
  \,.
$$

Hence by prop. \ref{MultiplicativeStructureFromSpectralProduct} 
the spectral product of def. \ref{SpectralProductForAHSS}
defines a mutliplicative structure on the Serre-WhiteheadAtiyah-Hirzebruch spectral sequence for multiplicative generalizted cohomology.

=--


+-- {: .proof}
###### Proof


The upper square commutes because the maps $F_{m,n,r}$ are [[natural transformations]]. 
For the lower square, we consider the boundary morphism $\delta$ of the triple

$$
  \begin{aligned}
    (&
     X^{m+r}\wedge X^{n+r-1}\cup X^{m+r-1}\wedge X^{n+r},
    \\
    &
    X^{m+r}\wedge X^{n-1}\cup X^{m+r-1}\wedge X^{n+r-1}\cup X^{m-1}\wedge X^{n+r},
    \\
    & X^{m+r}\wedge X^{n-1}\cup X^{m-1}\wedge X^{n+r})
  \end{aligned}
  \;.
$$

The following diagram commutes:

$$
  \array{
    \tilde h^{-p}(X^{m+r-1}/ X^{m-1})
    \otimes
    \tilde h^{-q}(X^{n+r-1}/X^{n-1})
    &\stackrel{\wedge}{\longrightarrow}&
    \tilde h^{-p-q}((X^{m+r-1}/X^{m-1}) \wedge (X^{n+r-1}/X^{n-1})
    \\
    \downarrow^{\mathrlap{\delta \wedge id \oplus id \wedge \delta}}
    &&
    \downarrow^{\mathrlap{\delta}}
    \\
    \tilde h(1-p)(X^{m+r}/X^{m+r-1}) \otimes \tilde h^{-q}(X^{n+r-1}/X^{n-1})
    &&
    \tilde h^{1-p-q}((X^{m+r}/X^{m+r-1}) \wedge (X^{n+r-1}/X^{n-1}))
    \\
    \oplus
    &\stackrel{\wedge \oplus \wedge}{\longrightarrow}&
    \\
    \tilde h^{-p}(X^{m+r-1}/X^{m-1}) \otimes \tilde h^{1-q}(X^{n+r}/X^{n+r-1})
    &&
    \tilde h^{1-p-q}( (X^{m+r-1}/ X^{m-1}) \wedge (X^{n+r}/ X^{n+r-1}) )
  }
  \,.
$$


By extend this diagram to the right using the maps $F_{m,n,r}$ once 
concludes that the lower square above also commutes. 

=--

## References


* {#Douady58} [[Adrien Douady]], _La suite spectrale d'Adams : structure multiplicative_ S&#233;minaire Henri Cartan, 11 no. 2 (1958-1959), Exp. No. 19, 13 p ([Numdam](http://www.numdam.org/item?id=SHC_1958-1959__11_2_A10_0))

* {#Gray80} Brayton Gray, _Products in the Atiyah-Hirzebruch spectral sequence and the calculation of $M SO_\ast$, Trans. Amer. Math. Soc. 260 (1980), 475-483 ([web](http://www.ams.org/journals/tran/1980-260-02/S0002-9947-1980-0574793-9/))

* {#Kochmann96} [[Stanley Kochmann]], prop. 4.2.9 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#McCleary00} [[John McCleary]], section 2.3 in _A User's Guide to Spectral Sequences_, Cambridge University Press (2000)

* {#Dugger03a} [[Daniel Dugger]], _Multiplicative structures on homotopy spectral sequences I_ ([arXiv:math/0305173](http://de.arxiv.org/abs/math/0305173))

* {#Dugger03b} [[Daniel Dugger]], _Multiplicative structures on homotopy spectral sequences II_ ([arXiv:math/0305187](http://de.arxiv.org/abs/math/0305187))

* {#Goette15} [[Sebastian Goette]], [MO comment a](http://mathoverflow.net/a/231235/381), [MO comment b](http://mathoverflow.net/a/231236/381) Feb 15, 2015

[[!redirects multiplicative spectral sequences]]
