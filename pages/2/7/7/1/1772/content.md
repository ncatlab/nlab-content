
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

We discuss two definitions: the first one is more elementary and describes concrete sheaves explicitly in terms of properties of the underlying [[site]]. 

The second one is more abstract and more general, and describes them entirely [[topos theory|topos theoretically]].

### On a concrete site

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

For $X \in PSh(C)$ any [[presheaf]], write

$$
  \tilde X_U : X(U) \to Hom_{Set}(Hom_C(*,U), X(*)) 
$$

for the [[adjunct]] of the restriction map

$$
  X(U) \times Hom_C(*,U) \to X(*)
  \,,
$$

which in turn is the adjunct of the component map of the functor

$$
  X_{*,U} . Hom_C(*,U) \to Hom_{Set}(X(U), X(*))
  \,.
$$

{#ConcSheafOnConcSite}
+-- {: .un_def}
###### Definition

A [[presheaf]] $X : C^{op} \to Set$ on a [[concrete site]] is a **concrete presheaf** if for each $U \in C$ the map $\tilde X_U : X(U) \to Hom_{Set}(Hom_C(*,U), X(*))$ is [[injective]].

A **concrete sheaf** is a presheaf that is both concrete and a [[sheaf]].

=--

So a concrete presheaf $X$ is a [[subobject]] of the presheaf $U \mapsto Hom_{Set}(Hom_C(*,U), X(*))$.

Write $Conc(Sh(C)) \hookrightarrow Sh(C)$ for the [[full subcategory]] of the [[category of sheaves]] on concrete sheaves.




### In a local topos

A more abstract perspective on the [previous definition](#ConcSheafOnConcSite) is obtained by noticing the following.

+-- {: .un_lemma}
###### Lemma

The [[category of sheaves]] on a [[concrete site]] is a [[local topos]].

=--

+-- {: .proof}
###### Proof

Taking $U=*$ in the second condition defining a concrete site implies that any [[covering]] family of $*$ contains a [[split epimorphism]], or equivalently that the only covering [[sieve]] of $*$ is the maximal sieve consisting of all morphisms with [[target]] $*$.  This means that a concrete site is in particular a [[local site]], which implies that its topos of sheaves is a [[local topos]].

=--

In fact, we can formulate the definition of concrete sheaf inside any [[local topos]] $E$ over any base topos $S$:

+-- {: .un_def}
###### Definition

Let 

$$(Disc \dashv \Gamma \dashv Codisc) : E \stackrel{\stackrel{\overset{Disc}{\leftarrow}}{\underset{\Gamma}{\to}}}{\underset{Codisc}{\leftarrow}} S$$

be a [[local topos]]. Since then by definition $S \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{Codisc}{\hookrightarrow}} E$ is a [[subtopos]] the morphisms $V = \Gamma^{-1}(isos(S)) \subset Mor E$ that are inverted by $\Gamma$ are the [[local isomorphism]]s with respect to which the objects of $S$ are [[sheaves]]/$V$-[[local object]]s in $E$.

The **concrete sheaves** are the objects of $E$ that are the $V$-[[separated presheaf|separated objects]]. 


=--

+-- {: .un_prop}
###### Proposition

For $E = Sh(C) \stackrel{\Gamma = Hom(*,-)}{\to} Set$ the [[category of sheaves]] on a [[concrete site]], this is equivalent to the 
[previous definition](#ConcSheafOnConcSite).

=--

+-- {: .proof}
###### Proof

Since $C$ is concrete, in the [[global sections]] [[geometric morphism]] $(L Const,\Gamma)\colon Sh(C) \to Set$, the [[direct image]] $\Gamma$ is evaluation on the point: $X\mapsto X(*)$. The further [[right adjoint]] $Codisc \colon Set\to Sh(C)$, sends a set $A$ to the functor $U\mapsto Hom_{Set}(Hom_C(*,U),A)$.  Moreover, this right adjoint $Codisc$ is [[full and faithful functor|fully faithful]] and thus embeds $Set$ as a [[subtopos]] of $Sh(C)$.  

We observe that $ (\Gamma \dashv Codisc) : Set \to  Sh(C)$ is the [[localization]] of $Sh(C)$ at the set $\{L Const \Gamma U \to U | U \in C\}$ of counits of the adjunction $(L Const \dashv \Gamma)$ on representables: because if for $X \in Sh(C)$ we have that

$$
  \begin{aligned}
     Hom_{Sh(C)}(L Const \Gamma U \to U, X) 
     & = (X(U) \to Hom_{Set}(\Gamma(U), \Gamma(X)))
     \\
     & = (X(U) \to Hom_{Set}(Hom_C(*,U)), X(*))
  \end{aligned}
$$

is an [[isomorphism]], then clearly $X = Codisc(X(*))$.

On the other hand, comparison with the [previous definition](#ConcSheafOnConcSite) shows that this is a [[monomorphism]] precisely if $X$ is a concrete sheaf.


=--




So the concrete sheaves on $C$ are precisely the [[separated presheaf|separated objects]] for this [[Lawvere-Tierney topology]] on $Sh(C)$ that corresponds to the subtopos $Codisc : S \hookrightarrow Sh(C)$.  



## Properties

Let $\Gamma : E \to S$ be a [[local topos]]. From the definition of concrete sheaves as [[separated presheaves]] it follows immediately that

+-- {: .un_prop}
###### Proposition

The category of concrete sheaves $Conc_\Gamma(E)$ forms a [[reflective subcategory]] of $E$

$$
  S 
   \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{Codisc}{\hookrightarrow}}
  Conc_\Gamma(E) 
    \stackrel{\overset{Conc}{\leftarrow}}{\hookrightarrow}
  E
$$

which is a [[quasitopos]]. 

The left adjoint $Conc$ is **concretization** which sends a sheaf $X$ to the [[image]] sheaf

$$
  Conc X : U \mapsto Im(X(U) \to Hom_{Set}(Hom_C(*,U), X(*)))
  \,.
$$

=--



## Examples

* The concrete sheaves on the [[concrete site]] [[CartSp]] are the [[diffeological space]]s.



## References 

Categories of concrete sheaves, with special attention to sheaves on [[CartSp]], i.e. to [[diffeological space]]s, are discussed in detail in 

* [[John Baez]], [[Alex Hoffnung]], _Convenient Categories of Smooth Spaces_, to appear in Trans. Amer. Math. Soc. ([arXiv](http://arxiv.org/abs/0807.1704))

[[!redirects concrete sheaves]]
[[!redirects concrete presheaf]]
[[!redirects concrete presheaves]]
