
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Given two [[monoidal categories]] $(V_1,\otimes_1, I_1)$ and $(V_2, \otimes_2, I_2)$ used for enrichment in [[enriched category theory]] (for instance two [[Bénabou cosmoi]]), a [[lax monoidal functor]] between them

$$
  F 
  \;\colon\;
  (V_1, \otimes_1, I_1)
    \longrightarrow
  (V_2, \otimes_2, I_2)  
$$

canonically induces a [[2-functor]]

$$
  F_\ast \;\colon\; V_1 Cat \longrightarrow V_2 Cat
$$

between [[categories of V-enriched categories]] sending a $V_1$-[[enriched category]] $\mathcal{C}$ to the $V_2$-[[enriched category]] $F_\ast(\mathcal{C})$ such that 

1. $F_\ast(\mathcal{C})$ has the same [[objects]] as $\mathcal{C}$;

1. the [[hom-objects]] of $F_\ast(\mathcal{C})$ are the [[images]] of the hom-objects of $\mathcal{C}$ under $F$:

   $$
     F_\ast(\mathcal{C})(x,y)
     \;\coloneqq\;
     F\big(\mathcal{C}(x,y)\big)
   $$

1. the [[composition]], [[unit]], [[associator]] and [[unitor]] [[morphisms]] in $F_\ast(\mathcal{C})$ are the [[images]] of those of $\mathcal{C}$ composed with the structure morphisms of the [[lax monoidal functor|lax monoidal]]-[[structure]] on $F$.

