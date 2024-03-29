[[!redirects etale topos]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### &#201;tale morphisms
+--{: .hide}
[[!include etale morphisms - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

In the context of the [[geometry]] of [[schemes]] there is a traditional notion of [[étale morphism of schemes]] and an _&#233;tale topos_ is a [[category of sheaves]] on the [[étale site]] of a [[scheme]], consisting of [[covers]] by such [[étale morphism of schemes|étale morphisms]]. This traditional notion we discuss in 

* [&#201;tale topos of a scheme](#EtaleToposOfAScheme).

More abstractly, given that [[étale morphisms of schemes]] may be characterized as modal morphisms with respect to an [[infinitesimal shape modality]], one can consider &#233;tale toposes in every context of [[differential cohesion]]. This we discuss in 

* [&#201;tale topos of a differentially cohesive object](#GeneralAbstract)

### &#201;tale topos of a scheme
 {#EtaleToposOfAScheme}

An **&#233;tale topos** is the [[sheaf topos]] over an [[étale site]], hence over a site whose "open subsets" are [[étale morphisms]] into the base [[space]]. The intrinsic [[cohomology]] of an &#233;tale [[(∞,1)-topos]] is _[[étale cohomology]]_.

More generally there is the pro-&#233;tale topos over a [[pro-étale site]], which is a bit better behaved. In particular the intrinsic [[cohomology]] of a pro-&#233;tale [[(∞,1)-topos]] includes the [[Weil cohomology theory]] [[ℓ-adic cohomology]].

Generally, given that an [[étale morphism of schemes]] is a [[formally étale morphism]] subject to a size constraint on its [[fibers]] -- for an actual [[étale morphism of schemes]] the fibers are [[finite sets]] in the suitable sense (formal duals to [[étale algebras]]) while for a [[pro-étale morphism of schemes]] they are [[pro-objects]] of such fibers --
in a suitable ambient context ("[[differential cohesion]]") one can drop all finiteness conditions and consider just opens given by [[formally étale morphisms]] as encoded by an [[infinitesimal shape modality]]. This we discuss [below](#GeneralAbstract).

### &#201;tale topos of a differentially cohesive object
 {#GeneralAbstract}

We discuss how in [[differential cohesion]] $\mathbf{H}_{th}$ every object $X$ canonically induces its &#233;tale topos $Sh_{\mathbf{H}_{th}}(X)$.


For $X \in \mathbf{H}_{th}$ any object in a [[differential cohesion|differential cohesive]] $\infty$-topos, we formulate 

1. the [[(∞,1)-topos]] denoted $\mathcal{X}$ or $Sh_\infty(X)$ of [[(∞,1)-sheaves]] over $X$, or rather of formally &#233;tale maps into $X$;


1. the [[structure (∞,1)-sheaf]] $\mathcal{O}_{X}$ of $X$.

The resulting structure is essentially that discussed ([Lurie, Structured Spaces](#Lurie)) if we regard $\mathbf{H}_{th}$ equipped with its formally &#233;tale morphisms, ([def.](differential+cohesive+%28infinity%2C1%29-topos#FormallyEtaleInHTh)), as a ([[large category|large]]) [[geometry for structured (∞,1)-toposes]]. 

One way to motivate this is to consider structure sheaves of flat differential forms. To that end, let $G \in Grp(\mathbf{H}_{th})$ a differential cohesive [[∞-group]] with [de Rham coefficient object](cohesive+%28infinity,1%29-topos+--+structures#deRhamCohomology) $\flat_{dR}\mathbf{B}G$ and for $X \in \mathbf{H}_{th}$ any differential homotopy type, the product projection 

$$
  X \times \flat_{dR} \mathbf{B}G \to X
$$

regarded as an object of the [[slice (∞,1)-topos]] $(\mathbf{H}_{th})_{/X}$ _almost_ qualifies as a "bundle of flat $\mathfrak{g}$-valued differential forms" over $X$: for $U \to X$ an cover (a [[1-epimorphism]]) regarded in $(\mathbf{H}_{th})_{/X}$, a $U$-plot of this product projection is a $U$-plot of $X$ together with a flat $\mathfrak{g}$-valued de Rham cocycle on $X$.

This is indeed what the sections of a corresponding bundle of differential forms over $X$ are supposed to look like -- but only _if_ $U \to X$ is sufficiently _spread out_ over $X$, hence sufficiently [[étale map|étale]]. Because, on the extreme, if $X$ is the point (the [[terminal object]]), then there should be no non-trivial section of differential forms relative to $U$ over $X$, but the above product projection instead reproduces all the sections of $\flat_{dR} \mathbf{B}G$.

In order to obtain the correct cotangent-like bundle from the product with the de Rham coefficient object, it needs to be _restricted_ to plots out of suficiently &#233;tale maps into $X$. In order to correctly test differential form data, "suitable" here should be "formally", namely infinitesimally. Hence the restriction should be along the full inclusion

$$
  (\mathbf{H}_{th})_{/X}^{fet} \hookrightarrow (\mathbf{H}_{th})_{/X}
$$

of the formally &#233;tale maps (see [def.](differential+cohesive+%28infinity%2C1%29-topos#FormallyEtaleInHTh)) into $X$. Since on formally &#233;tale covers the sections should be those given by $\flat_{dR}\mathbf{B}G$, one finds that the corresponding "cotangent bundle" must be the [[coreflective subcategory|coreflection]] along this inclusion. The following proposition establishes that this coreflection indeed exists.


 
+-- {: .num_defn #EtaleSlice}
###### Definition

For $X \in \mathbf{H}_{th}$ any object, write

$$
  (\mathbf{H}_{th})^{fet}_{/X} \hookrightarrow (\mathbf{H}_{th})_{/X}
$$ 

for the full [[sub-(∞,1)-category]] of the [[slice (∞,1)-topos]] over $X$ on those maps into $X$ which are formally &#233;tale, (see [def.](differential+cohesive+%28infinity%2C1%29-topos#FormallyEtaleInHTh)).

We also write $FEt_{\mathbf{X}}$ or $Sh_{\mathbf{H}}(X)$ for $(\mathbf{H}_{th})_{/X}^{fet}$.


=--

+-- {: .num_prop #EtalificationIsCoreflection}
###### Proposition

The inclusion $\iota$ of def. \ref{EtaleSlice} is both [[reflective sub-(∞,1)-category|reflective]] as well as [[coreflective subcategory|coreflective]], hence it fits into an [[adjoint triple]] of the form

$$
  (\mathbf{H}_{th})_{/X}^{fet} 
  \stackrel{\overset{L}{\leftarrow}}{\stackrel{\overset{\iota}{\hookrightarrow}}{\underset{Et}{\leftarrow}}}
  (\mathbf{H}_{th})_{/X}
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the general discussion at _[[reflective factorization system]]_, the reflection is given by sending a morphism $f \colon Y \to X$ to 
$X \times_{\mathbf{\Pi}_{inf}(X)} \mathbf{\Pi}_{inf}(Y) \to Y$ and the reflection unit is the left horizontal morphism in 

$$
  \array{
    Y &\to& X \times_{\mathbf{\Pi}_{inf}(Y)} \mathbf{\Pi}_{inf}(Y) &\to& \mathbf{\Pi}_{inf}(Y)
   \\
    & \searrow & \downarrow^{} && \downarrow^{\mathrlap{\mathbf{\Pi}_{inf}(f)}}
   \\
   && X &\to& \mathbf{\Pi}_{inf}(X)
  }
  \,.
$$ 

Therefore $(\mathbf{H}_{th})_{/X}^{fet}$, being a reflective subcategory of a [[locally presentable (∞,1)-category]], is (as discussed there) itself locally presentable. Hence by the [[adjoint (∞,1)-functor theorem]] it is now sufficient to show that the inclusion preserves all small [[(∞,1)-colimits]] in order to conclude that it also has a right [[adjoint (∞,1)-functor]]. 

So consider any [[diagram]] [[(∞,1)-functor]] $I \to (\mathbf{H}_{th})_{/X}^{fet}$ out of a [[small (∞,1)-category]]. Since the inclusion of $(\mathbf{H}_{th})_{/X}^{fet}$ is full, it is sufficient to show that the $(\infty,1)$-colimit over this diagram taken in $(\mathbf{H}_{th})_{/X}$ lands again in $(\mathbf{H}_{th})_{/X}^{fet}$ in order to have that $(\infty,1)$-colimits are preserved by the inclusion. Moreover, colimits in a slice of $\mathbf{H}_{th}$ are computed in $\mathbf{H}_{th}$ itself (this is discussed at _[slice category - Colimits](overcategory#LimitsAndColimits)_).


Therefore we are reduced to showing that the square

$$
  \array{
    \underset{\to_i}{\lim} Y_i &\to& \mathbf{\Pi}_{inf} \underset{\to_i}{\lim} Y_i 
    \\
    \downarrow && \downarrow
    \\
    X &\to& \mathbf{\Pi}_{inf}(X)
  }
$$

is an [[(∞,1)-pullback]] square. But since $\mathbf{\Pi}_{inf}$ is a [[left adjoint]] it commutes with the $(\infty,1)$-colimit on objects and hence this diagram is equivalent to 

$$
  \array{
    \underset{\to_i}{\lim} Y_i &\to& \underset{\to_i}{\lim} \mathbf{\Pi}_{inf} Y_i 
    \\
    \downarrow && \downarrow
    \\
    X &\to& \mathbf{\Pi}_{inf}(X)
  }
  \,.
$$

This diagram is now indeed an [[(∞,1)-pullback]] by the fact that we have [[universal colimits]] in the [[(∞,1)-topos]] $\mathbf{H}_{th}$, hence that on the left the component $Y_i$ for each $i \in I$ is the [[(∞,1)-pullback]] of $\mathbf{\Pi}_{inf}(Y_i) \to \mathbf{\Pi}_{inf}(X)$, by assumption that we are taking an $(\infty,1)$-colimit over formally &#233;tale morphisms.

=--

+-- {: .num_prop }
###### Proposition

The $\infty$-category $(\mathbf{H}_{th})_{/X}^{fet}$ is an [[(∞,1)-topos]] and the canonical inclusion into $(\mathbf{H}_{th})_{/X}$ is a [[geometric embedding]].

=--

+-- {: .proof}
###### Proof

By prop. \ref{EtalificationIsCoreflection} the inclusion $(\mathbf{H}_{th})_{/X}^{fet} \hookrightarrow (\mathbf{H}_{th})_{/X}$ is [[reflective sub-(infinity,1)-category|reflective]] with reflector given by the $(\mathbf{\Pi}_{inf}-equivalences , \mathbf{\Pi}_{inf}-closed)$ factorization system. Since $\mathbf{\Pi}_{inf}$ is a [[right adjoint]] and hence in particular preserves [[(∞,1)-pullbacks]], the $\mathbf{\Pi}_{inf}$-equivalences are stable under pullbacks. By the discussion at _[[stable factorization system]]_ this is the case precisely if the corresponding reflector preserves [[finite (∞,1)-limits]]. Hence the embedding is a [[geometric embedding]] which exhibits a [[sub-(∞,1)-topos]] inclusion.

=--

+-- {: .num_defn #TheStructureSheafOfX}
###### Definition


For $X \in \mathbf{H}_{th}$ we speak of 

$$
  \mathcal{X} \coloneqq Sh_{\mathbf{H}_{th}}(X)
  \coloneqq
  (\mathbf{H}_{th})_{/X}^{fet}
$$

also as the ([[petit (∞,1)-topos|petit]]) [[(∞,1)-topos]] of $X$, or the **&#233;tale topos** of $X$.

Write

$$
  \mathcal{O}_X 
    \colon
  \mathbf{H}_{th}
    \stackrel{(-) \times X}{\to}
  (\mathbf{H}_{th})_{/X}
    \stackrel{Et}{\to}
  (\mathbf{H}_{th})_{/X}^{fet}  
$$

for the composite [[(∞,1)-functor]] that sends any $A \in \mathbf{H}_{th}$ to the etalification, prop. \ref{EtalificationIsCoreflection}, of the projection $A \times X \to X$.

We call $\mathcal{O}_X$ the **[[structure sheaf]]** of $X$.


=--


+-- {: .num_remark }
###### Remark

For $X, A \in \mathbf{H}_{th}$ and for $U \to X$ a [[formally étale morphism]] in $\mathbf{H}_{th}$ (hence like an [[open subset]] of $X$), we have that 

$$
  \begin{aligned}
    \mathcal{O}_{X}(A)(U) 
    & \coloneqq
    Sh_{\mathbf{H}_{th}}(X)( U , \mathcal{O}_{X}(A) )
    \\
    & \coloneqq   
    Sh_{\mathbf{H}_{th}}(X)( U , Et(X \times A) )
    \\
    & \simeq
    (\mathbf{H}_{th})_{/X}(U, X \times A)
    \\
    & \simeq
    \mathbf{H}_{th}(U,A)
    \\
    & \simeq
    A(U)
  \end{aligned}
  \,,
$$

where we used the [[adjoint (∞,1)-functor|∞-adjunction]] $(\iota \dashv Et)$ of prop. \ref{EtalificationIsCoreflection} and the [[(∞,1)-Yoneda lemma]].

This means that $\mathcal{O}_{X}(A)$ behaves as the _sheaf of $A$-valued functions over $X$_. 

Since $\mathcal{O}_{X}$ is [[right adjoint]] to the forgetful functor

$$
  Sh_{\mathbf{H}}(X) 
    \simeq 
  (\mathbf{H}_{th})_{/X}^{fet} 
    \hookrightarrow 
  (\mathbf{H}_{th})_{/X} 
    \stackrel{\underset{X}{\sum}}{\to}
  \mathbf{H}_{th}
$$

it preserves [[(∞,1)-limits]]. Therefore this is a [[structure sheaf]] which exhibits $Sh_{\mathbf{H}_{th}}(X)$ as a [[structured (∞,1)-topos]] over $\mathbf{H}_{th}$ regarded as a (large) [[geometry (for structured (∞,1)-toposes)]], with the formally &#233;tale morphisms being the "admissible morphisms".

=--


+-- {: .num_example #CotangentBundle}
###### Example

Let $G \in Grp(\mathbf{H}_{th})$ be an [[∞-group]] and write $\flat_{dR} \mathbf{B}G \in \mathbf{H}_{th}$ for the corresponding de Rham coefficient object.

Then 

$$
  \mathcal{O}_X(\flat_{dR}\mathbf{B}G)
  \in 
  Sh_{\mathbf{H}}(X)
$$ 

we may call the **$G$-valued flat cotangent sheaf** of $X$.

=--

+-- {: .num_remark }
###### Remark

For $U \in \mathbf{H}_{th}$ a test object (say an object in a [[(∞,1)-site]] of definition, under the [[Yoneda embedding]]) a formally &#233;tale morphism $U \to X$ is like an [[open map]]/open embedding. Regarded as an object in $(\mathbf{H}_{th})_{/X}^{fet}$ we may consider the sections over $U$ of the cotangent bundle as defined above, which in $\mathbf{H}_{th}$ are diagrams

$$
  \array{
    U &&\to&& \mathcal{O}_X(\flat_{dR}\mathbf{B}G)
    \\
    & \searrow && \swarrow
    \\
    && X
  }
  \,.
$$

By the fact that $Et(-)$ is [[right adjoint]], such diagrams are in bijection to diagrams

$$
  \array{
    U &&\to&& X \times \flat_{dR} \mathbf{B}G
    \\
    & \searrow && \swarrow
    \\
    && X
  }
$$

where we are now simply including on the left the formally &#233;tale map $(U \to X)$ along $(\mathbf{H}_{th})^{fet}_{/X} \hookrightarrow (\mathbf{H}_{th})_{/X}$.

In other words, the sections of the $G$-valued flat cotangent sheaf $\mathcal{O}_X(\flat_{dR}\mathbf{B}G)$ are just the sections of $X \times \flat_{dR}\mathbf{B}G \to X$ itself, only that the _domain_ of the section is constrained to be a formally &#233; patch of $X$.

But then by the very nature of $\flat_{dR}\mathbf{B}G$ it follows that the flat sections of the $G$-valued cotangent bundle of $X$ are indeed nothing but the flat $G$-valued differential forms on $X$.

=--

+-- {: .num_prop #StructuredPetitToposesAreLocallyContractible}
###### Proposition

For $X \in \mathbf{H}_{th}$ an object in a differentially cohesive
$\infty$-topos, then its petit structured $\infty$-topos
$Sh_{\mathbf{H}_{th}}(X)$, according to def. \ref{TheStructureSheafOfX},
is [[locally ∞-connected (∞,1)-topos|locally ∞-connected]].

=--

+-- {: .proof}
###### Proof

We need to check that the composite

$$
  \infty Grpd \stackrel{Disc}{\longrightarrow} \mathbf{H}_{th}
   \stackrel{(-) \times X}{\longrightarrow}
   (\mathbf{H}_{th})_{/X}
  \stackrel{L}{\longrightarrow}
  Sh_{\mathbf{H}}(X)
$$

preserves [[(∞,1)-limits]], so that it has a further 
[[left adjoint]]. Here $L$ is the 
reflector from prop. \ref{EtalificationIsCoreflection}. 
Inspection shows that this composite sends an object $A \in \infty Grpd$ to 
$\mathbf{\Pi}_{inf}(Disc(A)) \times X \to X$:

$$
  \array{
    \mathbf{\Pi}_{inf}(Disc(A)) \times X
     &\longrightarrow&
    \mathbf{\Pi}_{inf}(Disc(A) \times X) & \simeq \mathbf{\Pi}_{inf}(Disc(A)) \times \mathbf{\Pi}_{inf}(X)
    \\
    \downarrow &{}^{(pb)}& \downarrow
    \\
    X &\longrightarrow& \mathbf{\Pi}_{inf}(X)
  }
  \,.
$$

 
By the discussion at [slice (∞,1)-category -- Limits and colimits](slice+infinity-category#LimitsAndColimits) an [[(∞,1)-limit]] in the slice $(\mathbf{H}_{th})_{/X}$ is computed as an [[(∞,1)-limit]] in $\mathbf{H}$ of the [[diagram]] with the slice [[cocone]] adjoined. By [[right adjoint|right adjointness]] of the inclusion $Sh_{\mathbf{H}}(X) \hookrightarrow (\mathbf{H}_{th})_{/X}$ the same is then true for $Sh_{\mathbf{H}}(X) \coloneqq (\mathbf{H}_{th})_{/X}^{et}$.

Now for $A \colon J \to \infty Grpd$ a [[diagram]], it is taken to the diagram $j \mapsto \mathbf{\Pi}_{inf}(Disc(A_j)) \times X \to X$ in $Sh_{\mathbf{H}}(X)$ and so its $\infty$-limit is computed in $\mathbf{H}$ over the diagram locally of the form

$$
  \array{
     X \times \mathbf{\Pi}_{inf}(Disc(A_{j}))
     &&\longrightarrow&&
     X \times \mathbf{\Pi}_{inf}(Disc(A_{j'}))
     \\
     & \searrow && \swarrow
     \\
     && X
  }
  \simeq
  \array{
     X \times \mathbf{\Pi}_{inf}(Disc(A_{j}))
     &&\longrightarrow&&
     X \times \mathbf{\Pi}_{inf}(Disc(A_{j'}))
     \\
     & \searrow && \swarrow
     \\
     && X \times \ast
  }
  \,.
$$

Since $\infty$-limits commute with each other this limit is the product of

1.  $\underset{\leftarrow}{\lim}_j \mathbf{\Pi}_{inf}(Disc(A_j))$ 

1. $\underset{\leftarrow}{\lim}_{J \star \Delta^0} X$ (over the co-coned diagram constant on $X$).

For the first of these, since the [[infinitesimal shape modality]] $\mathbf{\Pi}_{inf}$
is in particular a [[right adjoint]] (with [[left adjoint]] the 
[[reduction modality]]), and since $Disc$ is also [[right adjoint]] by [[cohesion]], we have a [[natural equivalence]]

$$
  \underset{\leftarrow}{\lim}_j \mathbf{\Pi}_{inf}(Disc(A_j))
  \simeq
   \mathbf{\Pi}_{inf}(Disc(\underset{\leftarrow}{\lim}_j(A_j)))
  \,.
$$

For the second, the $\infty$-limit over an $\infty$-category $J \star \Delta^0$ of a functor constant on $X$ is 

$$
  \begin{aligned}
     \underset{\leftarrow}{\lim}_{J \star \Delta^0} X
     & \simeq
     \underset{\leftarrow}{\lim}_{J \star \Delta^0} [\ast, X]
     \\
     & \simeq
     [\underset{\rightarrow}{\lim}_{J \star \Delta^0} \ast, X]
     \\
     & \simeq
     [{\vert {J \star \Delta^0}\vert}, X]
     \\
     & \simeq 
     [\ast, X] \simeq X
  \end{aligned}
  \,,
$$

where the last line follows since ${J \star \Delta^0}$
has a terminal object and hence contractible geometric realization.

In conclusion this shows that $\infty$-limits are preserved by $L \circ (-)\times X\circ Disc$.

=--

## Properties

### Sheaf condition and examples of &#233;tale sheaves
 {#SheafConditionAndExamples}

+-- {: .num_prop #EtaleDescentDetectedOnOpenImmersionCovers}
###### Proposition

For $X$ a [[scheme]], and $A \in PSh(X_{et})$ a [[presheaf]],
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
showing that the represented presheaf satisfies [[descent]] along collections of open immersions and along surjective maps of affines. For the first this is clear (it is [[Zariski topology]]-descent). For the second case of a [[faithfully flat]] cover of affines $Spec(B) \to Spec(A)$ it follows with the exactness of the correspomnding [[Amitsur complex]]. See there for details.

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


+-- {: .num_defn}
###### Definition

For $X_{et}$ an [[étale site]], write $\mathcal{D}(X_{et})$ for the [[derived category]] of the [[abelian category]] $Ab(Sh(X_{et}))$ of [[abelian sheaves]] on $X$.

=--

+-- {: .num_prop}
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

By the discussion at _[[direct image]]_ and at _[[abelian sheaf cohomology]]_. See e.g. ([Tamme, II (1.3.4)](#Tamme), [Milne prop. 12.1](#Milne)).

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


### Quasi-coherent modules
 {#QuasiCoherentModules}

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


### Relation to Zariski topos

+-- {: .num_remark }
###### Remark

A [[cover]] in the [[Zariski topology]] on [[schemes]] is an [[open immersion of schemes]] and hence is in particular an [[étale morphism of schemes]]. Hence the [[étale site]] is finer than the [[Zariski site]] and so every &#233;tale [[sheaf]] is a Zariski sheaf, but not necessarily conversely. Expressed in a different way, the &#233;tale topos is a [[subtopos]] of the Zariski topos.

=--


For more see at _[&#233;tale cohomology -- Properties -- Relation to Zariski cohomology](etale+cohomology#RelationZariskiEtaleCohomology)_.

### As a classifying topos

The &#233;tale topos over the big &#233;tale site of [[commutative rings]] is the [[classifying topos]] for [[strict local rings]].



## Related concepts

* [[basics of étale cohomology]]

* [[étale homotopy]]

* [[étale cohomology]]

## References

### Etale topos of a schemes

* [[Günter Tamme]], section II 1 of _[[Introduction to Étale Cohomology]]_
 {#Tamme}

* [[James Milne]], section 7 of _[[Lectures on Étale Cohomology]]_
 {#Milne}

### Etale topos of a differentially cohesive object

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ ([arXiv:1310.7930](http://arxiv.org/abs/1310.7930))




[[!redirects etale toposes]]
[[!redirects etale topoi]]

[[!redirects étale topos]]
[[!redirects étale toposes]]
[[!redirects étale topoi]]

[[!redirects étale (∞,1)-topos]]
[[!redirects etale (∞,1)-topos]]
[[!redirects étale (∞,1)-toposes]]
[[!redirects etale (∞,1)-toposes]]

[[!redirects étale (infinity,1)-topos]]

[[!redirects etale (infinity,1)-topos]]
[[!redirects étale (infinity,1)-toposes]]
[[!redirects etale (infinity,1)-toposes]]