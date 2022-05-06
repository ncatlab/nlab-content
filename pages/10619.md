

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

The previous invariant in the sequence is the [[d-invariant]], the next is the [[f-invariant]]. These are elements that appear on the second page of the $E$-[[Adams spectral sequence]].


## Definition

Let $X \overset{f}{\longrightarrow} Y$ be morphism in the [[stable homotopy category]] out of a [[finite spectrum]] $X$ (for instance the image under [[suspension]] $\Sigma^\infty$ of a morphism in the [[classical homotopy category]] of [[pointed homotopy types]] out of a [[finite CW-complex]]).

Let $E$ be a [[multiplicative cohomology theory]], such that the [[d-invariant]] of $f$ in $E$ vanishes, hence such that pullback $f^\ast \;\colon\; E^\bullet(Y) \to E^\bullet(X)$ in $E$-cohomology is the [[zero morphism]].

The archetypical example is $f \;\colon\; S^{2n-1} \to S^{2n}$ a map out of an [[odd integer|odd]]-[[dimension|dimensional]] [[sphere]] and $E = KU$ [[complex topological K-theory]].

\linebreak

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

\[
  \label{GeneraleInvariantAsElementOfExtGroup}
  e(f)
  \;\in\;
  Ext^1\big( 
   E^\bullet(Y),
   \,
   E^\bullet(\Sigma X)
  \big)
\]

and this is the e-invariant of $f$.

