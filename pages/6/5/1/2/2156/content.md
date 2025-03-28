

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
=--
=--


# Inner product spaces
* table of contents
{: toc}

## Idea

An _inner product_ on a [[vector space]] $V$ (also "scalar product" in the sense of: with values in "[[scalars]]", namely in the [[ground field]] $\mathbb{K}$) is a pairing $\langle\text{-},\text{-}\rangle$ of [[vectors]] to [[scalars]]
$$
  v_1,\, v_2
  \,\in\,
  V
  \;\;\;\;\;\;\;\;\;
    \vdash
  \;\;\;\;\;\;\;\;\;
  \langle v_1,\, v_2 \rangle
  \,\in\,
  \mathbb{K}
$$
which is  [[bilinear form|bilinear]] *or rather* -- namely if $\mathbb{K}$ is understood with a [[star-algebra|star]]-[[involution]] (such as the [[complex numbers]] under [[complex conjugation]]) -- [[sesquilinear form|sesquilinear]], in which case one also speaks of a *[[Hermitian inner product]]*, for definiteness.

Often one requires such a pairing to be non-degenerate or even [[positive-definite]] in order to qualify as an inner product, standard conventions depend on context.

For example, the ([[Hermitian inner product|Hermitian]]) inner product on a [[Hilbert space]] is required to be positive definite, as is that on [[tangent spaces]] in [[Riemannian geometry]], but the inner product on [[tangent spaces]] in [[pseudo-Riemannian geometry]] is only required to be non-degenerate. 

The group of [[automorphisms]] of an inner product space is the [[orthogonal group of an inner product space]].


## Definitions

Let $V$ be a [[vector space]] over the [[field]] (or more generally a [[ring]]) $\mathbb{K}$.  Suppose that $\mathbb{K}$ is equipped with an [[involution]] $r \mapsto \overline{r}$, called _conjugation_; in many examples, this will simply be the [[identity function]], but not always (for the [[complex numbers]] one typically consider the involution by [[complex conjugation]]).  

Then a ([[Hermitian inner product|Hermitian]]) _inner product_ on $V$ is a function
$$ 
  \langle\text{-},\, \text{-}\rangle
  \;\colon\;
  V \times V \to k 
$$
that is (1--3) _sesquilinear_ (or _bilinear_ when the involution is the identity) and (4) _conjugate-symmetric_ (or _symmetric_ when the involution is the identity).  That is:

1.  $ \langle 0, x \rangle = 0 $ and $ \langle x, 0 \rangle = 0 $;
2.  $ \langle x + y, z \rangle = \langle x, z \rangle + \langle y, z \rangle $ and $ \langle x, y + z \rangle = \langle x, y \rangle + \langle x, z \rangle $;
3.  $ \langle c x, y \rangle = \bar{c} \langle x, y \rangle $ and 
$\langle x, c y \rangle = \langle x, y \rangle c$;
4.  $ \langle x, y \rangle = \overline{\langle y, x \rangle} $.

Here we use the _physicist\'s convention_ that the inner product is antilinear (= conjugate-linear) in the first variable rather than in the second, rather than the _mathematician\'s convention_, which is the reverse.   

Note that we use the same ring as values of the inner product as for [[scalars]], and that $\langle x, c y \rangle = \langle x, y \rangle c$ is written with $c$ on the right for the case that we deal with noncommutative division ring.

+-- {: .query}
Are the two conventions really equivalent when $k$ is noncommutative?  &#8212;Toby
=--

(The axiom list above is rather redundant.  First of all, (1) follows from (3) by setting $c = 0$; besides that, (1--3) come in pairs, only one of which is needed, since each half follows from the other using (4).  It is even possible to derive (3) from (2) under some circumstances.)

An __inner product space__ is simply a vector space equipped with an inner product.


We define a function ${\|{-}\|^2}\colon V \to k$ by ${\|x\|^2} = \langle x, x \rangle$; this is called the __norm__ of $x$.  As the notation suggests, it is common to take the norm of $x$ to be the square root of this expression in contexts where that makes sense, but for us ${\|{-}\|^2}$ is an atomic symbol.  The norm of $x$ is __real__ in that it equals its own conjugate, by (4).


