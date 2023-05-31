
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



# Content
* table of contents
{: toc}

## Definitions

If a [[group]] $G$ [[action|acts]] on a group $\Gamma$ (on the left, say) by group [[automorphism]]

$$
  \rho : G \to Aut(\Gamma)
  \,,
$$

then there is a __semidirect product__ group $\Gamma \rtimes \, G$ whose underlying set is the [[Cartesian product]] $\Gamma \times  G$ but whose multiplication is twisted by $\rho$:

$$
  (\delta,h)(\gamma,g)= (\delta \rho(h)(\gamma) , h g)
$$

for $\delta, \gamma \in \Gamma,\; h,g \in G$.  For the rest of this page, $^h \gamma \coloneqq \rho(h)(\gamma)$ denotes the result of acting with $h$ on the left on $\gamma$.

If the twist is trivial, then this reduces to just the [[direct product group]] construction, whence the name.

There is a [[projection]] morphism $p:\Gamma \rtimes \, G \to G$ ,
$(\gamma, g) \to g$. A [[section]] $s$ of this can be identified with a
[[derivation]] $d$, i.e. $d$  satisfies $d(h g) = (d h) \,^h (d g)$.


### Interior semidirect products

Let $H$ be any group.  A decomposition of $H$ as an __internal__ semidirect product consists of a [[normal subgroup]] $\Gamma$ and a [[subgroup]] $G$, such that every element of $H$ can be written uniquely in the form $\gamma g$, for $\gamma \in \Gamma$ and $g \in G$.

The internal and external concepts are equivalent.  In particular, any (external) semidirect product $\Gamma \rtimes G$ is an internal semidirect product of the [[images]] of $\Gamma$ and $G$ in it.


### Right semidirect products

The definitions above are not symmetric in left and right; since the first definition begins with a left action, we may call it a *left* semidirect product.  Then a __right__ semidirect product is given by an action on the right, or internally by the requirement that every element can be written in the form $g \gamma$.

However, right and left semidirect products are equivalent.  Essentially, this is because any left action $(h,g) \mapsto {}^h{g}$ defines a right action $(g,h) \mapsto g^h \coloneqq {}^{h^{-1}}g$ and vice versa.

### As a left adjoint

Consider the [[category]] $GrpActions$ with

* [[objects]] $(G,\Gamma,\rho)$ where $G$ and $\Gamma$ are [[groups]] and $\rho: G \to \Aut(\Gamma)$ is a [[group homomorphisms]], and whose

* [[morphisms]] $(G,\Gamma,\rho) \to (G',\Gamma',\rho')$ are $G$-[[equivariant]] pairs of morphisms $f: G \to G'$ and $h: \Gamma \to \Gamma'$, i.e. such that $h(\rho(g)(\gamma)) = \rho'(f(g))(h(\gamma))$ for all $g \in G$ and $\gamma \in \Gamma$.

There is a [[forgetful functor]] $U: Arr(Grp) \to GrpActions$ from the [[arrow category]] of [[Grp]], sending a [[group homomorphism]] $f\colon G \to \Gamma$ to $(G,\Gamma,\rho)$ where $\rho: G \to Aut(\Gamma)$ is given by conjugation, i.e. $\rho(g)(\gamma) \coloneqq f(g) \gamma f(g)^{-1}$.

Now, its [[left adjoint functor]] $GrpActions \to Arr(Grp)$ maps $(G,\Gamma,\rho)$ to the [[inclusion]] $G \hookrightarrow \Gamma \rtimes_\rho G$.

### As a Grothendieck construction

Writing $\mathbb{B} G$ for the [[category]] with a single [[object]] $\ast$ and the [[group]] $G$ as its [[hom set]] (i.e. the [[delooping]] [[groupoid]] of $G$), define a [[functor]] $F \colon \mathbb{B}G \to$ [[Cat]] to send that single object to the delooping groupoid of $\Gamma$, i.e. $* \mapsto \mathbb{B}\Gamma$ and to send the morphisms $G \to Aut(\Gamma)$ according to the given [[action]] of $G$ on $\Gamma$.

Then the delooping of the semidirect product group $\Gamma \rtimes G$ arises as the [[Grothendieck construction]] of this functor:

$$
  \mathbb{B}( \Gamma \rtimes G)
  \;\simeq\;
  \int_{\mathbb{B}G}F
$$

### Semidirect products of groupoids

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

where $N$ is the [[normal closure]] in $\Gamma \rtimes \, G$ of all
elements $(1_x,g)$. Details are in the book reference below (but the
conventions are not quite the same).


## Properties

### As split group extensions

Semidirect product groups $A \rtimes_\rho G$ are precisely the split [[group extensions]] of $G$ by $A$. See at _[group extension -- split extensions and semidirect product groups](group+extension#SplitExtensionsAndSemidirectProductGroups)_.

## Examples

### The automorphisms on the circle group

For $U(1) = \mathbb{R}/\mathbb{Z}$ the [[circle group]], the [[automorphism group]] is

$$
  Aut(U(1)) \simeq \mathbb{Z}_2
  \,,
$$

where the nontrivial element in $\mathbb{Z}_2$ acts on $\mathbb{R}$ by multiplication with $-1$. Write $\rho_{aut} : U(1) \times \mathbb{Z}_2 \to U(1)$ for the automorphism [[action]]. The corresponding semidirect product group is the [[group extension]]

$$
  U(1) \stackrel{}{\hookrightarrow} U(1) \rtimes_{\rho_{aut}} \mathbb{Z}_2
  \to \mathbb{Z}_2
$$

where the group operation is given by

$$
  (c_1 \; mod \; \mathbb{Z}, \sigma_1)
  \cdot
  (c_2\; mod \; \mathbb{Z}, \sigma_2)
  =
  (c_1 + \sigma_1(c_2) \; mod \; \mathbb{Z}, \sigma_1 + \sigma_2)
  \,.
$$

## Related concepts

* [[direct product of groups]]

* [[free product of groups]]

* [[central product of groups]]


* [[semidirect product Lie algebra]]

* [[equivariant group]]

* [[crossed homomorphism]]

## References

A general survey is in

* Wikipedia, _[Semidirect product](http://en.wikipedia.org/wiki/Semi-direct_product)_

Lecture notes include

* Patrick Morandi, _Semidirect products_ ([pdf](http://sierra.nmsu.edu/morandi/notes/semidirect.pdf))

Relevant textbooks include

* [[R. Brown]], _Topology and groupoids_, Booksurge 2006.

* [[P. J. Higgins]] and J. Taylor,  _The Fundamental Groupoid and
  Homotopy Crossed Complex of an Orbit Space_, in K.H. Kamps et al., ed.,
   Category Theory: Proceedings Gummersbach 1981, Springer LNM
  962  (1982) 115--122.



[[!redirects semidirect product groups]]
