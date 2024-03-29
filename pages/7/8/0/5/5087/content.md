
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
* table of contents
{:toc}

 
## Definition

+-- {: .num_defn #EquivalentDefinitions}
###### Definition

A [[geometric morphism]] between [[toposes]] $(f^* \dashv f_*) : \mathcal{E} \to \mathcal{F}$ is **surjective** or a **geometric surjection** if it satisfies the following equivalent criteria:

* its [[inverse image functor]] $f^*$ is [[faithful functor|faithful]] (in contrast to the [[direct image]] being [[full and faithful functor|full and faithful]] as for a [[geometric embedding]]); 

* its [[inverse image functor]] $f^*$ is [[conservative 
functor|conservative]];

* the components $X \to f_* f^* X$ of the [[unit of an adjunction|adjunction unit]] are [[monomorphism]]s, for all $X \in \mathcal{F}$;

* $f^*$ induces a injective homomorphism of [[subobject]] [[lattice]]s
  
  $$
    Sub(X) \hookrightarrow Sub(f^* X)
  $$

  for all $X \in \mathcal{F}$;

* $f^*$ reflects the order on [[subobject]]s;

* $(f^* \dashv f_*)$ is a [[comonadic adjunction]].

=--

The equivalence of these condition appears for instance as [MacLaneMoerdijk, VII 4. lemma 3 and prop. 4](#MacLaneMoerdijk).

+-- {: .proof}
###### Proof

We discuss the equivalence of these conditions:

The equivalence $(f^* \; faithful) \Leftrightarrow (Id \to f^* f_* \;is \; mono)$ is a general property of [[adjoint functors]] (see there). 

The implication $(f^* faithful) \Rightarrow (f^* induces\;injection\;on\;subobjects)$ works as follows: 

first of all $f^*$ does indeed preserves subobjects: since it respects [[pullback]]s and since [[monomorphism]]s are characterized as those morphisms whose domain is stable under pullback along themselves.

To see that $f^*$ induces an injective function on subobjects let $U \hookrightarrow X$ be a subobject with characteristic morphism $char U : X \to \Omega$ and consider the image

$$
  \array{
    f^* U &\to& f^* * \simeq *
    \\
    \downarrow && \downarrow
    \\
    f^* X &\stackrel{f^* char U}{\to}& f^* \Omega
  }
  \,.
$$

of the pullback diagram that exhibits $U$ as a subobject. Since $f^*$ preserves pullbacks, this is still a pullback diagram. 

If now $U \leq \tilde U$ but $f^* (U) = f^*(\tilde U)$ then both corresponding pullback diagrams are sent by $f^*$ to the same such diagram. By faithfulness this implies that also

$$
  \array{
    \tilde U &\to& * 
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{char U}{\to}& \Omega
  }
$$

commutes, and hence that also $\tilde U \subset U$, so that in fact $\tilde U \simeq U$.

Next we consider the implication ($f^*$ induces injection on subobjects) $\Rightarrow$ ($f^*$ is conservative).

Assume $f^* (X \stackrel{\phi}{\to} X')$ is an isomorphism. We have to show that then $\phi$ is an isomorphism. Consider the [[image]] factorization $X \to im(\phi) \hookrightarrow X'$. Since $f^*$ preserves pushouts and pullbacks, it preserves epis and monos and so takes this to the image factorization 

$$  
  f^* X \to f^* (im \phi) \stackrel{\simeq}{\to} f^* X'
$$

of $f^* \phi$, where now the second morphism is an iso, because $f^* \phi$ is assumed to be an iso. By the assumption that $f^* $ is injective on subobjects it follows that also $im \phi \simeq X'$ and thus that $\phi$ is an epimorphism.

It remains to show that $\phi$ is also a monomorphism. For that it is sufficient to show that in the pullback square

$$
  \array{
    X \times_{X'} X &\to& X
    \\
    \downarrow && \downarrow^{\mathrlap{\phi}}
    \\
    X &\stackrel{\phi}{\to}& X'
  }
$$

we have $X \times_{X'} X \simeq X$. Write $\Delta : X \to X \times_{X'} X$ for the [[diagonal]] and let

$$
  X \to im \Delta_\phi \to X \times_{X'} X
$$

be its [[image]] factorization. Doing the same for $f^* \phi$, which we have seen is a monomorphism, and using that $f^*$ preserves the pullback,  we get

$$
  f^* im \Delta_\phi \simeq f^* (X \times_{X'} X)
  \,.
$$

Now using again the assumption that $f^*$ is injective on subobjects, this implies $im \Delta_\phi = X \times_{X'} X$ and hence that $\phi$ is a monomorphism.

(...)

The statement about the comonadic adjunction we discuss below as prop. \ref{Comonadicity}.

=--

## Properties

### Surjection/embedding factorization

+-- {: .num_prop #CofreeAlgebraFunctorIsSurjective}
###### Observation

For $T : \mathcal{E} \to \mathcal{E}$ a [[left exact functor|left exact]] [[comonad]] the cofree algebra functor

$$
  F : \mathcal{E} \to T CoAlg(\mathcal{E})
$$

to the [[topos of coalgebras]] is a geometric surjection.

=--

+-- {: .proof}
###### Proof

By the discussion at [[topos of coalgebras]] the [[inverse image]] is the [[forgetful functor]] to the underlying $\mathcal{E}$-objects. This is clearly a [[faithful functor]].

=--

+-- {: .num_prop #Comonadicity}
###### Proposition

Up to [[equivalence of categories|equivalence]], every geometric surjection is of this form.

=--

This appears for instance as ([MacLaneMoerdijk, VII 4., prop 4](#MacLaneMoerdijk)).

+-- {: .proof}
###### Proof

With observation \ref{CofreeAlgebraFunctorIsSurjective} we only need to show that if $f : \mathcal{E} \to \mathcal{F}$ is surjective, then there is $T$ such that

$$
  \array{
     \mathcal{E} &\stackrel{f}{\to}& \mathcal{F}
     \\
     & {}_{\mathllap{F}}\searrow & \downarrow^{\mathrlap{\simeq}}
     \\
     && T CoAlg(\mathcal{E})
  }
  \,.
$$

For this, take $T := f^* f_*$. This is a [[left exact functor]] by definition of [[geometric morphism]]. By assumption on $f$ and using the equivalent definition of def. \ref{EquivalentDefinitions} we have that $f^*$ is a [[conservative functor]]. This means that the conditions of the [[monadicity theorem]] are met, so so $f^*$ is a [[monadic functor|comonadic functor]]. 

=--

For more on this see _[[geometric surjection/embedding factorization]]_  . Also at _[[monadic descent]]_.

## Examples

Trivially, any [[connected geometric morphism]] is surjective.

+-- {: .num_prop}
###### Proposition

For $f : X \to Y$ a [[continuous function]] between [[topological space|topological spaces]] and $(f^* \dashv f_*) : Sh(X) \to Sh(Y)$ the corresponding geometric morphism of [[sheaf topos|sheaf toposes]]: if $f$ is surjective then $(f^* \dashv f_*)$ is a surjective geometric morphism, conversely, if $(f^* \dashv f_*)$ is a surjective geometric morphism and $Y$ a $T_1$-space then $f$ is surjective.
=--

For a proof see e.g [MacLane-Moerdijk](#MacLaneMoerdijk), p.367. A similar result holds for injective functions and [[geometric embedding|geometric embeddings]] but there $T_0$ suffices as a [[separation axiom|separation requirement]] on $X$.

## Related concepts

* [[geometric morphism]]

  * **geometric surjection**

  * [[geometric embedding]]

  * [[connected geometric morphism]]

* [[monadic descent]]

## References

* {#Johnstone77} [[Peter Johnstone]], _Topos Theory _ , Academic Press New York 1977. (Available as Dover reprint 2014; Section 4.1) 

* {#MacLaneMoerdijk} [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ , Springer Heidelberg 1994. (Section VII.4)
 
[[!redirects surjective geometric morphisms]]
[[!redirects geometric surjection]]
[[!redirects geometric surjections]]