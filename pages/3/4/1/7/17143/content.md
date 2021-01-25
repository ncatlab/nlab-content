
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
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

## Statement

For $E$ a [[homotopy commutative ring spectrum]], there is a [[bijection]] between [[complex oriented cohomology theory|complex orientations]] on $E$ and homotopy ring spectrum homomorphism $MU \longrightarrow E$ from [[MU]].

Hence $MU$ is the universal [[complex oriented cohomology theory]].


(e.g [Lurie 10, lect. 6, theorem 8](#LurieLect6), [Ravenel, chapter 4, lemma 4.1.13](#Ravenel))


## Details


##### Conner-Floyd $E$-Chern classes are $E$-Thom classes
  {#ConnerFloydChernClassesAreThomClasses}

We discuss that for $E$ a [[complex oriented cohomology theory]], the $n$th universal [[Conner-Floyd-Chern class]] $c^E_n$ is in fact a universal [[Thom class]] for rank $n$ [[complex vector bundles]]. On the one hand this says that the choice of a [[complex oriented cohomology theory|complex orientation]] on $E$ indeed universally [[orientation in generalized cohomology|orients]] all [[complex vector bundles]]. On the other hand, we interpret this fact [below](#ComplexOrientationAsRingSpectrumMaps) as the [[unitality]] condition on a [[homomorphism]] of [[homotopy commutative ring spectra]] $M U \to E$ which represent that universal orienation.

+-- {: .num_lemma #SphereBundleBunminus1}
###### Lemma

For $n \in \mathbb{N}$, the [[fiber sequence]] ([prop.](classifying+space#SphereFibrationOverInclusionOfClassifyingSpaces))

$$
  \array{
    S^{2n-1} &\longrightarrow& B U(n-1)
    \\
    && \downarrow
    \\
    && B U(n)
  }
$$

exhibits $B U(n-1)$ as the [[sphere bundle]] of the [[universal vector bundle|universal complex vector bundle]] over $B U(n)$.


=--

+-- {: .proof}
###### Proof

When exhibited by a fibration, here the vertical morphism is equivalently the quotient map

$$
 (E U(n))/U(n-1) \longrightarrow (E U(n))/U(n)
$$

(by the proof of [this prop.](classifying+space#SphereFibrationOverInclusionOfClassifyingSpaces)).

Now the [[universal principal bundle]] $E U(n)$ is ([def.](classifying+space#EOn)) equivalently the colimit 

$$
  E U(n) \simeq \underset{\longrightarrow}{\lim}_k  U(k)/U(k-n)
  \,.
$$

Here each [[Stiefel manifold]]/[[coset spaces]] $U(k)/U(k-n)$ is equivalently the space of (complex) $n$-dimensional subspaces of $\mathbb{C}^k$ that are equipped with an orthonormal (hermitian) [[linear basis]]. The [[universal vector bundle]] 

$$
  E U(n) \underset{U(n)}{\times} \mathbb{C}^n 
    \simeq 
  \underset{\longrightarrow}{\lim}_k  U(k)/U(k-n) \underset{U(n)}{\times} \mathbb{C}^n
$$

has as fiber precisely the linear span of any such choice of basis.


While the quotient $U(k)/(U(n-k)\times U(n))$ (the [[Grassmannian]]) divides out the entire choice of basis, the quotient $U(k)/(U(n-k) \times U(n-1))$ leaves the choice of precisly one unit vector. This is parameterized by the sphere $S^{2n-1}$ which is thereby identified as the [[unit sphere]] in the respective fiber of $E U(n) \underset{U(n)}{\times} \mathbb{C}^n$.

=--

In particular:

+-- {: .num_lemma #UniversalComplexLineBundleThomSpace}
###### Lemma
**([[zero-section into Thom space of universal line bundle is weak equivalence]])

The [[zero-section]] map from the [[classifying space]] $B U(1) \simeq \mathbb{C}P^\infty$ (the infinite [[complex projective space]]) to the [[Thom space]] of the [[universal vector bundle|universal]] [[complex line bundle]] (the [[tautological line bundle]] on infinite [[complex projective space]]) is a [[weak homotopy equivalence]]

$$
  B U(1) 
    \overset{\in W_{cl}}{\longrightarrow}
  M U(1)
   \coloneqq
  Th( E U(1) \underset{U(1)}{\times} \mathbb{C})
  \,.
$$

=--

(e.g. [Adams 74, Part I, Example 2.1](#Adams74))

+-- {: .proof}
###### Proof

Observe that the [[circle group]] $U(1)$ is naturally identified with the [[unit sphere]] in $\mathbb{C}$: $U (1) \simeq S(\mathbb{S})$. Therefore the [[sphere bundle]] of the universal complex line bundle is equivalently the $U(1)$-[[universal principal bundle]]

$$
  \begin{aligned}
    E U(1) \underset{U(1)}{\times} S(\mathbb{C})
    & 
    \;\simeq\;
    E U(1) \underset{U(1)}{\times} U(1)
    \\
    & 
    \;\simeq\; 
    E U(1)
  \end{aligned}
  \,.
$$ 

But the [[universal principal bundle]] is [[contractible topological space|contractible]]

$$
  E U(1) \overset{\in W_{cl}}{\longrightarrow} \ast
  \,.
$$

(Alternatively this is the special case of lemma \ref{SphereBundleBunminus1} for $n = 1$.)


Therefore the [[Thom space]] of the universal complex line bundle is:

$$
  \begin{aligned}
    Th( E U(1) \underset{U(1)}{\times} \mathbb{C} )
    & 
    \;\coloneqq\;
    D( E U(1) \underset{U(1)}{\times} \mathbb{C} )
    /
    S( E U(1) \underset{U(1)}{\times} \mathbb{C} )
    \\
    & 
    \;\overset{\in W_{cl}}{\longrightarrow}\;
    D( E U(1) \underset{U(1)}{\times} \mathbb{C} )
    \\
    & 
    \;\overset{\in W_{cl}}{\longrightarrow}\;
    B U(1)
  \end{aligned}
  \,.
$$

=--



+-- {: .num_lemma #UniversalComplexVectorBundleThomSpace}
###### Lemma

For $E$ a [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology]] theory, the $E$-[[reduced cohomology]] of the [[Thom space]] of the complex [[universal vector bundle]] is equivalently the $E$-[[relative cohomology]] of $B U(n)$ relative $B U(n-1)$:

$$
  \tilde E^\bullet( Th(E U(n) \underset{U(n)}{\times} \mathbb{C}^n ) )
    \;\simeq\;
  E^\bullet( B U(n), B U(n-1))
  \,.
$$

If $E$ is equipped with the structure of a [[complex oriented cohomology theory]] then

$$
  \tilde E^\bullet( Th(E U(n) \underset{U(n)}{\times} \mathbb{C}^n ) )
   \simeq
  c^E_n \cdot (\pi_\bullet(E))[ [ c^E_1, \cdots, c^E_n ] ]
  \,,
$$

where the $c_i$ are the universal $E$-[[Conner-Floyd-Chern classes]].

=--

+-- {: .proof}
###### Proof

Regarding the first statement:

In view of lemma \ref{SphereBundleBunminus1} and using that the disk bundle is homotopy equivalent to the base space we have

$$
  \begin{aligned}
    \tilde E^\bullet( Th(E U(n) \underset{U(n)}{\times} \mathbb{C}^n ) )
    & 
    \;=\;
    E^\bullet( D(E U(n) \underset{U(n)}{\times} \mathbb{C}^n), S(E U(n) 
\underset{U(n)}{\times} \mathbb{C}^n) )
    \\
    & 
    \;\simeq\;
    E^\bullet( B U(n), B U(n-1))
  \end{aligned}
  \,.
$$

Regarding the second statement: the [[Conner-Floyd-Chern classes]] freely generate the $E$-cohomology of $B U(n)$ for all $n$ ([prop.](Conner-Floyd+Chern+class#ConnerFloyedClasses)):

$$
  E^\bullet(B U(n))
  \simeq
  \pi_\bullet(E)[ [ c^E_1, \cdots, c^E_n ] ]
  \,.
$$

and the restriction morphism

$$
  E^\bullet(B U(n))
   \longrightarrow
  E^{\bullet}(B U(n-1))
$$

projects out $c_n^E$. Since this is in particular a surjective map, the [[relative cohomology]] $E^\bullet( B U(n), B U(n-1) )$ is just the [[kernel]] of this map.

=--

+-- {: .num_prop #ThomClassesCFClass}
###### Proposition

Let $E$ be a [[complex oriented cohomology theory]]. Then the $n$th $E$-[[Conner-Floyd-Chern class]]

$$
  c^E_n \in \tilde E(Th( E U(n) \underset{U(n)}{\times} \mathbb{C}^n ))
$$

(using the identification of lemma \ref{UniversalComplexVectorBundleThomSpace}) is a [[Thom class]] in that its restriction to the Thom space of any fiber is a suspension of a unit in $\pi_0(E)$. 

=--

([Lurie 10, lecture 5, prop. 6](#Lurie10))

+-- {: .proof}
###### Proof

Since $B U(n)$ is [[connected topological space|connected]], it is sufficient to check the statement over the base point. Since that fixed fiber is canonically isomorphic to the direct sum of $n$ complex lines, we may equivalently check that the restriction of $c^E_n$ to the pullback of the universal rank $n$ bundle along

$$
  i \colon B U(1)^n \longrightarrow B U(n)
$$

satisfies the required condition. By the [[splitting principle]], that restriction is the product of the $n$-copies of the first $E$-Conner-Floyd-Chern class

$$
  i^\ast c_n \simeq ( (c_1^E)_1 \cdots (c_1^E)_n )
  \,.
$$

Hence it is now sufficient to see that each factor restricts to a unit on the fiber, but that is precisely the condition that $c_1^E$ is a complex orientation of $E$. In fact by def. \ref{StrictComplexOrientation} the restriction is even equal to $1 \in \pi_0(E)$.

=--

##### Complex orientation as ring spectrum maps
 {#ComplexOrientationAsRingSpectrumMaps}

For the present purpose:

+-- {: .num_defn #StrictComplexOrientation}
###### Definition

For $E$ a [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology]] theory, a _[[complex oriented cohomology theory|complex orientation]]_ on $E$ is a choice of element

$$
 c_1^E \in E^2(B U(1))
$$

in the cohomology of the [[classifying space]] $B U(1)$ (given by the infinite [[complex projective space]]) such that its image under the restriction map

$$
  \phi
  \;\colon\;
  \tilde E^2( B U(1) )
    \longrightarrow
  \tilde E^2 (S^2)
    \simeq
  \pi_0(E)
$$

is the unit

$$
  \phi(c_1^E) = 1
  \,.
$$

=--

([Lurie 10, lecture 4, def. 2](#Lurie10))


+-- {: .num_remark}
###### Remark

Often one just requires that $\phi(c_1^E)$ is _a_ [[unit]], i.e. an invertible element. However we are after identifying $c_1^E$ with the degree-2 component $M U(1) \to E_2$ of homtopy ring spectrum morphisms $M U \to E$, and by unitality these necessarily send $S^2 \to M U(1)$ to the unit $\iota_2 \;\colon\; S^2 \to E$ (up to homotopy).

=--

+-- {: .num_lemma #S2SpectrumMapFromComplexOrientation}
###### Lemma

Let $E$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) equipped with a [[complex oriented cohomology theory|complex orientation]] (def. \ref{StrictComplexOrientation}) represented by a map

$$
  c_1^E
  \;\colon\;
  B U(1)
    \longrightarrow
  E_2
  \,.
$$

Write $\{c^E_k\}_{k \in \mathbb{N}}$ for the induced [[Conner-Floyd-Chern classes]]. Then there exists a morphism of $S^2$-[[sequential spectra]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#SequentialTSpectra))

$$
  M U \longrightarrow E
$$

whose component map $M U_{2n} \longrightarrow E_{2n}$ represents $c_n^E$ (under the identification of lemma \ref{UniversalComplexVectorBundleThomSpace}), for all $n \in \mathbb{N}$.

=--

+-- {: .proof}
###### Proof

Consider the standard model of [[MU]] as a sequential $S^2$-spectrum with component spaces the [[Thom spaces]] of the complex [[universal vector bundle]]

$$
  M U_{2n}
    \coloneqq
  Th( E U(n) \underset{U(n)}{\otimes} \mathbb{C}^n)
  \,.
$$

Notice that this is a [[CW-spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#CWSpectrum), [lemma](Thom+space#ThomSpaceCWStructure)).

In order to get a homomorphism of $S^2$-[[sequential spectra]], we need to find representatives $f _{2n} \;\colon\; M U_{2n} \longrightarrow E_{2n}$ of $c^E_n$ (under the identification of lemma \ref{UniversalComplexVectorBundleThomSpace}) such that all the squares

$$
  \array{
    S^2 \wedge M U_{2n}
      &\overset{id \wedge f_{2n}}{\longrightarrow}&
    S^2 \wedge E_{2n}
    \\
    \downarrow
      && 
    \downarrow
    \\
    M U_{2(n+1)}
      &\underset{f_{2(n+1)}}{\longrightarrow}&
    E_{2n+1}
  }
$$

commute strictly (not just up to homotopy). 

To begin with, pick a map

$$
  f_0 \;\colon\; M U_0 \simeq S^0 \longrightarrow E_0
$$

that represents $c_0 = 1$.

Assume then by [[induction]] that maps $f_{2k}$ have been found for $k \leq n$. Observe that we have a homotopy-commuting diagram of the form

$$
  \array{
    S^2 \wedge M U_{2n} 
      &\overset{id \wedge f_{2n}}{\longrightarrow}&
    S^2 \wedge E_{2n}
    \\
    \downarrow
      &\swArrow& 
    \downarrow
    \\
    M U_{2} \wedge M U_{2 n}
      &\overset{c_1 \wedge c_{n}}{\longrightarrow}&
    E_2 \wedge E_{2n}
    \\
    \downarrow
      &\swArrow&
    \downarrow^{\mathrlap{\mu_{2,2n}}}
    \\
    M U_{2(n+1)}
      &\underset{c_{n+1}}{\longrightarrow}&
    E_{2(n+1)}
  }
  \,,
$$

where the maps denoted $c_k$ are any representatives of the Chern classes of the same name, under the identification of lemma \ref{UniversalComplexVectorBundleThomSpace}. Here the homotopy in the top square exhibits the fact that $c_1^E$ is a complex orientation, while the homotopy in the bottom square exhibits the Whitney sum formula for Chern classes ([prop.](Chern+class#WhitneySumChernClasses)).

Now since $M U$ is a [[CW-spectrum]], the total left vertical morphism here is a [[classical model structure on topological spaces|Serre-cofibration]], hence a [[Hurewicz cofibration]], hence satisfies the [[homotopy extension property]]. This means precisely that we may find a map $f_{2n+1} \colon M U_{2(n+1)} \longrightarrow E_{2(n+1)}$ homotopic to the given representative $c_{n+1}$ such that the required square commutes strictly.

=--




+-- {: .num_lemma #HRingSpectrumS2SpectrumMapFromComplexOrientation}
###### Lemma

For $E$ a [[complex oriented cohomology theory|complex oriented]] [[homotopy commutative ring spectrum]], the morphism of spectra

$$
  c \;\colon\; M U \longrightarrow E
$$

that represents the complex orientation by lemma \ref{S2SpectrumMapFromComplexOrientation} is a [[homomorphism]] of [[homotopy commutative ring spectra]].

=--

([Lurie 10, lecture 6, prop. 6](#Lurie10))

+-- {: .proof}
###### Proof

The unitality condition demands that the diagram

$$
  \array{
    \mathbb{S} 
      &\overset{}{\longrightarrow}&
    M U
    \\
    & \searrow & \downarrow^{\mathrlap{c}}
    \\
    && E
  }
$$

commutes in the [[stable homotopy category]] $Ho(Spectra)$. In components this means that 

$$
  \array{
    S^{2n} 
      &\overset{}{\longrightarrow}&
    M U_{2n}
    \\
    & \searrow & \downarrow^{\mathrlap{c_n}}
    \\
    && E_{2n}
  }
$$

commutes up to homotopy, hence that the restriction of $c_n$ to a fiber is the $2n$-fold suspension of the unit of $E_{2n}$. But this is the statement of prop. \ref{ThomClassesCFClass}: the Chern classes are universal Thom classes. 

Hence componentwise all these triangles commute up to some homotopy. Now we invoke the [[Milnor sequence]] for generalized cohomology of spectra ([prop.](lim^1+and+Milnor+sequences#CohomologyOfSpectraMilnorSequence)). Observe that the [[tower]] of abelian groups $n \mapsto E^{n_1}(S^n)$ is actually constant ([[suspension isomorphism]]) hence trivially satisfies the [[Mittag-Leffler condition]] and so a homotopy of morphisms of spectra $\mathbb{S} \to E$ exists as soon as there are componentwise homotopies ([cor.](lim^1+and+Milnor+sequences#WithSomeLefflerTheHomsOfSpectraAreHomotopicIfComponentsAre)).

Next, the respect for the product demands that the square

$$
  \array{
    M U \wedge M U
      &\overset{c \wedge c}{\longrightarrow}&
    E \wedge E
    \\
    \downarrow 
      && 
    \downarrow
    \\
    M U 
      &\underset{c}{\longrightarrow}&
    E
  }
$$

commutes in the [[stable homotopy category]] $Ho(Spectra)$. In order to rephrase this as a condition on the components of the ring spectra, regard this as happening in the [[homotopy category of a model category|homotopy category]] $Ho(OrthSpec(Top_{cg}))_{stable}$ of the [[model structure on orthogonal spectra]], which is [[equivalence of categories|equivalent]] to the [[stable homotopy category]]  ([thm.](Introduction+to+Stable+homotopy+theory+--+1-2#SequentialSpectraQuillenEquivalence)).

Here the derived [[symmetric monoidal smash product of spectra]] is given by [[Day convolution]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#SsymModuleSymmetricSpectra)) and maps out of such a product are equivalently as in the above diagram is equivalent ([cor.](Introduction+to+Stable+homotopy+theory+--+1-2#DayConvolutionViaNaturalIsosInvolvingExternalTensorAndTensor)) to a suitably equivariant collection diagrams of the form

$$
  \array{
    M U_{2 n_1} \wedge M U_{2 n_2}
      &\overset{c_{n_1} \wedge c_{n_2}}{\longrightarrow}&
    E_{2 n_1} \wedge E_{2 n_2}
    \\
    \downarrow 
      &&
    \downarrow
    \\
    M U_{2(n_1 + n_2)}
      &\underset{c_{(n_1 + n_2)}}{\longrightarrow}&
   E_{2 (n_1 + n_2)}
  }
  \,,
$$

where on the left we have the standard pairing operations for $M U$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#OrthogonalComplexThomSpectrum)) and on the right we have the given pairing on $E$.

That this indeed commutes up to homotopy is the Whitney sum formula for Chern classes ([prop.](Chern+class#WhitneySumChernClasses)).

Hence again we have componentwise homotopies. And again the relevant [[Mittag-Leffler condition]] on $n \mapsto E^{n-1}((MU \wedge MU)_n)$-holds, by the nature of the universal [[Conner-Floyd classes]] ([prop.](Conner-Floyd+Chern+class#ConnerFloyedClasses)). Therefore these componentwise homotopies imply the required homotopy of morphisms of spectra ([cor.](lim^1+and+Milnor+sequences#WithSomeLefflerTheHomsOfSpectraAreHomotopicIfComponentsAre)).

=--

+-- {: .num_theorem}
###### Theorem

Let $E$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)). Then the map

$$
  (M U \overset{c}{\longrightarrow} E)
  \;\mapsto\;
  (B U(1) \simeq M U_{2} \overset{c_1}{\longrightarrow} E_2)
$$

which sends a homomorphism $c$ of [[homotopy commutative ring spectra]] to its component map in degree 2, interpreted as a class on $B U(1)$ via lemma \ref{UniversalComplexLineBundleThomSpace}, constitutes a [[bijection]] from homotopy classes of homomorphisms of homotopy commutative ring spectra to complex orientations (def. \ref{StrictComplexOrientation}) on $E$.

=--

([Lurie 10, lecture 6, theorem 8](#Lurie10))

+-- {: .proof}
###### Proof

By lemma \ref{S2SpectrumMapFromComplexOrientation} and lemma \ref{HRingSpectrumS2SpectrumMapFromComplexOrientation} the map is surjective, hence it only remains to show that it is injective.

So let $c, c' \colon M U \to E$ be two morphisms of homotopy commutative ring spectra that have the same restriction, up to homotopy, to $c_1 \simeq c_1'\colon M U_2 \simeq B U(1)$. Since both are homotopy ring spectrum homomophisms, the restriction of their components $c_n, c'_n \colon M U_{2n} \to E_{2 n}$ to $B U(1)^{\wedge^n}$ is a product of $c_1 \simeq c'_1$, hence $c_n$ becomes homotopic to $c_n'$ after this restriction. But by the [[splitting principle]] this restriction is injective on cohomology classes, hence $c_n$ itself ist already homotopic to $c'_n$.

It remains to see that these homotopies may be chosen compatibly such as to form a single homotopy of maps of spectra

$$
  f \;\colon\; M U \wedge I_+ \longrightarrow E 
  \,,
$$

This follows due to the existence of the [[Milnor exact sequence|Milnor]] [[short exact sequence]] of the form

$$
  0 
    \to
  \underset{\longleftarrow}{\lim}^1_n E^{-1}( \Sigma^{-2n} M U_{2n} )
    \longrightarrow
  E^0(M U) 
    \longrightarrow 
  \underset{\longleftarrow}{\lim}_n E^0( \Sigma^{-2n} M U_{2n} )
    \to 
  0
$$

([prop.](lim^1+and+Milnor+sequences#CohomologyOfSpectraMilnorSequence)).

Here the [[Mittag-Leffler condition]] is clearly satisfied (by lemma \ref{UniversalComplexVectorBundleThomSpace} all relevant maps are epimorphisms). Hence the [[lim^1]]-term vanishes, and so by exactness the canonical morphism

$$
  E^0(M U) 
    \overset{\simeq}{\longrightarrow}
  \underset{\longleftarrow}{\lim}_n E^0( \Sigma^{-2n} M U_{2n} )
$$

is an [[isomorphism]]. This says that two homotopy classes of morphisms $M U \to E$ are equal precisely already if all their component morphisms are homotopic (represent the same cohomology class).

=--


##### Universal finite-rank orientation on MΩΩSU(n)


The analogous universal finite-rank complex orientation on [[MΩΩSU(n)]]: [Hopkins 84,  Prop. 1.2.1](MOmegaSUn#Hopkins84).


## Related concepts

* [[zero-section into Thom space of universal line bundle is weak equivalence]]

* [[Lazard's theorem]]

* [[Landweber exact functor theorem]]

* [[Quillen's theorem on MU]]

* [[Landweber-Novikov theorem]]



## References

* {#Adams74} [[Frank Adams]], Part II, lemma 4.6, example 4.7 in: _[[Stable homotopy and generalised homology]]_, 1974

* {#Ravenel} [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_,1986

* {#Kochmann96} [[Stanley Kochmann]], section 4.4 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Lurie10} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010 ([web](http://www.math.harvard.edu/~lurie/252x.html)), Lecture 6 _MU and complex orientations_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture6.pdf))

[[!redirects MU and complex orientation]]

[[!redirects complex orientation and MU]]
[[!redirects complex orientations and MU]]

[[!redirects universal complex orientation of MU]]
[[!redirects MU and complex orientations]]
