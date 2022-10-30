
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--




# Contents
* tic
{:toc}


## Idea

The _Chevalley-Eilenberg algebra_ $CE(\mathfrak{g})$ of a [[Lie algebra]] is a [[differential graded algebra]] of elements dual to $\mathfrak{g}$ whose [[differential]] encodes the Lie bracket on $\mathfrak{g}$.

The [[cochain cohomology]] of the underlying [[cochain complex]] is the [[Lie algebra cohomology]] of $\mathfrak{g}$.

This generalizes to a notion of Chevalley-Eilenberg algebra for $\mathfrak{g}$ an [[L-∞-algebra]], a [[Lie algebroid]] and generally an [[∞-Lie algebroid]].

## Grading conventions {#GradingConvention}

This differential-graded subject is somewhat notorious for a plethora of equivalent but different conventions on gradings and signs. 

For the following we adopt the convention that for $V$ an $\mathbb{N}$-[[graded vector space]] we write

$$
  \begin{aligned}
    \wedge^\bullet V &:= Sym(V[1])
     \\
      & = k \oplus (V_0) \oplus (V_1 \oplus V_0 \wedge V_0) \oplus 
     (V_2 \oplus V_1 \otimes V_0 \oplus V_0 \wedge V_0 \wedge V_0)
     \oplus \cdots
  \end{aligned}
$$

for the [[free construction|free]] graded-commutative algebra on the graded vector space obtained by shifting $V$ _up_ in degree by one.

Here the elements in the $n$th term in parenthesis are in degree $n$.

A plain vector space, such as the dual $\mathfrak{g}^*$ of the vector space underlying a Lie algebra, we regard here as a $\mathbb{N}$-graded vector space in degree 0. For such, $\wedge^\bullet \mathfrak{g}^*$ is the ordinary [[Grassmann algebra]] over $\mathfrak{g}^*$, where elements of $\mathfrak{g}^*$ are generators of degree 1.



## Of Lie algebras {#OfLieAlgebra}

### Definition {#DefForLieAlg}

The _Chevalley-Eilenberg algebra_ $CE(\mathfrak{g})$ of a finite dimensional [[Lie algebra]] $\mathfrak{g}$ is the [[semifree dga|semifree]] graded-commutative [[dg-algebra]] whose underlying graded algebra is the [[Grassmann algebra]] 

$$
  \wedge^\bullet \mathfrak{g}^*
  = 
  k \oplus \mathfrak{g}^* \oplus (\mathfrak{g}^* \wedge \mathfrak{g}^* ) \oplus \cdots
$$ 

(with the $n$th skew-symmetrized power in degree $n$)

and whose [[differential]] $d$ (of degree +1) is on $\mathfrak{g}^*$ the dual of the Lie bracket

$$
  d|_{\mathfrak{g}^*} := [-,-]^* : \mathfrak{g}^* \to \mathfrak{g}^* \wedge \mathfrak{g}^*
$$

extended uniquely as a graded [[derivation]] on $\wedge^\bullet \mathfrak{g}^*$.

That this differential indeed squares to 0, $d \circ d = 0$, is precisely the fact that the Lie bracket satisfies the [[Jacobi identity]].


If we choose a dual basis $\{t^a\}$ of $\mathfrak{g}^*$ and let $\{C^a{}_{b c}\}$ be the structure constants of the Lie bracket in that basis, then the action of the differential on the basis generators is

$$
  d t^a = - \frac{1}{2} C^a{}_{b c} t^b \wedge t^c
  \,,
$$

where here and in the following a sum over repeated indices is implicit.

This has a more or less evident generalization to infinite-dimensional Lie algebras.,


### Properties {#PropertiesForLieAlg}

One observes that for $\mathfrak{g}$ a vector space,  the graded-commutative dg-algebra structures on $\wedge^\bullet \mathfrak{g}^*$ are precisely in bijection with Lie algebra structures on $\mathfrak{g}$: the dual of the restriction of $d$ to $\mathfrak{g}^*$ defines a skew-linear bracket and the condition $d^2 = 0$ holds if and only if that bracket satisfies the Jacobi identity.