## Definiteness
   {#definite}

Notice that, by (1), $\langle 0, y \rangle = 0$ for all $y$.  In fact, the [[subset]] $\{ x \;|\; \forall y,\; \langle x, y \rangle = 0 \}$ is a [[linear subspace]] of $V$.  Of course, we also have ${\|0\|^2} = 0$, but $\{ x \;|\; {\|x\|^2} = 0 \}$ may not be a subspace.  These observations motivate some possible conditions on the inner product:

*  The inner product is __semidefinite__ if $\{ x \;|\; {\|x\|^2} = 0 \}$ *is* closed under addition (and hence is a subspace); it\'s __indefinite__ if there are $x$ and $y$ with ${\|x\|^2} = 0$ and ${\|y\|^2} = 0$ but ${\|x + y\|^2} \ne 0$.
*  The inner product is __nondegenerate__ if $x = 0$ whenever $\langle x, y \rangle = 0$ for all $y$; it\'s __degenerate__ if there is $x$ with $x \ne 0$ but $\langle x, y \rangle = 0$ for all $y$.
*  The inner product is __definite__ if $x = 0$ whenever ${\|x\|^2} = 0$; there ought to be a term for the condition that there is some $x \ne 0$ with ${\|x\|^2} = 0$, so let\'s call it __nondefinite__.

(In [[constructive mathematics]], we usually want an [[inequality relation]] relative to which the vector-space operations and the inner product are [[strongly extensional function|strongly extensional]], to make sense of the conditions with $\ne$ in them.  We can also use [[contrapositives]] to put $\ne$ in the other conditions, which makes them stronger if the inequality relation is [[tight relation|tight]].)

An inner product is definite iff it\'s both semidefinite and nondegenerate.  Semidefinite inner products behave very much like definite ones; you can mod out by the elements with norm $0$ to get a [[quotient vector space|quotient space]] with a definite inner product.  In a similar way, every inner product space has a nondegenerate quotient.


Now suppose that $k$ is equipped with a [[partial order]].  (Note that the [[complex numbers]] are standardly so equipped, with $a \leq b$ iff $b - a$ is a nonnegative real.)  Then we can consider other conditions on the inner product:

*  The inner product is __positive semidefinite__, or simply __positive__, if ${\|x\|^2} \geq 0$ always.
*  The inner product is __positive definite__ if it is both positive and definite, in other words if ${\|x\|^2} \gt 0$ whenever $x \ne 0$.
*  The inner product is __negative semidefinite__, or simply __negative__, if ${\|x\|^2} \leq 0$ always.
*  The inner product is __negative definite__ if it is both negative and definite, in other words if ${\|x\|^2} \lt 0$ whenever $x \ne 0$.

In this case, we have these theorems:

*  A positive or negative inner product really is semidefinite (as the terminology implies).
*  Conversely, a semidefinite inner product is either positive or negative, at least if we use [[classical logic]].  (In [[constructive mathematics]], we can say that a semidefinite inner product is either positive or negative, indeed is positive [[xor]] negative, as long as it is nonzero in the sense that at least some $\lang{x,y}\rang$ is [[apart]] from zero.  And of course, the zero inner product is the only one that is both positive and negative.)
*  Hence, a definite inner product is either positive or negative definite.  (We can strengthen this to 'xor' and state it constructively if we assume that $V$ is nonzero in that there exists $x$ with $x \ne 0$.)
*  Conversely, an inner product is indefinite if and only if some norms are positive and some are negative.  (No constructive caveats here!)

Negative (semi)definite inner products behave very much like positive (semi)definite ones; you can turn one into the other by multiplying all inner products by $-1$.


The study of positive definite inner product spaces (hence essentially of all semidefinite inner product spaces over partially ordered fields) is essentially the study of [[Hilbert spaces]].  (For Hilbert spaces, one usually uses a [[topological field]], typically $\mathbb{C}$, and requires a completeness condition, but this does not effect the algebraic properties much.)  The study of indefinite inner product spaces is very different; see the [English Wikipedia article](http://secure.wikimedia.org/wikipedia/en/wiki/Krein_space) on [[Krein space]]s for some of it.


All of this definiteness terminology may now be applied to an *[[linear operator|operator]]* $T$ on $V$, since $(x, y) \mapsto \langle{x, T y}\rangle$ is another inner product (on $\dom T$, if necessary).  See [[positive operator]].


## Examples

* [[Euclidean space]];

* [[Hilbert spaces]] (over $\mathbb{C}$), for example $\mathbb{C}^n$;

* Finite-dimensional modules over $\mathbb{H}$, the [[quaternions]].

* [[semisimple Lie algebras]] with the negative of the [[Killing form]] are positive-definite inner product spaces.

* [[inner product abelian groups]]

## Related concepts

* [[orthogonal structure]]

* [[self-dual object]]

* [[inner product of vector bundles]]

* [[bra-ket]]

## References

Original discussion of [[Hermitian inner products]] in the context of defining [[Hilbert spaces]] (as mathematical foundations of [[quantum mechanics]]):

* {#vonNeumann30} [[John von Neumann]], p. 64 in: *Allgemeine Eigenwerttheorie Hermitescher Funktionaloperatoren*, Math. Ann. **102** (1930) 49–131 &lbrack;[doi:10.1007/BF01782338](https://doi.org/10.1007/BF01782338)&rbrack;

* [[John von Neumann]]:

  p. 21 in: *Mathematische Grundlagen der Quantenmechanik*, Springer (1932, 1971) &lbrack;[doi:10.1007/978-3-642-96048-2](https://link.springer.com/book/10.1007/978-3-642-96048-2)&rbrack;

  pp. 38 in: *Mathematical Foundations of Quantum Mechanics* Princeton University Press (1955) &lbrack;[doi:10.1515/9781400889921](https://doi.org/10.1515/9781400889921), [Wikipedia entry](https://en.wikipedia.org/wiki/Mathematical_Foundations_of_Quantum_Mechanics)&rbrack;

Textbook accounts in the context of [[operator algebra]]:

* [[Richard V. Kadison]], [[John R. Ringrose]], §2.1 in: *Fundamentals of the theory of operator algebras* Vol I *Elementary Theory*, Graduate Studies in Mathematics **15**, AMS (1997) &lbrack;[ISBN:978-0-8218-0819-1](https://bookstore.ams.org/gsm-15)&rbrack;

* [[Bruce Blackadar]], §I.1.1 in: *Operator Algebras -- Theory of $C^\ast$-Algebras and von Neumann Algebras*, Encyclopaedia of Mathematical Sciences **122**, Springer (2006) &lbrack;[doi:10.1007/3-540-28517-2](https://doi.org/10.1007/3-540-28517-2)&rbrack;

Discussion of plain inner products (without star-involution) in terms of [[self-dual objects]] in suitable [[symmetric monoidal category|symmetric]] [[monoidal categories]]:

* {#Selinger12} [[Peter Selinger]], _Autonomous categories in which $A \simeq A^\ast$_, talk at QPL 2012 ([[SelingerSelfDual.pdf:file]])
 

[[!redirects inner product]]
[[!redirects inner products]]
[[!redirects inner product space]]
[[!redirects inner product spaces]]

[[!redirects scalar product]]
[[!redirects scalar products]]

[[!redirects dot product]]
[[!redirects dot products]]


