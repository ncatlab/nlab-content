#Idea#


Given a [[group]] $G$ with subgroup $H \hookrightarrow G$ and a [[representation]] of $H$, there is canonically induced a representation of $G$: the _induced representation_.


#Detailed description#


Given a [[group]] $G$ with a subgroup $H$, and a [[representation]] $s$ of $H$ on a vector space $V$, we define a left [[action]] of $H$ on the [[product]] $G\times V$ by $h\cdot (g, v) = (g h^{-1}, s(h)v)$.  We write $[(g,v)]$ for the orbit, or equivalence class, that contains $(g,v)$.

We then define $E = (G\times V)/H$ as the set of orbits of that [[action]] of $H$, $M = G/H$ as the set of right cosets of $H$, and the projection $\pi: E\to M$ by $\pi ([(g,v)]) = g H$, where of course it makes no difference if we re-describe the orbit $[(g,v)]$ as $[(g h^{-1}, s(h)v]$ for any $h\in H$ because $(g h^{-1}) H = g H$.

For each $x\in M$, choose $g$ to be any element of $G$ such that $x = g H$.  Define $E_x = \pi^{-1}(x)$, and $\phi_g:V\to E_x$, $\phi_g(v) = [(g,v)]$.

The map $\phi_g$ is onto:  for any $[(k,w)]\in E_{(g H)} = \pi^{-1}(g H)$, we have $k=g h_1^{-1}$ for some $h_1\in H$, so $k^{-1} g\in H$, $(k^{-1} g)\cdot (g, s(g^{-1} k)w) = (k,w)$, so $\phi_g(s(g^{-1} k)w) = [(g, s(g^{-1} k)w)] = [(k,w)]$.

The map $\phi_g$ is one-to-one:  if $\phi_g(v) = \phi_g(w)$, then $[(g,v)]=[(g,w)]$, so for some $h_1\in H$, we have $h_1\cdot (g,v) = (g,w)$, or $(g h_1^{-1}, s(h_1)v) = (g,w)$; equating the first coordinates requires $h_1=e$, and $s$ is a representation so $s(e)=1_V$, and $v=w$.

Since $\phi_g$ is a bijection between $E_x$ and the vector space $V$, we can make $E_x$ into a vector space by defining $\alpha p + \beta q \equiv \phi_g(\alpha \phi_g^{-1}(p) + \beta \phi_g^{-1}(q))$, for all $\alpha, \beta \in \mathbb{R}, p, q \in E_x$.  But is this independent of our choice of $g$?  If we chose $g h$ instead of $g$, we'd have $\phi_{g h}(v) = [(g h,v)] = [(g, s(h)v)] = \phi_g(s(h)v)$, so $\phi_{g h}=\phi_g\circ s(h)$, and $\phi_{g h}^{-1}=s(h^{-1})\circ \phi_g^{-1}$.  Then:

$\phi_{g h}(\alpha \phi_{g h}^{-1}(p) + \beta \phi_{g h}^{-1}(q)) =
(\phi_g\circ s(h))(\alpha (s(h^{-1})\circ \phi_g^{-1})(p) + \beta (s(h^{-1})\circ \phi_g^{-1})(q)) = \phi_g(\alpha \phi_g^{-1}(p) + \beta \phi_g^{-1}(q))$


in agreement with our original definition.

We define the action of $G$ on $E$ by $g_1\cdot [(g,v)] = [(g_1 g,v)]$, or in other words $g_1\cdot \phi_g(v) = \phi_{g_1 g}(v)$.
We then have:

$\pi(g_1\cdot [(g,v)]) = \pi[(g_1 g,v)] = (g_1 g) H = g_1\cdot (g H) = g_1\cdot \pi([(g,v)])$

That is, $\pi$ is a $G$-morphism.  This also means that the action maps fibres to fibres, $g_1:E_{(g H)}\to E_{g_1\cdot (g H)}$.  What's more, the action of $g_1$ restricted to the fibre $E_{(g H)}$ is $\phi_{g_1 g}\circ \phi_g^{-1}$, passing from $E_{(g H)}\to V \to E_{g_1\cdot (g H)}$, and this
is linear simply by virtue of the way we've defined the vector space operations on the $E_x$.

We get a representation $r$ of $G$ on the vector space $\Gamma(E)$ of sections of the bundle $E$ by:

$(r(g_1)f)(x) = g_1\cdot f(g_1^{-1}\cdot x)$


#References#

This blog entry contains related discussion:

* John Baez, [Unitary Representations of the Poincare Group](http://golem.ph.utexas.edu/category/2009/03/unitary_representations_of_the.html#comments)

The above text is taken from this comment by Greg Egan

* Greg Egan _[Induced representations](http://golem.ph.utexas.edu/category/2009/03/unitary_representations_of_the.html#c023252)_