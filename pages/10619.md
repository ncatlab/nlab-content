

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea


The _$e$-invariant_ ([Adams 66, section 7](#Adams66)) is the second in a sequence of homotopy invariants of "stable maps", i.e. of [[morphisms]] in the [[stable homotopy category]] (in particular: of [[stable homotopy groups of spheres]]), being elements of [[Ext-groups]] between the [[homology groups]]/[[cohomology groups]] of the [[domain]] and [[codomain]] of the map, with respect to some suitable choice of [[Whitehead-generalized cohomology theory]] $E$. 

The previous invariant in the sequence is the [[d-invariant]], the next is the [[f-invariant]]]. These are elements that appear on the second page of the $E$-[[Adams spectral sequence]].


## Definition

Let $X \overset{f}{\longrightarrow} Y$ be morphism in the [[stable homotopy category]] out of a [[finite spectrum]] $X$ (for instance the image under [[suspension]] $\Sigma^\infty$ of a morphism in the [[classical homotopy category]] of [[pointed homotopy types]] out of a [[finite CW-complex]]).

Let $E$ be a [[multiplicative cohomology theory]], such that the [[d-invariant]] of $f$ in $E$ vanishes, hence such that pullback $f^\ast \;\colon\; E^\bullet(Y) \to E^\bullet(X)$ in $E$-cohomology is the [[zero morphism]]].

The archetypical example is $f \;\colon\; S^{2n-1} \to S^{2n}$ a map out of an [[odd integer|odd]]-[[dimension|dimensional]] [[sphere]] and $E = KU$ [[complex topological K-theory]].

