[[!redirects codiscrete objects]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $\Gamma \colon \mathcal{E} \to \mathcal{B}$ a [[functor]] we say that it _has [[codiscrete object]]s_ if it has a  [[full and faithful functor|full and faithful]] [[right adjoint]] $coDisc : \mathcal{B} \hookrightarrow \mathcal{E}$. 

An object in the [[essential image]] of $coDisc$ is called a **codiscrete object.

This is for instance the case for the [[global section]] [[geometric morphism]] of a [[local topos]] $ (Disc \dashv \Gamma \dashv coDisc) \mathcal{E} \to \mathcal{B}$. 

If one thinks of $\mathcal{E}$ as a [[category]] of [[spaces]], then the codiscrete objects are called [[codiscrete spaces]].

The dual notion is that of _[[discrete objects]]_.

## Examples

* [[codiscrete topology]]

* [[codiscrete groupoid]]

## Properties

\begin{prop}
$\Gamma$ is a [[faithful functor]] on [[morphisms]] whose [[codomain]] is concrete. 
\end{prop}


+-- {: .num_prop}
###### Proposition

If $\mathcal{E}$ has a [[terminal object]] that is preserved by $\Gamma$, then $\mathcal{E}$ has concrete objects.

=--

This is ([Shulman, theorem 1](#Shulman)).


+-- {: .num_prop}
###### Proposition

If $\mathcal{E}$ has codiscrete objects and has [[pullbacks]] that are preserved by $\Gamma$ and , then $\Gamma$ is a [[Grothendieck fibration]].

=--

This is ([Shulman, theorem 2](#Shulman)).

## Related concepts

* [[chaos]]


[[!include cohesion - table]]


## References

* {#Shulman} [[Mike Shulman]], _Discreteness, Concreteness, Fibrations, and Scones_ ([blog post](http://golem.ph.utexas.edu/category/2011/11/discreteness_concreteness_fibr.html))
 

[[!redirects concrete objects]]