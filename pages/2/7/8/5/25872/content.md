
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

What is called the *category of vines* is the [[free construction|free]] [[braided monoidal category|braided]] [[strict monoidal category]] containing a braided monoid (i.e. an [[E2-algebra|$E_2$-algebra]]). It is also the [[PRO|PROB]] for braided monoids.  

Concretely:

\begin{defn}
Let 

* $P_I \coloneqq \big\{ (i,0,1) \,\big\vert\, i=1, 2, \ldots, m \big\}$ 

* $P_T \coloneqq \big\{ (i,0,0) \,\big\vert\, i=1, 2, \ldots,n \big\}$ 

be [[linear order|linearly ordered]] collections of points in [[Cartesian space|$\mathbb{R}^3$]]. 

Then an *$(m,n)$-vine* is a set of arcs $\{v_1,\ldots,v_m\}$ (i.e. piecewise linear maps from $[0,1]$ to $\mathbb{R}^3$) with the following properties: 

1. $v_i(0)=(i,0,1)$, 

1. $v_i(1)\in P_T$, 

1. for all $h\in [0,1]$, $v_i(h)$ has $z$-coordinate $1-h$,

1. if $v_i(t)=v_j(t)$ for any $t\in (0,1]$ then $v_i(s)=v_j(s)$ for all $t\leq s\leq 1$. 

\end{defn}

\begin{defn}\label{CategoryV}
Let $\mathbb{V}$ be the category with set of [[objects]] the [[natural numbers]] with set of [[morphisms]] $\mathbb{V}(m,n)$ being $(m,n)$-vines modulo a suitable notion of "isotopy" that allows arcs to be deformed up to homotopy but not pass through one another.
\end{defn}


## References

* [[Mark Weber]], §6.3 of: _Internal algebra classifiers as codescent objects of crossed internal categories_. Theory and Applications of Categories, **30** 50 (2015) 1713–1792 &lbrack;[tac:30/50](http://www.tac.mta.ca/tac/volumes/30/50/30-50abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/30/50/30-50.pdf)&rbrack;



[[!redirects vines]]
