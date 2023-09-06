
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _action object_ or _module object_ is the [[internalization]] of the notion of [[action]]/[[module]] of [[monoids]] (such as [[groups]] or [[rings]]) on [[sets]] (such as [[group representations]] or [[modules]]), into any [[monoidal category]] $\mathcal{C}$ to yield a notion of actions of [[monoid objects]] (such as [[group objects]] or [[ring objects]]) on the [[objects]] of that [[category]] $\mathcal{C}$.


## Definition
 {#Definition}

+-- {: .num_defn #MonoidsInMonoidalCategory}
###### Definition

Given a [[monoidal category]] $(\mathcal{C}, \otimes, 1)$, and given $(A,\mu,e)$ a [[monoid in a monoidal category|monoid in]] $(\mathcal{C}, \otimes, 1)$, then a **left module object** in $(\mathcal{C}, \otimes, 1)$ over $(A,\mu,e)$ is

1. an [[object]] $N \in \mathcal{C}$;

1. a [[morphism]] $\rho \;\colon\; A \otimes N \longrightarrow N$ (called the _[[action]]_);

such that 

1. {#Unitality} ([[unitality]]) the following [[commuting diagram|diagram commutes]]:

   $$
     \array{
       1 \otimes N 
         &\overset{e \otimes id}{\longrightarrow}&
       A \otimes N
       \\
       & {}_{\mathllap{\ell}}\searrow 
       & \downarrow^{\mathrlap{\rho}} 
       \\
       && N
     }
     \,,
   $$

   where $\ell$ is the left unitor isomorphism of $\mathcal{C}$.


1. {#ActionProperty} (action property) the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       (A\otimes A) \otimes N
         &\underoverset{\simeq}{a_{A,A,N}}{\longrightarrow}&
       A \otimes (A \otimes N)
         &\overset{A \otimes \rho}{\longrightarrow}&
       A \otimes N
       \\
       {}^{\mathllap{\mu \otimes N}}\downarrow  
         && &&
       \downarrow^{\mathrlap{\rho}}
       \\
       A \otimes N
         &\longrightarrow&
         &\overset{\rho}{\longrightarrow}&
       N
     }
     \,,
   $$

=--

## Generalisation
A module and the monoid it lies over do not necessarily belong to the same category, a fact suggested by the [[microcosm principle]]:

+-- {: .num_defn #MonoidsInActegory}
###### Definition
Given a [[monoidal category]] $(\mathcal{M}, \odot, 1)$ and an $\mathcal{M}$-module (also called $\mathcal{M}$-[[actegory]]) $\mathcal{C}$ (supported by the monoidal action $\bullet : \mathcal{M} \times \mathcal{C} \to \mathcal{C}$), and given $(A,\mu,e)$ a [[monoid in a monoidal category|monoid in]] $(\mathcal{M}, \odot, 1)$, then a **left module object** in $\mathcal{C}$ over $(A,\mu,e)$ is

1. an [[object]] $N \in \mathcal{C}$;

1. a [[morphism]] $\rho \;\colon\; A \bullet N \longrightarrow N$ (called the _[[action]]_);

such that 

1. ([[unitality]]) the following [[commuting diagram|diagram commutes]]:

   $$
     \array{
       1 \bullet N 
         &\overset{e \bullet id}{\longrightarrow}&
       A \bullet N
       \\
       & {}_{\mathllap{\lambda}}\searrow 
       & \downarrow^{\mathrlap{\rho}} 
       \\
       && N
     }
     \,,
   $$

   where $\lambda$ is the [[actegory#Actegory|unitor]] of $\bullet$.


1. (action property) the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       (A \odot A) \bullet N
         &\underoverset{\simeq}{\alpha_{A,A,N}}{\longrightarrow}&
       A \bullet (A \bullet N)
         &\overset{A \bullet \rho}{\longrightarrow}&
       A \bullet N
       \\
       {}^{\mathllap{\mu \bullet N}}\downarrow  
         && &&
       \downarrow^{\mathrlap{\rho}}
       \\
       A \bullet N
         &\longrightarrow&
         &\overset{\rho}{\longrightarrow}&
       N
     }
     \,,
   $$

   where $\alpha$ is the [[actegory#Actegory|actor]] of $\bullet$.
=--

## Examples


\begin{example}\label{GeometricActions}
**(geometric actions)**

A [[group object]]-action 

* internal to [[Sets]] is a [[G-set]]: a [[set]] equipped with a [[group action]] by a [[discrete group]] -- this is the plain notion of a group action;

* internal to [[TopologicalSpaces]] is a [[topological G-space]]: a [[topological group]] equipped with an [[action]] on a [[topological space]] by [[continuous functions]];

* internal to [[SmoothManifolds]] is a [[G-manifold]]: a [[Lie group]] equipped with an [[action]] on a [[smooth manifold]] by [[smooth functions]];

* internal to [[SimplicialSets]] is a [[simplicial group action]],

\end{example}

\begin{example}\label{EquivariantPrincipalBundle}
**([[equivariant principal bundles]])**

A $G$-[[equivariant principal bundle]] is an internal action of a [[group object]] internal to a [[category]] of internal $G$-[[actions]] as in Example \ref{GeometricActions}, such as [[G-sets]]/[[G-spaces]]/[[G-manifolds]] (an "[[equivariant group]]") which satisfies, internally, [[principal bundle|principality]] and [[locally trivial bundle|local triviality]]-condition.

\end{example}

\begin{example}\label{ActionObjectsInCat}
**(2-actions)**
\linebreak
The notion of [[coherence|coherent]] action object in the [[2-category]] [[Cat]] (of [[categories]] with [[functors]] and [[natural transformations]]) is a [[categorification|categorified]] notion of "action" (namely of [[monoidal categories]]), known as *[[module categories]]* (also: "*[[actegories]]*"), see also *[[2-module]]* and *[[n-module]]*).
\end{example}

\begin{example}
**([[module spectrum]])** \linebreak

A module object in a [[symmetric monoidal category of spectra]] is a [[module spectrum]] over a [[ring spectrum]].

Internal to just the [[stable homotopy category]] it is a _[[homotopy module spectrum]]_.


\end{example}


## Related concepts


* [[module over a monoidal functor]]

* [[(infinity,1)-module]], [[(infinity,n)-module]]


\linebreak

[[categorical algebra -- contents]]

**[[internalization]] and [[categorical algebra]]**

* [[monoid object]]

* [[group object]]

* [[ring object]]

* [[algebra object]] (associative, [[Lie algebra object|Lie]], ...)

* [[module object]]/[[action object]]


* [[internal locale]]

* [[internal category]]

  * [[internal groupoid]]

  * [[internal site]]

  * [[internal diagram]]


**[[universal algebra]]**

* [[Lawvere theory|algebras over]]$\,$ [[algebraic theories]], 

* [[algebra over a monad|algebras over]]$\,$ [[monads]], 

* [[algebra over an operad|algebras over]]$\,$ [[operads]].

**[[categorical semantics]]**

* [[internal logic]], [[internal language]]

* [[relation between category theory and type theory]]





## References

The general definition of internal actions seems to have first been formulated in:

* {#Grothendieck61} [[Alexander Grothendieck]], p. 106 (9 of 21) of: [[FGA]] _Techniques de construction et théorèmes d'existence en géométrie algébrique III: préschémas quotients_, Séminaire Bourbaki: années 1960/61, exposés 205-222, Séminaire Bourbaki, no. 6 (1961), Exposé no. 212,   ([numdam:SB_1960-1961__6__99_0](http://www.numdam.org/item/?id=SB_1960-1961__6__99_0), [pdf](http://www.numdam.org/item/SB_1960-1961__6__99_0.pdf), [English transl. pdf](https://labs.thosgood.com/builds/fga-3-III.pdf))

following the general principle of [[internalization]] formulated in:

* {#Grothendieck60} [[Alexander Grothendieck]], p. 370 (3 of 23) in: [[FGA]] *Technique de descente et théorèmes d'existence en géométrie algébriques. II: Le théorème d'existence en théorie formelle des modules*, Séminaire Bourbaki : années 1958/59 - 1959/60, exposés 169-204, Séminaire Bourbaki, no. 5 (1960), Exposé no. 195 ([numdam:SB_1958-1960__5__369_0](http://www.numdam.org/item/SB_1958-1960__5__369_0), [pdf](http://www.numdam.org/item/SB_1958-1960__5__369_0.pdf), [English transl. pdf](https://labs.thosgood.com/builds/fga-3-II.pdf))

Review:

* [[Barbara Fantechi]], [[Lothar Göttsche]], [[Luc Illusie]], [[Steven L. Kleiman]], [[Nitin Nitsure]], [[Angelo Vistoli]], Section 2.2 of: _Fundamental algebraic geometry. Grothendieck's [[FGA explained]]_, Mathematical Surveys and Monographs __123__, Amer. Math. Soc. (2005) &lbrack;[MR2007f:14001](http://www.ams.org/mathscinet-getitem?mr=2007f:14001), [ISBN:978-0-8218-4245-4](https://bookstore.ams.org/surv-123-s), [lecture notes](http://indico.ictp.it/event/a0255/other-view?view=ictptimetable)&rbrack;

* [[Saunders MacLane]], Sections VII.4 in: *[[Categories for the Working Mathematician]]*, Springer  (1979, 2nd ed.) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

* [[John Michael Boardman]], *Algebraic objects in categories*, Chapter 7 of: _Stable Operations in Generalized Cohomology_ &lbrack;[pdf](https://math.jhu.edu/~wsw/papers2/math/28a-boardman-stable.pdf), [[Boardman-StableOperations.pdf:file]]&rbrack; in: [[Ioan Mackenzie James]] (ed.) _[[Handbook of Algebraic Topology]]_ Oxford (1995) &lbrack;[doi:10.1016/B978-0-444-81779-2.X5000-7](https://doi.org/10.1016/B978-0-444-81779-2.X5000-7)&rbrack;

* [[Magnus Forrester-Barker]], *Group Objects and Internal Categories* &lbrack;[arXiv:math/0212065](https://arxiv.org/abs/math/0212065)&rbrack;

See also:

* [[Francis Borceux]], [[George Janelidze]], [[Gregory Maxwell Kelly]], p. 8 of: _Internal object actions_, Commentationes Mathematicae Universitatis Carolinae (2005) Volume: 46, Issue: 2, page 235-255 ([dml:249553](https://eudml.org/doc/249553))


* [[Mark Hovey]], [[Brooke Shipley]], [[Jeff Smith]], pp. 15 in: *Symmetric spectra*, J. Amer. Math. Soc. **13** (2000) 149-208 &lbrack;[arXiv:math/9801077](http://arxiv.org/abs/math/9801077), [doi:10.1090/S0894-0347-99-00320-3](https://doi.org/10.1090/S0894-0347-99-00320-3)&rbrack;

Discussion that the [[Mod|category of module objects]] over a [[commutative monoid in a symmetric monoidal category|commutative monoid in]] a [[bicomplete category|bicomplete]] [[closed symmetric monoidal category]] is itself [[bicomplete category|bicomplete]] [[closed symmetric monoidal category|closed symmetric monoidal]]:

* [[Mark Hovey]], [[Brooke Shipley]], [[Jeff Smith]], Lemma 2.2.2 & 2.2.8 in: *Symmetric spectra*, J. Amer. Math. Soc. **13** (2000) 149-208 &lbrack;[arXiv:math/9801077](http://arxiv.org/abs/math/9801077), [doi:10.1090/S0894-0347-99-00320-3](https://doi.org/10.1090/S0894-0347-99-00320-3)&rbrack;

* [[Florian Marty]], Prop. 1.2.14, 1.2.16, 1.2.17 in: _Des Ouverts Zariski et des Morphismes Lisses en G&#233;om&#233;trie Relative_, Ph.D. Toulouse (2009) &lbrack;[theses:2009TOU30071](https://www.theses.fr/2009TOU30071), [[Marty-DesOuverts.pdf:file]]&rbrack;

* [[Martin Brandenburg]], Prop. 4.1.10: *Tensor categorical foundations of algebraic geometry* &lbrack;[arXiv:1410.1716](http://arxiv.org/abs/1410.1716)&rbrack;

See also:

* [MO:180673](http://mathoverflow.net/questions/180673/category-of-modules-over-commutative-monoid-in-symmetric-monoidal-category).

Lecture notes:

* [[Urs Schreiber]]: *[Algebras and Modules](Introduction+to+Stable+homotopy+theory+--+1-2#AlgebrasAndModules)*, in *[[Introduction to Stable Homotopy Theory]]* 1.2: *[[Introduction to Stable homotopy theory -- 1-2|Structured Spectra]]* 



[[!redirects module objects]]

[[!redirects module in a monoidal category]]
[[!redirects modules in a monoidal category]]

[[!redirects action object]]
[[!redirects action objects]]

[[!redirects internal action]]
[[!redirects internal actions]]

[[!redirects group action object]]
[[!redirects group action objects]]

