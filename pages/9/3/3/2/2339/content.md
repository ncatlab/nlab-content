<div class="rightHandSide toc">
[[!include cohomology - contents]]

***

[[!include higher geometry - contents]]
</div>



+-- {: .standout}

This is a sub-entry of

* [[A Survey of Elliptic Cohomology]]

see there for background and context.

This entry disscusses basics of [[formal group law]]s arising from [[periodic cohomology theory|periodic]] [[multiplicative cohomology theory|multiplicative]] [[cohomology theory|cohomology theories]]

=--

Previous:

* [[A Survey of Elliptic Cohomology - cohomology theories]]

Next:

* [[A Survey of Elliptic Cohomology - E-infinity rings and derived schemes]]


## rough notes from a talk##

>the following are rough unpolished notes taken more or less verbatim from some seminar talk -- needs attention


**Formal groups and elliptic cohomology.**

In all of the following, all [[cohomology theory|cohomology theories]] are [[multiplicative cohomology theory|multiplicative]] and all [[formal group law]]s are one-dimensional (and commutative).

**[[A Survey of Elliptic Cohomology - cohomology theories|Last time]].**  Orienting a [[periodic cohomology theory|periodic]] [[even cohomology theory]] gives a [[formal group law]]
over the [[cohomology ring]] $A^0(\bullet)$.  (Note: $A^0$ and not $A^*$ because of the periodicity property.)

**Today.**  A generalization of the above statement.
Orienting a [[weakly periodic cohomology theory|weakly periodic]] even cohomology theory gives a formal group over $A^0(\bullet)$.
In particular, [elliptic cohomology]] theories give [[elliptic curve]]s over $A^0(\bullet)$.

**Formal group laws and Landweber's criterion.**

