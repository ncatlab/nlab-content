
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition
 {#Definition}

An **involution** is an [[endomorphism]] $\sigma$ whose [[composition]] with itself is the [[identity morphism]]:

\[
  \label{InvolutiveProperty}
  \sigma \circ \sigma \;=\; id
  \,.
\]

Such an endomorphism is necessarily an [[automorphism]], being its own [[inverse morphism|inverse]].

On [[algebras]] and other [[mathematical structures]] where this makes sense, an __anti-involution__ is an [[anti-homomorphism]] satisfying (eq:InvolutiveProperty), instead of a [[homomorphism]] (hence an anti-[[endomorphism]] and necessarily an anti-[[automorphism]]). 

An [[associative algebra]] equipped with an anti-involution is called a *[[star-algebra]]*.


## Properties

### Commuting involutions

Two involutions $f, g \colon X \to X$ [[commutative diagram|commute]] if and only if their [[composition]] $f g$ is also an involution, as shown by the following manipulations:

$$
  \begin{aligned}
  f g 
   \;=\; 
  g f 
  &\;\;\;\;\;\implies\;\;\;\;\; 
  (f g) (f g) 
    \;=\; 
  (f g) (g f) 
    \;=\; 
  f (g g) f 
    \;=\; 
  f f 
   \;=\; 
  id
  \\
  (f g) (f g) 
    \;=\; 
  id
  &\;\;\;\;\;\implies\;\;\;\;\; 
  f g 
    \;=\; 
  f 
  \big(
     (f g) (f g)
  \big) 
  g 
    \;=\; 
  (f f) (g f) (g g) 
    \;=\; 
  g f
  \,.
  \end{aligned}
$$


### Fixed point free involutions

In [[combinatorics]], an important class of involutions are the [[fixed point]] free ones: an arbitrary involution on a [[finite set]] of cardinality $n$ may be specified by the choice of $k$ elements which are fixed together with a fixed point free involution on the remaining $(n-k)$.  The number of fixed point free involutions on a set of $2n$ labelled elements is counted by the double factorial $(2n-1)!! = (2n-1)\cdot (2n-3)\cdot\dots\cdot 3\cdot 1 = \frac{(2n)!}{2^n n!}$, while arbitrary involutions on a set of $n$ labelled elements are counted by OEIS sequence [A000085](https://oeis.org/A000085), which also counts the number of [[Young tableaux]] with $n$ cells.

### Monad of involutions
 {#MonadOfInvolutions}

An involution on a set $X$ is the same thing as an [[action]] of $\mathbb{Z}/2\mathbb{Z}$ on $X$.

More generally, let $(C,\otimes,1)$ be a [[monoidal category]] with [[distributive monoidal category|distributive]] finite [[coproducts]]. The object $2 = 1 + 1$ is equipped with an involution
$$
not : 2 \to 2
$$
defined as the [[copairing]] $not = [inr,inl]$ of the right and left injections.
Moreover, 2 can be given the structure of a [[monoid]] in $C$, with unit and multiplication
$$false : 1 \to 2 \qquad xor : 2 \otimes 2 \to 2$$
defined by $false = inl$ and $xor = [id,not]$ (here we make use of the isomorphism $2 \otimes 2 \cong 2 + 2$ to define $xor$ by copairing). The mapping
$$
X \mapsto 2 \otimes X \cong X + X
$$
thus extends to a [[monad]] on $C$, sending any object $X$ to the free object equipped with an involution over $X$. Explicitly, the unit $\eta_X : X \to 2\otimes X$ and the multiplication $\mu_X : 2\otimes 2\otimes X \to 2\otimes X$ of the monad are defined by tensoring the unit and the multiplication of the monoid with the identity on $X$, while the involution on $2 \otimes X$ is likewise defined by tensoring the involution on 2 with the identity on $X$.

We then have that involutions in $C$ are precisely the [[module over a monad|algebras]] of the monad $(2\otimes-,false\otimes-,xor\otimes-)$. In the forward direction, given an involution $f : X \to X$, we define a monad algebra structure $\alpha : 2\otimes X \to X$ on $X$ by $\alpha = [id,f]$ (again using the isomorphism $2\otimes X \cong X+X$). Conversely, given a monad algebra $\alpha : 2\otimes X \to X$, we can define an endomorphism $f : X \to X$ by $f = \alpha \circ inr$. The monad algebra laws imply that
$$\alpha \circ inr \circ \alpha \circ inr = \alpha \circ (2\otimes \alpha) \circ (2\otimes inr) \circ inr = \alpha \circ (xor\otimes id) \circ (2\otimes inr) \circ inr$$
and since $xor$ is defined such that $(xor\otimes id) \circ (2\otimes inr) \circ inr = id$, we derive that $\alpha \circ inr$ is an involution.



## Related concepts


* [[star-algebra]]

* [[dagger category]]

* [[duality]]

* [[involutive Hopf algebra]]

* [[complex conjugation]]

* [[idempotent]]


## References

* Philippe Flajolet and Robert Sedgewick, _Analytic Combinatorics_, CUP, 2009. ([author pdf](http://algo.inria.fr/flajolet/Publications/book.pdf))

[[!redirects involution]]
[[!redirects involutions]]

[[!redirects antiinvolution]]
[[!redirects antiinvolutions]]
[[!redirects anti-involution]]
[[!redirects anti-involutions]]
