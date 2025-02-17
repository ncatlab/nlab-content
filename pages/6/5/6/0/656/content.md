
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _bimodule_ is a [[module]] in two compatible ways over two [[rings]].

## Definition

### Over a ring

#### With a left action and a right action

Given two [[rings]] $R$ and $S$, a $R$-$S$-bimodule is an [[abelian group]] $B$ with a [[bilinear function|bilinear]] [[left action|left $R$-action]] $\alpha_R:R \times B \to B$ and a bilinear [[right action|right $S$-action]] $\alpha_S:B \times S \to B$ such that for all $r \in R$, $b \in B$, and $s \in S$, $\alpha_R(r, \alpha_S(b, s)) = \alpha_S(\alpha_R(r, b), s)$. 

#### With a biaction

Equivalently, given two [[rings]] $R$ and $S$, a $R$-$S$-bimodule is an [[abelian group]] $B$ with a [[multilinear function|trilinear]] [[biaction|$R$-$S$-biaction]], a function $(-)(-)(-):R \times B \times S \to B$ such that 

* for all $b \in B$, $1_R b 1_S = b$

* for all $b \in B$, $r_1 \in R$, $r_2 \in R$, $s_1 \in S$, $s_2 \in S$, $r_1 (r_2 b s_1) s_2 = (r_1 \cdot_R r_2) b (s_1 \cdot_S s_2)$

* for all $r_1 \in R$, $r_2 \in R$, $b \in B$, $s \in S$, $(r_1 + r_2) b s = r_1 b s + r_2 b s$

* for all $r \in R$, $b_1 \in B$, $b_2 \in B$, $s \in S$, $r (b_1 + b_2) s = r b_1 s + r b_2 s$

* for all $r \in R$, $b \in B$, $s_1 \in S$, $s_2 \in S$, $r b (s_1 + s_2) = r b s_1 + r b s_2$

representing simultaneous left multiplication by scalars $r \in R$ and right multiplication by scalars $s \in S$. 

#### Over a fixed ring

In the case $R=S$ the category of $(R,R)$-bimodules can be described as the category of [[abelian group object | abelian group objects]] in the slice category of (not necessarily commutative) rings over $R$. See [[Beck module]] for a proof.

### Over a monoid in a monoidal category

We can define in more generality what is a $(A,B)$-bimodule in a monoidal category $(\mathcal{C},\otimes,I)$ where $(A,\nabla^{A},\eta^{A})$ and $(B,\nabla^{B},\eta^{B})$ are two monoids. It is given by:

* An object $X \in \mathcal{C}$
* A left-action $l:A \otimes X \rightarrow X$
* A right-action $r:X \otimes B \rightarrow X$

such that:

* $(X,l)$ is a [[module over a monoid| left module]]
* $(X,r)$ is a [[module over a monoid| right module]]