[[formal group law|Formal group law]]s over $R$ are classified by [[morphism]]s from the [[Lazard ring]] to $R$.
We can define $A_f^n(X)=MP^n(X)\otimes_{MP(\bullet)}R$.
Here $MP$ denotes [[complex cobordism cohomology theory|complex cobordism]], in particular $MP(\bullet)$ is isomorphic to [[Lazard ring|Lazard's ring]].

**Definition.**  A sequence $v_0,\ldots,v_n$ of elements of $R$ is regular
if [[endomorphism]]s of $R/(v_0,\ldots,v_{k-1})$ given by multiplication by $v_k$
are injective for all $0\le k\le n$.

**Landweber's Criterion.**  Let $f(x,y)$ be a formal group law and $p$ a prime,
$v_i$ the coefficient of $x^{p^i}$ in $[p]_f(x)=x+_f\cdots+_fx$.
If $v_0,\ldots,v_i$ form a regular sequence for all $p$ and $i$ then $f(x,y)$ gives a 
[[cohomology theory]] via the formula with [[tensor product]] above.

**Example.**  $g_a(x,y)=x+y$, $[p]_a(x)=px$, $v_0=p$, $v_i=0$ for all $i\ge1$;
regularity condtions imply that
the zero map $R/(p)\to R/(p)$ must be injective.  The last statement implies that
$R$ contains the rational numbers as a subring.

Note that $HP^*(X,R)=\prod_k H^{n+2k}(X,R)$ is a [[cohomology theory]] over any [[ring]] $R$.

**Example.**  $g_m(x,y)=xy$, $[p]_m(x)=(x+1)^p-1$, $v_0=p$, $v_1=1$, $v_i=0$ for all $i \gt 1$.
The regularity conditions are trivial.
Hence we know that $K^*(X)=MP^*(X)\otimes_{MP(\bullet)} \mathbb{Z}$ is a cohomology theory.

**Groups from formal group laws.**  Given a commutative topological
$R$-algebra $A$ and a formal group law$f(x,y)$ if $f(a,b)$ converges for all $a,b\in A$ and the formula giving an inverse to $a$ converges for all $a\in A$,
we get an abelian group $(A,+_f)$, where $a+_f b=f(a,b)$.

**Example.**  For any $A$ the pair $(N(A),+_f)$ is an abelian group, where
$N(A)$ denotes the set of nilpotent elements of $A$.

**Example.**  Let $A$ be an complex oriented cohomology theory.
Then computing [[Chern class]]es of [[line bundle]]s is the same as evaluating the
formal group law of $A$ on some algebra.
Recall that [[line bundle]]s on $X$ are [[classifying space|classified]] by maps from $X$ to $\mathbb{C}P^\infty$,
pairs of line bundles are classified by maps to $\mathbb{C}P^\infty \times \mathbb{C}P^\infty$,
and tensor product of line bundles gives a map $\mathbb{C}P^\infty \times \mathbb{C}P^\infty \to \mathbb{C}P^\infty$.
Now apply cohomology functor to the sequence $X\to \mathbb{C}P^\infty \times \mathbb{C}P^\infty \to \mathbb{C}P^\infty$.
We have a degree 0 element $t$ in the cohomology of $\mathbb{C}P^\infty$.
Its image in the cohomology of $\mathbb{C}P^\infty \times \mathbb{C}P^\infty$ is a formal group law.
The image of this formal group law in the cohomology of $X$ makes sense
if $X$ is a finite cell complex so that $A^0(X)$ is a nilpotent algebra.

When do two formal group laws yield isomorphic groups?

**Definiton.**  A homomorphism of formal group laws $f$ and $g$ over $A$
is a formal power series $\phi\in A[x]$ such that $\phi(f(x,y))=g(\phi(x),\phi(y))$.
(The constant term of~$\phi$ is zero.)
Hence formal group laws form a category.

**Example.**  If $R$ contains rational numbers as a subring,
then we have two canonical homomorphisms.  The first one is $\exp\colon g_a\to g_m$, where
$\exp(x)=\sum_{k \gt 0}x^k/k!$.  Its inverse is $\log\colon g_m\to g_a$, where
$\log(x)=\sum_{k \gt 0}(-1)^{k+1}x^k/k$.
This shows up in cohomology as Chern character.
(Isomorphism from $K^n(X)\otimes_{\mathbb{Z}} \mathbb{Q}$ to $\prod_kH^{n+2k}(X,\mathbb{Q})$.

**Formal groups.**  A [[formal group]] is a group in the [[category]] of [[formal scheme]]s.

Intuitive explanation of the notion of [[formal scheme]]:
Informally, $\hat X$ is like the $\infty$-jet bundle of $Y$ inside of $X$.

**Definition.**  The locally [[ringed space]] $\hat X$ is defined as the [[topological space]] $Y$
with structure sheaf $\lim O_X/^n$, where $V(U)$ has underlying space $Y$.
(Where $Y$ is a closed subscheme of $X$.)

**Examples.**  $X=\hat X$ when $Y=X$.  $\mathrm{Spec} k[t]=X$, $Y=V(t)$, $\hat X=k[t,t^{-1}]$.

**Definition.** $\mathrm{Spf} R$ is the locally [[ringed space]] with the underlying [[topological space]]
$\mathrm{Spec} R/I$ and [[sheaf]] $O_{\mathrm{Spf} R}(\mathrm{Spf} R)=\lim R/I^n$.


### formal group laws from elliptic curve ###

recall from the above that a given a [[formal group law]] $F(x,y) \in R[[x,y]]$ we get te structure of a [[formal group]] on the [[formal spectrum]] $Spf$ by taking the product to be given by

$$
  \array{
    Spf R[[x,y]] \simeq
    Spf[[x]] \times Spf R[[y]]
    &\to& Spf R[[z]]
    \\
    f(x,y)&\leftarrow |& z 
  }
$$

Isomorphic [[formal group law]]s give [isomorphism|isomorphic]] (of [[formal group]]s) if $G$ a [[formal group]] has $G \simeq Spf R[[z]]$; we must choose such an iso to get a [[formal group law]].





Now we get [[formal group]]s from [[elliptic curve]]s over $R$

**definition** An **elliptic curve** over a commutative [[ring]] $R$ is a [[group object]] in the [[category]] of [[scheme]]s over $R$ that is a relative 1-dimensional, , [[smooth scheme|smooth curve]], [[proper scheme|proper]] curve over $R$. 

This implies that it has [[genus]] 1. (by a direct argument of the Chern class of the tangent bundle.)

Given an [[elliptic curve]] over $R$, $E \to Spec R$, we get a [[formal group]] $\hat E$ by completing $D$ along its identity [[section]] $\sigma_0$

$$
  E \to Spec(R) \stackrel{\sigma_0}{\to} E
$$

(the one dual to the map that maps everything to $0 \in R$), we get a [[ringed space]] $(\hat E, \hat O_{E,0})$











*example** if $R$ is a [[field]] $k$, then the [[structure sheaf]] $\hat O_{E,0} \simeq k[[z]]$

then 

$$
  \hat O_{E \times E, (0,0)} \simeq
  \hat O_{E,0}
  \hat \otimes_k
  \hat O_{E,0}
  \simeq 
  k[[x,y]]
$$



**example** **Jacobi quartics**

$$
  y^2 = 1- 2 \delta x^2 + \epsilon x^4
$$

defines 4E$ over $R = \mathbb{Z}[Y_Z,\epsilon, \delta]$.

The corresponding [[formal group law]] is **Euler's formal group law**

$$
  f(x,y) = \frac{x\sqrt{1- 2 \delta y^2 + \epsilon y^4}
   + y \sqrt{1- 2 \delta x^2 + \epsilon x^4}}
  {1- \epsilon x^2 y^2}
$$

if $\Delta := \epsilon(\delta^2 - \epsilon)^2 \neq 0$ then this is a non-trivial elliptic curve.

If $\Delta = 0$ then $f(x,y) \simeq G_m, G_a$ (additive or multiplicative formal group law corresponding to [[integral cohomology]] and [[K-theory]], respectively).

## weakly periodic cohomology theories and formal groups ##

**Definition** A [[cohomology theory]] $A$ is **weakly periodic** if the natural map

$$
  A^2({*}) \otimes A^0({*}) A^n({*}) \stackrel{\simeq}{\to}
  A^{n+2}({*})
$$

is an [[isomorphism]] for all $n \in \mathbb{Z}$.

To get a [[formal group]] from a [[weakly periodic cohomology theory|weakly periodic]], [[even cohomology theory|even]] [[multiplicative cohomology theory|multiplicative]] [[cohomology theory]] $A^\bullet$, we look at the induced map on $A^\bullet$ from 

$$
  {*} \to \mathbb{C}P^\infty
$$

and 

$$
  ker(i_0^* : A^0(\mathbb{C}P^\infty) \to A^0({*}))
$$ 
is the [[ideal]] 

that we complete along to define the [[formal scheme]] $Spf A^0(\mathbb{C}P^\infty)$.

Notice that the map from the point is unique only up to [[homotopy]], so accordingly there are lots of chocies here, which however all lead to the same result.

The fact that $A$ is weakly periodic allow to reconstruction the cohomoloogy theory essentially from this formal scheme.

To get a [[formal group law]]: if the [[Lie algebra]] $Lie(Spf A^0(\mathbb{C}P^\infty))$ of the [[formal group]] 

$$
  Lie(Spf A^0(\mathbb{C}P^\infty))
  \simeq
  ker(i_0^*)/ker(i:0^*)^2
$$

is a free $A^0({*})$-module, we can pick a generator $t$ and this gives an [[isomorphism]] 

$$
  Spf(A^0(\mathbb{C}P^\infty)) \simeq Spf(A^0({*})[[t]])
$$

if $A^0(\mathbb{C}P^\infty) A^0({{*})[[t]]$ then $i_0^*$ "forgets the $t$coordinate".

**Definition** An **elliptic cohomology theory** over $R$ is

* a commutative [[ring]] $R$

* an [[elliptic curve]] $E/R$

* a [[weakly periodic cohomology theory|weakly periodic]], [[multiplicative cohomology theory|multiplicative]], [[even cohomology theory|even]] [[cohomology theory]] $A^\bullet$

* [[isomorphism]]s $A^0({*}) \simeq R$ and $\hat E \simeq Spf(A^0(\mathbb{C}P^\infty))$.


So we have on one side 

$$
  \array{
    \hat E &\stackrel{\simeq}{\to}& Spf A^0(\mathbb{C}P^\infty)
    \\
    \downarrow && \downarrow
    \\
    Spec R &\stackrel{\simeq}{\to}&
    Spec A^0({*})
    \\
    \downarrow^{\sigma_0} && \downarrow    
    \hat E &\stackrel{\simeq}{\to}& Spf A^0(\mathbb{C}P^\infty)
  }
$$

We can check that the [[Landweber exactness criterion]] is satisfied for the [[formal group law]] of the [[Jacobi quartic]], i.e. for [[Euler's formal group law]] over $\mathbb{Z}[\Delta^{-1}, \epsilon, \delta, 1/2]$, so this provides an example of an [[elliptic cohomology]] theory.

$$
  A^n_G(X) = M P (X) \otimes_{M P({*})} \mathbb{Z}[\Delta^{-1}, \epsilon, \delta, 1/2]
$$

