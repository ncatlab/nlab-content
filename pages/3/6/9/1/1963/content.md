
#Contents#
* automatic table of contents goes here
{:toc}


## Definitions


### Derivations on an algebra

For $A$ an [[nonassociative algebra|algebra]] (over some [[ring]] $k$), a **derivation** on $A$ is a $k$-linear morphism

$$
  d : A \to A
$$

such that for all $a,b \in A$ we have

$$ 
  d(a b) = d(a) b + a d (b) 
  \,,
$$

This identity is called the __Leibniz rule__; compare it to the product rule in ordinary calculus (first written down by [[Gottfried Leibniz]]).


### Derivations with values in a bimodule

For $A$ an [[nonassociative algebra|algebra]] (over some [[ring]] $k$) and $N$ a [[bimodule]] over $A$, a **derivation** of $A$ with values in $N$ is a $k$-linear morphism

$$
  d : A \to N
$$

such that for all $a,b \in A$ we have

$$ 
  d(a b) = d(a) \cdot b + a \cdot d (b) 
  \,,
$$

where on the dot on the right-hand side denotes the right (first term) and left (second term) [[action]] of $A$ on the bimodule $N$. 

The previous definition is a special case of this one, where the bimodule is $N = A$, the algebra itself with its canonical left and right action on itself.


### Graded derivations

A __graded derivation__ of degree $p$ on a [[graded object|graded]] algebra $A$ is a degree-$p$ graded-module homomorphism $d: A \to A$ such that
$$ d(a b) = d(a) b + (-1)^{pq} a d(b) $$
whenever $a$ is homogeneous of degree $q$.  (By default, the grade is usually $1$, or sometimes $-1$.)


### Augmented derivations

An __augmented derivation__ on an algebra $A$, augmented by an algebra homomorphism $\epsilon: A \to B$, is a module homomorphism $d: A \to B$ such that
$$ d(a b) = d(a) \epsilon(b) + \epsilon(a) d(b) .$$

If you think about it, you should be able to figure out the definition of an __augmented graded derivation__.


### Further variations

There are many further extensions, for examples derivations with values in an $A$-[[bimodule]] $M$ forming $Der_k(A,M) \subset Hom_k(A,M)$ (see also [[double derivation]]), skew-derivations in ring theory (with a twist in the Leibniz rule given by an endomorphism of a ring) and the dual notion of a [[coderivation]] of a coalgebra.  The latter plays role in Koszul-dual definitions of $A_\infty$-[[A-infinity-algebra|algebras]] and $L_\infty$-[[L-infinity-algebra|algebras]].  See also [[derivation on a group]], which uses a modified Leibniz rule: $d(a b) = d(a) + a d(b)$.


### Generalization to arbitrary $(\infty,1)$-categories {#Infty1Version}

Another equivalent reformulation of the notion of derivations 
turns out to be useful for the [[vertical categorification]] of the concept:

for $N$ an $R$-module, there is the **nilpotent extension** ring $G(N) := N \oplus R$, equipped with the product operation

$$
  (r_1, n_1) \cdot (n_2, r_2) := (r_1, r_2, n_1 r_2 + n_2 r_1)
  \,.
$$ 

This comes with a [[natural transformation|natural]] morphism of rings

$$
 G(N) \to R
$$

given by sending the elements of $N$ to 0. One sees that a derivation on $R$ with values in $N$ is precisely a ring homomorphism $R \to G(N)$ that is a [[section]] of this morphism.

In terms of the [[bifibration]] $p : Mod \to Ring$ of [[module]]s over [[ring]]s, this is the same as a morphism from the module of [[Kähler differential]]s $\Omega_K(R)$ to $N$ in the fiber of $p$ over $R$.

While this is a trivial restatement of the universal property of [[Kähler differential]]s, it is this perspective that vastly generalizes:

we may replace $Mod \to Ring$ by the [[tangent (∞,1)-category]] projection $p : T_C \to C$ of any [[(∞,1)-category]] $C$. The functor that assigns [[Kähler differential]]s is then replaced by a [[left adjoint]] [[section]] of this projection 

$$
  \Omega : C \to T_C
  \,.
$$

An **$(\infty,1)$-derivation** on an object $R$ with coefficients in an object $N$ in the fiber of $T_C$ over $R$ is then defined to be morphism $\Omega(R) \to N$ in that fiber.

More discussion of this is at [[deformation theory]].


## Examples


### Derivations on an algebra

