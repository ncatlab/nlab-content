


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


\tableofcontents

## Idea

The *Hahn--Banach theorem* explains why the concept of [[locally convex spaces]] is of interest in the [[analysis]] of [[topological vector spaces]]: It ensures that such a space will have enough [[continuous function|continuous]] [[linear functionals]] such that the [[dual vector space|topological dual space]] is interesting.

## Statement 

+-- {: .num_theorem} 
###### Theorem 
Let $V$ be a [[vector space]] over a [[local field]] $K$ (usually [[real numbers|$\mathbb{R}$]] or [[complex numbers|$\mathbb{C}$]]), equipped with a [[seminorm]] $p \colon
 V \to [0, \infty)$. Let $W \subseteq V$ be a [[linear subspace]], and $f \colon W \to K$ a [[linear functional]] such that ${|f(x)|} \leq p(x)$ for all $x \in W$, then there exists an [[extension]] of $f$ to a linear functional $g: V \to K$ such that ${|g(x)|} \leq p(x)$ for all $x \in V$. 
=-- 

## Foundational issues

The full Hahn--Banach theorem may be seen as a weak form of the [[axiom of choice]]; this is the perspective taken in, for example, _[[HAF]]_.  It fails in [[dream mathematics]] and is generally not accepted in [[constructive mathematics]].  (It does not actually imply [[excluded middle]], but the [[ultrafilter principle]] frequently used to prove the Hahn-Banach theorem implies [[De Morgan's law]] which is usually not accepted in [[constructive mathematics]].) 

The Hahn-Banach theorem can be proven in [[set theory]] with the [[axiom of choice]], or more weakly in set theory assuming the [[ultrafilter theorem]], itself a weak form of choice. (To be continued...)

However, under the additional assumption that the bound $p$ in the statement is [[continuous]], the Hahn--Banach theorem for a restricted class of spaces, including e.g. [[separable spaces]] is much weaker. It may be proved [[constructive mathematics|constructively]] using only [[dependent choice]]. This is false if the continuity assumption is removed. See [Dodu & Morillon 2010](#DoduMorillon2010).

There is also a version of the theorem for [[locales]] proven
in [Pelletier 1991](#Pelletier91). This constructs a [[locale]] of functionals (whose points are the unit ball of the dual space) and proves that it is [[compact space|compact]] and [[completely regular space|completely regular]].

## Consequences 

(...)



## References ##

See also:

* Wikipedia, *[Hahn-Banach theorem] (http://en.wikipedia.org/wiki/Hahn%E2%80%93Banach_theorem)*

Discussion in [[constructive mathematics]]:

* {#DoduMorillon2010} Juliette Dodu, Marianne Morillon: *The Hahn-Banach Property and the Axiom of Choice*, Mathematical Logic Quarterly **45** 3 (2010) 299-314 &lbrack;[doi:10.1002/malq.19990450303](https://doi.org/10.1002/malq.19990450303)&rbrack;

Discussion in the generality of [[locales]]:

* {#Pelletier91} Joan Wick Pelletier: *Locales in Functional Analysis*, Journal of Pure and Applied Algebra **70** 1–2 (1991) 133-145 \[<a href="https://doi.org/10.1016/0022-4049(91)90013-R">doi:10.1016/0022-4049(91)90013-R</a>\]




[[!redirects Hahn-Banach theorem]]
[[!redirects Hahn-Banach theorems]]
[[!redirects Hahn–Banach theorem]]
[[!redirects Hahn–Banach theorems]]
[[!redirects Hahn--Banach theorem]]
[[!redirects Hahn--Banach theorems]]
