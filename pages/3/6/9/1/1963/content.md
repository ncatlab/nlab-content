
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Disambiguation

For derivations in [[logic]], see [[deduction]].


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

This identity is called the __[[Leibniz rule]]__; compare it to the product rule in ordinary calculus (first written down by [[Gottfried Leibniz]]). 


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

A special case is where $A$ is a [[group algebra]] $k G$ of a [[group]] $G$, and $N$ is a left $G$-module, regarded as a bimodule where the right action is trivial. Here a derivation is also called a 1-[[cocycle]], as used in [[group cohomology]]. 


### Graded derivations

A __graded derivation__ of degree $p$ on a [[graded object|graded]] algebra $A$ is a degree-$p$ graded-module homomorphism $d: A \to A$ such that
$$ d(a b) = d(a) b + (-1)^{p q} a d(b) $$
whenever $a$ is homogeneous of degree $q$.  (By default, the grade is usually $1$, or sometimes $-1$.)


### Augmented derivations

An __augmented derivation__ on an algebra $A$, augmented by an algebra homomorphism $\epsilon: A \to B$, is a module homomorphism $d: A \to B$ such that
$$ d(a b) = d(a) \epsilon(b) + \epsilon(a) d(b) .$$

If you think about it, you should be able to figure out the definition of an __augmented graded derivation__. 

+-- {: .num_prop} 
###### Proposition 
Let $k Alg$ denote the category of commutative $k$-algebras, and $k Alg/k$ the slice, i.e., the category of commutative $k$-algebras $A$ equipped with an augmentation $\epsilon: A \to k$. Then the functor 

$$Der: (k Alg/k)^{op} \to k Mod$$ 

which takes an augmented algebra to the module of augmented derivations $d: A \to k$ is represented by the augmented algebra $eval_0: k[x]/(x^2) \to k$. 
=-- 

+-- {: .proof} 
###### Proof 
Indeed, an algebra map $\delta: A \to k[x^2]/(x^2)$ which renders the triangle 

$$\array{ 
A & \stackrel{\delta}{\to} & k[x]/(x^2) \\ 
 & \mathllap{\epsilon} \searrow & \downarrow \mathrlap{eval_0} \\ 
 & & k
}$$ 

commutative may be uniquely written in the form $\delta(a) = \epsilon(a) + d(a)x$ for some $k$-module map $d: A \to k$, and then we have 

$$\array{ 
\epsilon(a b) + d(a b)x & = & \delta(a b) \\ 
 & = & \delta(a)\delta(b) \\ 
 & = & (\epsilon(a) + d(a)x)(\epsilon(b) + d(b)x) \\ 
 & = & \epsilon(a)\epsilon(b) + (\epsilon(a)d(b) + d(a)\epsilon(b))x + d(a)d(b) x^2 \\ 
 & = & \epsilon(a b) + (\epsilon(a)d(b) + d(a)\epsilon(b))x
}$$ 

and we conclude $d(a b) = \epsilon(a)d(b) + d(a)\epsilon(b)$, so that $d$ is an augmented derivation. Of course the calculation may be run in reverse, so that $\delta$ is an augmented algebra homomorphism precisely when $d$ is a derivation. 
=-- 


### Further variations

There are many further extensions, for examples derivations with values in an $A$-[[bimodule]] $M$ forming $Der_k(A,M) \subset Hom_k(A,M)$ (see also [[double derivation]]), skew-derivations in ring theory (with a twist in the Leibniz rule given by an endomorphism of a ring) and the dual notion of a [[coderivation]] of a coalgebra.  The latter plays role in Koszul-dual definitions of $A_\infty$-[[A-infinity-algebra|algebras]] and $L_\infty$-[[L-infinity-algebra|algebras]].  See also [[derivation on a group]], which uses a modified Leibniz rule: $d(a b) = d(a) + a d(b)$.


