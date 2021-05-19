+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

# $2$-pullbacks
* tic
{: toc}

An ordinary [[pullback]] is a [[limit]] over a [[diagram]] of the form $A \to C \leftarrow B$.  Accordingly, a __2-pullback__ (or **2-fiber product**) is a [[2-limit]] over such a diagram.


## Definition

Saying that "a 2-pullback is a 2-limit over a [[cospan]]" is in fact a sufficient definition, but we can simplify it and make it more explicit.

A __$2$-pullback__ in a [[2-category]] is a square
$$\array{P & \overset{p}{\to} &A \\
  ^q\downarrow & \cong & \downarrow^f\\
  B& \underset{g}{\to} &C }$$
which commutes up to [[isomorphism]], and which is universal among such squares in a 2-categorical sense.  This means that (1) given any other such square
$$\array{Z & \overset{v}{\to} &A \\
  ^w\downarrow & \cong & \downarrow^f\\
  B& \underset{g}{\to} &C }$$
which commutes up to isomorphism, there exists a morphism $u:Z\to P$ and isomorphisms $p u \cong v$ and $q u \cong w$ which are coherent with the given ones above, and (2) given any two morphisms $u,t:Z\to P$ and 2-cells $\alpha:p u \to p t$ and $\beta:q u \to q t$ such that $f \alpha = g \beta$ (modulo the given isomorphism $f p \cong g q$), there exists a unique 2-cell $\gamma:u\to t$ such that $p \gamma = \alpha$ and $q \gamma = \beta$.


## Equivalence of definitions

The simplification in the above explicit definition has to do with the omission of an unnecessary structure map.  Note that an ordinary pullback of $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ comes equipped with maps $P\overset{p}{\to} A$, $P\overset{q}{\to} B$, and $P\overset{r}{\to} C$, but since $r = f p$ and $r = g q$, the map $r$ is superfluous data and is usually omitted.  In the 2-categorical case, where identities are replaced by isomorphisms, it is, strictly speaking, different to give merely $p$ and $q$ with an isomorphism $f p \cong g q$, than to give $p$, $q$, and $r$ with isomorphisms $r \cong f p$ and $r \cong g q$.  However, when 2-limits are considered as only defined up to equivalence (as is the default on the nLab), the two resulting notions of "2-pullback" are the same.  In much of the 2-categorical literature, the version with $r$ specified would be called a __bipullback__ and the version with $r$ not specified would be called a __bi-iso-comma-object__.

The unsimplified definition would be: a __$2$-pullback__ in a [[2-category]] is a diagram
$$\array{P & \overset{p}{\to} &A \\
  ^q\downarrow & \searrow & \downarrow^f\\
  B& \underset{g}{\to} &C }$$
in which each triangle commutes up to [[isomorphism]], and which is universal among such squares in a 2-categorical sense.  This means that (1) given any other such square
$$\array{Z & \overset{r}{\to} &A \\
  ^s\downarrow & \searrow & \downarrow^f\\
  B& \underset{g}{\to} &C }$$
$$\array{Z & \overset{v}{\to} &A \\
  ^w\downarrow & \cong & \downarrow^f\\
  B& \underset{g}{\to} &C }$$
in which the triangles commute up to isomorphism, there exists a morphism $u\colon Z \to P$ and isomorphisms $p u \cong v$ and $q u \cong w$ which are coherent with the given ones above, and (2) given any two morphisms $u,t\colon Z \to P$ and 2-cells $\alpha\colon p u \to p t$ and $\beta\colon q u \to q t$ such that $f \alpha = g \beta$ (modulo the given isomorphism $f p \cong g q$), there exists a unique 2-cell $\gamma\colon u \to t$ such that $p \gamma = \alpha$ and $q \gamma = \beta$.

+--{.query}
Stephan: I would not write $f\alpha =g \beta$ since 1-cells are not composable with 2-cells.

_Toby_:  They are, through the operation of [[whiskering]].

Stephan: Thank you Toby. I inserted this example in [[horizontal composition]]
=--

To see that these definitions are equivalent, we observe that both assert the [[representable functor|representability]] of some [[2-functor]] (where "representability" is understood in the 2-categorical "up-to-equivalence" sense), and that the corresponding 2-functors are equivalent.

