
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

## Idea

A _bimodule_ is a [[module]] in two compatible ways over two [[rings]] or [[algebras]].

## Definition

### In ring theory/algebra

#### With a left action and a right action

Given two [[rings]] $R$ and $S$, a $R$-$S$-bimodule is an [[abelian group]] $B$ with a [[bilinear function|bilinear]] [[left action|left $R$-action]] $\alpha_R:R \times B \to B$ and a bilinear [[right action|right $S$-action]] $\alpha_S:B \times S \to B$ such that for all $r \in R$, $b \in B$, and $s \in S$, $\alpha_R(r, \alpha_S(b, s)) = \alpha_S(\alpha_R(r, b), s)$. 

#### With a biaction

Equivalently, given two [[rings]] $R$ and $S$, a $R$-$S$-bimodule is an [[abelian group]] $B$ with a [[multilinear function|trilinear]] [[biaction|$R$-$S$-biaction]], a function $(-)(-)(-):R \times B \times S \to B$ such that 

* for all $b \in B$, $1_R b 1_S = b$

* for all $b \in B$, $r_1 \in R$, $r_2 \in R$, $s_1 \in S$, $s_2 \in S$, $r_1 (r_2, b, s_1) s_2 = (r_1 \cdot_R r_2) b (s_1 \cdot_S s_2)$

* for all $r_1 \in R$, $r_2 \in R$, $b \in B$, $s \in S$, $(r_1 + r_2) b s = r_1 b s + r_2 b s$

* for all $r \in R$, $b_1 \in B$, $b_2 \in B$, $s \in S$, $r (b_1 + b_2) s = r b_1 s + r b_2 s$

* for all $r \in R$, $b \in B$, $s_1 \in S$, $s_2 \in S$, $r b (s_1 + s_2) = r b s_1 + r b s_2$

representing simultaneous left multiplication by scalars $r \in R$ and right multiplication by scalars $s \in S$. 

#### Relation between biactions, left actions, and right actions of a bimodule 

Given a left $R$-action $\alpha_R$ and a right $S$-action $\alpha_S$ of a $R$-$S$-bimodule, the biaction $(-)(-)(-):R \times B \times S \to B$ is defined as 

$$r b s \coloneqq \alpha_R(r, \alpha_S(b, s)) = \alpha_S(\alpha_R(r, b), s)$$

The biaction is trilinear because the left $R$-action and right $S$-action are bilinear. 

On the other hand, given an $R$-$S$-biaction $\alpha$ of a $R$-$S$-bimodule, the [[left action|left $R$-action]] is defined from the $R$-$S$-biaction as 

$$\alpha_R(r, b) \coloneqq r b 1_S$$

for all $r \in R$ and $b \in B$. It is a left action because 

$$\alpha_R(1_R, b) = 1_R b 1_S = m$$

$$\alpha_R(r_1, \alpha_L(r_2, b)) = r_1 (r_2 b 1_S) 1_S = (r_1 \cdot_R r_2) b (1_S \cdot_S 1_S) = (r_1 \cdot_R r_2) b 1_S = \alpha_R(r_1 \cdot_R r_2, b)$$

The [[right action|right $S$-action]] is defined from the $R$-$S$-biaction as 

$$\alpha_S(b, s) \coloneqq 1_R b s$$

for all $s \in S$ and $b \in B$. It is a right action because 

$$\alpha_S(b, 1_S) = 1_R b 1_S = m$$

$$\alpha_S(\alpha_S(b, s_1), s_2) = 1_R (1_R, b, s_1) s_2 = (1_R \cdot_R 1_R) b (s_1 \cdot_S s_2) = 1_S b (s_1 \cdot_S s_2) = \alpha_S(b, s_1 \cdot_S s_2)$$

The left $R$-action and right $S$-action satisfy the following identity: 

* for all $b \in B$, $r \in R$ and $s \in S$, $\alpha_R(r, \alpha_S(b, s)) = \alpha_S(\alpha_R(r, b), s)$. 

This is because when expanded out, the identity becomes:

$$\alpha(r, \alpha(1_R, b, s), 1_S) = \alpha(1_R, \alpha(r, b, 1_S), s)$$

$$(r \cdot_R 1_R) b (s \cdot_S 1_S) = (1_R \cdot_R r) b (1_S \cdot_S s)$$

$$r b s = r b s$$