*  Let $A$ consist of the smooth real-valued functions on an [[interval]] in the [[real line]].  Then differentiation is a derivation; this is the motivating example.
*  Let $A$ consist of the [[holomorphic function|holomorphic functions]] on a region in the [[complex plane]].  Then differentiation is a derivation again.
*  Let $A$ consist of the [[meromorphic function|meromorphic functions]] on a region in the [[complex plane]].  Then differentiation is still a derivation.
*  Let $A$ consist of the smooth functions on a [[manifold]] (or [[generalized smooth space]]) $X$.  Then any [[tangent vector field]] on $X$ defines a derivation on $A$; indeed, this serves as one definition of tangent vector field.
*  Let $A$ consist of the [[germs]] of differentiable functions near a point $p$ in a smooth space $X$.  Then any [[tangent vector]] at $a$ on $X$ defines a derivation on $A$ augmented by evaluation at $a$; again, this serves to define tangent vectors.
*  Let $A$ consist of the smooth [[differential forms]] on a smooth space $X$.  Then [[exterior differentiation]] is a graded derivation (of degree $1$).
*  In any of the above examples containing the adjective 'smooth', replace it with $C^k$ and augment $A$ by the inclusion of $C^k$ into $C^{k-1}$.  Then we have an augmented derivation.

There should be some more clearly algebraic examples (other than obvious things like restricting the above to polynomials), but I don\'t know how to state them.


### Derivations with values in a bimodule

The standard example of a derivation not on an algebra, but with values in a [[bimodule]] is a restriction of the above case of the exterior differential acting on the [[deRham complex|deRham algebra]] of differential forms. Restricting this to 0-fomrs yields a morphism

$$
  d : C^\infty(X) \to \Omega^1(X)
$$ 

where $\Omega^1(X)$ is the space of 1-forms on $X$, regarded as a bimodule over the algebra of functions in the obvious way. 

A variation of this example is given by the [[Kähler differentials]]. These provide a **universal derivation** in some sense.

### Derivations of smooth functions

**Proposition** Let $X$ be a [[smooth manifold]] and $C^\infty(X)$ its algebra of smooth functions. Then the morphism

$$
  Vect(X) \to Der(C^\infty(X))
$$

that sends a [[vector field]] $v$ to the derivation $v(-) : C^\infty(X) \to C^\infty(X)$ is a bijection.

**Proof** This is true because $C^\infty(X)$ satisfies the [[Hadamard lemma]].

Since every smooth manifold is locally isomorphic $\mathbb{R}^n$, it suffices to consider this case. By the [[Hadamard lemma]] every function $f \in C^\infty(\mathbb{R}^n)$ may be written as

$$
  f(x) = f(0) + \sum_i x_i g_i(x)
$$

for smooth $\{g_i \in C^\infty(X)\}$ with $g_i(0) = \frac{\partial f}{\partial x_i}(0)$. Since any derivation $\delta : C^\infty(X) \to C^\infty(X)$ satisfiesthe the Leibniz rule, it follows that

$$
  \delta(f)(0) = \sum_i \delta(x_i) \frac{\partial f}{\partial x_i}(0)
  \,.
$$

Similarly, by translation, at all other points. Therefore $\delta$ is already fixed by its action of the coordinate functions $\{x_i \in C^\infty(X)\}$. Let $v_\delta \in T \mathbb{R}^n$ be the [[vector field]] 

$$
  v_\delta = = \sum_i \delta(x_i) \frac{\partial}{\partial x_i}
$$

then it follows that $\delta$ is the derivation coming from $v_\delta$ under $Vect(X) \to Der(C^\infty(X))$.

### Derivations of continuous functions {#DerOfContFuncts}

Let now $X$ be a [[topological space|topological]] [[manifold]] and $C(X)$ the algebra of continuous real-valued functions on $X$. 

**Proposition** The derivations $\delta : C(X) \to C(X)$ are all tivial.

**Proof** Observe that generally every derivation vanishes on the function 1 that is constant on $1 \in \mathbb{R}$. Therefore it is sufficient to show that if $f \in C(X)$ vanishes at $x_0 \in X$ also $\delta(f)$ vanishes att $x_0$, because we may write every function $g$ as $(g  - g(x_0)) + g(x_0)$.

So let $f \in C(X)$ with $f(x_0) = 0$. Then we may write $f$ as a product

$$
  f = g_1 g_2
$$

with 

$$
  g_1 = \sqrt{|f|}
$$

and

$$
  g_2 : x \mapsto 
  \left\{
   \array{
      f(x)/\sqrt{|f(x)|} & | f(x) \neq 0
      \\
      0 & | f(x) = 0
   }
  \right.
  \,.
$$

Notice that indeed both functions are continuous. (But even if $X$ is a smooth manifold and $f$ a smooth function, $g_1$ will in general not be smooth.)

But also both functions vanish at $x_0$. This implies that

$$
  \delta(f)(x_0) = \delta(g_1)(x_0) g_2(x_0) +
    g_1(x_0) \delta(g_2(x_0)) = 0
  \,.
$$



[[!redirects derivations]]
[[!redirects Leibniz rule]]
[[!redirects Leibniz identity]]