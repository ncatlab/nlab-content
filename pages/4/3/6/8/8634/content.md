
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _[[localization of a ring|localization]]_ of a  [[commutative ring]] $R$ at a [[set]] $S$ of its [[elements]] is a new ring $R[S]^{-1}$ in which the elements of $S$ become invertible ([[unit|units]]) and which is [[universal property|universal]] with this property. 

When interpreting a ring under [[Isbell duality]] as the [[ring of functions]] on some [[space]] $X$ (its [[spectrum of a commutative ring|spectrum]]), then localizing it at $S$ corresponds to restricting to the complement of the subspace $Y \hookrightarrow X$ on which the elements in $S$ vanish.

See also _[[commutative localization]]_ and _[[localization of a ring]] (noncommutative)_. 


\begin{remark}\label{Terminology}
**Localization "at" and "away from"**

The common terminology in algebra is as follows.

For $S$ a set of [[primes]], "localize at $S$" means "invert what is not divisible by $S$"; so for $p$ prime, localizing "at $p$" means considering only $p$-[[torsion subgroup|torsion]].

Adjoining inverses $[S^{-1}]$ is pronounced "localized away from $S$". Inverting a [[prime]] $p$ is localizing away from $p$, which means ignoring $p$-torsion.

See also lecture notes such as ([Gathmann](#Gathmann)) and see at _[[localization of a space]]_ for more discussion of this.

Evidently, this conflicts with more-categorial uses of "localized"; "inverting weak equivalences" is called localization, by obvious analogy, and is written as "localizing at weak equivalences". This is confusing! It's also weird: since a ring is a one-object Ab-enriched category with morphisms "multiply-by", the localization-of-the-category $R$ "at $p$" (or its Ab-enriched version, if saying that is necessary) really means the localization-of-the-ring R "away from p".

\end{remark}

## Definition

### For commutative rings

Let $R$ be a [[commutative ring]]. Let $S \hookrightarrow U(R)$ be a [[multiplicative subset]] of the underlying [[set]].

The following gives the [[universal property]] of the localization.

\begin{definition}
{#UniversalPropertyOfLocalizationOfARing}
The **localization** $L_S \colon R \to R[S^{-1}]$ is a [[homomorphism]] to another commutative ring $R[S^{-1}]$ such that 

* for all elements $s \in S \hookrightarrow R$ the image $L_S(s) \in R[S^{-1}]$ is invertible (is a [[unit]]);

* for every other homomorphism $R \to \tilde R$ with this property, there is a unique [[homomorphism]] $R[S^{-1}] \to \tilde R$ such that we have a [[commuting diagram]]

   $$
     \array{
       R &\stackrel{L_S}{\to}& R[S^{-1}]
       \\
       & \searrow & \downarrow
       \\
       && \tilde R
     }
     \,.
   $$
\end{definition}

The special case of inverting an element $r$ of $R$, in which $S$ is the set $\{ r, r^{2}, r^{3}, \ldots \}$, is discussed at [[localisation of a commutative ring at an element]]. See also for example [Sullivan 70, first pages](#Sullivan70).

\begin{remark}
The [[Isbell duality|formal duals]] $Spec(R[S^{-1}]) \longrightarrow Spec(R)$ of the localization maps $R \longrightarrow R[S^{-1}]$ (under forming [[spectrum of a commutative ring|spectra]]) serve as the standard [[open immersion of schemes|open immersions]] that define the [[Zariski topology]] on [[algebraic varieties]].
\end{remark}

Explicitly:

\begin{definition}
The localization of a [[commutative ring]] $R$ at a [[multiplicative subset]] $S$ is the [[commutative ring]] whose underlying  [[set]] is the set of [[equivalence classes]] on $R \times S$ under the [[equivalence relation]]

$$
  (r_1, s_1) \sim (r_2, s_2) 
  \;\;\Leftrightarrow\;\;
  \exists u \in S
  \;
  (r_1 s_2- r_2 s_1) u = 0 \;\in R
  \,.
$$

Write $r s^{-1}$ for the [[equivalence class]] of $(r,s)$. On this set, addition and multiplication is defined by

$$
  r_1 s_1^{-1} + r_2 s_2^{-1} \coloneqq (r_1 s_2 + r_2 s_1) (s_1 s_2)^{-1}
$$

$$
  (r_1 s_1^{-1})(r_2 s_2^{-1}) \coloneqq r_1 r_2 (s_1 s_2)^{-1}
  \,.
$$
\end{definition}

(e.g. [[The Stacks Project|Stacks Project, def. 10.9.1]])

\begin{remark}
The above definitions also work for non-commutative [[rings]] $R$ as well, so long as the [[multiplicative subset]] $S$ is a [[submonoid]] of the [[center]] $Z(R)$ of the multiplicative monoid of $R$. 
\end{remark}

### For $E_\infty$-rings
 {#ForEInfinityRings}

(...) By the lifting property of etale morphisms for $E_\infty$-rings, see [here](&#233;tale+morphism+of+E-∞+rings#LocalizationOfRings). (...)


Localization away from a suitably tame ideal may be understood as the [[dR-shape modality]] in the [[cohesion]] of [[E-infinity arithmetic geometry]]:

[[!include arithmetic cohesion -- table]]



## Examples

* [[field of fractions]]


## Related concepts

* [[completion of a ring]]

* [[localization]], 

* [[localization of a monoid]]

* [[localization of an abelian group]]

* [[localization of a module]]

* [[localization of a ring]], [[localization of a category]]

* [[Cohn localization]], [[Ore localization]].

* [[Bousfield localization of spectra]]

  * [[localization of a space]] (and of a [[spectrum]])

  * [[p-localization]], [[p-completion]]

* [[quotient ring]]




## References
 {#References}

A classical set of lecture notes:

* {#Sullivan70} [[Dennis Sullivan]], _Localization, Periodicity and Galois Symmetry_ (The 1970 MIT notes) edited by [[Andrew Ranicki]], K-Monographs in Mathematics, Dordrecht: Springer ([pdf](http://www.maths.ed.ac.uk/~aar/surgery/gtop.pdf)) 

Concretely on localization of commutative rings:

* {#Sullivan05} [[Dennis Sullivan]], Section 1 of: _Geometric topology: localization, periodicity and Galois symmetry_, volume 8 of K- Monographs in Mathematics. Springer, Dordrecht, 2005. The 1970 MIT notes, Edited and with a preface
by [[Andrew Ranicki]] ([pdf](http://www.maths.ed.ac.uk/~aar/books/gtop.pdf))

Discussion in [[constructive mathematics]]:

* [[Henri Lombardi]], [[Claude Quitté]] chapter 2 section 2 in:  *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) &lbrack;[doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf)&rbrack;

Further review:

* {#Gathmann} Andreas Gathmann, _Localization_ ([[GathmannLocalization.pdf:file]])

* [[Joseph Neisendorfer]] _A Quick Trip through Localization_ ([pdf](https://www.math.rochester.edu/people/faculty/jnei/localization.pdf))


Other accounts of the basics include

* {#Gathmann} Andreas Gathmann, _Localization_ ([[GathmannLocalization.pdf:file]])

* [[The Stacks Project]], 10.9. _Localization_

* Yoshifumi Tsuchimoto, Review of commutative (usual) affine schemes. _[Localization of a commutative ring](http://www.math.kochi-u.ac.jp/docky/bourdoki/NAS/nas002/node4.html)_

[[!redirects localizations of a commutative ring]]
[[!redirects localisation of a commutative ring]]
[[!redirects localization of commutative rings]]
[[!redirects Localization of commutative rings]]
[[!redirects localizations of commutative rings]]
[[!redirects Localizations of commutative rings]]