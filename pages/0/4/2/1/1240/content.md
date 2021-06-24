
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

# Induced modules
* table of contents
{:toc}

## Idea

Given a [[group]] $G$ with [[subgroup]] $H \hookrightarrow G$ and a [[representation]] of $H$, there is a canonically induced representation of $G$: the _induced representation_.

## Definition

We give an exposition of the 

* [Traditional formulation](#TraditionalFormulation)

of induced representations. Then we provide a 

* [General abstract formulation in homotopy type theory](#GeneralAbtractDefinition)

that refines the notion to [[∞-action|∞-representations]] of [[∞-groups]] equipped with any additional geometric structure.


### Traditional formulation
 {#TraditionalFormulation}

#### Induced representations
 {#InducedRepresentations}

Every [[subgroup]]-inclusion $H \overset{\iota}{\hookrightarrow} G$ induces a [[restricted representation]]-functor between the corresponding [[categories of representations]]

$$
  Rep(G)
    \overset{\iota^\ast }{\longrightarrow}
  Rep(H)
$$

which simply [[forgetful functor|forgets]] the full $G$-[[action]] on a given $G$-representation $V$ and remembers only the action of the subgroup $H$.

+-- {: .num_defn #InducedRepresentationsAsLeftAdjointToRestriction}
###### Definition
**(left-induced representations as [[left adjoint]] to [[restricted representations]])**

If the [[restricted representation|restriction functor]] $\iota^\ast$ has a [[left adjoint]] (which is usually the case, but depends on which exact flavour of [[groups]] and of their [[category of representations]] one considers), then this is called the functor assigning _left-induced representations_, often just _induced representations_, for short:

$$
  Rep(G)
    \underoverset
     {\underset{\iota^\ast}{\longrightarrow}}
     {\overset{ind_H^G}{\longleftarrow}}
     {\bot}
  Rep(H)
$$

=--

+-- {: .num_remark}
###### Remark

This is directly analogous to [[extension of scalars]] $\dashv$ [[restriction of scalars]].

=-- 

With given flavour of [[groups]] and their [[category of representations]] specified, it is typically immediate to give explicit formulas for left induced representations:

+-- {: .num_example #InductionOfFiniteDimensionalRepresentationsOfFiniteGroups}
###### Example
**(induction of [[finite-dimensional vector space|finite-dimensional]] [[linear representations]] of [[finite groups]])**

In the case that $G$ (and hence $H$) is a [[finite group]] and $Rep(G)$ is the [[category of representations|category of]] [[finite-dimensional vector space|finite-dimensional]] representations over some [[ground field]] $k$.,
the general induced representation functor (Def. \ref{InducedRepresentationsAsLeftAdjointToRestriction}) exists and is explicitly given by forming the [[tensor product of representations]] with the $H$-[[permutation representation]] spanned by the underlying [[set]] of $G$:

$$
  ind_H^G
  \;\colon\;
  V 
    \mapsto 
  k[G] \otimes_{H} V
  \,.
$$

For example, if $V = \mathbf{1}$ is the [[trivial representation]] of [[dimension]] 1 then its induced representation is the basic [[permutation representation]] spanned by the [[coset]]-space $G/H$:

$$
  ind_H^G
  \left( 
    \mathbf{1}
  \right)
  \;=\;
  k[G/H]
  \,.
$$

See at _[[induced representation of the trivial representation]]_ for more.

=--

See e.g. [tomDieck 09, Chapter 4](#tomDieck09).

<br/>

#### More exposition
 {#TraditionalFormulationExplanation}

Suppose a [[Lie group]] $G$ acts smoothly and transitively on a [[smooth manifold]] $M$.  The [[stabilizer subgroup]] of a given point $x \in M$ is then a Lie subgroup $H \subseteq G$, and 

$$ 
  M \cong G/H
  \,, 
$$

is the [[coset]] space.

Starting from this, there's a recipe taking any [[representation]] $s$ of $H$ on a [[vector space]] $V$ and turns it into a [[vector bundle]] $E$ over $M$ --- called the _induced bundle_.  Moreover, the group $G$ [[action|acts]] on this [[bundle]], and the [[projection]] 

$$ \pi : E \to M $$

is compatible with the [[action]] of $G$:

$$ \pi(g e) = g \pi(e) .$$

Hence $E$ is a **$G$-equivariant** vector bundle over $M$.

The 'process' described is actually a [[functor]], the **induction functor**.

There's a [[category]]

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

And why is this so great?  Well, there's also a process that takes any representation of $G$ and [[restricted representation|restricts]] it to a representation of $H$:

$$R': Rep(G) \to Rep(H) $$

And this too, has a [[left adjoint]]:

$$L' : Rep(H) \to Rep(G) $$

which is called the _induced representation_.



#### Detailed description
 {#TraditionalDetailed}

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



### General abstract formulation in homotopy type theory
 {#GeneralAbtractDefinition}

We formulate induction and coinduction of representations abstractly in [[homotopy type theory]]. (Hence the following is automatically the [[(∞,1)-category theory]]-version, which in parts is sometimes referred to as _[[cohomological induction]]_.)

Let $\mathbf{H}$ be an ambient [[(∞,1)-topos]]. By the discussion at _[[∞-action]]_, for $G \in Grp(\mathbf{H})$ a [[group object in an (∞,1)-category|group object]] in $\mathbf{H}$, hence an [[∞-group]], the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}G}$ over its [[delooping]] is the [[(∞,1)-category]] of $G$-[[∞-actions]] 

$$
  Act(G) \simeq \mathbf{H}_{/\mathbf{B}G}
  \,.
$$

(A genuine _[[∞-representation]]/[[∞-module]]_ over $G$ may be taken to be a an abelian $\infty$-group object in $Act(G)$, but we can just as well work in the more general context of possibly non-linear representations, hence of actions.)

Accordingly, for $f \colon H \to G$ a homomorphism of [[∞-groups]], hence for a morphism $\mathbf{B}f \colon \mathbf{B}H \to \mathbf{B}G$ of their [[deloopings]], there is the corresponding [[base change geometric morphism]]

$$
  (\sum_f \dashv f^* \dashv \prod_f)
  \colon
  Act(H)
   \stackrel{\overset{\sum_f}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\underset{\prod_f}{\to}}}
  Act(G)
  \,.
$$

Here

* the [[inverse image]]/[[(∞,1)-pullback]] functor $f^*$ produces the "[[restricted representation|restricted]]" $\infty$-representations along $f$;

* the [[dependent sum]] $\sum_f$ is the _induced representation_ ∞-functor;

* the [[dependent product]] $\prod_f$ is the _coinduced representation_ ∞-functor.
 
{#LawvereInduced} For the case of [[permutation representations]] of [[discrete groups]]  this perspective is made explicit in ([Lawvere 69, p. 14](#Lawvere69), [Lawvere 70, p. 5](#Lawvere70)).


## Properties

### Brauer induction theorem
 {#BrauerInductionTheorem}

The [[Brauer induction theorem]] says that over the [[complex numbers]] the [[virtual representations]] of a [[finite group]] are all virtual combinations of [[induced representations]] of 1-dimensional representations.

### Unitarity

+-- {: .standout}
Beware! The chain of reasoning in this subsection is not complete, and I'm not confident that it's entirely correct. I'm posting it half-finished in the hope that many hands will make lighter (and more accurate) work.
=--

We discuss that [[unitary representations]] induce again unitary representations.

(This is for instance relevant in applications to [[physics]], such as in the study of [[unitary representation of the Poincaré group]].)

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


### Adjoint of induced bundle construction

The induced bundle construction described above is a [[functor]] that takes representations of the [[stabilizer subgroup]] $H$ to $G$-equivariant vector bundles over $M$:

$$L: Rep(H) \to Vect(M,G) $$

There is a related functor going the other way:

$$R: Vect(M,G) \to Rep(H) $$

which [[restriction|restricts]] the action of $G$ on the whole bundle to the action of the stabilizer subgroup $H$ on the fiber over the chosen point $x$.  The existence of this [[adjunction]] is known as **[[Frobenius reciprocity]]**.

We now wish to show that $L$ and $R$ are adjoint functors.

[[!include induced representation > adjoint]]

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

## Examples and Applications

### Regular representation

The [[regular representation]] of a group $G$, as a linear representation, is the induced representation of the trivial representation along the trivial subgroup inclusion $Ind_1^G(1)$.

### Centralizer algebra / Hecke algebra
 {#HeckeAlgebra}

Let 

$$
  i \colon H \hookrightarrow G
$$ 

be a group homomorphism (often assumed to be a [[subgroup]] inclusion, and sometimes with $G$ assumed to be a [[finite group]]). For $E \in H Rep$ some $H$-representation (often taken to be the trivial $H$-representation), let $Ind_i E \in G Rep$ be the induced $G$-representation. Then the [[endomorphism ring]] $End_G(Ind_i E)$ of $Ind_i E$ in $G Rep$ is called the _centralizer algebra_ or also the _[[Hecke algebra]]_ or _[[Iwahori-Hecke algebra]]_ $Hecke(E,i)$ of the induced representation. (Basics are in ([Woit, def. 2](#Woit)), details are in ([Curtis-Reiner, section 67](#CR)), a quick survey of related theory is in ([Srinivasan](http://homepages.math.uic.edu/~srinivas/bfggpaper.pdf))).

In terms of the notation in _[General abstract formulation](#GeneralAbtractDefinition)_ above and for $i \colon H \to G$ any homomorphism of $\infty$-groups, we have the [[∞-monoid]]

$$
  Hecke(E,i)
  \coloneqq
\underset{\mathbf{B}G}{\prod}\left[\underset{\mathbf{B}i}{\sum} E, \underset{\mathbf{B}i}{\sum} E \right]
  \,,
$$

where $[-,-]$ is the [[internal hom]] in the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}G} \simeq G Act(\mathbf{H})$.

For $V \in Act(G)$ any other representation, there is a canonical [[∞-action]] of $Hecke(E,i)$ on $\underset{\mathbf{B}G}{\prod} \left[\underset{\mathbf{B}i}{\sum} E , V \right]$. If here $E$ is the trivial representation then by adjointness this is the [[invariants]] $V^G$ of $V$ and hence the Hecke algebra acts on the invariants. (See for instance ([Woit, def. 2](#Woit))). This is sometimes called the _Hecke algebra action on the Iwahori fixed vectors_ ([e.g. here, p. 9](#http://sporadic.stanford.edu/bump/bbf.pdf))

### Zuckerman functors: Coinduction on Harish-Chandra modules

Coinduction on [[Harish-Chandra modules]] is referred to as
_[[Zuckerman induction]]_. See there for more details.

## Related concepts

* The identification of representation induction as the extra left adjoint in a [[base change]] morphism, as discussed in the _[General abstract discussion](#GeneralAbtractDefinition)_ above, puts induced representations in the same general abstract framework as [[existential quantification]] in [[logic]] and generally of [[dependent sum]] in [[dependent type theory]] (see there for more details). This relation has first been amplified in ([Lawvere](#Lawvere)).

* If the modules over a group are considered as comodules over the function Hopf algebra over the group, then one can instead consider the induction for comodules. See [[cotensor product]]. 

* The [[derived functor]] of the representation induction functor is often referred to as _[[cohomological induction]]_.

* [[Dirac induction]]

* The [[character]] of an induced representation is an [[induced character]].

[[!include homotopy type representation theory -- table]]


## References

### Traditional formulation
 {#ReferencesTraditionalFormulation}

* encyclopaedia of math [induced representation](https://www.encyclopediaofmath.org/index.php/Induced_representation)

Original articles includes

* {#Mackey52} [[George Mackey]], _Induced representations of locally compact groups I_, Annals of Mathematics, 55 (1952) 101&#8211;139; 

* {#Mackey53} [[George Mackey]], _Induced representations of locally compact groups II_, Annals of Mathematics, 58 (1953) 193&#8211;221; 

* {#Mackey68} [[George Mackey]], _Induced representations of groups and quantum mechanics_, W. A. Benjamin, New York, 1968


Textbook accounts include

* {#CR} C. Curtis and I. Reiner, _Methods of Representation Theory with applications to finite groups and orders_, Wiley (1987)
 


Lecture note with standard material on induced representations and [[Frobenius reciprocity]] include

* {#tomDieck09} [[Tammo tom Dieck]], Chapter 4 of _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf))
 

MO discussion includes

* [Wrong-way Frobenius reciprocity for finite groups representations](http://mathoverflow.net/questions/132272/wrong-way-frobenius-reciprocity-for-finite-groups-representations)




The [exposition of the Traditional formulation](#TraditionalFormulation) in the above entry is in parts taken from 

* [[Greg Egan]], _[Induced representations](http://golem.ph.utexas.edu/category/2009/03/unitary_representations_of_the.html#c023252)_

* [[John Baez]] _[Reply](http://golem.ph.utexas.edu/category/2009/03/unitary_representations_of_the.html#c023258)_

and related discussion is in

* [[John Baez]], [Unitary Representations of the Poincare Group](http://golem.ph.utexas.edu/category/2009/03/unitary_representations_of_the.html#comments)

### General abstract formulation

The [general abstract formulation](#GeneralAbtractDefinition) above is mentioned (for [[discrete groups]] and their [[permutation representations]]) in 

* {#Lawvere69} [[Bill Lawvere]], _[[Adjointness in Foundations]]_, Dialectica 23 (1969), 281-296,  Reprints in Theory and Applications of Categories, No. 16, 2006, pp. 1&#8211;16. ([pdf](http://www.tac.mta.ca/tac/reprints/articles/16/tr16.pdf))
 
* {#Lawvere70} [[Bill Lawvere]], _[[Equality in hyperdoctrines and comprehension schema as an adjoint functor]]_, Proceedings of the AMS Symposium on Pure Mathematics XVII (1970), 1-14. ([pdf](https://ncatlab.org/nlab/files/LawvereComprehension.pdf))

 
The general case of $\infty$-groups in $\infty$-toposes is further discussed in 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_


[[!redirects induced module]]
[[!redirects induced representations]]
[[!redirects induction functor]]
[[!redirects induction functors]]

[[!redirects coinduced representation]]
[[!redirects coinduced representations]]
[[!redirects coinduction functor]]
[[!redirects coinduction functors]]
