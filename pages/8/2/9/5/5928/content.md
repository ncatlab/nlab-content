
#Contents#
* table of contents
{:toc}

## Idea

The _Zariski topology_ is a [[coverage]] on the [[opposite category]] [[CRing]]${}^{op}$ of commutative rings.

## Definition

For $R$ a commutative [[ring]], write $Spec R \in CRing^{op}$ for its incarnation in the [[opposite category]].

+-- {: .un_defn}
###### Definition

A family of morphisms $\{Spec A_i \to Spec R\}$ in $CRing^{op}$ is a Zariski-[[covering]] precisely if 

* each ring $A_i$ is the [[localization]]

  $$
    A_i = R[s_i^{-1}]
  $$

  of $R$ at a single element $r_i \in R$ 

* $Spec A_i \to Spec R$ is the canonical inclusion, dual to the canonical ring homomorphism $R \to R[s_i^{-1}]$;

* There exists $\{f_i \in R\}$ such that

  $$
    \sum_i f_i r_i = 1
    \,.
  $$

=--

+-- {: .num_remark}
###### Remark

Geometricall, one may think of

* $r_i$ as a function on the [[space]] $Spec R$;

* $R[r_i^{-1}]$ as the [[open subset]] of points in this space on which the function is not 0;

* the covering condition as saying that he functions form a [[partition of unity]] on $Spec R$.

=--

+-- {: .num_defn #ZariskiTopos}
###### Definition

Let $CRing_{fp} \hookrightarrow CRing$ be the [[full subcategory]] on [[finitely presented object]]s. This inherity the Zariski [[coverage]].

The [[sheaf topos]] over this [[site]] is the [[big topos]] version of the  **Zariski topos**.


=--

## Properties

+-- {: .un_prop}
###### Proposition

The Zariski coverage is [[subcanonical coverage|subcanoncial]].

=--

+-- {: .un_prop}
###### Proposition

Then 

* $CRing_{fp}^{op}$ is the [[syntactic category]] of the [[cartesian theory]] of commutative rings;

* $CRing_{fp}^{op}$ equipped with the Zariski topology is the [[syntactic site]] of the [[geometric theory]] of [[local ring]]s.

Hence the big Zariski topos, def. \ref{ZariskiTopos}, is the [[classifying topos]] for local rings.

A [[locally ringed topos]] is equivalently a topos $\mathcal{E}$ equipped with a [[geometric morphism]] into the big Zariski topos.

=--

See [[classifying topos]] and [[locally ringed topos]] for more details on this.

## Related concepts

* [[fppf site]], [[fpqc site]], [[étale site]]

## References

Examples A2.1.11(f) and D3.1.11 in

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

[[!redirects Zariski topology]]
[[!redirects Zariski topos]]
[[!redirects big Zariski topos]]

[[!redirects theory of local rings]]
[[!redirects geometric theory of local rings]]