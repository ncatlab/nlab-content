
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The Leray-Hirsch theorem states sufficient fiberwise condition for the [[ordinary cohomology]] of the total space of a [[fiber bundle]] with [[coefficients]] in a [[commutative ring]] to be [[free module]] over the [[cohomology ring]] of the base space.

An important consequence is the [[Thom isomorphism]].

## Statement

Let 

\[
  \label{TheFiberBundles}
  \array{
     F &\stackrel{\iota}{\hookrightarrow}& Y
     \\
     && \downarrow^{\mathrlap{p}}
     \\
     && X
  }
\]

be an $F$-[[fiber bundle]] (in [[Top]]) of [[topological spaces]] that admit the [[mathematical structure|structure]] of finite [[CW-complexes]].


### In ordinary cohomology 
 {#StatementInOrdinaryCohomology}

Let $R$ be a [[commutative ring]] and write $H^\bullet(-;\,R)$ for the [[cohomology rings]] of [[ordinary cohomology]] with [[coefficients]] in $R$.

If there exists 

* a [[finite set]] of elements 

  $$
    \alpha_i \in H^\bullet(Y,R)\;,\;\;\;\; i \in \{1, 2, \cdots, n\}
  $$

  in the [[ordinary cohomology]] of $Y$ with [[coefficients]] in $R$, 

such that 

* for each point $x \in X$ the restriction ([[pullback in cohomology|pullback]] along $\iota$) of the $\alpha_i$ to the [[fiber]] $F_x \hookrightarrow Y$ 

  1. is $R$-[[linearly independent]] 

  1. their $R$-[[linear span]] is [[isomorphism|isomorphic]] to the [[cohomology group]] $H^\bullet(F,R)$ of the fiber

     $$
       H^\bullet(F;\, R)
       \simeq
       R
       \langle 
         \iota_x^\ast \alpha_1, \cdots, \iota_x^\ast \alpha_n
       \rangle
       \;\;\;\;
       \in R Mod
      $$

  (i.e. a [[free module]] over $R$)

then:

1. the $\{\alpha_1, \cdots, \alpha_n\}$ themselves are $H^\bullet(X;\,R)$-[[linearly independent]],

1. their $H^\bullet(X;\,R)$-[[linear span]] gives the [[cohomology group]] of the total space $Y$:

   $$
     H^\bullet(Y;\,R) 
     \;\simeq\; 
     H^\bullet(X;\,R)
     \langle 
       \alpha_1, \cdots,\alpha_n
     \rangle
     \;\;\;\;\;
     \in 
     \;
     H^\bullet(X;\, R) Mod
     \,,
   $$

   via the [[isomorphism]]

   $$
     H^\bullet(X;\, R) 
       \otimes_R 
     H^\bullet(F;\, R)
       \stackrel{\simeq}{\longrightarrow}
     H^\bullet(Y;\, R) 
   $$

   given by [[pullback in cohomology|pulling back]] classes from the base space and there forming their [[cup product]] with these generators on the total space:

   $$
     \underset{i,j}{\sum} c_i \otimes \iota^\ast(\alpha_j)
       \mapsto 
     \underset{i,j}{\sum}
     p^\ast(c_i) \cup \alpha_j
     \,.
   $$


\linebreak

### In generalized cohomology
 {#StatementInGeneralizedCohomology}

The statement generalizes verbatim from [[ordinary cohomology]] to any [[multiplicative cohomology theory|multiplicative]] [[Whitehead-generalized cohomology theory]] $E$ ([Conner-Floyd 66, theorem 7,4](#ConnerFloyd66), attributed there to [[Albrecht Dold]], review in [Tamaki-Kono 06, Section 3.1](#TamakiKono06)):

Let $E$ be a [[multiplicative cohomology theory|multiplicative]] [[Whitehead-generalized cohomology theory]] and write 

* $E^\bullet(-)$ for its [[cohomology rings]];

* $E_{-\bullet} \;\coloneqq \; E^\bullet(\ast)$ for its [[ground ring]]

If there exists 

* a [[finite set]] of elements 

  \[
    \label{GeneratorsInELerayHirschTheorem}
    \alpha_i \;\in\; E^\bullet(Y)\;,\;\;\;\; i \in \{1, 2, \cdots, n\}
  \]

  in the [[ordinary cohomology]] of the total space $Y$, 

such that 

* for each point $x \in X$ the restriction ([[pullback in cohomology|pullback]] along $\iota$) of the $\alpha_i$ to the [[fiber]] $F_x \hookrightarrow Y$ 

  1. is $E_{-\bullet}$-[[linearly independent]] 

  1. their $E_{-\bullet}$-[[linear span]] is [[isomorphism|isomorphic]] to the [[cohomology group]] $E^\bullet(F)$ of the fiber

     \[
       \label{AssumptionOnFiberCohomologyInELerayHirschTheorem}
       H^\bullet(F;\, R)
       \simeq
       R
       \langle 
         \iota_x^\ast \alpha_1, \cdots, \iota_x^\ast \alpha_n 
       \rangle
       \;\;\;\;
       \in E_{-\bullet} Mod
      \]

   (i.e. a [[free module]] over $E_{-\bullet}$)

then:

1. the $\{\alpha_1, \cdots, \alpha_n\}$ themselves are $E^\bullet(X)$-[[linearly independent]],

1. their $E^\bullet(X)$-[[linear span]] gives the [[cohomology group]] of the total space $Y$:

   $$
     E^\bullet(Y)
     \;\simeq\; 
     E^\bullet(X)
     \langle 
       \alpha_1, \cdots,\alpha_n
     \rangle
     \;\;\;\;\;
     \in 
     \;
     E^\bullet(X) Mod
     \,,
   $$

   via the [[isomorphism]]

   $$
     E^\bullet(X)
       \otimes_{E_{-\bullet}}
     E^\bullet(F)
       \stackrel{\simeq}{\longrightarrow}
     E^\bullet(Y)
   $$

   given by [[pullback in cohomology|pulling back]] classes from the base space and there forming their [[cup product]] with these generators on the total space:

   $$
     \underset{i,j}{\sum} c_i \otimes \iota^\ast(\alpha_j)
       \mapsto 
     \underset{i,j}{\sum}
     p^\ast(c_i) \cup \alpha_j
     \,.
   $$

## Examples

### Complex-oriented cohomology of the twistor fibration

Let $E$ be a [[Whitehead-generalized cohomology theory]] equipped with [[complex oriented cohomology|complex orientation]] in the form of a [[first Chern class|first]] [[Conner-Floyd-Chern class]] 

$$
  c^E_1
  \;\in\;
  {\widetilde E}{}^2\big( \mathbb{C}P^\infty \big)
    \longrightarrow
  {\widetilde E}{}^2\big( \mathbb{C}P^n \big)
  \,.
$$

Then, for $n \in \mathbb{N}$, the $E$-[[cohomology ring]] of the [[complex projective space]] $\mathbb{C}P^n$ is (see [there](complex+oriented+cohomology+theory#CohomologyRingOfBU1))

$$
  E^\bullet
  \big(
    \mathbb{C}P^n 
  \big)
  \;\simeq\;
  E_{-\bullet}
  \big[
    c^E_1
  \big]  
  \big/
  \big(
    c^E_1 
  \big)^{n+1}
  \;\;\;
  \in
  \;
  E_{-\bullet} Algebras
  \,,
$$

whence the [[cohomology group]] is

\[
  \label{ECohomologyGroupOfComplexProjectiveSpace}
  E^\bullet
  \big(
    \mathbb{C}P^n 
  \big)
  \;\simeq\;
  E_{-\bullet}
  \big\langle
    1,\,
    c^E_1,\,
    \big(c^E_1\big)^2,\,
    \cdots
    ,\,
    \big(c^E_1\big)^n,\,
  \big\rangle
  \;\;\;
  \in
  \;
  E_{-\bullet} Modules
  \,.
\]

For each $n = 2 k + 1$ these are [[Riemann sphere]]
$\mathbb{H}^\times/\mathbb{C}^\times = \mathbb{C}P^1$-[[fiber bundles]]

$$
  \array{
    \mathbb{C}P^1
    &
    \longrightarrow
    &
    \mathbb{C}^{2k+1}
    & 
    =
    &
    \big(
      \mathbb{C}^{2k+2} \setminus \{0\}
    \big)
    \big/
    \mathbb{C}^\times
    \\
    &&
    \big\downarrow
    &&
    \big\downarrow 
    {}^{ 
       \mathrlap{
       v \cdot \mathbb{C}^\times  
         \mapsto
       v \cdot \mathbb{H}^\times  
       }
    }
    \\
    && 
    \mathbb{H}P^k
    &
    =
    &
    \big(
      \mathbb{H}^{k+1} \setminus \{0\}
    \big)
    \big/
    \mathbb{H}^\times
  }
$$

over [[quaternionic projective space]] $\mathbb{H}P^{k}$,
whose [[fiber]]-inclusion is ([[homotopy|homotopic]] to) the canonical inclusion $\mathbb{C}P^1 \hookrightarrow \mathbb{C}P^n$ (see [there](complex+projective+space#Definition)).

For $k = 1$ this is also known as the _[[twistor fibration]]_.
For $k = \infty$ this is the fibration of [[classifying spaces]]

$$
  \array{
    SU(2)/\mathrm{U}(1)
    &\longrightarrow&
    B \mathrm{U}(1)
    \\
    && 
    \big\downarrow
     {}^{\mathrlap{
       B\big( z \mapsto diag(z,z^\ast)  \big)
     }}
    \\
    &&
    B SU(2)
  }
$$

Therefore, by (eq:ECohomologyGroupOfComplexProjectiveSpace), the assumption (eq:AssumptionOnFiberCohomologyInELerayHirschTheorem) of the $E$-Leray-Hirsch theorem ([above](#StatementInGeneralizedCohomology)) is met if we take the classes (eq:GeneratorsInELerayHirschTheorem) to be the [[cup product|cup powers]] $(c^E_1)^n$, and the $E$-Leray-Hirsch theorem says that:

(...)



(...)

## Related concepts

* [[Thom isomorphism]]

## References

### For ordinary cohomology

Review of the theorem for [[ordinary cohomology]]:

* [[Alan Hatcher]], _[Algebraic topology](https://www.math.cornell.edu/~hatcher/AT/ATpage.html)_, 2002, theorem 4D.1 on p. 432 ([pdf](https://www.math.cornell.edu/~hatcher/AT/ATch4.4.pdf))

* {#Ebert12} [[Johannes Ebert]], section 2.3 of _A lecture course on Cobordism Theory_, 2012 ([pdf](http://wwwmath.uni-muenster.de/u/jeber_02/skripten/bordism-skript.pdf)) 

### For generalized cohomology

Discussion for [[Whitehead-generalized cohomology|Whitehead-generalized]] [[multiplicative cohomology theories]]:

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], Theorem 7.4 of: _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__, Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))

* {#TamakiKono06} [[Dai Tamaki]], [[Akira Kono]], Section 3.1 in: _Generalized Cohomology_, Translations of Mathematical Monographs, American Mathematical Society, 2006 ([ISBN: 978-0-8218-3514-2](https://bookstore.ams.org/mmono-230))