Moreover, morphisms if Lie algebras $\mathfrak{g} \to \mathfrak{h}$ are precisely in bijection with morphisms of dg-algebras $CE(\mathfrak{g}) \leftarrow CE(\mathfrak{h})$. And the $CE$-construction is functorial.

Therefore, if we write $dgAlg_{sf,1}$ for the category whose objects are [[semifree dga]]s on generators in degree 1, we find that the construction of CE-algebras from Lie algebras constitutes a canonical [[equivalence of categories]]

$$
  LieAlg \stackrel{CE(-)}{\underset{\simeq}{\to}} (dgAlg_{sf,1})^{op}
  \,,
$$

where on the right we have the [[opposite category]].

This says that in a sense the Chevalley-Eilenberg algebra is just another way of looking at (finite dimensional) Lie algebras. 

There is an analogous statement not involving the dualization: Lie algebra structures on $\mathfrak{g}$ are also in bijection with the structure of a _[[differential graded coalgebra]]_ $(\vee^\bullet \mathfrak{g}, D)$ on the free graded-co-commutative coalgebra $\vee^\bullet \mathfrak{g}$ on $\mathfrak{g}$ with $D$ a [[derivation]] of degree -1 squaring to 0.

The relation between the differentials is simply dualization

$$
  (\vee^\bullet \mathfrak{g}, D) \leftrightarrow
  (\wedge^\bullet \mathfrak{g}^* , d )
$$

where for each $\omega \in \wedge^\bullet \mathfrak{g}^*$ we have

$$
  d \omega = \omega(D(-))
  \,.
$$

## Of $L_\infty$-algebras

The equivalence between Lie algebras and differential graded algebras/coalgebras discussed above  suggests a grand generalization by simply generalizing the [[Grassmann algebra]] over a [[vector space]] $\mathfrak{g}^*$ to the Grassmann algebra over a [[graded vector space]].

If $\mathfrak{g}$ is a graded vector space, then a differential $D$ of degree -1 squaring to 0 on $\vee^\bullet \mathfrak{g}$ is precisely the same as equipping $\mathfrak{g}$ with the structure of an [[L-∞ algebra]].

Dually, this corresponds to a general [[semifree dga]] 

$$
  CE(\mathfrak{g}) := (\wedge^\bullet \mathfrak{g}^*, d = D^*)
  \,.
$$ 

This we may usefully think of as the Chevalley-Eilenberg algebra of the $L_\infty$-algebra $\mathfrak{g}$.

So _every_ commutative [[semifree dga]] (degreewise finite-dimensional) is the Chevaley-Eilenberg algebra of some [[L-∞ algebra]] of finite type.

This means that many constructions involving [[dg-algebra]]s are secretly about [[∞-Lie theory]]. For instance the [[Sullivan construction]] in [[rational homotopy theory]] may be interpreted in terms of [[Lie integration]] of $L_\infty$-algebras.


## Of Lie algebroids {#OfLieAlgebroids}

For $\mathfrak{a}$ a [[Lie algebroid]] given as 

* a [[vector bundle]] $E\to X$ 

* with anchor map $\rho : E \to T X$ 

* and bracket $[-,-] : \Gamma(E)\wedge_{C^\infty(X)} \Gamma(E) \to \Gamma(E)$ 

the corresponding Chevalley-Eilenberg algebra is

$$
  CE(\mathfrak{a}) := (\wedge^\bullet_{C^\infty(X)} \Gamma(E)^*, d)
  \,,
$$

where now the [[tensor product]]s and dualization is over the ring $C^\infty(X)$ of [[smooth function]]s on the base space $X$ (with values in the [[real number]]s). The differential $d$ is given by the formula

