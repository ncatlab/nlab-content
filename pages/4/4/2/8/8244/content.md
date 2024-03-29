
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

# $C^*$-coalgebras
* table of contents
{: toc}

## Idea

$C^*$-coalgebras are like $C^*$-[[C-star-algebra|algebras]], but [[coalgebras]].  Their [[dual vector space|duals]] are $W^*$-[[W-star-algebra|algebras]].


## Definition

Let $A$ be a [[Banach *-coalgebra]] over the [[ground field]] $K$.  Let $\lambda\colon A \to K$ be a [[bounded linear functional]] on $A$, and let $\lambda^*$ be the composite
$$ A \overset{*}\to A \overset{\lambda}\to K \overset{\bar{}}\to K $$
(where $\bar{}$ is [[complex conjugation]], trivial if $K$ is [[real field|real]]); although some of the maps in this composite may be only [[antilinear map|antilinear]], the composite $\lambda^*$ is linear (over all of $K$).  Now consider the composite
\[ (\lambda {\displaystyle\hat{\otimes}_\pi} \lambda^*) \circ \Delta\colon A \to K {\displaystyle\hat{\otimes}_\pi} K \cong K ;\label{Cstarfunctional} \]
since $\Delta$ and $*$ are short, the norm of this functional is at most ${\|\lambda\|^2}$.

$A$ is a __$C^*$-coalgebra__ if the norm of the map in \eqref{Cstarfunctional} is exactly ${\|\lambda\|^2}$, for every bounded linear functional $\lambda$.

Although there is an asymmetry in \eqref{Cstarfunctional} (in the relative placement of $\lambda$ and $\lambda^*$), if we start with $\lambda^*$ instead of $\lambda$, we see that the [[universal quantification|universally quantified]] definition of $C^*$-coalgebra is symmetric.


## Justification

If we take the formal dual of everything in the definition above, then $A$ becomes a [[Banach *-algebra]] and $\lambda\colon K \to A$ becomes (multiplication of scalars by) an element $x$ of $A$.  The formal dual of the composite \eqref{Cstarfunctional} is (multiplication of scalars by) the element $x^* x$.  The requirement that the norm of this be exactly the square of the norm of $x$ is the $B^*$-identity that defines a $C^*$-[[C-star-algebra|algebra]].

So the definition of $C^*$-coalgebra dualises *everything* in the definition of $C^*$-algebra, down to using [[coelement]]s (in this case linear functionals) instead of [[elements]].


## Dual $W^*$-algebras

In general, the [[dual in a closed category|dual]] of a [[coalgebra]] is an [[algebra]], in any [[closed monoidal category]].  In particular, the [[dual vector space|dual]] of a [[Banach coalgebra]] is a [[Banach algebra]].  The involution $*$ gets along with this just fine; the dual of a [[Banach *-coalgebra]] is a [[Banach *-algebra]].  Finally, the linear functional in \eqref{Cstarfunctional} becomes the element in the $B^*$-identity for the dual, so the dual of a $C^*$-coalgebra is a $C^*$-[[C-star-algebra|algebra]].

But we have more!  If $A$ is a $C^*$-coalgebra, then (as we\'ve just seen) $A^*$ is a $C^*$-algebra; but since $A^*$ has a [[predual]] $A$, this means that $A^*$ is actually a $W^*$-[[W-star-algebra|algebra]] as well.

+-- {: .standout}
Which $W^*$-algebras arise in this way?
=--


## Examples (and non-examples)

The [[sequence space]] $l^1$ is a $C^*$-coalgebra, whose dual $W^*$-algebra is the sequence space $l^\infty$.  (For details of the comultiplication on $l^1$, see the examples in [[Banach coalgebra]].)

Although $l^\infty$ is a Banach coalgebra (under 'coconvolution'), it is *not* a $C^*$-coalgebra (at least not under coconvolution).

+-- {: .query}
(YC) Moreover, the TVS-isomorphism class of the predual of a $W^*$-algebra is very restricted (let alone its isomorphism class in Bang). In particular $\ell^\infty$ doesn't have a snowball's chance in Texas of being a $C^*$-coalgebra under any kind of choice of comultiplication, because it's the wrong kind of Banach space.)
=--


Although the dual of the [[Lebesgue space]] $L^1$ (on the [[real line]] $\mathbb{R}$ with [[Lebesgue measure]]) is the $W^*$-algebra $L^\infty$, $L^1$ is *not* a $C^*$-coalgebra, nor even a Banach coalgebra (at least not in the obvious way).  Essentially, this is because the [[diagonal subset|diagonal]] in $\mathbb{R}^2$ has [[null set|measure zero]] (so $\Delta$ takes an element of $L^1(\mathbb{R})$, interpreted as an [[absolutely continuous measure]] on $\mathbb{R}$, to a measure on $\mathbb{R} \times \mathbb{R}$ that is *not* absolutely continuous and so cannot be reinterpreted as an element of $L^1(\mathbb{R} \times \mathbb{R}) \cong L^1(\mathbb{R}) {\displaystyle\hat{\otimes}_\pi} L^1(\mathbb{R})$).


[[!redirects C-star coalgebra]]
[[!redirects C-star coalgebras]]
[[!redirects C-star-coalgebra]]
[[!redirects C-star-coalgebras]]
[[!redirects C* coalgebra]]
[[!redirects C* coalgebras]]
[[!redirects C*-coalgebra]]
[[!redirects C*-coalgebras]]
[[!redirects C-star cogebra]]
[[!redirects C-star cogebras]]
[[!redirects C-star-cogebra]]
[[!redirects C-star-cogebras]]
[[!redirects C* cogebra]]
[[!redirects C* cogebras]]
[[!redirects C*-cogebra]]
[[!redirects C*-cogebras]]
