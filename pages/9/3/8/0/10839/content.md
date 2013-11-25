
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### &#201;tale morphisms
+--{: .hide}
[[!include etale morphisms - contents]]
=--
=--
=--

This page goes through some basics of [[étale cohomology]].

#Contents#
* table of contents
{:toc}


## &#201;tale topos

### &#201;tale morphisms

Of the many equivalent characterizations of [[étale morphisms]], here we will have use of the following incarnation

+-- {: .num_defn }
###### Definition

A morphisms of [[schemes]] is an _[[étale morphism of schemes]]_ if it is

1. [[formally étale morphism of schemes|formally étale]] -- defined in a [moment](#ExplicitDefinition);

1. [[locally of finite presentation]].

=--

+-- {: .num_remark }
###### Remark

The first condition makes an [[étale morphism of schemes]] be like an [[étale space]] over its [[codomain]]. The second essentially just says demands this has [[finite set|finite]] [[fibers]].

=--

The definition of [[formally étale morphisms of schemes|formally étale]] in components goes like this.

+-- {: .num_defn #ExplicitDefinition}
###### Definition

A [[morphism]] of [[commutative rings]] $R \hookrightarrow A$
is called _[[formally étale morphisms of schemes|formally étale]]_ if for every ring $B$ and for every [[nilpotent ideal]] $I \subset B$ and for every [[commuting diagram]] of the form

$$
  \array{
    B/I &\leftarrow& A
    \\
    \uparrow && \uparrow
    \\
    B &\leftarrow& R
  }
$$

there is a unique diagonal morphism

$$
  \array{
    B/I &\leftarrow& A
    \\
    \uparrow &\swarrow& \uparrow
    \\
    B &\leftarrow& R
  }
$$

that makes both triangles commute.

=--

(e.g. [Stacks Project 57.9, 57.12](#StackProject))

By [[Isbell duality|formal duality]] and [[sheafification|locality]] this yields a notion of formally &#233;tale morphisms of [[affine varieties]] and of [[schemes]].

It is useful to realize this equivalently but a bit more naturally as follows.


+-- {: .num_defn #ReductionOnRings}
###### Definition

Write

$$
  Red \;\colon\; CRing \longrightarrow CRing
$$

for the [[functor]] which sends a [[commutative ring]] $R$ to its [[reduced scheme|reduced ring]] $R/I$, where $I$ is the [[nilradical]] (the maximal [[nilpotent ideal]] if $R$ is finitely presented). 
=--

+-- {: .num_prop #DifferentialCohesionModality}
###### Proposition

There is an [[adjoint triple]] of [[idempotent monad|idempotent]] [[comonad|co]]-[[monads]]

$$
  (Red \dashv \int_{inf} \dashv \flat_{inf}) \;\colon\; Sh(CRing) \longrightarrow Sh(CRing)
$$

where the [[left adjoint]] [[comonad]] $Red$ is given on [[representable functor|representables]] by the [[reduced scheme|reduction]] functor of def. \ref{ReductionOnRings}.

=--

+-- {: .num_remark }
###### Remark

Here $\int_{inf}$ sends a [[scheme]] to its [[de Rham space]].

=--

+-- {: .num_prop }
###### Proposition

A morphism $f \;\colon\; Spec A \to Spec R$ in $CRing^{op} \hookrightarrow Sh(CRing)$ is 
formally &#233;tale, def. \ref{ExplicitDefinition}, precisely if it is $\int_{inf}$-[[modal type|modal]] relative $Spec R$, hence if the [[natural transformation|naturality square]] of the [[infinitesimal shape modality]]-[[unit of a monad|unit]] 

$$
  \array{
    Spec A &\longrightarrow& \int_{inf} Spec A
    \\
    \downarrow && \downarrow
    \\
    Spec R &\longrightarrow& \int_{inf} Spec R
  }
$$

is a [[pullback]] square.

=--

+-- {: .proof}
###### Proof

Evaluated on $B \in CRing$ any object, by the [[Yoneda lemma]] and the $(Red \dashv \int_{inf})$-[[adjunction]], the naturality square becomes

$$
  \array{
    CRing(A,B) &\longrightarrow& CRing(A,B/I)
    \\
    \downarrow && \downarrow
    \\
    CRing(R,B) &\longrightarrow& CRing(R,B/I)
  }
  \,.
$$

in [[Set]]. Chasing elements through this shows that this is a [[pullback]] precisely if the condition in def. \ref{ExplicitDefinition} holds.

=--

We repeatedly use the following example of &#233;tale morphisms.

+-- {: .num_prop #OpenImmersionIsEtale}
###### Proposition

Every [[open immersion of schemes]] is an [[étale morphism of schemes]].
In particular a standard open inclusion (a [[cover]] in the [[Zariski topology]]) induced by the [[localization of a commutative ring]]

$$
  Spec(R[S^{-1}]) \longrightarrow Spec(R)
$$

is &#233;tale.

=--

(e.g. [[The Stacks Project|Stacks Project, lemma 28.37.9]])

+-- {: .proof}
###### Proof

By one of the equivalent characterizations of [[étale morphism]] it is sufficient to check that the map $Spec(R[S^{-1}]) \longrightarrow Spec(R)$ is a [[formally étale morphism]] and [[locally of finite presentation]].

The latter is clear, since the very definition of 

$$
  R[S^{-1}] = R[s_1^{-1}, \cdots, s_n^{-1}](s_1 s_1^{-1} - 1, \cdots , s_n s_n^{-1} - 1)
$$ 

exhibits a [[finitely presented algebra]] over $R$.

To see that it is formally &#233;tale we need to check that for every [[commutative ring]] $T$ with [[nilpotent ideal]] $J$ we have a [[pullback]] diagram

$$
  \array{
    Hom(R[S^{-1}], T) &\longrightarrow& Hom(R[S^{-1}],T/J)
    \\
    \downarrow && \downarrow
    \\
    Hom(R, T) &\longrightarrow& Hom(R, T/J)
  }
  \,.
$$

Now by the [[universal property]] of the [[localization of a commutative ring|localization]], a homomorphism $R[S^{-1}] \longrightarrow T$ is a homomorphism $R \longrightarrow T$ which sends all elements in $S \hookrightarrow R$ to invertible elements in $T$. But no element in a [[nilpotent ideal]] can be invertible, Therefore the fiber product of the bottom and right map is the set of maps from $R$ to $T$ such that $S$ is taken to invertibles, which is indeed the top left set.


=--




### Sheaf condition and examples of &#233;tale sheaves
 {#SheafConditionAndExamples}

+-- {: .num_defn #EtaleSite}
###### Definition

For $X$ a [[scheme]], its [[étale site]] has a [[objects]] the [[étale morphisms of schemes]] into $X$, as [[morphisms]] the morphisms of schemes [[over category|over]] $X$, and as [[coverings]] the jointly surjective [[étale morphisms of schemes|étale morphisms]] over $X$.

=--

+-- {: .num_prop #EtaleDescentDetectedOnOpenImmersionCovers}
###### Proposition

For $X$ a [[scheme]], and $A \in PSh(X_{et})$ a [[presheaf]] on its [[étale site]], def. \ref{EtaleSite},
for checking the [[sheaf]] condition it is sufficient to 
check [[descent]] on the following two kinds of [[covers]] 
in the [[étale site]]

1. jointly surjective collections of [[open immersions of schemes]];

1. single surjective/[[étale morphism of schemes|étale]] morphisms between [[affine schemes]]

(all over $X$).

=--

([Tamme, II Lemma (3.1.1)](#Tamme), [Milne, prop. 6.6](#Milne))

+-- {: .proof}
###### Proof (sketch)

Since [[covers]] by standard [[open immersions of schemes]] in the [[Zariski topology]] are also [[étale morphisms of schemes]] and &#233;tale covers, we may take any &#233;tale cover $\{Y_i \to Y\}$ over $X$, find an Zariski cover $\{U_i \to X\}$ of $X$, pull back the original cover to that and in turn cover the pullbacks themselves by Zariski covers. The result is still a cover and is so by a collection of [[open immersions of schemes]].
Now using compactness assumptions we find finite subcovers of all these covers. This makes their [[disjoint union]] be a single morphisms of affines.

=--


+-- {: .num_prop #XSchemesRepresentSheaves}
###### Proposition

For $Z \to X$ any [[scheme]] over a [[scheme]] $X$, the induced [[presheaf]] on the [[étale site]]

$$
  (U_Y \to X) \mapsto Hom_X(U_Y, Z)
$$

is a [[sheaf]].

=--

This is due to ([[Grothendieck]], [[SGA]]1 exp. XIII 5.3) A review is in ([Tamme, II theorem (3.1.2)](#Tamme), [Milne, 6.2](#Milne)).

+-- {: .proof}
###### Proof 

By prop. \ref{EtaleDescentDetectedOnOpenImmersionCovers} we are reduced to
showing that the represented presheaf satisfies [[descent]] along collections of open immersions and along surjective maps of affines. For the first this is clear (it is [[Zariski topology]]-descent). For the second case of a [[faithfully flat]] cover of affines $Spec(B) \to Spec(A)$ it follows with the exactness of the corresponding [[Amitsur complex]], see [below](#DescentTheorem) for details.

=--

+-- {: .num_remark}
###### Remark

This map from $X$-schemes to sheaves on $X_{et}$ is not injective, different $X$-schemes may represent the same sheaf on $X_{et}$.
Unique representatives are given by [[étale morphism of schemes|étale schemess]] over $X$.

=--

(e.g. [Tamme, II theorem 3.1](#Tamme))

We consider some examples of [[sheaves of abelian groups]]
induced by prop. \ref{XSchemesRepresentSheaves} from  [[group schemes]]
over $X$.


+-- {: .num_example}
###### Example

The [[additive group]] over $X$ is the [[group scheme]]

$$
  \mathbb{G}_a  \coloneqq Spec(\mathbb{Z}[t]) \times_{Spec(\mathbb{Z})} X
  \,.
$$

By the [[universal property]] of the [[pullback]], the corresponding sheaf $(\mathbb{G}_a)_X$ is given by the assignment

$$
  \begin{aligned}
     (\mathbb{G}_a)_X(U_X \to X) & =
     Hom_X(U_X, Spec(\mathbb{Z}[t]) \times_{Spec(\mathbb{Z})} X)
     \\
     & = 
     Hom(U_X, Spec(\mathbb{Z}[t]))  
     \\
     & = 
     Hom(\mathbb{Z}[t], \Gamma(U_X, \mathcal{O}_{U_X}))
     \\ 
     & = \Gamma(U_X, \mathcal{O}_{U_X})
  \end{aligned}
  \,.
$$

In other words, the sheaf represented by the [[additive group]] is the [[abelian sheaf]] underlying the [[structure sheaf]] of $X$.

=--

Similarly one finds

+-- {: .num_example}
###### Example

The [[multiplicative group]] over $X$

$$
  \mathbb{G}_m \coloneqq Spec(\mathbb{Z}[t,t^{-1}]) \times_{Spec(\mathbb{Z})} X
$$

represents the sheaf $(\mathbb{G}_m)_X$ given by 

$$
  (\mathbb{G}_m)_X(U_X)
  \mapsto
  \Gamma(U_X, \mathcal{O}_{U_X})^\times
  \,.
$$

=--

(e.g. [Tamme, II, 3](#Tamme))


### Base change and sheaf cohomology
 {#BaseChange}

+-- {: .num_defn #BaseChangeOnSites}
###### Definition

For $f \colon X \longrightarrow Y$ a [[homomorphism]] of [[schemes]], there is induced a [[functor]] on the [[categories]] underlying the [[étale site]]

$$
  f^{-1} \;\colon\; Y_{et} \longrightarrow X_{et}
$$

given by sending an [[object]] $U_Y \to Y$ to the [[fiber product]]/[[pullback]] along $f$

$$
  f^{-1} \colon (U_Y \to Y) \mapsto (X \times_Y U_Y \to X)
  \,. 
$$

=--

+-- {: .num_prop #DirectAndInverseImageAlongMapOfBases}
###### Proposition

The morphism in def. \ref{BaseChangeOnSites} is a [[morphism of sites]]
and hence induces a [[geometric morphism]] between the &#233;tale toposes

$$
  (f^\ast \dashv f_\ast)
  \;\colon\;
  Sh(X_{et})
  \stackrel{\overset{f^\ast}{\leftarrow}}{\underset{f_\ast}{\longrightarrow}}
  Sh(Y_{et})
  \,.
$$

Here the [[direct image]] is given on a [[sheaf]] $\mathcal{F} \in Sh(X_{et})$ by

$$
  f_\ast \mathcal{F} \;\colon\;  (U_Y \to Y) \mapsto \mathcal{F}(f^{-1}(U_Y)) = \mathcal{F}(X \times_X U_Y)
$$

while the [[inverse image]] is given on a [[sheaf]] $\mathcal{F} \in Sh_(Y_{et})$ by

$$
  f^\ast \mathcal{F} \;\colon\; (U_X \to X) \mapsto \underset{\underset{U_X \to f^{-1}(U_Y)}{\longrightarrow}}{\lim} \mathcal{F}(U_Y)
  \,.
$$


=--

By the discussion at _[morphisms of sites -- Relation to geometric morphisms](morphism+of+sites#RelationToGeometricMorphisms)_.
See also for instance ([Tamme I 1.4](#Tamme)).



+-- {: .num_prop #DerivedDirectImageByCohomology}
###### Proposition

The $q$th [[derived functor]] $R^q f_\ast$ of the [[direct image]] functor of def. \ref{DirectAndInverseImageAlongMapOfBases} sends $\mathcal{F} \in Ab(Sh(X_{et}))$ to the [[sheafification]] of the [[presheaf]]

$$
  (U_Y \to Y)
  \mapsto
  H^q(X \times_Y U_Y, \mathcal{F})
  \,,
$$

where on the right we have the degree $q$ [[abelian sheaf cohomology]] [[cohomology group|group]] with [[coefficients]] in the given $\mathcal{F}$ ([[étale cohomology]]).


=--

(e.g. [Tamme, I (3.7.1), II (1.3.4)](#Tamme), [Milne, 12.1](#Milne)).


+-- {: .proof}
###### Proof

We have a [[commuting diagram]]

$$
  \array{
    Ab(PSh(X)) &\stackrel{(-)\circ f^{-1}}{\longrightarrow}& Ab(PSh(Y))
    \\
    \uparrow^{\mathrlap{inc}} && \downarrow^{L}
    \\
    Ab(Sh(X)) &\stackrel{f_\ast}{\longrightarrow}& Ab(Sh(Y))
  }
  \,,
$$

where the right vertical morphism is [[sheafification]]. Because $(-) \circ f^{-1}$ and $L$ are both [[exact functors]] it follows that for $I^\bullet \to \mathcal{F}$ an [[injective resolution]] that

$$
  \begin{aligned}
     R^p f_\ast(\mathcal{F})
     & :\simeq
     H^p( f_\ast I)
     \\
     & = H^p(L I^\bullet(f^{-1}(-)))
     \\
     & = L (H^p(I^\bullet)(f^{-1}(-)))
  \end{aligned}
$$

=--



+-- {: .num_remark}
###### Remark

For $O_X \stackrel{f^{-1}}{\leftarrow} O_Y \stackrel{g^{-1}}{\leftarrow} O_Z$
two composable [[morphisms of sites]], 
the [[Leray spectral sequence]] for the corresponding [[direct images]] exists and is of the form

$$
  E^{p,q}_2 = R^p f_\ast(R^q g_\ast(\mathcal{F}))
  \Rightarrow
  E^{p+q} = R^{p+q}(g f)_\ast(\mathcal{F})
  \,.
$$ 


For the special case that $S_Z = \ast$ and $g^{-1}$ includes an [[étale morphism of schemes|étale morphism]] $U_Y \to Y$ this yields

$$
  E^{p,q}_2 = H^p(U_Y, R^q f_\ast \mathcal{F})
  \Rightarrow
  E^{p+q} = H^{p+q}(U_Y \times_Y X , \mathcal{F})
  \,.
$$


=--


## &#201;tale cohomology



### With coefficients in coherent modules
 {#WithCoefficientsInCoherentModules}


+-- {: .num_prop }
###### Proposition


For $X$ a [[scheme]] and $N$ a [[quasicoherent module]] over its [[structure sheaf]] $\mathcal{O}_X$, then this induces an [[abelian sheaf]] on the [[étale site]] by

$$
  N_{et} \;\colon\; (U_X \to X) 
   \mapsto 
  \Gamma(U_Y, N \otimes_{\mathcal{O}_X} \mathcal{O}_{U_X})
  \,.
$$

=--

(e.g. [Tamme, II 3.2.1](#Tamme))


+-- {: .num_remark }
###### Remark

A [[cover]] in the [[Zariski topology]] on [[schemes]] is an [[open immersion of schemes]] and hence is in particular an [[étale morphism of schemes]]. Hence the [[étale site]] is finer than the [[Zariski site]] and so every &#233;tale [[sheaf]] is a Zarsiki sheaf, but not necessarily conversely. 

=--



+-- {: .num_remark #LerayForInclusionOfZariskiIntoEtale}
###### Remark

For $X$ a [[scheme]], the inclusion

$$
  \epsilon \;\colon\; X_{Zar} \longrightarrow X_{et}
$$

of the [[Zariski site]] into the [[étale site]] is indeed a [[morphism of sites]]. Hence there is a [[Leray spectral sequence]] which computes &#233;tale cohomology in terms of Zarsiki cohomology 

$$
  E^{p,q}_2 = H^p(X_{Zar}, R^q \epsilon^\ast \mathcal{F})
  \Rightarrow
  E^{p+q} = H^{p+q}(X_{et}, \mathcal{F})
  \,.
$$

=--

This is originally due to ([[Grothendieck]], [[SGA]] 4 (Chapter VII, p355)). Reviews include ([Tamme, II 1.3](#Tamme)).


+-- {: .num_prop #CohomologyWithCoeffsInCoherentModules}
###### Proposition

For $N$ a [[quasi-coherent sheaf]] of $\mathcal{O}_X$-[[modules]] and $N_{et}$ the induced &#233;tale sheaf (by the discussion at [&#233;tale topos -- Quasicohetent sheaves](etale+topos#QuasiCoherentModules)),
then the [[edge morphism]]

$$
  H^p_{Zar}(X, N)
  \longrightarrow
  H^p_{et}(X,N_{et})
$$

of the [[Leray spectral sequence]] of remark \ref{LerayForInclusionOfZariskiIntoEtale} is an  [[isomorphism]] for all $p$, itentifying the [[abelian sheaf cohomology]] on the [[Zariski site]] with [[coefficients]] in $N$ with the &#233;tale cohomology with coefficients in $N_{et}$.

Moreover, for $X$ affine we have

$$
  H^p_{et}(X, N_{et}) \simeq 0
  \,.
$$


=--

This is due to ([[Grothendieck]], [[FGA]] 1). See also for instance ([Tamme, II (4.1.2)](#Tamme)).

+-- {: .proof}
###### Proof

By the discussion at _[[edge morphism]]_ it suffices to show that 

$$
  R^q \epsilon_\ast (N) = 0 \;\,,\;\;\; for \;\; p \gt 0
  \,.
$$

By prop \ref{DerivedDirectImageByCohomology}, $R^q \epsilon_\ast N$ is the [[sheaf]] on the [[Zariski topology]] which is the [[sheafification]] of the [[presheaf]] given by

$$
  U \mapsto H^q(X_{et}|U, N)
  \,,
$$

hence it is sufficient that this vanishes, or rather, by locality ([[sheafification]]) it suffices to show this vanishes for $X = U = Spec(A)$ an affine [[algebraic variety]].

By the existence of [cofinal affine &#233;tale covers](etale+site#CofinalAffineCovers) the [[full subcategory]] $X_{et}^{a} \hookrightarrow X_{at}$ with the induced [[coverage]] is a [[dense subsite]] of affines. Therefore it suffices to show the statement there. 
Moreover, by the finiteness condition on [[étale morphisms]]  every cover of $X_{et}^{a}$ may be refined by a finite cover, hence by an affine covering map 

$$
  Spec(B) \longrightarrow Spec(A)
  \,.
$$

It follows (by a discussion such as e.g. at [[Sweedler coring]]) that the corresponding [[Cech cohomology]] complex

$$
  N_{et}(Spec(A)) \to C^0(\{Spec(B) \to Spec(A)\}, N_{et}) \to C^1(\{Spec(B) \to Spec(A)\}, N_{et}) \to \cdots
$$

is of the form

$$
  0 \to N \to N \otimes_A B \to N \otimes_{A} B \otimes_A B \to \cdots
  \,.
$$

known as the _[[Amitsur complex]]_ of $A \to B$, tensored with $N$.

Since $A \to B$ is a [[faithfully flat morphism]], it follows by the [[descent theorem]] (reviewed [below](#DescentTheorem)) that this is [[exact sequence|exact]], hence that the cohomology indeed vanishes.


=--

### With coefficients in a cyclic group
 {#WithCoefficientsInACyclicGroup}

Let $X$ be a [[reduced scheme|reduced]] [[scheme]] of [[characteristic]] the [[prime number]] $p$, hence such that for all points $x \in X$

$$
  p \cdot \mathcal{O}_{X,x} = 0
  \,.
$$

Write

$$
  F - id \coloneqq (-)^p - (-) \;\colon\; (\mathbb{G}_a)_X \longrightarrow (\mathbb{G}_a)_X
$$

for the [[endomorphism]] of the [[additive group]] over the [[étale site]] $X_{et}$ of $X$ (the [[structure sheaf]] regarded as just a [[sheaf of abelian groups]]) which is the [[Frobenius endomorphism]] $F(-) \coloneqq (-)^p$ minus the identity.

+-- {: .num_prop}
###### Proposition

There is a [[short exact sequence]] of [[abelian sheaves]] over the [[étale site]]

$$
  0 \to (\mathbb{Z}/p\mathbb{Z})_X \to (\mathbb{G}_a)_X \stackrel{F-id}{\to} (\mathbb{G}_a)_X \to 0
  \,.
$$


=--

This is called the _[[Artin-Schreier sequence]]_ (e.g. [Tamme, section II 4.2](#Tamme), [Milne, example 7.9](#Milne)).


+-- {: .proof}
###### Proof

By the discussion at [category of sheaves -- Epi-/Mono-morphisms](category+of+sheaves#EpiMonoIsomorphisms) we need to show that the left morphism is an injection over any [[étale morphism]] $U_Y \to X$, and that for every element $s \in \mathcal{O}_X$ there exists an [[étale site]] [[covering]] $\{U_i \to X\}$ such that $(-)^p- (-)$ restricts on this to a morphism which hits the restriction of that element.

The first statement is clear, since $s = s^p$ says that $s$ is a constant section, hence in the image of the [[constant sheaf]]
$\mathbb{Z}/p\mathbb{Z}$  and hence for each connected $U_Y \to X$ the left morphism is the inclusion

$$
  \mathbb{Z}/p\mathbb{Z} \hookrightarrow \mathcal{O}_{X'}
$$ 

induced by including the unit [[section]] $e_{X'}$ and its multiples $r e_{X'}$ for $0 \leq r \lt p$. (This uses the "[[freshman's dream]]"-fact that in [[characteristic]] $p$ we have $(a + b)^p = a^p + b^p$).

This is injective by assumption that $X$ is of characteristic $p$.

To show that $(-)^p - (-)$ is an epimorphism of sheaves, it is sufficient to find for each element $s \in \mathcal{O}_X = A$ an [[étale site|étale cover]] $Spec(B) \to Spec(A)$ such that its restriction along this cover is in the image of $(-)^p - (-) \colon B \to B$. The choice

$$
  B \coloneqq A[t]/(t- t^p - s)
$$

by construction has the desired property concerning $s$, the preimage of $s$ is the equivalence class of $t$. 

To see that with this choice $Spec(B) \to Spec(A)$ is indeed an [[étale morphism of schemes]] it is sufficient to observe that it is a [[morphism of finite presentation]] and a [[formally étale morphism]]. The first is true by construction. For the second observe that for a ring homomorphism $B \to T$ the generator $t$ cannot go to a nilpotent element since otherwise $s$ would have to be nilpotent. This implies [[formally étale morphism|formal étaleness]] analogous to  the discussion at [&#233;tale morphism of schemes -- Open immersion is Etale](etale+morphism+of+schemes#OpenImmersionIsEtale).



=--



+-- {: .num_prop}
###### Proposition

If $X = Spec(A)$ is an affine [[reduced scheme]] of [[characteristic]] a [[prime number]] $p$, then its [[étale cohomology]] with [[coefficients]] in $\mathbb{Z}/p\mathbb{Z}$ is

$$
  H^q(X, (\mathbb{Z}/p\mathbb{Z})_X)
  \simeq
  \left\{
    \array{
      A/(F - id)A & if\; q = 1
      \\
      0 & if \; q \gt 0
    }
  \right.
  \,.
$$


=--

+-- {: .proof}
###### Proof

Under the given assumptions, the [[Artin-Schreier sequence]] (see there) induces a [[long exact sequence in cohomology]] of the form

$$
  \begin{aligned}
    0 & \to 
    H^0(X_{et}, \mathbb{Z}/p\mathbb{Z}) \to H^0(X_{et}, \mathcal{O}_X) \stackrel{F-id}{\to} H^0(X_{et}, \mathcal{O}_X)
   \\
    & \to
     H^1(X_{et}, \mathbb{Z}/p\mathbb{Z}) \to H^1(X_{et}, \mathcal{O}_X) \stackrel{F-id}{\to} H^1(X_{et}, \mathcal{O}_X)
   \\
    & \to
     H^2(X_{et}, \mathbb{Z}/p\mathbb{Z}) \to H^2(X_{et}, \mathcal{O}_X) \stackrel{F-id}{\to} H^2(X_{et}, \mathcal{O}_X) \to \cdots
  \end{aligned}
  \,,
$$

where $F(-) = (-)^p$ is the [[Frobenius endomorphism]]. 
By prop. \ref{CohomologyWithCoeffsInCoherentModules}
the terms of the form $H^{p \geq 1}(X, \mathcal{O}_X)$ vanish,
and so from [[exact sequence|exactness]] we find an [[isomorphism]]

$$
  H^0(X_{et}, \mathcal{O}_X)/(F-id)(H^0(X_{et}, \mathcal{O}_X))
    \stackrel{\simeq}{\to}
  H^1(X_{et}, \mathbb{Z}/p\mathbb{Z})
  \,,
$$

hence the claimed isomorphism

$$
  A/(F-id)(A)
    \stackrel{\simeq}{\to}
  H^1(X_{et}, \mathbb{Z}/p\mathbb{Z})
  \,.
$$

By the same argument all the higher cohomology groups vanish, as claimed.


=--

### With coefficients in the multiplicative group

the &#233;tale cohomology groups with [[coefficients]] in the [[multiplicative group]] $\mathbb{G}_m$ in the first few degrees go by special names:

* $H^0_{et}(-, \mathbb{G}_m)$: [[group of units]];

* $H^1_{et}(-, \mathbb{G}_m)$: [[Picard group]] ([[Hilbert's theorem 90]], [Tamme, II 4.3.1](#Tamme));

* $H^2_{et}(-, \mathbb{G}_m)$: [[Brauer group]];



## Outlook: Then main theorems
 {#MainTheorems}


* [[proper base change theorem]]

([Milne, section 17](#Milne))

* [[comparison theorem (étale cohomology)]]

([Milne, section 21](#Milne))

* [[Künneth formula]]

([Milne, section 22](#Milne))

* cycle map

([Milne, section 23](#Milne))

* [[Poincaré duality]]

([Milne, section 24](#Milne))


[K&#252;nneth formula](#K&#252;nnethFormula) + [cycle map](#CycleMap) + [Poincar&#233; duality](#PoincareDuality) $\Rightarrow$ [[Lefschetz fixed-point formula]]
 
([Milne, section 25](#Milne))

## Appendix

### Descent theorem
 {#DescentTheorem}

+-- {: .num_defn }
###### Definition

Given a [[commutative ring]] $R$ and an $R$-[[associative algebra]] $A$, hence a [[ring]] [[homomorphism]] $f \colon R \longrightarrow A$, the _[[Amitsur complex]]_ is the [[Moore complex]] of the dual [[Cech nerve]] of $Spec(A) \to Spec(R)$, hence the [[chain complex]]

$$
  0 \to R \stackrel{f}{\to} A \stackrel{1 \otimes id - id \otimes 1}{\longrightarrow} A \otimes_R A \to A \otimes_R A \otimes_R A \to \cdots
  \,.
$$

=--

(See also at _[[Sweedler coring]]_ and at _[[commutative Hopf algebroid]]_ for the same or similar constructions.)

+-- {: .num_theorem }
###### Theorem
**(descent theorem)**

If $A \to B$ is [[faithfully flat]] then its Amitsur complex is [[exact sequence|exact]].

=--

This is due to ([[Grothendieck]], [[FGA]]1)

The following reproduces the proof in low degree from [Milne, prop. 6.8](#Milne).

+-- {: .proof}
###### Proof 

We show that 

$$
  0 \to A \stackrel{f}{\longrightarrow} B \stackrel{1 \otimes id - id \otimes 1}{\longrightarrow} B \otimes_A B
$$ 

is an [[exact sequence]] if $f \colon A \longrightarrow B$ is [[faithfully flat]].

First observe that the statement follows if $A \to B$ admits a [[section]] $s \colon B \to A$. Because then we can define a map 

$$
  k \colon B \otimes_A B \longrightarrow B
$$

$$
  k \;\colon\; b_1 \otimes b_2 \mapsto b \cdot f(s(b)) - b
  \,.
$$

This is such that applied to a coboundary it yields

$$
  k(1 \otimes b - b \otimes 1) = f(s(b)) - b 
$$

and hence it exhibits every cocycle $b$ as a coboundary $b = f(s(b))$.

So the statement is true for the special morphism 

$$
  B \to B \otimes_A B
$$

$$
  b \mapsto b \otimes 1
$$

because that has a section given by the multiplication map. 

But now observe that the morphism $B \to B \otimes_A B$ is the [[tensor product]] of the morphism $f$ with $B$ over $A$. That $A \to B$ is [[faithfully flat]] by assumption, hence that it exhibits $B$ as a [[faithfully flat module]] over $A$ means by definition that the Amitsur complex for $(A \to B)\otimes_A B$ is exact precisely if that for $A \to B$ is exact.

=--



### Leray spectral sequence

* [[Leray spectral sequence]]


## References

* [[Günter Tamme]], _[[Introduction to Étale Cohomology]]_
 {#Tamme}

* [[James Milne]], _[[Lectures on Étale Cohomology]]_
 {#Milne}


[[!redirects basics of étale cohomology]]

