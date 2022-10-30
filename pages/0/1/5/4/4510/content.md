
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In the context of [[homological algebra]] the [[right derived functor]] of the [[hom-functor]] is called the _$Ext$-functor_ . It derives its name from the fact that the derived hom between [[abelian groups]] classifies [[group extensions]] of $A$ by $K$. (This is a special case of the general classificaton of [[principal ∞-bundles]]/[[∞-group extensions]] by general [[cohomology]]/[[group cohomology]].)

Together with the [[Tor]]-functor it is one of the central objects of interest in homological algebra.

Given a [[abelian category]] $\mathcal{A}$ we may consider the [[hom-functor]] $Hom_{\mathcal{A}} : \mathcal{A}^{op}\times \mathcal{A}\to $[[Ab]] either as a functor in first or in second argument, and compute the corresponding [[right derived functors]]. 

If they exist, the classical right derived functors of either functor agree and also agree with the [[homology]] of the mixed [[double complex]] obtained by taking simultaneously an  [[injective resolution]] of the first contravariant argument and [[projective resolution]] of the second covariant argument. The last construction is called the _balanced $Ext$._

Alternatively, one can consider the [[derived category]] $D(\mathcal{A})$ and define 

$$
  Ext^p(X,A) \coloneqq Hom_{D(A)}(X,A[p])
$$

