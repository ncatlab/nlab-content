
# Contents
* the following line creates the automatic table of contents
{:toc}

## Idea

The Hahn--Banach theorem explains why the concept of [[locally convex spaces]] is of interest in the analysis of [[topological vector spaces]]: It ensures that such a space will have enough continuous linear functionals such that the [[dual vector space|topological dual space]] is interesting.

## Statement 

+-- {: .num_theorem} 
###### Theorem 
Let $V$ be a [[vector space]] over a [[local field]] $K$ (usually $\mathbb{R}$ or $\mathbb{C}$), equipped with a [[seminorm]] $p: V \to [0, \infty)$. Let $W \subseteq V$ be a subspace, and $f: W \to K$ a [[linear functional]] such that ${|f(x)|} \leq p(x)$ for all $x \in W$, then there exists an [[extension]] of $f$ to a linear functional $g: V \to K$ such that ${|g(x)|} \leq p(x)$ for all $x \in V$. 
=-- 

## Foundational issues

The full Hahn--Banach theorem may be seen as a weak form of the [[axiom of choice]]; this is the perspective taken in, for example, _[[HAF]]_.  It fails in [[dream mathematics]] and is generally not accepted in [[constructive mathematics]].  (Does it actually imply [[excluded middle]]? No, but the [[ultrafilter principle]] frequently used to prove the Hahn-Banach theorem implies [[De Morgan's law]] which is usually not accepted in constructive mathematics.) 

The Hahn-Banach theorem can be proven in [[set theory]] with the axiom of choice, or more weakly in set theory assuming the [[ultrafilter theorem]], itself a weak form of choice. (To be continued...)

However, the Hahn--Banach theorem for [[separable spaces]] is much weaker.  It may be proved constructively using only [[dependent choice]].  There is also a version of the theorem for [[locales]] (or so I heard).

## Consequences 



## References ##

* Wikipedia on the [Hahn-Banach theorem] (http://en.wikipedia.org/wiki/Hahn%E2%80%93Banach_theorem)


[[!redirects Hahn-Banach theorem]]
[[!redirects Hahn-Banach theorems]]
[[!redirects Hahn–Banach theorem]]
[[!redirects Hahn–Banach theorems]]
[[!redirects Hahn--Banach theorem]]
[[!redirects Hahn--Banach theorems]]
