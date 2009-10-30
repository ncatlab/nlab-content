#Contents#
* automatic table of contents goes here
{:toc}

#Idea#


Given a [[group]] $G$ with subgroup $H \hookrightarrow G$ and a [[representation]] of $H$, there is canonically induced a representation of $G$: the _induced representation_.


#Explanation#


We start with a Lie group $G$ acting smoothly and transitively on a smooth [[manifold]] $M$.  The stabilizer of your favorite point $x \in M$ will be a Lie subgroup $H \subseteq G$, and we have

$$ M \cong G/H $$

Starting from this, there's a process that takes any representation $s$ of $H$ on a vector space $V$ and turns it into a vector bundle $E$ over $M$ --- the so-called 'induced bundle'.  Even better, the group $G$ acts on this bundle, and the projection 

$$ \pi : E \to M $$

gets along with the action of $G$:

$$ \pi(g e) = g \pi(e) .$$

So, we say that $E$ is a **$G$-equivariant** vector bundle over $M$.

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

We then define $E = (G\times V)/H$ as the set of orbits of that [[action]] of $H$, $M = G/H$ as the set of left cosets of $H$, and the projection $\pi: E\to M$ by $\pi ([(g,v)]) = g H$, where of course it makes no difference if we re-describe the orbit $[(g,v)]$ as $[(g h^{-1}, s(h)v]$ for any $h\in H$ because $(g h^{-1}) H = g H$.

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

That is, $\pi$ is a $G$-morphism.  This also means that the action maps fibers to fibers, $g_1:E_{(g H)}\to E_{g_1\cdot (g H)}$.  What's more, the action of $g_1$ restricted to the fiber $E_{(g H)}$ is $\phi_{g_1 g}\circ \phi_g^{-1}$, passing from $E_{(g H)}\to V \to E_{g_1\cdot (g H)}$, and this
is linear simply by virtue of the way we've defined the vector space operations on the $E_x$.

We get a representation $r$ of $G$ on the vector space $\Gamma(E)$ of sections of the bundle $E$ by:

$(r(g_1)f)(x) = g_1\cdot f(g_1^{-1}\cdot x)$

##Unitarity##

+-- {: .standout}
Beware! The chain of reasoning in this subsection is not complete, and I'm not confident that it's entirely correct. I'm posting it half-finished in the hope that many hands will make lighter (and more accurate) work.
=--

In physics, one is often concerned with unitary representations, so we should make sure that a unitary representation of $H$ will induce a unitary representation of $G$.

Let's say $V$ has an inner product, $\lang \cdot, \cdot \rang$, and $s$ is a unitary representation. We can define an inner product on $E_x$ by $\lang \lang p, q \rang \rang \equiv \lang \phi_g^{-1}(p), \phi_g^{-1}(q) \rang$. This definition is independent of our choice of $g$: if we chose $g h$ instead, we'd have

$$\lang \lang p, q \rang \rang = \lang \phi_{g h}^{-1}(p), \phi_{g h}^{-1}(q) \rang = \lang s(h^{-1}) \circ \phi_g^{-1}(p), s(h^{-1}) \circ \phi_g^{-1}(q) \rang = \lang \phi_g^{-1}(p), \phi_g^{-1}(q) \rang.$$

To be really thorough, we should verify that $\lang \lang \cdot, \cdot \rang \rang$ is in fact an inner product, but this should follow directly from our definition of the vector space operations on $E_x$.

Now we need to show that the action of any $g_1 \in G$ on the fiber $E_{(g H)}$ is unitary:

$$\lang \lang g_1 \cdot p, g_1 \cdot q \rang \rang = \lang \lang \phi_{g_1 g} \circ \phi_g^{-1}(p), \phi_{g_1 g} \circ \phi_g^{-1}(q) \rang \rang = \lang \phi_{g_1 g}^{-1} \circ \phi_{g_1 g} \circ \phi_g^{-1}(p), \phi_{g_1 g}^{-1} \circ \phi_{g_1 g} \circ \phi_g^{-1}(q) \rang = \lang \phi_g^{-1}(p), \phi_g^{-1}(q) \rang = \lang \lang p, q \rang \rang.$$

Finally, we need to define an inner product on $\Gamma(E)$, and show that the representation $r$ is unitary. If we had a $G$-invariant measure $\mu$ on $G/H$, we could define the inner product of two sections of $f$ and $f'$ of $E$ to be

$$\int \lang \lang f(x), f'(x) \rang \rang \; d\mu(x).$$

We would then have

$$\int \lang \lang (r(g_1)f)(x), (r(g_1)f')(x) \rang \rang \; d\mu(x) = \int \lang \lang g_1 \cdot f(g_1^{-1} \cdot x), g_1 \cdot f'(g_1^{-1} \cdot x) \rang \rang \; d\mu(x) = \int \lang \lang f(g_1^{-1} \cdot x), f'(g_1^{-1} \cdot x) \rang \rang \; d\mu(x)$$

(because $g_1$ acts unitarily on each fiber)

$$= \int \lang \lang f(x), f'(x) \rang \rang \; d\mu(g_1 \cdot x)$$

(because $G$ acts transitively on $G/H$)

$$= \int \lang \lang f(x), f'(x) \rang \rang \; d\mu(x)$$

(because $\mu$ is $G$-invariant). This shows that $r$ is unitary.

+-- {: .query}
But where do we get a $G$-invariant measure on $G/H$?
=--

#Adjoint of induced bundle construction#


The induced bundle construction described above is a functor that takes representations of the stabilizer subgroup $H$ to $G$-equivariant vector bundles over $M$:

$$L: Rep(H) \to Vect(M,G) $$

There is a related functor going the other way:

$$R: Vect(M,G) \to Rep(H) $$

which restricts the action of $G$ on the whole bundle to the action of the stabilizer subgroup $H$ on the fiber over the chosen point $x$.  We now wish to show that $L$ and $R$ are adjoint functors.

[[!include induced representation/adjoint]]

In the diagram above, on the top left we have a generic $G$-equivariant vector bundle over $M$, $F\in Vect(M,G)$, with projection $\pi_1:F\to M$, and a chosen point $x\in M$ whose stabilizer subgroup is $H$.  The functor $R$ maps $F$ to a representation of $H$ on the fiber over $x$, $\pi_1^{-1}(x)$, shown on the top right.

On the bottom right, we have a generic representation of $H$ on a vector space $V$.  The morphisms of $Rep(H)$ are intertwiners, so we are interested in intertwiners such as $i:V\to \pi_1^{-1}(x)$.  The functor $L$, the induced bundle construction, maps a generic representation of $H$ to a $G$-equivariant vector bundle $(G\times V)/H$, shown on the bottom left.  This bundle has a projection $\pi_2: (G\times V)/H \to G/H$, $\pi_2([(g,v)])=g H$.  Since $M \cong G/H$, this bundle is in $Vect(M,G)$.  And we are interested in the morphisms of $Vect(M,G)$, such as $(f,m)$ where $f:L(V)\to F$ and $m:G/H\to M$.

In fact, we need to work with a _subcategory_ of $Vect(M,G)$ in which all morphisms preserve the point $x\in M$.  When we deal with bundles over $G/H \cong M$, we will use the obvious bijection $g H \to g\cdot x$, and accordingly restrict ourselves to vector bundle morphisms that map $x$ to the coset $e H$ or _vice versa_.

We are assuming that $G$ acts transitively on $M$, so given any $y\in M$ there exists at least one element of $G$, say $k(y)$, such that $k(y)\cdot x = y$.  We will now assume that some definite function $k:M\to G$ has been chosen with this property, and for convenience we will further assume that $k(x)=e$, the identity element in $G$.  The group element $k(y)$ gives us a specific way to use the action of $G$ on $M$ to get from our chosen point $x$ to some other point $y$ --- and equally, to use the action of $G$ on the whole bundle $F$ to get from the fiber over $x$ to the fiber over $y$.

Now, to show that $L$ and $R$ are adjoint functors, we need to construct a bijection between the intertwiners $i:V\to \pi_1^{-1}(x)$ and the $G$-equivariant vector bundle morphisms $(f,m)$, where $f:L(V)\to F$ and $m:G/H\to M$.

Given an intertwiner $i:V\to \pi_1^{-1}(x)$, we start by defining $m:G/H\to M$ by:

$$m(g H)=g\cdot x$$

which is independent of $i$, and is just the obvious bijection between $G/H$ and $M$.  Next, we define $f:L(V)\to F$ by:

$$f([(g,v)]) = g\cdot i(v)$$

In other words, given the equivalence class $[(g,v)]$ we use the intertwiner $i$ to take $v\in V$ to $\pi_1^{-1}(x)$, and then the action of $G$ on $F$ to take the result to the fiber $\pi_1^{-1}(g\cdot x)$.  This satisfies the compatibility condition on the projections:

$$\pi_1(f([(g,v)])) = g\cdot x = m(g H) = m(\pi_2([(g,v)]))$$

We also need to check that $f$ commutes with the actions of $G$ on the respective bundles:

$$f(g_1\cdot [(g,v)]) = f([(g_1 g,v)]) = (g_1 g)\cdot i(v) = g_1\cdot f([(g,v)])$$

Next, given a $G$-equivariant vector bundle morphism $(f,m)$, where $f:L(V)\to F$ and $m:G/H\to M$ with $m(e H)=x$, we define an intertwiner $i:V\to \pi_1^{-1}(x)$ by:

$$i(v)=f([(e,v)])$$

We know $i$ will map to $\pi_1^{-1}(x)$ because $f$ must map $[(e,v)]$ to a point in the fiber over $m(\pi_2([(e,v)]))=m(e H)=x$.

We check that this is an intertwiner for the representations of $H$ on the respective vector spaces:

$$i(s(h)v)=f([(e,s(h)v)])=f([(h,v)])=f(h\cdot[(e,v)])=h\cdot i(v)$$

We can also demonstrate a bijection between intertwiners and $G$-equivariant vector bundle morphisms in the other direction:  intertwiners $i^*:\pi_1^{-1}(x)\to V$ and vector bundle morphisms $(f^*,m^*)$, where $f^*:F\to L(V)$ and $m^*:M\to G/H$.

Given an intertwiner $i^*:\pi_1^{-1}(x)\to V$, we define $m^*:M\to G/H$ as:

$$m^*(y) = k(y) H$$

We define the map $f^* : F \to L(V)$ by:

$$f^*(w) = [(k(\pi_1(w)), i^*(k(\pi_1(w))^{-1}\cdot w) )]$$

for each $w\in F$.  Because $k(\pi_1(w))\cdot x = \pi_1(w)$, $k(\pi_1(w))^{-1}$ will map the entire fiber to which $w$ belongs to $\pi_1^{-1}(x)$, the domain of the intertwiner $i^*$.  And we have:

$$\pi_2(f^*(w)) = k(\pi_1(w)) H = m^*(\pi_1(w))$$

The map $f^*$ is a linear map between the fibers $\pi_1^{-1}(y)$ and $\pi_2^{-1}(m^*(y))$, because, along with the linearity of $i^*$, the vector space structure on the fibers of $L(V)$ is _defined_ so all maps of the form $v\to [(g,v)]$ are linear.  So, $m^*$ and $f^*$ together give us a vector bundle morphism from $F$ to $L(V)$.

In order to be a morphism in the category of $G$-equivariant vector bundles, $f^*$ should also commute with the action of $G$.  We have:

$$f^*(g\cdot w) = [(k(\pi_1(g\cdot w)), i^*(k(\pi_1(g\cdot w))^{-1} g\cdot w) )] = [(k(g\cdot \pi_1(w)), i^*(k(g\cdot \pi_1(w))^{-1} g\cdot w) )]$$

Let's abbreviate $\pi_1(w)$ as $y$ and define $h=k(g\cdot y)^{-1} g k(y)$, which takes $x$ to $x$ and so must lie in $H$.  Then we have:

$$f^*(g\cdot w) = [(k(g\cdot y), i^*(h k(y)^{-1}\cdot w) )] = [(k(g\cdot y), s(h) i^*(k(y)^{-1}\cdot w) )] = [(k(g\cdot y) h, i^*(k(y)^{-1}\cdot w) )]$$
$$ = [(g k(y) , i^*(k(y)^{-1}\cdot w) )] = g\cdot [(k(y) , i^*(k(y)^{-1}\cdot w) )] = g\cdot f^*(w)$$

Suppose we're given a $G$-invariant vector bundle morphism $(f^*,m^*)$, where $f^*:F\to L(V)$ and $m^*:M\to G/H$, with $m^*(x)=e H$.

We make use of the linear bijection $\phi_e:V\to E_{e H}$, defined by $\phi_e(v)=[(e,v)]$.  We introduced these linear bijections $\phi_g$ when initially describing the induced bundle construction. We define $i^*:\pi_1^{-1}(x)\to V$ by:

$$i^*(w) = \phi_e^{-1}(f^*(w))$$

We check that this is an intertwiner between the relevant representations of $H$:

$$i^*(h\cdot w) = \phi_e^{-1}(f^*(h\cdot w))= \phi_e^{-1}(h\cdot f^*(w))$$

Suppose $f^*(w)=[(e,v)]$ for some $v\in V$.  Then $i^*(w) = v$, and :

$$h\cdot f^*(w) = [(h,v)] = [(e,s(h)v)]$$

$$i^*(h\cdot w) = \phi_e^{-1}([(e,s(h)v)]) = s(h)v = s(h) i^*(w)$$

#Related issues#

[[Bill Lawvere]] noted a structural similarity between induced representations and quantification. See blog [discussion](http://golem.ph.utexas.edu/category/2007/10/concrete_groups_and_axiomatic.html#c012917).

If the modules over a group are considered as comodules over the function Hopf algebra over the group, then one can instead consider the induction for comodules. See [[cotensor product]]. 

#References#

This blog entry contains related discussion:

* John Baez, [Unitary Representations of the Poincare Group](http://golem.ph.utexas.edu/category/2009/03/unitary_representations_of_the.html#comments)

The above text is taken from these comments

* Greg Egan _[Induced representations](http://golem.ph.utexas.edu/category/2009/03/unitary_representations_of_the.html#c023252)_

* John Baez _[Reply](http://golem.ph.utexas.edu/category/2009/03/unitary_representations_of_the.html#c023258)_