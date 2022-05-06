

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


The _$e$-invariant_ ([Adams 66, Sections 3,7](#Adams66), short for "extension invariant", see Def. \ref{EInvariantAsExtensionClassInECohomology} below) is the second in a sequence of homotopy invariants of "stable maps", i.e. of [[morphisms]] in the [[stable homotopy category]] (in particular: of [[stable homotopy groups of spheres]]), being elements of [[Ext-groups]] between the [[homology groups]]/[[cohomology groups]] of the [[domain]] and [[codomain]] of the map, with respect to some suitable choice of [[Whitehead-generalized cohomology theory]] $E$. 

The previous invariant in the sequence is the _[[d-invariant]]_, the next is the _[[f-invariant]]_. These are the elements that appear in the first lines on the second page of the $E$-[[Adams spectral sequence]] for $[X,Y]_\bullet$.


## Definition

Let $X \overset{f}{\longrightarrow} Y$ be morphism in the [[stable homotopy category]] out of a [[finite spectrum]] $X$ (for instance the image under [[suspension]] $\Sigma^\infty$ of a morphism in the [[classical homotopy category]] of [[pointed homotopy types]] out of a [[finite CW-complex]]).

Let $E$ be a [[multiplicative cohomology theory]], such that the [[d-invariant]] of $f$ in $E$ vanishes, hence such that pullback $f^\ast \;\colon\; E^\bullet(Y) \to E^\bullet(X)$ in $E$-cohomology is the [[zero morphism]].

The archetypical example is $f \;\colon\; S^{2n-1} \to S^{2n}$ a map out of an [[odd integer|odd]]-[[dimension|dimensional]] [[sphere]] and $E = KU$ [[complex topological K-theory]].

\linebreak

### As an extension of generalized Adams-operation modules
 {#AsAnExtensionOfAdamsOperationModules}

+-- {: .num_defn #EInvariantAsExtensionClassInECohomology} 
###### Definition
**(e-invariant as extension class in E-cohomology)**

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

and this is the _e-invariant_ of $f$ seen in $E$-theory.

=--

([Adams 66, Section 3, p. 27](#Adams66), review includes [BL 09, Sec. 2](#BL09)).

\linebreak

## For $E = KU$

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

#### Abelian groups with Adams operations

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

#### The Adams $e_{\mathbb{C}}$-invariant in $\mathbb{Q}/\mathbb{Z}$
 {#TheEInvariantAsAnElementOfQModZ}

+-- {: .num_example #TheDefinignSESInComplexTopologicalKTheory} 
###### Example
**(the defining short exact sequence in complex topological K-theory)**

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
  \,,
\]

where $V_{2(n + n')} \;\coloneqq\; p_{2(n+n')}^\ast \Sigma^{2(n+n')} 1$ and where $V_{2n}$ is a choice of lift of $\Sigma^{2n} 1$ through $i_{2n}^\ast$ in the short exact sequence (eq:ShortExactSequenceForComplexTopologicalKTheory):

\[
  \label{TheSplittingOfExactSequenceOfAbelianGroups}
  \array{
    0 
    \to
    & 
    \widetilde K\big( S^{2(n+n')} \big)
    &
    \overset{p^\ast_{2(n+n')}}{\longrightarrow}
    &
    \widetilde K\big( C_f \big)
    &
    \overset{i^\ast_{2n}}{\longrightarrow}
    &
    \widetilde K\big( S^{2n} \big)
    &
    \to 
    0
    \\
    & 
    \Sigma^{2(n+n')} 1
    &\mapsto&
    V_{2(n+n')}
    \\
    & &&
    V_{2n}
    &\mapsto&
    \Sigma^{2n} 1
    \,.
  }
\]

Notice that the [[isomorphism]] (eq:UnderlyingAbelianGroupOfKTheoryOfCofiberSpace) depends on a choice of [[splitting]] (eq:TheSplittingOfExactSequenceOfAbelianGroups) of the short exact sequence (eq:ShortExactSequenceForComplexTopologicalKTheory) in [[Ab]]: any two choices $V_{2n}$, $V'_{2n}$ differ by a multiple $s \in \mathbb{Z}$ of the generator $V_{2(n + n')}$:

\[
  \label{DependenceOfDegree2nGeneratorOnChoiceOfSplitting}
  V'_{2n}
  \;=\;
  V_{2n} + s \cdot V_{2(n + n')}
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
Remark \ref{ExtensionAfterForgettingAdamsModuleStructureIsTrivial}  
that the [[Adams operations]] (Example \ref{AdamsOperationsOnComplexTopologicalKTheoryGroups}) on the cofiber space $C_f$ (eq:ThePushoutDiagramsForTheCofiberSpaceAndSuspension) must be of the form

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

Namely, the first summands on the right are constrained to be as shown, by Prop. \ref{AdamsOperationOnComplexTopologicalKtheoryOfnSpheres} and using 
that [[pullback in cohomology]] $i^\ast_{2n}$, $p^\ast_{2(n + n')}$(eq:PullbackInKCohomologyRespectsAdamsOperation) respects the [[Adams operations]] (Example \ref{AdamsOperationsOnComplexTopologicalKTheoryGroups}); while the second summand, which vanishes under $i^\ast_{2n}$, must be some multiple  

$$
  \mu_k(f) \;\in\; \mathbb{Z}
$$

of the only other generator $V_{2(n + n')}$ (eq:UnderlyingAbelianGroupOfKTheoryOfCofiberSpace). This $\mu$ is the only part of the data that is not completely fixed by the Adams module structure, and which may depend on the map $f$.

We say that the _[[Adams e-invariant]] of $f$_ is this multiple $\mu$, normalized as a [[rational number]] as follows, and then regarded modulo addition of [[integers]] as an element in [[Q/Z]]:

\[
  \label{eInvariantAsRationalNumberModuloIntegers}
  e_{\mathbb{C}}(f)
  \;\coloneqq\;
  \left[
  \frac{
    \mu_k(f)
  }{
    k^{n}
    \big(
      k^{n'} - 1
    \big)
  }
  \right]
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
is well-defined, in that it is 

1. independent of the choice of splitting $\Sigma^{2n} 1 \,\mapsto\, V_{2n}$ in (eq:UnderlyingAbelianGroupOfKTheoryOfCofiberSpace);

1. independent of the choice of $k$ on the right of (eq:eInvariantAsRationalNumberModuloIntegers).



=--

+-- {: .proof}
###### Proof

**On 1.**  Under a different choice of splitting, $V_{2n}$ changes to (eq:DependenceOfDegree2nGeneratorOnChoiceOfSplitting)

$$
  V'_{2n} \;=\; V_{2n} + s \cdot V_{2(n + n')}
$$

for some $s \in \mathbb{Z}$. By inspection of (eq:ActionOfAdamsOperationsOnCofiberSpace) this implies that $\mu_k(f)$ changes to

$$
  \mu'_k(f)
  \;=\;
  \mu_k(f) + s \cdot \big( k^{n + n'} - k^n \big) 
  \,;
$$

and so in (eq:eInvariantAsRationalNumberModuloIntegers) we have

$$
  e'_{\mathbb{C}}(f)
  \;=\;
  \left[
  \frac{
    \mu'_k(f)
  }{
    k^n(k^{n'} -1 )
  }
  \right]
  \;=\;
  \left[
  \frac{
    \mu_k(f)
  }{
    k^n(k^{n'} -1 )
  }  
  + s
  \right]
  \;=\;
  \left[
  \frac{
    \mu_k(f)
  }{
    k^n(k^{n'} -1 )
  }  
  \right]
  \;=\;
  e_{\mathbb{C}}(f)
  \,.
$$

**On 2.** Use the commutativity 
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


### As the top degree Chern character on cofiber space
  {#AsThe2nFormComponentOfTheChernCharacterOnCofiberSpaces}


+-- {: .num_prop #QModZValuedEInvariantIsTopDegreeCoefficientOfChernCharacterOnCofiberSpace} 
###### Proposition
**([[Q/Z]]-valued [[e-invariant]] is top-degree coefficient of [[Chern character]] on cofiber space)**

In the situation of Example \ref{TheDefinignSESInComplexTopologicalKTheory}, with 

$$
  f \;\colon\; S^{2(n+n')-1 } \longrightarrow S^{2n}
$$

a map between spheres, and with $V_{2n} \,\in\, \widetilde K\big( C_f \big)$ any lift (eq:TheSplittingOfExactSequenceOfAbelianGroups)
of $\Sigma^{2 n} 1 \,\in\, \widetilde K \big( S^{2n} \big) $ to its  homotopy cofiber space, we have that the [[e-invariant]] $e(f)$ (Def. \ref{eInvariantInComplexTopologicalKtheoryAsRationalNumberModuloIntegers}) is equivalently the [[Kronecker pairing|evaluation]] [[modulo]] [[integers]] of the [[Chern character]] $ch(V_{2n}) \,\in\,  H^{ev}\big( C_f;\, \mathbb{Q}  \big)$ on the [[fundamental class]] of the cofiber space:

$$
  \exp
  \left(
    2 \pi \mathrm{i}
    \int_{C_f}
      ch\big( V_{2n} \big)
  \right)
  \;=\;
  \exp
  \left(
    2 \pi \mathrm{i}
    \,
    {
      \color{blue}
      e(f)
    }
  \right)
  \;\;\;
  \in 
  \mathrm{U}(1)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By (eq:ActionOfAdamsOperationsOnCofiberSpace) we have,
now in [[matrix calculus]]-notation:

$$
  \psi^k
  \;\colon\;
  \left[
  \array{
    V_{2 n }
    \\
    V_{2(n + n')}
  }
  \right]
  \;\;\;
  \mapsto
  \;\;\;
  \left[
  \array{
    k^n
    & 
    0
    \\
    e(f) \, k^n (k^{n'} - 1)
    & 
    k^{n + n'}
  }
  \right]
  \cdot
  \left[
  \array{
    V_{2 n }
    \\
    V_{2(n + n')}
  }
  \right]
  \;\;\;\;\;
  \in
  \;
  \widetilde K\big( C_f \big)
  \,.
$$

This [[matrix]] has two [[eigenvectors]] over the [[rational numbers]] (in general). Therefore we now consider the image of these K-theory classes under the [[Chern character]] map

$$
  ch 
    \;\colon\; 
  \widetilde K\big( C_f \big) 
    \longrightarrow 
  H^{ev}\big( C_f;\, \mathbb{Q}\big)
  \,.
$$

Since the [[Adams operations are compatible with the Chern character]], we then have the following [[eigenvectors]] of the [[Adams operations]] under $ch$:

\[
  \label{EigenvectorsOfAdamsOperationsAfterPassageThroughChernCharacter}
  \psi^k_H 
    \;\;\colon\;\; 
  \left\{
  \array{
     ch
     \big(
       V_{2 n} 
     \big)
     -
     e(f)
     \cdot
     ch
     \big(
       V_{2(n + n')}
     \big) 
     &
       \mapsto
     & 
       k^{n } 
     &
       \cdot 
     & 
     \big(
     ch
     (
       V_{2 n} 
     )
     -
     e(f)
     \cdot
     ch
     (
       V_{2(n + n')}
     ) 
     \big)
     \\
     ch
     (
       V_{2(n+n')} 
     )
     &
       \mapsto
     & 
       k^{n + n'} 
     &
       \cdot 
     & 
     ch
     (
        V_{2 (n + n')}
     )
   }
  \right.
  \;\;\;\;
  \in
  \;
  H^{ev}\big( C_f; \, \mathbb{Q} \big)/H^{2(n+n')}\big( C_f; \, \mathbb{Z} \big)
  \,.
\]

Here, since $V_{2n}$ is well defined modulo addition (eq:DependenceOfDegree2nGeneratorOnChoiceOfSplitting) of integral multiples of $V_{2(n+n')}$, and since 

\[
  \label{ChernCharacterOnCofiverSpaceOfGeneratorofTopCell}
  ch\big( V_{2(n+n')} \big)
  \;=\;
  1 
  \,\in\,
  \mathbb{Z}
  \,\simeq\,
  H^{2(n+n')}\big( C_f;\, \mathbb{Z} \big)
  \,,
\]

this expression (eq:EigenvectorsOfAdamsOperationsAfterPassageThroughChernCharacter) is well-defined in [[ordinary cohomology|ordinary]] [[rational cohomology]] in even degrees [[modulo]] [[integral cohomology]] in top degree.

But since the [[eigenvectors]] of $\psi^k_H $ to [[eigenvalue]] $k^r$ are precisely the ordinary cohomology classes in homogeneous degree $H^{2r}\big( C_f;\, \mathbb{Q} \big) \,\subset\, H^{ev}\big( C_f;\, \mathbb{Q} \big)$ (see [there](Adams+operations+compatible+with+the+Chern+character#eq:AdamsOperationOnOrdinaryCohomologyInDegree2r)), this means that

$$
  ch
  \big(
    V_{2n}
  \big)
  \;\;=\;\;
  \underset{
    \in \; H^{2n}\big( C_f; \, \mathbb{Q} \big)
  }{
    \underbrace{
       ch
       \big(
         V_{2n} 
       \big)
       - 
       e(f)
       \cdot
       ch
       \big(
         V_{2(n+n')}
       \big)
    }
  }
  \;+\;
  \underset{
    \in \; H^{2(n + n')}\big( C_f; \, \mathbb{Q}/\mathbb{Z} \big)
  }{
    \underbrace{
       e(f)
       \cdot
       ch
       \big(
         V_{2(n+n')}
       \big)
       \,.
    }
  }
$$

(See also [Conner-Floyd 66, p. 100](#ConnerFloyd66).)

The evaluation of this cohomology class on the [[fundamental class]] of $C_f$ picks out the [[coefficient]] of $ch\big( V_{2(n+n')} \big)$, by (eq:ChernCharacterOnCofiverSpaceOfGeneratorofTopCell):

$$
  \int_{C_f}
  ch
  \big(
    V_{2n}
  \big)
  \;=\;
  e(f)
  \;\;\;
  \in
  \;
  \mathbb{Q}/\mathbb{Z}
  \,,
$$

and hence the claim follows.

=--




\linebreak


### As a cobordism invariant of U-manifolds with framed boundary
 {#AsACobordismInvariantOfManifoldsWithBoundary}

We discuss how the [[e-invariant]] in its [[Q/Z]]-incarnation (Def. \ref{eInvariantInComplexTopologicalKtheoryAsRationalNumberModuloIntegers}) has a natural formulation in [[cobordism theory]] ([Conner-Floyd 66](#ConnerFloyd66)). 

This is Prop. \ref{EInvariantIsToddClassOnCoboundingUFrManifold} below; but first to recall some background:


+-- {: .num_remark} 
###### Remark

In generalization to how the [[U-bordism ring]] $\Omega^U_{2k}$ is [[Brown representability theorem|represented]] by [[homotopy classes]] of [[maps]] into the [[Thom spectrum]] [[MU]], so the [[(U,fr)-bordism ring]] $\Omega^{U,fr}_{2k}$ is represented by maps into the [[quotient spaces]] $MU_{2k}/S^{2k}$ (for $S^{2k} = Th(\mathbb{C}^{k}) \to Th( \mathbb{C}^k \times_{U(k)} E U(k) ) = MU_{2k}$ the canonical inclusion):

\[
  \label{InTermsOfHomotopyGroupsOfQuotientedThomSpace}
  \Omega^{(U,fr)}_\bullet
  \;=\;
  \pi_{\bullet + 2k}
  \big(
    MU_{2k}/S^{2k}
  \big)
  \,,
  \;\;\;\;\;
  \text{for any}
  \;
  2k \geq \bullet + 2
  \,.
\]

=--

([Conner-Floyd 66, p. 97](#ConnerFloyd66))


+-- {: .num_remark} 
###### Remark

The [[bordism rings]] for [[MU]], [[MUFr]] and [[MFr]] sit in a [[short exact sequence]] of the form

\[
  \label{ShortExactSequenceOfUFrBordismRings}
  0 
  \to
  \Omega^U_{\bullet+1}
  \overset{i}{\longrightarrow}
  \Omega^{U,fr}_{\bullet+1}
  \overset{\partial}{
    \longrightarrow
  }
  \Omega^{fr}_\bullet
  \to
  0
  \,,
\]

where $i$ is the evident inclusion, while $\partial$ is restriction to the [[boundary]].

(By [this Prop.](MUFr#AShortExactSequenceOfUFrBordismRings) at _[[MUFr]]_.)

In particular, this means that $\partial$ is [[surjective function|surjective]], hence that every $Fr$-manifold is the boundary of a [[(U,fr)-manifold]].

=--


+-- {: .num_prop #EInvariantIsToddClassOnCoboundingUFrManifold} 
###### Proposition
**([[e-invariant is Todd class of cobounding (U,fr)-manifold]])**

Evaluation of the [[Todd class]] on [[(U,fr)-manifolds]] yields [[rational numbers]] which are [[integers]] on actual $U$-manifolds. It follows with the [[short exact sequence]] (eq:ShortExactSequenceOfUFrBordismRings) that assigning to $Fr$-manifolds the Todd class of any of their cobounding $(U,fr)$-manifolds yields a well-defined element in [[Q/Z]].

Under the [[Pontrjagin-Thom isomorphism]] between the [[framed bordism ring]] and the [[stable homotopy group of spheres]] $\pi^s_\bullet$, this assignment coincides with the [[Adams e-invariant]] in [its Q/Z-incarnation](#TheEInvariantAsAnElementOfQModZ):

\[
  \label{ToddClassesOnShortExactSequenceOfUFrBordismRings}
  \array{
  0 
  \to
  &
  \Omega^U_{\bullet+1}
  &
  \overset{i}{\longrightarrow}
  &
  \Omega^{U,fr}_{\bullet+1}
  &
  \overset{\partial}{
    \longrightarrow
  }
  &
  \Omega^{fr}_\bullet
  &
  \simeq
  &
  \pi^s_\bullet
  \\
  & 
  \big\downarrow{}^{\mathrlap{Td}}
  &&
  \big\downarrow{}^{\mathrlap{Td}}
  &&
  \big\downarrow{}^{}
  &&
  \big\downarrow{}^{e}
  \\
  0 
  \to
  & 
  \mathbb{Z}
  &\overset{\;\;\;\;\;}{\hookrightarrow}&
  \mathbb{Q}  
  &\overset{\;\;\;\;}{\longrightarrow}&
  \mathbb{Q}/\mathbb{Z}
  &=&
  \mathbb{Q}/\mathbb{Z}
  }
  \,,
\]

=--

([Conner-Floyd 66, Theorem 16.2](#ConnerFloyd66))

The first step in the proof of (eq:ToddClassesOnShortExactSequenceOfUFrBordismRings) is the observation ([Conner-Floyd 66, p. 100-101](#ConnerFloyd66)) that the representing map (eq:InTermsOfHomotopyGroupsOfQuotientedThomSpace) for a $(U,fr)$-manifold $M^{2k}$ cobounding a $Fr$-manifold represented by a map $f$ is given by the following [[homotopy coherent diagram|homotopy]] [[pasting diagram]] (see also at _[[Hopf invariant]] -- [In generalized cohomology](Hopf+invariant#InGeneralizedCohomology)_):

\begin{imagefromfile}
        "file_name": "CoboundingUFrManifoldDiagrammatically.jpg",
        "web": "nlab",
        "width": 470,
        "unit": "px",
        "margin": {
            "top": -20,
            "right": 0,
            "bottom": 20,
            "left": 20,
            "unit": "px"
        },
        "alt": "homotopy pasting diagram exhibiting cobounding UFr-manifolds",
        "caption": "from [SS21](https://ncatlab.org/schreiber/show/Equivariant+Cohomotopy+and+Oriented+Cohomology+Theory)"
\end{imagefromfile}


\linebreak

## For $E = KO$
 {#KOVersion}

### The Adams $e_{\mathbb{R}}$-invariant in $\mathbb{Q}/\mathbb{Z}$

Definition \ref{eInvariantInComplexTopologicalKtheoryAsRationalNumberModuloIntegers} applies verbatim also with real (i.e. orthogonal) [[topological K-theory]] [[KO]] in place of complex topological K-theory [[KU]]. The resulting invariant is denoted $e_{\mathbb{R}}$ ([Adams 66, p. 39](#Adams66)).

### As a cobordism invariant of $SU$-manifolds with framed boundary

An analogous but finer version of the [[cobordism theory|cobordism]]-theoretic construction ([above](#AsACobordismInvariantOfManifoldsWithBoundary))  works for [[special unitary group]]-structure instead of [[unitary group]]-structure and in dimensions $8\bullet + 4$: 

Since on $(8 \bullet + 4)$-dimensional $SU$-manifolds the [[Todd class]] is divisible by 2 [Conner-Floyd 66, Prop. 16.4](#ConnerFloyd66), we have ([Conner-Floyd 66, p. 104](#ConnerFloyd66)) the following variant of (eq:ToddClassesOnShortExactSequenceOfUFrBordismRings):

\[
  \label{HalfToddClassesOnShortExactSequenceOfSUFrBordismRings}
  \array{
  0 
  \to
  &
  \Omega^{SU}_{8\bullet+4}
  &
  \overset{i}{\longrightarrow}
  &
  \Omega^{SU,fr}_{8\bullet+4}
  &
  \overset{\partial}{
    \longrightarrow
  }
  &
  \Omega^{fr}_{8 \bullet + 3}
  &
  \simeq
  &
  \pi^s_{8 \bullet + 3}
  \\
  & 
  \big\downarrow{}^{\tfrac{1}{2}\mathrlap{Td}}
  &&
  \big\downarrow{}^{\tfrac{1}{2}\mathrlap{Td}}
  &&
  \big\downarrow{}^{}
  &&
  \big\downarrow{}^{e_{\mathbb{R}}}
  \\
  0 
  \to
  & 
  \mathbb{Z}
  &\overset{\;\;\;\;\;}{\hookrightarrow}&
  \mathbb{Q}  
  &\overset{\;\;\;\;}{\longrightarrow}&
  \mathbb{Q}/\mathbb{Z}
  &=&
  \mathbb{Q}/\mathbb{Z}
  }
  \,.
\]

This produces $e_{\mathbb{R}}$, the [[Adams e-invariant]] with respect to [[KO]]-theory instead of [[KU]] ([Adams 66, p. 39](#Adams66)), which, in degrees $8k + 3$, is indeed half of the e-invariant $e_{\mathbb{C}}$ for $KU$ (by [Adams 66, Prop. 7.14](#Adams66)). 

\linebreak

## Diagrammatic construction
 {#ConstructionViaUnitCofiberTheories}

> under construction -- not complete yet

The following is meant to be another, more abstractly homotopy theoretic, way to approach the construction of the e-invariant (following [[schreiber:M-Theory as Mf-Theory|SS21]]). This perspective makes various facts immediately manifest, notably the equality between Adams's construction via the Chern character on [[KU]] and Conner-Floyd's construction via the Todd character on [[MUFr]]. 

1. [Preliminaries](#DiagrammaticConstructionPreliminaries)

1. [Unit cofiber cohomology theory](#UnitCofiberCohomologyTheory)

1. [The diagrammatic e-invariant](#TheDiagrammaticEInvariant)

1. [Recovering Adams's construction](#DiagrammaticEInvariantRecoveringAdamsConstruction)

1. [Recovering Conner-Floyd's construction](#ConnerFloydTheoremViaPastingDiagram)



### Preliminaries
 {#DiagrammaticConstructionPreliminaries}

First some **Notation:** 

* For $E$ a [[spectrum]] and $n \in \mathbb{Z}$ we write 

  * $E^n \coloneqq \Omega^\infty \Sigma^n E$ for the $n$th component space 
  
  *  $E_n  \coloneqq  \pi_n(E)  \simeq  \widetilde E{}^0(S^n)  \simeq  \pi_0(E^{-n})$ for its [[homotopy groups of a spectrum|homotopy groups]]. 

* For $R$ a [[ring]] we write $H R$ for its [[Eilenberg-MacLane spectrum]]
and $ H^{\mathrm{ev}}R \;\coloneqq\; \underset{k \in \mathbb{N}}{\oplus} \Sigma^{2k} H R$ for its [[connective spectrum|connective]] even 2-periodic version.


The **Setup** is as above, which we recall for completeness:

* Let $n, d \in \mathbb{N}$, with $d \geq 1$,

* consider a map $ S^{2(n+d)-1} \xrightarrow{\;c\;} S^{2n}$ representing a class in $\mathbb{S}_{2d-1}$, which we will denote by the same name.

  Without restriction of generality we may assume that this class is non-trivial $c \neq 0 \,\in\, \mathbb{S}_{2d-1}\,.$

* We write $C_c$ for the cofiber space of $c$:

\begin{xymatrix}
    S^{2(n+d)-1}
    \ar[r]^-c
    &
    S^{2n}
    \ar[r]
    &
    C_c
    \ar[r]
    &
    S^{2(n+d)}
    \ar[r]^{ \Sigma c }
    &
    S^{2 n + 1}
    \ar[r]
    & 
    \cdots
\end{xymatrix}



### Unit cofiber cohomology theory
 {#UnitCofiberCohomologyTheory}


\begin{definition}[Unit cofiber cohomology theory]
  \label{UnitCofiberCohomologyTheory}

For $E$ a [[multiplicative cohomology theory]] ([[Brown representability theorem|represented]] by a [[homotopy-commutative ring spectrum]]) with unit operation $\mathbb{S} \overset{ e^E }{\longrightarrow} E$ we denote the corresponding [[homotopy cofiber]]-theory $E/\mathbb{S}$. 

(In notation common around the [[Adams spectral sequence]] this would be 
"$\Sigma \overline {E}$" -- as in [Adams 74, theorem 15.1 page 319](Adams+spectral+sequence#Adams74) --  or just "$\overline{ E }$" -- as in [Hopkins 99, Cor. 5.3](Adams+spectral+sequence#Hopkins99)).

Via the induced [[homotopy cofiber sequence]] 

\begin{xymatrix}
      \mathbb{S}
      \ar[r]^{1^E}
      &
      E
      \ar[r]
      &
      E/\mathbb{S}
      \ar[r]
      &
      \Sigma \mathbb{S}
      \ar[r]^{ \Sigma (1^E) }
      &
      \Sigma E 
      \ar[r]
      &
      \cdots
\end{xymatrix}

this comes with a canonical [[cohomology operation]] $\partial \;\colon\; E/\mathbb{S} \longrightarrow \Sigma \mathbb{S}$ to shifted [[stable Cohomotopy]]:

\begin{xymatrix@C=50pt@R=12pt}

    \mathbb{S}
    \ar[dd]
      ^>>{\ }="t"
    \ar[rr]
      ^-{
        \;1^E\;
      }
      _>>{\ }="s"
    &&
    \overset{
      \mathclap{
      \raisebox{4pt}{
        \tiny
        \color{blue}
        \bf
        \begin{tabular}{c}
          $E$-cohomology
        \end{tabular}
      }
      }
    }{
      E
    }
    \ar[dd]
      _-{
        \mathclap{\phantom{\vert^{\vert^{\vert}}}}
        i^E
        \mathclap{\phantom{\vert_{\vert}}}
      }
      ^>>{\ }="t2"
    \ar[rr]
      ^-{
      }
      _>>{\ }="s2"
    &&
    \ast
    \ar[dd]
    \\
    {\phantom{A}}
    \\
    \ast
    \ar[rr]
    &&
    \underset{
      \mathclap{
      \raisebox{-4pt}{
        \tiny
        \color{blue}
        \bf
        \begin{tabular}{c}
          $E$-cofiber
          \\
          cohomology
          \\
          theory
        \end{tabular}
      }
      }
    }{
      E/\mathbb{S}
    }
    \ar[rr]
      |-{ \;\partial^E\; }
      _-{
        \mbox{
          \tiny
          \color{green}
          \bf
          \begin{tabular}{c}
            \phantom{-}
            \\
            boundary
            \\
            operation
          \end{tabular}
        }
      }
    &&
    \underset{
      \mathclap{
      \raisebox{-6pt}{
        \tiny
        \color{blue}
        \bf
        \begin{tabular}{c}
          shifted stable
          \\
          Cohomotopy
        \end{tabular}
      }
      }
    }{
      \Sigma \mathbb{S}
    }
    \,,
    &
    {\phantom{AAA}}
    %
    \ar@{=>}^-{ \mbox{\tiny\rm(po)} }
      "s"; "t"
    \ar@{=>}^-{ \mbox{\tiny\rm(po)} }
      "s2"; "t2"

\end{xymatrix}

\end{definition}

\begin{definition}\label{InducedCohomologyOperationsOnCofiberCohomology}
  [Induced cohomology operations on cofiber cohomology]
  Let $E \overset{\phi}{\longrightarrow} F$ be a 
  [[multiplicative cohomology theory|multiplicative]] 
  [[cohomology operation]], so that in particular 
  it preserves the units, witnessed 
  by a homotopy-commutative square on the 
  left here:
\begin{xymatrix@=24pt}
    \mathbb{S}
    \ar[rr]|-{ \;1^{E}\; }
    \ar@{=}[d]
    &&
    E
    \ar[d]
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        \phi
        \mathclap{\phantom{\vert_{\vert}}}
      }
    \ar[rr]
    &&
    E/\mathbb{S}
    \ar[rr]|-{ \;\partial^E\; }
    \ar[d]
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        \phi/\mathbb{S}
        \mathclap{\phantom{\vert_{\vert}}}
      }
    &&
    \Sigma \mathbb{S}
    \ar@{=}[d]
    \\
    \mathbb{S}
    \ar[rr]|-{ \;1^F\; }
    &&
    F
    \ar[rr]
    &&
    F/\mathbb{S}
    \ar[rr]|-{ \;\partial^F\; }
    &&
    \Sigma\mathbb{S}
    \,.
\end{xymatrix}
Then passing to [[homotopy cofibers]] yields  the induced cohomology operation $\phi/\mathbb{S}$ on cofiber theories (Def. \ref{UnitCofiberCohomologyTheory}).
\end{definition}

\begin{example}\label{ChernCharacterOnCofiberOfKTheory}
  [Chern character on cofiber of K-theory]
  The [[Chern character]] operation 
  $\mathrm{KU} \overset{\phi}{\longrightarrow} H^{\mathrm{ev}}\mathbb{Q}$
  is multiplicative, hence passes to an operation
  $\mathrm{KU}/\mathbb{S} 
    \overset{ \;\mathrm{ch}/\mathbb{S}\; }{\longrightarrow}
    H^{\mathrm{ev}}\mathbb{Q}$
   via Def. \ref{InducedCohomologyOperationsOnCofiberCohomology}.   
\end{example}

In a similar fashion we get:

\begin{remark}
\label{CanonicalSplittingOfCofiberOfPeriodicRationalCohomology}
There is a canonical [[split exact sequence|splitting]]  $\mathrm{spl}_0$ of the [[short exact sequence]]

\begin{xymatrix@=18pt}
    0
    \ar[r]
    &
    \big(
      \widetilde {H^{\mathrm{ev}}\mathbb{Q}}
    \big)
    {}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    \ar[rr]
    \ar@{=}[d]
    &&
    \big(
      \widetilde {(H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}}
    \big)
    {}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    \ar[rr]
    \ar[d]
      |-{
      \hspace{2.7pt}
      \scalebox{.7}{
        \rotatebox{-90}{$
          \,
          \simeq
          \,
        $}
      }
      }
      _{\mathrm{spl}_0}
    &&
    \widetilde {\mathbb{S}}
    {}^{2n+1}
    \big(
      S^{2(n+d)}
    \big)
    \ar[r]
    \ar@{=}[d]
    &
    0
    \\
    0
    \ar[r]
    &
    \mathbb{Q}
    \;
    \ar@{^{(}->}[rr]
    &&
    \mathbb{Q}
    \oplus
    \mathbb{S}_{2d-1}
    \ar@{->>}[rr]
    &&
    \mathbb{S}_{2d-1}
    \ar[r]
    &
    0
    \,,
\end{xymatrix}

namely that coming from the inclusion 
$H\mathbb{Q} \hookrightarrow H^{\mathrm{ev}}\mathbb{Q}$ (which is multiplicative, in particular preserves the unit):

\begin{xymatrix@=18pt}
    0
    \ar[r]
    &
    \big(
      \widetilde {H\mathbb{Q}}
    \big)
    {}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    \ar[rr]
    \ar@{=}[d]
    &&
    \big(
      \widetilde {(H\mathbb{Q})/\mathbb{S}}
    \big)
    {}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    \ar[rr]
    \ar[d]|-{
      \hspace{2.7pt}
      \scalebox{.7}{
        \rotatebox{-90}{$
          \,
          \simeq
          \,
        $}
      }
    }
    &&
    \widetilde {\mathbb{S}}
    {}^{2n+1}
    \big(
      S^{2(n+d)}
    \big)
    \ar[r]
    \ar@{=}[d]
    &
    0
    \\
    0
    \ar[r]
    &
    0
    \;
    \ar@{^{(}->}[rr]
    &&
    \mathbb{S}_{2d-1}
    \ar@{=}[rr]
    &&
    \mathbb{S}_{2d-1}
    \ar[r]
    &
    0
\end{xymatrix}

\end{remark}



\begin{lemma}
  \label{CofiberECohomologyAsExtensionOfStableCohomotopyByECohomology}
  [Cofiber $E$-cohomology as extension of stable Cohomotopy by $E$-cohomology]

  For $E$ a [[multiplicative cohomology theory]] and
  $X$ a space, assume that the
  $E$-[[Boardman homomorphism]]
  $\widetilde {\mathbb{S}}{}^\bullet(X) \xrightarrow{ \;\beta^\bullet_X\; }
  \widetilde E^\bullet(X)$
  is [[zero morphism|zero]] in degrees $n$ and $n + 1$
  -- for instance in that $X \simeq S^{k \geq 2}$,
  $n = 0$ and the
  groups $\widetilde E^0(S^k) = \pi_k(E)$ have no [[torsion subgroup|torsion]] --
  then the [[cohomology operations]] $i^E$, $\partial^E$
  form a [[short exact sequence]] of [[cohomology groups]]:

\begin{xymatrix@C=12pt}
      0
      \ar[r]
      &
      \widetilde E
      \big(
        X
      \big)
      \;
      \ar@{^{(}->}[rr]^-{ i }
      &&
      (
      \widetilde
      {
        E/\mathbb{S}
      }
      ){}^n(X)
      \ar@{->>}[rr]^-{ \partial }
      &&
      \widetilde {\mathbb{S}}{}^{n+1}(X)
      \ar[r]
      &
      0
\end{xymatrix}

\end{lemma}

(e.g. [Stong 68, p. 102](MOFr#Stong68))

\begin{proof}
  Generally, the long cofiber sequence of cohomology theories

  induces a long exact sequence of cohomology groups (...)

\begin{xymatrix@C=12pt}
      \cdots
      \ar[r]
      &
      \widetilde {\mathbb{S}}{}^{n}(X)
      \ar[rr]^-{ 1^n_X }
      &&
      \widetilde E^n(X)
      \ar[rr]^-{ i^n_X }
      &&
      (\widetilde{E/\mathbb{S}})^n(X)
      \ar[rr]^-{ \partial^n_X }
      &&
      \widetilde S^{n+1}(X)
      \ar[rr]^-{ 1^{n+1}_X }
      &&
      \widetilde {E}^{n+1}(X)
      \ar[r]
      &
      \cdots
\end{xymatrix}
 Under the given assumption the two outermost morphisms
  shown are zero, and hence the sequence truncates as claimed.

\end{proof}










### The diagrammatic e-invariant
 {#TheDiagrammaticEInvariant}

\begin{proposition}\label{EFluxesAreCocycleInCofiberTheory}
  Let $E$ be a [[multiplicative cohomology theory]]
  and $n,d \in \mathbb{N}$. 
  Consider the [[function]] that sends [[pairs]] consisting of 
  
  1. the stable class  $\big[ G^{\mathbb{S}}_n (c) \big]$ of a map $S^{n+d-1} \overset{\;c\;}{\longrightarrow} S^n$ 
  
  1. the class of a trivialization $H^E_{n-1}\!(c)$ of its [[d-invariant]] in $E$-cohomology

\begin{xymatrix@C=18pt}
    S^{n + d - 1}
    \ar[dd]
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        \color{green}
        c
        \mathclap{\phantom{\vert_{\vert}}}
      }
      ^>>>{\ }="t"
    \ar[rr]_>>>{\ }="s"
    &&
    \ast
    \ar[dd]
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        0
        \mathclap{\phantom{\vert_{\vert}}}
      }
    \\
    \\
    S^n
    \ar[rr]
      |-{
        \;
        \Sigma^n (1^E)
        \;
      }
    &&
    E^{n}
    %
    \ar@{=>}
      |-{
        \mathclap{\phantom{\vert^{\vert^{\vert}}}}
        \color{orange}
        H^E_{n-1}\!(c)
        \mathclap{\phantom{\vert_{\vert_{\vert}}}}
      }
     "s"; "t"
\end{xymatrix}

to the class in $(E/\mathbb{S})_d$ of this diagram:

\begin{xymatrix@=30pt}
   S^{n + d - 1}
   \ar[dd]
     |-{
       \mathclap{\phantom{\vert^{\vert}}}
       \color{green}
       c
       \mathclap{\phantom{\vert_{\vert}}}
     }
   \ar[rr]
   \ar@{}[ddrr]|-{
     \rotatebox[origin=c]{-45}{\color{orange}$\big\Downarrow$}
     \mbox{\tiny (po)}
   }
   &&
   \ast
   \ar[dr]
   \ar[dd]
   \\
   && &
   \ast
   \ar[dd]|-{
     \mathclap{\phantom{\vert^{\vert}}}
     0
     \mathclap{\phantom{\vert_{\vert}}}
   }
   \\
   S^{n}
   \ar[dd]
   \ar[rr]
   \ar@{}[ddrr]|-{
     \rotatebox[origin=c]{-45}{$\big\Downarrow$}
     \mbox{\tiny (po)}
   }
   \ar@/_.7pc/[drrr]
     |<<<<<{ \;\Sigma^{n} (1^{E})\;\; }
     |>>>>>>>>>>{ {\phantom{AA}} \atop {\phantom{AA}} }
   &&
   C_c
   \ar[dd]
   \ar@{-->}[dr]|-{
     \vdash
     {
       \color{orange}
       H^E_{n-1}\!(c)
     }
   }
   &&
   \\
   && &
   E^{n}
   \ar[dd]
   \\
   \ast
   \ar@/_.7pc/[drrr]|-{ \;0\; }
   \ar[rr]
   &&
   S^{n + d}
   \ar@{-->}[dr]|-{
     \mathllap{\vdash}
     (
       {\color{green}
         G^{\mathbb{S}}_n\!(c)
       }
       \,,\,
       {\color{orange}
         H^E_{n-1}\!(c)
       }
     )
   }
   &&
   \\
   && &
   (E/\mathbb{S})^{n}
\end{xymatrix}


  Then: This function a [[bijection]] which respects the canonical 
  fibrations of both sides over 
  $\mathbb{S}_{d-1}$.
    
\end{proposition}
See also [this Prop.](d-invariant#EFluxesAreCocycleInCofiberTheory) at _[[d-invariant]]_.




\begin{proof}

**First**, here is a quick formal argument to see that _some_ such bijection does exist:

By Definition \ref{SetOfTrivializationsOfTheDInvariant}, an element in $H_{n-1}Fluxes^E\big( S^{n+d-1} \big)$ is equivalently the class of a homotopy [[cone]] with tip $\Sigma^{n+d-1} \mathbb{S}$ over the [[cospan]] formed by the ring spectrum unit $e^E$ and the [[zero morphism]]:

\begin{xymatrix@=26pt}
    \Sigma^{n+d-1}\mathbb{S}
    \ar[rr]_>>>{\ }="s"
    \ar[dd]^>>>{\ }="t"
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        c
        \mathclap{\phantom{\vert_{\vert}}}
      }
    &&
    \ast
    \ar[dd]
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        0
        \mathclap{\phantom{\vert_{\vert}}}
      }
    \\
    \\
    \Sigma^n \mathbb{S}
    \ar[rr]
      |-{
        \; \Sigma^n(e^E) \;
      }
    &&
    \Sigma^n E
    %
    \ar@{=>}
      |-{
        \mathclap{\phantom{\vert^{\vert^{\vert}}}}
        {
          \color{orange}
          H^E_{n-1}\!(c)
        }
        \mathclap{\phantom{\vert_{\vert_{\vert}}}}
      }
      "s"; "t"
\end{xymatrix}

But in [[Spectra]] [[homotopy cofiber sequences]] are [[homotopy fiber sequences]] (by [this Prop.](Spectrum#InSpectraHomotopyFiberSequencesAreHomotopyCofiberSequences)), so that by the [[universal property]] of [[homotopy fibers]] the class of the above diagram is equivalently the class of a map from $\Sigma^{n+d-1}\mathbb{S}$ to  $fib\big( \Sigma^{n} e^E \big) \,\simeq\, \Sigma^{n-1} (E/\mathbb{S}$):

\begin{xymatrix@=26pt}
    \Sigma^{n+d-1}\mathbb{S}
    \ar@/_1pc/[dddr]
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        c
        \mathclap{\phantom{\vert_{\vert_{\vert}}}}
      }
    \ar@/^1pc/[rrrd]
    \ar@{-->}[dr]
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        \vdash
        {
          \color{orange}
          H^E_{n-1}\!(c)
        }
        \mathclap{\phantom{\vert_{\vert}}}
      }
    \\
    & 
    \Sigma^{n-1}
    (\mathbb{S}/E)
    \ar[rr]_>>>{\ }="s"
    \ar[dd]^>>>{\ }="t"
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        \partial
        \mathclap{\phantom{\vert_{\vert}}}
      }
    &&
    \ast
    \ar[dd]
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        0
        \mathclap{\phantom{\vert_{\vert}}}
      }      
    \\
    \\
    &
    \Sigma^n \mathbb{S}
    \ar[rr]
      |-{
        \;\Sigma^n(e^E)\;
      }
    &&
    \Sigma^n E
    %
    \ar@{=>} 
      ^-{ \mbox{\tiny\color{orange}(pb)} }
    "s"; "t"
\end{xymatrix}


This implies the claim, by 

$$
  \pi_0
  Maps
  \Big(
    \Sigma^{n+d - 1}\mathbb{S}
    \,,\,
    \Sigma^{n-1} (E/\mathbb{S})
  \Big)
  \;\simeq\;
  (E/\mathbb{S})_{d}
  \,.
$$

\linebreak

**Second,** to see that this bijection is realized as claimed (the following constructions is close to the proof of [Conner-Floyd 66, Theorem 16.2](MUFr#ConnerFloyd66)): 


Let
$\big[ S^{n + d - 1} \overset{c}{\longrightarrow} S^{n} \big] \;\in\; \pi^n\big(S^{n+d-1}\big)$ be a given class in Cohomotopy.
We need to produce a map of the form

\begin{xymatrix@R=10pt}
    {
      \color{orange}
      H^E_{n-1}\!(c)
    }
    \ar@{}[rr]|-{\longmapsto}
    &&
    M^d
    \\
    H_{n-1}\mbox{Fluxes}(X)_c
    \ar[rr]
    \ar[dd]
    &&
    \big(
      E\!/\mathbb{S}
    \big)_d
    \ar[dd]^-{ \partial }
    \\
    {\phantom{A}}
    \\
    \big\{
      [
        \Sigma^\infty c
      ]
    \big\}
    \;
    \ar@{^{(}->}[rr]
    &&
    \;
    \mathbb{S}_{d-1}
\end{xymatrix}

and show that it is a bijection onto this fiber, hence that the square is [[cartesian square|cartesian]]. To this end, we discuss the following [[homotopy coherent diagram|homotopy]] [[pasting diagram]], all of whose cells are homotopy cartesian:

\begin{xymatrix@R=15pt@C=60pt}
    \Sigma^\infty S^{n + d - 1}
    \ar[dd]_-{
      \Sigma^\infty
      {\color{green}
        c
      }
    }
    \ar[rr]
    &&
    \ast
    \ar[dd]
    \\
    \\
    \Sigma^\infty S^{n}
    \ar[dd]
    \ar[rr]|-{ 
      %\;\Sigma^\infty q_c\; 
    }
    \ar@/_1.4pc/[rrr]
      |<<<<<<<<<<<<<<<<<<<{
        \; \Sigma^{n}(e^{E}) \;
      }
    &&
    \Sigma^\infty C_c
    \ar[dd]|<<<<{ \phantom{A} }
    \ar@{-->}[r]
    \ar@{}[r]
    |-{
      \scalebox{.7}{$
        \begin{array}{c}
          \vdash
          {\color{orange}
            H^E_{n-1}\!(c)
          }
          \\
          {\phantom{a}}
        \end{array}
      $}
    }
    \ar@/^2pc/[rr]
    &
    \Sigma^n E
    \ar[r]
    \ar[dd]
    &
    \ast
    \ar[dd]
    \\
    \\
    \ast
    \ar[rr]
    &&
    \Sigma^{\infty\scalebox{.6}{$+1$}} S^{n + d - 1}
    \ar[r]^-{
      \color{magenta}
      M^{d}
    }
    \ar@/_1.2pc/[rr]|-{
      \;
      \Sigma^{\infty\scalebox{.5}{$+1$}}
      {\color{green}
        c
      }
      \;
    }
    &
    \Sigma^{n}(E\!/\mathbb{S})
    \ar[r]^{ \partial }
    &
    \Sigma^{\infty\scalebox{.6}{$+1$}} S^{n}
\end{xymatrix}

For given $H^E_{n-1}\!(c)$, this diagram is constructed as follows
(where we say "square" for any _single_ cell and "rectangle" for the pasting composite of any adjacent _pair_ of them):

* The two squares on the left are the stabilization of the homotopy pushout squares defining the cofiber space $C_c$ and the suspension of $S^{n + d - 1}$

* The bottom left rectangle (with $\Sigma^n(e^E)$ at its top)
is the homotopy pushout defining $\Sigma^n(E\!/\mathbb{S})$.

* The classifying map for the given $(n-1)$-flux, shown as a dashed arrow,
completes a co-cone under the bottom left square. Thus the map ${\color{magenta}M^d}$ forming the bottom middle square is uniquely implied by the homotopy pushout property of the bottom left square.
Moreover, the [[pasting law]] implies that this bottom middle square is itself homotopy cartesian.

* The bottom right square is the homotopy pushout defining $\partial$.

* By the [[pasting law]] it follows that also the bottom right rectangle is homotopy cocartesian, hence that, after the two squares on the left, it exhibits the third step in the long homotopy cofiber sequence of $\Sigma^\infty c$. This means that its total bottom morphism is $\Sigma^{\infty + 1} c$, and hence that $\partial \big[ M^d \big] = [c]$.


In conclusion, these construction steps yield a map map $H^E_{n-1}\!(c) \mapsto M^d$ over $[\Sigma^\infty c]$ a required.

It only remains to see that this map is bijective over any $\big[\Sigma^\infty c\big]$: So assume conversely that $M^d$ is given, and with it the above diagram  except for the dashed arrow. But since the bottom right square is a [[homotopy pushout]], it is also a [[homotopy pullback]] (by [this Prop.](Spectrum#InSpectraHomotopyFiberSequencesAreHomotopyCofiberSequences)), so that a dashed morphism is uniquely implied. By its uniqueness, this reverse assignment $M^{2d} \mapsto H^E_{n-1}\!(c)$ must be the inverse of the previous construction.

\end{proof}
























\begin{definition}
  \label{LiftedEInvariantDiagrammatically}
The _lifted e-invariant_ $\widehat e_{\mathbb{C}}$ is the composite of 

1. the equivalence from Prop. \ref{EFluxesAreCocycleInCofiberTheory} for $E = $ [[KU]],

1. the cofiber Chern character from Example \ref{ChernCharacterOnCofiberOfKTheory},

1. the canonical splitting from Remark \ref{CanonicalSplittingOfCofiberOfPeriodicRationalCohomology}:

\begin{xymatrix@C=40pt@R=6pt}
    H^{\mathrm{KU}}_{n-1}\mbox{Fluxes}
    \big(
      S^{2(n+d)-1}
    \big)
    \ar[r]|-{
      \raisebox{2.4pt}{
        \scalebox{.7}{$\simeq$}
      }
    }
    &
    (\mathrm{KU}/\mathbb{S})_{2d}
    \ar[r]_-{\;\mathrm{ch}/\mathbb{S}\;}
    &
    \big((H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}\big)_{2d}
    \ar[r]
      |-{
        \raisebox{2.2pt}{
        \scalebox{.7}{$
          \simeq
        $}
        }
      }
      _-{ \mathrm{spl}_0 }
    &
    \mathbb{S}_{2(n+d)-1}
    \oplus
    \mathbb{Q}
    \\
    \Big(
      [{\color{green}c}]
      ,
      \big[
        {\color{orange}
        H^{\mathrm{KU}}_{2n-1}\!(c)
        }
      \big]
    \Big)
    \ar@{|->}[rrr]
    &
    &&
    \Big(
      [{\color{green}c}]
      ,
      {\color{orange}
        \widehat e_{\mathbb{C}}(c)
      }
    \Big)
\end{xymatrix}
sending a trivialization of the d-invariant
\begin{xymatrix@=30pt}
    S^{2(n + d) - 1}
    \ar[dd]
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        \color{green}
        c
        \mathclap{\phantom{\vert_{\vert}}}
      }
      ^>>>{\ }="t"
    \ar[rr]_>>>{\ }="s"
    &&
    \ast
    \ar[dd]
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        0
        \mathclap{\phantom{\vert_{\vert}}}
      }
    \\
    \\
    S^{2n}
    \ar[rr]
      |-{
        \;
        \Sigma^{2n} (1^{\mathrm{KU}})
        \;
      }
    &&
    \mathrm{KU}^{2n}
    %
    \ar@{=>}
      |-{
        \mathclap{\phantom{\vert^{\vert^{\vert}}}}
        \color{orange}
        H^{\mathrm{KU}}_{2n-1}\!(c)
        \mathclap{\phantom{\vert_{\vert_{\vert}}}}
      }
     "s"; "t"
\end{xymatrix}
to the class of this pasting composite:
\begin{xymatrix@R=1.8em@C=24pt}
   S^{2(n + d) - 1}
   \ar[dd]
     |-{
       \mathclap{\phantom{\vert^{\vert}}}
       \color{green}
       c
       \mathclap{\phantom{\vert_{\vert}}}
     }
   \ar[rr]
   \ar@{}[ddrr]|-{
     \rotatebox[origin=c]{-45}{\color{orange}$\big\Downarrow$}
     \mbox{\tiny (po)}
   }
   &&
   \ast
   \ar[dr]
   \ar[dd]
   \\
   && &
   \ast
   \ar[dd]|-{
     \mathclap{\phantom{\vert^{\vert}}}
     0
     \mathclap{\phantom{\vert_{\vert}}}
   }
   \\
   S^{n}
   \ar[dd]
   \ar[rr]
   \ar@{}[ddrr]|-{
     \rotatebox[origin=c]{-45}{$\big\Downarrow$}
     \mbox{\tiny (po)}
   }
   \ar@/_.7pc/[drrr]
     |<<<<<{ \;\Sigma^{n} (1^{\mathrm{MU}})\;\; }
     |>>>>>>>>>{ {\phantom{AA}} \atop {\phantom{AA}} }
   &&
   C_c
   \ar[dd]
   \ar@{-->}[dr]|-{
     \vdash
     {
       \color{orange}
       H^{\mathrm{KU}}_{2n-1}\!(c)
     }
   }
   &&
   \\
   && &
   \mathrm{KU}^{n}
   \ar[dd]
   \ar[dr]
     |-{
       \;\mathrm{ch}\;
     }
   \\
   \ast
   \ar@/_.7pc/[drrr]|-{ \;0\; }
   \ar[rr]
   &&
   S^{2(n + d)}
   \ar@{-->}[dr]|-{
     \mathllap{\vdash}
     (
       {\color{green}
         G^{\mathbb{S}}_n\!(c)
       }
       \,,\,
       {\color{orange}
         H^{\mathrm{KU}}_{n-1}\!(c)
       }
     )
   }
   &&
   (H^{\mathrm{ev}}\mathbb{Q})^{2n}
   \ar[dd]
   \\
   && &
   (\mathrm{KU}/\mathbb{S})^{n}
   \ar[dr]
     |-{
       \;\mathrm{ch}/\mathbb{S}\;
     }
   \\
   && &&
   \big(
     (H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}
   \big)^{2n}
\end{xymatrix}

\end{definition}


\begin{lemma}\label{DiagrammaticecInvariantTakesIntegerLattiveValues}
The values of the lifted e-invariant from Def. \ref{LiftedEInvariantDiagrammatically} for fixed [[Cohomotopy]] class $[c]$ form an integer lattice inside the rational numbers:

$$
  \widehat e_{\mathrm{KU}}
  \Big(
    [c],
    \big[
      H^{\mathrm{KU}}_{2d-1}\!(c)
    \big]
  \Big)
  -
  \widehat e_{\mathrm{KU}}
  \Big(
    [c],
    \big[
      {H}^\prime{}^{\mathrm{KU}}_{2d-1}\!(c)
    \big]
  \Big)
  \;\in\;
  \mathbb{Z}
$$
\end{lemma}
\begin{proof}
Using the same three ingredients that enter Def. \ref{LiftedEInvariantDiagrammatically}, we paste together the following commuting diagram, all whose rows are [[short exact sequence|exact]]:

\begin{xymatrix@R=16pt}
    \mathbb{Z}
    \;
    \ar[rr]
    \ar@{=}[d]
    &&
    H^{\mathrm{KU}}_{2n-1}\mbox{Fluxes}
    \big(
      S^{2(n+d)}
    \big)
    \ar[rr]
    \ar@{=}[d]
    &&
    \widetilde {\mathbb{S}}{}^{2n+1}
    \big(
      S^{2(n+d)}
    \big)
    \ar@{=}[d]
    \\
    \widetilde { \mathrm{KU} }{}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    \ar[rr]
    \ar[dd]|-{
      \mathclap{\phantom{\vert^{\vert}}}
      \mathrm{ch}
      \mathclap{\phantom{\vert_{\vert}}}
    }
    &&
    \big(\widetilde { (\mathrm{KU}/\mathbb{S}) }\big){}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    \ar[dd]
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        \mathrm{ch}/\mathbb{S}
        \mathclap{\phantom{\vert_{\vert}}}
      }
    \ar[rr]
    &&
    \widetilde {\mathbb{S}}{}^{2n+1}
    \big(
      S^{2(n+d)}
    \big)
    \ar@{=}[dd]
    \\
    &&
    &
    \\
    \big(
      \widetilde {H^{\mathrm{ev}}\mathbb{Q}}
    \big){}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    \ar@{=}[d]
    \ar[rr]
    &&
    \big(
      \widetilde { (H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S} }
    \big){}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    \ar[rr]
    \ar[d]
      |-{
      \hspace{2.7pt}
      \scalebox{.7}{
        \rotatebox{-90}{$
          \,
          \simeq
          \,
        $}
      }
      }
      _{\mathrm{spl}_0}
    &&
    \widetilde {\mathbb{S}}{}^{2n+1}
    \big(
      S^{2(n+d)}
    \big)
    \ar@{=}[d]
    \\
    \mathbb{Q}
    \;
    \ar@{^{(}->}[rr]
    &&
    \mathbb{Q}
    \oplus
    \mathbb{S}_{2d-1}
    \ar@{->>}[rr]
    &&
    \mathbb{S}_{2d-1}
\end{xymatrix}
\end{proof}

Hence we have a diagrammatic construction of an invariant of $[c]$ in
$\mathbb{Q}/\mathbb{Z}$. It just remains to see that this actually coincides with the classical Adams invariant:


\linebreak

### Recovering Adams's construction
  {#DiagrammaticEInvariantRecoveringAdamsConstruction}

Besides inspection of the defining homotopy-pasting diagram below, we just need the following technical lemma:

\begin{lemma}
  \label{identifyingCofiberRationalCohomoloyOfCofiberSpace}
  Given non-trivial 
  $\big[ S^{2(n+d)-1} \xrightarrow{\;c\;} S^{2n}\big] 
  \,\in \, \mathbb{S}_{2d-1}$
  for any $n,d \in \mathbb{N}$ with $d \geq 1$, we have 
  the following diagonal isomorphisms
  \begin{xymatrix@=7pt}
      &&
      \big(
        \widetilde { (H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S} }
      \big)^{2n}
      \big(
        S^{2(n+d)}
      \big)
      \ar[dd]
      \ar@{=}[dr]
      \\
      &&
      &
      \mathbb{Q} \oplus \mathbb{S}_{2d-1}
      \ar[dd]
      \\
      \big(
        \widetilde { H^{\mathrm{ev}}\mathbb{Q} }
      \big)^{2n}
      \big(
        C_c
      \big)
      \ar@{=}[dr]
      \ar[rr]
      &&
      \big(
        \widetilde { (H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S} }
      \big)^{2n}
      \big(
        C_c
      \big)
      \ar@{=}[dr]
      \\
      & 
      \mathbb{Q} \oplus \mathbb{Q}
      \ar[rr]
      &&
      \mathbb{Q} \oplus 
      \big(
        \mathbb{Q}/\mathbb{Z}
        \oplus
        \mathbb{S}_{2d-1}/\mathbb{Z}
      \big)
  \end{xymatrix}
  such that both morphisms are the identity on the first 
  $\mathbb{Q}$-summand.
\end{lemma}

Here $\mathbb{S}_{2d-1}/\mathbb{Z}$ is the [[cofiber]] of $\mathbb{Z} \xrightarrow{\;c\;} \mathbb{S}_{2d-c}$.

\begin{proof}
Consider the diagram which is the image under $\pi_0 \mathrm{Maps}^{\ast/}(-,-)$ of the sequences

\begin{xymatrix@R=12pt@C=17pt}
      \vdots
      \ar@{<-}[d]
      \\
      S^{2(n+d)}
      \ar@{<-}[dd]
      \\
      \\
      C_c
      \ar@{<-}[dd]
      \ar@{}[r]|-{ , }
      &
    (H^{\mathrm{ev}}\mathbb{Q})^{2n}
    \ar[r]
    &
    \big(
      (H^{\mathrm{ev}}\mathbb{Q})
      /
      \mathbb{S}
    \big)^{2n}
    \ar[r]
    &
    \mathbb{S}^{2n-1}      
      \\
      \\
      S^{2n}
      \ar@{<-}[d]
      \\
      \vdots
\end{xymatrix}

In this diagram all rows and columns are exact (since $\mathrm{Maps}^{\ast/}$ sends both homotopy cofiber sequences in the first argument as well as homotopy fiber sequences in the second argument to homotopy fiber sequences, and  using that these induce [[long exact sequences of homotopy groups]]).

By the definition (or [[Brown representability theorem|characterization]]) of  [[reduced cohomology|reduced]] [[Whitehead-generalized cohomology theory|generalized cohomology]] [[cohomology group|groups]], this diagram is equal (in the sector shown) to the following [[commuting diagram]] of [[abelian groups]]:

\begin{xymatrix@C=18pt}
    \widetilde {\mathbb{S}}{}^{2n}
    \big(
      S^{2n+1}
    \big)
    \ar[d]
    \ar[r]
    &
    \widetilde { (H^{\mathrm{ev}}\mathbb{Q}) }{}^{2n}
    \big(
      S^{2n+1}
    \big)
    \ar[r]
    \ar[d]
    &
    (\widetilde {(H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}}){}^{2n}
    \big(
      S^{2n+1}
    \big)
    \ar[d]
    \ar[r]
    &
    \widetilde {\mathbb{S}}{}^{2n+1}
    \big(
      S^{2n+1}
    \big)
    \ar[d]
    \\
    \widetilde {\mathbb{S}}{}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    \ar[r]
    \ar[d]
    &
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    \;
    \ar[r]
    \ar[d]
    &
    (\widetilde {(H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}}){}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    \ar[r]
    \ar[d]
    &
    \widetilde {\mathbb{S}}{}^{2n+1}
    \big(
      S^{2(n+d)}
    \big)
    \ar[d]
    \ar[r]
    &
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n+1}
    \big(
      S^{2(n+d)}
    \big)
    \ar[d]
    \\
    \widetilde {\mathbb{S}}{}^{2n}
    \big(
      C_c
    \big)
    \ar[d]
    \ar[r]
    &
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n}
    \big(
      C_c
    \big)
    \;
    \ar[r]
    \ar[d]
    &
    (\widetilde {(H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}}){}^{2n}
    \big(
      C_c
    \big)
    \ar[r]
    \ar[d]
    &
    \widetilde {\mathbb{S}}{}^{2n+1}
    \big(
      C_c
    \big)
    \ar[d]
    \ar[r]
    &
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n+1}
    \big(
      C_c
    \big)
    \\
    \widetilde {\mathbb{S}}{}^{2n}
    \big(
      S^{2n}
    \big)
    \ar[d]
    \ar[r]
    &
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n}
    \big(
      S^{2n}
    \big)
    \ar[r]
    \ar[d]
    &
    (\widetilde {(H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}}){}^{2n}
    \big(
      S^{2n}
    \big)
    \ar[r]
    &
    \widetilde {\mathbb{S}}{}^{2n+1}
    \big(
      S^{2n}
    \big)
    \\
    \widetilde {\mathbb{S}}{}^{2n}
    \big(
      S^{2(n+d)-1}
    \big)
    \ar[r]
    &
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n}
    \big(
      S^{2(n+d)-1}
    \big)
\end{xymatrix}

Evaluating here all the cohomology groups on spheres yields:
\begin{xymatrix@=18pt}
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n}
    \big(
      S^{2n+1}
    \big)
    }}
    \hspace{-28pt}
    \mathclap{
     \color{blue}
     \mathbb{S}_{1} \oplus 0
    }
    \hspace{+28pt}
    \ar[d]
    \ar[r]
    &
    {\phantom{
    \widetilde { (H^{\mathrm{ev}}\mathbb{Q}) }{}^{2n}
    \big(
      S^{2n+1}
    \big)
    }}
    \hspace{-43pt}
    \mathclap{
      \color{blue}
      0
    }
    \hspace{+43pt}
    \ar[r]
    \ar[d]
    &
    (\widetilde {(H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}}){}^{2n}
    \big(
      S^{2n+1}
    \big)
    \ar[d]
    \ar[r]
    &
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n+1}
    \big(
      S^{2n+1}
    \big)
    }}
    \hspace{-35pt}
    \mathclap{
      \color{blue}
      0 \oplus \mathbb{Z}
    }
    \hspace{+35pt}
    \ar[d]
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        \color{blue} 
        c 
        \mathclap{\phantom{\vert_{\vert}}}
      }
    \\
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    }}
    \hspace{-37pt}
    \mathclap{
      \color{blue}
      \mathbb{S}_{2d} \oplus 0
    }
    \hspace{+37pt}
    \ar[r]|<<<{ \color{blue}\;0\; }
    \ar[d]
    &
    {\phantom{
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    }}
    \hspace{-46pt}
    \mathclap{
      \color{blue}
      \mathbb{Q} \oplus 0
    }
    \hspace{+46pt}
    \;
    \ar[r]
    \ar[d]
    &
    (\widetilde {(H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}}){}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    \ar[r]
    \ar[d]
    &
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n+1}
    \big(
      S^{2(n+d)}
    \big)}}
    \hspace{-35pt}
    \mathclap{
      \color{blue}
      0 \oplus \mathbb{S}_{2d-1}
    }
    \hspace{+35pt}
    \ar[d]
    \ar[r]
    &
    {\phantom{
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n+1}
    \big(
      S^{2(n+d)}
    \big)
    }}
    \hspace{-52pt}
    \mathclap{
      \color{blue}
      0
    }
    \hspace{+52pt}
    \ar[d]
    \\
    \widetilde {\mathbb{S}}{}^{2n}
    \big(
      C_c
    \big)
    \ar[d]
    \ar[r]
    &
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n}
    \big(
      C_c
    \big)
    \;
    \ar[r]
    \ar[d]
    &
    (\widetilde {(H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}}){}^{2n}
    \big(
      C_c
    \big)
    \ar[r]
    \ar[d]
    &
    \widetilde {\mathbb{S}}{}^{2n+1}
    \big(
      C_c
    \big)
    \ar[d]
    \ar[r]
    &
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n+1}
    \big(
      C_c
    \big)
    \\
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n}
    \big(
      S^{2n}
    \big)
    }}
    \hspace{-24pt}
    \mathclap{
      \color{blue}
      0 \oplus \mathbb{Z}
    }
    \hspace{+24pt}
    \ar[d]
      |-{
        \mathclap{\phantom{\vert^\vert}}
        \color{blue}
        c
        \mathclap{\phantom{\vert_\vert}}
      }
    \ar[r]
      |-{
        \color{blue}
        \; 1 \mapsto 1\;
      }
    &
    {\phantom{
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n}
    \big(
      S^{2n}
    \big)
    }}
    \hspace{-37pt}
    \mathclap{
      \color{blue}
      0 \oplus \mathbb{Q}
    }
    \hspace{+37pt}
    \ar[r]
    \ar[d]
    &
    (\widetilde {(H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}}){}^{2n}
    \big(
      S^{2n}
    \big)
    \ar[r]
    &
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n+1}
    \big(
      S^{2n}
    \big)
    }}
    \hspace{-30pt}
    \mathclap{
      \color{blue}
      0
    }
    \hspace{+30pt}
    \\
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n}
    \big(
      S^{2(n+d)-1}
    \big)
    }}
    \hspace{-29pt}
    \mathclap{
      \color{blue}
      0 \oplus \mathbb{S}_{2d-1}
    }
    \hspace{+29pt}
    \ar[r]
    &
    {\phantom{
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n}
    \big(
      S^{2(n+d)-1}
    \big)
    }}
    \hspace{-52pt}
    \mathclap{
      \color{blue}
      0
    }
    \hspace{+52pt}
\end{xymatrix}

Now recognizing [[split exact sequences]] using the vanishing [[Ext]]-groups $Ext^1(-,\mathbb{Q}) = 0$ and $Ext^1(\mathbb{Z},-) = 0$ (see [here](Ext#Examples)) yields:

\begin{xymatrix@=18pt}
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n}
    \big(
      S^{2n+1}
    \big)
    }}
    \hspace{-28pt}
    \mathclap{
     \mathbb{S}_{1} \oplus 0
    }
    \hspace{+28pt}
    \ar[d]
    \ar[r]
    &
    {\phantom{
    \widetilde { (H^{\mathrm{ev}}\mathbb{Q}) }{}^{2n}
    \big(
      S^{2n+1}
    \big)
    }}
    \hspace{-43pt}
    \mathclap{
      0
    }
    \hspace{+43pt}
    \ar[r]
    \ar[d]
    &
    {\phantom{
    (\widetilde {(H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}}){}^{2n}
    \big(
      S^{2n+1}
    \big)
    }}
    \hspace{-53pt}
    \mathclap{
      \color{blue}
      0 \oplus \mathbb{Z}
    }
    \hspace{+53pt}
    \ar[d]
    \ar[r]
    &
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n+1}
    \big(
      S^{2n+1}
    \big)
    }}
    \hspace{-35pt}
    \mathclap{
      0 \oplus \mathbb{Z}
    }
    \hspace{+35pt}
    \ar[d]
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        c
        \mathclap{\phantom{\vert_{\vert}}}
      }
    \\
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    }}
    \hspace{-37pt}
    \mathclap{
      \mathbb{S}_{2d} \oplus 0
    }
    \hspace{+37pt}
    \ar[r]|<<<{ \;0\; }
    \ar[d]
    &
    {\phantom{
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    }}
    \hspace{-46pt}
    \mathclap{
      \mathbb{Q} \oplus 0
    }
    \hspace{+46pt}
    \;
    \ar[r]
    \ar[d]
    &
    {\phantom{
    (\widetilde {(H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}}){}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    }}
    \hspace{-50pt}
    \mathclap{
      \color{blue}
      \mathbb{Q} \oplus \mathbb{S}_{2d-1}
    }
    \hspace{+50pt}
    \ar[r]
    \ar[d]
    &
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n+1}
    \big(
      S^{2(n+d)}
    \big)}}
    \hspace{-35pt}
    \mathclap{
      0 \oplus \mathbb{S}_{2d-1}
    }
    \hspace{+35pt}
    \ar[d]
    \ar[r]
    &
    {\phantom{
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n+1}
    \big(
      S^{2(n+d)}
    \big)
    }}
    \hspace{-52pt}
    \mathclap{
      0
    }
    \hspace{+52pt}
    \ar[d]
    \\
      \color{blue}
      (\mathbb{S}_{2d}/\mathbb{S}_1)
      \oplus
      \mathbb{Z}
    \ar[d]|-{
      \color{blue}
      \mathclap{\phantom{\vert^{\vert}}}
      0 \,\oplus\, \mathrm{ord}(c)
      \mathclap{\phantom{\vert_{\vert}}}
    }
    \ar[r]
    &
    {\phantom{
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n}
    \big(
      C_c
    \big)
    }}
    \hspace{-35pt}
    \mathclap{
      \color{blue}
      \mathbb{Q} \oplus \mathbb{Q}
    }
    \hspace{+35pt}
    \;
    \ar[r]
    \ar[d]
    &
    (\widetilde {(H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}}){}^{2n}
    \big(
      C_c
    \big)
    \ar[r]
    \ar[d]
    &
    \color{blue}
    0 \oplus 
    \mathbb{S}_{2d-1}/\mathbb{Z}
    \ar[d]
    \ar[r]
    &
    {\phantom{
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n+1}
    \big(
      C_c
    \big)
    }}
    \hspace{-41pt}
    \mathclap{
      \color{blue}
      0
    }
    \hspace{+41pt}
    \\
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n}
    \big(
      S^{2n}
    \big)
    }}
    \hspace{-24pt}
    \mathclap{
      0 \oplus \mathbb{Z}
    }
    \hspace{+24pt}
    \ar[d]
      |-{
        \mathclap{\phantom{\vert^\vert}}
        c
        \mathclap{\phantom{\vert_\vert}}
      }
    \ar[r]
      |-{
        \; 1 \mapsto 1\;
      }
    &
    {\phantom{
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n}
    \big(
      S^{2n}
    \big)
    }}
    \hspace{-37pt}
    \mathclap{
      0 \oplus \mathbb{Q}
    }
    \hspace{+37pt}
    \ar[r]
    \ar[d]
    &
    {\phantom{
    (\widetilde {(H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}}){}^{2n}
    \big(
      S^{2n}
    \big)
    }}
    \hspace{-48pt}
    \mathclap{
      \color{blue}
      0 \oplus \mathbb{Q}/\mathbb{Z}
    }
    \hspace{+48pt}
    \ar[r]
    &
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n+1}
    \big(
      S^{2n}
    \big)
    }}
    \hspace{-30pt}
    \mathclap{
      0
    }
    \hspace{+30pt}
    \\
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n}
    \big(
      S^{2(n+d)-1}
    \big)
    }}
    \hspace{-29pt}
    \mathclap{
      0 \oplus \mathbb{S}_{2d-1}
    }
    \hspace{+29pt}
    \ar[r]
    &
    {\phantom{
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n}
    \big(
      S^{2(n+d)-1}
    \big)
    }}
    \hspace{-52pt}
    \mathclap{
      0
    }
    \hspace{+52pt}
\end{xymatrix}

From this, the remaining entry must be
\begin{xymatrix@=18pt}
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n}
    \big(
      S^{2n+1}
    \big)
    }}
    \hspace{-28pt}
    \mathclap{
     \mathbb{S}_{1} \oplus 0
    }
    \hspace{+28pt}
    \ar[d]
    \ar[r]
    &
    {\phantom{
    \widetilde { (H^{\mathrm{ev}}\mathbb{Q}) }{}^{2n}
    \big(
      S^{2n+1}
    \big)
    }}
    \hspace{-43pt}
    \mathclap{
      0
    }
    \hspace{+43pt}
    \ar[r]
    \ar[d]
    &
    {\phantom{
    (\widetilde {(H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}}){}^{2n}
    \big(
      S^{2n+1}
    \big)
    }}
    \hspace{-53pt}
    \mathclap{
      0 \oplus \mathbb{Z}
    }
    \hspace{+53pt}
    \ar[d]
    \ar[r]
    &
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n+1}
    \big(
      S^{2n+1}
    \big)
    }}
    \hspace{-35pt}
    \mathclap{
      0 \oplus \mathbb{Z}
    }
    \hspace{+35pt}
    \ar[d]
      |-{
        \mathclap{\phantom{\vert^{\vert}}}
        c
        \mathclap{\phantom{\vert_{\vert}}}
      }
    \\
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    }}
    \hspace{-37pt}
    \mathclap{
      \mathbb{S}_{2d} \oplus 0
    }
    \hspace{+37pt}
    \ar[r]|<<<{ \;0\; }
    \ar[d]
    &
    {\phantom{
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    }}
    \hspace{-46pt}
    \mathclap{
      \mathbb{Q} \oplus 0
    }
    \hspace{+46pt}
    \;
    \ar[r]
    \ar[d]
    &
    {\phantom{
    (\widetilde {(H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}}){}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    }}
    \hspace{-50pt}
    \mathclap{
      \mathbb{Q} \oplus \mathbb{S}_{2d-1}
    }
    \hspace{+50pt}
    \ar[r]
    \ar[d]
    &
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n+1}
    \big(
      S^{2(n+d)}
    \big)}}
    \hspace{-35pt}
    \mathclap{
      0 \oplus \mathbb{S}_{2d-1}
    }
    \hspace{+35pt}
    \ar[d]
    \ar[r]
    &
    {\phantom{
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n+1}
    \big(
      S^{2(n+d)}
    \big)
    }}
    \hspace{-52pt}
    \mathclap{
      0
    }
    \hspace{+52pt}
    \ar[d]
    \\
      (\mathbb{S}_{2d}/\mathbb{S}_1)
      \oplus
      \mathbb{Z}
    \ar[d]|-{
      \mathclap{\phantom{\vert^{\vert}}}
      0 \,\oplus\, \mathrm{ord}(c)
      \mathclap{\phantom{\vert_{\vert}}}
    }
    \ar[r]
    &
    {\phantom{
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n}
    \big(
      C_c
    \big)
    }}
    \hspace{-35pt}
    \mathclap{
      \mathbb{Q} \oplus \mathbb{Q}
    }
    \hspace{+35pt}
    \;
    \ar[r]
    \ar[d]
    &
      \color{magenta}
      \mathbb{Q}
      \oplus
      \!
      \big(
        \mathbb{Q}/\mathbb{Z}
        \oplus
        \mathbb{S}_{2d-1}/\mathbb{Z}
      \big)
    \ar[r]
    \ar[d]
    &
    0 \oplus
    \mathbb{S}_{2d-1}\!/\mathbb{Z}
    \ar[d]
    \ar[r]
    &
    {\phantom{
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n+1}
    \big(
      C_c
    \big)
    }}
    \hspace{-41pt}
    \mathclap{
      0
    }
    \hspace{+41pt}
    \\
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n}
    \big(
      S^{2n}
    \big)
    }}
    \hspace{-24pt}
    \mathclap{
      0 \oplus \mathbb{Z}
    }
    \hspace{+24pt}
    \ar[d]
      |-{
        \mathclap{\phantom{\vert^\vert}}
        c
        \mathclap{\phantom{\vert_\vert}}
      }
    \ar[r]
      |-{
        \; 1 \mapsto 1\;
      }
    &
    {\phantom{
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n}
    \big(
      S^{2n}
    \big)
    }}
    \hspace{-37pt}
    \mathclap{
      0 \oplus \mathbb{Q}
    }
    \hspace{+37pt}
    \ar[r]
    \ar[d]
    &
    {\phantom{
    (\widetilde {(H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}}){}^{2n}
    \big(
      S^{2n}
    \big)
    }}
    \hspace{-48pt}
    \mathclap{
      0 \oplus \mathbb{Q}/\mathbb{Z}
    }
    \hspace{+48pt}
    \ar[r]
    &
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n+1}
    \big(
      S^{2n}
    \big)
    }}
    \hspace{-30pt}
    \mathclap{
      0
    }
    \hspace{+30pt}
    \\
    {\phantom{
    \widetilde {\mathbb{S}}{}^{2n}
    \big(
      S^{2(n+d)-1}
    \big)
    }}
    \hspace{-29pt}
    \mathclap{
      0 \oplus \mathbb{S}_{2d-1}
    }
    \hspace{+29pt}
    \ar[r]
    &
    {\phantom{
    \widetilde {(H^{\mathrm{ev}}\mathbb{Q})}{}^{2n}
    \big(
      S^{2(n+d)-1}
    \big)
    }}
    \hspace{-52pt}
    \mathclap{
      0
    }
    \hspace{+52pt}
\end{xymatrix}

\end{proof}


\begin{proposition}
  The diagrammatic lifted $\widehat e_{\mathbb{C}}$-invariant from Def. \ref{LiftedEInvariantDiagrammatically}

\begin{xymatrix@=18pt}
   S^{2(n + d)-1}
   \ar[dd]_-{ c }
   \ar[rr]
   \ar@{}[ddrr]|-{
     \rotatebox[origin=c]{-45}{\color{orange}$\big\Downarrow$}
     \mbox{\tiny (po)}
   }
   &&
   \ast
   \ar[dr]
   \ar[dd]
   \\
   && &
   \ast
   \ar[dd]|-{
     \mathclap{\phantom{\vert^{\vert}}}
     0
     \mathclap{\phantom{\vert_{\vert}}}
   }
   \\
   S^{2n}
   \ar[dd]
   \ar[rr]
   \ar@{}[ddrr]|-{
     \rotatebox[origin=c]{-45}{$\big\Downarrow$}
     \mbox{\tiny (po)}
   }
   \ar@/_.7pc/[drrr]
     |<<<<<{ \;\Sigma^{2n} (1^{\mathrm{KU}})\;\; }
     |>>>>>>>>>{ {\phantom{AA}} \atop {\phantom{AA}} }
   &&
   C_c
   \ar[dd]
   \ar@{-->}[dr]^-{
     \color{magenta} V_{2n}
   }
   &&
   \\
   && &
   \mathrm{KU}^{2n}
   \ar[dd]
   \ar[dr]|-{
     \;\mathrm{ch}\;
   }
   \\
   \ast
   \ar@/_.7pc/[drrr]|-{ \;0\; }
   \ar[rr]
   &&
   S^{2(n+d)}
   \ar@{-->}[dr]^-{
   }
   &&
   (H^{\mathrm{ev}}\mathbb{Q})^{2n}
   \ar[dd]
   \\
   && &
   (\mathrm{KU}/\mathbb{S})^{2n}
   \ar[dr]
     |-{
       \; \mathrm{ch}/\mathbb{S} \;
     }
   \\
   && &&
   \big(
     (H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}
   \big)^{2n}
\end{xymatrix}

reproduces the classical $e_{\mathbb{C}}$-invariant.
\end{proposition}
\begin{proof}
By Lemma  \ref{DiagrammaticecInvariantTakesIntegerLattiveValues} the class of this diagram over $[c]$ is a rational number, well-defined modulo integers.

By Lemma \ref{identifyingCofiberRationalCohomoloyOfCofiberSpace} with Prop. \ref{QModZValuedEInvariantIsTopDegreeCoefficientOfChernCharacterOnCofiberSpace}, this number is the Adams $e_{\mathbb{C}}$-invariant.
\end{proof}

\linebreak

### Recovering Conner-Floyd's e-invariant
 {#ConnerFloydTheoremViaPastingDiagram}

With this diagrammatic formulation of the e-invariant, the Conner-Floyd theorem -- that the [[e-invariant is the Todd class of cobounding (U,fr)-manifolds]] -- follows as an immediate corollary: It just amounts to factoring the above pasting composite further through [[MU]], as follows:

\begin{xymatrix@C=15pt}
   S^{2(n + d)-1}
   \ar[dd]_-{ c }
   \ar[rr]
   \ar@{}[ddrr]|-{
     \rotatebox[origin=c]{-45}{\color{orange}$\big\Downarrow$}
     \mbox{\tiny (po)}
   }
   &&
   \ast
   \ar[dr]
   \ar[dd]
   \\
   && &
   \ast
   \ar[dd]|-{
     \mathclap{\phantom{\vert^{\vert}}}
     0
     \mathclap{\phantom{\vert_{\vert}}}
   }
   \\
   S^{2n}
   \ar[dd]
   \ar[rr]
   \ar@{}[ddrr]|-{
     \rotatebox[origin=c]{-45}{\color{orange}$\big\Downarrow$}
     \mbox{\tiny (po)}
   }
   \ar@/_.7pc/[drrr]
     |<<<<<{ \;\Sigma^{2n} (1^{M\mathrm{U}})\;\; }
     |>>>>>>>>>{ {\phantom{AA}} \atop {\phantom{AA}} }
   &&
   C_c
   \ar[dd]
   \ar@{-->}[dr]^-{
   }
   %\ar@/_2pc/[dddrrr]
   %  |>>>>>>>>>>>>>>>{
   %    \mathclap{\phantom{\vert}}
   %    \;{\color{magenta} e(f)}\;
   %  }
   &&
   \\
   && &
   M\mathrm{U}^{2n}
   \ar[dd]
   \ar[dr]|-{
     \;\sigma\;
   }
   \ar@/^1.7pc/[ddrr]|>>>>>>>>>>>{
     \;
     \mathclap{\phantom{\vert^{\vert}}}
     \mathrm{Td}
     \mathclap{\phantom{\vert_{\vert}}}
     \;
   }
   \\
   \ast
   \ar@/_.7pc/[drrr]|-{ \;0\; }
   \ar[rr]
   &&
   S^{2(n+d)}
   \ar@{-->}[dr]|-{
     \;
     \mathclap{\phantom{\vert^{\vert}}}
     \color{magenta}M^{2d}
     \mathclap{\phantom{\vert_{\vert}}}
   }
   &&
   \mathrm{KU}^{2n}
   \ar[dr]|-{
     \;
     \mathrm{ch}
     \;
     \mathclap{\phantom{\vert_{\vert}}}
   }
   \ar[dd]|>>>>>>{ \phantom{\vert_{\vert}} }
   \\
   && &
   (M\mathrm{U}/\mathbb{S})^{2n}
   \ar@/^1.7pc/[ddrr]
     |>>>>>>>>>{
       \mathclap{\phantom{\vert^{\vert}}}
       \;\mathrm{Td}/\mathbb{S}\;
       \mathclap{\phantom{\vert_{\vert}}}
     }
   \ar[dr]|-{ \;\sigma/\mathbb{S}\; }
   &&
   (H^{\mathrm{ev}}\mathbb{Q})^{2n}
   \ar[dd]
   \\
   && &&
   (\mathrm{KU}/\mathbb{S})^{2n}
   \ar[dr]|-{ \;\mathrm{ch}/\mathbb{S}\; }
   \\
   && && &
   \big(
     (H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}
   \big)^{2n}
\end{xymatrix}

using that [[the rational Todd class is the Chern character of the Thom class]] and that this identification is represented by a corresponding factorization of maps of multiplicative cohomology theories, as show (e.g. [Smith 73, Section 1](rational+Todd+class+is+Chern+character+of+Thom+class#Smith73))


\linebreak


## Examples

### Third stable homotopy group of spheres
 {#ThirdStableStem}

+-- {: .num_prop #AdamseRInvariantDetectsThirdStableHomotopyGroupOfSpheres} 
###### Proposition
**([Adams 66, Example 7.17  and p. 46](#Adams66))**

In degree 3, the [[KO]]-theoretic [[e-invariant]] $e_{\mathbb{R}}$ takes the value $\left[\tfrac{1}{24}\right] \in \mathbb{Q}/\mathbb{Z}$ on the [[quaternionic Hopf fibration]] $S^7 \overset{h_{\mathbb{H}}}{\longrightarrow} S^4$  and hence reflects the full [[third stable homotopy group of spheres]]:

$$
  \array{
    \pi^s_3 
      &
      \underoverset{
        \simeq
      }{
        e_{\mathbb{R}}
      }{
        \;\;\longrightarrow\;\;
      } 
      &
    \mathbb{Z}/24 
    & 
    \subset 
    &  
    \mathbb{Q}/\mathbb{Z}
    \\
    [h_{\mathbb{H}}]
    &&\mapsto&&
    \left[\tfrac{1}{24}\right]    
  }
$$

while $e_{\mathbb{C}}$ sees only "half" of it (by [Adams 66, Prop. 7.14](#Adams66)).

=--



## Related concepts

* [[eta-invariant]]

* [[d-invariant]], [[f-invariant]]

* [[Hopf invariant]], [[Hopf invariant one problem]]

* [[J-homomorphism]]

* [[stable homotopy groups of spheres]]


## References

The definition is due to:

* {#Adams66} [[John Adams]], Sections 3,7 of: _On the groups $J(X)$ IV_, Topology 5: 21 (1966) ([pdf](http://math.unice.fr/~cazanave/Gdt/ImJ/J-IV.pdf), <a href="https://doi.org/10.1016/0040-9383(66)90004-8">doi:10.1016/0040-9383(66)90004-8</a>)

  _Correction_, Topology 7 (3): 331 (1968)

Discussion in more general [[Whitehead generalized cohomology theories]]:

* {#Krueger73} Warren M. Krueger, _Generalized Steenrod-Hopf Invariants for Stable Homotopy Theory_, Proceedings of the American Mathematical Society, Vol. 39, No. 3 (Aug., 1973), pp. 609-615 ([jstor:2039603](https://www.jstor.org/stable/2039603))

* Warren M. Krueger, _Relation with the Hopf invariant revisited_, Illinois J. Math.
Volume 24, Issue 2 (1980), 188-191 ([euclid:ijm/1256047713](https://projecteuclid.org/euclid.ijm/1256047713))

and in relation to the [[Adams spectral sequence]]:

* {#Switzer75} [[Robert Switzer]], Section 19.19 in: _Algebraic Topology - Homotopy and Homology_, Grundlehren der Mathematischen Wissenschaften, Vol. 212, Springer, 1975 ([doi:10.1007/978-3-642-61923-6](https://link.springer.com/book/10.1007/978-3-642-61923-6))

and to the [[f-invariant]]:

* {#BL09} Mark Behrens, Gerd Laures, _$\beta$-Family congruences and the $f$-invariant_, Geometry & Topology Monographs 16 (2009) 9–29 ([arXiv:0809.1125](https://arxiv.org/abs/0809.1125), [doi: 10.2140/gtm.2009.16.9](https://msp.org/gtm/2009/16/p002.xhtml))


Interpretation in [[MUFr]] [[bordism theory]]:

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], Section 16 of: _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__, Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))

Interpretation via [[index theory]]:

* [[Michael Atiyah]], [[Vijay Patodi]], [[Isadore Singer]], p. 18 onwards in: _Spectral asymmetry and Riemannian geometry. II_, Volume 78, Issue 3 November 1975 , pp. 405-432 ([doi:10.1017/S0305004100051872](https://doi.org/10.1017/S0305004100051872))





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


