
#Contents#
* table of contents
{:toc}

## Idea

There is a [[little site]] notion of Zariski topology, and a [[big site]] notion. As for the little site notion: the Zariski topology on the set of prime ideals of a commutative ring $R$ is the smallest topology that contains, as open sets, sets of the form $\{p\; \text{prime}: a \notin p\}$ where $a$ ranges over elements of $R$. 

As for the big site notion, the _Zariski topology_ is a [[coverage]] on the [[opposite category]] [[CRing]]${}^{op}$ of commutative rings. This article is mainly about the big site notion. 

## Definition

For $R$ a commutative [[ring]], write $Spec R \in CRing^{op}$ for its [[spectrum of a commutative ring]], hence equivalently for its incarnation in the [[opposite category]].

+-- {: .num_defn #StandardOpenImmersion}
###### Definition

For $S \subset R$ a [[multiplicative subset]], write $R[S^{-1}]$ for the corresponding [[localization of a ring|localization]] and 

$$
  Spec(R[S^{-1}]) \longrightarrow Spec(R)
$$

for the dual of the canonical ring homomorphism $R \to R[S^{-1}]$.

=--

+-- {: .num_remark}
###### Remark

The maps as in def. \ref{StandardOpenImmersion} are not [[open immersion of schemes|open immersions]] for arbitrary multiplicative subsets $S$ (see [a MathOverflow discussion](http://mathoverflow.net/questions/20782/ring-theoretic-characterization-of-open-affines)). They are for subsets of the form $S = \{ f^0, f^1, f^2, \ldots \}$, in which case they are called the _standard opens_ of $Spec(R)$.

=--

+-- {: .num_defn}
###### Definition

A family of [[morphisms]] $\{Spec A_i \to Spec R\}$ in $CRing^{op}$ is a Zariski-[[covering]] precisely if 

* each ring $A_i$ is the [[localization]]

  $$
    A_i = R[r_i^{-1}]
  $$

  of $R$ at a single element $r_i \in R$ 

* $Spec A_i \to Spec R$ is the canonical inclusion, dual to the canonical ring homomorphism $R \to R[r_i^{-1}]$;

* There exists $\{f_i \in R\}$ such that

  $$
    \sum_i f_i r_i = 1
    \,.
  $$

=--

+-- {: .num_remark}
###### Remark

Geometrically, one may think of

* $r_i$ as a function on the [[space]] $Spec R$;

* $R[r_i^{-1}]$ as the [[open subset]] of points in this space on which the function is not 0;

* the covering condition as saying that the functions form a [[partition of unity]] on $Spec R$.

=--

+-- {: .num_defn #ZariskiTopos}
###### Definition

Let $CRing_{fp} \hookrightarrow CRing$ be the [[full subcategory]] on [[finitely presented object]]s. This inherits the Zariski [[coverage]].

The [[sheaf topos]] over this [[site]] is the [[big topos]] version of the  **Zariski topos**.


=--

## Properties

### Points

The [[maximal ideal]] in $R$ correspond precisely to the [[closed subset|closed]] points of the [[prime spectrum]] $Spec(R)$ in the Zariski topology.

### As a site

+-- {: .num_prop}
###### Proposition

The Zariski coverage is [[subcanonical coverage|subcanoncial]].

=--

+-- {: .num_prop}
###### Proposition


* $CRing_{fp}^{op}$ is the [[syntactic category]] of the [[cartesian theory]] of commutative rings;

* $CRing_{fp}^{op}$ equipped with the Zariski topology is the [[syntactic site]] of the [[geometric theory]] of [[local ring]]s.

Hence 

* the big Zariski topos, def. \ref{ZariskiTopos}, is the [[classifying topos]] for [[local ring]]s.

* a [[locally ringed topos]] is equivalently a topos $\mathcal{E}$ equipped with a [[geometric morphism]] into the big Zariski topos.

=--

See [[classifying topos]] and [[locally ringed topos]] for more details on this.

## Kripke&#8211;Joyal semantics
 {#KripkeJoyal}

Writing $R \models \varphi$ for the interpretation of a formula $\varphi$ of the [[internal language]] of the big Zariski topos over $Spec(R)$ with the [[Kripke–Joyal semantics]], the forcing relation can be expressed as follows.

$$
\begin{array}{lcl}
  R \models x = y : F &\Longleftrightarrow&
    x = y \in F(R). \\
  R \models \top &\Longleftrightarrow&
    1 = 1 \in R. \\
  R \models \bot &\Longleftrightarrow&
    1 = 0 \in R. \\
  R \models \phi \wedge \psi &\Longleftrightarrow&
    R \models \phi \,\text{and}\, R \models \psi. \\
  R \models \phi \vee \psi &\Longleftrightarrow&
    \text{there is a partition}\, \sum_i f_i = 1 \in R \,\text{such that for all}\, i,
      R[f_i^{-1}] \models \phi \,or\, R[f_i^{-1}] \models \psi. \\
  R \models \phi \Rightarrow \psi &\Longleftrightarrow&
    \text{for any}\, R\text{-algebra}\, S \,\text{it holds that}\, (S \models \phi) \,implies\, (S \models \psi). \\
  R \models \forall x:F. \phi &\Longleftrightarrow&
    \text{for any}\, R\text{-algebra}\, S \,\text{and any element}\, x \in F(S) \,\text{it holds that}\, S \models \phi[x]. \\
  R \models \exists x.F. \phi &\Longleftrightarrow&
    \text{there is a partition}\, \sum_i f_i = 1 \in R \,\text{such that for all}\, i,
    \text{there exists an element}\, x_i \in F(R[f_i^{-1}]) \,\text{such that}\,
    R[f_i^{-1}] \models \phi[x_i].
\end{array}
$$

The only difference to the Kripke&#8211;Joyal semantics of the _little_ Zariski topos is that in the clauses for $\Rightarrow$ and $\forall$, one has to restrict to $R$-algebras $S$ of the form $S = R[f^{-1}]$.

## Related concepts

[[fpqc-site]] $\to$ [[fppf-site]] $\to$ [[syntomic site]] $\to$ [[étale site]] $\to$ [[Nisnevich site]] $\to$ **Zariski site**

* [[spectrum of a commutative ring]]

## References

Examples A2.1.11(f) and D3.1.11 in

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
 {#Johnstone}

Section VIII.6 of 

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_
 {#MacLaneMoerdijk}

* [[The Stacks Project]], chapter 33 _Topologies on Schemes_

* Nick Duncan, _Gros and Petit Toposes_, talk notes, [88th Peripatetic Seminar on Sheaves and Logic](http://cheng.staff.shef.ac.uk/pssl88/), [pdf](http://cheng.staff.shef.ac.uk/pssl88/pssl88-duncan.pdf).

category: algebraic geometry
[[!redirects Zariski topology]]
[[!redirects Zariski topos]]
[[!redirects big Zariski topos]]

[[!redirects Zariski sheaf]]
[[!redirects Zariski sheaves]]

[[!redirects Zariski descent]]

[[!redirects theory of local rings]]
[[!redirects geometric theory of local rings]]