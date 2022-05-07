
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

* [[Saunders Mac Lane]], [[Ieke Moerdijk]], Section V.6 of: _[[Sheaves in Geometry and Logic]]_, Springer 1992 ([doi:10.1007/978-1-4612-0927-0](https://link.springer.com/book/10.1007/978-1-4612-0927-0))


* [[Francis Borceux]], [[George Janelidze]], [[Gregory Maxwell Kelly]], p. 8 of: _Internal object actions_, Commentationes Mathematicae Universitatis Carolinae (2005) Volume: 46, Issue: 2, page 235-255 ([dml:249553](https://eudml.org/doc/249553))



* Tao Lu, Zhenzhen Zhu, _The Action of Group Object in A Topos_,   Proceedings of:  _2015 International Conference on Management, Education, Information and Control_ ([doi:10.2991/meici-15.2015.312](https://doi.org/10.2991/meici-15.2015.312))

[[!redirects module objects]]

[[!redirects module in a monoidal category]]
[[!redirects modules in a monoidal category]]

[[!redirects action object]]
[[!redirects action objects]]

