#Definition#

A **coproduct** of two [[object|objects]] $a,b$ in a [[category]] $C$ is an object $a+b$ (also written $a\amalg b$, especially when it is [[disjoint coproduct|disjoint]], or $a \sqcup b$ if your fonts don\'t include '$\amalg$') equipped with [[morphism|morphisms]] $i:a\to a+b$ and $j:b\to a+b$ such that for any object $c$ with morphisms $f:a\to c$ and $g:b\to c$, there is a unique morphism $p:a+b\to c$ such that $p \circ i=f$ and $p \circ j=g$.

This map $p$ is called the __[[copairing]]__ of $f$ and $g$ and is often denoted $[f,g]$ or $\{f,g\}$ or (when possible) given vertically:
$$\left\{{f \atop g}\right\}$$


#Examples#

*  In [[Set]], the coproduct of a family of sets $(C_i)_{i\in I}$ is the [[disjoint union]] $\coprod_{i\in I} C_i$ of sets.
*  In [[Top]], the coproduct of a family of spaces $(C_i)_{i\in I}$ is the space whose set of points is $\coprod_{i\in I} C_i$ and whose open subspaces are of the form $\coprod_{i\in I} U_i$ (the internal [[disjoint union]]) where each $U_i$ is an open subpace of $C_i$.  This is typical of [[topological concrete categories]].
*  In [[Grp]], the coproduct is the [[free product]], whose underlying set is *not* a disjoint union.  This is typical of [[algebraic category|algebraic categories]].
*  In [[Cat]], the coproduct of a family of categories $(C_i)_{i\in I}$ is the category with
   $$Obj(\coprod_{i\in I} C_i) = \coprod_{i\in I} Obj(C_i)$$
   and
   $$
     Hom_{\coprod_{i\in I} C_i}(x,y) = 
     \left\{
       \begin{aligned}
         Hom_{C_i}(x,y) & if x,y \in C_i
         \\
         \emptyset & otherwise
       \end{aligned}
     \right.
   $$ 
*  In [[Grpd]], the coproduct follows [[Cat]] rather than [[Grp]].  This is typical of [[oidifications]]: the coproduct becomes a disjoint union again.


#Remarks#

* When they exist, coproducts are unique up to unique canonical isomorphism, so we often say "[[generalized the|the]] coproduct."
* One can define in a similar way a coproduct of any family of objects.  A coproduct of the [[empty set|empty]] family is an [[initial object]].
* A coproduct is a special case of a [[colimit]] in which the diagram category is [[discrete category|discrete]].
* A coproduct in $C$ is the same as a [[product]] in the [[opposite category]] $C^{op}$.


[[!redirects coproducts]]