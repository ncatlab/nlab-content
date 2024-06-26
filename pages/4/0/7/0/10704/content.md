
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Localization of a space
* table of contents
{: toc}

## Idea


The **localization of a space** (really: [[homotopy type]], [[∞-groupoid]]) or [[spectrum]] with respect to some [[prime numbers]] is a [[homotopy theory|homotopical]] analogue of the notion of [[localization of a commutative ring]] (or rather of [[localization of a module]]), specifically the ring $\mathbb{Z}$ of [[integers]], with respect to some [[prime numbers]].  In good cases, at least, this localization acts on the [[homotopy groups|homotopy]] and/or [[homology groups]] as algebraic localization.  (For spaces, there are multiple inequivalent notions of localization, although all agree on [[nilpotent spaces]].)

Localization in this sense is closely related to [[Bousfield localization]].  The localization of spectra is a [[Bousfield localization of spectra]], while one of the constructions of localization of spaces is a Bousfield localization of model categories.  The present notion of localization should not be confused with the [[completion of a space]], which is a different sort of Bousfield localization.

## Preliminaries

### Sets of primes

For all of this page, 

* let $T$ be a [[set]] of [[prime numbers]], 

* write $\neg T$ for the set of primes not in $T$.  


+-- {: .num_defn}
###### Definition

Write $\mathbb{Z}_T$ for the [[commutative ring|ring]] of [[integers]] [[localization of a commutative ring|localized]] by inverting all primes in $\neg T$, i.e. the subring of $\mathbb{Q}$ whose denominators are products of primes in $\neg T$.  

=--

+-- {: .num_example}
###### Example

The most important cases are:

* $T = \{p\}$ for a prime $p$.  In this case, $T$-localization will be **localization at $p$** or **$p$-localization**.

* $T = \neg \{p\}$, the set of all primes except $p$.  In this case, $T$-localization will be **localization away from $p$**.

* $T = \emptyset$.  In this case, $T$-localization will be **[[rationalization]]**.

In these cases:

*  $\mathbb{Z}_\emptyset = \mathbb{Q}$ is the [[rational numbers]];

* $\mathbb{Z}_{\neg\{p\}} = \mathbb{Z}[\frac{1}{p}]$;

* $\mathbb{Z}_{\{p\}} = \mathbb{Z}_{(p)}$ is the integers localized at the [[prime ideal]] $(p)$.

=--

+-- {: .num_remark}
###### Remark