and moreover this diagram commutes:
\begin{tikzcd}
A \otimes X \otimes B \arrow[d, "l \otimes B"'] \arrow[rr, "A \otimes r"] &  & A \otimes X \arrow[d, "l"] \\
X \otimes B \arrow[rr, "r"']                                              &  & X                         
\end{tikzcd}

## Properties

### Biactions, left actions, and right actions

Let $R$ and $S$ be [[ring]]s, and let $B$ be a $R$-$S$-bimodule. 

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

### Linear maps

Let $R$ and $S$ be [[rings]]. A **$R$-$S$-linear map** or **$R$-$S$-bimodule homomorphism** between two $R$-$S$-bimodules $A$ and $B$ is an abelian group [[homomorphism]] $f:A \to B$ such that for all $a \in A$, $r \in R$, and $s \in S$,

$$f(r a s) = r f(a) s$$

A $R$-$S$-linear map $f:A \to B$ is [[monic]] or an **$R$-$S$-bimodule monomorphism** if for every other $R$-$S$-bimodule $C$ and $R$-$S$-linear maps $h:C \to A$ and $k:C \to A$, $f \circ h = f \circ k$ implies that $h = k$. 

A **sub-$R$-$S$-bimodule** of a $R$-$S$-bimodule $B$ is a $R$-$S$-bimodule $A$ with a [[monic]] linear map $i:A \hookrightarrow B$. 

A $R$-$S$-linear map $f:A \to B$ is [[invertible]] or an **$R$-$S$-bimodule isomorphism** if there exists a $R$-$S$-linear map $g:B \to A$ such that $g \circ f = id_A$ and $f \circ g = id_B$, where $id_A$ and $id_B$ are the identity linear maps on $A$ and $B$ respectively. 

### Tensor product of bimodules

Given [[rings]] $R, S, T$ and an $R$-$S$ bimodule $A$ and an $S$-$T$ bimodule $B$, the tensor product of $A$ and $B$ is formed as a [[quotient]] $A \otimes_N B$ of the [[tensor product of abelian groups]] $A\otimes B$. This is a special case of a more general construction:  

Given three monoids $M,N,P$ in a monoidal category $(\mathcal{C},\otimes,I)$, a $M$-$N$-bimodules $A$ and a $N$-$P$-bimodule $B$, we denote the monoid actions as $\lambda^{A}:M \otimes A \rightarrow A$, $\rho^{A}:A \otimes N \rightarrow N$, $\lambda^{B}:N \otimes B \rightarrow N$ and $\rho^{B}:B \otimes P \rightarrow P$. The tensor product, $A \otimes_{N} B$ is defined as this coequalizer:

\begin{tikzcd}
A \otimes N \otimes B \arrow[rr, "\rho^{A} \otimes B", shift left] \arrow[rr, "A \otimes \lambda^{B}"', shift right] &  & A \otimes B \arrow[r, "\pi_{A,B}"] & A \otimes_{N} B
\end{tikzcd}

We suppose moreover that this coequalizer is preserved by tensoring on the left by $M$ and tensoring on the right by $P$, meaning that these diagrams are coequalizer diagrams:
\begin{tikzcd}
M \otimes A \otimes N \otimes B \arrow[rr, "M \otimes \rho^{A} \otimes B", shift left] \arrow[rr, "M \otimes A \otimes \lambda^{B}"', shift right] &  & M \otimes A \otimes B \arrow[rr, "{M \otimes \pi_{A,B}}"] &  & M \otimes A \otimes_{N} B
\end{tikzcd}
\begin{tikzcd}
A \otimes N \otimes B \otimes P \arrow[rr, "\rho^{A} \otimes B \otimes P", shift left] \arrow[rr, "A \otimes \lambda^{B} \otimes P"', shift right] &  & A \otimes B \otimes P \arrow[rr, "{\pi_{A,B} \otimes P}"] &  & A \otimes_{N} B \otimes P
\end{tikzcd}
$A \otimes B$ becomes a $M$-$P$-bimodule with left action defined by the following diagram:
\begin{tikzcd}
M \otimes A \otimes N \otimes B \arrow[rr, "M \otimes \rho^{A} \otimes B", shift left] \arrow[rr, "M \otimes A \otimes \lambda^{B}"', shift right] \arrow[d, "\lambda^{A} \otimes N \otimes B"'] &  & M \otimes A \otimes B \arrow[rr, "{M \otimes \pi_{A,B}}"] \arrow[d, "\lambda^{A} \otimes B"'] &  & M \otimes A \otimes_{N} B \arrow[d, "\lambda^{A \otimes_{N}B}", dashed] \\
A \otimes N \otimes B \arrow[rr, "\rho^{A} \otimes B", shift left] \arrow[rr, "A \otimes \lambda^{B}"', shift right]                                                                             &  & A \otimes B \arrow[rr, "{\pi_{A,B}}"']                                                        &  & A \otimes_{N} B                                                        
\end{tikzcd}
and right action defined by the following diagram:

\begin{tikzcd}
A \otimes N \otimes B \otimes P \arrow[rr, "\rho^{A} \otimes B \otimes P", shift left] \arrow[rr, "A \otimes \lambda^{B} \otimes P"', shift right] \arrow[d, "A \otimes N \otimes \rho^{B}"'] &  & A \otimes B \otimes P \arrow[rr, "{\pi_{A,B} \otimes P}"] \arrow[d, "A \otimes \rho^{B}"'] &  & A \otimes_{N} B \otimes P \arrow[d, "\rho^{A \otimes_{N}B}", dashed] \\
A \otimes N \otimes B \arrow[rr, "\rho^{A} \otimes B", shift left] \arrow[rr, "A \otimes \lambda^{B}"', shift right]                                                                          &  & A \otimes B \arrow[rr, "{\pi_{A,B}}"']                                                     &  & A \otimes_{N} B                                                     
\end{tikzcd} 

Assuming all requisite [[reflexive coequalizer|(reflective) coequalizers]] exist, universal property arguments guarantee associativity isomorphisms of type 

$$(A \otimes_N B) \otimes_P C \to A \otimes_N (B \otimes_P C).$$ 

In fact, this tensor product defines composition in a [[bicategory]] where objects or 0-cells are monoids in a monoidal category, where 1-cells $A$ from $R$ to $S$ are $R$-$S$ bimodules, and where 2-cells from $A$ to $B$ are morphisms of $R$-$S$ bimodules. 

This in turn can be seen as a special case of a bicategory of [[profunctors]] [[enriched category|enriched]] in a [[monoidal category]] with suitably nice cocompleteness properties -- see [[monoidally cocomplete category]] and [[Benabou cosmos]]. 

### Two-sided ideals of a ring

Every ring $R$ is a $R$-$R$-bimodule, with the [[biaction]] $(-)(-)(-):R \times R \times R \to R$ defined by the ternary product $a b c \coloneqq a \cdot b \cdot c$ for elements $a \in R$, $b \in R$, $c \in R$. 

Given a ring $R$, a **[[two-sided ideal]]** of $R$ is a sub-$R$-$R$-bimodule of $R$. 

### Rings over a ring

Let $R$ be a [[ring]]. An **$R$-ring** $S$ is a $R$-$R$-bimodule with a [[bilinear function]] $(-)\cdot(-):S \times S \to S$ and an element $1 \in S$ such that $(S, \cdot, 1)$ forms a [[monoid]]. 

## Categories of bimodules

### The 1-category of bimodules and intertwiners

+-- {: .num_defn #1CategoryOfBimodulesAndIntertwiners}
###### Definition 

Write $BMod$ for the [[category]] whose

* [[objects]] are triples $(R,S,B)$ where $R$ and $S$ are [[rings]] and where $B$ is an $R$-$S$-bimodule;

* [[morphisms]] are triples $(f,g, \phi)$ consisting of two ring [[homomorphisms]] $f \colon R \to R'$ and $g \colon S \to S'$ and an [[intertwiner]] of $R$-$S'$-bimodules $\phi \colon B \cdot g \to f \cdot B'$. This we may depict as a 

  $$
    \array{
      R &\stackrel{B}{\to}& S
      \\
      {}^{\mathllap{f}}\downarrow &\Downarrow_{\phi}& \downarrow^{\mathrlap{g}}
      \\
      R' &\stackrel{B'}{\to}& S'
    }  
    \,.
  $$

=--

+-- {: .num_remark }
###### Remark

As this notation suggests, $BMod$ is naturally the vertical category of a [[pseudo double category]] whose horizontal composition is given by tensor product of bimodules. 

=--

### The 2-category of rings, bimodules, and intertwiners
 {#AsMorphismsInA2Category}

Consider bimodules over [[rings]].

+-- {: .num_prop #AlgebrasAndBimodules}
###### Proposition

There is a [[2-category]] whose 

* [[objects]] are [[rings]];

* [[1-morphisms]] are bimodules;

* [[2-morphisms]] are [[intertwiners]].

The [[composition]] of 1-morphisms is given by the [[tensor product of modules]] over the middle algebra.

=--

+-- {: .num_prop}
###### Proposition

There is a [[2-functor]] from the above 2-category of rings and bimodules to [[Cat]] which

* sends an ring $R$ to its [[category of modules]] $Mod_R$;

* sends a $R$-$S$-bimodule $B$ to the [[tensor product]] [[functor]]

  $$
    (-)\otimes_{R} B
    \;\colon\;
    Mod_{R} \to Mod_{S}
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

In the context of [[higher category theory]]/[[higher algebra]] one may interpret this as says that the [[2-category]] of those [[2-modules]] over the given ring which are equivalent to a [[category of modules]] is that of rings, bimodules and intertwiners. See also at _[[2-ring]]_.

=--

+-- {: .num_remark}
###### Remark

The 2-category of rings and bimodules is an archtypical example for a [[2-category with proarrow equipment]], hence for a [[pseudo double category]] with niche-fillers. Or in the language of [[internal (infinity,1)-category]]-theory: it naturally induces the structure of a [[simplicial object]] in the [[(2,1)-category]] $Cat$ 

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
  X_0 =  Ring
$$ 

is the category of [[rings]] and [[homomorphisms]] between them, while 

$$
  X_1 = BMod
$$ 

is the category of def. \ref{1CategoryOfBimodulesAndIntertwiners}, whose objects are pairs consisting of two rings $A$ and $B$ and an $A$-$B$ bimodule $N$ between them, and whose morphisms are pairs consisting of two ring homomorphisms $f \colon A \to A'$ and $g \colon B \to B'$ and an [[intertwiner]] $N \cdot (g) \to (f) \cdot N'$.

=--


### The $(\infty,2)$-category of $\infty$-algebras and $\infty$-bimodules
 {#Infinity2CategoryOfInfinityAlgebrasAndBimodules}

The above has a generalization to _[[(infinity,1)-bimodules]]_. See there for more.

## Related concepts

* [[module over a monad]]

* [[bimodule object]]

* [[quotient bimodule]]

* [[Hilbert bimodule]]

* [[Noetherian bimodule]]

* [[Artinian bimodule]]

* [[Soergel bimodule]]

* [[two-sided ideal]]

* [[category of two-sided ideals in a ring]]

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
[[!redirects bimodule monomorphism]]
[[!redirects bimodule monomorphisms]]
[[!redirects bimodule isomorphism]]
[[!redirects bimodule isomorphisms]]

[[!redirects tensor product of bimodules]]
[[!redirects tensor products of bimodules]]

[[!redirects subbimodule]]
[[!redirects subbimodules]]
