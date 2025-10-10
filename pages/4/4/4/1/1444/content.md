
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

\tableofcontents

## Idea

The **bicrossed product**, also known as the **Zappa–Szép product**, generalizes the [[semidirect product]] of groups.

This construction is essential to the [[quantum double]] construction of Drinfel'd. The bicrossed product applies more generally to [[monoids]] and other algebraic entities, see ([Brin 04](#Brin04)).

## Definition 

Given a pair of matched groups $H$ and $K$, the bicrossed product of groups $H\times K$ on the set $H \times K$
is given by
\[ (h,k)\cdot(h',k') = (h\alpha(k,h'),\beta(k,h')k')\]
with unit $(1,1)$ and $h,h'\in H$, $k,k'\in K$, where $\alpha: K\times H\rightarrow H$, $\beta: K\times H\rightarrow K$ are left and right actions, respectively.

A pair of groups $(H,K)$ is said to be matched if there exists a left action $\alpha$ of $K$ on the set $H$ and a right action $\beta$ of the group $H$ on the set $K$ such that for all $h,h'\in H$, $k,k'\in K$, the following hold:

* $\beta(k k',h) = \beta(k,\alpha(k',h))\beta(k',h)$,
* $\alpha(k,h h') = \alpha(k,h)\alpha(\beta(k,h),h')$,
* $\alpha(k,1) = 1$,
* $\beta(1,h) = 1$.


## Properties

The bicrossed products of two groups $H$ and $K$ precisely correspond to the [[distributive laws]] between the [[monads]] $T=H \times -$ and $S=K\times -$. 

## References

* [[Christian Kassel]], *Quantum groups*, Graduate Texts in Mathematics __155__, Springer (1995) &lbrack;[doi:10.1007/978-1-4612-0783-2](https://link.springer.com/book/10.1007/978-1-4612-0783-2), [webpage](http://www-irma.u-strasbg.fr/~kassel/QGbk.html), [errata pdf](http://www-irma.u-strasbg.fr/~kassel/QGerrata030399.pdf)&rbrack;

* {#Brin04} Matthew G. Brin, *On the Zappa-Szep Product* &lbrack;[arXiv:math/0406044](https://arxiv.org/abs/math/0406044)&rbrack;

[[!redirects bicrossed products]]
[[!redirects matched group]]
[[!redirects matched groups]]
[[!redirects Zappa–Szép product]]
[[!redirects Zappa–Szép products]]
[[!redirects Zappa-Szép product]]
[[!redirects Zappa-Szép products]]