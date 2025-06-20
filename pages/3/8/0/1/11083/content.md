
> This entry contains one chapter of the material at _[[geometry of physics]]_.

> previous chapters: _[[geometry of physics -- categories and toposes|categories and toposes]]_, _[[geometry of physics -- smooth spaces|smooth sets]]_,

> next chapter: _[[geometry of physics -- groups|groups]]_, _[[geometry of physics -- supergeometry|supergeometry]]_, _[[geometry of physics -- prequantum geometry|prequantum geometry]]_

> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--





Fundamental physics is all based on the _[[gauge principle]]_. This says in particular that it is wrong to think of two different _[[gauge field]] configurations_ (discussed in detail below in _[Fields](#Fields)_) as being [[equality|equal]] or not. Instead it makes sense to ask if there is (or not) a _[[gauge transformation]]_ from one to the other that exibits an gauge [[equivalence]] between the two fields. The simplest example of this is described in detail below in  _[Gauge transformations in electromagnetism](#GaugeTransformationsInElectromagnetism)_.

But this means that the collection of [[gauge fields]] on a [[spacetime]] $X$, which we will write as a [[mapping space]] $[X, \mathbf{B}G_{conn}]$, cannot be a [[smooth space]] as considered above, for if it were such a smooth space, then we could ask if two gauge fields $\nabla_1, \nabla_2 \colon * \to [X,\mathbf{B}G_{conn}]$ were equal or not. 

Notice that this already applies to a single gauge field: given any $\nabla \colon * \to [X,\mathbf{B}G_{conn}]$ it is certainly equal to itself, but is nevertheless also _gauge equivalent_ to itself, but the latter it may be in several non-equivalent ways: there may be non-trivial auto-gauge transformations $\nabla \to \nabla$. Since these can be composed, are, by definition, invertible, and contain the trivial gauge transformaiton, these form a _[[group]]_, the group of auto-gauge equivalences of $\nabla$. (Groups are discussed in detail below in _[Groups](#Groups)_) If that gauge field $\nabla$ is itself the trivial gauge field, $\nabla = \nabla_0$, then this group of auto-gauge equivalences is the _[[gauge group]]_ of the given [[gauge theory]]:

$$
  G \simeq Aut(\nabla_0) \simeq \{\nabla_0 \stackrel{\simeq}{\to} \nabla_0\}
  \,.
$$

For this reason, the collection of _all_ gauge fields and all gauge transformations between them form something that is a [[group]] over ever fixed element, but which generalizes the notion of a group in that there are not only auto-equivalences, but also equivalences going from one element to another. Such a structure is called a _[[groupoid]]_. Gauge fields form not a [[set]] with smooth structure, a [[smooth space]], but a [[groupoid]] with smooth structure: a _[[smooth groupoid]]_. 

At least ordinary gauge fields do. More generally, the gauge principle goes further: it is in general also a mistake to assume that given two gauge transformations $\lambda_1, \lambda_2 \colon \nabla_1 \to \nabla_2$ between two gauge fields, it makes good sense to ask whether they are equal or not. Again, the gauge prinicle says that we should instead ask if there is a _[[gauge-of-gauge transformation]]_ between them, that exhibits a gauge [[equivalence]] $\rho \colon \lambda_1 \simeq \lambda_2$. If these gauge-of-gauge equivalences are nontrivial it would seem that gauge fields form a generalization of the notion of a [[groupoid]] called a _[[2-groupoid]]_. But in general the gauge principle goes on: we can in general never decide if two $n$-fold gauge-of-gauge transformations are actually equal, all we have is, possibly, an $(n+1)$-fold gauge transformation going between them which exhibits their gauge equivalence, this being so for all $0 \lt n \lt \infty$. One therefore says that gauge fields in general form an _[[∞-groupoid]]_ whose _[[n-morphisms]]_ are $n$-fold [[gauge-of-gauge transformations]]. These $\infty$-groupoids are also called _[[homotopy types]]_. And since at the same time there is still a notion of gauge fields varying smoothly, these are _[[smooth ∞-groupoids]]_ or _[[smooth homotopy types]]_. This is what we discuss here. 

Remarkably, the same concept appears in [[constructive mathematics]]: there it is in general wrong to consider an [[equality]] between two [[terms]] $\nabla_1, \nabla_2 \colon [X, \mathbf{B}G_{conn}]$, instead one is to consider an explicit [[proof]] that they are equal, provide an explicit [[equivalence]] between them. Such a proof $\lambda$ is itself a [[term]], of [[identity type]], written just as before, $\lambda \colon (\nabla_1 \simeq \nabla_2)$. And, in turn, the same applies to these proofs of equivalence themselves: in [[constructive mathematics]] one demands a [[proof]] $\rho$ that two equivalences $\lambda_1, \lambda_2 \colon (\nabla_1 \simeq \nabla_2)$ are equivalent, and hence a term $\rho \colon (\lambda_1 \simeq \lambda_2)$ of a higher [[identity type]]. If this goes ever on, and one speak of _[[intensional type theory]]_ or _[[homotopy type theory]]_.

This remarkable matching of [[higher gauge theory]] and [[homotopy type theory]] is what drives the discussion here.  


#Contents#
* table of contents
{:toc}


## Smooth 1-groupoids


### Motivation: Fields and gauge transformations in electromagnetism
 {#GaugeTransformationsInElectromagnetism}

The mathematical concept of _[[smooth groupoid]]_ is well familiar, in slight disguise, in basic _[[gauge theory]]_. Here we make this explicit for basic [[electromagnetism]]. For more exposition and details along these lines see
([[schreiber:bachelor thesis Eggertsson|Eggertson 14]]).

We have seen in _[The electromagnetic field strength](#ElectromagneticFieldStrength)_ that a configuration of the electromagnetic field on $\mathbb{R}^4$ is given by a [[differential 1-form]] $A \in \Omega^1(\mathbb{R}^4)$, the "[[electromagnetic potential]]". It describes a field configuration with [[field strength]] Lorentz tensor (with respect to the canonical [[coordinates]] $(t, x^1, x^2, x^3) \coloneqq (x^i)_{i = 1}^4 = $ on $\mathbb{R}^4$)

$$
  \begin{aligned}
    F & = \mathbf{d}A 
      \\
      & =
       E_1 \mathbf{d}x^1 \wedge \mathbf{d}t
       + 
       E_1 \mathbf{d}x^1 \wedge \mathbf{d}t
       + 
       E_1 \mathbf{d}x^1 \wedge \mathbf{d}t
       + 
      \\
      & 
       + B_1 \mathbf{d}x^2 \wedge \mathbf{d}x^3
       + B_2 \mathbf{d}x^3 \wedge \mathbf{d}x^1
       + B_3 \mathbf{d}x^1 \wedge \mathbf{d}x^2
  \end{aligned}     
$$

with electric [[field strength]] $(E_i \in C^\infty(\mathbb{R}^4))_{i = 1}^3$ and magnetic [[field strength]] $(B_i \in C^\infty(\mathbb{R}^4))_{i = 1}^3$ given  that is given by the [[de Rham differential]] of $A$:

$$
  \begin{aligned}
    F = \mathbf{d}A
  \end{aligned}
  \,.
$$

After Maxwell it was thought that $F \in \Omega^2(\mathbb{R}^4)$ alone genuinely reflects the configuration of the electromagnetic field. But with the discovery of [[quantum mechanics]] it became clear that it is indeed the potential $A$ itself that reflects the configuration of the electromagnetic field: in the presence of [[magnetic flux]] or other topoligical constraints, there can be different $A, A' $ with the _same_ $F = \mathbf{d}A = \mathbf{d}A'$ which nevertheless describe experimentally distinguishable electromagnetic field configurations. (Distinguishable by the [[Aharonov-Bohm effect]] and also to some extent by [[Dirac charge quantization]]; this is discussed at _[Circle-principal connections](#CirclePrincipalConnections)_ below.)

However, not all different gauge potentials describe different physics. The actual configuration space of electromagnetism on a [[spacetime]] $X$ is finer than $\mathbf{\Omega}^2_{cl}(X)$ but coarser than $\mathbf{\Omega}^1(X)$. And it is not quite a smooth space itself, but a _[[smooth groupoid]]_:

one finds that two electromagnetic potentials $A, A' \in \Omega^1(\mathbb{R}^4)$ for which there is a function $\lambda \in C^\infty(\mathbb{R}^4)$ such that 

$$
  A' = A + \mathbf{d}\lambda
$$

represent _different but [[equivalence|equivalent]]_ field configurations. One says that _$\lambda$ induces a [[gauge transformation]] from $A$ to $A'$_. We write $\lambda \colon A \stackrel{\simeq}{\to} A'$ to reflect this.

So the configuration space of electromagnetism does not just have points and coordinate systems. But it is also equipped with the information of a space of gauge transformations between any two coordinate systems laid out in it (which may be empty). 

To see what the structure of such a _smooth gauge groupoid_ should be, notice that the above defines an [[action]] of smooth functions $\lambda$ on smooth $1$-forms $A$, 


+-- {: .num_defn #ActionOfFunctionsOnForms}
###### Definition

For any $U \in $ [[CartSp]], Write $\Omega^1_{vert}(X \times U)$ for the set of [[differential 1-forms]] on $X \times U$ with no components along $U$, and write $C^\infty(X \times U , U(1))$ for the [[group]] of [[circle group]] valued [[smooth functions]]. There is an [[action]] of this group on the 1-forms 

$$
  \rho_U 
   \colon 
  \Omega^1_{vert}(X \times U) \times C^\infty(X \times U, U(1))
    \to
  \Omega^1_{vert}(X \times U)
$$

given by

$$
  \rho_U \colon (A,\lambda) \mapsto A + \mathbf{d}_X \lambda
  \,.
$$

=--

Given such an action of a [[discrete group]] on a [[set]], we might be demoted to form the [[quotient]] set $\Omega^1_{vert}(X\times U)/C^\infty(X \times U, U(1))$. This set contains the gauge [[equivalence classes]] of $U$-parameterized collections of electromagnetic gauge fields on $X$. But it turns out that this is too little information to correctly capture physics. For that instead we need to remember not just that two gauge fields are equivalent, but how they are equivalent. That is, we for $\lambda$ a gauge transformation from $A_1$ to $A_2$, we should have an [[equivalence]] $\lambda \colon A_1 \stackrel{\simeq}{\to} A_2$.

+-- {: .num_defn #EMGaugeGroupoidOverU}
###### Definition

The [[action groupoid]]

$$
  \Omega^1_{vert}(X\times U)//  C^\infty(X \times U, U(1))
  \coloneqq
  (
    \Omega^1_{vert}(X\times U) \times C^\infty(X \times U, U(1))
    \stackrel{\overset{t = \rho}{\longrightarrow}}{\underset{s = p_1}{\longrightarrow}}
    \Omega^1_{vert}(X\times U)
  )
$$

is the [[groupoid]] whose 

* [[objects]] are $U$-parameterized collections of gauge potentials $A \in \Omega^1_{vert}(X \times U)$;

* [[morphisms]] are pairs $(A,\lambda)$ with $A$ an object and $\lambda \in C^\infty(X \times U, U(1))$, with [[domain]] $A$ and [[codomain]] $A + \mathbf{d}_X \lambda$;

* [[composition]] is given by multiplication of the $\lambda$-labels in the group $C^\infty(X \times U, U(1))$.

=--

This is the discrete _gauge groupoid_ for $U$-parameterized collections of fields. It refines the _[[gauge group]]_, which is recoverd as its [[fundamental group]]:

+-- {: .num_prop }
###### Proposition

Let $A_0 \coloneqq 0 \in \Omega^1_{vert}(X \times U)$ be the trivial gauge field. Then its [[automorphism group]] in the gauge groupoid of def. \ref{EMGaugeGroupoidOverU} is the group of [[circle]]-group valued functions on $U$:

$$
  \pi_1(\Omega^1_{vert}(X\times U)// C^\infty(X \times U, U(1)), A_0)
  =
  Aut(A_0)
  \simeq
  C^\infty(U,U(1))
  \,.
$$

=--

+-- {: .proof}
###### Proof

By definition, an automorphism of $A_0$ is given by a function 
$\lambda \in C^\infty(X \times U, U(1))$ such that $A_0 = A_0 + \mathbf{d}_X \lambda$. This is the case precisely if $\mathbf{d}_X \lambda = 0$, hence if $\lambda$ is constant along $X$. But a function on $X \times U$ which is constant along $X$ is canonically identified with a function on just $U$.

=--

All this data is in fact [[natural transformation|natural]] in $U$. Recall that $\Omega^1_{vert}(X \times U) = \mathbf{\Omega}^1(X)(U)$ is the set of $U$-charts of the smooth moduli space $\mathbf{\Omega}^1(X)$ of smooth 1-forms on $X$. Similarly $C^\infty(X \times U) = \mathbf{C}^\infty(X)(U)$.

+-- {: .num_prop }
###### Proposition

There is a homomorphism of [[smooth spaces]] (def. \ref{HomomorphismOfSmoothSpaces})

$$
  \rho \colon \mathbf{\Omega}^1(X)\times \mathbf{C}^\infty(X) \to \mathbf{\Omega}^1(X)
$$

from the product smooth space, def. \ref{ProductOfSmoothSpaces}, of the smooth moduli spaces of 1-forms and 0-forms on $X$, def. \ref{SmoothSpaceOfFormsOnSmoothSpace}, to that of smooth functions, def. \ref{SmoothSpaceOfSmoothFunctions}, whose component over $U \in $ [[CartSp]] is the action 

$$
  \rho_U \colon (A,\lambda) \mapsto  A + \mathbf{d}\lambda
$$

of def. \ref{ActionOfFunctionsOnForms}.

=--

We then also want to consider a _smooth action groupoid_.

+-- {: .num_defn }
###### Definition

Write 

$$
  \mathbf{\Omega}^1(X) // \mathbf{C}^\infty(X, U(1))
  : 
  CartSp^{op}
  \to 
  Grpd
$$

for the [[contravariant functor]] from coordinate systems to the [[category]] of [[groupoids]], which assigns to $U \in CartSp$ the discrete action groupoid of $U$-collections of gauge fields of def. \ref{EMGaugeGroupoidOverU}.

$$
  U \mapsto \Omega^1_{vert}(X \times U) // C^\infty(X\times U, U(1))
  \,.
$$

=--

Such a structure _[[presheaf]]_ of [[groupoids]] is a common joint generalization of the notion of [[discrete groupoids]] and [[smooth spaces]]. We call them _[[smooth groupoids]]_. This is what we turn to in _[Smooth groupoids](#SmoothGroupoids)_




### Definition
 {#SmoothGroupoids}


+-- {: .num_remark }
###### Remark
**on how not to define smooth groupoids**

One could be tempted to define smooth groupoids to be [[internal groupoids]] in [[smooth sets]]. Restricting this definition to groupoids internal to [[diffeological spaces]] yields the concept of _[[diffeological groupoid]]_, restricting it further to groupoids internal to [[smooth manifolds]] yields the concept of _[[Lie groupoid]]_. While these are respectable definitions in themselves, care needs to be exercised in interpreting them correctly: they do _not_ in themselves exhibit the correct [[homotopy theory]] of smooth groupoids. One may of course fix this by changing the concept of [[morphisms]] to generalized morphisms called _[[Morita morphisms]]_ or _[[bibundles]]_. These are certainly useful tools for working with smooth groupoids, and they serve to present their correct homotopy theory, but they do not serve well as the definition of this homotopy theory. For instance without further insight it is rather impossible to guess form the concept of [[bibundles]] between groupoids its correct generalization to [[smooth 2-groupoids]] etc.

But just as the definition of [[smooth sets]], contrasted with that of [[smooth manifolds]], is not only more powerful but also _simpler_, so there is a definition of smooth groupoids which not only does give the correct homotopy theory, but it does so while being much more transparent than these more traditional presentations.

Now, this definition, given below, amounts to saying that smooth groupoids are stacks on the site of smooth manifolds, and that in turn may tend to not sound like a simple definition at all. But there is a further simplification at work. Traditional texts tend to define stacks in terms of the comparatively intricate structures of [[pseudofunctors]] or (dually under the [[Grothendieck construction]]) [[fibered categories]] satisfying [[descent]], and the rich structure of these combinatorial objects tends to become unwieldy already for fairly simple examples. But the theory of [[localization]] of categories turns out to handle the same theory of stacks by much more tractable means (e.g. [Hollander 01](stack#Hollander01)). Here a stack is _presented_ by a plain functor with no [[descent]] condition imposed, something that is hence as simple as a pair of two presheaves. The nature of stacks is then instead just encoded in remembering that some of the morphisms of presheaves of groupoids are to be labeled as [[weak equivalences]], namely those that locally restrict to equivalences of groupoids. 

This style of definition combines the simplicity of the naive definition of Lie groupoids with the full power of [[homotopy theory]], and it immediately generalizes to a definition of [[∞-stacks]] which is just as simple, hence, in the present context, to a definition of [[smooth ∞-groupoid]].

=--


#### Pre-smooth groupoids
 {#PreSmoothGroupoids}


+-- {: .num_defn }
###### Definition

Write [[CartSp]] for the [[category]] of [[Cartesian spaces]] $\mathbb{R}^n$, $n \in \mathbb{N}$, with [[smooth functions]] between them. (The [[full subcategory]] of [[SmoothMfd]] on the Cartesian spaces.) Regard this as a [[site]] by equipping it with the [[coverage]] of (differentiably) [[good open covers]].

=--

For more on this see at _[[geometry of physics -- coordinate systems]]_.


In view of the [[motivation for sheaves, cohomology and higher stacks]] and in direct [[analogy]] with the discussion at _[[geometry of physics -- smooth sets]]_, just replacing [[sets]] by [[groupoids]] throughout, we set:

+-- {: .num_defn #PreSmoothGroupoid}
###### Definition

A _pre-smooth groupoid_ $X$ is a [[presheaf]] of [[groupoids]] on [[CartSp]], hence a [[functor]]

$$
  X \colon CartSp^{op} \longrightarrow Grpd
$$

from [[CartSp]] to the [[1-category]] [[Grpd]].


=--

See at _[geometry of physics -- homotopy types -- groupoids](geometry+of+physic+--+homotopy+types#Groupoids)_ for more on bare groupoids. Here we will freely assume familiarity with these.

+-- {: .num_remark #YonedaIntuition}
###### Remark

The intuition for def. \ref{PreSmoothGroupoid} is the following: a smooth structure on a groupoid is to be determined by which maps from abstract [[coordinate systems]] $\mathbb{R}^n$ into it are to be regarded as smooth maps. Since, by its groupoidal nature, two such maps may be related by a smooth [[homotopy]]/[[gauge transformation]] (in physics: "twisted sectors"), the collection of all smooth functions from $\mathbb{R}^n$  into the smooth groupoid $X$ is itself a bare groupoid. We here _define_ a pre-smooth groupoid as something that assigns to each abstract coordinate systems a groupoid of would-be smooth maps into it

"$X(\mathbb{R}^n) = \left\{ \array{
     & \nearrow \searrow^{\mathrlap{smooth}}
     \\
    \mathbb{R}^n
    &\Downarrow&
    X
    \\
    & \searrow \nearrow_{\mathrlap{smooth}}
 } \right\}$"

We sometimes therefore speak of $X(\mathbb{R}^n)$ as the groupoid of _plots_ or of _probes_ of $X$ (which here is only defined by these!) by $n$-dimensional coordinate systems.

=--

The [[Yoneda lemma]] will turn this intuition into a theorem. For that we need to speak of [[homomorphisms]] of pre-smooth groupoids, hence of "smooth functors" between pre-smooth groupoids.

+-- {: .num_defn #HomGroupoidsOfPreSmoothGroupoids}
###### Definition

A [[homomorphism]] or _smooth map_ between pre-smooth groupoids is a [[natural transformation]] between the [[presheaves]] that they are. We write  

$$
  PreSmooth1Type
  \coloneqq
  Funct(CartSp^{op}, Grpd)
$$ 

for the [[functor category]], the _[[category]] of pre-smooth groupoids_, def. \ref{PreSmoothGroupoid}, regarded naturally as a [[Grpd]]-[[enriched category]].

This means that for $X,Y \in PreSmooth1Type$ two pre-smooth groupoids, then the bare [[hom-groupoid]] 

$$
  PreSmooth1Type(X,Y)_\bullet
  \in 
  Grpd
$$

between them has 

* as [[objects]] the [[natural transformations]] $f \colon X \to Y$ between $X$ and $Y$ regarded as [[functors]], hence collections $\{f(\mathbb{R}^n)\}_{n \in \mathbb{N}}$ of [[functors]] between [[groupoids]] of probes

  $$
     f(\mathbb{R}^n) \colon X(\mathbb{R}^n) \longrightarrow Y(\mathbb{R}^n)
  $$

  such that for every [[smooth function]] $\phi \colon \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ between abstract coordinate charts, these form a (strictly) [[commuting diagram]] with the probe-pullback functors of $X$ and $Y$:

  $$
    \array{
       X(\mathbb{R}^{n_1}) &\overset{f(\mathbb{R}^n)}{\longrightarrow}& Y(\mathbb{R}^{n_1})
       \\
       {}^{\mathllap{X(\phi)}}\downarrow && \downarrow^{\mathrlap{Y(\phi)}}
       \\
       X(\mathbb{R}^{n_2}) &\overset{f(\mathbb{R}^n)}{\longrightarrow}& Y(\mathbb{R}^{n_2})       
    }
    \,;
  $$

* as [[morphisms]] $H \colon f \rightarrow g$ the "[[modifications]]" of these, hence collections $H(\mathbb{R}^n) \colon f(\mathbb{R}^n)\to g(\mathbb{R}^n)$ of [[natural transformations]], such that for every [[smooth function]] $\phi \colon \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ the [[whiskering]] of these satisfies

  $$
    \array{
       X(\mathbb{R}^{n_1})
       \\
       \downarrow^{\mathrlap{X(\phi)}}
       \\
       & \nearrow \searrow^{\mathrlap{f(\mathbb{R}^{n_2})}}
       \\
       X(\mathbb{R}^{n_2})
       &\Downarrow^{H(\mathbb{R}^{n_2})}&
       Y(\mathbb{R}^{n_2})
       \\
       & \searrow \nearrow_{\mathrlap{g(\mathbb{R}^{n_1})}}
    }
    \;\;\;
    =
    \;\;\;
    \array{
       & \nearrow \searrow^{\mathrlap{f(\mathbb{R}^{n_1})}}
       \\
       X(\mathbb{R}^{n_1})
       &\Downarrow^{H(\mathbb{R}^{n_1})}&
       Y(\mathbb{R}^{n_1})
       \\
       & \searrow \nearrow_{\mathrlap{g(\mathbb{R}^{n_1})}}
       \\
       && \downarrow^{\mathrlap{Y(\phi)}}
       \\
       && Y(\mathbb{R}^{n_2}) 
    }
  $$
 
=--

+-- {: .num_remark}
###### Remark

Despite the size of the diagrams in def. \ref{HomGroupoidsOfPreSmoothGroupoids}, what they encode is immediate: this just says that smooth maps between pre-smooth groupoids take all probes of $X$ by abstract coordinate charts to probes of $Y$ by these charts, and take gauge transformations between these to gauge transformations between those, in a way that it compatible with changing probes along smooth maps.

=--


The following is the [[Yoneda lemma]] in this context, and it says that this intuition in remark \ref{YonedaIntuition} is fully correct:


+-- {: .num_prop #YonedaForPreSmoothGroupoids}
###### Proposition

Every [[Cartesian space]] $\mathbb{R}^n$ defines a pre-smooth groupoid $\underline{\mathbb{R}}^n$, def. \ref{PreSmoothGroupoid}, by the assignment

$$
  \underline{\mathbb{R}}^n \colon \mathbb{R}^k  \mapsto C^\infty(\mathbb{R}^k, \mathbb{R}^n)
   \in 
  Set
  \hookrightarrow
  Grpd
$$

where the [[set]] of [[smooth functions]] on the right is regarded as a [[groupoid]] with only [[identity]] morphisms. This construction constitutes a [[fully faithful functor]]

$$
  \underline{(-)}
  \colon
  CartSp \hookrightarrow PreSmooth1Type
$$

making [[CartSp]] a [[full subcategory]] of that of pre-smooth groupoids (the [[Yoneda embedding]]).
Under this embedding for any pre-smooth groupoid $X\in PreSmooth1Type$ and any Cartesian space $\mathbb{R}^n$, there is a [[natural equivalence]] of [[groupoids]]

$$
  PreSmooth1Type(\underline{\mathbb{R}}^n, X)
  \simeq
  X(\mathbb{R}^n)
$$

(the [[Yoneda lemma]] proper).

=--

+-- {: .num_remark}
###### Remark

The last statement of the [[Yoneda lemma]] in prop. \ref{YonedaForPreSmoothGroupoids} expresses just the intuition of remark \ref{YonedaIntuition} and justifies removing the quotation marks displayed there. It also justifies dropping the extra underline denoting the [[Yoneda embedding]]. We will freely identify from now on $\mathbb{R}^n$ with the pre-smooth groupoid that it represents.

=--

+-- {: .num_example}
###### Example

For $X$ a [[smooth set]] (e.g. a [[smooth manifold]]), hence in particular a functor

$$
  X \colon CartSp^{op} \to Set
$$

then its embedding into groupoids

$$
  X \colon CartSp^{op} \to Set \hookrightarrow Grpd
$$

is a pre-smooth groupoid.

=--

More generally:

+-- {: .num_example #ExternalYonedaEmbeddingsIntoPreSmooth1Type}
###### Example

Let 

$$
  \mathcal{G}_\bullet
  = 
  \left\{
    \mathcal{G}_1
      \stackrel{\overset{s}{\longrightarrow}}{\stackrel{\overset{i}{\longleftarrow}}{\underset{t}{\longrightarrow}}}
    \mathcal{G}_0
  \right\}
$$ 

be an [[internal groupoid]] in [[smooth sets]], hence a pair $\mathcal{G}_0, \mathcal{G}_1 \in Smooth0Type$ of smooth sets, equipped with source, target, identity homomorphisms of smooth sets between them, and equipped with a compatibly unital, associative and invertible composition map $\mathcal{G}_1 \underset{\times}{\mathcal{G}_0} \mathcal{G}_1 \to \mathcal{G}_1$. By definition of [[smooth sets]], this means that for every abstract coordinate system $\mathbb{R}^n$ then 

$$
  \mathcal{G}(\mathbb{R}^n)_\bullet
  = 
  \left\{
    \mathcal{G}(\mathbb{R}^n)_1
      \stackrel{\overset{s(\mathbb{R}^n)}{\longrightarrow}}{\stackrel{\overset{i(\mathbb{R}^n)}{\longleftarrow}}{\underset{t(\mathbb{R}^n)}{\longrightarrow}}}
    \mathcal{G}(\mathbb{R}^n)_0
  \right\}
$$ 

is a bare [[groupoid]]. Moreover, this assignment is functorial and hence defines a pre-smooth groupoid

$$
  \mathbb{R}^n 
  \mapsto
  \mathcal{G}(\mathbb{R}^n)_\bullet
  \,.
$$


This exhibits sequence of [[full subcategory]] inclusions

$$
  Grp
  \hookrightarrow
  LieGrpd
  \hookrightarrow
  DiffGrpd
  \hookrightarrow
  Grpd(Smooth0Type)
  \hookrightarrow
  PreSmooth1Type
$$

of [[internal groupoids]] in [[smooth sets]] into pre-smooth groupoids, and hence (by further restriction) also of [[diffeological groupoids]], of [[Lie groupoids]] and of course of just bare [[groupoids]], too. 

Regarding a bare groupoid $\mathcal{G}_\bullet$ as a pre-smooth groupoid this way means to regard it as equipped with [[discrete object|discrete]] [[smooth structure]]. It is given by the [[constant presheaf]]

$$
  \mathbb{R}^n \mapsto \mathcal{G}_\bullet
$$

exhibiting the fact that smooth functions from an $\mathbb{R}^n$ into a geometrically discrete space are constant on one of the points of this space, a situation which here is only refined by the fact that every morphism in the groupoid thus gives a [[homotopy]]/[[gauge transformation]] between the two smooth functions that are constant on the two endpoints of this morphism.

=--

A particular case of this of special importance is this:

+-- {: .num_example #DeloopedGroupAsPreSmoothGroupoid}
###### Example

For $G$ a [[Lie group]], we write $(\mathbf{B}G)_\bullet \in Grpd(Smooth0Type)$ for the Lie groupoid which 

$$
  (\mathbf{B}G)_\bullet
  =
  \left(
     G \stackrel{\longrightarrow}{\stackrel{\overset{i}{\longleftarrow}}{\longrightarrow}}
    \ast
  \right)
$$

whose composition is the product operation in the group (the groupoidal [[delooping]] of $G$). The pre-smooth groupoid that this corresponds to under the embedding of example \ref{ExternalYonedaEmbeddingsIntoPreSmooth1Type} has groupoids of probes of the form


$$
  \mathbb{R}^n 
   \mapsto 
   B \left(C^\infty(\mathbb{R}^n,G)_{disc}\right)
$$

where on the right we have the [[homotopy 1-type]] whose [[fundamental group]] is that of smooth $G$-valued functions on $\mathbb{R}^n$, under pointwise mulitplication.


=--


More specifically, the following class of examples plays a special role in the theory, as they encode what it takes for a pre-smooth groupoid to be a genuinely smooth groupoid.

+-- {: .num_example #GroupoidOfCover}
###### Example

For $X$ a [[smooth manifold]], let $\{U_i \to X\}_{i \in I}$ be an [[open cover]] of $X$. Its _[[Cech groupoid]]_ is the [[Lie groupoid]] ([[diffeological groupoid]]) $C(\{U_i\})_\bullet$ whose

* manifold of objects is $C(\{U_i\})_0 \coloneqq \underset{i \in I}{\coprod} U_i$ is the [[disjoint union]] of all the [[charts]] of the cover;

* manifold of morphisms is $C(\{U_i\})_1 \coloneqq  \underset{i,j \in I}{\coprod}U_i \underset{X}{\times} U_j$ is the [[disjoint union]] of all [[intersections]] of charts.

and whose source, target and identity maps are the evident inclusions. There is then a _unique_ composition operation.

So a global point $\ast \to C(\{U_i\})_\bullet$ may be thought of as a pair $(x,i)$ of a point in the manifold $X$ and a label $i$ of a chart $U_i$ that contains it, and there is is precisely one morphism between two such global point $(x,i)\to (y,j)$ whenever $x = y$ in $X$ and both $U_i$ as well as $U_j$ contain $x$, hence one morphism for each point in an intersection of two patches. Composition of morphism is just re-remembering which intersections they sit in, the schematic picture of the Cech groupoid is this this:

$$
  C(\{U_i\})_\bullet
  =
  \left\{
    \array{
      && (x,j)
      \\
      & \nearrow && \searrow
      \\
      (x,i)
      && \longrightarrow &&
      (x,k)
    }
  \right\}
  \,.
$$

Under the embedding of example \ref{ExternalYonedaEmbeddingsIntoPreSmooth1Type} there is an evident morphism of pre-smooth groupoids

$$
  C(\{U_i\})
  \longrightarrow
  X
$$

from this Cech groupoid of the cover to the manifold that is being covered. This morphism simply forgets the information of which chart or intersection of charts a point is regarded to be in, and just remembers it as a point of $X$. 

$$
  ((x,i) \to (x,j))
  \mapsto
  (x \stackrel{id_x}{\to} x)
  \,.
$$

=--

+-- {: .num_prop #CechCoyclesAsSmoothMaps}
###### Proposition


Let $X$ a [[smooth manifold]], $\{U_i \to X\}$ an [[open cover]]
and $C(\{U_i\})$ the corresponding Cech groupoid, def. \ref{GroupoidOfCover}.
Let $G$ be a [[Lie group]] and $\mathbf{B}G$ its groupoidal [[delooping]] according to example \ref{DeloopedGroupAsPreSmoothGroupoid}.

Then the hom-groupoid $PreSmooth1Type(C(\{U_i\}), \mathbf{B}G)$ of maps from $C(\{U_i\})$ to $\mathbf{B}G$, def. \ref{HomGroupoidsOfPreSmoothGroupoids},
has

* as [[objects]] the [[Cech cohomology|Cech cocycles]] of degree 1 on $X$ relative to the cover and with values in $G$; i.e. collections of smooth functions

  $$
    g_{i j} \;\colon\; U_i \underset{X}{\times} U_j \longrightarrow G
  $$

  satisfying on each triple intersection the cocycle condition

  $$
    g_{i j} g_{j k} = g_{i k}
  $$

* as [[morphisms]] the [[coboundaries]] between such cocycles $\{g_{i j}\}$ and $\{\tilde g_{j k}\}$, hence  collections of smooth functions 

  $$
    h_{i} \colon U_i \longrightarrow G
  $$

  such that on each intersection of charts

  $$
    g_{i j} h_j  = h_i \tilde g_{i j}
    \,.
  $$

In particular the [[connected components]] of the Hom-groupoid is hence the [[Cech cohomology]] itself:

$$ 
  \pi_0
  PreSmooth1Type(C(\{U_i\}), \mathbf{B}G)
  \simeq
  H^1_{Cech}(X,\{U_i\}; G)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The components of a morphism $C(\{U_i\})\longrightarrow \mathbf{B}G$ look as follows

$$
  \left(
    \array{
       && (x,j)
       \\
       & \nearrow && \searrow
       \\
      (x,i) &&\to&& (x,k)
    }
  \right)
  \mapsto
  \left(
    \array{
       && \bullet
       \\
       & {}^{\mathllap{g_{i j}(x)}}\nearrow
       && \searrow^{\mathrlap{g_{j k}(x)}}
       \\
      \bullet &&\stackrel{g_{i k}(x)}{\to}&& \bullet
    }
  \right)
  \,.
$$

This means that evaluating the morphism on the point $\ast = \mathbb{R}^0$, hence after forgetting the smooth structure, then it is a [[functor]] of groupoids as shown. Since $\mathbf{B}G(\mathbb{R}^0)$ has a single object, there is no choice for this functor on the level of objects. On morphisms it has to send each point $(x,i,j)$ in a double intersection of the cover to a group element $g_{i j}(x)\in G$. Hence the functor is given by functions

$$
  ( g_{i j} )_{i,j \in I} \colon \underset{i,j}{\coprod} U_i \underset{X}{\times} U_j \longrightarrow G
  \,.
$$ 

The [[Yoneda lemma]] gives that these must be [[smooth functions]] (as discussed at _[[geometry of physics -- smooth sets]]_). Finally functoriality says that composition on the left needs to be taken to composition on the right, which means here that these functions satisfy

$$
  g_{i j}(x) g_{j k}(x) = g_{i k}(x)
$$

for all $(x,i,j)$. This is precisely the data of a $G$-valued [[Cech cohomology]] cocycle.

Similarly, a homotopy between two such morphisms $h \colon g \Rightarrow \tilde g$ is in components a [[natural transformation]] of the form

$$
  \array{
    (x,i)
    \\
    \downarrow
    \\
    (x,j)
  }
  \;\;\;
  \mapsto
  \;\;\;
  \array{
     \bullet &\stackrel{h_i(x)}{\longrightarrow}& \bullet
     \\
     {}^{\mathllap{g_{i j}(x)}}\downarrow && \downarrow^{\mathrlap{\tilde g_{i j}(x)}}
     \\
     \bullet &\underset{h_j(x)}{\longrightarrow}& \bullet
  }
$$

hence is given by smooth functions

$$
  (h_i)_{i \in I} \colon \underset{i}{\coprod} U_i \longrightarrow G
$$

such that 

$$
  h_i(x) \tilde g_{i j}(x) = g_{i j}(x) h_j(x)
  \,.
$$

This is precisely the formula characterizing $(h_i)_{i \in I}$ as a Cech [[coboundary]].

=--

More along these lines is at _[[geometry of physics -- principal bundles]]_.


#### Gluing 
 

The "bootstrap"-definition of pre-smooth groupoids [above](#PreSmoothGroupoids) works as intended, by prop. \ref{YonedaForPreSmoothGroupoids}, it just needs to be restricted now to something a little less general. The issue is that while this definition consistently identifies a smooth-structure-to-be by what its possible smooth probes are, it does not enforce yet the consistent _gluing_ of probes:

for $X$ a pre-smooth groupoid, then given a probe of it of the form $\sigma \colon \mathbb{R}^n \to X$ and given a [[covering]] $\{U_i \to \mathbb{R}^n\}$ of the probe space by other probe spaces $U_i \simeq \mathbb{R}^n$, then it should be possible to reconstruct $\sigma$ from knowing its restrictions $\sigma_{|U_i}\colon U_i \to X$ to these charts, and the information of how these are identified by gauge transformations on double overlaps.

Such a system of local data and of gauge identification on double overlaps is just what maps out of the Cech groupoid $C(\{U_i\})$, def. \ref{GroupoidOfCover}, encode. This is shown by prop. \ref{CechCoyclesAsSmoothMaps} for the case that $X$ is of the form $(\mathbf{B}G)_\bullet$, example \ref{DeloopedGroupAsPreSmoothGroupoid}, but this is already the archetypical case. 

In other words, the condition that smooth probes of $X$ by coordinate charts $\mathbb{R}^n$ glue along covers $\{U_i \to \mathbb{R}^n\}$ of these charts is the condition that the groupoid of smooth maps out of $\mathbb{R}^n$ itself

$$
  \mathbb{R}^n \longrightarrow X
$$

is equivalent to the groupoid of maps out of the Cech groupoid of any cover

$$
  C(\{U_i\}) \longrightarrow X
$$

and is so via the "restriction" map that takes the former and precomposes it with the canonical map $C(\{U_i\}) \to \mathbb{R}^n$.

$$
  \array{
    C(\{U_i\}) &\longrightarrow& X
    \\
    \downarrow & \nearrow
    \\
    \mathbb{R}^n
  }
  \,.
$$


+-- {: .num_defn #DescentForPreSmoothGroupoids}
###### Definition

A pre-smooth groupoid $X \in PreSmooth1Type$, def. \ref{PreSmoothGroupoid}, _satisfies descent_ if for all $n \in \mathbb{N}$ and for all differentiably [[good open covers]] $\{U_i \to \mathbb{R}^n\}$ of the $n$-dimensional abstract [[coordinate chart]], the functor

$$
  X(\mathbb{R}^n) \simeq PreSmooth1Type(\mathbb{R}^n, X)
  \longrightarrow
  PreSmooth1Type(C(\{U_i\}),X)
$$

given by pre-composition with $C(\{U_i\}) \to \mathbb{R}^n$, is an [[equivalence of groupoids]].

=--

+-- {: .num_remark}
###### Remark

The condition in def. \ref{DescentForPreSmoothGroupoids} is called the _stack condition_, or the condition of _[[descent]]_, alluding to the fact that it says that $X$ "descends" down along the cover projection. So a smooth groupoid is a _[[stack]]_ on the [[site]] [[CartSp]]. This is a higher analog of the [[sheaf]] condition (see the next example) and hence a more systematic terminology would be to say that such $X$ is a _[[2-sheaf]]_ or rather a _[[(2,1)-sheaf]]_ (since it takes values in [[groupoids]] as opposed to in more general [[categories]]).

=--

+-- {: .num_prop}
###### Proposition

Let $X \in PreSmooth0Type \hookrightarrow PreSmooth1Type$ be a pre-smooth groupoid which is really just a pre-smooth set, hence a presheaf on $CartSp$ that takes values in groupoids with only identity morphisms

$$
  X \colon CartSp^{op} \longrightarrow Set \hookrightarrow Grp
  \,.
$$ 

Then $X$ is a smooth groupoid in the sense of def. \ref{DescentForPreSmoothGroupoids} precisely if it is a [[smooth set]], hence precisely if, as a presheaf, it satisfies the [[sheaf]] condition.

=--

+-- {: .num_example #SmoothManifoldsSatisfyDescentAsPreSmoothGroupoids}
###### Example

In particular, for $X \in SmoothMfd \hookrightarrow PreSmooth0Type \hookrightarrow PreSmooth1Type$ a [[smooth manifold]], it satisfies descent as a pre-smooth groupoid.

=--


+-- {: .num_remark}
###### Remark

There is an alternative formulation of the whole theory where instead of the [[site]] [[CartSp]] one uses the site [[SmoothMfd]] of all [[smooth manifolds]]. Everything discussed so far goes through verbatim for that site, too, but the [[descent]] condition in def. \ref{DescentForPreSmoothGroupoids} is a much stronger condition.

For instance the presheaves of the form $(\mathbf{B}G)_\bullet = (G \stackrel{\longrightarrow}{\longrightarrow} \ast)$ from example \ref{DeloopedGroupAsPreSmoothGroupoid} satisfy descent on $CartSp$, but not all $SmoothMfd$. Still, once we have defined the higher category of smooth groupoids, the definition will be equivalent for both choices of sites. 

The choice of the smaller site is the one that is easier to work with, and therefore we stick with that. In fact, most every example of a pre-smooth groupoid that one runs into satisfies descent on $CartSp$.

=--

For example:

+-- {: .num_prop #bfBGbulletSatisfiesDescent}
###### Proposition

For $G$ a [[Lie group]], then the pre-smooth [[delooping]] groupoid
$(\mathbf{B}G)_\bullet$ of example \ref{DeloopedGroupAsPreSmoothGroupoid}
satisfies descent on $CartSp$, def. \ref{DescentForPreSmoothGroupoids}.

=--

+-- {: .proof}
###### Proof

For $\{U_i \to \mathbb{R}^n\}$ a differentiably good open cover,
then by prop. \ref{CechCoyclesAsSmoothMaps} the groupoid
$PreSmooth1Type(C(\{U_i\}),(\mathbf{B}G)_\bullet)$
is the groupoid of [[Cech cohomology|Cech 1-cocycles and coboundaries]]
with coeffcients in $G$ on $\mathbb{R}^n$ relative to the cover.
But this is equivalently the groupoid of $G$-principal bundles
on $\mathbb{R}^n$. Now because the underlying [[topological space]]
of $\mathbb{R}^n$ is [[contractible topological space|contractible]],
all $G$-principal bundles on it are equivalent to the trivial one. 
But this is evidently represented by the image of point
under the map

$$
  B (C^\infty(G)_{disc})
  \simeq
  PreSmooth1Type(\mathbb{R}^n, (\mathbf{B}G)_\bullet)
  \longrightarrow
  PreSmooth1Type(C(\{U_i\}), (\mathbf{B}G)_\bullet)
  \,.
$$

Therefore this is an [[essentially surjective functor]] of groupoids.
Moreover, the [[automorphisms]] of the trivial $G$-principal bundles
are precisely the smooth $G$-functions, hence this is also 
a [[fully faithful functor]] of groupoids. Accordingly it is 
an [[equivalence]] of groupoids.

=--

The same argument however shows that on the larger site [[SmoothMfd]] this object does not satisfy descent. Put positively, this is the content of prop. \ref{StackMapsFromXtoDeloopingOfG}. below.





#### Weak equivalences

While the morphisms of pre-smooth groupoids defined above correctly encode
morphisms of smooth structures (by taking smooth probes compatibly to smooth probes),
they are not sensitive enough yet to the required concept of [[equivalence]].
This is because smooth structure, being about existence of [[differentiation]],
is to be detected entirely locally, namely [[stalk]]-wise. If for instance $X$ is a [[smooth manifold]], then its smooth structure is determined, around any of its points, by the smooth structure of an arbitrarily small [[open ball]] around that point.

+-- {: .num_defn #Stalks}
###### Definition

For $n \in \mathbb{N}$, and $0 \lt r \lt 1 \in \mathbb{R}$ let 

$$
  \mathbb{R}^n \simeq D^n_r \hookrightarrow \mathbb{R}^n
$$

be the [[smooth function]] that regards the [[Cartesian space]] $\mathbb{R}^n$ as the standard $n$-[[disk]] of [[radius]] $r$ around the origin in $\mathbb{R}^n$. 

For $X \in PreSmooth1Type$ we write

$$
  (D^n)^* X \coloneqq {\underset{\longrightarrow_r}{\lim}} X(D^n_r) \in Grpd
$$

for the [[colimit]] (in the 1-category of groupoids) of the restrictions of its groupoids of plots along the inclusion of these open balls -- the _$n$-[[stalk]]_ of $X$. This extends to a [[functor]]

$$
  (D^n)^* \colon PreSmooth1Type \longrightarrow Grpd
$$

=--

This means that objects in $(D^n)^\ast X$ are [[equivalence classes]] of pairs $(r,x_r)$ where $0 \lt r \lt 1$ and where $x_r \in X(D^n_r)$, with two such pairs being equivalent $(r_1, x_{r_1})\sim (r_2, x_{r_2})$ precisely if there is $r_0 \lt r_1,r_2$ such that $x_{r_1}$ becomes equal to $x_{r_2}$ after restriction to $D^n_{r_0}$.

+-- {: .num_defn #LocalWeakEquivalence}
###### Definition

A morphism $f \colon X \longrightarrow Y$ of pre-smooth groupoids, def. \ref{HomGroupoidsOfPreSmoothGroupoids}, is called a 
_local [[weak equivalence]]_ if for every $n \in \mathbb{N}$
the $n$-stalk, def. \ref{Stalks}, is an [[equivalence of groupoids]]

$$
  ((D^n)^* f) \colon (D^n)^* X \stackrel{}{\longrightarrow} (D^n)^* Y
  \,.
$$

=--

We write $X\stackrel{\simeq}{\longrightarrow} Y$ for local
weak equivalences of pre-smooth groupoids. We will mostly just say
_weak equivalence_ for short.


+-- {: .num_prop #CoveringMapIsLocalWeakEquivalence}
###### Proposition

For $X$ a [[smooth manifold]] and $\{U_i \to X\}$ an [[open cover]] for it, then 
the canonical morphism from the corresponding [[Cech groupoid]] to $X$, 
def. \ref{GroupoidOfCover}, is a local weak equivalence in the sense of
def. \ref{LocalWeakEquivalence}.

=--

+-- {: .proof}
###### Proof

The $n$-stalk of the smooth manifold $X$ regarded as a presheaf is the set of equivalence classes of maps from open pointed $n$-disks into it, where two such are identified if they coincide on some small joint sub-disk of their domain. We may call this the set of _[[germs]]_ of $X$ (but beware that this terminology is typically used for something a little bit more restrictive, namely for the case that $n$ is the dimension of $X$ and that all maps from the disks into $X$ are required to be [[embeddings]]).

On the other hand the $n$-stalk of $C(\{U_i\})$ is the groupoid whose set of objects is the set of germs, in this sense, of the disjoint union $\underset{i}{\coprod} U_i$, and whose set of morphisms is the set of germs of the disjoint union $\underset{i,j}{\coprod} U_i \underset{X}{\times} U_j$.

But now since the cover is by _[[open subset|open]]_ subsets, it follows that for every $(x,i,j) \in \underset{i,j}{\coprod} U_i \underset{X}{\times} U_j$, then every germ of objects $[g]$ around $(x,i)$  has a representative $g$ that factors through this double intersection charts:  $g \colon D^n_r \to U_i \underset{X}{\times} U_j \to \underset{i}{\coprod} U_u$. And similarly for $(x,j)$.

This means that the groupoid of $n$-stalks is a disjoint union of groupoids, one for each germ of $X$, all whose components are groupoids in which there is a unique morphism between any two objects, which are copies of this germ regarded as sitting in one of the charts of the cover. This means that each of these connected components is [[equivalence of groupoids|equivalent]] to the point.

Now the canonical cover projection sends each of these connected components to the germ that it corresponds to. Hence this is a an [[equivalence of groupoids]].

=--

#### Hypercovers

+-- {: .num_defn #SplitHypercover}
###### Definition

A morphism $p \colon Y \longrightarrow X$ of pre-smooth groupoids
is called a [[split hypercover]] if 

1. $Y$ is 

   1. degreewise a [[coproduct]] of [[Cartesian spaces]];

   1. such that the degenerate elements split off as a dijoint summand.

1. $p$ is a weak equivalence, def. \ref{LocalWeakEquivalence}.

=--

+-- {: .num_prop #GoodCechCoverIsSplitHypercover}
###### Proposition

For $X$ a [[smooth manifold]] and $\{U_i \to X\}$ an [[open cover]],
then the canonical projection $C(\{U_i\}) \to X$
from the corresponding [[Cech groupoid]], def. \ref{GroupoidOfCover},
is a split hypercover precisely if the cover is differentiably [[good open cover|good]].

=--

+-- {: .proof}
###### Proof

For every cover the map is a weak equivalence, by prop. \ref{CoveringMapIsLocalWeakEquivalence}.

For the Cech groupoid the condition of cofibrancy in def. \ref{SplitHypercover} means that every non-empty finite intersection of patches is [[diffeomorphism|diffeomorphic]] to a [[Cartesian space]], hence to an [[open ball]].
This is precisely the definition of differentialbly [[good open cover]].

=--




#### The $(2,1)$-category of smooth groupoids

The [[Grpd]]-[[enriched category]] of genuine smooth groupoids is that obtained from that of pre-smooth groupoids, def. \ref{HomGroupoidsOfPreSmoothGroupoids} by "universally turning local [[weak equivalences]], def. \ref{LocalWeakEquivalence}, into actual [[homotopy equivalences]]". This is stated formally by def. \ref{SmoothGroupoidsBySimplicialLocalization} below, but for many applications in practice certain concrete presentations of what this means concretely are well sufficient, one of these we state below in prop. \ref{HomGroupoidsOutOfCofibrantIntoFibrantGroupoidPresheaves}.

+-- {: .num_defn #SmoothGroupoidsBySimplicialLocalization}
###### Definition

Write 

$$
  Smooth1Type 
   \coloneqq
  L_{lwe} PreSmooth1Type
$$

for the [[(2,1)-category]] which is the [[simplicial localization]] of groupoid-valued presheaves at the local weak equivalences, def. \ref{LocalWeakEquivalence}.

An [[object]] $X \in Smooth1Type$ we call a **[[smooth groupoid]]** or
**[[smooth homotopy type|smooth homotopy 1-type]]**.

=--



+-- {: .num_prop #HomGroupoidsOutOfCofibrantIntoFibrantGroupoidPresheaves}
###### Proposition

Let $X,A \in PreSmooth1Type$ such that $A$ satisfies descent, 
def. \ref{DescentForPreSmoothGroupoids}. Let $Y \to X$
be a [[split hypercover]] of $X$, def. \ref{SplitHypercover}.

Then there is an [[equivalence of groupoids]]

$$
  Smooth1Type(X,A)
  \simeq
  PreSmooth1Type(Y,A)
$$

between the [[hom-groupoid]] of smooth groupoids from $X$ to $A$,
and that of pre-smooth groupoids, def. \ref{HomGroupoidsOfPreSmoothGroupoids},
from $Y$ to $A$.

=--

Such statements follow with [[model structures on simplicial presheaves]] after embedding the present situation in the more general context of [[smooth infinity-groupoids]]. See there for more.

+-- {: .num_remark #NotationForLocalization}
###### Remark

There is a canonical localization functor

$$
  PreSmooth1Type
  \longrightarrow
  L_{lwe} PreSmooth1Type
  =
  Smooth1Type
  \,.
$$

which is really just the identity as a functor. Instead of doing anything
to the objects, passing along this functor just means to change the
definition of the hom-groupoids from the direct definition of 
def. \ref{HomGroupoidsOfPreSmoothGroupoids} to the localized definition.

When a pre-smooth groupoid is given by an [[internal groupoid]]
$\mathcal{G}_\bullet$ in [[smooth sets]] via example \ref{ExternalYonedaEmbeddingsIntoPreSmooth1Type}, then we indicate its image under this functor by removing the subscript index, writing just $\mathcal{G}$.
This reflects the fact that in $Smooth1Type$ it no longer makes
sense to ask what the space of 0-cells and of 1-cells of an object is, as
these are concepts not invariant under local weak equivalence.

In particular this means that we write $\mathbf{B}G$ for the
image of $(\mathbf{B}G)_\bullet$ in $Smooth1Type$.

=--


+-- {: .num_prop #StackMapsFromXtoDeloopingOfG}
###### Proposition

Let $X$ be a [[smooth manifold]], regarded as a smooth 0-groupoid, and let $G$ be a [[Lie group]], with smooth [[delooping]] groupoid $\mathbf{B}G$ 
(example \ref{DeloopedGroupAsPreSmoothGroupoid}, remark \ref{NotationForLocalization}).

Then 

$$
  Smooth1Type(X,\mathbf{B}G)
  \simeq
  G Bund(X)
$$

is equivalently the [[groupoid]] of $G$-[[principal bundles]] on $X$.

=--

+-- {: .proof}
###### Proof

By prop. \ref{bfBGbulletSatisfiesDescent} the object
$(\mathbf{B}G)_\bullet$ satisfies descent on [[CartSp]].
Choose $\{U_i \to X\}$ a differentiably [[good open cover]].
By prop. \ref{GoodCechCoverIsSplitHypercover} the correspoding
[[Cech groupoid]] projection
$C(\{U_i\}) \to X$ is a [[split hypercover]], def. \ref{SplitHypercover}.
Hence, by prop. \ref{HomGroupoidsOutOfCofibrantIntoFibrantGroupoidPresheaves},
there is an [[equivalence of groupoids]]

$$
  Smooth1Type(X,\mathbf{B}G)
  \simeq
  PreSmooth1Type(C(\{U_i\}), (\mathbf{B}G)_\bullet)
  \,.
$$

The groupoid on the right is, by prop. \ref{CechCoyclesAsSmoothMaps},
the groupoid of [[Cech cohomology|Cech 1-cocycles and coboundaries]]
with values in $G$ relative to a good open cover. This is 
equivalently the groupoid of $G$-principal bundles.

=--


+-- {: .num_remark }
###### Remark

The content of prop. \ref{StackMapsFromXtoDeloopingOfG} is in 
common jargon that: _$\mathbf{B}G \in SmoothGrpd$ is the [[moduli stack]] of $G$-[[principal bundles]]".

=--





## Smooth $\infty$-Groupoids 

(...under construction...)

### Simplicial presheaves

We need structures a bit richer than just bare [[∞-groupoids]]. In generalization to [[Lie groupoid]]s, we need [[∞-Lie groupoid]]s. A useful way to encode that an $\infty$-groupoid has extra structure modeled on geometric test objects that themselves form a category $C$ is to remember the rule which for each test space $U$ in $C$ produces the $\infty$-groupoid of $U$-parameterized families of $k$-morphisms in $K$.  For instance for an [[∞-Lie groupoid]] we could test with each [[Cartesian space]] $U = \mathbb{R}^n$ and find the $\infty$-groupoids $K(U)$ of smooth $n$-parameter families of $k$-morphisms in $K$.

This data of $U$-families arranges itself into a [[presheaf]] with values in Kan complexes

$$
  K : C^{op} \to KanCplx \hookrightarrow sSet
$$

hence with values in simplicial sets. This is equivalently a [[simplicial presheaf]] of sets. The [[functor category]] $[C^{op}, sSet]$ on the [[opposite category]] of the category of test objects $C$ serves as a model for the [[(∞,1)-category]] of $\infty$-groupoids with $C$-structure.

While there are no [[higher morphism]]s in this functor 1-category that could for instance witness that two $\infty$-groupoids are not [[isomorphic]], but still [[equivalence of categories|equivalent]], it turns out that all one needs in order to reconstruct _all_ these higher morphisms (up to equivalence!) is just the information of which morphisms of simplicial presheaves would become invertible if we were keeping track of higher morphism. These would-be invertible morphisms are called _weak equivalences_ and denoted $K_1 \stackrel{\simeq}{\to} K_2$. 

For common choices of $C$ there is a well-understood way to define the weak equivalences $W \subset mor [C^{op}, sSet]$, and equipped with this information the category of simplicial presheaves becomes a _[[category with weak equivalences]]_ . There is a well-developed but somewhat intricate theory of how exactly this 1-cagtegorical data models the full higher category of structured groupoids that we are after, but for our purposes we essentially only need to work inside the [[category of fibrant objects]] of a [[model category]] structure [[model structure on simplicial presheaves|on simplicial presheaves]], which in practice amounts to the fact that we use the following three basic constructions:

1. **[[∞-anafunctor]]s** -- A morphisms $X \to Y$ between $\infty$-groupoids with $C$-structure is not just a morphism $X\to Y$ in $[C^{op}, sSet]$, but is a [[span]] of such ordinary morphisms

   $$
     \array{  
        \hat X &\to& Y
        \\
        \downarrow^{\mathrlap{\simeq}}
        \\
        X
     }
   $$

   where the left leg is a weak equivalence. This is sometimes called an _$\infty$-anafunctor_ from $X$ to $Y$.
 
1. **[[homotopy pullback]]** -- For $A \to B \stackrel{p}{\leftarrow} C$ a [[diagram]], the [[(∞,1)-pullback]] of it is the ordinary [[pullback]] in $[C^{op}, sSet]$ of a replacement diagram $A \to B \stackrel{\hat p}{\leftarrow} \hat C$, where $\hat p$ is a _good replacement_  of $p$ in the sense of the following factorization lemma.

1. **[[factorization lemma]]** -- For $p : C \to B$ a morphism in $[C^{op}, sSet]$, a _good replacement_ $\hat p : \hat C \to B$ is given by the composite vertical morphism in the ordinary [[pullback]] diagram

   $$
     \array{
       \hat C &\to& C
       \\
       \downarrow && \downarrow^{\mathrlap{p}}
       \\
       B^{\Delta[1]} &\to& B
       \\
       \downarrow
       \\
       B
     }
     \,,
   $$

  where $B^{\Delta[1]}$ is the [[path object]] of $B$: 
  the simplicial presheaf that is over each $U \in C$ the
  simplicial path space $B(U)^{\Delta[1]}$.

* [[simplicial presheaf]]

* [[model structure on simplicial presheaves]]

### Good covers and split hypercovers

* [[Cech nerve]]

* [[good open cover]]

* [[split hypercover]]

+-- {: .num_prop #DifferentiablyGoodCoverGivesSPlitHyperCoverOverCartSp}
###### Proposition

For $X$ a [[smooth manifold]] let $\{U_i \hookrightarrow X\}_i$ be an [[open cover]]. This is a _differentiably good open cover_, def. \ref{DifferentiallyGoodOpenCover}, precisely if the corresponding  [[Cech nerve]] $C(\{U_i\}) \to X$ in $sPh(CartSp)_{proj,loc}$ is a [[split hypercover]].

=--

## Examples

### Parallel transport
 {#1FormsAsSmoothFunctors}

We give a more intrinsic characterization of [[differential 1-forms]].

+-- {: .num_defn #SmoothPath}
###### Definition

A **smooth path with sitting instants** in $\mathbb{R}^k$ is a [[smooth function]] $\gamma \colon \mathbb{R} \to \mathbb{R}^k$ such 

1. the value of $\gamma$ converges to two points $x = \underset{t \to -\infty}{\lim} \gamma \in \mathbb{R}^k$ and $y = \underset{t \to \infty}{\lim} \gamma \in \mathbb{R}^k$;

1. the value of all [[derivatives]] of $\gamma$ converges to 0 at $t \to \pm \infty$.

A **localized diffeomorphism** $\phi \colon \mathbb{R} \to \mathbb{R}$ is a [[diffeomorphism]] such that there is an an open ball in $\mathbb{R}$ outside of which $\phi$ restricts to the identity.

Write

$$
  [\mathbb{R}, \mathbb{R}^k] // Diff(\mathbb{R}) 
  \in 
  Smooth0Type
$$

for the smooth quotient space of smooth paths modulo localized diffeomorphism.

=--

+-- {: .num_defn #SmoothFunctorOnPathsInRkWithValuesInBR}
###### Definition

Say that a **smooth functor** $\mathbf{P}_1(\mathbb{R}^k) \to \mathbf{B}\mathbb{R}$ from the [[smooth path groupoid]] of $\mathbb{R}^k$ is

* a [[homomorphism]] of smooth space 

  $$
    S \colon [\mathbb{R}, \mathbb{R}^k] \to \mathbb{R}
  $$

* such that 

  1. composition of paths $\gamma_1, \gamma_2$ is sent to addition in $\mathbb{R}$

     $$
       S(\gamma_2\circ \gamma_1) = S(\gamma_1) + S(\gamma_2)
       \,.
     $$
  
  1. the constant path is sent to 0.

=--

+-- {: .num_prop }
###### Proposition

There is an [[equivalence]]

$$
  [\mathbf{P}_1(-), \mathbf{B}\mathbb{R}]
  \stackrel{\overset{\int_{(-)}(-)}{\longleftarrow}}{\underset{}{\longrightarrow}}
  DK(C^\infty(-) \stackrel{\mathbf{d}}{\to} \Omega^1(-)
  \,.
$$

=--

([SchreiberWaldorf](#SchreiberWaldorf)).


### Lie integration of $\infty$-Lie algebroids
 {#LieIntegrationOfLInfinityAlgebroids}

In classical [[Lie theory]], a [[Lie group]] may be (re-)constructed from infinitesimal data, namely from its _[[Lie algebra]]_ by a process of [[Lie integration]]. We now discuss a procedure that constructs [[smooth homotopy types]]/[[smooth ∞-groupoids]] from [[Lie integration]] of infinitesimal data, namely from higher Lie algebras, called _[[L-∞ algebras]]_ and more generally from [[L-∞ algebroids]].

#### Lie algebras via their Chevalley-Eilenberg algebras

The quickest way to introduce [[L-∞ algebras]] of [[finite type]] is via theiry [[formal dual|formally dual]] [[Chevalley-Eilenberg dg-algebras]]. Here we recall how this works and then [below](#LInfinityAlgebroidsViaTheiryCEAlgebras) we use this to define [[L-∞ algebroids]] of [[finite type]].

+-- {: .num_defn #CEAlgebra}
###### Definition

The _[[Chevalley-Eilenberg algebra]]_ $CE(\mathfrak{g})$ of a finite dimensional [[Lie algebra]] $\mathfrak{g}$ is the [[semifree dga|semifree]] graded-commutative [[dg-algebra]] whose underlying graded algebra is the [[Grassmann algebra]] 

$$
  \wedge^\bullet \mathfrak{g}^*
  = 
  k \oplus \mathfrak{g}^* \oplus (\mathfrak{g}^* \wedge \mathfrak{g}^* ) \oplus \cdots
$$ 

(with the $n$th skew-symmetrized power in degree $n$)

and whose [[differential]] $d$ (of degree +1) is on $\mathfrak{g}^*$ the dual of the Lie bracket

$$
  d|_{\mathfrak{g}^*} := [-,-]^* : \mathfrak{g}^* \to \mathfrak{g}^* \wedge \mathfrak{g}^*
$$

extended uniquely as a graded [[derivation]] on $\wedge^\bullet \mathfrak{g}^*$.

That this differential indeed squares to 0, $d \circ d = 0$, is precisely the fact that the Lie bracket satisfies the [[Jacobi identity]].

=--

+-- {: .num_remark #CEAlgebraInTermsOfBasis}
###### Remark

If in the situation of prop. \ref{CEAlgebra} we choose a dual basis $\{t^a\}$ of $\mathfrak{g}^*$ and let $\{C^a{}_{b c}\}$ be the structure constants of the Lie bracket in that basis, then the action of the differential on the basis generators is

$$
  d t^a = - \frac{1}{2} C^a{}_{b c} t^b \wedge t^c
  \,,
$$

where here and in the following a sum over repeated indices is implicit.

=--

+-- {: .num_prop #CEIfFullyFaithful}
###### Proposition

The construction of Chevalley-Eilenberg algebras in def. \ref{CEAlgebra}
yields a [[fully faithful functor]]

$$
  CE(-)
  \colon
  LieAlg
  \longrightarrow
  dgAlg^{op}
$$

embedding [[Lie algebras]] into [[formal duals]] of [[differential graded algebras]]. Its image consists of precisely of the [[semifree dg-algebras]], those whose underlying [[graded algebra]] (forgetting the [[differential]]) is a [[Grassmann algebra]] generated on a [[vector space]].

=--

+-- {: .num_defn #WeilForLInfinitityAlgebra}
###### Definition

Given a [[Lie algebra]] $\mathfrak{g}$, its **[[Weil algebra]]** $W(\mathfrak{g})$ is the [[semi-free dga]] whose underlying graded-commutative algebra is the [[exterior algebra]]

$$
  \wedge^\bullet (\mathfrak{g}^* \oplus \mathfrak{g}^*[1])
$$

on $\mathfrak{g}^*$ and a shifted copy of $\mathfrak{g}^*$,
and whose [[differential]] is the sum

$$
  d_{W(\mathfrak{g})} = d_{CE(\mathfrak{g})} + \mathbf{d}
$$

of two graded [[derivations]] of degree +1 defined by

* $\mathbf{d}$ acts by degree shift $\mathfrak{g}^* \to \mathfrak{g}^*[1]$ on elements in $\mathfrak{g}^*$ and by 0 on elements of $\mathfrak{g}^*[1]$;

* $d_{CE(\mathfrak{g})}$ acts on unshifted elements in $\mathfrak{g}^*$ as the differential of the [[Chevalley-Eilenberg algebra]] of $\mathfrak{g}$ and is extended uniquely to shifted generators by graded-commutattivity 
 
  $$
    [d_{CE(\mathfrak{g}}, \mathbf{d}] = 0
  $$

  with $\mathbf{d}$:

  $$
    d_{CE(\mathfrak{g})} \mathbf{d} \omega :=
    - \mathbf{d} d_{CE(\mathfrak{g})} \omega
  $$

  for all $\omega \in \wedge^1 \mathfrak{g}^*$.

=--



+-- {: .num_prop #LieAlgValuedFormsViaDgAlgHoms}
###### Proposition

Given a [[Lie algebra]] $\mathfrak{g}$, then 
a [[Lie algebra valued differential form]] on, say, 
a [[Cartesian space]] $\mathbb{R}^n$, is 
equivalently a dg-algebra homomorphims

$$
  \Omega^\bullet(\mathbb{R}^p)
  \longleftarrow
  W(\mathfrak{g})
  \colon
  A
  \,,
$$ 

hence there is a [[natural bijection]]

$$
  \Omega^1(\mathbb{R}^p, \mathfrak{g})
  \simeq
  Hom_{dgAlg}(W(\mathfrak{g}), \Omega^\bullet(\mathbb{R}^p))
  \,.
$$

The form $A$ is _flat_ in that its [[curvature]] [[differential 2-form]] $F_A$ vanishes, precisely if this morphism factors through the CE-algebra. 

=--

+-- {: .num_remark}
###### Remark

With a choice of basis as in remark \ref{CEAlgebraInTermsOfBasis}, then the content of prop. \ref{LieAlgValuedFormsViaDgAlgHoms} is seen in components as follows:

a dg-algebra homomorphism is first of all a homomorphism of [[graded algebras]], and since the domain $W(\mathfrak{g})$ is free as a graded algebra, such is entirely determined by what it does to the generators

$$
  \array{
    t^a, &\mapsto& A^a & \in \Omega^1(\mathbb{R}^n)
    \\ 
    r^a &\mapsto& F^a & \in \Omega^2(\mathbb{R}^n)
  }
  \,.
$$

But being a dg-algebra homomorphism, this assignment needs to respect the differentials on both sides. For the original generators this gives

$$
  \array{
    t^a &\mapsto&&&  A^a
    \\
    \downarrow^{\mathrlap{d_{W(\mathfrak{g})}}} &&&& \downarrow^{\mathrlap{\mathbf{d}_{dR}}}
    \\
    - \frac{1}{2} C^a{}_{b c} t^b \wedge t^c
    + r^a
    &\mapsto&
    (- \frac{1}{2} C^a{}_{b c} A^b \wedge A^c + F^a)
    &=&
    \mathbf{d}_{dR} A^a 
  }
  \,.
$$

With this satisfied, then, by the very nature of the [[Weil algebra]],
the differential is automatically respected also on the shifted generators. This statement is the _[[Bianchi identity]]_.

=--

#### $L_\infty$-Algebroids via their Chevalley-Eilenberg algebras
 {#LInfinityAlgebroidsViaTheiryCEAlgebras}

+-- {: .num_defn }
###### Definition

The [[category]] of [[L-∞ algebras]] of _[[finite type]]_ is 
the [[full subcategory]] of that of the [[opposite category]] of [[dg-algebras]]

$$
  CE(-)
  \;\colon\;
  L_\infty Alg 
   \hookrightarrow
  dgAlg^{op}
$$

$$
  (\mathfrak{g}, [-],[-,-], [-,-,-],\cdots)
  \mapsto
  (\wedge^\bullet \mathfrak{g}^\ast , d_{CE} = [-]^\ast + [-,-]^\ast + [-,-,-]^\ast + \cdots)
$$

on those whose underlying [[graded algebra]] is the [[Grassmann algebra]] $\wedge^\bullet \mathfrak{g}$ on a $\mathbb{N}$-[[graded vector space]] $\mathfrak{g}$ of [[finite type]].

More generally, the [[category]] [[L-∞ algebroids]] is the [[full subcategory]]

$$
  CE(-)
  \;\colon\;
  L_\infty Algd 
   \hookrightarrow
  dgAlg^{op}
$$

on those dg-algebras (over $\mathbb{R}$)

$$
  (\mathfrak{a}_X, [-],[-,-], [-,-,-],\cdots)
  \mapsto
  (\wedge^\bullet_{C^\infty(X)} \mathfrak{a}^\ast , d_{CE} = [-]^\ast + [-,-]^\ast + [-,-,-]^\ast + \cdots)
$$

whose underlying graded algebra is the [[Grassmann algebra]] over $C^\infty(X)$ of an $\mathbb{N}$-graded [[projective module]] $\mathfrak{a}$ of [[finite type]] over $C^\infty(X)$ (i.e. by the [[Serre-Swan theorem]], of [[sections]] of  an $\mathbb{N}$-graded [[vector bundle]]).
 
=--


#### $\infty$-Lie algebroid valued differential forms 


For $X$ a [[smooth manifold]] and $\mathfrak{g}$ an [[∞-Lie algebra]] or more generally an [[∞-Lie algebroid]], a  **[[∞-Lie algebroid valued differential forms]]** on $X$ is a morphism of [[dg-algebra]]s

$$
  \Omega^\bullet(X)
  \leftarrow
  W(\mathfrak{g})
  : 
  A
$$

from the [[Weil algebra]] of $\mathfrak{g}$ to the [[de Rham complex]] of $X$. Dually this is a morphism of [[∞-Lie algebroid]]s

$$
  A : T X \to inn(\mathfrak{g})
$$

from the [[tangent Lie algebroid]] to the [[Weil algebra|inner automorphism ∞-Lie algebra]].

Its [[curvature]] is the composite of morphisms of [[graded vector space]]s

$$
  \Omega^\bullet(X) \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{F_{(-)}}{\leftarrow}
  \wedge^1 \mathfrak{g}^*
  : 
  F_{A}
  \,.
$$

Precisely if the curvatures vanish does the morphism factor through the [[Chevalley-Eilenberg algebra]] $W(\mathfrak{g}) \to CE(\mathfrak{g})$.

$$
  (F_A = 0) 
  \;\;\Leftrightarrow
  \;\;
  \left(
  \array{
     && CE(\mathfrak{g})
     \\
     & {}^{\mathllap{\exists A_{flat}}}\swarrow & \uparrow
     \\
     \Omega^\bullet(X) &\stackrel{A}{\leftarrow}& W(\mathfrak{g})     
  }
  \right)
$$

in which case we call $A$ **flat**.




#### Higher dimensional paths in an $\infty$-Lie algebroid
 {#HigherPathsInAnInfinityLieAlgebroid}


+-- {: .num_example}
###### Example

For $X$ a [[smooth manifold]] (possibly [[nLab:manifold with boundary|with boundary]] and [[manifold with corners|with corners]]) then its [[tangent Lie algebroid]] $T X$ is the one whose [[Chevalley-Eilenberg algebra]] is the [[de Rham complex]] 

$$
  CE(T X) = (\Omega^\bullet(X), d_{dR})
  \,.
$$

=--

+-- {: .num_defn #kPath}
###### Definition

For $k \in \mathbb{N}$ write $\Delta^k$ for the standard $k$-[[simplex]] regarded as a [[smooth manifold]] ([[nLab:manifold with boundary|with boundary]] and [[manifold with corners|with corners]]).  

A **$k$-path** in the $\infty$-Lie algebroid $\mathfrak{a}$ is a morphism of $\infty$-Lie algebroids of the form

$$
  \Sigma \; \coloneqq \; T \Delta^k \longrightarrow \mathfrak{a}
$$ 

from the [[tangent Lie algebroid]] $T \Delta^k$ of the standard smooth $k$-simplex to $\mathfrak{a}$. Dually this is equivalently a [[homomorphism]] of [[dg-algebras]]

$$
  \Omega^\bullet(\Delta^k) \longleftarrow CE(\mathfrak{a}) \;\colon\; \Sigma^*
$$

from the [[Chevalley-Eilenberg algebra]] of $\mathfrak{a}$ to the [[de Rham complex]] of $\Delta^d$.

=--

See also at _[[differential forms on simplices]]_.

+-- {: .num_remark}
###### Remark

A $k$-path in $\mathfrak{a}$, def. \ref{kPath}, is equivalently 

1. a _flat_ $\mathfrak{a}$-[[infinity-Lie algebroid valued differential form|valued differential form]] on $\Delta^k$;

1. a [[Maurer-Cartan element]] in $\Omega^\bullet(\Delta^k)\otimes \mathfrak{a}$.

=--

The Lie integration of $\mathfrak{a}$ is essentially the [[simplicial object]] whose $k$-cells are the $d$-paths in $\mathfrak{a}$. However, in order for this to be well-behaved, it is possible and useful to restrict to $d$-paths that are sufficiently well-behaved towards the [[boundary]] of the simplex:

+-- {: .num_defn}
###### Definition

Regard the smooth simplex $\Delta^k$ as embedded into the [[Cartesian space]] $\mathbb{R}^{k+1}$ in the standard way, and equip $\Delta^k$ with the [[metric space]] structure induced this way.

A smooth [[differential form]] $\omega$ on $\Delta^k$ is said to have **sitting instants** along the boundary if, for every $(r \lt k)$-face $F$ of $\Delta^k$ there is an [[open neighbourhood]] $U_F$ of $F$ in $\Delta^k$ such that $\omega$ restricted to $U$ is constant in the directions perpendicular to the $r$-face on its value restricted to that face.

More generally, for any $U \in $ [[CartSp]] a smooth differential form $\omega$ on $U \times\Delta^k$ is said to have sitting instants if there is $0 \lt \epsilon \in \mathbb{R}$ such that for all points $u : * \to U$ the pullback along  $(u, \mathrm{Id}) : \Delta^k \to U \times \Delta^k$ is a form with sitting instants on $\epsilon$-[[open neighbourhood|neighbourhood]]s of faces.

Smooth forms with sitting instants clearly form a sub-dg-algebra of all smooth forms. We write $\Omega^\bullet_{si}(U \times \Delta^k)$ for this sub-dg-algebra.

We write $\Omega_{si,vert}^\bullet(U \times \Delta^k)$ for the further sub-dg-algebra of [[vertical differential form]]s with respect to the projection $p : U \times \Delta^k \to U$, hence the [[coequalizer]]

$$
  \Omega^\bullet(U)
  \stackrel{\stackrel{p^*}{\longrightarrow}}{\underset{0}{\longrightarrow}}
  \Omega^\bullet_{si}(U \times \Delta^k)
  \to
  \Omega^\bullet_{si, vert}(U \times \Delta^k)  
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The dimension of the normal direction to a face depends on the dimension of the face:  there is one perpendicular direction to a codimension-1 face, and $k$ perpendicular directions to a
vertex. 

=--

+-- {: .num_example}
###### Examples

* A smooth 0-form (a [[smooth function]]) has sitting instants on $\Delta^1$ if in a neighbourhood of the endpoints it is constant.

  A smooth function $f : U \times \Delta^1 \to \mathbb{R}$ is in $\Omega^0_{\mathrm{vert}}(U \times \Delta^1)$ if there is $0 \lt \epsilon \in \mathbb{R}$ such that for each $u \in U$ the function $f(u,-) : \Delta^1  \simeq [0,1] \to \mathbb{R}$ is constant on $[0,\epsilon) \coprod (1-\epsilon,1)$.

* A smooth 1-form has sitting instants on $\Delta^1$ if in a neighbourhood of the endpoints it vanishes.

* Let $X$ be a [[smooth manifold]], $\omega \in \Omega^\bullet(X)$ be a smooth differential form. Let 

  $$
    \phi \colon \Delta^k \to X
  $$

  be a [[smooth function]] that has [[sitting instants]] as a function: towards any $j$-face of $\Delta^k$ it eventually becomes perpendicularly constant.

  Then the [[pullback of differential forms|pullback]] form $\phi^* \omega \in \Omega^\bullet(\Delta^k)$ is a form with sitting instants.

=--

+-- {: .num_remark}
###### Remark

The condition of sitting instants serves to make smooth differential forms not be affected by the boundaries and corners of $\Delta^k$. Notably for $\omega_j \in \Omega^\bullet(\Delta^{k-1})$ a collection of forms with sitting instants on the $(k-1)$-cells of a [[horn]] $\Lambda^k_i$ that coincide on adjacent boundaries, and for

$$
  p \colon \Delta^k \to \Lambda^{k-1}_i
$$

a standard piecewise smooth [[retract]], the [[pullback of differential forms|pullbacks]]

$$
  p^* \omega_i 
$$

glue to a single smooth differential form (with sitting instants) on $\Delta^k$.

=--

+-- {: .num_remark}
###### Remark

That $\omega \in \Omega^\bullet(\Delta^k)$ having sitting instants does not imply that there is a neighbourhood of the boundary of $\Delta^k$ on which $\omega$ is entirely constant. It is important for the following constructions that in the vicinity of the boundary $\omega$ is allowed to vary parallel to the boundary, just not perpendicular to it.

=--


#### Higher Lie integration

_[[Lie integration]]_ is a process that assigns to a [[Lie algebra]] $\mathfrak{g}$ -- or more generally to an [[L-∞-algebra|∞-Lie algebra]] or [[∞-Lie algebroid]] -- a [[Lie group]] -- or more generally [[∞-Lie groupoid]] -- that is [[infinitesimal space|infinitesimally]] modeled by $\mathfrak{g}$. It is essentially the reverse operation to [[Lie differentiation]], except that there are in general several objects Lie integrating a given Lie algebraic datum, due to the fact that the infinitesimal data does not uniquely determine global topological properties.

Classically, Lie integration of [[Lie algebras]] is part of [[Lie's three theorems]], which in particular finds an unique (up to [[isomorphism]]) [[simply connected]] Lie group integrating a given finite-dimensional Lie algebra. 

One may observe that the [[simply connected]] [[Lie group]] integrating a (finite-dimensional) Lie algebra is equivalently realized as the collection of [[equivalence classes]] of [[Lie algebra valued 1-forms]] on the interval where two such are identified if they are interpolated by a _flat_ Lie-algebra valued 1-form on the [[disk]]. ([Duistermaat-Kolk 00, section 1.14](Lie+integration#DuistermaatKolk00), see also the example [below](Lie+intgeration#LieAlgebrasToLieGroups)). 

This _path method_ of Lie integration stands out as having natural generalizations to [[higher Lie theory]] ([&#352;evera 01](Lie+integration#Severa01)).  

In its evident generalization from [[Lie algebra valued differential forms]] to [[Lie algebroid valued differential forms]] this provides a means for Lie integration of [[Lie algebroids]] (e.g. [Crainic-Fernandes 01](Lie+integration#Crainic)).

In another direction, one may observe that [[L-∞ algebras]] are [[formal dual|formally dually]] incarnated by their [[Chevalley-Eilenberg algebra|Chevalley-Eilenberg]] [[dg-algebras]], and that under this identification the evident generalization of the path method to [[L-∞ algebra valued differential forms]] is essentially the [[Sullivan construction]], known from [[rational homotopy theory]], applied to these dg-algebras ([Hinich 97](Lie+integration#Hinich97), [Getzler 04](Lie+integration#Getzler04)). Or rather, the bare such construction gives the [[geometrically discrete ∞-groupoid|geometrically discrete]] [[∞-group]] underlying what should be the Lie integration to a [[smooth ∞-group]]. This is naturally obtained, as in the classical case, by suitably smoothly parameterizing the [[∞-Lie algebroid valued differential forms]] ([Henriques 08](Lie+integration#Henriques), [Roytenberg 09](Lie+integration#Roytenberg09), [FSS 12](Lie+integration#FSS12)).

Both these directions may be combined via the evident concept of [[∞-Lie algebroid valued differential forms]] to yield a Lie integration of [[∞-Lie algebroids]] to [[smooth ∞-groupoids]].

While the construction exists and behaves as expected in examples, there is to date no good general theory providing higher analogs of, say, [[Lie's three theorems]]. But people are working on it.


Let $\mathfrak{a}$ be an [[∞-Lie algebroid]] (for instance a [[Lie algebra]], or a [[Lie algebroid]] or an [[L-∞-algebra]]). 

For $\mathfrak{a}$ an $\infty$-Lie algebroid, the $d$-paths in $\mathfrak{a}$ naturally form a [[simplicial set]] as $d$ varies:

$$
  \begin{aligned}
    \exp(\mathfrak{a})_{bare}
    & \coloneqq
    \left(
     \cdots    
     Hom_{\infty LieAlgd}(T \Delta^2, \mathfrak{a})
     \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
     Hom_{\infty LieAlgd}(T \Delta^1, \mathfrak{a})
     \stackrel{\longrightarrow}{\longrightarrow}
     Hom_{\infty LieAlgd}(T \Delta^0, \mathfrak{g})
    \right)
     \\
    & =
   (
   \cdots 
   Hom_{dgAlg}(CE(\mathfrak{a}), \Omega^\bullet(\Delta^2))
   \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
   Hom_{dgAlg}(CE(\mathfrak{a}), \Omega^\bullet(\Delta^1))
   \stackrel{\longrightarrow}{\longrightarrow}
   Hom_{dgAlg}(CE(\mathfrak{a}), \Omega^\bullet(\Delta^0))
   )
  \end{aligned}
  \,.
$$

(We are indicating only the face maps, not the degeneracy maps, just for notational simplicity).

If here instead of smooth differential forms one uses [[polynomial differential forms]] then this is precisely the [[Sullivan construction]] of [[rational homotopy theory]] applied to $CE(\mathfrak{a})$. We next realize [[smooth structure]]  on this and hence realize this as an object in [[higher Lie theory]].



We now discuss Lie integration of $\infty$-Lie algebroids to [[smooth ∞-groupoid]]s, [[presentable (∞,1)-category|presented]] by the [[model structure on simplicial presheaves]] $[CartSp_{smooth}^{op}, sSet]_{proj,loc}$ over the [[site]] [[CartSp]]${}_{smooth}$.

For the following definition recall the [[presentable (∞,1)-category|presentation]] of [[smooth ∞-groupoids]] by the [[model structure on simplicial presheaves]] over the [[site]] [[CartSp]]${}_{smooth}$. 

+-- {: .num_defn}
###### Definition

For $\mathfrak{a}$ an [[L-∞ algebra]] of [[finite type]] with [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ define the [[simplicial presheaf]] 

$$
  \exp(\mathfrak{a}) \;\colon\; CartSp_{smooth}^{op} \to sSet
$$

by

$$  
  \exp(\mathfrak{a})
  \;\colon\;
  (U,[k]) \mapsto 
  Hom_{dgAlg}(CE(\mathfrak{a}), 
  \Omega^\bullet(U \times \Delta^k)_{si,vert})
  \,,
$$


for all $U \in $ [[CartSp]] and $[k] \in \Delta$. 

=--

+-- {: .num_remark}
###### Remark

Compared to the integration to [[discrete ∞-groupoids]] [above](#IntToBareGrpd) this definition knows about $U$-parametrized _smooth families_ of $k$-paths in $\mathfrak{g}$.

The underlying [[discrete ∞-groupoid]] is recovered as that of the $\mathbb{R}^0 = *$-parameterized family:

$$
  \exp(\mathfrak{a}) \colon \mathbb{R}^0 \mapsto \exp(\mathfrak{a})_{disc}
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The objects $\exp(\mathfrak{g})$ are indeed [[Kan complexes]] over each $U \in $ [[CartSp]].

=--

+-- {: .proof}
###### Proof

Observe that the standard [[continuous function|continuous]] [[horn]] [[retracts]] $f : \Delta^k \to \Lambda^k_i$ are [[smooth function|smooth]] away from the preimages of the $(r \lt k)$-faces of $\Lambda[k]^i$.

For $\omega \in \Omega^\bullet_{si,vert}(U \times \Lambda[k]^i)$ a differential form with sitting instants on $\epsilon$-neighbourhoods, let therefore $K \subset \partial \Delta^k$ be the set of points of distance $\leq \epsilon$ from any subface. Then we have a smooth function 

$$
  f : \Delta^k \setminus K \to \Lambda^k_i \setminus K
  \,.
$$

The [[pullback of differential forms|pullback]] $f^* \omega \in \Omega^\bullet(\Delta^k \setminus K)$ may be extended constantly back to a form with sitting instants on all of $\Delta^k$. 

The resulting assignment

$$
  (CE(\mathfrak{g}) \stackrel{A}{\longrightarrow} \Omega^\bullet_{si,vert}(U \times \Lambda^k_i))
  \mapsto
  (CE(\mathfrak{g}) \stackrel{A}{\to} \Omega^\bullet_{si,vert}(U \times \Lambda^k_i) \stackrel{f^*}{\to} \Omega^\bullet_{si,vert}(U \times \Delta^n))

$$


provides fillers for all [[horns]] over all $U \in $ [[CartSp]].

=--

+-- {: .num_defn}
###### Definition

Write $\mathbf{cosk}_{n+1} \exp(a)$ for the simplicial presheaf obtained by postcomposing $\exp(\mathfrak{a}) : CartSp^{op} \to sSet$ with the $(n+1)$-[[coskeleton]] [[functor]] $\mathbf{cosk}_{n+1} : sSet \stackrel{tr_n}{\longrightarrow} sSet_{\leq n+1} \stackrel{cosk_{n+1}}{\to} sSet$.

=--


#### Interating Lie algebras to Lie groups 
 {#LieAlgebrasToLieGroups}

Let $\mathfrak{g} \in L_\infty$ be an ordinary (finite dimensional) [[Lie algebra]]. Standard [[Lie theory]] (see [[Lie's three theorems]]) provides a [[simply connected]] [[Lie group]] $G$ integrating $\mathfrak{g}$.

With $G$ regarded as a [[smooth ∞-groupoid|smooth ∞-group]] write $\mathbf{B}G \in $ [[Smooth∞Grpd]] for its [[delooping]]. The standard presentation of this on $[CartSp_{smooth}^{op}, sSet]$ is by the [[simplicial presheaf]] 

$$
  \mathbf{B}G_c : U \mapsto N(C^\infty(U,G) \stackrel{\to}{\to} *)
  *
  \,.
$$


See <a href="http://ncatlab.org/nlab/show/smooth+infinity-groupoid#LieGroups">Cohesive ∞-groups -- Lie groups</a> for details.

+-- {: .num_prop}
###### Proposition

The operation of [[parallel transport]] $P \exp(\int -) : \Omega^1([0,1], \mathfrak{g}) \to G$ yields a weak equivalence (in $[CartSp^{op}, sSet]_{proj}$)

$$
  P \exp(\int - )
  :
  \mathbf{cosk}_3 \exp(\mathfrak{g}) 
  \simeq 
   \mathbf{cosk}_2 \exp(\mathfrak{g}) \simeq \mathbf{B}G_c
  \,.
$$

=--


This follows from the [[Steenrod-Wockel approximation theorem]] and the following observation.

+-- {: .num_lemma}
###### Lemma

For $X$ a [[simply connected]] [[smooth manifold]] and $x_0 \in X$ a basepoint, there is a canonical [[bijection]]

$$
  \Omega^1_{flat}(X,\mathfrak{g}) \simeq C^\infty_*(X,G)
$$

between the set of [[Lie-algebra valued 1-form]]s on $X$ whose [[curvature]] 2-form vanishes, and the set of [[smooth function]]s $X\to G$ that take $x_0$ to the neutral element $e \in G$.

=--

+-- {: .proof}
###### Proof

The bijection is given as follows. For $A \in \Omega^1_{flat}(X,\mathfrak{g})$ a flat 1-form, the corresponding function $f_A : X \to G$ sends $x \in X$ to the [[parallel transport]] along any path $x_0 \to x$ from the base point to $x$

$$
  f_A : x \mapsto tra_A(x_0 \to x)
  \,.
$$

Because of the assumption that the [[curvature]] 2-form of $A$ vanishes and the assumption that $X$ is [[simply connected]], this assignment is independent of the choice of path.

Conversely, for every such function $f : X \to G$ we recover $A$ as the pullback of the [[Maurer-Cartan form]] on $G$

$$
  A = f^* \theta
  \,.
$$

=--

From this we obtain

+-- {: .proof}
###### Proof of the proposition

The $\infty$-groupoid $\mathbf{cosk}_2 \exp(\mathfrak{g})$ is equivalent to the [[groupoid]] with a single object (no non-trivial 1-form on the point) whose morphisms are equivalence classes of smooth based paths $\Delta^1 \to G$ (with sitting instants), where two of these are taken to be equivalent if there is a smooth [[homotopy]] $D^2 \to G$ (with sitting instant) between them.

Since $G$ is [[simply connected]], these equivalence classes are labeled by the endpoints of these paths, hence are canonically identified with $G$.

=--

+-- {: .num_remark}
###### Remark

We do not need to fall back to classical [[Lie theory]] to obtain $G$ in the above argument. A detailed discussion of how to find $G$ with its group structure and smooth structure from $d$-paths in $\mathfrak{g}$ is in ([Crainic](#Crainic)).

=--

#### Integrating to line/circle Lie $n$-groups 
 {#IntegrationToLineNGroup}

+-- {: .num_defn}
###### Definition

For $n \in \mathbb{N}, n \geq 1$ write $b^{n-1} \mathbb{R}$ for the [[L-∞-algebra]] whose [[Chevalley-Eilenberg algebra]] is given by a single generator in degree $n$ and vanishing differential. We may call this the **line Lie $n$-algebra**.

Write $\mathbf{B}^{n} \mathbb{R}$ for the <a href="http://ncatlab.org/nlab/show/smooth+infinity-groupoid#CircleLienGroup">smooth line (n+1)-group</a>.

=--


+-- {: .num_prop}
###### Observation

The [[discrete ∞-groupoid]] underlying $\exp(b^{n-1} \mathbb{R})$ is given by the [[Kan complex]] that in degree $k$ has the set of closed differential $n$-forms (with sitting instants) on the $k$-[[simplex]]

$$
  \exp(b^{n-1} \mathbb{R})_{disc}
  : 
  [k] \mapsto \Omega^n_{si,cl}(\Delta^k)
$$

=--

+-- {: .num_prop}
###### Proposition

The $\infty$-Lie integration of $b^{n-1} \mathbb{R}$ is the <a href="http://ncatlab.org/nlab/show/smooth+infinity-groupoid#CircleLienGroup">line Lie n-group</a> $\mathbf{B}^{n} \mathbb{R}$. 

Moreover, with $\mathbf{B}^n \mathbb{R}_{chn} \in [CartSp_{smooth}^{op}, sSet]$ the standard presentation given under the [[Dold-Kan correspondence]] by the chain complex of sheaves concentrated in degree $n$ on $C^\infty(-, \mathbb{R})$ the equivalence is induced by the [[fiber integration]] of differential $n$-forms over the $n$-[[simplex]]:

$$
  \int_{\Delta^\bullet} 
   : 
  \exp(b^{n-1} \mathbb{R})
   \stackrel{\simeq}{\to}
  \mathbf{B}^{n} \mathbb{R}_{chn}
  \,.
$$


=--



+-- {: .proof}
###### Proof


First we observe that the map

$$
  \int_{\Delta^\bullet}
  :
  (\omega \in \Omega^n_{si,vert,cl}(U \times \Delta^k))
  \mapsto
  \int_{\Delta^k} \omega \in C^\infty(U, \mathbb{R})
$$ 

is a morphism of 
[[simplicial presheaves]] $\exp(b^{n-1} \mathbb{R}) \to \mathbf{B}^{n}\mathbb{R}_{chn}$ on [[CartSp]]${}_{smooth}$. Since it goes between presheaves of abelian [[simplicial group]]s by the [[Dold-Kan correspondence]] it is sufficient to check that we have a morphism of [[chain complex]]es of presheaves on the corresponding [[Moore complex|normalized chain complex]]es.

The only nontrivial degree to check is degree $n$. Let $\lambda \in \Omega_{si,vert,cl}^n(\Delta^{n+1})$. The differential of the [[Moore complex|normalized chains complex]] sends this to the signed sum of its restrictions to the $n$-faces of the $(n+1)$-simplex. Followed by the integral over $\Delta^n$ this is the piecewise integral of $\lambda$ over the boundary of the $n$-simplex. Since $\lambda$ has sitting instants, there is $0 \lt \epsilon \in \mathbb{R}$ such that there are no contributions to this integral in an $\epsilon$-neighbourhood of the $(n-1)$-faces. Accordingly the integral is equivalently that over the smooth surface inscribed into the $(n+1)$-simplex, as indicated in the following diagram


<svg width="640" height="480" xmlns="http://www.w3.org/2000/svg">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <g>
  <title>Layer 1</title>
  <path id="svg_1" d="m40,149l281,-2l-138,192l-143,-190z" stroke="#000000" fill="#ffffff"/>
  <ellipse ry="117" rx="127" id="svg_2" cy="248" cx="495" stroke-width="2" stroke="#000000" fill="#5874c9"/>
  <path id="svg_5" d="m64,181l92,124c16.66701,23 38.33299,22 53,0l89,-125c18.33301,-26 16.66699,-33 -26,-33l-185,2c-30.66666,-0.33333 -39.33334,10.33333 -23,32z" stroke="#000000" fill="#558cc6"/>
  <path id="svg_6" d="m90,182c-16,-15.66667 -10,-22.33333 18,-20l152,-1c20,-1.33333 28,7.33333 18,20l-84,114c-6.33333,13 -14.66667,15 -22,0l-82,-113z" stroke="#000000" fill="#ffffff"/>
  <ellipse ry="52" rx="55" id="svg_7" cy="157" cx="61" stroke-dasharray="5,5" stroke="#000000" fill="none"/>
  <ellipse ry="55" rx="60" id="svg_8" cy="159" cx="289" stroke-dasharray="5,5" stroke="#000000" fill="none"/>
  <ellipse ry="46" rx="51" id="svg_9" cy="317" cx="180" stroke-dasharray="5,5" stroke="#000000" fill="none"/>
  <ellipse ry="87" rx="99" id="svg_10" cy="248.00001" cx="496" stroke-dasharray="5,5" stroke="#000000" fill="#ffffff"/>
  <line id="svg_13" y2="160" x2="103" y1="148" x1="103" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_14" y2="160" x2="240" y1="147" x1="241" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_15" y2="161" x2="144" y1="148" x1="144" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_16" y2="159" x2="185" y1="147" x1="185" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_17" y2="184" x2="425" y1="161" x1="407" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_18" y2="165" x2="458" y1="139" x1="446" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_19" y2="160" x2="507" y1="131" x1="507" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_20" y2="172" x2="543" y1="146" x1="556" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_22" y2="193" x2="76" y1="183" x1="90" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_23" y2="219" x2="93" y1="208" x1="108" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_24" y2="257" x2="121" y1="247" x1="135" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_25" y2="295" x2="150" y1="285" x1="164" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_26" y2="256" x2="396" y1="259" x1="368" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_27" y2="297" x2="413" y1="314" x1="391" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_28" y2="323" x2="444" y1="345" x1="427" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_29" y2="333" x2="479" y1="362" x1="473" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_30" y2="295" x2="215" y1="284" x1="201" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_31" y2="271" x2="231" y1="261" x1="218" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_32" y2="236" x2="255" y1="227" x1="243" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_33" y2="198" x2="283" y1="188" x1="271" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_34" y2="348" x2="555" y1="323" x1="542" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_35" y2="311" x2="602" y1="293" x1="580" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_36" y2="260" x2="620" y1="256" x1="594" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_37" y2="210" x2="615" y1="221" x1="590" stroke-width="4" stroke="#ffff00" fill="none"/>
  <path id="svg_39" d="m256,272c16.33334,40.33334 68.66666,63.66666 109,49" stroke-width="4" stroke="#000000" fill="none"/>
  <line id="svg_40" y2="320" x2="362" y1="311" x1="349" stroke-width="4" stroke="#000000" fill="none"/>
  <line id="svg_41" y2="321" x2="363" y1="332" x1="355" stroke-width="4" stroke="#000000" fill="none"/>
 </g>
</svg>

Since $\lambda$ is a closed form on the $n$-simplex, this surface integral vanishes, by the [[Stokes theorem]]. Hence $\int_{\Delta^\bullet}$ is indeed a chain map.

It remains to show that $\int_{\Delta^\bullet} : \exp(b^{n-1} \mathbb{R}) \to \mathbf{B}^{n}\mathbb{R}_{chn}$ is an [[isomorphism]] on all the [[simplicial homotopy]]s group over each $U \in CartSp$. This amounts to the statement that 

1. a smooth family of closed $n$-forms with sitting instants on the boundary of $\Delta^{n+1}$ may be extended to a smooth family of closed forms with sitting instants on $\Delta^{n+1}$ precisely if their smooth family of integrals over the boundary vanishes;

1. Any smooth family of closed $n \lt k$-forms with sitting instants on the boundary of $\Delta^{k+1}$ may be extended to a smooth family of closed $n$-forms with sitting instants on $\Delta^{k+1}$.

To demonstrate this, we want to work with forms on the $(k+1)$-[[ball]] instead of the $(k+1)$-[[simplex]]. To achieve this, choose again $0 \lt \epsilon \in \mathbb{R}$ and construct the [[diffeomorphism|diffeomorphic]] image of $S^k \times [1,1-\epsilon]$ inside the $(k+1)$-simplex as indicated in the above diagram: outside an $\epsilon$-neighbourhood of the corners the image is a rectangular $\epsilon$-thickening of the faces of the simplex. Inside the $\epsilon$-neighbourhoods of the corners it bends smoothly. By the [[Steenrod-Wockel approximation theorem]] the diffeomorphism from this $\epsilon$-thickening of the smoothed boundary of the simplex to $S^k \times [1-\epsilon,1]$ extends to a smooth function from the $(k+1)$-simplex to the $(k+1)$-ball. 

By choosing $\epsilon$ smaller than each of the sitting instants of the given $n$-form on $\partial \Delta^{k+1}$, we have that this $n$-form vanishes on the $\epsilon$-neighbourhoods of the corners and is hence entirely determined by its restriction to the smoothed simplex, identified with the $(k+1)$-ball.

It is now sufficient to show: a smooth family of smooth $n$-forms $\omega \in \Omega^n_{vert,cl}(U \times S^k)$ extends to a smooth family of closed $n$-forms $\hat \omega \in \Omega^n_{vert,cl}(U \times B^{k+1})$ that is radially constant in a neighbourhood of the boundary for all $n \lt k$ and for $k = n$ precisely if its smooth family of integrals vanishes, $\int_{S^k} \omega = 0 \in C^\infty(U, \mathbb{R})$.

Notice that over the point this is a direct consequence of the [[de Rham theorem]]: an $n$-form $\omega$ on $S^k$ is exact precisely if $n \lt k$  or if $n = k$ and its integral vanishes. In that case there is an $(n-1)$-form $A$ with $\omega = d A$. Choosing any smoothing function $f : [0,1] \to [0,1]$ (smooth, surjective, non,decreasing and constant in a neighbourhood of the boundary) we obtain an $n$-form $f \wedge A$ on $(0,1] \times S^k$, vertically constant in a neighbourhood of the ends of the interval, equal to $A$ at the top and vanishing at the bottom. Pushed forward along the canonical $(0,1] \times S^k \to D^{k+1}$ this defines a form on the $(k+1)$-ball, that we denote by the same symbol $f \wedge A$. Then the form $\hat \omega := d (f \wedge A)$ solves the problem.

To complete the proof we have to show that this simple argument does extend to smooth families of forms, i.e., that we can choose the $(n-1)$-form $A$ in a way depending smoothly on the the $n$-form $\omega$. 

One way of achieving this is using [[Hodge theory]]. Fix a [[Riemannian metric]] on $S^n$, and let $\Delta$ be the corresponding [[Laplace operator]], and $\pi$ the projection on the space of [[harmonic forms]]. Then the 
<a href="http://ncatlab.org/nlab/show/Hodge+theory#ResultsOverRiemannianManifold">central result of Hodge theory</a> for [[compact topological space|compact]] [[Riemannian manifold]]s states that the operator $\pi$, seen as an operator from the 
[[de Rham complex]] to itself, is a cochain map [[homotopy|homotopic]] to the identity, via an explicit homotopy $P := d^* G$ expressed in terms of the adjoint $d^*$ of the de Rham differential and of the [[Green operator]] $G$ of $\Delta$. Since the $k$-form $\omega$ is exact its projection on [[harmonic form]]s vanishes. Therefore

$$
  \begin{aligned}
    \omega & = (Id-\pi)\omega 
    \\
     & = d (P\omega)+P (d\omega)
    \\
    & = d (P\omega).
  \end{aligned}
$$

Hence $A := P\omega$ is a solution of the differential equation $d A=\omega$ depending smoothly on $\omega$.
 
=--

#### Integrating the string Lie 2-algebra to the string Lie 2-group

Let $\mathfrak{string} = \mathfrak{g}_\mu$ be the [[string Lie 2-algebra]].

Then $\mathbf{cosk}_3 \exp(\mathfrak{g}_\mu)$ is equivalent to the [[2-groupoid]] $\mathbf{B}String$ 

* with a single object;

* whose morphisms are based paths in $G$;

* whose 2-morphisms are equivalence class of pairs $(\Sigma,c)$, where 

  * $\Sigma : D^2_*  \to G$ is a smooth based map (where we use a [[homeomorphism]] $D^2 \simeq \Delta^2$ which away from the corners is smooth, so that forms with sitting instants there do not see any non-smoothness, and the basepoint of $D^2_*$ is the 0-vertex of $\Delta^2$) 

  * and $c \in U(1)$, and where two such are equivalent if the maps coincides at their boundary and if for any 3-ball $\phi : D^3 \to G$ filling them the labels $c_1, c_2 \in U(1)$ differ by the integral $\int_{D^3} \phi^* \mu(\theta) \;\; mod \;\; \mathbb{Z}$,,

where $\theta$ is the [[Maurer-Cartan form]], $\mu(\theta) = \langle \theta\wedge [\theta \wedge \theta]\rangle $ the 3-form obtained by plugging it into the cocycle.

This is the [[string Lie 2-group]]. It's construction in terms of integration by paths is due to ([Henriques](#Henriques))


