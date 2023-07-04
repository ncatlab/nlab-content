##Definition

The so-called category of vines is the free braided strict monoidal category containing a [[braided monoids|braided monoid]]. It is also the [[PRO|PROB]] for braided monoids.  However, it has a concrete description as follows:

\begin{defn}
Let $P_I=\{(i,0,1):i=1,2,\ldots,m\}$ and $P_T=\{(i,0,0):i=1,2,\ldots,n\}$ be linearly ordered collections of points in $\mathbb{R}^3$. Then an $(m,n)$-vine is a set of arcs $\{v_1,\ldots,v_m\}$ (i.e. piecewise linear maps from $[0,1]$ to $\mathbb{R}^3$) with the following properties: $v_i(0)=(i,0,1)$, $v_i(1)\in P_T$,for all $h\in [0,1]$, $v_i(h)$ has $z$-coordinate $1-h$,
and if $v_i(t)=v_j(t)$ for any $t\in (0,1]$ then $v_i(s)=v_j(s)$ for all $t\leq s\leq 1$. 
\end{defn}

\begin{defn}
Let $\mathbb{V}$ be the category with set of objects the natural numbers with set of morphisms $\mathbb{V}(m,n)$ being $(m,n)$-vines modulo a suitable notion of "isotopy" that allows arcs to be deformed up to homotopy but not pass through one another.
\end{defn}


##References

* [[Mark Weber]], §6.3 of _Internal algebra classifiers as codescent objects of crossed internal categories_. Theory and Applications of Categories, 30(50):1713–1792, 2015. ([pdf](http://www.tac.mta.ca/tac/volumes/30/50/30-50.pdf))