(Discussion in this generality includes [BL 09, Sec. 2](#BL09)).

\linebreak

### As an extension of K-groups with Adams operations
 {#AsAnExtensionOfComplexTopologicalKTheoryWithAdamsOperations}

We discuss this in more detail for the case of [[complex topological K-theory]] $E = KU$, and for $f \;\colon\; S^{2(n + \bullet)-1} \to S^{2n}$ a map between [[spheres]]; and we show how the resulting extension is characterized by a single [[rational number]] [[modulo]] the [[integers]], this being the e-invariant in the form of a [[Q/Z]]-valued character 

$$
  e_{\mathbb{C}}
  \;\colon\;
  \pi^s_{\bullet}
  \overset{\;\;\;\;\;}{\longrightarrow}
  \mathbb{Q}/\mathbb{Z}
$$

on [[stable homotopy groups of spheres]] (Def. \ref{eInvariantInComplexTopologicalKtheoryAsRationalNumberModuloIntegers} below).

We follow [Hopkins-Mathew 12, Lecture 11](#HopkinsMathew12).

\linebreak

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

\[
  \label{ActionPropertyOfAbstractAdamsOperations}
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
\]

Moreover, for $\big(A,\{\psi_A^k\}_{k \in \mathbb{N}}\big), \, \big(A',\{\psi_{A'}^k\}_{k \in \mathbb{N}}\big)$ two abelian groups with Adams operations, a [[homomorphism]] between them is a [[group homomorphism]] (a [[linear map]]) $\phi \;\colon\; A \to A'$ that respects these operations, hence such that the following [[commuting square|squares commute]]:

\[
  \label{HomomorphismOfAbelianGroupsWithAdamsOperations}
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
\]

This makes an [[abelian category]] which we denoted $Ab_{Adams}$, canonically equipped with a [[forgetful functor]] to [[Ab]]:

\[
  \label{ForgetfulFunctorFromAbelianGroupsWithAdamsOperations}
  \array{
    Ab_{Adams}
    &\overset{\;\;\;\;\;\;}{\longrightarrow}&
    Ab
    \\
    \big(
      A, 
      \,
      \{\psi^k_A\}_{k \in \mathbb{N}}
    \big)
    &\mapsto&
    A
    \,.
  }
\]

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
  \,,
$$

in the sense of Def. \ref{AbelianGroupWithAdamsOperations}, by setting

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

Moreover, for each (pointed) [[continuous function]] $X \overset{f}{\longrightarrow} Y$ the corresponding [[pullback in cohomology]] respects the Adams operations and hence yields a [[homomorphism]] (eq:HomomorphismOfAbelianGroupsWithAdamsOperations):

\[
  \label{PullbackInKCohomologyRespectsAdamsOperation}
  \widetilde K(X)
  \overset{\;\;f^\ast\;\;}{\longrightarrow}
  \widetilde K(Y)
  \,,
  \;\;\;\;
  \in 
  \;
  Ab_{Adams}
  \,.
\]

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

and hence are [[isomorphism|isomorphic]] in $Ab_{Adams}$ (Def. \ref{AbelianGroupWithAdamsOperations}) to the [[objects]] from Example \ref{IntegersEquippedWithHomogeneousAdamsOperations}:

$$
  \widetilde K
  \big( 
    S^{2n}
  \big)
  \;\simeq\;
  \mathbb{Z}(n)
  \;\;\;\;
  \in
  \;
  Ab_{Adams}
  \,.
$$

=--

+-- {: .num_example #TheDefinignSESInComplexTopologicalKTheory} 
###### Example
**(defining short exact sequence in complex topological K-theory)**

For $n, n' \,\in\, \mathbb{N}$ let 

$$
  f \;\colon\; S^{2(n + n') - 1} \longrightarrow S^{2n}
$$ 

be a [[continuous function]] between [[spheres]] (representing its image in the [[classical homotopy category]] and in fact in the [[stable homotopy category]], which is all that its image in a [[Whitehead-generalized cohomology theory]] such as [[complex topological K-theory]] depends on), such that the [[d-invariant]] of $f$ vanishes under [[complex topological K-theory]] $E = KU$, hence such that the [[pullback in cohomology|pullback]] $f^\ast$ is the [[zero map]] in K-theory:

$$
  d(f) \;\coloneqq\; f^\ast \;=\; 0 \;\;\;\colon\;
  \widetilde K\big(S^{2n}\big)
  \longrightarrow
  \widetilde K\big( S^{2(n + n') - 1} \big)
  \,.
$$

Writing $C_f$ for the [[homotopy type]] of the [[homotopy cofiber]]/[[attaching space]] of $f$:

\[
  \label{ThePushoutDiagramsForTheCofiberSpaceAndSuspension}
  \array{
    S^{2(n + n') - 1}
    &\longrightarrow&
    \ast
    \\
    {}^{\mathllap{f}}
    \big\downarrow
    &
    {}^{_{(hpo)}}
    &
    \big\downarrow
    \\
    S^{2n}
    &\underset{i_{2n}}{\longrightarrow}&
    C_f
    \\
    {}^{}
    \big\downarrow
    &
    {}^{_{(hpo)}}
    &
    \big\downarrow
    {}^{\mathrlap{ p_{2(n+n')} }}
    \\
    \ast
    &\longrightarrow&
    S^{2(n + n')}
  }
  \;\;\;\;\;\;\;\;
  \simeq
  \;\;\;\;\;\;\;\;
  \array{
    S^{2(n + n') - 1}
    &\longrightarrow&
    D^{2(n + n')}
    \\
    {}^{\mathllap{f}}
    \big\downarrow
    &
    {}^{_{(po)}}
    &
    \big\downarrow
    \\
    S^{2n}
    &\underset{i_{2n}}{\longrightarrow}&
    C_f
    \\
    {}^{}
    \big\downarrow
    &
    {}^{_{(po)}}
    &
    \big\downarrow
    {}^{\mathrlap{ p_{2(n+n')} }}
    \\
    \ast
    &\longrightarrow&
    S^{2(n + n')}
  }
\]

this implies that the [[long exact sequence in cohomology]] induced by the [[CW-pair]] $S^{2n} \hookrightarrow C_f$ truncates to the [[short exact sequence]] (eq:TheShortExactSequenceInETheory), here regarded, by Example \ref{AdamsOperationsOnComplexTopologicalKTheoryGroups}, in the [[abelian category]] $Ab_{Adams}$ of abelian groups with Adams operations (Def. \ref{AbelianGroupWithAdamsOperations}):

\[
  \label{ShortExactSequenceForComplexTopologicalKTheory}
  \array{
    0 
    &\to&
    \widetilde K\big( S^{2(n + n')} \big)
    &\overset{\;\;\; p_{2(n+n')}^\ast \;\;\;}{\longrightarrow}&
    \widetilde K\big( C_f \big)
    &\overset{\;\;\; i_{2n}^\ast \;\;\;}{\longrightarrow}&
    \widetilde K\big( S^{2n} \big)
    &\to&
    0
    \\
    &&
    \big\downarrow
    {}^{\mathrlap{\simeq}}
    &&
    \big\downarrow
    {}^{\mathrlap{=}}
    &&
    \big\downarrow
    {}^{\mathrlap{\simeq}}
    \\
    0 
    &\to&
    \mathbb{Z}(n + n')
    &\underset{\;\;\; \;\;\;\; \;\;\;}{\longrightarrow}&
    \widetilde K\big( C_f \big)
    &\underset{\;\;\; \;\;\;\; \;\;\;}{\longrightarrow}&
    \mathbb{Z}(n)
    &\to&
    0
  }
  \;\;\;\;\;\;\;\;
  \in
  \;
  Ab_{Adams}
  \,,
\]

where in the second line we have identified the outer groups via Prop. \ref{AdamsOperationOnComplexTopologicalKtheoryOfnSpheres}.

By definition of [[Ext-groups]], the [[isomorphism class]] of this short exact sequence with the outer groups fixed is an element

\[
  \label{AdamsInvariantInComplexKTheoryAsElementOfExt1}
  e_{\mathbb{C}}(f) 
  \;\;\in\;\;
  Ext^1_{Ab_{Adams}}
  \big(
    \mathbb{Z}(n),
    \,
    \mathbb{Z}(n + n')
  \big)
  \,.
\]

This is the [[Adams e-invariant]] of $f$ as seen in [[complex topological K-theory]]; in specialization of (eq:GeneraleInvariantAsElementOfExtGroup).

=--

More concretely, it turns out that the extension (eq:AdamsInvariantInComplexKTheoryAsElementOfExt1) is completely characterized by a single [[rational number]] modulo this [[integers]]. This we discuss next (Def. \ref{eInvariantInComplexTopologicalKtheoryAsRationalNumberModuloIntegers} below).


+-- {: .num_remark #ExtensionAfterForgettingAdamsModuleStructureIsTrivial} 
###### Remark
**(extension after forgetting the Adams module structure is trivial)**

After forgetting the action of the Adams operations via (eq:ForgetfulFunctorFromAbelianGroupsWithAdamsOperations), the sequence (eq:ShortExactSequenceForComplexTopologicalKTheory) is still a [[short exact sequence]], now of plain [[abelian groups]]. However, since $Ext^1_{Ab}(\mathbb{Z},-) = 0$ ([this Prop.](Ext#ExtensionsOfTheIntegersAreTrivial)), it is necessarily trivial as an extension, showing that the underlying abelian cohomlogy group of the cofiber space is just

\[
  \label{UnderlyingAbelianGroupOfKTheoryOfCofiberSpace}
  \array{
  \mathbb{Z} \oplus \mathbb{Z}
  &
    \simeq
  &
  \widetilde K \big( S^{2n} \big)
  \,\oplus\,
  \widetilde K \big( S^{2(n + n')} \big)
  &
  \simeq
  &
  \widetilde K
  \big(
    C_f 
  \big)  
  \\
  \big( 
     1, 
     \, 
     1  
  \big)
  &\mapsto&
  \big(
    \Sigma^{2n} 1, 
    \,
    \Sigma^{2(n + n')} 1
  \big)
  &\mapsto&
  \big(
    V_{2n},
    \,
    V_{2(n+n')}
  \big)  
  }
  \;\;
  \;\in\;
  Ab
  \,.
\]

=--

Conversely, this means that all the information in the extension (eq:ShortExactSequenceForComplexTopologicalKTheory) is in how the Adams operations act on the K-theory of the cofiber space:

+-- {: .num_defn #eInvariantInComplexTopologicalKtheoryAsRationalNumberModuloIntegers} 
###### Definition
**([[e-invariant]] in [[complex topological K-theory]] as [[rational number]] [[modulo]] [[integers]])**

Given a map $f \;\colon\; S^{2(n + n') - 1} \longrightarrow S^{2n}$
with vanishing $KU$-[[d-invariant]],
as in Example \ref{TheDefinignSESInComplexTopologicalKTheory}, we have by 
Remark \ref{ExtensionAfterForgettingAdamsModuleStructureIsTrivial}  that the [[Adams operations]] (Example \ref{AdamsOperationsOnComplexTopologicalKTheoryGroups}) on the cofiber space $C_f$ (eq:ThePushoutDiagramsForTheCofiberSpaceAndSuspension) must be of the form

\[
  \label{ActionOfAdamsOperationsOnCofiberSpace}
  \array{
    \widetilde K\big( C_f\big)
    &\overset{ \;\;\; \psi^k\;\;\; }{\longrightarrow}&
    \widetilde K\big( C_f\big)
    \\
    V_{2n}
    &\mapsto&
    k^n \cdot V_{2n}
    \;+\;
    {\color{blue}
      \mu_k(f) 
    }
    \cdot V_{2(n+ n')}
    \\
    V_{2(n + n')}
    &\mapsto&
    k^{n + n'} \cdot V_{2(n + n')}
    \;\;\;\;\;\;\;\;
    \,.
  }
\]

Namely, the first summands on the right are constrained to be as shown, by Example \ref{AdamsOperationOnComplexTopologicalKtheoryOfnSpheres} and using 
that [[pullback in cohomology]] $i^\ast_{2n}$, $p^\ast_{2(n + n')}$(eq:PullbackInKCohomologyRespectsAdamsOperation) respects the [[Adams operations]] (Example \ref{AdamsOperationsOnComplexTopologicalKTheoryGroups}); while the second summand, which vanishes under $i^\ast_{2n}$, must be some multiple  

$$
  \mu_k(f) \;\in\; \mathbb{Z}
$$

of the only other generator $V_{2(n + n')}$ (eq:UnderlyingAbelianGroupOfKTheoryOfCofiberSpace). This $\mu$ is the only part of the data that is not completely fixed by the Adams module structure, and which may depend on the map $f$.

We say that the _[[Adams e-invariant]] of $f$_ as an element in [[Q/Z]] is this multiple $\mu$, normalized as follows:

\[
  \label{eInvariantAsRationalNumberModuloIntegers}
  e_{\mathbb{C}}(f)
  \;\coloneqq\;
  \frac{
    \mu_k(f)
  }{
    k^{n}
    \big(
      k^{n'} - 1
    \big)
  }
  \;\;
  \in
  \;\;
  \mathbb{Q}/\mathbb{Z}
  \,.
\]

=--

+-- {: .num_prop #eInvariantInKTheoryAsRationalNumberModuloIntegersIsWellDefined} 
###### Proposition
**(e-invariant as rational number modulo integers is well defined)**

The e-invariant $e_{\mathbb{C}}(f)$ (eq:eInvariantAsRationalNumberModuloIntegers) from Def. \ref{eInvariantInComplexTopologicalKtheoryAsRationalNumberModuloIntegers}
is well-defined, in that it is independent of the choice of $k$ on the right of (eq:eInvariantAsRationalNumberModuloIntegers).


=--

+-- {: .proof}
###### Proof

Use the commutativity 
(eq:ActionPropertyOfAbstractAdamsOperations) of the Adams operation 
together with the formula (eq:ActionOfAdamsOperationsOnCofiberSpace)  to find for any $k_1, k_2 \,\in\, \mathbb{N}$:

$$
  \begin{aligned}
    & 
    \phantom{\;=\;\;}
    \psi^{k_1} \circ \psi^{k_2}
    \big(
      V_{2n} 
    \big)
    \\
    & 
    \;=\;
    \psi^{k_2} \circ \psi^{k_1}
    \big(
      V_{2n} 
    \big)
    \\
    \\
    \Leftrightarrow
    \;\;\;
    & 
    \phantom{\;=\;\;}
    \psi^{k_1}
    \big(
      k_2^n \cdot V_{2n}
      +
      \mu_{k_2}(f) \cdot V_{2(n + n')}
    \big)
    \\
    & 
    \;=\;
    \psi^{k_2}
    \big(
      k_1^n \cdot V_{2n}
      +
      \mu_{k_1}(f) \cdot V_{2(n + n')}
    \big)
    \\
    \\
    \Leftrightarrow
    \;\;\;
    & 
    \phantom{\;=\;\;}
    (k_1 k_2)^n \cdot V_{2n}
    +
    \Big(
      k_2^n \mu_{k_1}(f)
      +
      k_1^{n + n'} \mu_{k_2}(f) 
    \Big)
    \cdot
    V_{2(n + n')}
    \\
    & 
    \;=\;
    (k_1 k_2)^n \cdot V_{2n}
    +
    \Big(
      k_1^n \mu_{k_2}(f)
      +
      k_2^{n + n'} \mu_{k_1}(f) 
    \Big)
    \cdot
    V_{2(n + n')}
    \\
    \\
    \Leftrightarrow
    \;\;\;
    & 
    \phantom{\;=\;\;}
    k_1^n
    \big(
      k_1^{n'}
      -
      1
    \big)
    \mu_{k_2}(f)
    \\
    & 
    \;=\;
    k_2^n
    \big(
      k_2^{n'}
      -
      1
    \big)
    \mu_{k_1}(f)
    \\
    \\
    \Leftrightarrow
    \;\;\;
    & 
    \phantom{\;=\;\;}
    \frac{
      \mu_{k_1}(f)
    }{
      k_1^n
      \big(
        k_1^{n'}
        -
        1
      \big)
    }
    \\
    & 
    \;=\;
    \frac{
      \mu_{k_2}(f)
    }{
      k_2^n
      \big(
        k_2^{n'}
        -
        1
      \big)
    }
  \end{aligned}
$$

=--


\linebreak


### As a cobordism invariant of U-manifolds with framed boundary
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


