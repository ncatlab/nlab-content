> For the concept in [[category theory]] see _[[exponential morphism]]_.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



# Exponential maps
* table of contents
{: toc}

## Idea

The exponential [[function]] of classical [[analysis]] given by the [[series]],
\[ \label{series} \exp x \coloneqq \sum_{i = 0}^{\infty} \frac{x^i}{i!} ,\]
is the solution of the [[differential equation]]
$$ f' = f $$
with initial value $f(0) = 1$.

It is also the limit of the following [[sequence]] of [[polynomial functions]]

$$f_n(x) \coloneqq \left(1 + \frac{x}{n}\right)^n$$

$$\exp x \coloneqq \lim_{n \to \infty} f_n(x)$$

This classical function is defined on the [[real line]] (or the [[complex plane]]).  To generalise it to other [[manifolds]], we need two things:

*  by its nature, the argument of the function should be a [[tangent vector]]; so in the classical function $\mathbb{R} \to \mathbb{R}$, the [[source]] $\mathbb{R}$ is really the [[tangent space]] to the [[target]] $\mathbb{R}$ at the point $\exp 0 = 1$.
*  We need a [[covariant derivative]] to tell us what $f'$ means.

So in the end we have, for any [[point]] $p$ on a [[differentiable manifold]] $M$ with an [[affine connection]] $\Del$, a map $\exp_p\colon T_p M \to M$, which is defined at least on a [[neighbourhood]] of $0$ in the [[tangent space]] $T_p M$.

Note that $p$ here comes from the initial value $\exp_p 0 = p$; we usually take $p = 1$ when we work in a [[Lie group]], but otherwise we are really generalising the classical exponential function $x \mapsto p \exp x$; every solution to $f' = f$ takes this form.

Classically, there are some other functions called 'exponential'; given any nonzero real (or complex) number $b$, the map $x \mapsto b^x$ (or even $x \mapsto p\, b^x$) is also an exponential map.  Using the [[natural logarithm]], we can define $b^x$ in terms of the natural exponential map $\exp$:
$$ b^x \coloneqq \exp (x \ln b) .$$
So while $b$ is traditionally called the 'base', it is really the number $\ln b$ that matters, or even better the operation of multiplication by $\ln b$.  This operation is an [[endomorphism]] of the real line (or complex plane), and every such endomorphism takes this form for some nonzero $b$ (and some branch of the natural logarithm, in the complex case).  So we see that this generalised exponential map is simply the [[composite]] of the natural exponential map after a linear endomorphism.


## Definition

See also at _[[flow of a vector field]]_.

### With respect to an affine connection

Let $M$ be a [[differentiable manifold]], let $\Del$ be an [[affine connection]] on $M$, and let $p$ be a [[point]] in $M$.  Then by the general theory of [[differential equations]], there is a unique [[maximal partial function|maximally]] defined [[partial function]] $\exp_p$ from the [[tangent space]] $T_p M$ to $M$ such that:

*  $\Del \exp_p = \exp_p$ and
*  $\exp_p(0) = p$.

This function is the __natural exponential map on $M$ at $p$ relative to $\Del$__.  We have $\exp_p\colon U \to M$, where $U$ is some [[neighbourhood]] of $0$ in $T_p M$.  If $M$ is [[complete manifold|complete]] (relative to $\Del$), then $U$ will be all of $T_p M$.

Let $M$ be a [[Riemannian manifold]] (or a [[pseudo-Riemannian manifold]]) and let $p$ be a point in $M$.  Then $M$ may be equipped with the [[Levi-Civita connection]] $\Del_{lc}$, so we define the __natural Riemannian exponential map on $M$ at $p$__ to be the natural exponential map on $M$ at $p$ relative to $\Del_{lc}$.


