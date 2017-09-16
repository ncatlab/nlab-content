#Idea#


Given a [[group]] $G$ with subgroup $H \hookrightarrow G$ and a [[representation]] of $H$, there is canonically induced a representation of $G$: the _induced representation_.


#Explanation#


We start with a Lie group $G$ acting smoothly and transitively on a smooth manifold $M$.  The stabilizer of your favorite point $x \in M$ will be a Lie subgroup $H \subseteq G$, and we have

$$ M \cong G/H $$

Starting from this, there's a process that takes any representation $s$ of $H$ on a vector space $V$ and turns it into a vector bundle $E$ over $M$ --- the so-called 'induced bundle'.  Even better, the group $G$ acts on this bundle, and the projection 

$$ \pi : E \to M $$

gets along with the action of $G$:

$$ \pi(g e) = g \pi(e) .$$

So, we say the $E$ is a **$G$-equivariant** vector bundle over $M$.

The 'process' described is actually a [[functor]].  

There's a category 

$$Rep(H)$$

of linear representations of $H$, and a category 

$$Vect(M,G)$$

of $G$-equivariant vector bundles over $M$.  The induced bundle construction gives a functor

$$L: Rep(H) \to Vect(M,G) $$

But, if you think about it, you'll notice there's also a functor going back the other way:

$$R: Vect(M,G) \to Rep(H) $$

If you give me a $G$-equivariant vector bundle $E$ over $M$, I can take its fiber over your favorite point $x$, and I get a vector space --- and this becomes a representation of the stabilizer group $H$, thanks to how $G$ acts on $E$.

This functor is <i>simpler</i> than the induced bundle construction!

Whenever we have functors going both ways between two categories, we should suspect that they're [[adjoint functor|adjoints]].   The simpler functor often amounts to 'forgetting' something.  This forgetful functor is usually the <i>right</i> adjoint.  It's partner going the other way, the <i>left</i> adjoint, usually involves 'constructing' something instead of 'forgetting' something.   

And indeed, that's what's happening here!
Technically, this is to say that

$$hom(L V, F) \cong hom(V, R F)$$

Here $V$ is a representation of $H$ --- note abuse of notation in calling it $V$, which is the name for the vector space on which $G$ acts, instead of the more pedantic full name for a representation, which is something like $s: G \to GL(V)$.   

Similarly, $F$ is a $G$-equivariant vector bundle over $M$ --- and this should be something like $\pi : F \to M$, or something even more long-winded that gives a name to how $G$ acts on $F$ and $M$.

$L V$ is the induced bundle corresponding to $V$.

$R F$ is the fiber of $F$ over your favorite point $x$, which becomes a representation of $G$.

And this: 

$$hom(L V, F) \cong hom(V, R F)$$

says that $G$-equivariant vector bundle maps from $L V$ to $F$ are in natural 1-1 correspondence with intertwining operators from $V$ to $R F$.  

Now, whenever you see any sort of 'forgetful' process, you should wonder if it has a left adjoint, a construction which in some loose sense is the 'reverse' of forgetting.  Why?  Because these left adjoints tend to be important.  

Endowed with this heuristic, as soon as you see there's a rather obvious 'forgetful' process that takes a $G$-equivariant vector bundle over $M$ and gives a representation of $H$ on the fiber over $x \in M$, you will seek the 'reverse' process --- and then you'll rediscover the induced bundle construction!

And why is this so great?  Well, there's also a process that takes any representation of $G$ and restricts it to a representation of $H$:

$$R': Rep(G) \to Rep(H) $$

And this too, has a left adjoint:

$$L' : Rep(H) \to Rep(G) $$

which is called the <b>induced representation</b> trick.



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



#Related issues#

[[Bill Lawvere]] noted a structural similarity between induced representations and quantification. See blog [discussion](http://golem.ph.utexas.edu/category/2007/10/concrete_groups_and_axiomatic.html#c012917).



#References#

This blog entry contains related discussion:

* John Baez, [Unitary Representations of the Poincare Group](http://golem.ph.utexas.edu/category/2009/03/unitary_representations_of_the.html#comments)

The above text is taken from these comments

* Greg Egan _[Induced representations](http://golem.ph.utexas.edu/category/2009/03/unitary_representations_of_the.html#c023252)_

* John Baez _[Reply](http://golem.ph.utexas.edu/category/2009/03/unitary_representations_of_the.html#c023258)_