### As an extension of generalized Adams-operation modules
 {#AsAnExtensionOfAdamsOperationModules}

Writing $C_f$ for the [[homotopy cofiber]] of $f$

$$
  \cdots
  \to
  X
  \overset{f}{\longrightarrow}
  Y
  \overset{}{\longrightarrow}
  C_f
  \overset{}{\longrightarrow}
  \Sigma X
  \to
  \cdots
  \,,
$$

this implies that the [[long exact sequence in cohomology]] corresponding to the pair $(Y, C_f)$ truncates to a [[short exact sequence]] of the form

\[
  \label{TheShortExactSequenceInETheory}
  0 
  \to
  E^\bullet(\Sigma X)
  \overset{}{\longrightarrow}
  E^\bullet(C_f)
  \overset{}{\longrightarrow}
  E^\bullet(Y)
  \to 
  0
  \,.
\]

This is hence an [[algebra extension|extension]] of $E^\bullet(Y)$ by $E^\bullet(\Sigma X)$ in any [[category]] in which $f^\ast$ is a [[homomorphism]], for instance that of modules over the [[E-Steenrod algebra]].  For the case of $E = KU$ take the category of [[graded abelian groups]] equipped with [[Adams operations]]. 

Thus this short exact sequence defines an element in the [[Ext group]] formed in this category

$$
  e(f)
  \;\in\;
  Ext^1\big( 
   E^\bullet(Y),
   \,
   E^\bullet(\Sigma X)
  \big)
$$

and this is the e-invariant of $f$.

(Discussion in this generality includes [BL 09, Sec. 2](#BL09)).

### As an extension of complex topological K-cohomology groups

We discuss this in more detail for the case of [[complex topological K-theory]] $E = KU$, and for $f \;\colon\; S^{2(n + n')-1} \to S^{2n}$ a map between [[spheres]].

We follow [Hopkins-Mathew 12, Lecture 11](#HopkinsMathew12).


+-- {: .num_defn #AbelianGroupWithAdamsOperations} 
###### Definition
**(abelian group with Adams operations)**

We say that an _abelian group with Adams operation_ $\big(A,\{\psi_A^k\}_{k \in \mathbb{N}}\big)$ is an [[abelian group]] $A$ equipped with an [[action]] of the [[multiplicative group|multiplicative]] [[monoid]] $(\mathbb{N}, \cdot)$ of [[natural numbers]], hence equipped with [[group homomorphisms]]

$$
  \psi_A^k \;\colon\; A \to A
  \,,
  \;\;\;\;\;\;\;
  \text{for all}
  \;
  k \in \mathbb{N}
$$

such that 

$$
  \psi_A^{k_1}
  \circ
  \psi_A^{k_2}
  \;=\;
  \psi_A^{ k_1 \cdot k_2 }
  \,,
  \;\;\;\;\;\;\;\;\;
  \text{for all}
  \;
  k_1, k_2 \,\in\, \mathbb{N}
  \,.
$$

Moreover, for $\big(A,\{\psi_A^k\}_{k \in \mathbb{N}}\big), \, \big(A',\{\psi_{A'}^k\}_{k \in \mathbb{N}}\big)$ two abelian groups with Adams operations, a [[homomorphism]] between them is a [[group homomorphism]] (a [[linear map]]) $\phi \;\colon\; A \to A'$ which respect these operations, hence such that the following [[commuting square|squares commute]]:

$$
  \array{
    A &\overset{\;\;\;\phi\;\;\;}{\longrightarrow}& A'
    \\
    {}^{\mathllap{ \psi^k_A }}  
    \big\downarrow 
    && 
    \big\downarrow
    {}^{\mathrlap{\psi_{A'}^k}}
    \\
    A &\overset{\;\;\;\phi\;\;\;}{\longrightarrow}& A'
    \,,
  }
  \;\;\;\;\;\;\;\;
  \text{for all}
  \;
  k \in \mathbb{N}
  \,.
$$

This makes an [[abelian category]] which we denoted $Ab_{Adams}$.

=--

+-- {: .num_example #IntegersEquippedWithHomogeneousAdamsOperations} 
###### Example

For $n \in \mathbb{N}$, the additive abelian group of [[integers]] $\mathbb{Z}$ becomes an _abelian group with Adams operations_ 

$$
  \mathbb{Z}(n)
  \;\coloneqq\;
  \big(
    \mathbb{Z},\,
    \{\psi^k_{\mathbb{Z}}_k\}
  \big)
$$

in the sense of Def. \ref{AbelianGroupWithAdamsOperations} by setting

$$
  \array{
    \mathbb{Z}
    &
    \overset{\;\;\; \psi^k\;\;\;}{\longrightarrow}
    &
    \mathbb{Z}
    \\
    r &\mapsto& k^n \cdot r
    \,.
  }
$$

=--


+-- {: .num_example #AdamsOperationsOnComplexTopologicalKTheoryGroups} 
###### Example
**([[Adams operations]] on [[complex topological K-theory]] [[cohomology groups|groups]])**

For $X$ a [[compact topological space|compact]] [[pointed topological space]], the  [[complex topological K-theory]] [[cohomology group|group]] $K(X)$ becomes an abelian group with Adams operations in the sense of Def. \ref{AbelianGroupWithAdamsOperations}, 
via the actual [[Adams operations]], 

$$
  K(X),
  \widetilde K(X)
  \;\in\;
  Ab_{Adams}
$$

and hence so does the [[reduced K-theory]] $\widetilde K(X)$:

$$
  \array{
    \widetilde K(X)
    &\overset{\;\;ker(i^\ast)\;\;}{\longrightarrow}&
    K(X)
    &\overset{\;i^\ast\;}{\longrightarrow}&
    K(\ast)
    \\
    \big\downarrow
    {}^{\mathrlap{\psi^k_{\widetilde K(X)}}}
    &&
    \big\downarrow
    {}^{\mathrlap{\psi^k_{K(X)}}}
    &&
    \big\downarrow
    {}^{\mathrlap{\psi^k_{K(\ast)}}}
    \\
    \widetilde K(X)
    &\underset{\;\;ker(i^\ast)\;\;}{\longrightarrow}&
    K(X)
    &\underset{\;i^\ast\;}{\longrightarrow}&
    K(\ast)
    \,,
  }
$$

Moreover, for each (pointed) [[continuous function]] $X \overset{f}{\longrightarrow} Y$ the corresponding [[pullback in cohomology]] respects the Adams operations and hence yields a morphism

$$
  \widetilde K(X)
  \overset{\;\;f^\ast\;\;}{\longrightarrow}
  \widetilde K(Y)
  \,,
  \;\;\;\;
  \in 
  \;
  Ab_{Adams}
  \,.
$$

=--

+-- {: .num_prop #AdamsOperationOnComplexTopologicalKtheoryOfnSpheres} 
###### Proposition
**([[Adams operations]] on [[complex topological K-theory]] of [[n-spheres]])**

For $n \in \mathbb{N}$, the [[Adams operations]] on the [[reduced K-theory]] (Example \ref{AdamsOperationsOnComplexTopologicalKTheoryGroups}) of the [[n-sphere|2n-sphere]] are given by:

$$
  \array{
    \widetilde K
    \big( 
      S^{2n}
    \big)
    &
    \overset{ \;\;\; \psi^k\;\;\; }{\longrightarrow}
    &
    \widetilde K
    \big( 
      S^{2n}
    \big)
    \\
    V &\mapsto& k^n \cdot V
  }
$$

and hence are [[isomorphism|isomorphic]] to the objects from Example \ref{IntegersEquippedWithHomogeneousAdamsOperations}:

$$
  \widetilde K
  \big( 
    S^n
  \big)
  \;\simeq\;
  \mathbb{Z}
  \;\;\;\;
  \in
  \;
  Ab_{Adams}
  \,.
$$

=--



Hence the [[short exact sequence]] (eq:TheShortExactSequenceInETheory) becomes short exact sequence in the [[abelian category]] of abelian groups with Adams operations (Def. \ref{AbelianGroupWithAdamsOperations}):

\[
  \label{ShortExactSequenceForComplexTopologicalKTheory}
  0 
  \to
  \widetilde K\big( S^{2(n + n')} \big)
  \overset{\;\;\;\;\;\;}{\longrightarrow}
  \widetilde K\big( C_f \big)
  \overset{\;\;\;\;\;\;}{\longrightarrow}
  \widetilde K\big( S^{2n} \big)
  \to
  0
  \,,
  \;\;\;\;\;\;\;\;
  \in
  \;
  Ab_{Adams}
  \,.
\]


### As a cobordism invariant of manifolds with boundary
 {#AsACobordismInvariantOfManifoldsWithBoundary}

(...) [Conner-Floyd 66](#ConnerFloyd66) (...)


## Related concepts

* [[eta-invariant]]

* [[d-invariant]], [[f-invariant]]

* [[Hopf invariant]], [[Hopf invariant one problem]]

* [[J-homomorphism]]

* [[stable homotopy groups of spheres]]


## References

The definition is due to:

* {#Adams66} [[John Adams]], Section 7 of: _On the groups $J(X)$ IV_, Topology 5: 21,(1966)   ([pdf](http://math.unice.fr/~cazanave/Gdt/ImJ/J-IV.pdf), <a href="https://doi.org/10.1016/0040-9383(66)90004-8">doi:10.1016/0040-9383(66)90004-8</a>)

  _Correction_, Topology 7 (3): 331 (1968)

Discussion in more general [[Whitehead generalized cohomology theories]]:

* {#Krueger73} Warren M. Krueger, _Generalized Steenrod-Hopf Invariants for Stable Homotopy Theory_, Proceedings of the American Mathematical Society, Vol. 39, No. 3 (Aug., 1973), pp. 609-615 ([jstor:2039603](https://www.jstor.org/stable/2039603))

* Warren M. Krueger, _Relation with the Hopf invariant revisited_, Illinois J. Math.
Volume 24, Issue 2 (1980), 188-191 ([euclid:ijm/1256047713](https://projecteuclid.org/euclid.ijm/1256047713))



and in relation to the [[Adams spectral sequence]]

* {#Switzer75} [[Robert Switzer]], Section 19.19 in: _Algebraic Topology - Homotopy and Homology_, Grundlehren der Mathematischen Wissenschaften, Vol. 212, Springer, 1975 ([doi:10.1007/978-3-642-61923-6](https://link.springer.com/book/10.1007/978-3-642-61923-6))

and to the [[f-invariant]]:

* {#BL09} Mark Behrens, Gerd Laures, _$\beta$-Family congruences and the $f$-invariant_, Geometry & Topology Monographs 16 (2009) 9–29 ([arXiv:0809.1125](https://arxiv.org/abs/0809.1125), [doi: 10.2140/gtm.2009.16.9](https://msp.org/gtm/2009/16/p002.xhtml))


Interpretation in [[bordism theory]]:

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], Section 16 of: _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))

Interpretation via [[index theory]]:

* [[Michael Atiyah]], [[Vijay Patodi]], [[Isadore Singer]], 
p. 18 onwards in: _Spectral asymmetry and Riemannian geometry. II_, Volume 78, Issue 3 November 1975 , pp. 405-432 ([doi:10.1017/S0305004100051872](https://doi.org/10.1017/S0305004100051872))





Review:

* {#Weibel} [[Charles Weibel]], chapter VI, section 2 of _[The K-book](http://www.math.rutgers.edu/~weibel/Kbook.html)_ ([pdf](http://www.math.rutgers.edu/~weibel/Kbook/Kbook.VI.pdf))

* [[Ulrich Bunke]], Section 2 of: _Differential cohomology in geometry and analysis_, talk 2008 ([pdf](https://www.uni-regensburg.de/Fakultaeten/nat_Fak_I/Bunke/Vortrag-Erlangen.pdf), [[BunkeEInvariantErlangen2008.pdf:file]])

* {#HopkinsMathew12} [[Michael Hopkins]] (notes by [[Akhil Mathew]]), Lecture 11 in: _Spectra and stable homotopy theory_, 2012 ([pdf](http://math.uchicago.edu/~amathew/256y.pdf), [[HopkinsMathewStableHomotopyTheory.pdf:file]])

* {#Quick14EInvariant} [[Gereon Quick]], _The $e$-invariant_, lecture notes in: _[Advanced algebraic topology](https://folk.ntnu.no/gereonq/Math231br.html)_, 2014 ([[QuickEInvariant.pdf:file]])

* {#Quick14JHomomorphism} [[Gereon Quick]], _The $e$-invariant and the $J$-homomorphism_, lecture notes in: _[Advanced algebraic topology](https://folk.ntnu.no/gereonq/Math231br.html)_, 2014 ([[QuickEInvariantAndJHomomorphism.pdf:file]])



Discussion via [[Toda brackets]]:

* Hiroaki Hamanaka, _Adams $e$-invariant, Toda bracket and $[X, U(n)]$_,  J. Math. Kyoto Univ. Volume 43, Number 4 (2003), 815-827. ([euclid:kjm/1250281737]( http://projecteuclid.org/euclid.kjm/1250281737))

Discussion in [[MU-theory]]:

* N. V. Panov, _Characteristic numbers in $U$-theory_, Akad. Nauk SSSR Ser. Mat., 1971 Volume 35, Issue 6 ([mathnet:2174](http://m.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=im&paperid=2174&option_lang=eng))



Discussion in [[BP-theory]]:

* Yasumasa Hirashima, _On the $BP_\ast$-Hopf invariant_, Osaka J. Math., Volume 12, Number 1 (1975), 187-196 ([euclid:ojm/1200757733](https://projecteuclid.org/euclid.ojm/1200757733))

* [[Martin Bendersky]], _The BP Hopf Invariant_, American Journal of Mathematics, Vol. 108, No. 5 (Oct., 1986) ([jstor:2374595](https://www.jstor.org/stable/2374595))




[[!redirects Adams e-invariants]]

[[!redirects e-invariant]]
[[!redirects e-invariants]]

[[!redirects Adams E-invariant]]
[[!redirects E-invariant]]

[[!redirects Adams E-invariants]]
[[!redirects E-invariants]]


