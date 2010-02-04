
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Grothendieck's [[Galois theory]] was constructed in order to define for [[scheme]]s an analogue of the familiar correspondence

: [[covering space]]s of $X$ : $\pi_1(X)$[[action|-sets]]

for a [[locally path-connected space|locally path connected]], [[semi-locally simply connected space|semilocally simply connected]] [[topological space]] $X$. 

The objects on the left are not difficult to define for schemes (at least naively -- one really needs trivialisations over &#233;tale [[coverage|covers]]), but it may not be entirely immediate what the [[fundamental group]] defined in terms of loops should be.

The reason Galois's name is attached to this theory is that in the case of the scheme $Spec(k)$, the objects corresponding to the covering spaces are simply [[field extension]]s $Spec(k')$. The fundamental group of schemes defined in this way is the [[algebraic fundamental group]], and is a [[profinite group]].

The basic idea of Grothendieck's Galois theory may be extended to objects in an [[topos]] and then to objects in any [[(∞,1)-topos]]. For more on this see [[homotopy group of an ∞-stack]].

## Details

### Preliminaries

+-- {: .un_defn}
###### Definition
Given an arrow $f:x \to y$ in a category $C$ the _category of arrows compatible with $f$_, denoted $Comp(f)$ is the full [[subcategory]] of the [[undercategory]] $x \downarrow C$ on the arrows that [[coequalizer|coequalize]] the same pairs $g,h:w\rightrightarrows x$ that $f$ does.
=--

+-- {: .un_defn}
###### Definition
An arrow $f:x\to y$ in a category $C$ is a _[[strict epimorphism]]_ if it is [[initial object|initial]] in $Comp(f)$.
=--

It is not obvious, but a strict epimorphism is an epimorphism.

### Grothendieck's axioms

In what follows, Let $C$ be a [[category]] and $F:C \to Set$ a [[functor]]. The axioms presented here are as in

* [[Eduardo Dubuc]] and C. S. de la Vega _On the Galois theory on Grothendieck_, Bol. Acad. Nac. Cienc. (Cordoba) **65** (2000) 111--136. [arXiv](http://arxiv.org/abs/math.CT/0009145)

Some terminology: $X\in C$ is called _finite_ if $F(X)$ is a finite [[set]]. Let $\int_F C$ denote the [[category of elements]] of $F$, in which an object $(X,a)$ is called finite if $X$ is finite.

* **G0)** The full subcategory of $\int_F C$ on the finite objects is [[cofinal subcategory|cofinal]].

* **G1)** $C$ has all finite [[limit]]s

* **G2)** $C$ has an [[initial object]], finite [[coproduct]]s and [[quotient object|quotients]] by finite [[group]]s

* **G3)** Given $f:x\to z$ in $C$ there is a factorisation $x \stackrel{e}{\to} y \stackrel{i}{\to} z$ where $e$ is a strict epimorphism and $i$ is a mono. Also, $y$ is assumed to be a [[direct sum]]mand of $z$.

* **G4)** $F$ preserves finite limits

* **G5)** $F$ preserves initial object, finite sums, quotients by finite group actions and sends strict epimorphisms to surjections

* **G6)** $F$ reflects isomorphisms

***

It follows from the axioms that $F$ is a [[pro-representable functor]]. The [[automorphism group]] of the [[pro-object]] $P$ representing $F$ is (should be. I'm not familiar enough with pro-objects) a [[profinite group]] $\pi$. This acts on $F(X) = [P,-]$ by precomposition (talking out of my depth here -- it's getting a bit vague) and so $F$ lifts to a functor to $\pi-Set$, and Grothendieck's result is that this functor is an [[equivalence of categories]].

There are several modifications one can make the above. In the case that $C$ is the category of covering spaces of a nice enough space, the functor $F$ is [[representable functor|representable]] by the [[universal covering space]], and so there is a 'representable' version of the above, not needing to utilise profinite groups. One can also consider just the connected-objects version, and end up with an equivalence to the category of _transitive_ $\pi$-sets.


## References

* [[Eduardo Dubuc]] and C. S. de la Vega _On the Galois theory on Grothendieck_, Bol. Acad. Nac. Cienc. (Cordoba) **65** (2000) 111--136. [arXiv](http://arxiv.org/abs/math.CT/0009145)


The constructon for general [[topos]]es is described in section 8.4 of

* [[Peter Johnstone]], _Topos theory_ , Academic Press (1977)


[[!redirects Grothendieck Galois theory]]
[[!redirects Grothendieck's Galois theory]]
[[!redirects Grothendieck-Galois theory]]
[[!redirects Grothendieck?Galois theory]]
[[!redirects Grothendieck--Galois theory]]