$$
  (d\omega)(e_0, \cdots, e_n)
  = 
  \sum_{\sigma \in Shuff(1,n)} sgn(\sigma) \rho(e_{\sigma(0)})(\omega(e_{\sigma(1)}, \cdots, e_{\sigma(n)}))
  +
  \sum_{\sigma \in Shuff(2,n-1)} sign(\sigma) 
   \omega([e_{\sigma(0)},e_{\sigma(1)}],e_{\sigma(2)}, \cdots, e_{\sigma(n)} )
  \,,
$$

for all $\omega \in \wedge^n_{C^\infty(X)} \Gamma(E)^*$ and $(e_i \in \Gamma(E))$, where $Shuff(p,q)$ denotes the set of $(p,q)$-[[shuffle]]s $\sigma$ and $sgn(\sigma)$ the [[signature]] $\in \{\pm 1\}$ of the corresponding [[permutation]].

For $X = *$ the point we have that $\mathfrak{a}$ is a Lie algebra and this definition reproduces the above definition of the CE-algebra of a Lie algebra (possibly up to an irrelevant global sign).

## Of $\infty$-Lie algebroids

See [[∞-Lie algebroid]].

## Examples

### Of abelian Lie $n$-algebras

The CE-algebra of the Lie algebra of the [[circle group]] $\mathfrak{u}(1)$ is the graded-commutative dg-algebra on a single generator in degree 1 with vanishing differential.

More generally, the $L_\infty$-algebra $b^n \mathfrak{u}(1)$ is the one whose CE algebra is the commutative dg-algebra with a single generator in degree $n+1$ and vanishing differential.


### Of $\mathfrak{su}(2)$

The CE-algebra of $\mathfrak{su}(2)$ has two generators $x, y, z$ in degree one and differential

$$
  d x_1 = x_2 \wedge x_3
$$

and cyclically.

### Of the tangent Lie algebroid $T X$

For $X$ a [[smooth manifold]] and $T X$ its [[tangent Lie algebroid]], the corresponding CE-algebra is the [[de Rham algebra]] of $X$.

$$
  CE(T X) = (\wedge^\bullet_{C^\infty(X)} \Gamma(T^* X), d_{dR})
  \,.
$$