Given any [[endomorphism]] $\phi\colon T_p M \to T_p M$, we can also consider the __exponential map on $M$ at $p$ relative to $\Del$ with logarithmic base $\phi$__, which is simply $x \mapsto \exp_p \phi(x)$.  We say 'logarithmic base' since a classical exponential function with base $b$ corresponds to an exponential function whose logarithmic base is multiplication by $\ln b$.


### Via geodesics

Recall that a [[geodesic]] is a [[curve]] on a manifold whose [[velocity]] is constant (as measured along that curve relative to a given affine connection).  Working na&#239;vely, we may write
$$ \gamma' = v ,$$
pretend that this is a differential equation for a function $\gamma\colon \mathbb{R} \to \mathbb{R}$, and take the solution
$$ \gamma(t) = p \exp t x ,$$
where $p$ is given by the initial value $\gamma(0) = p$.  We recognise this as being, morally, $\exp_p t x$.  This suggests (although we need more work for a proof) the following result:

Let $M$ be a [[differentiable manifold]], let $\Del$ be an [[affine connection]] on $M$, and let $p$ be a [[point]] in $M$.  Given a [[tangent vector]] $x$ at $p$, there is a unique [[maximal geodesic]] $\gamma$ on $M$ tangent to $x$ at $p$.  If $\gamma(1)$ is defined (which it will be whenever $M$ is [[complete manifold|complete]] and may be in any case), we have $exp_p x = \gamma(1)$.  In any case, we have $\exp_p (t x) = \gamma(t)$ for sufficiently small $t$.

## In real algebras

Let $\mathbb{R}$ be any [[sequentially Cauchy complete]] [[Archimedean field|Archimedean]] [[ordered field|ordered]] [[field]], and let $F:\mathbb{R}\mathrm{Alg} \to \mathbb{R}\mathrm{Vect}$ be the [[forgetful functor]] which takes an $\mathbb{R}$-algebra $A$ to its underlying $\mathbb{R}$-[[vector space]] $F(A)$. Given any $\mathbb{R}$-algebra $A$ whose underlying $\mathbb{R}$-[[vector space]] $F(A)$ is finite-dimensional, each element of $A$ could be expressed as a [[linear combination]], a finite sum of basis vectors. Then one could define the exponential function $\exp:A \to A$ as either 

$$\exp(x) \coloneqq \lim_{n \to \infty} \left(1 + \frac{x}{n}\right)^n$$

or 

$$\exp(x) \coloneqq \lim_{n \to \infty} \sum_{i = 0}^{n} \frac{x^i}{i!}$$

since according to the [[algebraic limit theorem]], limits distribute over finite sums. 

In particular, this is how exponential functions are defined in [[Clifford algebras]] and [[matrix algebras]]. However, the exponential functions in non-commutative algebras are not [[abelian group homomorphisms]], because multiplication is not commutative while addition is commutative. 

### In the dual numbers

The [[dual number]] real algebra $\mathbb{D} \coloneqq \mathbb{R}[\epsilon]/\epsilon^2$ has a notion of exponential function, which is the solution to the functional equation $\exp(x + \epsilon) = \exp(x) (1 + \epsilon)$ with $\exp(0) = 1$. 

## In arbitrary Archimedean ordered fields

In general, Archimedean ordered fields which are not [[sequentially Cauchy complete]] do not have an exponential function. Nevertheless, the exponential map is still guaranteed to be a [[partial function]], because every Archimedean ordered field is a [[Hausdorff space]] and thus a [[sequentially Hausdorff space]]. Thus, an axiom could be added to an Archimedean ordered field $F$ to ensure that the exponential partial function is actually a total function:

**Axiom of exponential function:** _For all elements $x \in F$, there exists a unique element $\exp(x) \in F$ such that for all positive elements $\epsilon \in F_+$, there exists a natural number $N \in \mathbb{N}$ such that for all natural numbers $n \in \mathbb{N}$, if $n \geq N$, then $-\epsilon \lt \left(1 + \frac{x}{n}\right)^{n} - \exp(x) \lt \epsilon$ (or equivalently, $-\epsilon \lt \left(\sum_{i = 0}^{n} \frac{x^i}{i!}\right) - \exp(x) \lt \epsilon$)._

