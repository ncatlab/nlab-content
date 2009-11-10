# Semidirect products
* tic
{: toc}


## Definitions

If a group $G$ [[action|acts]] on a group $\Gamma$ on the left, then there is a
[[semidirect product]] group whose underlying set is $\Gamma \times  G$
but whose multiplication is

$$(\delta,h)(\gamma,g)= (\delta \, ^h \gamma, h g)$$

for $\delta, \gamma \in \Gamma,\; h,g \in G$. This is called in
group theory the semidirect product (see for example the [Wikipedia entry](http://en.wikipedia.org/wiki/Semi-direct_product)) and written $\Gamma \rtimes \, G$.
There is a projection morphism $p:\Gamma \rtimes \, G \to G$ ,
$(\gamma, g) \to g$. A section $s$ of this can be identified with a
derivation $d$, i.e. $d$  satisfies $d(h g)= (d h) \,^h (d g)$.

It is useful to generalise this to the case $\Gamma$ is a [[groupoid]].
This occurs if for example $\Gamma = \pi_1 X$ where $X$ is a (left)
$G$-space.

So if $X=Ob(\Gamma)$, then $\Gamma \rtimes \, G$ has object set $X$ and
a morphism $y \to x$ is a pair $(\gamma,g)$ such that $\gamma: y \to
g x$ in $\Gamma$. The composition law is then given again by   

$$(\delta,h)(\gamma,g)= (\delta \, ^h \gamma, h g) $$

if  $(\delta, h): z \to y$, so that $\delta: z \to h y$ in $\Gamma$. 

If $\Gamma$ is a discrete groupoid, and so identified with $X$, then
we get $X \rtimes \, G$ which is the [[action groupoid]] of the action. In
this case the projection $p: X \rtimes \, G \to G$ is a covering
morphism of groupoids, i.e.  any $g \in G$ has a unique lifting with
given initial point. Note that if $Y \to X $ is a covering map of
spaces, then the induced morphism of fundamental groupoids is a
covering morphism of groupoids. If $q: H \to \pi_1 X$ is a covering
morphism of groupoids, and $X$ admits a universal covering map, then
there is a topology on $Y=Ob(H)$ such that $H \cong \pi_1 Y$. In
this way, the category of covering maps of $X$ is equivalent to the
category of covering morphisms of $\pi_1 X$.

The utility of the more general construction is that there is notion
of orbit groupoid $\Gamma //G$ (identify any $\gamma$ and $^g
\gamma$) and it is a theorem that the orbit groupoid is isomorphic to
the quotient groupoid

$$ (\Gamma \rtimes \, G)/N$$

where $N$ is the normal closure in $\Gamma \rtimes \, G$ of all
elements $(1_x,g)$. Details are in the book reference below (but the
conventions are not quite the same).


##References##

* R. Brown, "Topology and groupoids", Booksurge 2006.

* P.J. Higgins and J. Taylor,  The Fundamental Groupoid and
  Homotopy Crossed Complex of an Orbit Space, in K.H. Kamps et al., ed.,
   Category Theory: Proceedings Gummersbach 1981, Springer LNM
  962  (1982) 115--122.


[[!redirects semi-direct product]]