The left $R$-action and right $S$-action are bilinear because the original biaction is trilinear. 

#### Bimodule homomorphisms

Let $R$ and $S$ be [[ring]]s. A **$R$-$S$-bimodule homomorphism** between two $R$-$S$-bimodules $A$ and $B$ is a function $f:A \to B$ such that for all $a_1 \in A$, $a_2 \in A$, $r_1 \in R$, $r_2 \in R$, $s_1 \in S$, and $s_2 \in T$, 

$$f(r_1 a_1 s_2 + r_2 a_2 s_2) = r_1 f(a_1) s_1 + r_2 f(a_2) s_2$$

### In general categories

Let $V$ be a [[closed monoidal category]]. Recall that for $C$ a category [[enriched category|enriched over]] $V$, a $C$-[[module]] is a $V$-functor $\rho : C \to V$. We think of the objects $\rho(a)$ for $a \in Obj(C)$ as the objects on which $C$ acts, and of $\rho(C(a,b))$ as the action of $C$ on these objects.

In this language a $C$-$D$ _bimodule_ for $V$-categories $C$ and $D$ is a $V$-functor

$$
  C^{op} \otimes D \to V
  \,.
$$

Such a functor is also called a profunctor or [[distributor]].

+--{.query}
Some points are in order. Strictly speaking, the construction of $C^{op}$ from a $V$-category $C$ requires that $V$ be symmetric (or at least braided) monoidal. It's possible to define $C$-$D$ bimodules without recourse to $C^{op}$, but then either that should be spelled out, or one should include a symmetry. (If the former is chosen, then closedness one on side might not be the best choice of assumption, in view of the next remark; a more natural choice might be biclosed monoidal.) 

Second: bimodules are not that much good unless you can compose them; for that one should add some cocompleteness assumptions to $V$ (with $\otimes$ cocontinuous in both arguments; biclosedness would ensure that), and consider smallness assumptions on the objects $C$, $D$, etc. ---Todd. 
=--

## Examples

* Let $V = Set$ and let $C = D$.  Then the hom functor $C(-, -):C^{op} \times C \to Set$ is a bimodule.  Bimodules can be thought of as a kind of generalized hom, giving a set of morphisms (or object of $V$) between an object of $C$ and an object of $D$.

* Let $\hat{C} = Set^{C^{op}}$; the objects of $\hat{C}$ are "generating functions" that assign to each object of $C$ a set.  Every bimodule $f:D^op \times C \to Set$ can be curried to give a Kleisli arrow $\tilde{f}:C \to \hat{D}$.  Composition of these arrows corresponds to convolution of the generating functions. 

  +--{.query}
  [[Todd Trimble|Todd]]: I am not sure what is trying to be said with regard to "convolution". I know about Day convolution, but this is not the same thing. 

  Also, with regard to "Kleisli arrow": I understand the intent, but one should proceed with caution since there is no global monad $C \mapsto \hat{C}$ to which Kleisli would refer. Again there are size issues that need attending to.
  =--

* Let $V = Vect$ and let $C = \mathbf{B}A_1$ and $D = \mathbf{B}A_2$ be two one-object $Vect$-enriched categories, whose endomorphism vector spaces are hence [[algebra]]s. Then a $C$-$D$ bimodule is a vector space $V$ with an action of $A_1$ on the left and and action of $A_2$ on the right.

## Properties

### The 1-category of bimodules and intertwiners

+-- {: .num_defn #1CategoryOfBimodulesAndIntertwiners}
###### Definition 

For $R$ a [[commutative ring]], write $BMod_R$ for the [[category]] whose

* [[objects]] are triples $(A,B,N)$ where $A$ and $B$ are $R$-[[associative algebra|algebras]] and where $N$ is an $A$-$B$-[[bimodule]];

* [[morphisms]] are triples $(f,g, \phi)$ consisting of two algebra [[homomorphisms]] $f \colon A \to A'$ and $B \colon B \to B'$ and an [[intertwiner]] of $A$-$B'$-bimodules $\phi \colon N \cdot g \to f \cdot N'$. This we may depict as a 

  $$
    \array{
      A &\stackrel{N}{\to}& B
      \\
      {}^{\mathllap{f}}\downarrow &\Downarrow_{\phi}& \downarrow^{\mathrlap{g}}
      \\
      A' &\stackrel{N'}{\to}& B'
    }  
    \,.
  $$

