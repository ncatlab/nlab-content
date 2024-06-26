
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--


# Recursion
* table of contents
{: toc}

## Idea

The traditional notion of _recursion_ over the [[natural numbers]] $\mathbb{N}$ is a way of defining a [[function]] out of $\mathbb{N}$ by specifying the image of *[[zero|$0$]]* (the "initial value") along with a way to obtain each *[[successor|successive]]* value from the previous one(s).  
The study of functions on the [[natural numbers]] which can or cannot be defined using only recursion -- *[[recursive functions]]* -- is the topic of [[computability theory]] and has deep connections with the [[formal logic]] of [[Peano arithmetic]].

More generally, recursion is a way of defining a function on any mathematical object which is "defined [[induction|inductively]]" (in a way analogous to how the [[natural numbers]] are characterized by [[zero]] and [[successor]]).  In place of the "initial value" and "successor step", a general definition by recursion consists of giving one "clause" for each "constructor" of the inductively defined object.

Recursion is formalized in [[type theory]] by the notion of _[[inductive type]]_ (and the corresponding [[elimination rule]])  and, equivalently, in [[category theory]] by the notion of _[[initial algebra of an endofunctor]]_.  For $F$ an [[endofunctor]], a [[morphism]] of the form $F(X) \to X$ determines a collection of _constructors_ and the _recursion principle_ is the statement that there is a (unique) morphism $f : A \to X$ from the [[initial object|initial]] such structure $F(A) \to A$.  This $f$ is the corresponding _recursively defined function_.

Viewed from just a slightly different angle, this state of affairs is the _[[induction principle]]_ on non-[[dependent types]].




## Examples

+-- {: .un_example}
###### Example

In the theory of [[Peano arithmetic]], we define $x + y$ recursively in terms of the [[successor]] operation $s$ as follows:

1. $x + 0 = x$

2. $x + s(y) = s(x + y)$

The definition above is taken as an [[axiom]] in [[Peano arithmetic]]. 

More generally, given a (parametrizable) [[natural numbers object]] $\mathbb{N}$, its universal property guarantees that there is a unique (!) map $\mathbb{N} \times \mathbb{N} \to \mathbb{N}$ with the above properties.
=--


## Recursion theorem

### In general

+-- {: .num_theorem}
###### Theorem

Let $X$, $Y$, and $Z$ be [[set|sets]], and suppose $\rightsquigarrow$ is a [[well-founded relation]] on $X$. Let $h\colon X \times Y \times \mathcal{P}(Z) \to Z$ be a given function. Then, there is a unique function $f\colon X \to Z$ satisfying
$$f (x', y) = h (x', y, S)$$
for all $y$ in $Y$, where
$$S = \{ z \in Z : \exists x . \, ( x \rightsquigarrow x' \wedge z = f (x, y) ) \}$$
=--

+-- {: .proof}
###### Proof

By the principle of well-founded induction. (Details to be added.)
=--


### For a natural numbers object

+-- {: .num_theorem}
###### Theorem

Let $\mathbb{N}$ be a (parametrizable) [[natural numbers object]] in a [[cartesian monoidal category|category with finite products]], with zero $0\colon 1 \to \mathbb{N}$ and successor $s\colon \mathbb{N} \to \mathbb{N}$. For any morphisms $f_0\colon Y \to Z$ and $h\colon \mathbb{N} \times Y \times Z \to Z$, there is a unique morphism $f\colon \mathbb{N} \times Y \to Z$ such that
$$f(0, -) = f_0$$
and
$$f(s(x), y) = h(s(x), y, f(x, y))$$
where $x\colon \mathbb{N} \times Y \to \mathbb{N}$ is the first projection and $y\colon \mathbb{N} \times Y \to Y$ is the second projection.
=--

+-- {: .proof}
###### Proof

Recall that the universal property for $\mathbb{N}$ states that for data $g_0\colon Y \to A$, $k\colon Y \times A \to A$, there is a unique morphism $u\colon \mathbb{N} \times Y \to A$ such that $u \circ (0 \times \mathrm{id}_Y) = g_0$ and $u \circ (s \times \mathrm{id}_Y) = k \circ u$. We take $A = \mathbb{N} \times Z$, $g_0 = 0 \times f_0$, and $k(y, n, z) = \langle n, h(n, y, z) \rangle$, where $n\colon Y \times \mathbb{N} \times Z \to \mathbb{N}$, $y\colon Y \times \mathbb{N} \times Z \to Y$, and $z\colon Y \times \mathbb{N} \times Z \to Z$ are the obvious projections. The $f$ we seek is then obtained as $p_2 \circ u$, where $p_2 : \mathbb{N} \times Z \to Z$ is the second projection.
=--


## Related concepts

* [[recursive mathematics]]

* [[recursive function]]

* [[partial recursive function]], [[recursive subset]]

* [[guarded recursion]]

Dually, there is a notion of [[corecursion]] on a [[coinduction|coinductive structure]]. 

[[!include computable mathematics -- table]]


## References

See also:

* Wikipedia, *<a href="https://en.m.wikipedia.org/wiki/Recursion_(computer_science)">Recursion (computer science)</a>*

Discussion in [[type theory]]:

* [[Frank Pfenning]], *Recursive types*, Section 4.6 in:  *Linear Logic* (1998) &lbrack;[pdf](https://www.cs.cmu.edu/~fp/courses/98-linear/handouts/notes.pdf), [webpage](https://www.cs.cmu.edu/~fp/courses/98-linear/handouts.html), [[Pfenning-LinearLogic98.pdf:file]]&rbrack;

and in view of [[homotopy type theory]]:

* [[Univalent Foundations Project]], §1.10 *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;


[[!redirects recursion]]
[[!redirects recursive]]
[[!redirects recursive definition]]
[[!redirects recursive definitions]]

[[!redirects recursion principle]]
