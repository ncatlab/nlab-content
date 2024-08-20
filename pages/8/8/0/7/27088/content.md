+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--


## Definition

Let $R$ be a ring and $M$ a left $R$-module. Then its __singular submodule__ $\mathcal{Z}(M)$ is the subset consisting of all $m\in M$ whose annihilator $Ann^l(m) = \{ r\in R| r m = 0\}$ is a left [[essential ideal]] in $R$ (including possibly entire $R$). 

Analogously we may define singular submodules of right $R$-modules. 

#### A proof that $\mathcal{Z}(M)$ is an $R$-submodule

$\mathcal{Z}(M)$ is clearly an additive subgroup because $Ann^l(m)\cap Ann^l(m')\subset Ann^l(m+m')$ and the intersection of essential ideals is essential. 

It remains to show that if $Ann^l(m)$ is essential and $r\in R$ then $Ann^l(r m)$ is also essential.
In the trivial case $r m = 0$ its annihilator is $R$. Thus we assume that also $r m \neq 0$. 

Then, take any other left ideal $0\neq I\subset R$. 
Then $I r\subset R$ is also a left ideal. If $I r$ is a non-zero ideal then, because $Ann^l(m)$ is essential, there is an $r' = r'' r \in I r \cap Ann^l(m)\neq 0$ with $r''\in I$ that is $r''\in I\cap Ann^l(r m)$. 
If, on the other hand, $I r = 0$ then $I r m = 0$ hence $I\subset Ann^l(r m)$. 

We have shown that in both cases $I\cap Ann^l(r m)\neq 0$. Thus, $Ann^l(r m)$ is essential as well and $\mathcal{Z}(M)$ is an $R$-submodule of $M$.


## Properties

$M\mapsto \mathcal{Z}(M)$ is a left exact (hence idempotent) additive subfunctor of the identity functor on $R-Mod$. However, it is typically not a radical functor: it is not satisfying $\mathcal{Z}(M/\mathcal{Z}(M)) = 0$.

## Literature

* wikipedia: [singular submodule](https://en.wikipedia.org/wiki/Singular_submodule)
* yhasrifi at wordpress: [The singular submodule](https://ysharifi.wordpress.com/2011/12/07/the-singular-submodule) 

category: algebra

[[!redirects singular submodules]]