([Eilenberg-Kelly 65](#EilenbergKelly65))

This operation $F_\ast$ is sometimes called **change of enriching category** or **change of enriching base** or just **change of base** (e.g. [Crutwell 14, chapter 4](#Crutwell14), [Riehl 14, lemma 3.4.3](#Riehl14)). But notice that, despite some vague similarity, this is different from [[base change]] of [[slice categories]].

In the special case that $\mathcal{C}$ has a single object and is hence (if thought of as [[pointed object|pointed]] by that object) equivalently a [[monoid object]] in $V_1$, this statement reduces to the statement that lax monoidal functors preserve [[monoids]] ([this Prop.](monoidal+functor#MonoidsToMonoidsByLaxMonoidal))


## Generalizations and enhancements

* The operation of change of enriching category is functorial from [[MonCat]] to [[2Cat]].  In particular, any [[monoidal adjunction]] $V_1\rightleftarrows V_2$ gives rise to a [[2-adjunction]] $V_1 Cat\rightleftarrows V_2 Cat$ (and also for profunctors).

* $V$-enriched categories can be defined more generally when $V$ is a [[multicategory]], and any functor $F:V_1\to V_2$ between multicategories induces a change of enrichment 2-functor.  Note that a functor of multicategorise between the underlying multicategories of two monoidal categories corresponds to a *lax* monoidal functor, as in the original version above.  The multicategorical version also includes change of enrichment between [[closed categories]].

* A different generalization is when $V$ is a [[bicategory]], yielding [[bicategory-enriched categories]].  Any lax functor of bicategories induces a similar functor between its 2-categories of enriched categories.

* When $V_1$ and $V_2$ are cocomplete monoidal categories (or locally cocomplete bicategories), so that the bicategories $V_i$-[[Prof]] of $V_i$-categories and $V_i$-[[profunctors]] exist, change of enrichment also induces a [[lax functor]] $V_1 Prof \to V_2 Prof$.  To make this version functorial on $MonCat_{cocomplete}$, we need to consider $V_i Prof$ as [[double categories]], yielding a functor from [[MonCat]] to [[DblCat]].

* Finally, a generalization subsuming all of these is that for any [[virtual double category]] $V$ we can construct another virtual double category $V Prof$, and this construction is functorial.


## Examples

+-- {: .num_example #Underlying}
###### Example
For any a monoidal category $V$, the functor $V(I,-): V \to Set$ is lax monoidal, hence induces a 2-functor from $V Cat$ to $Cat$.  This assigns to any $V$-enriched category, $\mathcal{C}$, its [[underlying ordinary category]], usually denoted $\mathcal{C}_0$, defined by $\mathcal{C}_0(x,y) = V(I, hom(x,y))$.
=--

+-- {: .num_example #FreeCats}
###### Example
If $V$ is a [[cocomplete category|cocomplete]] monoidal category, the functor $V(I,-)$ above has a [[left adjoint]] that takes a set $X$ to the [[copower]] of $X$ copies of $I$.  The resulting 2-functor $Cat \to V Cat$ takes an ordinary category to the "free" $V$-category it generates.  Such $V$-categories are used, for instance, in subsuming "conical" [[limits]] under enriched [[weighted limits]].

By functoriality, the adjunction between these two functors gives rise to a 2-adjunction $Cat \rightleftarrows V Cat$.
=--

+-- {: .num_example #GenUnderlying}
###### Example
More generally, if an adjunction $F:V_1 \rightleftarrows V_2:U$ can be regarded as a [[free-forgetful adjunction]], then the corresponding adjunction between enriched categories can also be so regarded.  For instance, if $V_1 = Top$ and $V_2 = G Top$ for some [[topological group]] $G$, then the right adjoint $V_2 Cat \to V_1 Cat$ takes the "underlying topologically enriched category" of a category enriched in $G$-spaces (its morphisms are the fixed-point spaces of the original $G$-space-enriched category; we think of these as the "$G$-equivariant maps" while the original spaces consisted of not-necessarily-equivariant maps acted on by conjugation).  Similarly, any category enriched in [[spectra]] has an underlying category enriched in spaces (whose hom-spaces are the 0-spaces of the original hom-spectra), any [[dg-category]] has an underlying [[Ab-category]] (whose morphisms are the degree-0 ones in the original category), and so on.
=--

+-- {: .num_example #RealSing}
###### Example
The [[geometric realization]] and [[total singular complex]] adjunction $Real:SSet \rightleftarrows Top : Sing$ between [[simplicial sets]] and [[topological spaces]] induces another adjunction $SSet Cat \rightleftarrows Top Cat$ between [[simplicially enriched categories]] and [[topologically enriched categories]].
=--

+-- {: .num_example #HomotopyCat}
###### Example
If $V=$[[SSet]] or [[Top]], then the set of connected components $\pi_0:V\to Set$ is lax monoidal.  The resulting change of enrichment functor takes a $V$-category $C$ to its "naive homotopy category" $h C(x,y) = \pi_0(C(x,y))$ obtained by "identifying homotopic morphisms".

Similarly, the [[fundamental groupoid]] functor $\Pi_1:V\to Gpd$ is lax monoidal, so any $V$-category has an underlying [[(2,1)-category]].
=--

+-- {: .num_example #EnrichedHomotopyCat}
###### Example
An enhancement of the last example is that if $V$ is any [[monoidal model category]], then its [[homotopy category]] $Ho(V)$ comes with a lax monoidal functor $\gamma : V \to Ho(V)$.  Thus any $V$-category $C$ has an underlying $Ho(V)$-enriched "homotopy category" $h C$.  Usually the underlying ordinary category of $h C$ is the naive homotopy category from the previous example.
=--

+-- {: .num_example #Tau1}
###### Example
The nerve functor $N:Cat \to SSet$ preserves products and has a left adjoint $\tau_1$ that also preserves products.  Thus, we have a change of enrichment adjunction in which any [[2-category]] can be regarded as a [[simplicially enriched category]], and similarly any simplicially enriched category has a "homotopy 2-category".  The latter plays an important role in the theory of [[quasi-categories]].
=--

+-- {: .num_example #PolyMorphisms}
###### Example
**([[poly-morphisms]])**

For $F = P \;\colon\; Set \to Set$ the [[power set]]-[[functor]], the change of base functor $P_\ast \;\colon\;
 Cat \to Cat$ sends plain [[categories]] to plain categories. For $C$ any category, the morphisms of $C^{poly} \coloneqq P\ast(C)$ are called the _[[poly-morphisms]]_ of $C$ in [Mochizuki 12, section 0](poly-morphism#Mochizuki12).

=--

## References


* {#EilenbergKelly65} [[Samuel Eilenberg]], [[Max Kelly]], *Closed categories*,  Proc. Conf. Categorical Algebra (La Jolla, Calif., 1965), Springer (1966) &lbrack;[doi:10.1007/978-3-642-99902-4_22](https://doi.org/10.1007/978-3-642-99902-4_22)&rbrack;


* {#Crutwell14} [[Geoff Cruttwell]], chapter 4 of: _Normed spaces and the Change of Base for Enriched Categories_, 2014 ([pdf](https://www.reluctantm.com/gcruttw/publications/thesis4.pdf))


* {#Riehl14} [[Emily Riehl]], lemma 3.4.3 inL _[[Categorical Homotopy Theory]]_, Cambridge University Press (2014)

[[!redirects changes of enriching category]]
[[!redirects changes of enriching categories]]
[[!redirects change of enriching categories]]

[[!redirects change of enrichment]]
[[!redirects changes of enrichment]]
[[!redirects changes of enrichments]]

[[!redirects change of enriching base]]
[[!redirects changes of enriching base]]
[[!redirects changes of enriching bases]]

[[!redirects change of base in enriched category theory]]
[[!redirects changes of base in enriched category theory]]
[[!redirects changes of bases in enriched category theory]]



