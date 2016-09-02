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

For it to be a universal property, just the existence of such a bijection is not sufficient. We will need some conditions to make sure the bijection is "natural". Abstractly, this says that the bijection is given by a [[natural isomorphism]] of certain [[functors]]. More concretely, by the [[Yoneda lemma]], this is equivalent to saying the bijection is "mediated" by some "universal maps", which is how universal properties are usually formulated. See [Concrete examples](#ConcreteExample) for more details.

Recall that by the [[Yoneda lemma]], specifying how we can map in or out of an object uniquely determines the object up to [[isomorphism]]. So we can use these universal properties as *definitions* of the constructions! These are known as **universal constructions**. Of course, these definitions are not actually "constructions". We still have to do the concrete constructions the good, old way to show that there are objects satisfying the universal property (or apply general theorems such as the [[adjoint functor theorem]]).

## Example

### Concrete examples {#ConcreteExample}
We first look at a few concrete examples of universal properties. These are all special cases of the ones described below.

+-- {: .num_example}
###### Example (products)
The [[product]] of two objects (eg. sets, groups, rings etc.) is specified by the property that maps $f: X \to A \times B$ biject naturally with pairs of maps $(f_1: X \to A, f_2: X \to B)$. Any object that 

The naturality condition is that if $f: X \to A \times B$ corresponds to $f_1: X \to A, f_2: X \to B$, and $g: Y \to X$ is a map, then $f \circ g$ corresponds to $f_1 \circ g$ and $f_2 \circ g$, so that the bijection respects composition.

In particular, the [[identity map]] $id: A \times B \to A \times B$ corresponds to a pair of [[projection maps]] $\pi_1: A \times B \to A$ and $\pi_2: A \times B \to B$. Then if $f: X \to A \times B$ is a map, then by naturality, it corresponds to $\pi_1 \circ f: X \to A$ and $\pi_2 \circ f: X \to B$.

Suppose we are not given a bijection, but just an object $P$ with maps $\pi_1: P \to A$ and $\pi_2: P \to B$. Then as above, we obtain a function from maps $X \to P$ to pairs of maps $X \to A, X \to B$ by composition. This makes $P$ into the product of $A$ and $B$ exactly when this function is a bijection, ie. for any pair of maps $f_1 : X \to A, f_2: X \to B$, there is a unique map $f: X \to P$ whose compositions with $\pi_1, \pi_2$ are $f_1, f_2$ respectively (naturality is easy to check).


(The experienced reader will notice that this is just a special case of the [[Yoneda lemma]])

Thus, the universal property can be stated as follows: $A \times B$ is a product of $A$ and $B$ if there exists maps $\pi_1: A \times B \to A$ and $\pi_2: A \times B \to B$ such that given any pair of maps $f_1: X \to A$ and $f_2: X \to B$, there is a unique map $f: X \to A \times B$ such that the following diagram commutes:
$$
\array{
& & X & & \\
& ^\mathllap{f_1}\swarrow & \downarrow^\mathrlap{f} & \searrow^\mathrlap{f_2}\\
A & \underset{\pi_1}{\leftarrow} & A \times B & \underset{\pi_2}{\rightarrow} & N
}
$$
=--

+-- {: .num_example}
###### Example (free groups)
The [[free group|free]] [[group]] on $n$ generators is a group $F_n$ such that [[group homomorphisms]] $F_n \to G$ bijects (naturally) with $n$ elements of $G$ (not necessarily distinct).

Similar to the above, the naturality condition says if $f: F_n \to G$ corresponds to $g_1, ..., g_n \in G$, and $h: G \to H$ is a map, then $h \circ f$ corresponds to the elements $h(g_1), ..., h(g_n)$. In particular, suppose the identity map $id: F_n \to F_n$ corresponds to $n$ elements $x_1, ..., x_n\in F_n$. Then any homomorphism $f: F_n \to G$ corresponds to the elements $f(x_1), ..., f(x_n)$ of $G$. 

Thus, given the specified elements $x_1, ..., x_n \in F_n$, the universal property says given any $n$ elements of $G$, we can find a unique homomorphism $f: F_n \to G$ that sends $x_1, ..., x_n$ to the $n$ elements.

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
###### Example (terminal and initial objects)
In the [[category of sets]], the singleton $1$ satisfies the property that there is always a unique from any object to $1$. So we can say that the maps $A \to 1$ biject (necessarily naturally) with the set $1$. More generally, in any category, if an object $X$ is such that there is always a unique map from any object to $X$, then $X$ is called the [[terminal object]].

Dually, an intial object is an object $0$ such that there is a unique map from $0$ to any object $X$.
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
