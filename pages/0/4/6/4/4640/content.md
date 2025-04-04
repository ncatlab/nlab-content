
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For every [[Lawvere theory]] $T$ containing the theory of [[abelian group]]s [[Isbell duality|Isbell dual]] [[sheaf topos]] over formal duals of $T$-algebras contains a canonical [[line object]] $\mathbb{A}^1$.

For $T$ the theory of commutative [[ring]]s this is called the _affine line_ .


## Definition

### Affine line

Let $k$ be a [[ring]], and $T$ the [[Lawvere theory]] of [[associative algebra]]s over $k$, such that the category of [[algebras over a Lawvere theory]] $T Alg = Alg_k$ is the [[category]] of $k$-algebras. 

+-- {: .num_defn}
###### Definition

The canonical $T$-[[line object]] is the **affine line**

$$
  \mathbb{A}_k := Spec(F_T(*))  = Spec (k[t])
  \,.
$$

=--

Here the [[free functor|free]] $T$-algebra on a single generator $F_T(*)$ is the [[polynomial algebra]] $k[t] \in Alg_k$ on a single generator $* = t$ and $Spec k[t]$ may be regarded as the corresponding object in the [[opposite category]] $Aff_k := Alg_k^{op}$ of [[affine scheme]]s over $Spec  k$.