or define $Ext^i$-groups as groups of extensions of length $i$, discussed below at _[Relation to extensions](#RelationToGroupExtensions)_.


## Definition

We give the definition following the discussion at _[[derived functors in homological algebra]]_.

### Contravariant $Ext$ on an ordinary object
 {#ContravariantExtOnObject}

Let $\mathcal{A}$ be an [[abelian category]] with 
[[projective object|enough projectives]]. And let $A \in \mathcal{A}$ be any object. Consider the [[contravariant functor|contravariant]] [[hom-functor]]

$$
  Hom_{\mathcal{A}}(-, A) : \mathcal{A}^{op} \to Ab
  \,.
$$

+-- {: .num_remark}
###### Remark

This is a [[left exact functor]]. 

Therefore to derive it by [[resolutions]] we need to consider
[[injective resolutions]] in the [[opposite category]] $\mathcal{A}^{op}$.
But these are [[projective resolutions]] in $\mathcal{A}$ itself.

=--

+-- {: .num_defn #OfSingleObjByProjResolution}
###### Definition

For $X \in \mathcal{A}$ any object and $((Q X) \to X) \in Ch_{\bullet \geq 0}(\mathcal{A})$ a [[projective resolution]], and for $n \in \mathbb{N}$, the **$n$th $Ext$-group** of $X$ with [[coefficients]] in $A$ is the degree-$n$ [[cochain cohomology]]

$$
  Ext^n(X,A) 
   \coloneqq 
  H^\bullet ( Hom_{\mathcal{A}}((Q X)_\bullet, A))
$$

of the [[cochain complex]] $Hom((Q X)_\bullet, A)$. 

=--

The following proposition expands a bit on the meaning of this definition. Write 

$$
  [-,-] : Ch_{\bullet}(\mathcal{A})^{op} \times Ch_\bullet(\mathcal{A})
  \to 
  Ch_\bullet(Ab)
$$ 

for the [[internal hom of chain complexes|enriched hom of chain complexes]]. 

+-- {: .num_prop}
###### Proposition

The $n$th Ext-group is canonically identified with the 0-th [[homology]] of this enriched hom from the resolution $Q X$ of $X$ to the $n$-fold [[delooping]]/[[suspension]] chain complex of $A$
$\mathbf{B}^n A = A[n]$ (concentrated on $A$ in degree $n$):

$$
  Ext^n(X,A)
  \simeq
  H_0 [(Q X), A[n] ]
  \,;
$$ 

or equivalently, if we think of degree [[chain homology]] as the 0th [[homotopy group]] (under [[Dold-Kan correspondence]]) and write the $n$-fold [[suspension]]/[[delooping]] of $A$ as $\mathbf{B}^n A$:

$$
  Ext^n(X,A)
  \simeq
  \pi_0 [(Q X), \mathbf{B}^n A ]
  \,.
$$ 


=--

+-- {: .proof}
###### Proof

This is a special case of the general discussion at [[cochain cohomology]].

By the discussion at _[[internal hom of chain complexes]]_, the 0-[[cycles]] of $[(Q X), \mathbf{B}^n A ]$ are [[chain maps]] of the form

$$
  \array{
    \vdots && \vdots
    \\
    \downarrow && \downarrow
    \\
    (Q X)_{n+1} &\stackrel{f_{n+1}}{\to}& 0
    \\
    \downarrow^{\mathrlap{\partial^{Q X}_{n-1}}} && \downarrow
    \\
    (Q X)_{n} &\stackrel{f_{n}}{\to}&  A
    \\
    \downarrow^{\mathrlap{\partial^{Q X}_{n-1}}} && \downarrow
    \\
    (Q X)_{n-1} &\stackrel{f_{n-1}}{\to}& 0
    \\
    \downarrow && \downarrow
    \\
    \vdots && \vdots
    \\
    \downarrow^{\mathrlap{\partial^{Q X}_1}} && \downarrow
    \\
    (Q X)_1 &\stackrel{f_1}{\to}& 0    
    \\
    \downarrow^{\mathrlap{\partial^{Q X}_0}} && \downarrow
    \\
    (Q X)_0 &\stackrel{f_0}{\to}& 0
  }
  \,.
$$ 

By the definition of chain maps this are precisely those morphisms
$f_n : (Q X)_n \to A$ such that 

$$
  d^n f_n \coloneqq f_n \circ \partial^{Q X}_n = 0
$$

which exhibits $f_n$ as a degree-$n$ [[cochain]] in the [[cochain complex]] $Hom((Q X)_\bullet, A)$.

Similarly, the $0$-[[boundaries]] in $[(Q X), \mathbf{B}^n A]$ come from [[chain homotopies]] $\lambda : 0 \Rightarrow f$:

$$
  \array{
    \vdots && \vdots
    \\
    \downarrow && \downarrow
    \\
    (Q X)_{n+1} &\stackrel{f_{n+1}}{\to}& 0
    \\
    \downarrow^{\mathrlap{\partial^{Q X}_{n-1}}} 
     &\nearrow_{\mathrlap{\lambda_{n+1}}}& \downarrow
    \\
    (Q X)_{n} &\stackrel{f_{n}}{\to}&  A
    \\
    \downarrow^{\mathrlap{\partial^{Q X}_{n-1}}} 
    &\nearrow_{\mathrlap{\lambda_{n}}}& \downarrow
    \\
    (Q X)_{n-1} &\stackrel{f_{n-1}}{\to}& 0
    \\
    \downarrow && \downarrow
    \\
    \vdots && \vdots
    \\
    \downarrow^{\mathrlap{\partial^{Q X}_1}} 
    &\nearrow_{\mathrlap{\lambda_{2}}}& \downarrow
    \\
    (Q X)_1 &\stackrel{f_1}{\to}& 0    
    \\
    \downarrow^{\mathrlap{\partial^{Q X}_0}} 
    &\nearrow_{\mathrlap{\lambda_{1}}}& \downarrow
    \\
    (Q X)_0 &\stackrel{f_0}{\to}& 0
  }
  \,.
$$ 

in that 

$$
  f_n = \lambda_n \circ \partial^{Q X}_{n-1}
  \,.
$$

This are precisely the degree-$n$ [[coboundaries]] in 
$Hom((Q X)_\bullet, A)$.  

=--

+-- {: .num_remark}
###### Remark

This perspective on the $Ext^n$-group as being the [[homotopy classes]] of maps out of (a resolution of) $X$ to $\mathbf{B}^n A$ is made more manifest in the discussion [in terms of derived categories](#InTermsOfDerivedCategories) below. It connects $Ext$-groups and their [relation to extensions](#RelationToGroupExtensions) to the general context of _[[cohomology]]_ and _[[∞-group extensions]]_. See at _[[abelian sheaf cohomology]]_ for more on this.
 
=--

### In terms of derived categories
 {#InTermsOfDerivedCategories}

(...)

([Kashiwara-Shapira](#KashiwaraShapira))

(...)

## Properties

### Relation to extensions
 {#RelationToGroupExtensions}

We discuss how the group $Ext^n(X,A)$ is identified with the group of [[extensions]] of $X$ by $\mathbf{B}^{n-1} A = A[n-1]$. In particular for $n = 1$ and $\mathcal{A} = $ [[Ab]] this means that $Ext^1(X,A)$ classified ordinary [[group extensions]] of $X$ by $A$. 

This is the relation that the name "$Ext$" derives from. At _[[infinity-group extension]]_ is discussed how this relation is a special case of the more general relation that identifies [[derived hom-spaces]] $\mathbf{H}(X,\mathbf{B}^{n+1} A)$ with $\mathbf{B}^n A$-[[principal ∞-bundles]] over $X$.

#### 1-Extensions over single objects

+-- {: .num_defn}
###### Definition

For $X,A \in \mathcal{A}$ two objects, an **[[extension]]** of $X$ by $A$ is a [[short exact sequence]]

$$
  0 \to A \to P \to X \to 0
  \,.
$$

An [[homomorphism]] of two such extensions $P_1$ and $P_2$ is a [[morphism]] $P_1 \to P_2$ in $\mathcal{A}$ fitting into a [[commuting diagram]] of the form

$$
  \array{
     && P_1
     \\
     & \nearrow & & \searrow
     \\
     A && \downarrow && X
     \\
     & \searrow & & \nearrow
     \\
     && P_2
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

All these homomophisms are necessarily [[isomorphisms]], by the [[short five lemma]].

=--

+-- {: .num_defn}
###### Definition


Write $Extensions(X,A)$ for the set of [[isomorphism classes]] of such extensions.

=--


+-- {: .num_prop}
###### Proposition

Under [[Baer sum]] $Extensions(X,A)$ becomes an [[abelian group]].

=--

+-- {: .num_defn #ExtractCocycleFromExtension}
###### Definition

Define a morphism

$$
  ExtractCocycle : Extensions(X,A) \to Ext^1(X,A)
$$

by the following construction:

choose a [[projective presentation]] $N \hookrightarrow Q \to X$ of $X$. Then 
for $A \to P \to X$ an extension consider the diagram

$$
  \array{
    N &\to& Q &\to& X
    \\
    \downarrow^{\mathrlap{\sigma|_N}} && \downarrow^{\mathrlap{\sigma}} && \downarrow^{\mathrlap{=}}
    \\
    A &\to& P &\to& X
  }
  \,,
$$

where

* $\sigma$ is any choice of lifts of $Q \to A$ through $P \to A$, which exists by definition since $P$ is a [[projective object]], 

* $\sigma|_N$ is the induces morphism on the fibers, which exists by the exactness of the two sequences.

By prop. \ref{Ext1FromProjectivePresentation} $\sigma|_N$ represents an element in $ [\sigma|_N] \in Ext^1(X,A)$. Let this be the image of the map to be defined:

$$
  ExtractCocycle : (A \to P \to X) \mapsto [\sigma|_N]
  \,.
$$

This definition is independent of the choice of $P$ and $\sigma$ involved.

=--



+-- {: .num_prop}
###### Proposition

The map from def. \ref{ExtractCocycleFromExtension} 
is a [[natural isomorphism]] of abelian groups

$$
  Extensions(X,A) \stackrel{\simeq}{\to} Ext^1(X,A) 
  \,.
$$

=--


#### Higher extensions over general chain complexes

(...)

Given $[g] \in \mathbb{R}Hom(X, A[n])$.

Let $Q \to X$ be a [[projective resolution]].
Let $g : Q \to A[n]$ be a representative of $[g]$.  
Consider the [[pullback]]

$$
  \array{
    P &\to& cone(0 \to A[n])
    \\
    \downarrow && \downarrow
    \\
    Q &\stackrel{g}{\to}& A[n]
    \\
    \downarrow
    \\
    X
  }
$$

(...)

### Localization
 {#Locatization}

(...)

### Techniques for constructing $Ext^n$

We discuss some facts helpful for the construction of $Ext^n$-groups in certain situations.

+-- {: .num_prop}
###### Proposition

If $X \in \mathcal{A}$ is a [[projective object]], then 

$$
  Ext^n(X, -)  = 0
$$

is the [[zero object|zero]]-[[functor]] for all $n \geq 1$.

=--

+-- {: .proof}
###### Proof

The covariant [[hom-functor]] $Hom(X,-)$ is generally a [[left exact functor]]. By the construction of $Ext^n$ via [[projective resolutions]], def. \ref{OfSingleObjByProjResolution}, it is sufficient to show that it is also a [[right exact functor]] if $P$ is projective. In fact, this is one of the equivalent characterizations of _[[projective objects]]_ (ee the section [projective object -- in abelian categories -- equivalent characterizations](projective+object#EquivalentCharacterizationInAbelianCats) for details).

=--

+-- {: .num_prop #Ext1FromProjectivePresentation}
###### Proposition

For $X, A \in \mathcal{A}$ two objects, and 

$$
  0 \to N \stackrel{i}{\hookrightarrow} P \stackrel{p}{\to} X \to 0
$$ 

a [[short exact sequence]] with $P$ a [[projective object]], hence exhibiting a [[projective presentation]] $X \simeq coker(N \hookrightarrow P)$ of $X$, there is an [[exact sequence]]

$$
  0 
   \to 
  Hom(X,A)
    \stackrel{Hom(p,A)}{\to}
  Hom(P, A)
    \stackrel{Hom(i,A)}{\to}
  Hom(N,A)
    \to
  Ext^1(X,A)
    \to 
  0
$$

exhibiting $Ext^1(X,A)$ as the [[cokernel]] of $Hom(i,A)$.

=--


## Applications in cohomology

[[derived hom-space|Derived hom-functors]]such as the $Ext$ on chain compelxes compute general notions of _[[cohomology]]_ (see the discussion there). Here we list some specific incarnations of the $Ext$-construction in the context of cohomology.

### Universal coefficient theorem

The _[[universal coefficient theorem]]_ identifies, under suitable conditions, [[cohomology]] to the [[duality|dual]] of [[homology]] up to $Ext^1$-groups.

### Various notions of cohomology expressed by $Ext$

Various notions of [[cohomology groups]] in the context of [[algebra]] can be expressed as $Ext$-groups, for instance:

* For $G$ a [[discrete group]] with $\mathbb{Z}[G]$ its [[group ring]], over the [[integers]], and for $N$ a linear $G$-[[representation]], hence a $\mathbb{Z}[G]$-[[module]], the [[group cohomology]] of $G$ with [[coefficients]] in $N$ is 
  
  $$
    Ext^\bullet_{\mathbb{Z}[G]Mod}(\mathbb{Z}[G], N)
    \,.
  $$

* For $A$ an [[associative algebra]] over some [[field]] $k$ and $N$ an $A$-[[bimodule]], hence an $A \otimes A^{op}$-[[module]], 

  $$
    Ext^\bullet_{(A \otimes A^{op})Mod}(A, N) 
  $$

  is the [[Hochschild cohomology]] of $A$ with [[coefficients]] in $N$.

* For $\mathfrak{g}$ a [[Lie algebra]] with [[universal enveloping algebra]] $\mathcal{U}(\mathcal{g})$ and $N$ a Lie algebra module, hence an $\mathcal{U}(\mathfrak{g})$-module, the [[Lie algebra cohomology]] of $\mathfrak{g}$ with [[coefficients]] in $N$ is

  $$
    Ext^\bullet_{\mathcal{U}(\mathfrak{g}) Mod}(\mathcal{U}(\mathfrak{g}), N)
    \,.
  $$

## Related concepts

[[!include homotopy-homology-cohomology]]

## References

Standard texbook accounts include (see also most references at _[[homological algebra]]_)

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_,  Cambridge Studies in Adv. Math. 38, CUP 1994
 {#Weibel}

* [[Henri Cartan]], [[Samuel Eilenberg]], _Homological algebra_, Princeton Univ. Press 1956.

* S. I . Gelfand, [[Yuri Manin]], _Methods of homological algebra_

A systematic discussion from the point of view of [[derived categories]] is in 

* [[Masaki Kashiwara]], [[Pierre Schapira]], _[[Categories and Sheaves]]_, Springer (2000)
 {#KashiwaraShapira}

Lecture notes include

* Kiyoshi Igusa, _25 The Ext Functor_ ([pdf](http://people.brandeis.edu/~igusa/Math101b/Ext.pdf))

section 4 of

* [[Peter May]], _Notes on Tor and Ext_ ([pdf](http://www.math.uchicago.edu/~may/MISC/TorExt.pdf))
 {#May}

as well as

* Patrick Morandi, _Ext Groups and Ext Functors_, ([pdf](http://sierra.nmsu.edu/morandi/oldwebpages/math683fall2002/Ext.pdf))



See also

* Wikipedia, _[Ext functor](http://en.wikipedia.org/wiki/Ext_functor)_

[[!redirects Ext group]]
[[!redirects Ext-group]]
[[!redirects Ext-groups]]
[[!redirects Ext groups]]
[[!redirects Ext functor]]
[[!redirects Ext functors]]
[[!redirects Ext-functor]]
[[!redirects Ext-functors]]