=--

+-- {: .num_remark }
###### Remark

As this notation suggests, $BMod_R$ is naturally the vertical category of a [[pseudo double category]] whose horizontal composition is given by tensor product of bimodules. 

=--


### The 2-category of algebras and bimodules
 {#AsMorphismsInA2Category}

Let $R$ be a [[commutative ring]] and consider bimodules over $R$-algebras.

+-- {: .num_prop #AlgebrasAndBimodules}
###### Proposition

There is a [[2-category]] whose 

* [[objects]] are $R$-[[algebras]];

* [[1-morphisms]] are bimodules;

* [[2-morphisms]] are [[intertwiners]].

The [[composition]] of 1-morphisms is given by the [[tensor product of modules]] over the middle algebra.

=--

+-- {: .num_prop}
###### Proposition

There is a [[2-functor]] from the above 2-category of algebras and bimodules to [[Cat]] which

* sends an $R$-algebra $A$ to its [[category of modules]] $Mod_A$;

* sends a $A_1$-$A_2$-bimodule $N$ to the [[tensor product]] [[functor]]

  $$
    (-)\otimes_{A_1} N
    \;\colon\;
    Mod_{A_1} \to Mod_{A_2}
  $$

* sends an [[intertwiner]] to the evident [[natural transformation]] of the above functors.

=--

+-- {: .num_prop}
###### Proposition

This construction has as its image precisely the [[colimit]]-preserving [[functors]] between [[categories of modules]].

=--

This is the [[Eilenberg-Watts theorem]].

+-- {: .num_remark}
###### Remark

In the context of [[higher category theory]]/[[higher algebra]] one may interpret this as says that the [[2-category]] of those [[2-modules]] over the given ring which are equivalent to a [[category of modules]] is that of $R$-algebras, bimodules and intertwiners. See also at _[[2-ring]]_.

=--

+-- {: .num_remark}
###### Remark

The 2-category of algebras and bimodules is an archtypical example for a [[2-category with proarrow equipment]], hence for a [[pseudo double category]] with niche-fillers. Or in the language of [[internal (infinity,1)-category]]-theory: it naturally induces the structure of a [[simplicial object]] in the [[(2,1)-category]] $Cat$ 

$$
  \left(
    \cdots
    \stackrel{\to}{\stackrel{\to}{\to}}
    X_1 
      \stackrel{\overset{\partial_1}{\to}}{\underset{\partial_0}{\to}}
    X_0
  \right)
  \in
  Cat^{\Delta^{op}}
$$

which satisfies the [[Segal conditions]]. Here 

$$
  X_0 =  Alg_R
$$ 

is the category of [[associative algebras]] and [[homomorphisms]] between them, while 

$$
  X_1 = BMod_R
$$ 

is the category of def. \ref{1CategoryOfBimodulesAndIntertwiners}, whose objects are pairs consisting of two algebras $A$ and $B$ and an $A$-$B$ bimodule $N$ between them, and whose morphisms are pairs consisting of two algebra homomorphisms $f \colon A \to A'$ and $g \colon B \to B'$ and an [[intertwiner]] $N \cdot (g) \to (f) \cdot N'$.

=--


### The $(\infty,2)$-category of $\infty$-algebras and $\infty$-bimodules
 {#Infinity2CategoryOfInfinityAlgebrasAndBimodules}

The above has a generalization to _[[(infinity,1)-bimodules]]_. See there for more.

## Related concepts

* [[Hilbert bimodule]]

* [[biaction]]

* [[amplimorphism]]

* [[bibundle]]

* [[(infinity,1)-bimodule]]

* [[bimodule category]]

* [[2-module]], [[2-ring]]



## References

The 2-category of bimodules in its incarnation as a [[2-category with proarrow equipment]] appears as example 2.3 in 

* [[Michael Shulman]], _Framed bicategories and monoidal fibrations_ ([arXiv:0706.1286](http://arxiv.org/abs/0706.1286))

Bimodules in [[homotopy theory]]/[[higher algebra]] are discussed in section 4.3 of 

* {#Lurie} [[Jacob Lurie]], _[[Higher Algebra]]_
 

For more on that see at _[[(∞,1)-bimodule]]_.

[[!redirects bimodules]]
[[!redirects bimodule homomorphism]]
[[!redirects bimodule homomorphisms]]
