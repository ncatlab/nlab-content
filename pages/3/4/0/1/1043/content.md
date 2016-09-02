
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Yoneda lemma
+--{: .hide}
[[!include Yoneda lemma - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
Universal properties are commonly used in mathematics, often without mentioning the word "universal property".

For example, if one were asked to give a map $\mathbb{R} \to \mathbb{R} \times \mathbb{C}$, they might write down something like $x \mapsto (x^2, x + ix)$. In effect, what is done is that a pair of maps $\mathbb{R} \to \mathbb{R}$ and $\mathbb{R} \to \mathbb{C}$ is given, namely $(x \mapsto x^2, x \mapsto x + ix)$. The **universal property** of the [[product]] is says that giving a map to $A \times B$ is the same as giving a map to $A$ and a map to $B$, and moreover this correspondence is [[natural]] in some precise sense.

Similarly, if we have [[rings]] $R$ and $S$, if we want to extend a [[ring homomorphism]] $R \to S$ to a homomorphism from the [[polynomial ring]] $R[x] \to S$, all we have to do is to specify an element of $S$ that we send $x$ to. In other words, a homomorphism $R[x] \to S$ is the same as a homomorphism $R \to S$ and an element of $S$.

Note that in both cases, the bijections aren't "arbitrary". we have some sort of "naturality" or "coherence" conditions specified on the bijections. In the case of the product, we have projection maps $\pi_1: A \times B \to A$ and $\pi_2: A \times B \to B$, such that if we pair up two maps $f: X \to A$ and $g: X \to B$ to $(f, g): X \to A \times B$, then composing with the projections give $\pi_1 \circ (f, g) = f$ and $\pi_2 \circ (f, g) = g$. In the case of the polynomial ring, if we are given a map $f: R \to S$ and an element $a \in S$, the induced map $f_a: R[x] \to S$ *extends* the map $f$.

By the [[Yoneda lemma]], specifying how we can map in or out of an object uniquely determines the object up to [[isomorphism]]. So we can use these universal properties as *definitions* of the constructions! These are known as **universal constructions**. Of course, these definitions are not actually "constructions". We still have to do the concrete constructions the good, old way to show that there are objects satisfying the universal property (or apply general theorems such as the [[adjoint functor theorem]]).

## Example

### Concrete examples
We first look at a few concrete examples of universal properties. These are all special cases of the ones described below. Note that in general, the naturality of the bijection can be specified by requiring that the bijection is a [[natural isomorphism]] between certain functors. By the [[Yoneda lemma]], we can rewrite this as a factorization condition, which is how the universal properties are often presented.

+-- {: .num_example}
###### Example (products)
The [[product]] of two objects (eg. sets, groups, rings etc.) is specified by the property that maps $f: X \to A \times B$ biject naturally with pairs of maps $(f_1: X \to A, f_2: X \to B)$.

The naturality condition says that there are [[projection maps]] $\pi_1: A \times B \to A$ and $\pi_2: A \times B \to B$ such that the maps $f_1$ and $f_2$ can be obtained via composition with these maps. More precisely, we have
$$
  f_1 = \pi_1 \circ f,\; f_2 = \pi_2 \circ f.
$$
In light of the maps $\pi_1$ and $\pi_2$, instead of a bijection, it suffices to require that two maps $f_1: X \to A$ and $f_2: X \to B$ can always be combined uniquely to give a map $(f_1, f_2): X \to A \times B$, since the other direction of the bijection is automatic via composition with $\pi_1, \pi_2$.

Thus, the universal property can be stated as follows: $A \times B$ is a product of $A$ and $B$ if there exists maps $\pi_1: A \times B \to A$ and $\pi_2 A \times B \to B$ such that given any pair of maps $f_1: X \to A$ and $f_2: X \to B$, there is a unique map $(f_1, f_2): X \to A \times B$ such that the following diagram commutes:
$$
\array{
& & X & & \\
& ^\mathllap{f_1}\swarrow & \downarrow^\mathrlap{(f_1, f_2)} & \searrow^\mathrlap{f_2}\\
A & \underset{\pi_1}{\leftarrow} & A \times B & \underset{\pi_2}{\rightarrow} & N
}
$$
=--


+-- {: .num_example}
###### Example (free groups)
The [[free group|free]] [[group]] on $n$ generators is a group $F_n$ such that a [[group homomorphism]] $f: F_n \to G$ bijects (naturally) with $n$ elements of $G$ (not necessarily distinct). The naturality condition is that there are $n$ elements of $F_n$ such that the elements of $G$ picked out by $f$ are exactly the images of the $n$ elements of $F$.

As above, instead of requiring a bijection between group homomorphisms $F_n \to G$ and $n$ elements of $G$, it suffices to require that every $n$ elements of $G$ comes from a unique group homomorphism $F_n \to G$, since the other direction (homomorphism $\to$ $n$ elements) can be obtained by applying the homomorphism to the specified $n$ elements of $F_n$.

Diagrammatically, picking $n$ elements out of a set $X$ is the same as a [[function]] (of sets) $n \to X$. If we write $U(G)$ for the underlying set of the group $G$ (ie. $U$ is the [[forgetful functor]] to $Set$), the universal property of the free group says that there is a specified function $\phi: n \to U(F_n)$, such that for every function $f: n \to U(G)$, we can find a unique group homomorphism $\tilde{f}: F_n \to G$ such that the following diagram commutes:
$$
\array{
  U(F_n) & \overset{U(\tilde{f})}{\to} & U(G)\\
  ^\mathllap{\phi}\uparrow & \nearrow_{\mathrlap{f}}\\
  n
}
$$
In other words, every map $f: n \to U(G)$ factors through the universal map $\phi: n \to U(F_n)$ uniquely.
=--

+-- {: .num_example}
###### Example (tensor products)
The [[tensor product]] of [[vector spaces]] has the universal property that a [[bilinear map]] $V \times W \to U$ bijects naturally with linear maps $V \otimes W \to U$. The naturality condition is given by the existence of a universal bilinear map $\phi: V \times W \to V \otimes W$ such that every bilinear map $V \times W \to U$ factors through $\phi$ uniquely.
=--

We have more degenerate examples such as the terminal object:
+-- {: .num_example}
###### Example (terminal objects)
In the [[category of sets]], the singleton $1$ satisfies the property that there is always a unique from any object to $1$. So we can say that the maps $A \to 1$ biject (necessarily naturally) with the set $1$. More generally, in any category, if an object $X$ is such that there is always a unique map from any object to $X$, then $X$ is called the [[terminal object]].
=--

### Classes of examples
In general, the __universal constructions__ in [[category theory]] include

* [[representable functor]]

* [[adjoint functor]]

* [[limit]]/[[colimit]]

* [[end]]/[[coend]]

* [[Kan extension]]

* [[dependent sum]]/[[dependent product]]

Each of these may be defined by requiring it to satisfy a __universal property__. A universal property is a property of some construction which boils down to (is manifestly equivalent to) the property that an associated object is a universal initial object of some (auxiliary) category. 

In good cases, every single one of these is a special case of every other, so somehow one single concept here comes to us with many different faces. 

Some or all of these have analogs in [[higher category theory]], notably in [[2-category]] theory and [[(∞,1)-category theory]]:

* [[2-limit]]

* [[2-adjunction]]

* [[limit in a quasi-category]]

* [[adjoint (∞,1)-functor]]


[[!redirects universal construction]]
[[!redirects universal constructions]]
[[!redirects universal mapping]]
[[!redirects universal mappings]]

[[!redirects universal property]]
[[!redirects universal properties]]
[[!redirects universal mapping property]]
[[!redirects universal mapping properties]]
[[!redirects universal]]
