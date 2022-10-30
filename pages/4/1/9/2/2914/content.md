

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Definition ##

+-- {: .num_prop}
###### Proposition


For $C$ a [[model category]] and $X \in C$ an [[object]], the [[over category]] $C/X$ as well as the [[undercategory]] $X/C$ inherit themselves structures of model categories whose [[fibrations]], [[cofibration]]s and [[weak equivalences]] are precisely the morphism that become fibrations, cofibrations and weak equivalences in $C$ under the forgetful functor $C/X \to C$ or $X/C \to C$.

=--

## Properties ##

+-- {: .num_prop #ModelStructureInheritsGoodProperties}
###### Proposition


If $C$ is

* a [[cofibrantly generated model category]]

* or a [[proper model category]]

* or a [[cellular model category]]

then so are $C/X$ and $X/C$.

=--

The proofs are in ([OvMod](#OvMod)).

+-- {: .num_cor #ModelStructureInheritsCombinatorial}
###### Proposition

If $C$ is a [[combinatorial model category]], then so is $C/X$.

=--

+-- {: .proof}
###### Proof

By [basic properties](http://ncatlab.org/nlab/show/locally+presentable+category#Properties) of [[locally presentable categories]] they are stable under slicing. Hence with $C$ locally presentable also $C/X$ is, 
and by prop. \ref{ModelStructureInheritsGoodProperties} with $C$ cofibrantly
generated also $C/X$ is. 

=--

+-- {: .num_prop #PresentationOfSliceInfinityCat}
###### Proposition

If $C$ is a [[simplicial model category]] and $X \in C$ is fibrant, then
the [[overcategory]] $C/X$ with the above slice model structure is a [[presentable (infinity,1)-category|presentation]] of the 
[[over-(∞,1)-category]] $C^\circ / X$: we have an [[equivalence of (∞,1)-categories]]

$$
  (C/X)^\circ \simeq C^\circ / X
  \,.
$$

=--


+-- {: .proof}
###### Proof

It is clear that we have an [[essentially surjective (∞,1)-functor]] $C^\circ/X \to (C/X)^\circ$. What has to be shown is that this is a [[full and faithful (∞,1)-functor]] in that it is an [[equivalence in an (∞,1)-category|equivalence]] on all [[hom-object|hom]]-[[∞-groupoid]]s $C^\circ/X(a,b) \simeq (C/X)^\circ(a,b)$.

To see this, notice that the hom-space in an [[over-(∞,1)-category]] $C^\circ/X$ between objects $a : A \to X$ and $b : B \to X$ is given (as discussed there) by the 
[[(∞,1)-pullback]]

$$
  \array{
    C^\circ/X(A \stackrel{a}{\to} X, B \stackrel{b}{\to} X) 
     &\to& C^\circ(A,B)
    \\
    \downarrow && \downarrow^{\mathrlap{b_*}}
    \\
    {*} &\stackrel{a}{\to}& C^\circ(A,X)
  }
$$

in [[∞Grpd]].

Let $A \in C$ be a cofibrant representative and $b : B \to X$ be a 
fibration representative in $C$ (which always exists) of the objects of these names in $C^\circ$, respectively. In terms of these we have a cofibration

$$
  \array{
    \emptyset &&\hookrightarrow&& A
    \\
    & \searrow && \swarrow_{\mathrlap{a}}
    \\ 
    && X
  }
$$

in $C/X$, exhibiting $a$ as a cofibrant object of $C/X$;  and a fibration

$$
  \array{
    B &&\stackrel{b}{\to}&& X
    \\
    & {}_{\mathllap{b}}\searrow && \swarrow_{\mathrlap{Id}}
    \\ 
    && X
  }
$$

in $C/X$, exhibiting $b$ as a fibrant object in $C/X$.
 
Moreover, the diagram in [[sSet]] given by

$$
  \array{
    C/X(a, b) &\to& C(A,B)
    \\
    \downarrow && \downarrow^{\mathrlap{b_*}}
    \\
    {*} &\stackrel{a}{\to}& C(A,X)
  }
$$

is 

1. a [[pullback]] diagram in [[sSet]] (by the definition of morphism in an ordinary [[overcategory]]);

1. a [[homotopy pullback]] in the [[model structure on simplicial sets]], because  by the axioms on the [[sSet]]${}_{Quillen}$ [[enriched model category]] $C$ and the above (co)fibrancy assumptions, all objects are [[Kan complex]]es and the right vertical morphism is a [[Kan fibration]]. 

1. has in the top left the correct [[derived hom-space]] in $C/X$ (since $a$ is cofibrant and $b$ fibrant).

This means that this correct hom-space $C/X(a,b) \simeq (C/X)^\circ(a,b) \in sSet$ is indeed a model for $C^\circ/X(a,b) \in \infty Grpd$.

=--


## Related concepts


* [[over-category]] 

  * [[slice category]] 

  * [[under category]] 

  * [[over topos]]


* [[over (∞,1)-category]],

  * **model structure on an over-category**

  * [[over-(∞,1)-topos]]


## References ##

* Hirschhorn, _Overcategories and undercategories of model categories_ ([pdf](http://www-math.mit.edu/~psh/undercat.pdf))
{#OvMod}

[[!redirects model structure on an overcategory]]
[[!redirects model structure on an under category]]
[[!redirects model structure on an undercategory]]