The analogous theory of the [[completion of a space]] involves the [[cyclic groups]] $\mathbb{Z}/p\mathbb{Z}$ -- written $\mathbb{F}_p$ when regarded as a [[finite field]] -- and/or the [[p-adic integers]] $\mathbb{Z}_p$ instead of $\mathbb{Z}_T$ (e.g. [Lurie "Proper morphisms", section 4](#LurieProper)).

For the relation of that to completion see remark \ref{RelationToCompletion} below.

Hence beware the subtle but crucial difference in what a subscript means, depending on which symbol is being subscribed and whether there are parenthesis or not:

* $\mathbb{Z}_{(p)}$: inverting all primes except $p$;

* $\mathbb{F}_p$: quotient by $p$;

* $\mathbb{Z}_p$: [[formal completion]] at $p$.

=--


### Local groups

+-- {: .num_defn #TLocalGroup}
###### Definition

A [[group]] $G$ is said to be **$T$-local** if the $p^{th}$ power map $G\to G$ is a bijection for all $p\in \neg T$.

=--

+-- {: .num_prop #CharacterizationOfAbelianLocalGroups}
###### Proposition

If $G$ is [[abelian group|abelian]], then this map is a group [[homomorphism]] and is  generally written additively as multiplication by $p$.  In this case the following are equivalent:

* $G$ is $T$-local;

* $G$ admits a structure of $\mathbb{Z}_T$-[[module]] (necessarily unique);

* The [[tensor product]] $G\otimes \mathbb{Z}/p\mathbb{Z}$ with the [[cyclic group]] of order $p$ is equal to zero for all $p\in\neg T$.

=--

+-- {: .num_prop}
###### Remark

The second characterization in prop. \ref{CharacterizationOfAbelianLocalGroups} implies that $T$-local abelian groups are [[reflective subcategory|reflective]] in [[Ab]]: the reflection is the [[extension of scalars]] functor $(\mathbb{Z}_T \otimes -)$.  In fact, $T$-local nonabelian groups are also reflective in [[Grp]], but the construction is less pretty.

=--

## Definitions

### Localization of spectra

+-- {: .num_defn #TLocalSpectrum}
###### Definition

A [[spectrum]] $X$ is called **$T$-local** (or $\mathbb{Z}_T$-local, if there is potential for confusion) if its [[homotopy groups]] are $T$-local abelian groups, def. \ref{TLocalGroup}.

The **$T$-localization** of a spectrum is its [[reflective sub-(infinity,1)-category|reflection]] into $T$-local spectra.  

=--

+-- {: .num_remark}
###### Remark

The $T$-localization, def. \ref{TLocalSpectrum}, may be constructed as the [[Bousfield localization of spectra]] with respect to the [[Moore spectrum]] $S(\mathbb{Z}_T)$ (e.g. [Bauer 11, Example 1.7](#Bauer11)).

It can also be constructed as a [[Bousfield localization of model categories]] where we invert the maps that induce an isomorphism on [[generalized homology]] with [[coefficients]] in $H \mathbb{Z}_T$; these are called **$\mathbb{Z}_T$-homology isomorphisms**. See at _[[homology localization]]_.

=--



### Localization of nilpotent spaces

The presence of the nonabelian group $\pi_1$ makes the theory of localization of unstable spaces more subtle than that of spectra.  If spaces are [[simply connected]], of course, then this is not a problem.  More generally, it suffices to consider [[simple spaces]]: those where $\pi_1$ is abelian and acts trivially on the higher homotopy groups.  Even more generally, it suffices to consider [[nilpotent spaces]], whose definition is more complicated; the reader is encouraged to think about simple or even simply connected spaces.

For a nilpotent space $Z$, the following conditions are equivalent.  When they hold, we say that $Z$ is **$T$-local**.  (See [May-Ponto, Theorem 6.1.1](#MayPonto).)

1. Whenever $X\to Y$ induces an isomorphism on homology with $\mathbb{Z}_T$-coefficients, the induced map $[Y,Z] \to [X,Z]$ is a bijection.

2. Each [[homotopy group]] $\pi_n(Z)$ is a $T$-local group.

3. Each [[homology group]] $H_n(Z,\mathbb{Z})$ is a $T$-local group.

For a general nilpotent space $X$, the following properties of a map $\phi:X\to Y$, with $Y$ nilpotent and $T$-local, are equivalent.  Such a map exists and is unique up to homotopy, and we call it the **$T$-localization** of $X$ at $T$.  (See [May-Ponto, Theorem 6.1.2](#MayPonto).)

1. The induced map $[Y,Z] \to [X,Z]$ is a bijection for all $T$-local nilpotent spaces $Z$.

2. $\phi$ induces an isomorphism on homology with $\mathbb{Z}_T$-coefficients.

3. The induced map $\pi_n(X) \to \pi_n(Y)$ is an algebraic $T$-localization for all $n$.

4. The induced map $H_n(X,\mathbb{Z}) \to H_n(Y,\mathbb{Z})$ is an algebraic $T$-localization for all $n$.

### Localization of non-nilpotent spaces

For non-nilpotent spaces, there are multiple inequivalent definitions of localization (see [May-Ponto, Remark 19.3.11](#MayPonto)).  For instance:

* One can do a [[Bousfield localization of model categories]] with respect to the class of $\mathbb{Z}_T$-homology isomorphisms.  In this case, the "$T$-local spaces" are those $Z$ such that $[Y,Z] \to [X,Z]$ is an isomorphism for all $\mathbb{Z}_T$-homology isomorphisms $X\to Y$ (the first characterization of $T$-local nilpotent spaces above).

* One can construct a [[totalization]] of the [[cosimplicial object]] induced by the "free simplicial $\mathbb{Z}_T$-module" monad.  This construction is due to [Bousfield-Kan](#BousfieldKan72).

* One can do a [[Bousfield localization of model categories]] with respect to the maps $p:S^1\to S^1$ for all $p\in \neg T$.  This construction is due to [Casacuberta-Peschke](#CasacubertaPeschke).  In this case, the "$T$-local spaces" are those such that $\pi_1(X)$ is a $T$-local group and acts "$T$-[[p-local module|locally]]" on each $\pi_n(X)$.

One can of course state the other two characterizations of "$T$-local space" from the nilpotent case even in the non-nilpotent case, as is done by [Sullivan](#Sullivan70), but these characterizations are no longer equivalent to the first one, and it is not clear whether corresponding "localizations" exist.

## Properties

### Relation to formal completion
 {#RelationToCompletion}

+-- {: .num_remark #RelationToCompletion}
###### Remark
**(relation to completion)**

A $\neg\{p\}$-local spectrum is also called **$\mathbb{Z}/p\mathbb{Z}$-acyclic**.  According to the general theory of [[Bousfield localization of spectra]], they are "dual" to the "$\mathbb{Z}/p\mathbb{Z}$-local spectra", in the sense that $X$ is $\mathbb{Z}/p\mathbb{Z}$-local if every map $Y \to X$ out of a $\mathbb{Z}/p\mathbb{Z}$-acyclic $Y$ is [[null homotopy|null homotopic]].  

$\mathbb{Z}/p\mathbb{Z}$-local spectra are also known as *$p$-complete* spectra, and are the [[Bousfield localization of spectra]] at the [[Moore spectrum]] $S \mathbb{Z}/p\mathbb{Z}$ (e.g. [Bauer 11, Example 1.7](#Bauer11)).  

This may be regarded as a consequence of the [[mod p Whitehead theorem]].

=--

See ([May-Ponto, example 19.2.3](#MayPonto), [Lurie, example 8](#Lurie),[Lurie "Proper morphisms", section 4](#LurieProper)).

In summary:

[[!include localization and completion -- table]]

+-- {: .num_remark}
###### Remark

In terms of [[arithmetic geometry]] this may be understood as follows:

1. $\mathbb{F}_p = \mathbb{Z}/(p \mathbb{Z})$ is the [[ring of functions]] exactly on the point $(p)\in $ [[Spec(Z)]]

1. $\mathbb{Z}_p$ is the functions on the [[formal neighbourhood]] of $(p)$.

1. $\mathbb{Z}_{(p)}$ is the ring of functions defined on the open complement of the point $(p)$, hence on an [[open neighbourhood]].


So the localization at the Moore spectrum of one of these rings localizes to the formal neighbourhood of their support. For $\mathbb{F}_p$ the support is the closed point, and so the localization there is infinitesimally bigger than that, as given by the $p$-adic completion. On the other hand the support of $\mathbb{Z}_{(p)}$ is open and hence contains its own formal neighbourhood, so localizing here just gives the plain localization.

=--

### Basic properties

* [[fracture theorem]]

### In chromatic homotopy theory

Many of the basic constructions and theorems in [[chromatic homotopy theory]] apply to [[finite spectrum|finite]] $p$-local spectra, such as


* [[telescopic localization]]

* [[periodicity theorem]]

* [[chromatic convergence theorem]]



## Examples

* [[Brown-Peterson spectrum]]


## Related concepts

* [[p-completion]]

* [[finite homotopy type]], [[finite spectrum]]

* [[nilpotent homotopy type]]

* [[rational homotopy type]]

## References


* {#Sullivan70} [[Dennis Sullivan]], _Localization, Periodicity and Galois Symmetry_ (The 1970 MIT notes) edited by [[Andrew Ranicki]], K-Monographs in Mathematics, Dordrecht: Springe ([pdf](http://www.maths.ed.ac.uk/~aar/surgery/gtop.pdf)) 

* {#BousfieldKan72} [[Aldridge Bousfield]], [[Daniel Kan]], _[[Homotopy limits, completions and localizations]]_, Lecture Notes in Mathematics, Vol 304, Springer 1972

* [[John Frank Adams]], [[Zbigniew Fiedorowicz]], *Localisation and Completion with an addendum on the use of Brown-Peterson homology in stable homotopy*, based on 1973 lectures by Adams &lbrack;[arXiv:1012.5020](https://arxiv.org/abs/1012.5020)&rbrack; 


* {#MayPonto} [[Peter May]], [[Kate Ponto]], _More concise algebraic topology: Localization, completion, and model categories_ ([pdf](http://www.maths.ed.ac.uk/~aar/papers/mayponto.pdf))

* {#CasacubertaPeschke} [[Carles Casacuberta]], [[Georg Peschke]], *Localizing with respect to self maps of the circle*, Trans. Amer. Math. Soc. **339** (1993) 117-140  &lbrack;[doi:10.1090/S0002-9947-1993-1123451-X](https://doi.org/10.1090/S0002-9947-1993-1123451-X), [pdf](http://www.ub.edu/topologia/casacuberta/articles/cpes.pdf)&rbrack;


* {#Lurie} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 20 _Bousfield localization_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture20.pdf))


* {#Bauer11} [[Tilman Bauer]], _Bousfield localization and the Hasse square_ ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/Chapter09/bauer.pdf))

* {#LurieProper} [[Jacob Lurie]], section 4 of _[[Proper Morphisms, Completions, and the Grothendieck Existence Theorem]]_ 

* [[Emily Riehl]], §14.4 in: *[[Categorical Homotopy Theory]]*, Cambridge University Press (2014) &lbrack;[doi:10.1017/CBO9781107261457](https://doi.org/10.1017/CBO9781107261457), [pdf](http://www.math.jhu.edu/~eriehl/cathtpy.pdf)&rbrack;


See also

* Wikipedia, _[Localization of a topological space](http://en.wikipedia.org/wiki/Localization_of_a_topological_space)_

and see at 

* [[Bousfield localization of spectra]] for more.

Formalization in [[homotopy type theory]]:

* [[J. Daniel Christensen]], [[Morgan Opie]], [[Egbert Rijke]], [[Luis Scoccola]], _Localization in Homotopy Type Theory_, Higher Structures, 4(1) (2020), 1-32 ([arXiv:1807.04155](https://arxiv.org/abs/1807.04155))

[[!redirects p-localization]]
[[!redirects p-localizations]]
[[!redirects p-localisation]]
[[!redirects p-localisations]]

[[!redirects p-local]]
[[!redirects p-locally]]

[[!redirects p-local spectrum]]
[[!redirects p-local spectra]]

[[!redirects p-local space]]
[[!redirects p-local spaces]]

[[!redirects p-local homotopy type]]
[[!redirects p-local homotopy types]]

[[!redirects localization of spaces]]
[[!redirects localizations of spaces]]
