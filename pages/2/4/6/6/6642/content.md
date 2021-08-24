

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
=--
=--



# Reflective factorization systems
* table of contents
{:toc}

## Idea

A *reflective factorization system* is an [[orthogonal factorization system]] $(E,M)$ that is determined by the [[reflective subcategory]] $M/1$.

## Definition

Let $C$ be a [[category]] with a [[terminal object]] $1$.  If $(E,M)$ is an (orthogonal) [[orthogonal factorization system|factorization system]] on $C$, then the [[full subcategory]] $M/1 \subseteq C$ (consisting of those objects $X$ for which $X\to 1$ is in $M$) is [[reflective subcategory|reflective]].  The reflection of $Y\in C$ is obtained by the $(E,M)$-factorization $Y \xrightarrow{e} \ell Y \xrightarrow{m} 1$. (e.g. ([Rosicky-Tholen 08, 2.10](#RosickyTholen08)))

In fact, in this we do not need $(E,M)$ to be a factorization system; only a [[orthogonal factorization system#prefactorization_systems|prefactorization system]] with the property that any morphism with [[terminal object|terminal]] [[codomain]] admits an $(E,M)$-factorization.  For the nonce, let us call such a prefactorization system *favorable*.

Conversely, suppose that $A\hookrightarrow C$ is a [[reflective subcategory]], and define $E$ to be the class of morphisms inverted by the [[reflector]] $\ell\colon C\to A$, and define $M = E^\perp$.  Then $(E,M)$ is a favorable prefactorization system.  In this way we obtain an [[adjunction]] 

$$ \Phi : \text{reflective subcategories} \; \rightleftarrows \; \text{favorable prefactorization systems} : \Psi. $$

Here subcategories form a (possibly [[large category|large]]) [[poset]] ordered by inclusion, and prefactorization systems form a poset ordered by inclusion of the right classes $M$.

The [[unit of an adjunction|unit]] of this adjunction is easily seen to be an [[isomorphism]].  That is, given a reflective subcategory $A$, if we construct $(E,M)$ from it as above, then $A \simeq M/1$.  Therefore, the adjunction allows us to identify reflective subcategories with certain favorable prefactorization systems.

The prefactorization systems arising in this way --- equivalently, those for which $(E,M) =  \Phi \Psi(E,M)$ --- are called the **reflective prefactorization systems**.  A **reflective factorization system** is a reflective prefactorization system which happens to be a factorization system.

More generally, for any favorable factorization system $(E,M)$, we have a reflective prefactorization system $ \Phi \Psi(E,M)$, called the **reflective interior** of $(E,M)$.  Dualizing, it also has a **coreflective closure**.

## Properties

### Characterization

The following is Theorem 2.3 in [CHK](#CHK).

+-- {: .num_theorem}
###### Theorem
Let $(E',M')$ be the reflective interior of $(E,M)$.  Then:

1. $f\in E'$ precisely when there exists a $g\in E$ such that $g f \in E$.
1. $(E,M)$ is reflective precisely when $g f\in E$ and $g\in E$ together imply $f\in E$.
=--
+-- {: .proof}
###### Proof
That (1) implies (2) is obvious, so we prove (1).

Since $E'$ is, by definition, the class of maps inverted by the reflector into $M/1$, it satisfies the [[2-out-of-3 property]].  Since $E\subseteq E'$, it follows that $f g\in E$ and $g\in E$ imply $f\in E'$.

Conversely, if $f\colon X\to Y$ is in $E'$, then we have $\eta_Y \circ f = \ell(f) \circ \eta_X$ by naturality, where $\ell$ is the reflector into $M/1$ and $\eta$ its unit.  But by construction of $\ell$, $\eta_Y$ and $\eta_X$ are in $E$, and by assumption, $\ell(f)$ is invertible; hence we can take $g = \eta_Y$.
=--

Note that the left class in any orthogonal factorization system is automatically closed under composition, contains the isomorphisms, and satisfies the property that $g f \in E$ and $f\in E$ together imply $g\in E$.  Therefore, $(E,M)$ is reflective precisely when $E$ is a system of [[category with weak equivalences|weak equivalences]].  See [Relation to Localization](#Localization), below.


### Construction of factorizations

The following is a slightly generalized version of Corollary 3.4 from [CHK](#CHK).

+-- {: .num_theorem}
###### Theorem
Suppose that $C$ is finitely complete and [[M-complete category|M-complete]] for some factorization system $(E,M)$, where $M$ consists of [[monomorphisms]] and contains the [[split monomorphism|split monics]].  Then any reflective prefactorization system on $C$ is a factorization system.
=--
+-- {: .proof}
###### Proof
This follows directly from [this theorem](/nlab/show/M-complete+category#OFSFromAdjunction) applied to the reflection adjunction.
=--

The following is a consequence of Theorems 4.1 and 4.3 from [CHK](#CHK).

+-- {: .num_theorem #SemiLeftExact}
###### Theorem
Suppose that $C$ is finitely complete and that $(E,M)$ is a reflective prefactorization system on $C$ such that $E$-morphisms are stable under pullback along $M$-morphisms.  Then $(E,M)$ is a factorization system.
=--
+-- {: .proof}
###### Proof
Write $\ell$ for the corresponding reflection.  Now given $f\colon A\to B$, let $m$ be the pullback of $\ell(f)$ along $\eta_B\colon B \to \ell B$:
$$\array{ Y & \overset{g}{\to} & \ell A \\
  ^m \downarrow & & \downarrow^{\ell(f)}\\
  B & \underset{\eta_B}{\to} & \ell B}$$
By closure properties of prefactorization systems, any morphism in $M/1$ lies in $M$, so in particular $\ell(f)\in M$.  Since $M$ is stable under pullback (being, again, the right class of a prefactorization system), we have $m\in M$.

But $f$ factors through $m$, by the universal property of the pullback applied to the naturality square for $\eta$ at $f$.  Thus we have $f = m e$ and it suffices to show $e\in E$.  However, we also have $g e = \eta_A$, where $\eta_A\in E$ by definition, and $g\in E$ by assumption (being the pullback of $\eta_B\in E$ along $\ell(f)\in M$).  By the characterization theorem above, since $(E,M)$ is reflective this implies $e\in E$, as desired.
=--

A reflection satisfying the condition of Theorem \ref{SemiLeftExact} is called **[[semi-left-exact reflection|semi-left-exact]]** (which see, for more equivalent characterizations).  Note that saying that $E$-morphisms are stable under *all* pullbacks is equivalent to saying that $\ell$ preserves all pullbacks, hence all finite limits---i.e. it is left-exact.  In this case the factorization system is called [[stable factorization system|stable]].  Thus the terminology "semi-left-exact" for the weaker assumption.

However, semi-left-exactness is not necessary for the "one-step" construction in the proof of Theorem \ref{SemiLeftExact} to work.  The necessary and sufficient condition is that the reflection is **simple**; one characterization of this is that a morphism $f$ is in $M$ if and only if its naturality square for the reflector $\ell:C\to A$ is a pullback.  For others, see [CHK, Theorem 4.1](#CHK).


### Relation to localizations {#Localization}

For any favorable prefactorization system $(E,M)$, it is easy to show that $M/1$ is the [[localization]] of $C$ at $E$.  If $(E',M')$ is the reflective interior of $(E,M)$, then since $E'$ is the class of maps inverted by the reflector into $M/1$, it is precisely the *saturation* of $E$ in the sense of localization (the class of maps inverted by the localization at $E$).

### Reflective stable factorization systems

A reflective factorization system on a finitely [[complete category]] is a [[stable factorization system]] if and only if its corresponding [[reflector]] preserves [[finite limits]].  A stable reflective factorization system is sometimes called **local**.


## Examples

Obviously, any [[reflective subcategory]] gives rise to a reflective factorization system.  Here are a few examples.

* The category of complete [[metric spaces]] is reflective in the category of all metric spaces; the reflector is completion.  In the corresponding factorization system, $E$ is the class of [[dense subspace|dense embeddings]].

* Given a small [[site]] $S$, the [[sheaf topos]] $Sh(S)$ is a reflective subcategory of the [[presheaf topos]] $Psh(S)$.  In the corresponding factorization system, $E$ is the class of [[local isomorphisms]].

On the other hand, many commonly encountered factorization systems are not reflective.

* The factorization system $(Epi, Mono)$ on [[Set]] is not reflective.  If  $(E',M')$ is its reflective interior, then $E'$ is the class of morphisms $e\colon X\to Y$ such that if $Y$ is [[inhabited set|inhabited]], so is $X$, while $M'$ is the class of morphisms $m\colon X\to Y$ such that if $X$ is inhabited, then $m$ is an isomorphism.

## Related concepts

* [[semi-left-exact reflection]]

* [[stable factorization system]]

* [[closure operator]]

* [[reflective localization]]

## References

The basic theory is developed in

* {#CHK} C. Cassidy, M. H&#233;bert, [[Max Kelly]], _Reflective subcategories, localizations, and factorization systems_,  J. Austral. Math Soc. (Series A) 38 (1985), 287--329 ([doi:10.1017/S1446788700023624](https://doi.org/10.1017/S1446788700023624))
 
* {#CJKP} [[Aurelio Carboni]], [[George Janelidze]], [[Max Kelly]], [[Robert Paré]], _On localization and stabilization for factorization systems_, Appl. Categ. Structures 5 (1997), 1--58 ([doi:10.1023/A:1008620404444](https://doi.org/10.1023/A:1008620404444))
 

Discussion of "simple" reflective factorization systems and of simultaneously reflective and coreflective factorization systems is in 

* {#RosickyTholen08} [[Jiri Rosicky]], [[Walter Tholen]], _Factorization, Fibration and Torsion_, Journal of Homotopy and Related Structures, Vol. 2(2007), No. 2, pp. 295-314  ([arXiv:0801.0063](http://arxiv.org/abs/0801.0063), [publisher](http://www.emis.de/journals/JHRS/volumes/2007/n2a14/))
 


[[!redirects reflective factorization system]]
[[!redirects reflective factorization systems]]
[[!redirects reflective prefactorization system]]
[[!redirects reflective prefactorization systems]]
[[!redirects coreflective factorization system]]
[[!redirects coreflective factorization systems]]
[[!redirects coreflective prefactorization system]]
[[!redirects coreflective prefactorization systems]]
[[!redirects reflective interior]]
[[!redirects coreflective closure]]
[[!redirects simple reflection]]
[[!redirects simple reflections]]