There is another axiom which uses the fact that derivatives of functions are well defined in the [[ordered local ring|ordered local]] [[local Artin algebra|Artin $F$-algebra]] $F[\epsilon]/\epsilon^2$ by the equation $f(x + \epsilon) = f(x) + f'(x) \epsilon$:

**Axiom of exponential function:** _Let $F[\epsilon]/\epsilon^2$ be the ordered local Artin $F$-algebra, with non-zero non-positive non-negative [[nilpotent element]] $\epsilon \in F[\epsilon]/\epsilon^2$ where $\epsilon^2 = 0$ and canonical $F$-algebra homomorphism $h:F \to F[x]/x^2$. There exists a unique function $\exp:F \to F$ and a function $\exp':F[\epsilon]/\epsilon^2 \to F[\epsilon]/\epsilon^2$ such that for every element $x \in F$, $h(\exp(x)) = \exp'(h(x))$, $\exp'(x + \epsilon) = \exp'(x) + \exp'(x) \epsilon$, and $\exp'(0) = 1$._

## In constructive mathematics

In classical mathematics, one could prove that the [[modulated Cantor real numbers]] $\mathbb{R}_C$ are [[sequentially Cauchy complete]] and equivalent to the [[HoTT book real numbers]] $\mathbb{R}_H$. However, in constructive mathematics, the above cannot be proven; while the HoTT book real numbers $\mathbb{R}_H$ are still sequentially Cauchy complete, the modulated Cantor real numbers $\mathbb{R}_C$ in general cannot be proven to be sequentially Cauchy complete. In particular, this means that the sequences 

$$\left(1 + \frac{x}{n}\right)^{n} \quad \mathrm{or} \quad \sum_{i = 0}^{n} \frac{x^i}{i!}$$ 

do not have a limit for all modulated Cantor real numbers $x \in \mathbb{R}_C$. However, the sequences, by definition of $\mathbb{R}_C$, do have a limit for all [[rational numbers]] $x \in \mathbb{Q}$; this means that one could restrict the [[domain]] of the exponential function to the rational numbers $\exp:\mathbb{Q} \to \mathbb{R}_C$, and define it in the usual manner:

* For all rational numbers $x \in \mathbb{Q}$, there exists a unique modulated Cantor real number $\exp(x) \in \mathbb{R}_C$ such that for all positive rational numbers $\epsilon \in \mathbb{Q}_+$, there exists a natural number $N \in \mathbb{N}$ such that for all natural numbers $n \in \mathbb{N}$, if $n \geq N$, then $-\epsilon \lt \left(1 + \frac{x}{n}\right)^{n} - \exp(x) \lt \epsilon$ (or equivalently, $-\epsilon \lt \left(\sum_{i = 0}^{n} \frac{x^i}{i!}\right) - \exp(x) \lt \epsilon$).

## In Lie groups {#exp_of_Lie_groups}

Note: this section is under repair. 

The classical exponential function $\exp \colon \mathbb{R} \to \mathbb{R}^*$ or $\exp \colon \mathbb{C} \to \mathbb{C}^*$ satisfies the fundamental property: 

+-- {: .num_prop} 
###### Proposition 
The function $\exp \colon \mathbb{C} \to \mathbb{C}^*$ is a homomorphism taking addition to multiplication: 
$$\exp(x + y) = \exp(x) \cdot \exp(y)$$ 
=-- 

+-- {: .proof} 
###### Proof 
A number of proofs may be given. One rests on the combinatorial [[binomial theorem|binomial identity]]  

$$(x + y)^n = \sum_{j + k = n} \frac{n!}{j! k!} x^j y^k$$ 

(which crucially depends on the fact that multiplication is [[commutative monoid|commutative]]), whereupon 