* In the simplified case, the functor $F_1\colon K^{op}\to Cat$ sends an object $Z$ to the category whose
  * objects are squares commuting up to isomorphism, i.e. maps $v\colon Z\to A$ and $w\colon Z\to B$ equipped with an isomorphism $\mu\colon f v \cong g w$, and whose 
  * morphisms from $(v,w,\mu)$ to $(v',w',\mu')$ are pairs $\phi\colon v\to v'$ and $\psi\colon w\to w'$ such that $\mu' . (f \phi) = (g \psi) . \mu$.
* In the unsimplified case, the functor $F_2\colon K^{op}\to Cat$ sends an object $Z$ to the category whose 
  * objects consist of maps $v\colon Z\to A$, $w\colon Z\to B$, and $x\colon Z\to C$ equipped with isomorphisms $\kappa\colon f v \cong x$ and $\lambda\colon x\cong g w$, and whose 
  * morphisms from $(v,w,x,\kappa,\lambda)$ to $(v',w',x',\kappa',\lambda')$ are triples $\phi\colon v\to v'$, $\psi\colon w\to w'$, and $\chi\colon x\to x'$ such that $\kappa' . (f \phi) = \chi . \kappa$ and $\lambda' . \chi = (g \psi) . \lambda$.

We have a canonical [[pseudonatural transformation]] $F_2\to F_1$ that forgets $x$ and sets $\mu = \lambda . \kappa$.  This is easily seen to be an [[equivalence]], so that any representing object for $F_1$ is also a representing object for $F_2$ and conversely.  (Note, though, that in order to define an inverse equivalence $F_1\to F_2$ we must choose whether to define $x = f v$ or $x = g w$.)


## Variations

2-pullbacks can also be identified with [[homotopy pullbacks]], when the latter are interpreted in $Cat$-enriched homotopy theory.


### Strict 2-pullbacks

If we are in a [[strict 2-category]] and all the coherence isomorphisms ($\mu$, $\kappa$, $\lambda$, etc.) are required to be identities, and $u$ in property (1) is required to be unique, then we obtain the notion of a **strict 2-pullback**.  This is an example of a [[strict 2-limit]].  Note that since we must have $x = f v = g w$, the two definitions above are still the same.  In fact, they are now even isomorphic (and determined up to isomorphism, rather than equivalence).

In literature where "2-limit" means "strict 2-limit," of course "2-pullback" means "strict 2-pullback."

Obviously not every 2-pullback is a strict 2-pullback, but also not every strict 2-pullback is a 2-pullback, although the latter is true if either $f$ or $g$ is an [[isofibration]] (and in particular if either is a [[Grothendieck fibration]]).  A strict 2-pullback is, in particular, an ordinary pullback in the underlying 1-category of our strict 2-category, but it has a stronger universal property than this, referring to 2-cells as well (namely, part (2) of the explicit definition).


### Strict weighted limits

If the coherence isomorphisms $\mu$, $\kappa$, $\lambda$ in the squares are retained, but in (1) the isomorphisms $p u \cong r$ and $q u \cong s$ are required to be identities and $u$ is required to be unique, then the simplified definition becomes that of a **strict iso-comma object**, while the unsimplified definition becomes that of a **strict pseudo-pullback**.  (Iso-comma objects are so named because if the isomorphisms in the squares are then replaced by mere morphisms, we obtain the notion of (strict) [[comma object]]).

Every strict iso-comma object, and every strict pseudo-pullback, is also a (non-strict) 2-pullback.  In particular, if strict iso-comma objects and strict pseudo-pullbacks both exist, they are equivalent, but they are *not* isomorphic.  (Note that their strict universal property determines them up to isomorphism, not just equivalence.)   In many strict 2-categories, such as [[Cat]], 2-pullbacks can naturally be constructed as either strict iso-comma objects or strict pseudo-pullbacks.


### Lax versions

Replacing the isomorphism $\mu$ in the simplified definition by a mere transformation results in a [[comma object]], while replacing $\kappa$ and $\lambda$ in the unsimplified definition by mere transformations results in a [[lax pullback]].  In a [[(2,1)-category]], any [[comma object]] or [[lax pullback]] is also a 2-pullback, but this is not true in a general 2-category.  Note that comma objects are often misleadingly called lax pullbacks.


[[!redirects 2-pullback]]
[[!redirects 2-pullbacks]]
[[!redirects 2-fiber product]]
[[!redirects 2-fiber products]]
[[!redirects bipullback]]
[[!redirects bipullbacks]]
[[!redirects bi-pullback]]
[[!redirects bi-pullbacks]]

[[!redirects bi-iso-comma-object]]
[[!redirects bi-iso-comma-objects]]
[[!redirects iso-comma-object]]
[[!redirects iso-comma-objects]]
[[!redirects strict iso-comma-object]]
[[!redirects strict iso-comma-objects]]
[[!redirects iso-comma object]]
[[!redirects iso-comma objects]]
[[!redirects strict iso-comma object]]
[[!redirects strict iso-comma objects]]

[[!redirects pseudopullback]]
[[!redirects pseudopullbacks]]
[[!redirects pseudo-pullback]]
[[!redirects pseudo-pullbacks]]
[[!redirects pseudo pullback]]
[[!redirects pseudo pullbacks]]

[[!redirects strict pseudopullback]]
[[!redirects strict pseudopullbacks]]
[[!redirects strict pseudo-pullback]]
[[!redirects strict pseudo-pullbacks]]
[[!redirects strict pseudo pullback]]
[[!redirects strict pseudo pullbacks]]