### Derivations on algebras over a dg-operad
 {#OfAlgebrasOverADGOperad}

More generally, there is a notion of derivation for every kind of [[algebra over an operad]] over a [[dg-operad]] (at least).

+-- {: .num_defn}
###### Definition

Let $\mathcal{O}$ be a [[dg-operad]] (a [[chain complex]]-enriched [[operad]]). For $A$ an $\mathcal{O}$-[[algebra over an operad]] and $N$ a [[module over an algebra over an operad|module over that algebra]] a **derivation** on $A$ with values in $N$ is a morphism

$$
  v : A \to N
$$

in the underlying category of [[graded vector space]]s, such that for each $n \gt 0$ we have a [[commuting diagram]]

$$
  \array{
     \mathcal{O}(n) \otimes A^{\otimes n}
     &\stackrel{}{\to}&
     A
     \\
     {}^{\mathllap{\sum_{a+b=n-1} id \otimes id^{\otimes a} \otimes v  \otimes id^{\otimes b}}}\downarrow 
     && \downarrow^{\mathrlap{v}}
     \\ 
     \oplus_{a+ b = n-1} \mathcal{O}(n) \otimes A^{\otimes a}
      \otimes N \otimes A^{\otimes b}
     &\to&
     N
  }
  \,,
$$

where the top horizontal morphism is that given by the $\mathcal{O}$-algebra structure of $A$ and the bottom that given by the $A$-module structure of $N$.

=--

This appears as ([Hinich, def. 7.2.1](#Hinich)).

The theory of [[tangent complex]]es, [[Kähler differential]]s, etc. exists in this generality for derivations on algebras over an operad. 

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

* Let $R[[x]]$ be a [[formal power series]] over a ring $R$. Then the [[formal derivative]] is a derivation. 

### Derivations with values in a bimodule

The standard example of a derivation not on an algebra, but with values in a [[bimodule]] is a restriction of the above case of the exterior differential acting on the [[deRham complex|deRham algebra]] of differential forms. Restricting this to 0-fomrs yields a morphism

$$
  d : C^\infty(X) \to \Omega^1(X)
$$ 

where $\Omega^1(X)$ is the space of 1-forms on $X$, regarded as a bimodule over the algebra of functions in the obvious way. 

A variation of this example is given by the [[Kähler differentials]]. These provide a **universal derivation** in some sense.

### Derivations of smooth functions

+-- {: .un_prop}
###### Proposition
Let $X$ be a [[smooth manifold]] and $C^\infty(X)$ its algebra of smooth functions. Then the morphism

$$
  Vect(X) \to Der(C^\infty(X))
$$

that sends a [[vector field]] $v$ to the derivation $v(-) : C^\infty(X) \to C^\infty(X)$ is a bijection.
=--

See also at _[[derivations of smooth functions are vector fields]]_.

+-- {: .proof}
###### Proof
This is true because $C^\infty(X)$ satisfies the [[Hadamard lemma]].

Since every smooth manifold is locally isomorphic to $\mathbb{R}^n$, it suffices to consider this case. By the [[Hadamard lemma]] every function $f \in C^\infty(\mathbb{R}^n)$ may be written as

$$
  f(x) = f(0) + \sum_i x_i g_i(x)
$$

for smooth $\{g_i \in C^\infty(X)\}$ with $g_i(0) = \frac{\partial f}{\partial x_i}(0)$. Since any derivation $\delta : C^\infty(X) \to C^\infty(X)$ satisfies the the Leibniz rule, it follows that

$$
  \delta(f)(0) = \sum_i \delta(x_i) \frac{\partial f}{\partial x_i}(0)
  \,.
$$

Similarly, by translation, at all other points. Therefore $\delta$ is already fixed by its action of the coordinate functions $\{x_i \in C^\infty(X)\}$. Let $v_\delta \in T \mathbb{R}^n$ be the [[vector field]] 

$$
  v_\delta \coloneqq \sum_i \delta(x_i) \frac{\partial}{\partial x_i}
$$

then it follows that $\delta$ is the derivation coming from $v_\delta$ under $Vect(X) \to Der(C^\infty(X))$.
=--

### Derivations of continuous functions {#DerOfContFuncts}

Let now $X$ be a [[topological space|topological]] [[manifold]] and $C(X)$ the algebra of continuous real-valued functions on $X$. 

+-- {: .un_prop}
###### Proposition
The derivations $\delta : C(X) \to C(X)$ are all trivial.
=--

+-- {: .proof}
###### Proof
Observe that generally every derivation vanishes on the function 1 that is constant on $1 \in \mathbb{R}$. Therefore it is sufficient to show that if $f \in C(X)$ vanishes at $x_0 \in X$ also $\delta(f)$ vanishes at $x_0$, because we may write every function $g$ as $(g  - g(x_0)) + g(x_0)$.

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

=--

## Related concepts

* [[operational tangent space]]

* [[p-derivation]]

* [[derivation Lie algebra]]


## References

Derivations on [[infinity-algebra over an (infinity,1)-operad|algebras]] over a [[dg-operad]] are discussed in section 7 of

* {#Hinich} [[Vladimir Hinich]],  _Homological algebra of homotopy algebras_ Communications in algebra, 25(10). 3291-3323 (1997)([arXiv:q-alg/9702015](http://arxiv.org/abs/q-alg/9702015), _Erratum_ ([arXiv:math/0309453](http://arxiv.org/abs/math/0309453)))
 
 


[[!redirects derivation]]
[[!redirects derivations]]