For $(v_i \in \Gamma(T X))$ [[vector field]]s and $\omega \in \Omega^n = \wedge^n_{C^\infty(X)} \Gamma(T X)^*$ a [[differential form]] of degree $n$, 
the [formula for the CE-differential](#OfLieAlgebroids)

$$
  (d\omega)(v_0, \cdots, v_n)
  = 
  \sum_{\sigma \in Sh(1,n)} sgn(\sigma) v_{\sigma(0)}(\omega(v_{\sigma(1)}, \cdots, v_{\sigma(n)}))
  +
  \sum_{\sigma \in Shuff(2,n-1)} sgn(\sigma) 
   \omega([v_{\sigma(0)},v_{\sigma(1)}],v_{\sigma(2)}, \cdots, v_{\sigma(n)} )
  \,,
$$

is indeed that for the de Rham differential.

### Of the string Lie 2-algebra

For $\mathfrak{g}$ a semisimple Lie algebra with binary [[invariant polynomial]] $\langle -,-\rangle$ -- the [[Killing form]] -- , the CE-algebra of the [[string Lie 2-algebra]] is

$$
  CE(\mathfrak{string}) = (\wedge^\bullet( \mathfrak{g}^+ \oplus \mathbb{R}^*[1]), d_{string})
$$

where the differential restricted to $\mathfrak{g}^*$ is $[-,-]^*$ while on the new generator $b$ spanning $\mathbb{R}^*[1]$ is it

$$
  d b = \langle -, [-,-]\rangle \in \wedge^3 \mathfrak{g}^*
  \,.
$$




### Weil algebra

For $\mathfrak{g}$ a [[Lie algebra]], the CE-algebra of the [[Lie 2-algebra]] given by the [[differential crossed module]] $(\mathfrak{g} \stackrel{Id}{\to} \mathfrak{g})$ is the [[Weil algebra]] $W(\mathfrak{g})$ of $\mathfrak{g}$

$$
  CE(\mathfrak{g} \stackrel{Id}{\to} \mathfrak{g})
  =
  W(\mathfrak{g})
  \,.
$$

### Lie algebra cohomology

[[Lie algebra cohomology]] of a $k$-[[Lie algebra]] $\mathfrak{g}$ with coefficients in the left $\mathfrak{g}$-module $M$ is defined as $H^*_{Lie}(\mathfrak{g},M) = Ext_{U\mathfrak{g}}^*(k,M)$. It can be computed as $Hom_{\mathfrak{g}}(V(\mathfrak{g}),M)$ (a similar story is for [[Lie algebra homology]]) where $V(\mathfrak{g})=U(\mathfrak{g})\otimes\Lambda^*(\mathfrak{g})$ is the [[Chevalley-Eilenberg chain complex]]. If $\mathfrak{g}$ is finite-dimensional over a field then $Hom_{\mathfrak{g}}(V(\mathfrak{g}),k) =  CE(\mathfrak{g}) = \Lambda^* \mathfrak{g}^*$ is the underlying complex of the Chevalley-Eilenberg algebra, i.e. the [[Chevalley-Eilenberg cochain complex]] with trivial coefficients. 

A [[cocycle]] in degree n of the [[Lie algebra cohomology]] of a [[Lie algebra]] $\mathfrak{g}$ with values in the trivial module $\mathbb{R}$ is a morphism of [[L-∞ algebra]]s

$$
  \mathfrak{g} \to b^{n-1} \mathfrak{u}(1)
  \,.
$$

In terms of CE-algebras this is a [[dg-algebra]] morphism

$$
  CE(\mathfrak{g}) \leftarrow CE(b^{n-1}\mathfrak{u}(1))
  \,.
$$

Since by the above example the dg-algebra on he right has a single generator in degree $n$ and vanishing differential, such a morphism is precisely the same thing as a degree $n$-element in $CE(\mathfrak{g})$, i.e. an element  $\omega \in \wedge^n \mathfrak{g}^*$ which is closed under the CE-differential 

$$
  d_{CE} \omega = 0
  \,.
$$

This is what one often sees as the definition of a cocycle in [[Lie algebra cohomology]]. However, from the general point of view of [[cohomology]], it is better to think of the cocycle equivalently as the morphism $\mathfrak{g} \to b^{n-1}\mathfrak{u}(1)$.


### BRST complex

In [[physics]], the Chevalley-Eilenberg algebra $CE(\mathfrak{g}, N)$ of the [[action]] of a  [[Lie algebra]] or [[L-∞ algebra]] of a [[gauge group]] $G$ on space $N$ of fields is called the [[BRST complex]].


In this context

* the generators in $N$ in degree 0 are called **fields**;

* the generators $\in \mathfrak{g}^*$ in degree $1$ are called **ghosts**;

* the generators in degree $2$ are called **ghosts of ghosts**;

* etc.

If $N$ is itself a [[chain complex]], then this is called a [[BV-BRST formalism|BV-BRST complex]]

## Related concepts

* [[∞-Lie algebra cohomology]]

* **Chevalley-Eilenberg algebra**

* [[Weil algebra]]

* [[invariant polynomial]]



## References

An elementary introduction for CE-algebras of Lie algebras is at the beginning of

* J. A. de Azcarraga, J. M. Izquierdo, J. C. Perez Bueno, _An introduction to some novel applications of Lie algebra cohomology and physics_ ([arXiv](http://arxiv.org/abs/physics/9803046))

More details are in section 6.7 of

* J. A. de Azc&#225;rraga, Jos&#233; M. Izquierdo, _Lie Groups, Lie Algebras, Cohomology and Some Applications in Physics_ , Cambridge monographs of mathematical physics, (1995)

See also almost any text on [[Lie algebra cohomology]] (see the list of references there).

[[!redirects Chevalley--Eilenberg algebra]]
[[!redirects Chevalley?Eilenberg algebra]]
[[!redirects Chevalley-Eilenberg algebras]]
[[!redirects Chevalley--Eilenberg algebras]]
[[!redirects Chevalley?Eilenberg algebras]]