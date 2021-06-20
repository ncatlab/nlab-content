
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

+-- {: .num_defn #MonoidsInMonoidalCategory}
###### Definition

Given a [[monoidal category]] $(\mathcal{C}, \otimes, 1)$, and given $(A,\mu,e)$ a [[monoid in a monoidal category|monoid in]] $(\mathcal{C}, \otimes, 1)$, then a **left [[module object]]** in $(\mathcal{C}, \otimes, 1)$ over $(A,\mu,e)$ is

1. an [[object]] $N \in \mathcal{C}$;

1. a [[morphism]] $\rho \;\colon\; A \otimes N \longrightarrow N$ (called the _[[action]]_);

such that 

1. ([[unitality]]) the following [[commuting diagram|diagram commutes]]:

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


1. (action property) the following [[commuting diagram|diagram commutes]]

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

## Examples


\begin{example}\label{GeometricActions}
**(geometric actions)**

A [[group object]]-action 

* internal to [[Sets]] is a [[topological G-space]]: a [[set]] equipped with an [[action]] of a [[discrete group]] -- this is the plain notion of a group action;

* internal to [[TopologicalSpaces]] is a [[topological G-space]]: a [[topological group]] equipped with an [[action]] on a [[topological space]] by [[continuous functions]];

* internal to [[SmoothManifolds]] is a [[G-manifold]]: a [[Lie group]] equipped with an [[action]] on a [[smooth manifold]] by [[smooth functions]].

\end{example}

\begin{example}\label{EquivariantPrincipalBundle}
**([[equivariant principal bundles]])**

A $G$-[[equivariant principal bundle]] is an internal action of a [[group object]] internal to a [[category]] of internal $G$-[[actions]] as in Example \ref{GeometricActions}, such as [[G-sets]]/[[G-spaces]]/[[G-manifolds]] (an "[[equivariant group]]") which satisfies, internally, [[principal bundle|principality]] and [[locally trivial bundle|local triviality]]-condition.

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

See also:

* [[Francis Borceux]], [[George Janelidze]], [[Gregory Maxwell Kelly]], p. 8 of: _Internal object actions_, Commentationes Mathematicae Universitatis Carolinae (2005) Volume: 46, Issue: 2, page 235-255 ([dml:249553](https://eudml.org/doc/249553))



[[!redirects module objects]]

[[!redirects module in a monoidal category]]
[[!redirects modules in a monoidal category]]

[[!redirects action object]]
[[!redirects action objects]]

[[!redirects internal action]]
[[!redirects internal actions]]

