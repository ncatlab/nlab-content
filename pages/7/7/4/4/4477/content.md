
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homological algebra
+-- {: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

+-- {: .num_defn #ProjectiveModule}
###### Definition

For $R$ a [[ring]], a _projective $R$-module_ is a [[projective object]] in the [[category]] $R$[[Mod]]. 

Hence an $R$-module $N$ is _projective_ precisely if for all [[diagrams]] of $R$-[[module]] [[homomorphisms]] of the form

$$
  \array{
    && A
    \\
    & & \downarrow^{\mathrlap{epi}}
    \\
    N &\underset{f}{\longrightarrow}& B
  }
$$

there exists a morphism $N \overset{\phi}{\to} A$ making a [[commuting diagram]] of the form

$$
  \array{
    && A
    \\
    & {}^{\mathllap{\phi}}\nearrow & \downarrow^{\mathrlap{epi}}
    \\
    N &\underset{f}{\longrightarrow}& B
  }
  \,.
$$


=--

+-- {: .num_prop #NProjectiveIFFHomNExact}
###### Proposition

An $R$-module $N$ is projective (def. \ref{ProjectiveModule}) precisely if the [[hom functor]] 

$$
  Hom_{R Mod}(N, - ) : R Mod \to Ab
$$

(out of $N$) is an [[exact functor]]. 

=--

+-- {: .proof}
###### Proof

The hom-functor in question is a [[left exact functor]] for all $N$, hence we need to show that it is a [[right exact functor]] precisely if $N$ is projective.

That $Hom_R(N,-)$ is right exact means equivalently that for

$$
  0 
    \to 
  A 
    \overset{i}{\longrightarrow} 
  B 
    \overset{p}{\longrightarrow}
  C 
    \to 
  0
  \,,
$$

any [[short exact sequence]],
hence for $p$ any [[epimorphism]] and $i$ its [[kernel]] inclusion,  then $Hom_R(N,p)$ is an epimorphism, hence that for any element $f \in Hom_R(N,C)$, 

$$
  \array{
    && B
    \\
    && \downarrow^{\mathrlap{p}}
    \\
    N &\underset{f}{\longrightarrow}& C
  }
$$

there exists $\phi \colon N \to B$ such that $f =  Hom_R(N,p)(\phi) \coloneqq p \circ \phi$, hence that 


$$
  \array{
    && B
    \\
    &{}^{\mathllap{\phi}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    N &\underset{f}{\longrightarrow}& C
  }
  \,.
$$

This is manifestly the condition that $N$ is projective.


=--


## Properties

### Existence of enough projective modules

+-- {: .num_lemma #FreeModulesAreProjective}
###### Lemma

Assuming the [[axiom of choice]],
a [[free module]] $N \simeq R^{(S)}$ is projective.

=--

+-- {: .proof}
###### Proof 

Explicitly: if $S \in Set$ and $F(S) = R^{(S)}$ is the [[free module]] on $S$, then a module homomorphism $F(S) \to N$ is specified equivalently by a [[function]] $f : S \to U(N)$ from $S$ to the underlying set of $N$, which can be thought of as specifying the images of the unit elements in $R^{(S)} \simeq \oplus_{s \in S} R$ of the ${\vert S\vert}$ copies of $R$.

Accordingly then for $\tilde N \to N$ an epimorphism, the underlying function $U(\tilde N) \to U(N)$ is an epimorphism, and the [[axiom of choice]] in [[Set]] says that we have all lifts $\tilde f$ in

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


+-- {: .num_prop #FreeForgetfulCounitEpimorphism}
###### Proposition

Assuming the [[axiom of choice]], the category $R$[[Mod]] has _[enough projectives](projective%20object#EnoughProjectives)_: for every $R$-[[module]] $N$ there exists an [[epimorphism]] $\tilde N \to N$ where $\tilde N$ is a projective module.

=--

+-- {: .proof}
###### Proof

Let $F(U(N))$ be the [[free module]] on the [[set]] $U(N)$ underlying $N$. By lemma \ref{FreeModulesAreProjective} this is a projective module.

The [[counit of an adjunction|counit]] 

$$
  \epsilon : F(U(N)) \to N
$$

of the [[free functor|free]]/[[forgetful functor|forgetful]]-[[adjunction]] $(F \dashv U)$ is an [[epimorphism]]. 

=--

Actually, the full axiom of choice is not necessary here; it is enough to have the [[presentation axiom]], which states the [[category of sets]] has enough projectives (whereas the axiom of choice states that *every* set is projective).  Then we can replace $U(N)$ above by a projective set $P \twoheadrightarrow U(N)$, giving an epimorphism $F(P) \twoheadrightarrow F(U(N)) \twoheadrightarrow N$ (and $F(P)$ is projective).


### Explicit characterizations

We discuss the more explicit characterization of projective modules
as [[direct sum|direct summands]] of [[free modules]].


+-- {: .num_lemma #DirectSummandOfFreeIsProjective}
###### Lemma

If $N \in R Mod$ is a [[direct sum|direct summand]] of a [[free module]], hence if there is $N' \in R Mod$ and $S \in Set$ such that 

$$
  R^{(S)} \simeq N \oplus N'
  \,,
$$

then $N$ is a projective module.

=--

+-- {: .proof}
###### Proof 

Let $\tilde K \to K$ be a surjective homomorphism of modules and 
$f : N \to K$ a homomorphism. We need to show that there is a lift $\tilde f$ in

$$
  \array{
    && \tilde K
    \\
    & {}^{\mathllap{\tilde f}}\nearrow & \downarrow
    \\
    N &\stackrel{f}{\to}& K 
  }
  \,.
$$

By definition of [[direct sum]] we can factor the [[identity]] on $N$ as

$$
  id_N : N \to N \oplus N' \to N
  \,.
$$

Since $N \oplus N'$ is free by assumption, and hence projective by lemma \ref{FreeModulesAreProjective}, there is a lift $\hat f$ in 

$$
  \array{
    && && \tilde K
    \\
    && & {}^{\mathllap{\hat f}}\nearrow & \downarrow
    \\
    N &\to& N \oplus N'  &\to& K
  }
  \,.
$$

Hence $\tilde f : N \to N \oplus N' \stackrel{\hat f}{\to} \tilde K$ is a lift of $f$.

=--

+-- {: .num_prop #ProjectiveIsPreciselyDirectSummandOfFreeModule}
###### Proposition

An $R$-module $N$ is projective precisely if it is the [[direct summand]] of a [[free module]]. 

=--

+-- {: .proof}
###### Proof

By lemma \ref{DirectSummandOfFreeIsProjective} if $N$ is a direct summand then it is projective. So we need to show the converse.

Let $F(U(N))$ be the [[free module]] on the [[set]] $U(N)$ underlying $N$ as in the proof of prop. \ref{FreeForgetfulCounitEpimorphism}. The [[counit of an adjunction|counit]] 

$$
  \epsilon : F(U(N)) \to N
$$

of the [[free functor|free]]/[[forgetful functor|forgetful]]-[[adjunction]] $(F \dashv U)$ is an [[epimorphism]]. Thefore if $N$ is projective, there is a [[section]] $s$ of $\epsilon$. This exhibits $N$ as a direct summand of $F(U(N))$.

=--

This proposition is often stated more explicitly as the existence of a [[dual basis]], see there. 

In some cases this can be further strengthened:

+-- {: .num_prop}
###### Proposition

If the [[ring]] $R$ is a [[principal ideal domain]] (in particular $R = \mathbb{Z}$ the [[integers]]), then every projective $R$-module is free.

=--

The details are discussed at _[pid - Structure theory of modules](http://ncatlab.org/nlab/show/principal+ideal+domain#StructureTheoryOfModules)_.

+-- {: .num_prop}
###### Proposition

For an $R$-module $P$, the following statements are equivalent:

1. $P$ is finite locally free in that there exists a partition $1 = \sum_i f_i \in R$ such that the localized modules $P[f_i^{-1}]$ are finite free modules over $R[f_i^{-1}]$.

1. $P$ is finitely generated and projective.

1. $P$ is a [[dualizable object]] in the category of $R$-modules (equipped with the tensor product as monoidal structure).

1. There exist elements $x_1,\ldots,x_n \in P$ and linear forms $\vartheta_1,\ldots,\vartheta_n \in Hom(P,R)$ such that $x = \sum_i \vartheta_i(x) x_i$ for all $x \in P$.

=--

+-- {: .proof}
###### Proof

The equivalence of 2., 3., and 4. is mostly formal. For the equivalence with 1., see [this math.SE discussion](http://math.stackexchange.com/questions/16814/finitely-generated-projective-modules-are-locally-free) for good references. Note that the equivalences are true without assuming that $R$ is [[Noetherian ring|Noetherian]] or that $P$ satisfies some finiteness condition.
=--

### Relation to projective resolutions of chain complexes
 {#RelationToProjectiveResolution}


+-- {: .num_defn}
###### Definition

For $N \in R Mod$ a **[[projective resolution]]** of $N$ is a [[chain complex]] $(Q N)_\bullet \in Ch_\bullet(R Mod)$ equipped with a [[chain map]]

$$
  Q N \to N
$$

(with $N$ regarded as a complex concentrated in degree 0) such that

1. this morphism is a [[quasi-isomorphism]] (this is what makes it a [[resolution]]), which is equivalent to 

   $$ \cdots \to (Q N)_1 \to (Q N)_0 \to N $$

   being an [[exact sequence]];

1.  all whose entries $(Q N)_n$ are projective modules.


=--

+-- {: .num_remark}
###### Remark

This means precisely that $Q N \to N$ is an [[cofibrant resolution]] with respect to the standard [[model structure on chain complexes]] (see [here](model%20structure%20on%20chain%20complexes#StandardQuillenOnBounded)) for which the fibrations are the positive-degreewise epimorphisms. Notice that in this model structure every object is fibrant, so that cofibrant resolutions are the only resolutions that need to be considered.

=--

+-- {: .num_prop}
###### Proposition

Every $R$-module has a projective resolution. 

=--

See at _[[projective resolution]]_.


## Examples

+-- {: .num_prop #ModuleOverAFieldIsProjective}
###### Proposition

Assuming the [[axiom of choice]], then by the [[basis theorem]] every module over a [[field]] is a [[free module]] and hence in particular every module over a field is a projective module (by prop. \ref{DirectSummandOfFreeIsProjective}).

=--


+-- {: .num_prop}
###### Proposition


If $R$ is the [[integers]] $\mathbb{Z}$, or a [[field]] $k$, or a [[division ring]], then every projective $R$-module is already a free $R$-module.

=--

## Related concepts

* [[projective object]], [[projective presentation]], [[projective cover]], [[projective resolution]]

* [[injective object]], [[injective presentation]], [[injective envelope]], [[injective resolution]]

  * [[injective module]]

* [[free object]], [[free resolution]]

  * [[free module]], [[locally free module]]

* flat object, [[flat resolution]]

  * [[flat module]]

* [[free module]] $\Rightarrow$ **projective module** $\Rightarrow$ [[flat module]] $\Rightarrow$ [[torsion-free module]]


* [[Serre-Swan theorem]]

* [[Quillen-Suslin theorem]]

## References


Lecture notes include

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_, section 2.2

* _Projective modules, Presentations and resolutions_ ([pdf](http://livetoad.org/Courses/Documents/8875/Notes/presentations_and_resolutions.pdf))

* Thomas Lam, chapter 6 ([pdf](http://www.math.lsa.umich.edu/~tfylam/Math221/6.pdf))

Original articles include

* Irving Kaplansky, _Projective modules_, The Annals of Mathematics
Second Series, Vol. 68, No. 2 (Sep., 1958), pp. 372-377 ([JSTOR]( http://www.jstor.org/stable/1970252))

[[!redirects projective modules]]
