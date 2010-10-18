
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

When regarding a [[sheaf]] as a [[space]] defined by how it is probed by test spaces, a _concrete sheaf_ is a generalized space that has (at least) an _underlying [[set]] of points_ out of which it is built.

So a concrete sheaf models a [[space]] that is given by a set of points and a choice of which morphisms of [[set]]s from concrete test spaces into it count as "structure preserving" (e.g. count as smooth, when the sheaf models a [[smooth space]]).

More in the intrinsic language of [[sheaves]], a _concrete sheaf_ is a [[sheaf]] on a [[concrete site]] $C$ that, while perhaps not [[representable functor|representable]], is "quasi-representable" in that it is a [[subobject]] of a sheaf of the form

$$
  U \mapsto Hom_{Set}(|U|, S)
$$

where $S$ is a [[set]] and $|U|$ is the [[set]] $|U| := Hom_C({*}, U)$ of points underlying the object $U$ in the [[concrete site]] $C$.

## Definition


+-- {: .un_def}
###### Definition

A **[[concrete site]]** is a [[site]] $C$ with a [[terminal object]] $*$ such that

1. the functor $Hom_C(*,-) : C \to Set$ is a [[faithful functor]];

1. for every [[coverage|covering family]] $\{f_i : U_i \to U\}$ in $C$ the morphism 

   $$
      \coprod_i Hom_C(*,f) : \coprod_i Hom_C(*, U_i) \to Hom_C(*, U) 
   $$

   is [[surjective]].

=--

For $F \in PSh(C)$ any [[presheaf]], write

$$
  \tilde F_U : F(U) \to Hom_{Set}(Hom_C(*,U), F(*)) 
$$

for the [[adjunct]] of the restriction map

$$
  F(U) \times Hom_C(*,U) \to F(*)
  \,,
$$

which in turn is the adjunct of the component map of the functor

$$
  F_{*,U} . Hom_C(*,U) \to Hom_{Set}(F(U), F(*))
  \,.
$$

+-- {: .un_def}
###### Definition

A [[presheaf]] $F : C^{op} \to Set$ on a [[concrete site]] is a **concrete presheaf** if for each $U \in C$ the map $\tilde F_U : F(U) \to Hom_{Set}(Hom_C(*,U), F(*))$ is [[injective]].

=--

So a concrete presheaf $F$ is a [[subobject]] of the presheaf $U \mapsto Hom_{Set}(Hom_C(*,U), F(*))$.

Write $ConPSh(C) \hookrightarrow PSh(C)$ for the [[full subcategory]] on concrete presheaves.


## Properties


+-- {: .un_prop}
###### Proposition

The category of concrete presheaves $ConPSh(C) \hookrightarrow PSh(C)$ is a [[reflective subcategory]] of the [[category of presheaves]].

The [[left adjoint]] functor $conc$ -- **concretization** --

$$
  ConPSh(C) \stackrel{\overset{conc}{\leftarrow}}{\hookrightarrow} PSh(C)
$$

sends a presheaf $F$ to the [[image]] sheaf

$$
  conc F : U \mapsto Im(\tilde F_U : F(U) \to Hom_{Set}(Hom_C(*,U), F(*)))
  \,.
$$

=--



Recall that the [[category of sheaves]] $Sh(C)$ on $C$ is a [[topos]] (a [[Grothendieck topos]]).


+-- {: .un_prop}
###### Proposition


The [[full subcategory]]

$$
  ConSh(C) \hookrightarrow Sh(C)
$$

on concrete sheaves is a [[quasitopos]].

=--


### A more abstract perspective

Note that taking $U=*$ in the second condition defining a concrete site implies that any covering family of $*$ contains a [[split epimorphism]], or equivalently that the only covering [[sieve]] of $*$ is the maximal sieve consisting of all morphisms with [[target]] $*$.  This means that a concrete site is in particular a [[local site]], which implies that its topos of sheaves is a [[local topos]].

Therefore, in the [[global sections]] [[geometric morphism]] $(L Const,\Gamma)\colon Sh(C) \to Set$, the right adjoint $\Gamma$ (which is just $F\mapsto F(*)$) has a further right adjoint $Ctr\colon Set\to Sh(C)$, which sends a set $A$ to the functor $U\mapsto Hom_{Set}(Hom(*,U),A)$.  Moreover, this right adjoint $Ctr$ is fully faithful and thus embeds $Set$ as a [[subtopos]] of $Sh(C)$.  The composite $Ctr \circ \Gamma$ which maps a sheaf $F$ to the sheaf $U\mapsto Hom_{Set}(Hom_C(*,U),F(*))$ is the [[reflector]] corresponding to this subtopos, and also has a corresponding [[Lawvere-Tierney topology]] on $Sh(C)$.

The concrete sheaves on $C$ are precisely the [[separated presheaf|separated objects]] for this Lawvere-Tierney topology on $Sh(C)$.  In particular, this implies immediately that they are reflective, with the reflector constructed as above, and that they form a [[quasitopos]].


## Examples

* The concrete sheaves on the [[concrete site]] [[CartSp]] are the [[diffeological space]]s.



## References 

Categories of concrete sheaves, with special attention to sheaves on [[CartSp]], i.e. to [[diffeological space]]s, are discussed in detail in 

* [[John Baez]], [[Alex Hoffnung]], _Convenient Categories of Smooth Spaces_, to appear in Trans. Amer. Math. Soc. ([arXiv](http://arxiv.org/abs/0807.1704))

[[!redirects concrete sheaves]]
[[!redirects concrete presheaf]]
[[!redirects concrete presheaves]]
