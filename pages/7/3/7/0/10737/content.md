[[!redirects p-completion]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Higher linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

$p$-completion is to [[p-adic homotopy theory]] as [[rationalization]] is to [[rational homotopy theory]].

For more see at _[[formal completion]]_.

### Of abelian groups, rings and modules

For $A$ an [[abelian group]] (or [[commutative ring]]) and $p$ a [[prime number]], the _$p$-completion_ of $A$ is the [[limit]]

$$
  A_p^\wedge \coloneqq \underset{\leftarrow}{\lim}_{n \geq 1} A/(p^n A)
  \,.
$$

(e.g. [May Ponto, 10.1.1](#MayPonto)) For more see at _[[formal completion]]_.

$A$ is called _$p$-complete_ if the canonical [[homomorphism]] $A \to A_p^\wedge$ is an [[isomorphism]].


### Of a homotopy type

(...) ([e.g. May-Ponto, 10.2](#MayPonto))

## Properties

The _[[fracture theorem]]_ says that under mild conditions a (stable) homotopy type decomposes into its [[rationalization]] and its $p$-completions.

## Examples

For $A = \mathbb{Z}$ the [[integers]], the $p$-completion is the [[p-adic integers]]. (Notice that here traditionally one writes $\mathbb{Z}_p = \mathbb{Z}_p^\wedge$.)  

More generally, if $A$ is [[finitely generated object|finitely generated]], then $A_p^\wedge \simeq A\otimes \mathbb{Z}_p$. (e.g. [May Ponto, p. 154](#MayPonto))

## Related concepts

* [[p-adic integers]]

* [[completion of a group]]

* [[completion of a ring]], [[analytic completion of a ring]]

* [[p-localization]]

* [[p-adic homotopy theory]]

* [[rationalization]], [[rational homotopy theory]]

* [[fracture theorem]]

* [[nilpotent homotopy type]], [[finite homotopy type]]

* [[nilpotent completion of spectra]]

* [[L-complete module]]



## References

Classical accounts:

* {#Sullivan05} [[Dennis Sullivan]], _Geometric topology: localization, periodicity and Galois symmetry_, volume 8 of K- Monographs in Mathematics. Springer, Dordrecht, 2005. The 1970 MIT notes, Edited and with a preface
by [[Andrew Ranicki]] ([pdf](http://www.maths.ed.ac.uk/~aar/books/gtop.pdf))

* {#BousfieldKan71} [[Aldridge Bousfield]], [[Daniel Kan]], *Localization and completion in homotopy theory*, Bull. Amer. Math. Soc. **77** 6 (1971) 1006-1010 &lbrack;[doi:10.1090/S0002-9904-1971-12837-9](https://doi.org/10.1090/S0002-9904-1971-12837-9), [pdf](https://www.ams.org/journals/bull/1971-77-06/S0002-9904-1971-12837-9/S0002-9904-1971-12837-9.pdf)&rbrack;

* {#BousfieldKan72} [[Aldridge Bousfield]], [[Daniel Kan]], _[[Homotopy limits, completions and localizations]]_, Lecture Notes in Mathematics, **304** Springer (1972) &lbrack;[doi:10.1007/978-3-540-38117-4](https://doi.org/10.1007/978-3-540-38117-4)&rbrack;

* {#MayPonto} [[Peter May]], [[Kate Ponto]], chapters 7 and 8 of _More concise algebraic topology: Localization, completion, and model categories_ ([pdf](http://www.maths.ed.ac.uk/~aar/papers/mayponto.pdf))

See also

* [[Doug Ravenel]], chapter 2, def. 2.1.14 _[[Complex cobordism and stable homotopy groups of spheres]]_

* {#Rognes12} [[John Rognes]], section 4.6 of _The Adams spectral sequence_, 2012 ([pdf](http://folk.uio.no/rognes/papers/notes.050612.pdf))

[[!redirects p-completions]]

[[!redirects p-complete ring]]
[[!redirects p-complete rings]]

[[!redirects p-complete homotopy type]]
[[!redirects p-complete homotopy types]]
