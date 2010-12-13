
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In the context of [[dg-geometry]] an [[∞-stack]] $X$ is called _perfect_ if its [[(∞,1)-category]] $QC(X)$ of [[quasicoherent ∞-stack]]s (of [[module]]s over the [[structure sheaf]] $\mathcal{O}(X)$) is generated from from modules that are locally [[perfect chain complex]]es.


 
## Definition

Let $k$ be a [[field]] of [[characteristic]] 0. Let $T$ be the [[Lawvere theory]] of commutative [[associative algebra]]s over $k$. When this is regarded as an [[(∞,1)-algebraic theory]], the $T$-$\infty$-algebras are modeled (by the [[monoidal Dold-Kan correspondence]] equivalently) by the

* [[model structure on simplicial T-algebras]];

* [[model structure on dg-algebras]] (over $k$, in non-positive deree, with positively graded differential).

The [[higher geometry]]/[[derived geometry]] over formal duals of these algebras is sometimes called [[dg-geometry]]: a general space in this context is given by an [[∞-stack]] over a full sub-[[(∞,1)-site]] 

$$
  C \subset T Alg_\infty^{op}
$$

of the [[opposite (∞,1)-category]] of these $\infty$-algebras.


+-- {: .un_defn}
###### Definition

The [[(∞,2)-sheaf]] of [[quasicoherent ∞-stack]]s is

$$
  Mod : C^{op} \to (\infty,1)Cat
$$

given by

$$
  Spec A \mapsto A Mod
  \,,
$$

where on the right we take the $(\infty,1)$-category of $\infty$-modules over the $\infty$-algebra $A$, regarded as an unbounded dg-algebra.

=--

+-- {: .un_defn}
###### Definition

For $X \in Sh_{(\infty,1)}(C)$ an [[∞-stack]] in [[dg-geometry]], write

$$
  QC(X) := Sh_{(\infty,2)}(C)\left( X, Mod \right)
$$

for the $(\infty,1)$-category of **quasicoherent $\infty$-stacks** on $X$.

=--

This appears as ([Ben-ZviFrancisNadler, section 3.1](#Ben-ZviFrancisNadler)).

+-- {: .un_prop}
###### Proposition

For all $X \in \mathbf{H}$, we have that $QC(X)$ 

* is a [[stable (∞,1)-category]]

* that has all [[(∞,1)-colimit]]s.

=--

([Ben-ZviFrancisNadler, section 3.1](#Ben-ZviFrancisNadler)).


+-- {: .un_defn}
###### Definition

Let $A \in T Alg_\infty$ . An $A$-module is a **perfect module** if it lies in the smallest [[sub-(∞,1)-category]] of $A Mod$ containing $A$ and closed under finite [[(∞,1)-colimit]]s and [[retract]]s. 

For a [[∞-stack]] $X \in Sh_{(\infty,1)}(C)$, the $\infty$-category $Perf(X)$ is the full sub-$(\infty,1)$-category of $QC(X)$ consisting of those modules that are prefect over every affine $U\to X$.

=--

This appears as ([Ben-ZviFrancisNadler, definition 3.1](#Ben-ZviFrancisNadler)).


+-- {: .un_defn}
###### Definition

A [[∞-stack]] $X \in Sh_{(\infty,1)}(C)$ is called a  **perfect stack** if 

* it has affine diagonal $X \to X \times X$;

* and $QC(X)$ is the [[ind-object in an (infinity,1)-category|(∞,1)-category of ind-objects]]

  $$
    QC(X) \simeq \Ind \Perf(X)
  $$

  of the full [[sub-(∞,1)-category]] $Perf(X) \subset QC(X)$ of perfect complexes of modules on $X$. 

A morphism $X \rightarrow Y$ is said to be **perfect morphism** if its fibers $X \times_Y U$ over affines $U \rightarrow Y$ are perfect.

=--

## Properties

The following proposition establishes that the concept of 'perfect stack' is robust in that various other roads would have led to the same destination.

+-- {: .un_def}
###### Definition

A [[stable (∞,1)-category]] $C$ is **compactly generated** if it has a [[small set]] $\{c_i\}_{i \in I}$ of [[compact object]] that are [[generator]]s in the sense that if for $N \in C$ we have that $C(c_i, N)$ is equivalent to the [[zero morphism]], then $N$ is the [[zero object]].

=--


+-- {: .un_theorem}
###### Proposition

For a [[∞-stack]] $X \in Sh_{(\infty,1)}(C)$ with affine diagonal, the following are equivalent:

* $X$ is perfect

* $QC(X)$ is 

  * compactly generated, 

  * and its [[compact object|compact]] and [[dualizable object|dualizable]] objects coincide.

=--


## Examples

Perfect stacks cover a broad array of spaces of interest, with notable exceptions being the ([[constant ∞-stack]] on a) [[classifying space]] $\mathcal{B}G$ of a [[topological group]] $G$ such as the [[circle]] $S^1 \simeq \mathcal{B} \mathbb{Z}$ or the classifying spaces of most [[algebraic group]]s in non-zero [[characteristic]]. This is because if $X$ is perfect, then the [[global section]]s functor $\Gamma$ must preserve colimits, which fails when the global sections $\Gamma(X, \mathcal{O}_X)$ of the structure sheaf is 'too large', as in the previous cases.

But the following are examples of perfect $\infty$-stacks

* quasi-compact [[derived scheme]]s with affine diagonal;

* the total space of a quasi-projective morphism over a perfect base;

* a quasi-projective [[derived scheme]];

* the quotient $X/G$ of a quasi-projective [[derived scheme]] $X$ by a linear action of an affine group (for $k$ of [[characteristic]] 0).



## References

The concept of a _perfect stack_ in the context of [[dg-geometry]] is considered in

* [[David Ben-Zvi|Ben-Zvi]], [[John Francis]],  [[David Nadler]], _Integral transforms and Drinfeld centers in derived algebraic geometry_ ([arXiv](http://arxiv.org/abs/0805.0157))
{#Ben-ZviFrancisNadler}


[[!redirects perfect infinity-stacks]]
[[!redirects perfect ∞-stack]]
[[!redirects perfect ∞-stacks]]