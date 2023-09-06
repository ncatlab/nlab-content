
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
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

A [[cohomology theory]] $E$ is called _multiplicative_ if each [[graded module|graded]] [[abelian group|abelian]] $E$-[[cohomology group]] $E^\bullet(X)$ is compatibly equipped with the structure of a [[graded ring]]. 

The corresponding [[Brown representability theorem|representing]] [[spectra]] are [[ring spectra]].

## Definition

+-- {: .num_defn #PairingOfUnreducedCohomologyTheories}
###### Definition

Let $E_1, E_2, E_3$ be three unreduced [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology theories]] ([def.](generalized+cohomology+theory#GeneralizedCohomologyTheory)). A **pairing of cohomology theories** 

$$
  \mu \;\colon\; E_1 \Box E_2 \longrightarrow E_3
$$

is a [[natural transformation]] (of functors on $(Top_{CW}^{\hookrightarrow}\times Top_{CW}^{\hookrightarrow})^{op} $) of the form

$$
  \mu_{n_1,n_2}
   \;\colon\;
  E_1^{n_1}(X,A)
    \otimes
  E_2^{n_2}(Y,B)
    \longrightarrow
  E_3^{n_1 + n_2}(X\times Y \;,\; A\times Y \cup X \times B)
$$

such that this is compatible with the connecting homomorphisms $\delta_i$ of $E_i$, in that the following are [[commuting squares]]

$$
  \array{
    E_1^{n_1}(A)
      \otimes 
    E_2^{n_2}(Y,B)
      &\overset{\delta_1 \otimes id_2}{\longrightarrow}&
    E_1^{n_1+1}(X,A) \otimes E_2^{n_2}(Y,B)
    \\
    {}^{\mathllap{\mu_{n_1,n_2}}}\downarrow && \downarrow^{\mathrlap{\mu_{n_1+1, n_2}}}
    \\
   \underoverset
     {E_3^{n_1 + n_2}(A \times Y  \cup  X \times B , X \times B)}
     {E_3^{n_1 + n_2}(A \times Y, A \times B)}
     {\simeq}
     &\overset{\delta_3}{\longrightarrow}&
     E_3^{n_1 + n_2+ 1}(X \times Y, A \times B)
  }
$$

and

$$
  \array{
    E_1^{n_1}(X,A)
      \otimes 
    E_2^{n_2}(B)
      &\overset{(-1)^{n_1} id_1 \otimes \delta_2}{\longrightarrow}&
    E_1^{n_1+1}(X,A) \otimes E_2^{n_2}(Y,B)
    \\
    {}^{\mathllap{\mu_{n_1,n_2}}}\downarrow 
      && 
    \downarrow^{\mathrlap{\mu_{n_1, n_2 + 1}}}
    \\
   \underoverset
     {E_3^{n_1 + n_2}(A \times Y \cup X \times B , A \times Y)}
     {E_3^{n_1 + n_2}(X \times B, A \times B)}
     {\simeq}
     &\overset{\delta_3}{\longrightarrow}&
     E_3^{n_1 + n_2+ 1}(X \times Y, A \times B)
  }
  \,,
$$

where the isomorphisms in the bottom left are the [excision isomorphisms](generalized+cohomology+theory##excision).

=--

+-- {: .num_defn #MultiplicativeCohomologyTheory}
###### Definition

An (unreduced) **multiplicative cohomology theory** is an unreduced [[generalized cohomology theory]] theory $E$ ([def.](generalized+cohomology+theory#GeneralizedCohomologyTheory)) equipped with 

1. (external multiplication) a pairing (def. \ref{PairingOfUnreducedCohomologyTheories}) of the form $\mu \;\colon\; E \Box E  \longrightarrow E$;

1. (unit) an element $1 \in E^0(\ast)$

such that

1. ([[associativity]]) $\mu \circ (id \otimes \mu) = \mu \circ (\mu \otimes id)$;

2. ([[unitality]]) $\mu(1\otimes x) = \mu(x \otimes 1) = x$ for all $x \in E^n(X,A)$.

The mulitplicative cohomology theory is called **commutative** (often considered by default) if in addition

* **(graded commutativity)** 

  $$  
    \array{
      E^{n_1}(X,A) \otimes E^{n_2}(Y,B)
      &\overset{(u \otimes v) \mapsto (-1)^{n_1 n_2} (v \otimes u) }{\longrightarrow}& 
      E^{n_2}(Y,B) \otimes E^{n_1}(X,A)
      \\
      {}^{\mathllap{\mu_{n_1,n_2}}}\downarrow && \downarrow^{\mathrlap{\mu_{n_1,n_2}}}
      \\
      E^{n_1 + n_2}( X \times Y , A \times Y \cup X \times B)
      &\underset{(switch_{(X,A), (Y,B)})^\ast}{\longrightarrow}&
      E^{n_1 + n_2}( Y \times X , B \times X \cup Y \times A)
    }
    \,.
  $$

{#InternalMultiplicationOfMultiplicativeCohomologyTheory} Given a multiplicative cohomology theory $(E, \mu, 1)$, its **[[cup product]]** is the composite of the above external multiplication with pullback along the [[diagonal]] maps $\Delta_{(X,A)} \colon (X,A) \longrightarrow (X\times X, A \times X \cup X \times A)$;

$$
  (-) \cup (-)
   \;\colon\;
  E^{n_1}(X,A)
   \otimes
  E^{n_2}(X,A)
    \overset{\mu_{n_1,n_2}}{\longrightarrow}
  E^{n_1 + n_2}( X \times X, \; A \times X \cup X \times A)
    \overset{\Delta^\ast_{(X,A)}}{\longrightarrow}
  E^{n_1 + n_2}(X, \; A \cup B)
  \,.
$$

=--

e.g. ([Tamaki-Kono 06, II.6](#TamakiKono06))



## Properties

### Ring and module structure on cohomology groups
 {#RingAndModuleStructureOnCohomologyGroups}

+-- {: .num_prop #RingAndModuleStructureOnCohomologyGroupsOfMultiplicativeCohomplogyTheory}
###### Proposition

Let $(E,\mu,1)$ be a multiplicative cohomology theory, def. \ref{MultiplicativeCohomologyTheory}. Then

1. For every space $X$ the [cup product](#InternalMultiplicationOfMultiplicativeCohomologyTheory) gives $E^\bullet(X)$ the structure of a $\mathbb{Z}$-[[graded ring]], which is graded-commutative if $(E,\mu,1)$ is commutative.

1. For every pair $(X,A)$ the external multiplication $\mu$ gives $E^\bullet(X,A)$ the structure of a left and right [[module]] over the graded ring $E^\bullet(\ast)$.

1. All pullback morphisms respect the left and right action of $E^\bullet(\ast)$ and the connecting homomorphisms respect the right action and the left action up to multiplication by $(-1)^{n_1}$

=--

+-- {: .proof}
###### Proof

Regarding the third point:

For pullback maps this is the [[natural transformation|naturality]] of the external product: let $f \colon (X,A) \longrightarrow (Y,B)$ be a morphism in $Top_{CW}^{\hookrightarrow}$ then naturality says that the following square commutes:

$$
  \array{
    E^{n_1}(\ast) \otimes E^{n_2}(Y,B)
    &\overset{\mu_{n_1,n_2}}{\longrightarrow}&
    E^{n_1 + n_2}(Y, B)
    \\
    {}^{\mathllap{(id,f^\ast)}}\downarrow && \downarrow^{\mathrlap{f^\ast}}
    \\
    E^{n_1}(\ast) \otimes E^{n_2}(X,A)
    &\overset{\mu_{n_1,n_2}}{\longrightarrow}&
    E^{n_1 + n_2}(Y,B)
  }
  \,.
$$

For connecting homomorphisms this is the (graded) commutativity of the squares in def. \ref{MultiplicativeCohomologyTheory}:

$$
  \array{
    E^{n_1}(\ast)\otimes E^{n_2}(A)
      &\overset{(-1)^{n_1} (id, \delta)}{\longrightarrow}&
    E^{n_1}(\ast) \otimes E^{n_2 + 2}(X)
    \\
    {}^{\mathllap{\mu_{n_1,n_2}}}\downarrow && \downarrow^{\mathrlap{\mu_{n_1,n_2}}}
    \\
    E^{n_1 + n_2}(A)     
      &\overset{\delta}{\longrightarrow}&
     E_3^{n_1 + n_2+ 1}(X,B)
  }
  \,.
$$

=--

### Multiplicative Atiyah-Hirzebruch spectral sequences

+-- {: .num_prop #AHSSForMultiplicativeCohomologyTheoryIsMultiplicative}
###### Proposition

Given a multiplicative cohomology theory $(A,\mu,1)$ (def. \ref{MultiplicativeCohomologyTheory}), then for every [[Serre fibration]] $X \to B$ the corresponding [[Atiyah-Hirzebruch spectral sequence]] inherits the structure of a [[multiplicative spectral sequence]].

=--

A proof of prop. \ref{AHSSForMultiplicativeCohomologyTheoryIsMultiplicative} via [[Cartan-Eilenberg systems]] is given at _[[multiplicative spectral sequence]]_. A proof arguing via [[Brown representability theorem|representing]] [[ring spectra]] is in ([Kochman 96, prop. 4.2.9](#Kochman96)).



+-- {: .num_prop #LinearityOfDifferentialsInSerreAHSSForMultiplicativeCohomologyTheory}
###### Proposition

Given a multiplicative cohomology theory $(A,\mu,1)$ (def. \ref{MultiplicativeCohomologyTheory}), then for every [[Serre fibration]] $X \to B$ all the differentials in the corresponding [[Atiyah-Hirzebruch spectral sequence]]

$$
  H^\bullet(B,A^\bullet(F)) 
  \;\Rightarrow\;
  A^\bullet(X) 
$$

are linear over $A^\bullet(\ast)$.

=--

+-- {: .proof}
###### Proof

By construction ([here](Atiyah&#8211;Hirzebruch+spectral+sequence#ConstructionByFilteringTheBaseSpace)) the differentials are those induced by the [[exact couple]]

$$
  \array{
    \underset{s,t}{\prod} A^{s+t}(X_{s})
    &&
      \stackrel{}{\longrightarrow} 
    &&
    \underset{s,t}{\prod} A^{s+t}(X_{s})
    \\
    & \nwarrow && \swarrow
    \\
    && \underset{s,t}{\prod} A^{s+t}(X_{s}, X_{s-1})
  }
  \;\;\;\;\;\;\;
  \left(
      \array{
        A^{s+t}(X_s) & \longrightarrow & A^{s+t}(X_{s-1})
        \\
        \uparrow && \downarrow_{\mathrlap{\delta}}
        \\
        A^{s+t}(X_s, X_{s-1}) && A^{s+t+1}(X_{s}, X_{s-1})
      }
  \right)
  \,.
$$

consisting of the pullback homomorphisms and the connecting homomorphisms of $A$.

By the nature of spectral sequences induced from exact couples ([this prop.](exact+couple#CohomologicalSpectralSequenceOfAnExactCouple)) its differentials on page $r$ are the composites of one pullback homomorphism, the preimage of $(r-1)$ pullback homomorphisms, and one connecting homomorphism of $A$. Hence the statement follows with prop. \ref{RingAndModuleStructureOnCohomologyGroupsOfMultiplicativeCohomplogyTheory}.


=--



### Brown representability by ring spectra
 {#BrownRepresentabilityByRingSpectra}

A _multiplicative structure_ on a [[generalized (Eilenberg-Steenrod) cohomology]] theory is the structure of a [[ring spectrum]] on the [[spectrum]] that [[Brown representability theorem|represents]] it.

(e.g. [Tamaki-Kono 06, appendix C](#TamakiKono06), for more details see [here](suspension+spectrum#SmashMonoidalDiagonals)).

In particular every [[E-∞ ring]] is a [[ring spectrum]], hence represents a multiplicative cohomology theory, but the converse is in general false.

## Examples

* [[ordinary cohomology]] with [[coefficients]] in a [[ring]], in particular [[integral cohomology]]

* [[topological K-theory]], [[K-theory]]

* [[cobordism cohomology theory]]

* [[tmf]]

* etc....

## Related entries

* [[Kronecker pairing]]

* [[universal coefficient theorem]], [[module spectrum|module cohomology theories]], ...

See also

* [[complex oriented cohomology theory]], [[chromatic homotopy theory]]

* [[Thom isomorphism]]

* [[orientation in generalized cohomology]]

* [[fiber integration]]

* [[K-theory of a bipermutative category]]

* [[multiplicative spectral sequence]]

## References

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], p. 23 (30 of 120) in: _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))

* [[John Michael Boardman]], Section 3 (p. 10-11) of: _Stable Operations in Generalized Cohomology_ &lbrack;[pdf](https://math.jhu.edu/~wsw/papers2/math/28a-boardman-stable.pdf), [[Boardman-StableOperations.pdf:file]]&rbrack; in: [[Ioan Mackenzie James]] (ed.) _[[Handbook of Algebraic Topology]]_ Oxford 1995 ([doi:10.1016/B978-0-444-81779-2.X5000-7](https://doi.org/10.1016/B978-0-444-81779-2.X5000-7))

	
* {#TamakiKono06} [[Dai Tamaki]], [[Akira Kono]], chapter 2.6 of _Generalized Cohomology_, Translations of Mathematical Monographs, American Mathematical Society, 2006 ([[GeneralizedCohomology.pdf:file]], [ISBN: 978-0-8218-3514-2](https://bookstore.ams.org/mmono-230))

* [[Jacob Lurie]], _[[A Survey of Elliptic Cohomology - cohomology theories]]_


See also

* {#Kochman96} [[Stanley Kochman]], _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996


[[!redirects multiplicative cohomology theories]]

[[!redirects multiplicative cohomology]]



