

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

Consider 

* a [[topological group]] $G$, 

* a [[locally compact Hausdorff space]] $X$,

* a [[group action]] of $G$ on $X$ (making $X$ a [[topological G-space]]):

  $$
    \array{
      G \times X
      &\overset{\rho}{\longrightarrow}&
      X
      \\
      (x,g) &\mapsto& g \cdot x
      \mathrlap{\,.}
    }
  $$


The action $\rho \colon (g,x) \mapsto g \cdot x$ is called *proper* ([Palais 61, Def. 1.2.2](#Palais61)) if one of the following equivalent conditions hold (their equivalence relies on $X$ being [[locally compact Hausdorff space|locally compact and Hausdorff]], [Palais 61, Thm. 1.2.9](#Palais61), [Karppinen 16, Rem. 5.2.4](#Karppinen16)):

1. **(Bourbaki properness)** The shear map is a [[proper continuous function]]:

   $$
     \array{
       G \times X &\overset{proper}{\longrightarrow}& X \times X
       \\
       (g,x) &\mapsto& (g\cdot x, x)
     }
   $$

   ([Bourbaki 60, Ch. III, Sec. 4.4](#Bourbaki60), review in [Lee 00, p. 266](#Lee00))

1. **(Borel properness)** For every [[compact subspace]] $K \subset X$
 the subset

   $$
     (K \vert K)
     \;\coloneqq\;
     \big\{
       g \in G
       \,\vert\,
       g \cdot K \,\cap\, K \neq \varnothing
     \big\}
     \;\subset\;
     G
   $$

   is [[compact subspace|compact]].

   ([Palais 61, Thm 1.2.9 (5)](#Palais61), attributed there to [[Armand Borel|Borel]])


1. {#PalaisProperness} **(Palais properness)** Every point $x \in X$ has a [[neighbourhood]] $U_x$ such that every point $y \in U_x$ has a neighbourhood $V_y$ such that

   $$
     (U_x \vert U_y)
     \;\coloneqq\;
     \big\{
       g \in G
       \,\vert\,
       g \cdot V_x \,\cap\, U_y \neq \varnothing
     \big\}
     \;\subset\;
     G
   $$

   has [[compact subspace|compact]] [[topological closure|closure]].

   ([Palais 61, Def. 1.2.2](#Palais61))


## Examples

### Lie group actions on smooth manifolds

> How is the following not a trivial consequence of the fact that compact groups have proper action? Needs clarification.

\begin{prop}\label{SmoothActionOfCompactLieGroupOnSmoothManifoldIsProper}

Let $X$ be a [[smooth manifold]] and let $G$ be a [[compact Lie group]].
Then every [[smooth function|smooth]] [[action]] of $G$ on $X$ is [[proper action|proper]].

\end{prop}

(e.g. [Lee 12, Cor. 7.2](#Lee12))

For more see at _[[equivariant differential topology]]_.

## Related concepts

* [[properly discontinuous action]]

* [[free action]], [[semi-free action]], [[transitive action]], [[regular action]]

* [[equivariant differential topology]]

## References

The original definition are due to:

* {#Palais61} [[Richard Palais]], _On the Existence of Slices for Actions of Non-Compact Lie Groups_, Annals of Mathematics
Second Series, Vol. 73, No. 2 (Mar., 1961), pp. 295-323 ([jstor:1970335](https://www.jstor.org/stable/1970335), [doi:10.2307/1970335](https://doi.org/10.2307/1970335), [pdf](http://vmm.math.uci.edu/ExistenceOfSlices.pdf))

  > (in the context of proving the [[slice theorem]])

* {#Bourbaki60} [[Nicolas Bourbaki]], *Éléments de mathématique*, *Topologie générale*, Chap. 3:  *Groupes topologiques*, 1960


Textbook accounts:

* {#Lee00} [[John M. Lee]], Section 12.3 of: _Introduction to topological manifolds_. Graduate Texts in Mathematics 202 (2000), Springer.  ISBN: 0-387-98759-2, 0-387-95026-5.
Second edition: Springer, 2011.  ISBN: 978-1-4419-7939-1 ([doi:10.1007/978-1-4419-7940-7](https://doi.org/10.1007/978-1-4419-7940-7), errata [pdf](https://sites.math.washington.edu/~lee/Books/ITM/errata.pdf))


* {#Lee12} [[John Lee]], around p. 147 of: _Introduction to Smooth Manifolds_, Springer 2012 ([doi:10.1007/978-1-4419-9982-5](https://doi.org/10.1007/978-1-4419-9982-5), [pdf](https://lost-contact.mit.edu/afs/adrake.org/usr/rkh/Books/books/Introduction%20to%20Smooth%20Manifolds%20-%20J.%20Lee.pdf))


* {#Kankaanrinta07} [[Marja Kankaanrinta]], Def. 2.1 in _Equivariant collaring, tubular neighbourhood and gluing theorems for proper Lie group actions_,     Algebr. Geom. Topol. Volume 7, Number 1 (2007), 1-27 ([euclid:agt/1513796653](https://projecteuclid.org/euclid.agt/1513796653))

See also

* [[John Lee|J. Lee]], [MO comment](https://math.stackexchange.com/a/989168/58526), Oct 2014

Further discussion

* {#Karppinen16} [[Sini Karppinen]], _The existence of slices in $G$-spaces, when $G$ is a Lie group_, Helsinki 2016 ([hdl:10138/190707](http://hdl.handle.net/10138/190707))

  > (in the context of the [[slice theorem]])

* {#Antonyan02} Sergey Antonyan, *Universal proper G-spaces*, Topology and its Applications Volume 117, Issue 1, 15 January 2002, Pages 23-43 (<a href="https://doi.org/10.1016/S0166-8641(00)00115-2">doi:10.1016/S0166-8641(00)00115-2</a>)


[[!redirects proper actions]]

[[!redirects proper group action]]
[[!redirects proper group actions]]

