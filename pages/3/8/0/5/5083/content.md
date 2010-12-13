
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

Just as the [[shape of an (∞,1)-topos]] is the functor $\infty Gpd\to \infty Gpd$ which it *corepresents* (after identifying ∞-groupoids with their presheaf (∞,1)-topoi), so the *coshape* of an (∞,1)-topos is the functor $\infty Gpd^{op}\to \infty Gpd$ which it *represents*.

Unlike the shape, which is only (co)representable (by an ∞-groupoid) when the topos is [[locally ∞-connected (∞,1)-topos|locally ∞-connected]], the coshape is *always* representable, albeit possibly by a *large* ∞-groupoid---specifically the ∞-groupoid of [[point of a topos|points]] of the (∞,1)-topos in question.


+--{: .standout}
For notational simplicity, on this page we will write $Topos$ to mean the $(\infty,1)$-category [[(∞,1)Topos]] of (∞,1)-topoi, and $Psh\colon \infty Gpd \hookrightarrow Topos$ for the embedding which sends an $\infty$-groupoid $A$ to its [[(∞,1)-category of (∞,1)-presheaves]] $Psh(A) = Func(A,\infty Gpd)$.
=--


## Definition

+-- {: .un_defn}
###### Definition

For $\mathbf{H}$ an [[(∞,1)-topos]], we say its **co-shape** $\Gamma \mathbf{H}$ is the functor $\Gamma(\mathbf{H}) \colon \infty Gpd^{op}\to \infty Gpd$ defined by

$$
  \Gamma(\mathbf{H})(A) =
  Topos(PSh(A), \mathbf{H})
$$

=--

Let $Pt(\mathbf{H}) = Topos(*,\mathbf{H})$ denote the (possibly large) $\infty$-groupoid of *points* of $\mathbf{H}$, where $*$ denotes the terminal $(\infty,1)$-topos $\infty Gpd$.

+-- {: .un_prop}
###### Proposition

The coshape $\Gamma(\mathbf{H})$ is represented by $Pt(\mathbf{H})$, i.e. for any (small) $\infty$-groupoid $A$ we have
$$ \Gamma(\mathbf{H})(A) \simeq \infty GPD(A, Pt(\mathbf{H})). $$

=--

+-- {: .proof}
###### Proof

Recall that colimits in $Topos$ are calculated via *limits* on the level of underlying $(\infty,1)$-categories.  In particular, the [[copower]] of $\mathbf{K}$ by an $\infty$-groupoid $A$ is the $(\infty,1)$-topos $\mathbf{K}^A$.

Thus, in even more particular, the functor $Psh$ preserves copowers, since each $\infty$-groupoid is the copower of the terminal object by itself.  Therefore, we have $Topos( Psh(A), \mathbf{H} ) \simeq \infty GPD(A, Topos( *, \mathbf{H} )) = \infty GPD(A,Pt(\mathbf{H}))$, as desired.

=--


## In terms of Universe Enlargements

Another way of phrasing the above argument is as follows.  For the same reason cited in the proof, the embedding $Psh$ preserves all small colimits.  Therefore, since $\Gamma(\mathbf{H}) \colon \infty Gpd^{op}\to \infty Gpd$ is the composite of this embedding with the representable functor $Topos(-,\mathbf{H})$, it must also preserves all small limits in $\infty Gpd^{op}$ (i.e. small colimits in $\infty Gpd$).

Therefore, we can regard it as an object of the category $Cts(\infty Gpd^{op},\infty Gpd)$ of small-limit-preserving functors, also known as the [[very large (∞,1)-sheaf (∞,1)-topos]] on [[?Gpd]] (and also the $\kappa$-[[ind-object in an (∞,1)-category|ind-objects]] of [[?Gpd]], for $\kappa$ the cardinality of the universe).  However, by the general theory of [[universe enlargement]], this category is equivalent to $\infty GPD$, and the equivalence gives the representability theorem above.


### Enlarging the category of toposes

Instead of being content with a "large-representability" result as above, we might wish that the coshape would actually give us a right adjoint to the embedding $Psh$.  For this to be possible, we would need to enlarge $\infty Gpd$ to $\infty GPD$, but if we also enlarged $Topos$ to its naive enlargement $TOPOS$, we would face the same problem "one universe higher."

Thus, to get "better behavior" we can instead replace $Topos$ by its locally presentable enlargement $\Uparrow Topos$, also called the [[very large (∞,1)-sheaf (∞,1)-topos]] on $Topos$.  We can then say:

+-- {: .un_prop}
###### Proposition

Coshape [[Yoneda extension|Yoneda-extends]] to a pair of [[adjoint (∞,1)-functor]]s

$$
  \infty GPD
  \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{Codisc}{\to}}
  \Uparrow Topos.
$$

=--

+-- {: .proof}
###### Proof

By [[Higher Topos Theory|HTT, lemma 6.3.5.21]] we have an [[(∞,1)-functor]] 

$$
  \Uparrow Topos
  \to 
  \Uparrow \infty Grpd = \infty GRPD
$$

that preserves $\mathcal{U}$-small colimits and finite limits and is given by sending

$$
  F : Topos^{op} \to \infty Grpd
$$

to the composite

$$
   \infty Grpd
   \stackrel{PSh(-)}{\to}
   (Topos/\infty Grpd)_{et}^{op}
   \stackrel{}{\to}
   Topos^{op}
   \stackrel{F}{\to}
   \infty Grpd
  \,,
$$

where the first step is forming [[(∞,1)-presheaf (∞,1)-topos]]es which sit by their terminal [[global section]] [[(∞,1)-geometric morphism]] over [[∞Grpd]] and the second step is the evident projection.

Applied to a [[representable functor|representable]] 
$F = Topos(-,\mathbf{H})$ this composite is hence $A \mapsto \Gamma(\mathbf{H})(A)$.

=--


## Related concepts

* [[shape of an (∞,1)-topos]]

* **coshape of an $(\infty,1)$-topos**


[[!redirects coshape of an (∞,1)-topos]]