### Multiplicative group
 {#MultiplicativeGroup}

The [[multiplicative group]] object in $Ring^{op}$ corresponding to the affine line -- usually just called the **multiplicative group** -- is the [[group scheme]] denoted $\mathbb{G}_m$

* whose underlying affine scheme is

  $$
    (\mathbb{A}^1 - \{0\}) := Spec \left(k[t,t^{-1}]\right)
    \,,
  $$

  where $k[t,t^{-1}]$ is the [[localization]] of the ring $k[t]$ at the element $t = (t-0)$.

* whose multiplication operation

  $$
    \cdot \mathbb{G}_m \times \mathbb{G}_m \to \mathbb{G}_m
  $$

  is the morphism in $Ring^{op}$ corresponding to the morphism in [[Ring]]

  $$
    k[t_1,t_1^{-1}] \otimes_k k[t_2, t_2^{-1}] \leftarrow k[t,t^{-1}]
  $$

  given by $t \mapsto t_1 \cdot t_2$;

* whose unit map $Spec k \to Spec k[t,t^{-1}]$ is given by

  $$
    t \mapsto 1
  $$

* and whose inversion map $Spec k[t,t^{-1}] \to Spec[t,t^{-1}]$ is given by

  $$
    t \mapsto t^{-1}
    \,.
  $$

Therefore for $R$ any [[ring]] a morphism

$$
  Spec R \longrightarrow \mathbb{G}_m
$$

is equivalently a ring homomorphism

$$
  R \leftarrow k[t,t^{-1}]
$$

which is equivalently a choice of multiplicatively invertible element in $R$. Therefore

$$
  Hom(Spec R , \mathbb{G}_m) \simeq R^\times = GL_1(R)
$$

is the [[group of units]] of $R$.

### Additive group
 {#AdditiveGroup}

The [[additive group]] in $Ring^{op}$ corresponding to the affine line -- usually just called the **additive group** -- is the [[group scheme]] denoted $\mathbb{G}_a$  

* whose underlying object is $\mathbb{A}^1$ itself;

* whose addition operation $\mathbb{G}_a \times \mathbb{G}_a \to \mathbb{G}_a$ is dually the ring homomorphism 

  $$
    k[t_1] \otimes_k k[t_2] \leftarrow k[t]
  $$

  given by

  $$
    t \mapsto t_1 + t_2
    \,;
  $$

* whose unit map is given by

  $$
    t \mapsto 0
    \,;
  $$

* whose inversion map is given by

  $$
    t \mapsto -t
    \,.
  $$

### Group of roots of unity

The group of $n$th [[roots of unity]] is

$$
  \mu_n = Spec(k[t](t^n -1))
  \,.
$$

This sits inside the [[multiplicative group]] via the [[Kummer sequence]]

$$
  \mu_n \longrightarrow \mathbb{G}_m \stackrel{(-)^n}{\longrightarrow}\mathbb{G}_m
 \,.
$$

## Properties 
 {#Properties}

### Grading
 {#Grading}

+-- {: .num_prop}
###### Proposition

Let $R$ be a commutative $k$-algebra. There is a [[natural isomorphism]] between

* $\mathbb{Z}$-[[graded algebra|gradings]] on $R$;

* $\mathbb{G}_m$-[[action]]s on $Spec R$.

=--

+-- {: .proof}
###### Proof


For the first direction, let $R$ be a $\mathbb{Z}$-[[graded algebra|graded commutative algebra]]. Then $X = Spec R$ comes with a $\mathbb{G}$-action given as follows: the action morphism

$$
 \rho :  X \times \mathbb{G}_m \to X
$$

is dually the ring homomorphism

$$
  R \otimes_k \mathbb{Z}[t,t^{-1}] \leftarrow R
$$

defined on homogeneous elements $r$ of degree $n$ by

$$
  r \mapsto r \cdot t^n
  \,.
$$

The action property

$$
  \array{
     X \times \mathbb{G}_m \times \mathbb{G}_m &\stackrel{Id \times \cdot}{\to}& X \times \mathbb{G}
     \\
     {}^{\mathllap{\rho} \times Id}\downarrow && \downarrow^{\mathrlap{\rho}}
     \\
     X \times \mathbb{G}_m &\stackrel{\rho}{\to}& X
  }
$$

is equivalently the equation

$$
  r (t_1)^n \cdot (t_2)^n = r (t_1 \cdot t_2)^n
$$

for all $n \in \mathbb{Z}$. Similarly the [[unitality]] of the action is the equation

$$
  (1)^n = 1
  \,.
$$

Conversely, given an action of $\mathbb{G}_m$ on $Spec R$ we have some morphism

$$
  R[t,t^{-1}] \leftarrow R
$$

that sends

$$
  r \mapsto \sum_{n \in \mathbb{Z}} r_n t^n
  \,.
$$


By the action property we have that 

$$
  \sum_n r_n (t_1 t_2)^n = \sum_{n,k} (r_n)_k t_1^n t_2^k
  \,.
$$

Hence 

$$
  (r_n)_k = 
  \left\{
    \array{
       r_n & if \; n = k
       \\
       0 & otherwise
    }
  \right.
$$

and so the morphism gives a decomposition of $R$ into pieces labeled by $\mathbb{Z}$.

One sees that these two constructions are [[inverse]] to each other.

=--


### &#201;tale homotopy type

+-- {: .num_example}
###### Example

For $k$ a [[field]] of [[characteristic]] 0, then the affine line $\mathbb{A}^1_k$ has a [[contractible homotopy type|contractible]] [[étale homotopy type]] . This is no longer the case in [[positive number|positive]] [[characteristic]].

=--

([HSS 13, section 1](#HSS13))

### Internal formulation
 {#InternalFormulation}

+-- {: .num_prop}
###### Proposition

Let $X$ be a [[scheme]] and $Sh(Sch/X)$ the [[Zariski site|big Zariski topos]] associated to $X$. Denote by $\mathbb{A}^1$ (the [[affine line]]) the [[ring object]] $T \mapsto \Gamma(T,\mathcal{O}_T)$, i.e. the functor represented by the $X$-scheme $\mathbb{A}^1_X \coloneqq X \times Spec(\mathbb{Z}[t])$. Then:

* $\mathbb{A}^1$ is [[internal logic|internally]] a [[local ring]].

* $\mathbb{A}^1$ is internally a [[field]] in the sense that any nonzero element is invertible.

* Internally, any [[function]] $f : \mathbb{A}^1 \to \mathbb{A}^1$ is a [[polynomial]] function, i.e. of the form $f(x) = \sum_i a_i x^i$ for some coefficients $a_i : \mathbb{A}^1$. More precisely,
$$ Sh(Sch/X) \models \forall f : [\mathbb{A}^1,\mathbb{A}^1]. \bigvee_{n \in \mathbb{N}} \exists a_0,\ldots,a_n : \mathbb{A}^1. \forall x : \mathbb{A}^1. f(x) = \sum_i a_i x^i. $$
Furthermore, these coefficients are uniquely determined.

=--

+-- {: .proof}
###### Proof

Since the internal logic is local, we can assume that $X = Spec(R)$ is affine. The interpretations of the asserted statements using the [[Zariski site#KripkeJoyal|Kripke–Joyal semantics]] are:

* Let $S$ be an $R$-algebra and $f, g \in S$ be elements such that $f + g = 1$. Then there exists a partition $1 = \sum_i s_i \in S$ such that in the localized rings $S[s_i^{-1}]$, $f$ or $g$ is invertible.

* Let $S$ be an $R$-algebra and $f \in S$ an element. Assume that any $S$-algebra $T$ in which $f$ is zero is trivial (fulfills $1 = 0 \in T$). Then $f$ is invertible in $S$.

* Let $S$ be an $R$-algebra and $f \in [\mathbb{A}^1,\mathbb{A}^1](S) = S[T]$ be an element. Then there exists a partition $1 = \sum_i s_i \in S$ such that in the localized rings $S[s_i^{-1}]$, $f$ is a polynomial with coefficients in $S[s_i^{-1}]$.

For the first statement, simply choose $s_1 \coloneqq f$, $s_2 \coloneqq g$.

For the second statement, consider the $S$-algebra $T \coloneqq S/(f)$.

The third statement is immediate, localization is not even necessary.

=--

+-- {: .num_remark}
###### Remark

Since the big Zariski topos is [[cocomplete category|cocomplete]] (being a [[Grothendieck topos]]), one can also get rid of the external [[disjunction]] and refer to the object $\mathbb{A}^1[X]$ of internal polynomials: The canonical ring homomorphism $\mathbb{A}^1[X] \to [\mathbb{A}^1,\mathbb{A}^1]$ (given by evaluation) is an [[isomorphism]].

=--

See also at _[[synthetic differential geometry applied to algebraic geometry]]_.

## Examples

### Projective space

The [[diagonal]] [[action]] of the multiplicative group on the [[product]] $\mathbb{A}^n := \prod_{i = 1 \cdots n} \mathbb{A}^1$ for $n \in \mathbb{N}$ 

$$
  \mathbb{A}^n \times \mathbb{G}_m \to \mathbb{A}^n
$$

is dually the morphism

$$
  k[t, t_1, \cdots, t_n] \leftarrow k[t_1, \cdots, t_n]
$$

given by

$$
  t_i \mapsto t \cdot t_i
  \,.
$$

This makes $k[t,\{t_i\}]$ the free [[graded algebra]] over $k$ on $n$ generators $t_i$ in degree 1. This is $\mathbb{N} \subset \mathbb{Z}$-graded. What is genuinely $\mathbb{Z}$-graded is 

$$
  \mathcal{O} (\mathbb{A}^n - \{0\}) \simeq k[t_1, t_1^{-1}, \cdots, t_n, t_n^{-1}]
  \,.
$$

The quotient by the multiplicative group action

$$
  \mathbb{A} P^n_k := (\mathbb{A}^{n+1} - \{0\})/\mathbb{G}_m
$$

is the [[projective space]] over $k$ of [[dimension]] $n$.

### $\mathbb{A}^1$-homotopy theory

In [[A1-homotopy theory|A^1 homotopy theory]] one considers the [[reflective sub-(∞,1)-category|reflective]] [[localization of an (∞,1)-category|localization]]

$$
  Sh_\infty(C)_{\mathbb{A}^1}
  \stackrel{\leftarrow}{\hookrightarrow}
  Sh_\infty(C)
$$

of the [[(∞,1)-topos]] of [[(∞,1)-sheaves]] over a [[site]] $C$ such as the [[Nisnevich site]], at the morphisms of the form

$$
  p_1 : X \times \mathbb{A}^1 \to X
$$

that contract away cartesian factors of the affine line.

## Related concepts

* [[analytic affine line]]

* [[spectral affine line]]

* [[Tate sphere]]

## References

Discussion of [[étale homotopy type]] is in

* {#HSS13} Armin Holschbach, Johannes Schmidt, Jakob Stix, _&#201;tale contractible varieties in positive characteristic_ ([arXiv:1310.2784](http://arxiv.org/abs/1310.2784))


[[!redirects affine lines]]