$$\array{
\sum_{n \geq 0} \frac{(x+y)^n}{n!} & = & \sum_{n \geq 0} \sum_{j + k = n} \frac1{j!} \frac1{k!} x^j y^k \\
 & = & (\sum_{j \geq 0} \frac{x^j}{j!}) \cdot (\sum_{k \geq 0} \frac{y^k}{k!}) \\ 
 & = & \exp(x) \cdot \exp(y)
}$$

An alternative proof begins with the observation that $f = \exp$ is the solution to the system $f' = f$, $f(0) = 1$. For each $y$, the function $g_1 \colon x \mapsto f(x) f(y)$ is a solution to the system $g' = g$, $g(0) = f(y)$, as is the function $g_2 \colon x \mapsto f(x + y)$. Then by uniqueness of solutions to ordinary differential equations (over connected domains; see, e.g., [here](http://en.wikipedia.org/wiki/Picard%E2%80%93Lindel%C3%B6f_theorem)), $g_1 = g_2$, i.e., $f(x + y) = f(x)f(y)$ for all $x, y$.[^fine] 
=-- 

[^fine]: A previous edit offered even more detail: "An alternative proof begins with the premise that each solution of the ordinary differential equation $g' = 0$ is locally constant. Suppose $c$ is a complex number. As $\exp' = \exp$, we find that $(\exp(x) \exp(c - x))' = \exp(x) \exp(c - x) + \exp(x) (-\exp(c-x)) = 0$. Hence, by the premise and the connectedness of the domain of $\exp$ (either ${\mathbb{R}}$ or ${\mathbb{C}}$), we obtain $\exp(x)\exp(c - x) = \exp(0)\exp(c)$. The initial condition $\exp(0) = 1$ then yields $\exp(x)\exp(c - x) = \exp(c)$. The result follows by setting $c = x + y$." 

Let $M$ be [[Lie group]] and let $\mathfrak{g}$ be its [[Lie algebra]] $T_1 M$, the tangent space to the [[identity element]] $1$.  Then $M$ may be equipped with the canonical left-invariant connection $\Del_l$ or the canonical right-invariant connection $\Del_r$.  It turns out that the natural Riemannian exponential maps on $M$ at $1$ relative to $\Del_l$ and $\Del_r$ are the same; we define this to be the __natural Lie exponential map on $M$ at the identity__, denoted simply $\exp$.  Several nice properties follow:

*  $\exp$ is defined on all of $\mathfrak{g}$.
*  $\exp \colon \mathfrak{g} \to G$ is a [[smooth map]]. 
*  If $\rho \colon \mathbb{R} \to \mathfrak{g}$ is a smooth homomorphism from the additive group $\mathbb{R}$ (i.e., if $\rho$ is an $\mathbb{R}$-linear map, uniquely determined by specifying $X = \rho(1)$), then $\exp \circ \rho_X \colon \mathbb{R} \to G$ is a smooth homomorphism. 
*  For $X, Y \in \mathfrak{g}$, if $[X, Y] = 0$, then the restriction of $\exp \colon \mathfrak{g} \to G$ to the subspace spanned by $X$ and $Y$ is a smooth homomorphism to $G$. In particular, $\exp \colon \mathfrak{g} \to G$ is a homomorphism if $\mathfrak{g}$ is abelian (e.g., if $G$ is a commutative Lie group). 
*  $\exp$ is [[surjection|surjective]] (a [[regular epimorphism]]) if $G$ is [[connected space|connected]] and [[compact space|compact]] (and also in some other situations, such as the classical cases where $G$ is $]0,\infty[$ or $\mathbb{C} \setminus \{0\}$). See [this post](https://terrytao.wordpress.com/2011/06/25/two-small-facts-about-lie-groups/) by Terence Tao, Proposition 1; see also the first comment which indicates an alternative proof based on the fact that [[maximal tori]] in $G$ are all conjugate to one another. Note also that the exponential map might not be surjective if the compactness assumption is dropped, as in the case of $G = SL_2(\mathbb{R})$ or $SL_2(\mathbb{C})$, both of which are connected; see [here](http://math.stackexchange.com/questions/643216/non-surjectivity-of-the-exponential-map-to-sl2-mathbbc) for instance. 
*  If $G$ is [[compact space|compact]], then it may be equipped with a [[Riemannian metric]] that is both left and right invariant (see Tao's post linked in the previous remark); then the Lie exponential map is the same as the Riemannian exponential map at $1$.
*  If $G$ is a [[matrix Lie group]], then $\exp$ is given by the classical series formula (eq:series).

(to be expanded on) 


## Logarithms

A __[[logarithm]]__ is a [[local section]] of an exponential map.

## Related concepts

* [[plane wave]]

* [[flow of a vector field]]

* [[Euler number]], [[e]]

* [[logarithm]]

* [[Euler's formula]]

* [[exponential exact sequence]]

* [[Hamiltonian flow]]

* [[exponential modality]]

* [[exponential ring]]

* [[one-parameter semigroup]]

## References

Discussion in [[constructive analysis]] of the exponential function on [[real numbers]]:

* {#Bishop} [[Errett Bishop]], §7 in: *[[Foundations of Constructive Analysis]]*, McGraw-Hill (1967)

* [[Errett Bishop]], [[Douglas Bridges]] §7 in: *[[Constructive Analysis]]*, Grundlehren der mathematischen Wissenschaften **279**, Springer (1985) &lbrack;[doi:10.1007/978-3-642-61667-9](https://doi.org/10.1007/978-3-642-61667-9)&rbrack;

See also:

* Wikipedia, [exponential map (Lie theory)](https://en.wikipedia.org/wiki/Exponential_map_%28Lie_theory%29), [derivative of the exponential map](https://en.wikipedia.org/wiki/Derivative_of_the_exponential_map), [exponential map (Riemannian geometry)](https://en.wikipedia.org/wiki/Exponential_map_(Riemannian_geometry))

* Springer [[eom]]: [exponential mapping](https://www.encyclopediaofmath.org/index.php/Exponential_mapping)

An extensive treatment for the general exponential map for an affine connection, for exponential map for Riemannian manifolds and the one for Lie groups is

* Sigurdur Helgason, Differential geometry, Lie groups and symmetric spaces

Specifically for [[Lie groups]], a different detailed treatment of the exponential map is in 

* [[M M Postnikov]], _Lie groups and Lie algebras_, Geometry V

Some nice historical notes are in

* Wilfried Schmid, _Poincare and Lie groups_, Bull. Amer. Math. Soc. 6:2, 1982 [pdf](http://www.ams.org/journals/bull/1982-06-02/S0273-0979-1982-14972-2/S0273-0979-1982-14972-2.pdf)

Discussion in [[point-free topology]]:

* Ming Ng, [[Steve Vickers]], *Point-free Construction of Real Exponentiation*, Logical Methods in Computer Science **18** 3 (2022) &lbrack;[doi:10.46298/lmcs-18(3:15)2022](https://doi.org/10.46298/lmcs-18%283%3A15%292022), [arXiv:2104.00162](https://arxiv.org/abs/2104.00162)&rbrack;

* [[Steve Vickers]], *The Fundamental Theorem of Calculus point-free, with applications to exponentials and logarithms* &lbrack;[arXiv:2312.05228](https://arxiv.org/abs/2312.05228)&rbrack;


[[!redirects exponential map]]
[[!redirects exponential maps]]
[[!redirects exponential function]]
[[!redirects exponential functions]]


[[!redirects exponent]]
[[!redirects exponents]]

[[!redirects exponentiation]]
[[!redirects exponential]]
[[!redirects exponentials]]

[[!redirects exponential series]]


