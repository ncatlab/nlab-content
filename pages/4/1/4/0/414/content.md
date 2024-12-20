
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition 

### General

+-- {: .num_defn}
###### Definition

An [[object]] $P$ of a [[category]] $C$ is **projective** (with respect to [[epimorphisms]]) if it has the [[left lifting property]] against [[epimorphisms]]. 

=--

This means that $P$ is projective if for any

1. [[morphism]]$\;f \colon P \to B$ 

1. [[epimorphism]]$\;q \colon A \twoheadrightarrow B$, 

{#DefiningLiftingDiagram} $f$ factors through $q$, making a [[commuting diagram]] (a *[[lift]]*) of this form:

\begin{tikzcd}[sep=20pt]
  && 
  A
  \ar[dd, ->>, "{ q }"]
  \\
  \\
  P
  \ar[rr, "f"]
  \ar[
    uurr,
    dashed,
    "{ \exists \, \widehat{f} }"
  ]
  &&
  B
\end{tikzcd}

Yet another way to say  this is that:


+-- {: .num_defn #ByCovHomPreservingEpis}
###### Definition

An object $P$ is projective precisely if the [[hom-functor]] $Hom(P,-)$ preserves [[epimorphisms]].

=--

+-- {: .num_remark}
###### Remark

This generalizes the notion of _[[projective modules]]_ over a [[ring]].

=--

+-- {: .num_remark}
###### Remark

There are variations of the definition where "epimorphism" is replaced by some other type of morphism, such as a [[regular epimorphism]] or [[strong epimorphism]] or the left class in some [[orthogonal factorization system]].  In this case one may speak of **regular projectives** and so on.  In a [[regular category]] "projective" almost always means "regular projective."


If the ambient category has an [[initial object]] $\emptyset$, then the projective objects $P$ are those for which $\emptyset \stackrel{\exists!}{\to} P$ is called a [[projective morphism]].



=--

+-- {: .num_remark}
###### Remark

The [[duality|dual]] notion is that of _[[injective objects]]_. 

=-- 

+-- {: .num_remark} 
###### Remark 
There is also a stronger notion of projective object, where $\hom(C, -)$ preserves coequalizers. See more at [[tiny object]], which can be defined as projective [[connected objects]] with "projective" used in this stronger sense. 
=-- 


+-- {: .num_defn #EnoughProjectives}
###### Definition

A category $C$ has **enough projectives** if for every object $X$ there is an [[epimorphism]] $P\to X$ where $P$ is projective.

Equivalently: if every object admits a _[[projective presentation]]_.

=--

This terminology refers to the existence of [[projective resolutions]], prop. \ref{EnoughIsEnough} below.


### In abelian categories
 {#InAbelianCats}

Projective objects and [[injective objects]] in [[abelian categories]] $\mathcal{A}$ are of central interest in [[homological algebra]]. Here they appear as parts of [[cofibrant resolutions]] and [[fibrant resolutions]], respectively, in the [[category of chain complexes]] $Ch_\bullet(\mathcal{A})$, with respect to one of the two standard [[model structures on chain complexes]].

#### Equivalent characterizations
 {#EquivalentCharacterizationInAbelianCats}

+-- {: .num_prop #EquivalenceOfDefinitionsInAbelian}
###### Proposition

The following are equivalent

1. $X \in \mathcal{A}$ is a projective object (in that it has the [[left lifting property]] against [[epimorphisms]], def. \ref{ByCovHomPreservingEpis});

1. The [[hom-functor]] $Hom(X,-) : \mathcal{A} \to $ [[Ab]] is an [[exact functor]].

=--

+-- {: .num_remark }
###### Remark

For every object $X$, the hom-functor $Hom(X,-)$ is a [[left exact functor]]. So the second statement is equivalently that it is also right exact precisely if $X$ is projective.

=--

+-- {: .proof}
###### Proof 
**of prop. \ref{EquivalenceOfDefinitionsInAbelian}**

Let 

$$
  0 \to A \stackrel{i}{\hookrightarrow} B \stackrel{p}{\to} C \to 0
$$

be a [[short exact sequence]]. The exactness at $A$ and $B$ together is equivalent to the statement that $i = \ker(p)$. Since as remarked above $Hom(X, -)$ is left exact, it preserves [[kernels]] and so $Hom(X, i) = \ker(Hom(X, p))$, giving exactness of the sequence 

$$
0 \to  Hom(X,A) 
    \stackrel{Hom(X,i)}{\to}
  Hom(X,B)
   \stackrel{Hom(X,p)}{\to}
  Hom(X,C)
  \,.
$$

Therefore we are reduced to showing that $Hom(X,p)$ is an [[epimorphism]] precisely if $X$ is projective. But this is def. \ref{ByCovHomPreservingEpis}.


=--


#### Projective resolutions

Let $\mathcal{A}$ be an [[abelian category]]. 

+-- {: .num_defn}
###### Definition

For $N \in \mathcal{A}$ an object, a **[[projective resolution]]** of $N$ is a [[chain complex]] $(Q N)_\bullet \in Ch_\bullet(\mathcal{A})$ equipped with a [[chain map]]

$$
  Q N \to N
$$

(with $N$ regarded as a complex concentrated in degree 0) such that

1. this morphism is a [[quasi-isomorphism]] (this is what makes it a [[resolution]]), which is equivalent to 

   $$ \cdots \to (Q N)_1 \to (Q N)_0 \to N $$

   being an [[exact sequence]];

1.  all whose entries $(Q N)_n$ are projective objects.


=--

+-- {: .num_remark}
###### Remark

This means precisely that $Q N \to N$ is an [[cofibrant resolution]] with respect to the standard [[model structure on chain complexes]] (see [here](model%20structure%20on%20chain%20complexes#StandardQuillenOnBounded)) for which the fibrations are the positive-degreewise epimorphisms. Notice that in this model structure every object is fibrant, so that cofibrant resolutions are the only resolutions that need to be considered.

=--

+-- {: .num_prop #EnoughIsEnough}
###### Proposition

If $\mathcal{A}$ has _enough projectives_ in the sense of def. \ref{EnoughProjectives}, then every object has a projective resolution.

=--






## Examples

+-- {: .num_remark #ProjectiveInSetsIsAxiomOfChoice}
###### Remark

The [[axiom of choice]] can be phrased as "all objects of [[Set]] are projective."  

See also _[[internally projective object]]_ and _[[COSHEP]]_.

=--

+-- {: .num_example}
###### Example

If $C$ has [[pullback|pullbacks]] and epimorphisms are preserved by pullback, as is the case in a [[pretopos]], then $P$ is projective iff any epimorphism $Q\to P$ is [[split epimorphism|split]].

=--

+-- {: .num_example #ProjectiveObjectsInAbAreFreeGroups}
###### Example

An object in [[Ab]], an [[abelian group]], is projective precisely if it is a [[free group]].

=--

+-- {: .num_example}
###### Example


For $R$ a [[commutative ring]], an object in  $R$[[Mod]], an $R$-[[module]], is projective (a [[projective module]], see there for more details) precisely if it is a [[direct sum|direct summand]] of a [[free module]]. See at _[[projective module]]_ for more on this.


=--

+-- {: .num_example}
###### Example

The projective objects in [[compact topological space|compact]] [[Hausdorff topological spaces]] are precisely the [[extremally disconnected profinite sets]].

=--




## Properties

### Existence of enough projectives
 {#ExistenceOfEnoughProjectives}

We list examples of classes of categories that have enough projective, according to def. \ref{EnoughProjectives}.

+-- {: .num_prop #ModHasEnoughProjectives}
###### Proposition

Assuming the [[axiom of choice]], for $R$ a [[ring]] the category $R$[[Mod]] of [[modules]] over $R$ is has enough projectives.

=--

See at _[[projective module]]_ for more.

+-- {: .num_lemma #FreeModulesAreProjective}
###### Lemma

Assuming the [[axiom of choice]],
a [[free module]] $N \simeq R^{(S)}$ is projective.

=--

+-- {: .proof}
###### Proof 

By remark \ref{ProjectiveInSetsIsAxiomOfChoice} and the [[free-forgetful adjunction]].

More explicitly: if $S \in Set$ and $F(S) = R^{(S)}$ is the [[free module]] on $S$, then a module homomorphism $F(S) \to N$ is specified equivalently by a [[function]] $f : S \to U(N)$ from $S$ to the underlying set of $N$, which can be thought of as specifying the images of the unit elements in $R^{(S)} \simeq \oplus_{s \in S} R$ of the ${\vert S\vert}$ copies of $R$.

Accordingly then for $\tilde N \to N$ an epimorphism, the underlying function $U(\tilde N) \to U(N)$ is an epimorphism, and by remark \ref{ProjectiveInSetsIsAxiomOfChoice} the [[axiom of choice]] in [[Set]] says that we have all lifts $\tilde f$ in

$$
  \array{
     && U(\tilde N)
     \\
     & {}^{\tilde f} \nearrow & \downarrow
     \\
     S &\stackrel{f}{\to}& U(N)
  }
  \,.
$$

By [[adjunction]] these are equivalently lifts of module homomorphisms

$$
  \array{
     && \tilde N
     \\
     & \nearrow & \downarrow
     \\
     R^{(S)} &\stackrel{}{\to}& N
  }
  \,.
$$


=--

+-- {: .proof}
###### Proof 
**of prop. \ref{ModHasEnoughProjectives}**

For $N \in R Mod$ and $U(N) \in Set$ its underlying set, 
consider the $R$-linear map

$$
  \left(
    \oplus_{n \in U(N)} R 
  \right)
  \to 
  N
$$

out of the [[direct sum]] of ${\vert U(N)\vert}$ copies of $N$,
which sends the unit element $1 \in R_{n}$ of the $n$-labeled copy of $R$ to the corresponding element of $N$ (and is thus fixed on all other elements by $R$-linearity).

This is clearly a [[surjection]] and by lemma \ref{FreeModulesAreProjective} it is a surjection out of a projective object. 

=--


A slightly subtle point is that there is no guarantee that the free module $F U(M)$ is actually projective, unless one assumes some form of the [[axiom of choice]]. Since the axiom of choice is not available in all [[toposes]], one cannot use this procedure in general to construct, say, projective resolutions of [[abelian sheaves]], hence in the abelian category $Ab(E)$ of abelian [[group objects]] in a general [[Grothendieck topos]] $E$ (even though one can construct 
[[free resolutions]]), such as needed in general in [[abelian sheaf cohomology]]. 

There are however weak forms of the axiom of choice that hold in many toposes, such as the [[presentation axiom]], aka _[[COSHEP]]_. We have the following result: 

+-- {: .num_prop #EnoughWithCOSHEP} 
###### Proposition 

Let $E$ be a [[W-pretopos]] that satisfies [[COSHEP]]. 
Then $Ab(E)$ has enough projectives.

=-- 

The idea of the proof is that under COSHEP, the underlying object of an abelian group $A$ in $E$ admits an [[epimorphism]] from a projective object $p \colon X \to U(A)$ in $E$. Then the corresponding $F(X) \to A$ is an epimorphism out of a projective in $Ab(E)$, for this map is a composite of epimorphisms 

$$F(X) \stackrel{F(p)}{\to} F U(A) \stackrel{\varepsilon_A}{\to} A$$ 

(the first is epic because left adjoints preserve epis, whereas the second map, the component of the counit $\varepsilon \colon F U \to id$ at $A$, is epic because $U$ is faithful). 



## Related concepts

* [[choice object]]

* [[COSHEP]]

* **projective object**, [[projective presentation]], [[projective cover]], [[projective resolution]]

  * [[projective module]]

  * [[internally projective object]]

  * [[compact projective object]]

* [[injective object]], [[injective presentation]], [[injective envelope]], [[injective resolution]]

  * [[injective module]]

* [[free object]], [[free resolution]]
 
  * [[free module]]

* flat object, [[flat resolution]]

  * [[flat module]]

## References

For instance section 4.3 of

* [[Pierre Schapira]], _Categories and homological algebra_ (2011) ([pdf](https://perso.imj-prg.fr/pierre-schapira/wp-content/uploads/schapira-pub/lectnotes/HomAl.pdf))



[[!redirects enough projectives]]
[[!redirects projective objects]]
