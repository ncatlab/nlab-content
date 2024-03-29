
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


# Localic geometric morphisms
* table of contents
{: toc}

## Definition

A [[geometric morphism]] $f\colon E\to F$ between [[topoi]] is **localic** if every [[object]] of $E$ is a [[subquotient]] of an object in the [[inverse image]] of $f$: of the form $f^*(x)$.


## Examples

* Any geometric morphism between [[localic topoi]] is localic.

* Any [[geometric embedding]] is localic.

* Any [[étale geometric morphism]] is localic. From the [[internal language|point of view]] of a base topos $F$, an étale geometric morphism $F/A \to F$ looks like the unique geometric morphism $\Sh(A) \to Set$ attached to the topos of sheaves over the discrete locale $A$.

* If $g:C\to D$ is a [[faithful functor]] between [[small categories]], then the induced geometric morphism $Set^C \to Set^D$ is localic.


## Properties

+-- {: .un_prop}
###### Proposition

A [[Grothendieck topos]] is a [[localic topos]] if and only if its unique [[global section]] geometric morphism to [[Set]] is a localic geometric morphism.  

=--

Thus, in general we regard a localic geometric morphism $E\to S$ as exhibiting $E$ as a "localic $S$-topos".




This is supported by the following fact. 

+-- {: .un_prop}
###### Proposition


For any base $S$, the [[2-category]] of localic $S$-toposes (i.e. the full sub-2-category 

  $$
    (Topos/S)_{loc} \subset Topos/S
  $$

of the [[over-category]] [[Topos]] over $S$ spanned by the localic morphisms into $S$) is equivalent to the 2-category of [[internalization|internal]] [[locales]] in $S$

$$
  Loc(S) \simeq (Topos/S)_{loc}
$$

Concretely, the internal locale in $\mathcal{E}$ defined by a localic geometric morphism $(f^* \dashv f_*) : \mathcal{F} \to \mathcal{E}$ is the formal dual to the [[direct image]] $f_*(\Omega_{\mathcal{F}})$ of the [[subobject classifier]] of $\mathcal{F}$, regarded as an internal poset (as described there) and $\mathcal{F}$ is equivalent to the internal [[category of sheaves]] over $f_*(\Omega_{\mathcal{F}})$.

=--

The last bit is lemma 1.2 in ([Johnstone](#Johnstone)).


+-- {: .un_prop}
###### Proposition


Localic geometric morphisms are the right class of a 2-categorical [[orthogonal factorization system]] on the 2-category [[Topos]] of topoi. The corresponding left class is the class of [[hyperconnected geometric morphism]]s.

([[(hyperconnected,localic) factorization system]])

=--

This is the main statement in ([Johnstone](#Johnstone)).


## References

Localic geometric morphisms are defined in def. 4.6.1 of

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

The discussion there is based on

* [[Peter Johnstone]], _Factorization theorems for geometric morphisms_ Cahiers, 22, no1 (1981) ([numdam](http://www.numdam.org/item?id=CTGDC_1981__22_1_3_0))
{#Johnstone}

[[!redirects localic geometric morphism]]
[[!redirects localic geometric morphisms]]
