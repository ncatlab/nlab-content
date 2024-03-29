## Idea 

A **non-unital operad** is a structure like an [[operad]] but without a unit or operadic identity. However, in contrast to operads where the multiplication operation substitutes $m$ operations simultaneously into a single $m$-ary operation, the primary operations for a non-unital operad are ones which substitute only one operation at a time. 

It is possible to package these individual substitution operations into a single operation, using not the [[plethysm|plethystic]] or substitution monoidal product (usually denoted $\circ$) but a certain lax monoidal product introduced below, called the *graft product*. At all events, it must be understood that the desired notion is not simply a species equipped $F$ equipped with an associative product $F \circ F \to F$, because that is not expressive enough. 

## Definitions  

There are various possible notions of non-unital operad; here we focus on the permutative and non-permutative cases. 

### Graft product of (permutative) species 

Let $FB$ be the monoidal groupoid of finite sets and bijections, where the monoidal product is obtained by restricting the coproduct on the category of finite sets. Let $F, G: FB \to V$ be (Joyal) species valued in a bicomplete symmetric monoidal closed category $V$. The **graft product** $F \ast G$ is defined by the formula 

$$(F \ast G)[S] = \sum_{T \subseteq S} F[S/T] \otimes G[T]$$ 

where $S/T$ denotes the pushout of $T \to 1$ along the inclusion $T \subseteq S$ in the category of finite sets. This includes the degenerate case where $T = 0$; in this case $S/0$ is the result of freely adjoining a point to $S$. In the theory of species, there is a fundamental differentiation functor $F \mapsto F'$ defined by the formula $F'[S] = F[S/0]$. 

The set $S/T$ has $T/T$ as distinguished basepoint, and if $U$ is complementary to $T$, we have natural bijections $S/T \cong U + \{T/T\} \cong U/0$. It follows that 

