
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A [[site]] is **$\infty$-local** if it satisfies sufficient conditions for the [[(∞,1)-sheaf (∞,1)-topos]] over it to be a [[local (∞,1)-topos]].



## Definition

+-- {: .un_def}
###### Definition

A [[site]] $C$ is **$\infty$-local** if 

* it has a [[terminal object]] $*$;

* the [[limit]]-functor $\lim_\leftarrow : [C^{op}, sSet] \to$ [[sSet]]
  sends [[Cech nerve]] projections $C(U) \to X$ over [[covering]] families
  $\{U_i \to X\}$ to [[weak homotopy equivalence]]s:

  $$
    Hom_C(*, C(U)) \stackrel{\simeq}{\to} Hom_C(*,X)
    \,.
  $$

=--


+-- {: .un_remark}
###### Remark

If $C$ is also a [[strongly ∞-connected site]] then it is an [[∞-cohesive site]].

=--

## Proposition

+-- {: .un_theorem}
###### Theorem

For $C$ an $\infty$-local site, the [[(∞,1)-sheaf (∞,1)-topos]] $Sh_{(\infty,1)}(C)$ over it is a [[local (∞,1)-topos]], in that the [[global section]] [[(∞,1)-geometric morphism]] has a further right [[adjoint (∞,1)-functor]]

$$
  Sh_{(\infty,1)}
  \stackrel{\overset{\nabla}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{\nabla}{\leftarrow}}}
  \infty Grpd
  \,.
$$

=--

+-- {: .proof}
###### Proof

We may [[presentable (∞,1)-category|present]] the [[(∞,1)-sheaf (∞,1)-topos]] by the local [[model structure on simplicial presheaves]]

$$
  Sh_{(\infty,1)}(C) \simeq [C^{op},sSet]_{proj,loc}^\circ
  \,.
$$

For the notation see the details of the analagous proof at [[∞-connected site]]. As discussed there, the functor $\Gamma$ is given by evaliation on the terminal object. At the level of [[simplicial presheaves]] the [[sSet]]-[[enriched functor|enriched]] [[right adjoint]] to $\Gamma$ is given by 

$$
  \nabla S : U \mapsto sSet(\Gamma(U), S)
$$

as confirmed by the following [[end]]/[[coend]] calculus computation:

$$
  \begin{aligned}
    [C^{op}, sSet](X, \nabla(S))
    & =
    \int_{U \in C} sSet(X(U), sSet(\Gamma(U), S)
    \\
    & = \int_{U \in C} sSet(X(U) \times \Gamma(U), S)
    \\
    & = sSet( \int^{U \in C} X(U) \times \Gamma(U), \;\; S )
    \\
    & = sSet( \int^{U \in C } X(U) \times Hom_C(*, U), \;\; S)
    \\
    & = sSet(X(*), S)
    \\
    & = sSet(\Gamma(X), S)
  \end{aligned}
  \,,
$$

where in the second but last step we used the [[co-Yoneda lemma]].

It is clear that 

$$
  (\Gamma \dashv \nabla)
    : 
  [C^{op}, sSet]_{proj} \stackrel{\overset{\Gamma}{\to}}{\underset{\nabla}{\leftarrow}}
  sSet_{Quillen}
$$

is a [[Quillen adjunction]], since $\nabla$ manifestly preserves fibrations and acyclic fibrations. Since $[C^{op}, sSet]_{proj,loc}$ is a [[left proper model category]] to see that this descends to a Quillen adjunction on the 
[[local model structure on simplicial presheaves]] it is sufficient to check that $\nabla : sSet_{Quillen} \to  [C^{op}, sSet]_{proj,loc}$ preserves fibrant objects, in that for $S$ a [[Kan complex]] we have that $\nabla S$ satisfies [[descent]] along [[Cech nerve]]s of covering families. 

This follows from the second defining condition on the $\infty$-local site $C$, that $Hom_C(*,C(U)) \simeq Hom_C(*,U)$. Using this we have for fibrant $S \in sSet_{Quillen}$ the descent weak equivalence

$$
  [C^{op}, sSet](U, \nabla S)
   =
  sSet(Hom_C(*,U), S)  
   \simeq
  sSet(Hom_C(*,C(U)), S)
   =
  [C^{op}, sSet](C(U), \nabla S)
  \,,
$$

where we use in the middle step that $sSet_{Quillen}$ is a [[simplicial model category]] so that homming the weak equivalence between cofibrant objects into the fibrant object $S$ indeed yields a weak equivalence (using the [[factorization lemma]]).

=--

## Examples

* [[CartSp]], [[ThCartSp]]


## Related concepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]

and

* [[locally connected site]] / [[locally ∞-connected site]]

  * [[connected site]] / [[∞-connected site]]

  * [[strongly connected site]] / [[strongly ∞-connected site]]

  * [[totally connected site]] / [[totally ∞-connected site]]

* [[local site]] / **∞-local site**

* [[cohesive site]], [[∞-cohesive site]]


[[!redirects ∞-local site]]

[[!redirects ∞-local sites]]
[[!redirects infinity-local sites]]