$$\array{
(F \ast G)[S] & \cong & \sum_{U + T = S} F[U + *] \otimes G[T] \\
 & \cong & \sum_{U + T = S} F'[U] \otimes G[T] \\
 & \cong & (F' \otimes G)[S]
}$$ 

where $\otimes$ refers to the usual Day convolution product on species, induced from the tensor product on $FB$. Since differentiation of species, 

$$V^{FB} \stackrel{- + *}{\to} V^{FB},$$ 

is cocontinuous, and since Day convolution is cocontinuous in each of its arguments, we see that 

$$F \ast G \cong F' \otimes G$$ 

is separately cocontinuous in each of its arguments $F$, $G$. (Contrast with the plethystic or substitution product on species $F \circ G$, which is cocontinuous in the first argument $F$ but not in the second $G$.) 

For $V = Set$, a structure of species $F \ast G$ is given by three data: 

* A tree obtained by grafting the root of a sprout (aka corolla) with leaf set $\tau$ to a leaf of another sprout with leaf set $\sigma$; 

* An element of $F[\sigma]$; 

* An element of $G[\tau]$. 

### Lax monoidal structure of graft product 

The graft poduct is not associative up to isomorphism, but there is a lax associativity. Specifically, we calculate (using a categorified [[Leibniz rule]]) 

$$\array{
(F \ast G) \ast H & \cong & (F' \otimes G)' \otimes H \\
 & \cong & F'' \otimes G \otimes H + F' \otimes G' \otimes H \\
 & \cong & F'' \otimes G \otimes H + F \ast (G \ast H)
}$$ 

so that there is a noninvertible associativity (an inclusion)  

$$\alpha_{F G H}: F \ast (G \ast H) \to (F \ast G) \ast H$$ 

which is natural in each of its arguments $F$, $G$, and $H$, and which satisfies an evident pentagon coherence condition. Additionally (although we won't really need this here), there is a lax monoidal unit, defined as the species $X$ for which $X[S]$ is the monoidal unit of $V$ if $card(S) = 1$, else $X[S]$ is initial, for which we have evident natural maps 

$$\lambda_F: X \ast F \to F, \qquad \rho_F: F \ast X \to F$$

The first map $\lambda_F$ is invertible, but the second is not: its component at a finite set $S$ is the codiagonal 

$$\nabla: S \cdot F[S] \to F[S]$$ 

However, the standard unit coherence conditions for monoidal categories hold. We may call such a structure, relaxing the condition of invertibility of $\alpha$ and $\rho$ but retaining the usual naturality and coherence conditions, a **lax monoidal category**. 

In the sequel, $F^{\ast n}$ will denote the iterated graft product defined recursively by 

$$F^{\ast 0} = X, \qquad F^{\ast (n+1)} = F^{\ast n} \ast F$$ 

so that all parentheses in $F^{\ast n}$ are to the left. We state without proof the following partial coherence theorem: 

+-- {: .num_prop} 
###### Proposition 
Any two maps 
$$F^{\ast m} \ast F^{\ast n} \to F^{\ast (m+n)}$$ 
definable in the language of lax monoidal categories are equal. We denote this map by $\alpha_{m n}$. 
=--

### Permutative non-unital operads 

+-- {: .num_defn} 
###### Definition 
A (permutative) _non-unital operad_ in a [[cosmos]] $V$ is a [[species]] $F: FB^{op} \to V$ equipped with a multiplication $m: F \ast F \to F$, satisfying the following two associativity axioms: 

1. $$\array{
F \ast (F \ast F) & \stackrel{1 \ast m}{\to} & F \ast F & \\
\alpha \downarrow & & & \searrow m \\
(F \ast F) \ast F & \underset{m \ast 1}{\to} F \ast F & \underset{m}{\to} & F
}$$ 
commutes; 

1. The two composites $F'' \otimes F^{\otimes 2} \to F$ named in 
$$F'' \otimes (F \otimes F) \stackrel{\overset{\sigma}{\to}}{\underset{1}{\to}} F'' \otimes (F \otimes F) \stackrel{i}{\to} (F \ast F) \ast F \stackrel{m(m \ast 1)}{\to} F$$ 
commute. Here $i$ denotes the inclusion complementary to $\alpha: F \ast (F \ast F) \to (F \ast F) \ast F$, and $\sigma$ is the involution 
$$\sigma_1 \otimes \sigma_2: F'' \otimes F^{\otimes 2} \to F'' \otimes F^{\otimes 2}$$ 
where $\sigma: F'' \to F''$ is the natural involution on the second derivative
$$(-)'' = (- + 2)*: V^{FB} \to V^{FB}$$ 
induced by the nonidentity involution $2 \to 2$, and $\sigma_2$ is the symmetry isomorphism $F^{\otimes 2} \to F^{\otimes 2}$. 

=-- 

Of course the notion can be reformulated perfectly well in a general symmetric monoidal category; the use of coproducts just makes for a more efficient packaging. 

### Graft product of (non-permutative) species 

A non-permutative species in a [[monoidally cocomplete category]] $V$ is simply an $\mathbb{N}$-[[graded object]] in $V$, which we may think of as equivalent to a functor $\mathbb{N} \to V$ from the monoidal groupoid of finite [[linear orders]], with the monoidal product given by restriction of the [[ordinal sum]] to the [[core]] groupoid. If $S$ is a finite linear order and $T = [a, b] \subseteq S$ is a [[subinterval]] of $S$, then we may again define $S/T$ via a pushout construction in the category of finite linear orders, and define a corresponding graft product by the formula 

$$(F \ast G)[S] = \sum_{subintervals T} F[S/T] \otimes G[T].$$ 

This graft product shares certain formal properties with the permutative graft product defined above, such as the fact that it is a lax monoidal product. A triple graft product $(F \ast G) \ast H$ cab be decomposed as a coproduct of parts, the first being  

$$F \ast (G \ast H)[S] = \sum_{subintervals T_1 \subseteq T_2} F[S/T_2] \otimes G[T_2/T_1] \otimes H[T_1]$$ 

and the second being 

$$\sum_{subint. T_1, T_2: T_1 \cap T_2 = \emptyset} F[S/(T_1, T_2)] \otimes G[T_1] \otimes H[T_2]$$ 

where $S/(T_1, T_2)$ denotes the pushout of the inclusion $T_1 + T_2 \hookrightarrow S$ along the quotient $! + !: T_1 + T_2 \to 1 + 1$. By interchanging the roles of $T_1$ and $T_2$, we get a nontrivial involution on the second part. 

To be continued... 